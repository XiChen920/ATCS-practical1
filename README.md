# ATCS-practical1

# Universal Sentence Representations
This project experiments with different ways to learn universal sentence representations. Four different neural models are implemented to encode sentences. These models are trained on the Stanford Natural Language Inference corpus to classify sentence pairs based on their relation. The learned sentence representations are evaluated using the SentEval framework. 
![](architectures.png)

## Project Organization
The project is organized as follows:
* models ..................................................... Model Architectures
* checkpoints/ ............................................ Trained Models
* results/ ..................................................... Experiment Logs
* trainer.py ................................................. Training Logic
* utils.py ..................................................... Utilities
* main.py .................................................... Run Experiments
* demo.ipynb .............................................. Demo \& Analysis    

## How to run?
1. use python3.9 and down load lib mentioned
2. Download the pre-trained checkpoints from [Google Drive]
3. Install [SentEval](https://github.com/facebookresearch/SentEval) 
4. Run the demonstration and analysis notebook: [demo.ipynb](.demo.ipynb)
5. To run our experiments:
```
python3 main.py --config=configs.baseline --train=True --test=True
```
6. To design your own experiment, use the configuration dictionaries in the configs directory as follows:
```
config = {
        'exp_name': 'experiment_1',
        'debug': True,
        'seed': 42,
        'batch_size': 64,
        'epochs': 10,
        'device': 'cuda' if torch.cuda.is_available() else 'cpu',
        'learning_rate': 0.001,
        'model_type': 'UniLSTM',
        'hidden_dim': 256,
        'embeddings_path': 'C:\\Users\\win11\\PycharmProjects\\pythonProject\\glove.840B.300d.txt',
        'embedding_dim': 300
    }
```
