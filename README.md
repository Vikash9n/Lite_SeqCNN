# Lite_SeqCNN+
This reprository is for Lite-SeqCNN+.

To run the python script, follow the code example given in the folder Example.
This has following main python files.


  1. Evaluate.py - This python file contains the code for the evaluation metrics used.
  2. Lite_SeqCNN_encoder.py - This contains the code for the construction of the posterior probability (output).
  3. Lite_SeqCNN_plus.py - This contains the code for the ensemble model.
  4. Segmentation.py - This python file contains the code for segmentation fo the protein sequences used for training the segment encoder.


Experimental Setups:-->

Step 1:--> Creating a segmented dataset

        This will allow creating a fixed-sized segments for the protein sequence. Execute the Segmenation.py .
        
Step 2:--> Training the segmented encoder

        This is two steps:-
        
        (i) Creating a tokenized segments (i.e., a string of n-mers)
        
        (ii) Train the dilated CNN-based architecture.
        
        For this, execute the Lite_SegCNN_encoder.py.

This trained segmented encoder is later used with the LiteSeqCNN+.
Implementing LiteSeqCNN+ :-->

This is an ensemble PFP framework based on multiple segment-size. i.e., (200,300,400).
The steps are as follows:
(1) Train segment encoder with the different segment size.


The dataset are available at gdrive: https://bit.ly/3EMJhLx
