Sure, here's your revised `README.md`:

````markdown
# Power Analysis with Python

This repository provides Python scripts to perform simple static power analysis. It is especially useful for determining the necessary sample size given a certain effect size, alpha level, and power. It can also be used to calculate the achieved power given effect size, sample size, and alpha level.

## Getting Started

These instructions will help you set up this project on your local machine.

### Prerequisites

The code uses the following Python libraries:

- statsmodels

### Installing

To clone the repository to your local machine, use:

```shell
git clone https://github.com/franc703/static_power_analysis.git
```
````

Then, navigate to the project directory:

```shell
cd static_power_analysis
```

Now, you can use the scripts with Python. You can also copy the examples from this file.

## Usage

### Calculating Sample Size

The following script calculates the required sample size for a given effect size, alpha level (significance level), and power:

```python
import statsmodels.stats.power as smp

# Define parameters
effect_size = 0.5  # Replace with your value
alpha = 0.05  # Replace with your value
power = 0.8  # Replace with your value

# Calculate sample size
sample_size = smp.TTestIndPower().solve_power(effect_size, power=power, alpha=alpha)

print(f"The required sample size is: {round(sample_size)}")
```

Ensure to replace the values for `effect_size`, `alpha`, and `power` with your specific values.

### Calculating Power

The following script calculates the achieved power given effect size, sample size, and alpha level:

```python
import statsmodels.stats.power as smp

# Define parameters
effect_size = 0.5  # Replace with your value
alpha = 0.05  # Replace with your value
sample_size = 100  # Replace with your value

# Calculate power
power = smp.TTestIndPower().solve_power(effect_size, nobs1=sample_size, alpha=alpha)

print(f"The achieved power is: {power}")
```

Again, replace the values for `effect_size`, `alpha`, and `sample_size` with your specific values.

## Authors

- **Rodrigo Franco** - _Initial work_ - [franc703](https://github.com/franc703)

```

```
