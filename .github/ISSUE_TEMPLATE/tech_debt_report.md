name: "Tech Debt Report"
description: "Report a new piece of technical debt"
title: "[Tech Debt] <short description>"
labels: ["tech-debt", "needs-review"]

body:
  - type: textarea
    id: description
    attributes:
      label: Description
      description: What is the technical debt?
      placeholder: Describe the issue, context, and affected components.
    validations:
      required: true

  - type: textarea
    id: impact
    attributes:
      label: Impact
      description: How does this debt affect performance, maintainability, or delivery?
    validations:
      required: true

  - type: dropdown
    id: severity
    attributes:
      label: Severity
      options:
        - Low
        - Medium
        - High
        - Critical
    validations:
      required: true

  - type: textarea
    id: reproduction
    attributes:
      label: Reproduction / Evidence
      description: Logs, screenshots, or examples.
