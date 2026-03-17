name: "Tech Debt Review"
description: "Review an existing tech debt item"
title: "[Review] <tech debt issue number>"
labels: ["tech-debt-review"]

body:
  - type: textarea
    id: analysis
    attributes:
      label: Analysis
      description: Summarize findings from the review.
    validations:
      required: true

  - type: textarea
    id: recommendations
    attributes:
      label: Recommendations
      description: Proposed remediation steps or alternatives.
    validations:
      required: true

  - type: input
    id: score
    attributes:
      label: Priority Score
      description: Score based on the scoring model (1–10).
    validations:
      required: true
