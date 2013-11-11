Note that: - There are trained crf-s (i.e. tcrf-s) in the directory bin.
           - If the accuracy value is 100% this means that the correspon-
           ding label has been "locked"
           - Latest_Labeled_Data3 contains the data with the highest 
           accuracy. All the tcrf-s (results from training the CRF) and
           model-s (result from training the svm) reside in this folder
           as well. See the README file.
           -TrainingSwitchedUnfrag contains the files used for training.

Explanation of the abbreviations used for naming the folders:
- WL        - wire-label classification
- GL        - gate-label classification
- WG        - wire-gate classification
- 3COMBO*   - means that we are doing the classifications above
            one at a time and later on we combine them using the 
            voting approaches (see "State of reasearch" in AntonBakalovLog)
- LOCKING/LOCKED - means that we have tested locking labels (see "State of 
            reasearch" in AntonBakalovLog)
- LOGMESSAGES - means that we use the log of the messages in the 
            inference algorithm - loopy bp (see the RunCRF documentation 
            on the wiki)
- PRODPROF  - means that we use max product and the product of the messages
            in the inference algorithm - loopy bp (see the RunCRF documentation 
            on the wiki)
- SUMSUM    - means that we are using the sum of the messages in the 
            inference algorithm - loopy bp(see the RunCRF documentation on the 
            wiki)
- GNG       - gate-nongate classification
- LNL       - label-nonlabel classification
- WNW       - wire-nonwire classification
- FRAG      - means that the sketches are fragmented
- INPUT-MULTIPASS - this folder contains the sketches used for labeling. 
- NEWFEATURES - means that we are testing feature functions using information
            regarding the strokes labeled as gates. For example, 
            NEWFEATURES-NO-minDist-touching-arePar-arePerp-penLift-GATE-maxDist-minDist-arePar-strcombo
            means that we are using all feature functions except for the ones 
            after NO in the name of the folder; also the feature functions
            after GATE are the ones using information regarding the strokes 
            labeled as gates during the first stage of the multipass recog-
            nition.

Example of the naming convention that I used:
OUTPUT-PART OF MULTIPASS-WL-No-SquareInkDensity-TwoCorn-TB(site)-MinTimeSmallLar-CSSC(inter)
The name of the folder tells us that we are doing a wire-label recognition as part of the
multipass recognition. We have used all site feature functions except for SquareInkDensity, 
TwoCorners, DistTB. Also we have used all interaction feature functions except for 
MinTimeSmall, MinTimeLarge, CS_TJxn, and SC_TJxn.
