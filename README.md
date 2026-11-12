# GekkGo models

The models the GekkGo app downloads: small files that let Gekk understand what a driver says and answer on the phone, with nothing sent to a server.

| Folder | What it is | Status |
| --- | --- | --- |
| `voice/` | The reader: turns a sentence into one of the app's 33 jobs ("take me to...", "avoid tolls"). 792 KB. | Published, version 1.0.0 |
| `voice/guide/` | Gekk's spoken voice for directions and answers: Supertonic 2, ten voices, runs on the phone. 96 MB. | Published, version 1 |
| `hearing/` | Speech to words on the phone. | Planned |
| `brain/` | Answers in Gekk's own words. | Planned |

Each folder has a `manifest.json` with the version, the download address, the size in bytes and the SHA-256 of the file. The app checks the hash before it uses a download and keeps its built-in copy if anything does not match.

Large files are attached to Releases, not stored in the repository.
