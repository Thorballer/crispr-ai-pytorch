# CRISPR AI — PyTorch research prototype

A PyTorch/XLA implementation of the sequence-and-effect-to-mutation model, with grouped-query/windowed attention code, SwiGLU feed-forward layers, CNN sequence downsampling, and bucketed data loading.

## Notebooks

- [science-fair-states-torch.ipynb](notebooks/science-fair-states-torch.ipynb) — [original Kaggle notebook](https://www.kaggle.com/code/thorballer/science-fair-states-torch)
- [multi-gpu-gene-dataset-parsing.ipynb](notebooks/multi-gpu-gene-dataset-parsing.ipynb) — [original Kaggle notebook](https://www.kaggle.com/code/thorballer/multi-gpu-gene-dataset-parsing)

Start with `science-fair-states-torch`; `multi-gpu-gene-dataset-parsing` handles preprocessing. Training targets TPU/XLA and needs external bucketed data and tokenizers. This is a modeling prototype, not biologically validated genome editing.

## Running

Open the original Kaggle notebook, attach its referenced data/models, choose the hardware expected by its setup cells, and run cells in order. Review install, login, and file-writing cells first.

For local use, install `requirements.txt` and adapt `/kaggle/input` paths. Dependencies are inferred from imports, not a tested lockfile; older APIs may need adjustment.

### Referenced Kaggle datasets

- [thorballer/all-uniprot-isodata](https://www.kaggle.com/datasets/thorballer/all-uniprot-isodata)
- [thorballer/bucketed-ds](https://www.kaggle.com/datasets/thorballer/bucketed-ds)
- [thorballer/teach-modelparse](https://www.kaggle.com/datasets/thorballer/teach-modelparse)

### Referenced Kaggle models/tokenizers

- `thorballer/dna-mutations-tokenizers/TensorFlow2/default/4`

## Status and source

These exports have no saved execution outputs. Training was not rerun, so this archive reports no benchmark scores.

Daniel Goldberg's Kaggle notebooks have source links and hashes in [PROVENANCE.json](PROVENANCE.json). Comments and formatting were cleaned up without changing executable logic or saved outputs; unedited copies are linked in the provenance record.

Credits and tutorial links are retained. Datasets and dependencies have their own licenses; no new blanket license is assigned. Architecture reference: [TensorFlow Transformer tutorial](https://www.tensorflow.org/text/tutorials/transformer).
