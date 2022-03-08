# Metric Card for Perplexity

## Table of Contents
- Metric Description(#metric-description)
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
Causal language models learn to generate text by iteratively predicting the next output token, using the previously generated tokens as context. The last step of each prediction consists of selecting one token from a probability distribustion over all of the tokens in the vocabulary. Note that this probability distribution depends on the context (i.e. the previously generated tokens).

Given a causal lanugage model and a snippet of text, perplexity is calculated by walking through the snippet token by token, pulling 

**To still mention:**
- lower is better
- hard to evaluate language in general
- add some language theory context
- note that score will depend on what the model's trained on
- mention pseudoperplexity for masked LMs

### Possible Values
- 0 and up (TO DO: double check if includes 0 or not)
- lower is better

### Requires Reference/'ground truth'?
no

### Supported Tasks and Leaderboards
- any lanugage generation task
- leaderboards: no (right??)

### Languages Supported
- any language for which there is both a trained model and data available to evaluate on

## Metric Use
### Inputs
### Outputs
### Examples

## Considerations for Using the Metric
### Social Impact of the Metric
### Discussion of Biases
### Other Known Limitations
- isn't bounded above
- isn't comparable between models or datasets
- 
### Reproducibility Considerations
- stride

## Mathematical Foundations
- oh boy
### Equation(s)
### Mathematical Context
### Additional Resources

## Metric Creation?? (find title for this!)
### Curation Rationale
### Source Data (if applicable)
### Related Metrics (if applicable)

## Additional Information
### Licensing Information
### Citation Information
### Contributions