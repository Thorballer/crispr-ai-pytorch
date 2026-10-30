# CRISPR AI — PyTorch research prototype

A PyTorch/XLA implementation of the sequence-and-effect-to-mutation model, with grouped-query/windowed attention code, SwiGLU feed-forward layers, CNN sequence downsampling, and bucketed data loading.

## Project status

Historical notebooks from Daniel Goldberg’s Kaggle account, organized for a maker portfolio. The model code is preserved, not rewritten during packaging. See [PROVENANCE.json](PROVENANCE.json) for original notebook URLs, timestamps, and SHA-256 hashes.

## Notebooks

- [science-fair-states-torch.ipynb](notebooks/science-fair-states-torch.ipynb) — [original Kaggle notebook](https://www.kaggle.com/code/thorballer/science-fair-states-torch)
- [multi-gpu-gene-dataset-parsing.ipynb](notebooks/multi-gpu-gene-dataset-parsing.ipynb) — [original Kaggle notebook](https://www.kaggle.com/code/thorballer/multi-gpu-gene-dataset-parsing)

## Running

Use the original Kaggle environment where possible: open the source notebook, attach its declared datasets/models, select the hardware expected by its setup cells, and run cells in order. Inspect any install, account-login, upload, or filesystem-changing cells before executing them.

For a local adaptation, install the packages listed in `requirements.txt` in an isolated environment and adjust `/kaggle/input` paths. Those packages are inferred from imports, **not** a tested lockfile. Historical APIs and accelerator assumptions can require changes. Do not run all training notebooks at once.

### Referenced Kaggle datasets

- [thorballer/all-uniprot-isodata](https://www.kaggle.com/datasets/thorballer/all-uniprot-isodata)
- [thorballer/bucketed-ds](https://www.kaggle.com/datasets/thorballer/bucketed-ds)
- [thorballer/teach-modelparse](https://www.kaggle.com/datasets/thorballer/teach-modelparse)

### Referenced Kaggle models/tokenizers

- `thorballer/dna-mutations-tokenizers/TensorFlow2/default/4`

## Results and limitations

CRISPR AI is the portfolio project label, not a claim of experimentally validated genome editing. The training notebook targets TPU/XLA and requires external bucketed shards and tokenizers. Data parsing is a supporting preprocessing notebook. No biological efficacy or independently reproduced accuracy is claimed.

The recovered Kaggle source exports contain no retained executed outputs; this repository therefore does not advertise a numeric result based on notebook titles or training settings. Training was not rerun as part of organization. Structural validation is not a runtime or scientific validation.

## Attribution and rights

Original notebook attribution, comments, and tutorial links are preserved. Standard TensorFlow/Keras examples and tutorial-style code should not be represented as newly invented algorithms. The precise human/AI/tool contribution history is not reconstructed by this archive. No blanket new license is assigned to third-party material. Datasets, pretrained models, and tutorial-derived content retain their own licenses and access requirements; their bytes are not bundled here.

The attention/encoder-decoder organization includes TensorFlow tutorial-style components; see the [TensorFlow Transformer tutorial](https://www.tensorflow.org/text/tutorials/transformer) for the standard architecture pattern. This is an attribution reference, not a verified line-by-line authorship audit.
