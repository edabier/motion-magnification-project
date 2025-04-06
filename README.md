# motion-magnification-project
### Asma Boukhdhir & Edgard Dabier

In this repository, we experiment with a **learning-based motion magnification** method introduced by [Tae-Hyun Oh et al.](https://people.csail.mit.edu/tiam/deepmag/), and implemented in PyTorch by [ZhengPeng7](https://github.com/ZhengPeng7/motion_magnification_learning-based).

ZhengPeng7 provides a Google Colab including his implementation of the learning-based motion magnification model in PyTorch, allowing us to use the pretrained model to magnify the motion of any given input video and by specifying the `magnification factor`.

We started by familliarizing with the code, and experimenting with several input videos, and then we conducted the following tests:

- Comparison with the state of the art **phase-based method**:

    The goal was to quantitatively measure the difference between the results obtained with the phase-based method and the learning-based method. In fact, the paper only presents visual comparison between the two,  but no rigorous metrics comparison was performed,except for noise robustness, so we chose to compare the **SSIM** and **BRISQUE** metrics for both methods. We have also conducted a comparison of the power spectral density spectrum of the magnified videos resulting from the two methods

The notebook created to perform this phase based magnification and metrics computation is the `Phase-based-Motion-Magnification.ipynb` file

  
- Testing the effect of different **temporal filters** and **magnification factors** on the resulting output video to verify what the authors stated as limitations of their model:
  
    The paper introduces as limitations of their model the degraded perceptual quality of videos obtained by applying high magnification factors on small motion videos and after adding temporal filtering on it. It is important to note that we couldn't access the *groundtruth* data with information about the actual quantity of motion inside the videos, we had to rely on hand-made videos that we magnified and filtered. Then, we compared the two results visualy and quantitatively (by computed the SSIM score compared to the original video).

The notebook created to perform this temporal filtering is the `temporal-filtering.ipynb` file

We recall that the actual video magnification was covered by ZhengPeng7 in his colab file, our work focuses on testing and experimenting with it. We selected the videos we wanted to magnify for our tests (inside the `videos` folder), and we used a custom version of ZhengPeng7's colab  [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1bTgyQ2WSEB7uruf7g_kLDAFNXzvHiSEX?usp=sharing)

The resulting magnified videos can be found in the `res-videos` folder, classified by sequences (`grass`, `sea_view`, `custom` - the `guitar` sequence was used directly inside the `Phase-based-Motion-Magnification.ipynb` file to perform metrics computation).

The file `Learning-based Video Motion Magnification.pdf` contains the slides for the method presentation (*flipped classroom*). The slides contain a bunch of animated gifs that are not always displayed correctly depending on the pdf redear one might use, so we suggest using Acrobat Reader.
