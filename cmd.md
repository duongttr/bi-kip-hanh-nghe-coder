# Combine multiple files into zip (tar) file while there's not enough storage
I'm a person who works with Google Colab and Kaggle notebook a lot, and sometimes I need to save a folder with a hundred (and even a thousand) of large files but it is almost out-of-storage, and it's easy to solve this problem, *divide-and-conquer* by below simple Python code:
```python
import os

list_dir = os.listdir('<your_folder_path>')
for d in list_dir:
  !tar --append -f '<your_tar_file>.tar' $d
  !rm -rf $d
```
