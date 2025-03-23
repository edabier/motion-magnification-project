# motion-magnification-project
### Asma Boukhdhir & Edgard Dabier

In this repository, we experiment with a **learning-based motion magnification** method introduced by [Tae-Hyun Oh et al.](https://people.csail.mit.edu/tiam/deepmag/), and implemented in PyTorch by [ZhengPeng7](https://github.com/ZhengPeng7/motion_magnification_learning-based).

ZhengPeng7 provides a Google Collab including his implementation of the learning-based motion magnification model in PyTorch, allowing us to use the pretrained model to magnify the motion of any given input video and by specifying the `magnification factor`.

We started by familliarizing with the code, and experimenting with several input videos, and then we conducted the following tests, that can be found in the `learning-based-motion-mag.ipynb`:

- Comparison with the state of the art **phase-based method**
- Testing the effect of different `temporal filters` and `magnification factors` on the resulting output video to verify what the authors stated as limitations of their model.

We recall that the actual video magnification was covered by ZhengPeng7 on his collab file, our work focuses on testing and experimenting with it, starting from the section **Comparison with the state of the art**.

We recommand using google Collab for this code to work properly.
