# Striding finding the Longest Word
Find the longest word (and its length) from a text file. Works considerably fast that a linear search by striding through each line and splitting it into chunks no smaller than the current found longest word, then testing these chunks.

For example:
    "This is an example of a line from the corpus"
    'supercalifragilisticexpialidocious'

The program finds 'This' to be the longest word, then strides forward to check 'is an', but finds a space so it cannot be the longest word. 'example' is then checked, which becomes the longest word, then 'of a line' is checked and discarded, then 'from the corpus' is checked and discarded.

If there are previous lines and 'supercalifragilisticexpialidocious' is the current longest word then this line is split into 'This is an example of a line from the' and 'corpus'. The former chunk is checked, but there is a space so it is discarded. The latter fragment is discarded because it is too short. In this case only 9 characters need to be compared ('the ' and 'This ') because of striding (instead of each character in the line). 