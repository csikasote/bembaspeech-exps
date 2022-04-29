# DeepSpeech-Bemba-Model
This repository contains resources (dataset and notebooks) for reproducing experiments in the <a href="https://arxiv.org/pdf/2102.04889.pdf">BembaSpeech: A Speech Recognition Corpus for the Bemba Language</a>.

## Citation

Please consider citing as follows if you use part of the code or data in your work or project:

    @inproceedings{sikasote-anastasopoulos21bembaspeech,
        abstract = {We present a preprocessed, ready-to-use automatic speech recognition corpus, BembaSpeech, consisting over 24 hours of read speech in the Bemba language, a written but low-resourced language spoken by over 30% of the population in Zambia. To assess its usefulness for training and testing ASR systems for Bemba, we train an end-to-end Bemba ASR system by fine-tuning a pre-trained DeepSpeech English model on the training portion of the BembaSpeech corpus. Our best model achieves a word error rate (WER) of 54.78%. The results show that the corpus can be used for building ASR systems for Bemba.},
        title = {BembaSpeech: A Speech Recognition Corpus for the Bemba Language},
        author = {Sikasote, Claytone and Anastasopoulos, Antonios},
        booktitle = {Proceedings of AfricaNLP},
        address = {Online},
        month = {April},
        year = {2021},
        url = {https://arxiv.org/pdf/2102.04889.pdf}
    }


## Experimental Setup
In this project we used the [DeepSpeech v0.8.2](https://deepspeech.readthedocs.io/en/v0.8.2/) release for our experiments. We refer the reader to [Mozilla DeepSpeech](https://github.com/mozilla/DeepSpeech) for latest updates.

## Resources
### Dataset
The data used in this project is a portion of the [BembaSpeech](https://github.com/csikasote/BembaSpeech) corpus consisting of audio files whose size is not more than 10 seconds as per DeepSpeech input pipeline requirement.

<div class="tg-wrap"><table>
<thead>
  <tr>
    <th> ID </th>
    <th>Dataset</th>
    <th>CSV file</th>
    <th>No. of Utterances</th>
    <th>Size</th>
    <th>Description</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td> 1 </td>
    <td><a href="https://drive.google.com/drive/folders/1LAb04Ylj8gPIJ1p5w2AnmUgDuAuuUifO?usp=sharing">training</a></td>
    <td><a href="https://drive.google.com/file/d/1tdUgGJnjOoI5JTNMJ5M4uDsH1eS-DgLb/view?usp=sharing">train.csv</a></td>
    <td>10200</td>
    <td>14hrs, 20min</td>
    <td>Used for training</td>
  </tr>
  <tr>
    <td> 2 </td>
    <td><a href="https://drive.google.com/drive/folders/1hGo5yJJy57hg0tShGdCLjHW0aEP-1iVO?usp=sharing">development</a></td>
    <td><a href="https://drive.google.com/file/d/1tbHiMEV9lcNjFzb1DfcPDe0gpU9QzZEq/view?usp=sharing">dev.csv</a></td>
    <td>1437</td>
    <td>2hrs</td>
    <td>Used for validation</td>
  </tr>
  <tr>
    <td> 3 </td>
    <td><a href="https://drive.google.com/drive/folders/1843to0yTW5xsLu_PIvJ_qAt9JnWIclDg?usp=sharing">testing</a></td>
    <td><a href="https://drive.google.com/file/d/1tXdBlQIpMf2aAks0kzsfpClpXXmBT7bX/view?usp=sharing">test.csv</a></td>
    <td>756</td>
    <td>1hr, 18min</td>
    <td>Used for testing</td>
  </tr>
</tbody>
</table></div>

### Language Model

To create the language model for our experiments, we used two sets of Bemba text; transcript (from train and dev sets) denited as [LM1]() and a combination of transcripts and JW300 denoted as [LM2](). 

You can run and follow the [notebook](https://github.com/csikasote/BembaASR/blob/main/notebooks/N_gram_LM.ipynb) which provides the step by step process of creating different N-gram language models using KenLM tool.

## Notebooks
In the [notebooks](https://github.com/csikasote/BembaASR/tree/main/notebooks) folder, you will find notebooks used in the training of the DeepSpeech Bemba ASR model. 
* [lm.ipynb](https://github.com/csikasote/BembaASR/blob/main/notebooks/N_gram_LM.ipynb) - used to create the N-gram language models
* [baseline.ipynb](https://github.com/csikasote/BembaASR/blob/main/notebooks/base_line.ipynb) - used to train the baseline for our experiments
* [ft_model.ipynb](https://github.com/csikasote/BembaASR/blob/main/notebooks/ft_model.ipynb) - used to finetune DeepSpeech English pretrained model without inclusion of language model.
* [ftune_5glm_trans.ipynb](https://github.com/csikasote/BembaASR/blob/main/notebooks/ftune_5glm_trans.ipynb) - used to finetune DeepSpeech\`s English pretrained model with inclusion of the 5-gram LM (from LM1 Bemba text) scorer.

## Results
You can download the models (both [acoustic](https://drive.google.com/file/d/166Qo55ZI9rufZjhnBX0-93Jal9jwxxXB/view?usp=sharing) and [scorer](https://drive.google.com/file/d/10Hk7dpY89ciIF_BD8M6Y1fm__OiUQ69y/view?usp=sharing)) that achieved the best results 54.78%.
