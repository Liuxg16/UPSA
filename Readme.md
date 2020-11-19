# UPSA
The source code is available at https://osf.io/xseuc/

# Data
The test sentences, generated sentences and the corresponding reference of the Quora dataset are in quora-results/


#Idea
![](sa.PNG)
# Requirement
python==2.7
cuda 9.0
## python packages
	nltk
	TensorFlow == 1.3.0
	numpy
	pickle
	Rake (pip install python-rake)
	zpar (pip install python-zpar, download model file from https://github.com/frcchang/zpar/releases/download/v0.7.5/english-models.zip and extract it to POS/english-models)
	

# run the code:
python source/run.py --exps_dir exps-sampling  --exp_name  test   --use_data_path data/quoradata/test.txt --mode kw-bleu  --N_repeat 1  --save_path sa.txt   --batch_size 1 --gpu 0  --search_size 50

## The sampling results may vary across different machines.


# evaluation script
python  source/evaluate.py --reference_path quora-results/ref.txt  --generated_path  quora-results/gen.txt

# Cite this paper
```bash
@inproceedings{UPSA,
title="Unsupervised Paraphrasing by Simulated Annealing",
author="Xianggen Liu, Lili Mou, Fandong Meng, Hao Zhou, Jie Zhou, Sen Song",
year = "2020",
booktitle="ACL"
}
```
