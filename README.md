# Qev local demo and notebook

This repository contains the Qev local decision playground and an experimental Colab notebook. It does not include model weights or provision a hosted runtime.

Before use, obtain authorization for the Qev checkpoint and matching Qwen base, and review their model cards, licenses, and your organization's requirements. Keep model files local; do not commit restricted weights. The local demo needs Python and sufficient RAM (or a supported GPU). Installing dependencies requires network access; inference runs from local files. Prepare a copy of the approved checkpoint, point its `model.json` `model_id` to the absolute path of the matching Qwen base, then run:

```sh
python -m pip install -r local/requirements.txt
python local/try_qev.py --checkpoint <local-checkpoint-directory>
```

Open `http://127.0.0.1:7861` on the same machine. The demo binds locally and does not create a public sharing link. The notebook is a template only: Colab runtime, credentials, GPU, model access, and dataset availability are not provisioned or verified. Check every setup cell and applicable terms before running it; this migration has not been run in Colab.

Outputs and retrospective examples are experimental and may be inaccurate. They are not validated operational decisions and must not be the sole basis for consequential or safety-critical actions. No production accuracy, latency, or cost claims are made.

## Benchmark comparison

See the [0.8B, 2B and 4B comparison tables](QEV-COMPARISON.md) for current validation results, disclosed gaps, and limitations.
