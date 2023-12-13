# SNN-467-final



To install the dependencies, do the following

conda create -n snn467f

pip install notebook

python -m pip install brian2

conda install numpy 

conda install matplotlib 

conda install scikit-learn



Pytorch should also be installed based on your specific setup. 



Due to randomized initializations, the generated results could be different from the results reported in the report. A noisier dataset generated in rnn-f1 will also negatively influence the performance of the SNN model by a lot. The performance of SNN could also possibly be a lot better than the results listed in the report, that the performance of the SNNs could be very similar to SMAs and the RNN. The variance of the model performance is really big, unlike the RNN and SMAs. Test MSE for the SNN model ranges from 780 to 7000 as I have tested, and the range could be bigger. 

---

Running cells in rnn-f1.ipynb will generate:

- train_labels.pt, test_labels.pt

- raw_train_seqs.pt, raw_test_seqs.pt
- rnn_h_train.pt, rnn_h_test.pt (not used later because it's saturated for most data points)

The above data would be useful for the SNN model in snn-brian2.ipynb. 

An RNN will be trained, and SMA could be tested on the dataset. 

Table 1 and Figure 1. 

---

Running cells in snn-brian2 sequentially will generate results for Table 2 and Table 3.

The code looks messy because there are problems accessing network parameters if the code of simulation and network initialization are handled in functions. 