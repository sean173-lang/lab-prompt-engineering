# Prompt Engineering Lab — Summary

## 1. Objective

The goal of this lab was to improve the reliability, consistency, and accuracy of AI-generated responses through different prompt engineering techniques.

Three tasks were tested:
- Sentiment Analysis
- Product Description Generation
- Data Extraction

## 2. Prompt Engineering Techniques

**Version 1 — Basic Prompting**

Simple instructions without strict output requirements. Responses varied in wording, formatting, and structure.

**Version 2 — Structured Prompting**

Added explicit instructions, output constraints, and formatting requirements to improve consistency.

**Version 3 — Advanced Prompting**

Used few-shot examples and structured instructions to improve classification, content generation, and data extraction.

## 3. Results

| Task | V1 Exact-Match Consistency | V2 Compliance | V3 Compliance |
|---|---|---|---|
| Sentiment Analysis | 26.7% | 100% | 100% |
| Product Description | 6.7% | 100% | 100% |
| Data Extraction | 20.0% | 100% | 100% |

Results are based on 15 runs per version. V1 exact-match consistency and V2/V3 compliance measure different things and should not be interpreted as directly comparable accuracy scores.

## 4. Testing Different Inputs

| Task | Results |
|---|---|
| Sentiment Analysis | 9/9 correct (100%) |
| Product Description | 5/5 format compliant (100%) |
| Data Extraction | 4/5 correct (80%) |

## 5. Failures and Limitations

**Sentiment Analysis:** Basic prompts produced inconsistent labels and explanations. Explicit output constraints and few-shot examples improved consistency.

**Product Description:** Although V3 consistently followed formatting requirements, it sometimes generated unsupported claims about product features, including ergonomic design, comfort, and precision. Formatting compliance did not guarantee factual accuracy.

**Data Extraction:** One test failed because the model returned "quickly" instead of the expected normalized value "fast". This demonstrated the importance of defining normalization rules.

An initial variation test also failed because of a string-replacement error in the test code. After correcting the test, the model achieved 80% accuracy.

## 6. Key Learnings

- Clear output constraints improve response consistency.
- Few-shot examples help demonstrate the desired output.
- Structured instructions can improve extraction reliability.
- Testing multiple inputs is necessary to evaluate generalization.
- Consistent formatting does not guarantee factual accuracy.
- Normalization rules should be explicitly defined.
- Automated testing helps identify weaknesses in both prompts and evaluation code.

## 7. Conclusion

This lab demonstrated how prompt engineering can improve the reliability of AI applications. Structured prompts and examples produced consistent output formats, while variation testing revealed limitations that were not visible when repeatedly testing the same input.

The next improvement would be to introduce stricter factual-grounding rules for product descriptions and explicit value normalization for data extraction.