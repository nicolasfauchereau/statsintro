.. image:: ..\Images\title_discrete.png
    :height: 100 px

.. Test on Discrete data

Data can be discrete for different reasons. On is that you acquired them in a
discrete way (e.g. levels in a questionnaires.) Another one is that your
paradigm only gives discrete results (e.g. rolling a dice). For the analysis of
such data, we can build on the tools that we have already covered in the
previous chapters.

Tests on Ordinal Data
---------------------

Ordinal data have clear rankings, e.g. "none - little - some - much - very
much". However they are not continuous. For the analysis of such *rank
ordered data* we can use rank order methods for the analysis:

- Two groups
    When comparing two rank ordered groups, we can use the *Mann-Whitney test* 

- Three or more groups
    When comparing two rank ordered groups, we can use the *Kruskal-Wallis test*


Binomial Test
~~~~~~~~~~~~~

.. index:: tests-binomial

Example
^^^^^^^

Suppose we have a board game that depends on the roll of a die and attaches
special importance to rolling a 6. In a particular game, the die is rolled 235
times, and 6 comes up 51 times. If the die is fair, we would expect 6 to come up
235/6 = 39.17 times. Is the proportion of 6's significantly higher than would be
expected by chance, on the null hypothesis of a fair die?

To find an answer to this question using the *Binomial Test*, we consult
the binomial distribution with n=235 and p=1/6, to determine the probability of
finding exactly 51 sixes in a sample of 235 if the true probability of rolling a
6 on each trial is 1/6. We then find the probability of finding exactly 52,
exactly 53, and so on up to 235, and add all these probabilities together. In
this way, we calculate the probability of obtaining the observed result (51 6s)
or a more extreme result (>51 6's) assuming that the die is fair. In this
example, the result is 0.0265443, which indicates that observing 51 6's is
unlikely (significant at the 5\% level) to come from a die that is not loaded to
give many 6's (one-tailed test).

Clearly a die could roll too few sixes as easily as too many and we would be
just as suspicious, so we should use the two-tailed test which (for example)
splits the 5\% probability across the two tails.

|python| `binomialTest.py <https://github.com/thomas-haslwanter/statsintro/blob/master/Code3/binomialTest.py>`_

Exercises
---------

#. Under which conditions do you use the *binomial distribution* to
   evaluate the likelihood of a discrete number of events? And under which
   do you use the *Poisson distribution* ?


.. |ipynb| image:: ../Images/IPython.jpg
    :scale: 50 % 

.. |python| image:: ../Images/python.jpg
    :scale: 50 % 
