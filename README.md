
## Download data
```bash
docker build -t amithapa/download_data:download_data_0.1 .
docker push amithapa/download_data:download_data_0.1
```

## Decision Tree
```bash
docker build -t amithapa/download_data:decision_tree_0.1 .
docker push amithapa/download_data:decision_tree_0.1
```

## Logistic Regression
```bash
docker build -t amithapa/download_data:logistic_regression_0.1 .
docker push amithapa/download_data:logistic_regression_0.1
```


## Show result
```python
from kfp.components import func_to_container_op

@func_to_container_op
def show_results(decision_tree : float, logistic_regression : float) -> None:
    # Given the outputs from decision_tree and logistic regression components
    # the results are shown.
    
    print(f"Decision tree (accuracy): {decision_tree}")
    print(f"Logistic regression (accuracy): {logistic_regression}")
```

### Reference
- [Blog](https://towardsdatascience.com/kubeflow-pipelines-how-to-build-your-first-kubeflow-pipeline-from-scratch-2424227f7e5)