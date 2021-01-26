# General Language Understanding Evaluation (GLUE)

The General Language Understanding Evaluation (GLUE) benchmark
is a collection of NLP tasks that is widely used in NLP research.

GLUE tasks are described at [here](https://gluebenchmark.com/tasks).

GLUE's paper is uploaded in this repo named `glue.pdf`.

## How to download GLUE data

Before preceding to process the GLUE data, there are several points
worth to mention.

* As we discussed in the MRPC repo, users need to download MRPC raw dataset
in order to created the reorganized MRPC dataset used in DL models.
* Although SQuAD is one of the GLUE tasks, its processing is not included
in the GLUE script. Users need to download SQuAD themselves.

The steps are

1. Download and process MRPC. See the MRPC [README](https://github.com/magsail/MRPC).

2. Make sure root of MRPC and GLUE are in the same directory, otherwise
you have to change the path in `download_glue_data.zsh` accordingly.

3. Run `download_glue_data.zsh`

4. Run `download_squad11_data.zsh` in `SQuAD_v1.1`

5. Run `download_squad20_data.zsh` in `SQuAD_v2.0`

## MRPC

In `./GLUE/glue_data/MRPC`, there are multiple files created by the script in step 3
above.

* `dev.tsv`: 408 entries selected from `msr_paraphrase_train.txt` according to `dev_ids.tsv`.
* `dev_ids.tsv`: Downloaded from google's site (see `download_glue_data.py`).
* `test.tsv`: 1725 entries from `msr_paraphrase_test.txt` with labels changed to indexes (Not sure why for now.)
* `train.tsv`: 3668 entries selected from `msr_paraphrase_train.txt` which are excluded from `dev_ids.tsv`.
* `vocab.txt`: the vocabulary file that BERT is trained on.

`train.tsv` + `dev.tsv` = `msr_paraphrase_train.txt`

## SQuAD 1.1


## SQuAD 2.0
