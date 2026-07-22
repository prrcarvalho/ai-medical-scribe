# Clinical Documentation

This context describes the language used by the AI medical scribe from consultation capture through clinician-approved documentation.

## Language

**Emergency Episode**:
The participating clinician's bounded period of urgent-care responsibility for one patient, within which multiple timestamped Clinical Diaries may be created while the clinician also attends other patients. It ends when that clinician no longer needs to follow the patient because care has ended or responsibility has passed elsewhere.
_Avoid_: Encounter, session, case

**Episode Closure**:
The clinician-confirmed end of an Emergency Episode when the participating clinician no longer expects to assess that patient, whether because of discharge, admission under another team, or formal transfer of responsibility. Closure marks the Episode `Concluído` but does not approve or discard unfinished Clinical Diaries.
_Avoid_: Medical discharge when referring to every possible closure outcome

**Clinical Diary**:
One timestamped clinical-documentation artifact within an Emergency Episode, prepared for clinician review, approval, and manual copying into the organisation's clinical-record system. It records the assessment and intended next steps at that point rather than replacing the episode's earlier entries; the pt-PT product term is `Diário clínico`.
_Avoid_: Encounter, episode

**Draft Clinical Diary**:
A generated or edited Clinical Diary that the clinician has not yet explicitly approved. It cannot become inherited context for a later Clinical Diary.
_Avoid_: Approved Clinical Diary, trusted history

**Deferred Clinical Diary**:
A Draft Clinical Diary deliberately saved as `Por concluir` so the clinician can handle other work and resume it later. Its recordings, context, and labels persist, but it holds no active recording and remains excluded from inherited context, even if its Emergency Episode has been closed.
_Avoid_: Closed diary, approved diary

**Approved Clinical Diary**:
The clinician-approved version of a Clinical Diary, eligible for manual copying and for inheritance as chronological context by later Clinical Diaries in the same confirmed Emergency Episode.
_Avoid_: Draft, generated diary

**Diary Amendment**:
An explicitly timestamped correction or addendum linked to an Approved Clinical Diary after approval or copying. It preserves the original rather than silently overwriting it.
_Avoid_: Silent edit, replacement diary

**Recording**:
A clinician-controlled audio source for a Clinical Diary, composed of one or more ordered Recording Segments. Pausing or interruption does not create a separate Recording.
_Avoid_: Audio file, segment

**Consultation Recording**:
A Recording captured during the clinician-patient interaction. It may contain multiple speakers and provides evidence of what was discussed or observed aloud.
_Avoid_: Post-consultation Recording, transcript

**Post-consultation Recording**:
A clinician-only Recording captured after the patient interaction. It may contain objective findings, differential diagnoses, uncertainty, interpretation, and plans that were not spoken during the consultation.
_Avoid_: Private Wrap-up, summary, plan recording

**Recording Segment**:
One uninterrupted, persisted interval of audio within a Recording. Pausing or interruption ends the current segment; resuming creates the next segment while preserving the gap.
_Avoid_: Recording, continuous stream

**Record Context Block**:
A timestamped block of clinical-record content pasted by the clinician into the scribe as an explicit source. It is attached either to the Emergency Episode as baseline context or to the Clinical Diary where it was added, retains its provenance, and remains distinguishable from recordings and model-generated content.
_Avoid_: Recording transcript, model suggestion

**Episode Baseline Context**:
Reusable Record Context Blocks, such as relevant antecedents, usual medication, and allergies, attached to a confirmed Emergency Episode and made available to every later Clinical Diary in that Episode.
_Avoid_: Diary-specific results, longitudinal patient record

**Episode Confirmation**:
The clinician's deliberate verification that the Emergency Episode in the scribe corresponds to the patient record currently open in the clinical-record system. Anonymous capture and draft generation may precede it, but confirmation is required before copying a Clinical Diary or adding a later Clinical Diary that inherits Episode context.
_Avoid_: Automatic patient matching

**Episode Identifier**:
The stable, episode-specific identifier issued by an organisation's clinical-record system and copied into the scribe as the primary identity anchor for an Emergency Episode.
_Avoid_: Patient name, patient-level record number

**Provisional Episode Label**:
An editable, unconfirmed display label inferred from audio or pasted context to help the clinician recognise anonymous work. It has no authority to confirm Episode identity.
_Avoid_: Episode Identifier, confirmed patient identity

**Clinical-record system**:
The organisation-controlled system that holds the official patient record; SClínico is one possible example, not the product boundary.
_Avoid_: SClínico when referring to clinical-record systems generally
