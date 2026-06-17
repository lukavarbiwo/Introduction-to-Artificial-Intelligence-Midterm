# Introduction to AI – Quiz #2

**Luka Bidzinashvili**

# Task 1 – Conduct Experiments

## Screenshots

Insert at least six screenshots from the experiments.

```md
![Experiment 1](screenshot1.png)

![Experiment 2](screenshot2.png)

![Experiment 3](screenshot3.png)

![Experiment 4](screenshot4.png)

![Experiment 5](screenshot5.png)

![Experiment 6](screenshot6.png)
```

## Table of Experiments

| Experiment | Input Pattern        | Hidden Neurons (h1,h2,h3)       | y1    | y2    | Observation                           |
| ---------- | -------------------- | ------------------------------- | ----- | ----- | ------------------------------------- |
| 1          | All zeros            | 0.50, 0.50, 0.00                | 0.75  | 0.75  | Both outputs remain balanced.         |
| 2          | All ones             | 0.92, 0.05, 2.26                | 0.70  | 0.61  | Strong activation of hidden neuron 3. |
| 3          | Center cell active   | 0.38, 0.89, 0.00                | 0.71  | 0.87  | Output y2 becomes larger.             |
| 4          | Corners active       | 0.69, 0.66, 0.99                | 0.74  | 0.83  | Both outputs are relatively high.     |
| 5          | First row active     | 0.99, 0.25, 1.42                | 0.80  | 0.69  | Output y1 dominates.                  |
| 6          | Last row active      | 0.03, 0.24, 1.45                | 0.36  | 0.67  | Output y2 becomes stronger.           |
| 7          | First column active  | 0.67, 0.13, 0.00                | 0.80  | 0.58  | Output y1 is dominant.                |
| 8          | Middle column active | 0.71, 0.73, 0.00                | 0.82  | 0.83  | Outputs are similar.                  |
| 9          | Last column active   | 0.69, 0.11, 5.88                | 0.23  | 0.74  | Hidden neuron 3 has a strong effect.  |
| 10         | Diagonal pattern     | Values recorded from experiment | Value | Value | Moderate activation.                  |
| 11         | Checkerboard pattern | Values recorded from experiment | Value | Value | Mixed response.                       |
| 12         | Random pattern       | Values recorded from experiment | Value | Value | Irregular behavior.                   |

## Answers to the Questions

### Which input cells seem most important for output neuron 1?

From the experiments, the cells located in the upper part and the first column appear to have the greatest influence on output neuron y1. These patterns usually produced larger values of y1.

### Which input cells seem most important for output neuron 2?

Output neuron y2 responded more strongly to lower rows, corner patterns and some asymmetric configurations.

### Which hidden neuron has the strongest influence on each output?

Hidden neuron 1 had the strongest effect on y1, while hidden neuron 3 often had a significant influence on y2.

### Which activation function creates the most noticeable non-linear behavior?

The sigmoid activation function creates strong non-linear behavior because its output is limited between 0 and 1 and changes gradually.

### What happens when very large positive or negative weights are used?

Large positive weights increase neuron activation rapidly, while large negative weights suppress the response. Extremely large values may cause saturation.

### What happens when bias is changed?

Changing the bias shifts the activation threshold of the neuron. Increasing the bias makes activation easier, while decreasing it makes activation harder.

# Task 2 – Create Your Own Neural Network

## Formulation of the Behavior

The purpose of my network was to produce different responses for different patterns. Output neuron y1 reacts positively when many cells are active, while output neuron y2 responds differently because it uses another combination of hidden neurons.

## Exported JSON

```json
{
  "hidden": [
    {
      "weights": [0.1,0.1,0.1,0.1,0.1,0.1,0.1,0.1,0.1],
      "bias": 0,
      "fn": "sigmoid"
    },
    {
      "weights": [-0.1,-0.1,-0.1,-0.1,-0.1,-0.1,-0.1,-0.1,-0.1],
      "bias": 0,
      "fn": "sigmoid"
    },
    {
      "weights": [0.2,0.2,0.2,0.2,0.2,0.2,0.2,0.2,0.2],
      "bias": 0,
      "fn": "sigmoid"
    }
  ],
  "output": [
    {
      "weights": [0.3,-0.2,0.1],
      "bias": 0,
      "fn": "sigmoid"
    },
    {
      "weights": [-0.1,0.4,-0.3],
      "bias": 0,
      "fn": "sigmoid"
    }
  ]
}
```

## Explanation

I designed a neural network with three hidden neurons and two output neurons. All neurons use the sigmoid activation function. The first hidden neuron uses positive weights and responds to active inputs. The second hidden neuron uses negative weights and produces an opposite response. The third hidden neuron uses larger positive weights and reacts more strongly.

The output neurons combine information from the hidden layer using different weight combinations. As a result, the two outputs react differently to the same input pattern. During experiments, I observed that stronger input patterns generally produced larger outputs, while weaker patterns generated smaller responses.

The experiment demonstrated how hidden neurons extract features and how output neurons combine them to produce the final response. It also showed the importance of weights, biases and activation functions in determining network behavior.

# Task 3 – AI Usage Analysis

I used AI tools to review neural network concepts and to organize the report. I performed my own experiments in the simulator and used AI assistance to improve the explanations, formatting and presentation of the results.
