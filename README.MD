Author:  Steve North

License: AGPLv3 or later

License URI: http://www.gnu.org/licenses/agpl-3.0.en.html

Can: Commercial Use, Modify, Distribute, Place Warranty

Can't: Sublicence, Hold Liable

Must: Include Copyright, Include License, State Changes, Disclose Source

Copyright (c) 2019, The University of Exeter

ease_dog_facial_expression_estimation_deeplabcut_trained_neural_net

This is a neural network trained to predict the locations of facial landmarks in dogs (particuarly street dogs).

It is intended for us with the Open Source set of Python tools called DeepLabCut (http://www.mousemotorlab.org/deeplabcut), for analysing novel videos, producing an output video with labelled facial landmarks.

This network was trained using videography of street dogs from the University Of Exeter, UK, EASE Anthrozoology research group's 'Tails from the Streets' project (Using trans-species ethnography to document, understand and help mitigate the ‘stray dog problem’ in Europe: https://socialsciences.exeter.ac.uk/ease/research/tailsfromthestreets/ ) and also example video clips of Facial Action Units and Action Descriptors from the Dog Facial Action Coding System (DogFACS):

Waller, B. M., Peirce, K., Caeiro, C. C., Scheider, L., Burrows, A. M., McCune, S. & Kaminski, J. 2013. Paedomorphic Facial Expressions Give Dogs a Selective Advantage. PLOS ONE, 8, 12, p.e82686.  http://dx.doi.org/10.1371/journal.pone.0082686. 

Waller, B. M. 2017. Dog Facial Action Coding System (DogFACS) [Online]. Available: http://dogfacs.com [Accessed 21 July 2017].

The network might require further raining (with as few as 10 frames), when encountering novel dog video.

pose_cfg.yaml is the configuration file used in DeepLabCut to train and use this network.

The network itself consists of 3 files in the sub-directory 'snapshot': 

snapshot-38000.meta, snapshot-38000.index and snapshot-38000.data-00000-of-00001.

Training for this network ended at - Iteration: 38000 (actually total iterations are around 100,000, as the name counter restarts at 0 after each stop to adding new frames to training set etc.) loss: 0.0053 lr: 0.02

Ideal training would probably be: loss:  iteration: 200,000 loss: 0.0001

As a use-case, EASE_TAILS_dog_facial_analysis.gif is included. This is an animated gif showing a video generated using this network (lefthand side), with some additional analysis based on raw data, shown on the righthand side.