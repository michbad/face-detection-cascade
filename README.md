# Face detection cascade
Face detection using a cascade of boosted simple classifiers. Implemented from the Viola, Jones paper ["Rapid Object Detection using a Boosted Cascade of Simple Features"](https://www.cs.cmu.edu/~efros/courses/LBMV07/Papers/viola-cvpr-01.pdf).

Vectorized NumPy code makes it pretty fast. In particular the function `best_split_fast` calculates the value of each split in a vectorized way, which seems to do around 10x speedup over a for loop.

Unfortunately, this still gives a lot of false positives. Longer training time and incorporating other types of simple features would probably help that. Also, there should be a better way to pick among overlapping detected windows.



