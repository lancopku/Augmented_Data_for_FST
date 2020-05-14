# Augmentd_Data_for_FST
This the augmented data of our paper "Parallel Data Augmentation for Formality Style Transfer".
## Augmented Parallel Data
### Back Translation
We augment a total of 1.6M sentence pairs by back translation strategy.

We use the original parallel data to train a seq2seq model in the formal-to-informal direction. Then we feed formal sentences to this model to generate sentences that are supposed to be informal. The formal input and the informal output sentences can be paired to establish augmented parallel data. The formal sentences identified by our formality discriminator are from the E\&M and F\&R domain on [Yahoo Answers L6](https://webscope.sandbox.yahoo.com/catalog.php).

### Formality Discrimination
We augment a total of 1.5M sentence pairs by formality discrimination strategy. 

We first collect a number of potentially informal English sentences and then translate them into a pivot language (e.g., French) by [Google Translation](https://translate.google.com/) and translate them back into English. In this way, each sentence obtains a rewritten version and they composes a sentence pair. The pairs where the rewritten sentence largely improves the formality of the original sentence will be selected as the augmented data. The informal sentences used in F-Dis strategy are also from Yahoo Answers L6 corpus. We use French, German and Chinese as pivot languages.

### Multi-task Transfer
We augment a total of 1.8M sentence pairs by multi-task transfer strategy.

We use the public GEC data (Lang-8 and NUCLE) as our augmented data. 

## Contact
Feel free to contact me (`zhangyi16@pku.edu.cn`) if you have any questions:)

## Cite
If you use this data or code for your research, please cite the following paper:
```
  @inproceedings{zhang2020parallel,  
  author = {Zhang, Yi and Tao, Ge and Sun, Xu},  
  title = {Parallel Data Augmentation for Formality Style Transfer},  
  booktitle = {ACL 2020},  
  year = {2020}  
  }  
 ```
