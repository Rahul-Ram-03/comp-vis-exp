### img-seg-transunet
Basically, the idea is to combine local info. encoding capabilities of a CNN and global info. encoding capabilties of a transformer. Inspiration from [this paper](https://arxiv.org/abs/2102.04306). Uses the Oxford-IIIT pet dataset.


### img-to-latex-eq
Takes in an image of a handwritten equation and generates the appropriate LaTex representation of the image. Trained using the CROHME-2023 dataset. Uses a resnet50 model (or atleast some of its layers) for feature extraction; the resnet50 layers that were used are all frozen.. Extracted features are sent through a convolution layer to combine patch extraction and positional encoding in a single step. The patches are then sent through a transformer encoder; that output is then sent through a transformer decoder alongside the target equation.

A custom regex-based tokenizer was used with a "vocabulary" of about 113 basic symbols used by LaTex