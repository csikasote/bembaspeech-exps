# BembaASR-Model
This repository contains the resources (dataset, code and scripts) for reproducing experiments in the [BembaSpeech: A Speech Recognition Corpus for the Bemba Language]().

## Experimental Setup
In this project we used the [DeepSpeech v0.8.2]() release for our experiments. We refer the reader to [Mozilla DeepSpeech]() for latest updates.

## Resources
### Dataset
The data used in this project was obtained from the [BembaSpeech]() corpus. It consist of audio files whose size is not more than 10 seconds as per DeepSpeech input pipeline requirement.

<div class="tg-wrap"><table>
<thead>
  <tr>
    <th> ID </th>
    <th>Datasets</th>
    <th>Associated CSV file</th>
    <th>Definition</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td> 1 </td>
    <td><a href="https://drive.google.com/drive/folders/1LAb04Ylj8gPIJ1p5w2AnmUgDuAuuUifO?usp=sharing">Training</a></td>
    <td><a href="https://drive.google.com/file/d/1tdUgGJnjOoI5JTNMJ5M4uDsH1eS-DgLb/view?usp=sharing">train.csv</a></td>
    <td>Used for training</td>
  </tr>
  <tr>
    <td> 2 </td>
    <td><a href="https://drive.google.com/drive/folders/1hGo5yJJy57hg0tShGdCLjHW0aEP-1iVO?usp=sharing">Development</a></td>
    <td><a href="https://drive.google.com/file/d/1tbHiMEV9lcNjFzb1DfcPDe0gpU9QzZEq/view?usp=sharing">dev.csv</a></td>
    <td>Used for validation</td>
  </tr>
  <tr>
    <td> 3 </td>
    <td><a href="https://drive.google.com/drive/folders/1843to0yTW5xsLu_PIvJ_qAt9JnWIclDg?usp=sharing">Testing</a></td>
    <td><a href="https://drive.google.com/file/d/1tXdBlQIpMf2aAks0kzsfpClpXXmBT7bX/view?usp=sharing">test.csv</a></td>
    <td>used for testing</td>
  </tr>
</tbody>
</table></div>

### Language Model
The 5-gram LM used in this experiment was created using default parameter values of DeepSpeech v0.8.2
* [lm.binary](https://drive.google.com/file/d/109a1poTnPpYf-ILQlsIRC44QHh_kaXBX/view?usp=sharing)
* [kenlm.scorer](https://drive.google.com/file/d/10Hk7dpY89ciIF_BD8M6Y1fm__OiUQ69y/view?usp=sharing)
* [vocabulary.txt](https://drive.google.com/file/d/109svD1u4ShzxaTWvtlXY4Bzr1gMjIreU/view?usp=sharing)

### Acoustic Model
* [ft_5glm_model.pbmm](https://drive.google.com/file/d/166Qo55ZI9rufZjhnBX0-93Jal9jwxxXB/view?usp=sharing)
* [ft_5glm_model.pb](https://drive.google.com/file/d/165Azk-mOduV3DTraxZFZqBOlFhcF_NCi/view?usp=sharing)
