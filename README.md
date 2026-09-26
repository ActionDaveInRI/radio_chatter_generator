# Radio chatter generator

Browser experiments in synthesized radio conversations, environmental context, and locally generated dialogue.

## Start here

[Open main build](https://actiondaveinri.github.io/radio_chatter_generator/tts_09.html) · [Choose a version](https://actiondaveinri.github.io/radio_chatter_generator/index.html) · [All projects](https://github.com/ActionDaveInRI/spaceship/blob/main/PROJECTS.md)

Choose the no-model 09 build for a simpler start, or explore the spaceflight and language-model variants.

## Run it

Open the version chooser and select a build, then press Start Simulation. Versions 06, 08, and 09 use browser speech synthesis without a language-model download. The LLM and hybrid variants import Transformers.js and download a model; internet access and browser compatibility are required. For local use, serve the repository over HTTP using the command below.

From inside this repository's folder, with Python 3 installed:

```sh
python3 -m http.server 8000 --bind 127.0.0.1
```

Then open <http://127.0.0.1:8000/>. On Windows, `py -m http.server 8000 --bind 127.0.0.1` is the equivalent command. Stop the server with Ctrl+C.

## Builds and files

| Build | File | Purpose |
|---|---|---|
| 09 · refined chain replies | [tts_09.html](tts_09.html) | Environmental context and refined replies; browser speech synthesis, without a language-model download. |
| Spaceflight · labeled stable | [tts_09_b_lm-02_hybrid-recursive-SF_stable.html](tts_09_b_lm-02_hybrid-recursive-SF_stable.html) | Spaceflight hybrid using Xenova/gpt2. “Stable” is the original filename label, not a new compatibility certification. |
| Spaceflight · DialoGPT experiment | [tts_09_b_lm-02_hybrid-recursive-SF_DIA.html](tts_09_b_lm-02_hybrid-recursive-SF_DIA.html) | Requests microsoft/DialoGPT-medium through Transformers.js; retained as an experiment. |
| Spaceflight · hybrid | [tts_09_b_lm-02_hybrid-recursive-SF.html](tts_09_b_lm-02_hybrid-recursive-SF.html) | Spaceflight context with the GPT-2 hybrid generator. |
| Hybrid · enhanced context memory | [tts_09_b_lm-02_hybrid-recursive.html](tts_09_b_lm-02_hybrid-recursive.html) | Context-memory variation on the hybrid generator. |
| Hybrid | [tts_09_b_lm-02_hybrid.html](tts_09_b_lm-02_hybrid.html) | Combined scripted and language-model radio generation. |
| LLM · minimal prompts | [tts_09_b_lm-02.html](tts_09_b_lm-02.html) | Ultra-minimal radio prompting experiment. |
| LLM · debug | [tts_09_b_lm.html](tts_09_b_lm.html) | Tuned language-model simulation with debugging output. |
| 08 · environment and mood | [tts_08.html](tts_08.html) | Environment, day/night, and character-influenced moods; no model download. |
| 06 · conversation chains | [tts_06.html](tts_06.html) | Earlier multi-user conversation-chain simulation; no model download. |

The file links in this table show source on GitHub. Use the launch links above to run a build.

## Keeping this organized

Keep the documented starting build on `main`. Record changes with a short description of what changed; use named Git milestones (tags) for future checkpoints instead of adding another numbered copy. Preserve existing historical file paths, and update this guide when the launch path changes. Independent experiments can use a clearly named folder or branch.
