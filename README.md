# How to download GLUE data

GLUE has multiple tasks. The user needs to download and process MRPC
before download and process GLUE data.

1. Download and process MRPC. See the MRPC README.

2. Make sure root of MRPC and GLUE are in the same directory, otherwise
you have to change the path in `download_glue_data.zsh` accordingly.

3. Run `download_glue_data.zsh`

4. Run `download_squad11_data.zsh` in `SQuAD_v1.1`

5. Run `download_squad20_data.zsh` in `SQuAD_v2.0`
