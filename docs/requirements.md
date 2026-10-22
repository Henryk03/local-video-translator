
# Software Requirements Specification

## 1. Introduction

### 1.1 Purpose

The purpose of this document is to define the functional and non-functional requirements of `local-video-translator`, a desktop application that transcribes the spoken content of video and audio files, translate the resulting transcript into a target language, and lets users ask questions about the transcription's content. The system is designed with privacy as a guiding principle: processing is performed locally by default. Optional remote model providers may be enabled by the user, and data leaves the user's device only after explicit, informed consent.

### 1.2 Scope

The system shall allow users to:

* Import video and audio files from their computer.
* Record audio directly within the application.
* Generate text transcriptions from spoken audio.
* Translate transcriptions into selected languages.
* Display original and translated text with timestamps.
* Export transcription and translation results.
* Access previously processed content.
* Configure the models used for each task, selecting from:
    * **Local models**, which run entirely on the user device (the default).
    * **Remote models**, which are accessed through an external service and which the user must explicitly enable.

For remote models, the system shall:

* Be disabled by default, with no data sent until the user enables a provider.
* Require explicit user consent per provider, stating what data will be sent.
* Show a clear indicator whenever a task is being processed remotely.
* Allow the user to switch back to local processing at any time.
* Store any user-supplied credentials (e.g. API keys) securely on the device.

For audio recorded within the application, the system shall:

* List the available microphones that can be used for recording.
* Apply the same transcription and translation workflow as for imported files.

The system shall not require user registration or authentication to use the application. Users who choose a remote provider may need to supply their own credentials for that provider.

### 1.3 Out of Scope

* Hosting, operating or billing for remote model services.

### 1.4 Intended Users

The application is intended for individuals who need to understand spoken content in video or audio recordings, including student, researchers and language learners.

User are expected to have basic computer literacy, but shall not be required to have programming knowledge.