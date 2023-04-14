# Abstract

Stress is a widespread phenomenon that can lead not only to psychological but also to physical illnesses. Early detection of stress using machine learning techniques enables contributions to stress management and reduction, thereby improving the quality of life for affected individuals.

In the context of this master's thesis, an approach to stress detection based on a Time-Series Classification Transformer architecture (TSCT) was investigated, while the effects of Differential Privacy (DP) on model performance were evaluated. The results showed that the use of TSCTs is a promising way to detect stress in the WESAD dataset with high accuracy. The model achieved an average accuracy of 91.89 percent and an average F1 score of 91.61 percent. The application of DP allowed the protection of participants privacy but resulted in compromises in model performance, particularly in terms of precision. For the best-trained models with DP, accuracy losses of about 4 percent and an F1 score drop of approximately 25 percentage points were observed. The work also has some limitations, such as the lack of generalizability of the results, the interpretability of transformer models, and the practical applicability of the approach in real-world applications.

In summary, this master's thesis demonstrates the potential of TSCTs for stress detection and the application of DP for maintaining privacy, although the performance of private models and the relationship to the epsilon metric are difficult to assess.

# Dataset

The [`WESAD-Dataset`](https://dl.acm.org/doi/10.1145/3242969.3242985) is used to train and evaluate the model.


### Setup

1. Download the dataset [here](https://ubicomp.eti.uni-siegen.de/home/datasets/icmi18/) and save the WESAD directory inside the [`data directory`](https://github.com/BDegenkolb/Privacy-Preserving-Stress-Transformer/tree/main/data).

2. To train the Transformer-model follow the notebook for the [`Transformer-model`](https://github.com/BDegenkolb/Privacy-Preserving-Stress-Transformer/blob/main/code/transformer.ipynb).
  
  a) Run NeptuneAI cell if you want to use neptune ai, but don't forget to put your api token and project name in the "Hyperparameter" Cell
  
3. Use the [`AutomatedTransformer`](https://github.com/BDegenkolb/Privacy-Preserving-Stress-Transformer/blob/main/code/AutomatedTransformer.ipynb) to train one transformer after another in a loop.
