# motion-magnification-project
### Asma Boukhdhir & Edgard Dabier

In this repository, we experiment with a **learning-based motion magnification** method introduced by [Tae-Hyun Oh et al.](https://people.csail.mit.edu/tiam/deepmag/), and implemented in PyTorch by [ZhengPeng7](https://github.com/ZhengPeng7/motion_magnification_learning-based).

ZhengPeng7 provides a Google Collab including his implementation of the learning-based motion magnification model in PyTorch, allowing us to use the pretrained model to magnify the motion of any given input video and by specifying the `magnification factor`.

We started by familliarizing with the code, and experimenting with several input videos, and then we conducted the following tests:

- Comparison with the state of the art **phase-based method**:
    The goal was to qualitatively mesure the difference between the results obtained with the phase-based method and the learning-based method. In fact, the paper only presents visual comparison between the two, but no rigorous metrics comparison was performed, so we chose to conduct this comparison.
- Testing the effect of different **temporal filters** and **magnification factors** on the resulting output video to verify what the authors stated as limitations of their model:
    The paper introduces as limitations of their model the degraded perceptual quality of videos obtained by applying high magnification factors on small motion videos and after adding temporal filtering on it. It is important to note that we couldn't access *groundtruht* data with information about the actual quantity of motion inside the videos, we had to rely on hand made videos.

We recall that the actual video magnification was covered by ZhengPeng7 in his collab file, our work focuses on testing and experimenting with it. We selected the videos we wanted to magnify for our tests (inside the `video` folder), and we used a custom version of ZhengPeng7's collab  [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)]([https://colab.research.google.com/drive/1inOucehJXUAVBlRhZvo650SoOPLKQFNv#scrollTo=BjgKRohk7Q5M](https://colab.research.google.com/drive/1dATor77-4c_L4jbWcFrPxMF64WdHG_Xh#scrollTo=FUX3pb77Axr0))

The resulting magnified videos can be found in the `res-videos` folder, classified by sequences (`grass`, `sea_view`, `custom`).

The file `Learning-based Video Motion Magnification.pdf` contains the slides for the method presentation. The slides contain a bunch of animated gifs that are not always displayed correctly depending on the pdf redear one might use, so we suggest using Acrobat Reader.
