.. _loss_intro:

How losses work in PyTlc
==================================

Some of the trainers in PyTlc accept a loss parameter, which defines the loss (also know as loss function, objective function, or optimization score function) that will be used for training.

Losses can be specified either as a string or a loss object. Available losses are ``'exp'``, ``'hinge'``, ``'log'``, ``'poisson'``, ``'smoothed_hinge'``, ``'squared'``, and ``'tweedie'``. When loss is specified as one of these strings, the default values are used for the loss parameters. To change the default parameters, a loss object should be used, as seen in examples below.

Each trainer supports only a subset of the losses mentioned above. To get the supported losses and the default loss, please refer to the documentation page for the specific trainer.


Example of specifying loss as a string
----------------------------------------------

::

  from microsoftml_scikit.linear_model import SgdBinaryClassifier
  from microsoftml_scikit.linear_model import FastLinearBinaryClassifier

  trainer1 = SgdBinaryClassifier(loss='exp')
  trainer2 = FastLinearBinaryClassifier(loss='smoothed_hinge')


Example of specifying loss as an object of a loss class
----------------------------------------------

::

  from microsoftml_scikit.linear_model import SgdBinaryClassifier
  from microsoftml_scikit.linear_model import FastLinearBinaryClassifier
  from microsoftml_scikit.loss import Exp, SmoothedHinge
  
  trainer1 = SgdBinaryClassifier(loss=Exp()) # equivalent to loss='exp'
  trainer2 = SgdBinaryClassifier(loss=Exp(beta=0.4))
  trainer3 = FastLinearBinaryClassifier(loss=SmoothedHinge(smoothing_const=0.5))
  
Loss classes
==================================

`microsoftml_scikit.loss.Exp`
----------------------------------------------
.. autoclass:: microsoftml_scikit.loss.Exp

`microsoftml_scikit.loss.Hinge`
----------------------------------------------
.. autoclass:: microsoftml_scikit.loss.Hinge

`microsoftml_scikit.loss.Log`
----------------------------------------------
.. autoclass:: microsoftml_scikit.loss.Log

`microsoftml_scikit.loss.Poisson`
----------------------------------------------
.. autoclass:: microsoftml_scikit.loss.Poisson

`microsoftml_scikit.loss.SmoothedHinge`
----------------------------------------------
.. autoclass:: microsoftml_scikit.loss.SmoothedHinge

`microsoftml_scikit.loss.Squared`
----------------------------------------------
.. autoclass:: microsoftml_scikit.loss.Squared

`microsoftml_scikit.loss.Tweedie`
----------------------------------------------
.. autoclass:: microsoftml_scikit.loss.Tweedie
