# Gekk's hearing

Gekk's ears are two models that work together: a small streaming one (Zipformer, 73 MB) that shows the words as you speak, and an accurate one that hears the whole sentence and gives the final words. `manifest.json` lists what is used, what each scored, and what was tried and not chosen.

The accurate English model is NVIDIA's Parakeet TDT 0.6B v2 (int8), attached to the `hearing-v2` release. On 50 hard English sentences (LibriSpeech test-other) it made 2.56 % word errors clean and 3.48 % with engine and wind noise laid over the sentences, against 6 to 10 % and 9 to 14 % for Whisper small, and it runs several times faster. The scoring script is `tools/voice/asr_eval.py` in the app's repository.

A version tuned for UAE accents and place names is still to come.
