Original code available at:
http://www.ti.uni-tuebingen.de/Eye-Movements-Identification.1845.0.html?&L=1
(Matlab implementation)

################################################################################
# LICENSE
################################################################################

Copyright (c) 2016, University of Tübingen

Permission to use, copy, modify, and distribute this software and its
documentation for non-commercial purposes, without fee, and without a written
agreement is hereby granted, provided that the above copyright notice and this
paragraph and the following two paragraphs appear in all copies.

IN NO EVENT SHALL THE UNIVERSITY OF TÜBINGEN BE LIABLE TO ANY PARTY FOR DIRECT,
INDIRECT, SPECIAL, INCIDENTAL, OR CONSEQUENTIAL DAMAGES, INCLUDING LOST PROFITS,
ARISING OUT OF THE USE OF THIS SOFTWARE AND ITS DOCUMENTATION, EVEN IF
UNIVERSITY OF TÜBINGEN HAS BEEN ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.

UNIVERSITY OF TÜBINGEN SPECIFICALLY DISCLAIMS ANY WARRANTIES, INCLUDING, BUT NOT
LIMITED TO, THE IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A
PARTICULAR PURPOSE. THE SOFTWARE PROVIDED HEREUNDER IS ON AN "AS IS" BASIS, AND
UNIVERSITY OF TÜBINGEN HAS NO OBLIGATIONS TO PROVIDE MAINTENANCE, SUPPORT,
UPDATES, ENHANCEMENTS, OR MODIFICATIONS.



################################################################################
# CITATION
################################################################################

T. Santini, W. Fuhl, T. Kübler, E. Kasneci
Bayesian Identification of Fixations, Saccades, and Smooth Pursuits
ACM Symposium on Eye Tracking Research & Applications, ETRA 2016



################################################################################
# RUNNING
################################################################################

1) Adjust the dataset directory in setup.m

2) Run setup.m

3) You can then run IBDT on a single dataset, for instance subject six and first dataset, as:

run(datasetDir, groundTruth, target, '6/1');



################################################################################
# OUTPUT
################################################################################

As output you will get:

-A list of the frames that have been misclassified in the form

[idx] groundTruthLabel -> algorithmLabel (function:line)

-The confusion matrix

-The resulting accuracy (acc), precision (prec), recall (rec), and specificity (spec) for fixations (fix), saccades (sac), and smooth pursuits (pur)

-The classification file (classification.csv) in the dataset's directory in the form

idx , label , timestamp



################################################################################
# SPECIAL NOTES
################################################################################

Note that originally the labeling and output functions supported more movement classes: fixations, saccades, pursuits, noise, undefined, vestibulo-ocular reflexes, head movements, a place holder classification (tmp), and unknown labels (see ClassificationEnum).

This is no longer supported by the scripts, so labels may only contain fixations, saccades, pursuits, and noise.

