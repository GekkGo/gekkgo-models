# Gekk's brain

The model the GekkGo app downloads so Gekk can answer in his own words on the phone. `manifest.json` lists the models; the app takes the largest one that fits the phone's memory (`minRamMb`), checks its SHA-256, and downloads it from the release named in `url`.

| Version | File | Size | Notes |
| --- | --- | --- | --- |
| 2 | `gekk-brain-0.5b-v2.task` (release `brain-v2`) | 541 MB | Qwen 2.5 0.5B Instruct tuned for GekkGo: tool calls (weather, lookup, FAQ) and answers from the facts the app gives it. |

How it is made: the data generators, training, scoring and conversion scripts are in `tools/brain` in the GekkGo app repository. A phone with less memory than a model needs gets no brain: commands, weather, lookups and search still work.
