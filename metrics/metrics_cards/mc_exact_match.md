# Metric Card for Exact Match

## Table of Contents
- Metric Description
    - Metric Summary
        - Possible Values
        - Requires Reference/'ground truth'?
    - Supported Tasks and Leaderboards
    - Possible Values
    - Languages Supported
- Metric Use
    - Inputs
    - Outputs
    - Examples
- Considerations for Using the Metric
    - Social Impact of the Metric
    - Discussion of Biases
    - Other Known Limitations
    - Reproducibility Considerations
- Mathematical Foundations
    - Equation(s)
    - Mathematical Context
    - Additional Resources
- Metric Creation?? (find title for this!)
    - Curation Rationale
    - Source Data (if applicable)
    - Related Metrics (if applicable)
- Additional Information
    - Licensing Information
    - Citation Information
    - Contributions

---

## Metric Description
- **Homepage:**
- **Repository:**
- **Paper:**
- **Point of Contact:**


## Metric Summary
A given predicted string's exact match score is 1 if it is the exact same as its reference string, and is 0 otherwise.

- Example 1: The exact match score of prediction "Happy Birthday!" is 0, given its reference is "Happy New Year!".
- Example 2: The exact match score of prediction "The Colour of Magic (1983)" is 1, given its reference is also "The Colour of Magic (1983)".

The exact match score of a set of predictions is the sum of all of the individual exact match scores in the set, divided by the total number of predictions in the set.

- Example: The exact match score of the set {Example 1, Example 2} (above) is 0.5.


### Possible Values
**Individual Examples:** Exact match scores of individual examples (i.e. (prediciton, reference) pairs) can be either 0 or 1.

**Sets of Examples:** Exact match scores of sets of examples can be any number from 0 to 1, inclusive.

### Do the examples require 'ground truth' references?
Yes. The exact match requires an input 'ground truth' reference for each input prediction.

## Supported Tasks and Leaderboards
**Tasks:** Any task where two strings are compared.

**Leaderboards:** None.

## Languages Supported
All lanugages are supported, as long as there is a 'ground truth' reference to compare each input against.

## Metric Use
** TO FINALIZE WHEN CODE IS FINALIZED **
### Inputs
- characters/strings to ignore:
    - this paper ignores punctuation and articles if they're different (https://web.stanford.edu/class/archive/cs/cs224n/cs224n.1174/reports/2761899.pdf)
        - e.g. "the cat sat!" and "a cat sat." would be marked as exact matches, with a score of 1
### Outputs
### Examples

## Considerations for Using the Metric

### Social Impact of the Metric
- works better with good data, good data is often more likely to appear for groups/cases/instances with more resources

### Discussion of Biases

### Other Known Limitations
This metric is limited in that it outputs the same score for something that is completely wrong as for something that is correct except for a single character. In other words, there is no award for being *almost* right.


### Reproducibility Considerations
When using this metric, it is important to record the following metric-specific information, in addition to general library, model, device, and dataset information (that should be noted no matter which metric you are using), so that your work can be replicated in the future:

1. Which characters and strings are ignored when comparing predictions and references


## Mathematical Foundations
### Equation(s)
$
\text{score} = \frac{\sum_{(p,r)\in N}{match(p,r)}}{\lvert N\rvert}
$
where $N$ is the set of examples, $ \lvert N\rvert $ is the total number of examples, and $match(p,r) = 1$ if the prediction ($p$) and reference ($r$) in a given example are exact matches, and $match(p,r) = 0$ if they are not.

### Mathematical Context
- N/A ?
### Additional Resources

## Metric Creation?? (find title for this!)
### Curation Rationale
### Source Data (if applicable)
### Related Metrics (if applicable)
- accuracy

## Additional Information
### Licensing Information
### Citation Information
### Contributions