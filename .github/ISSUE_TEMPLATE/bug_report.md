name: Bug Report
description: File a bug report.
title: '[Bug]: '
labels: ["bug", "triage"]
assignees: ''
body:
  - type: markdown
    value: |
      Thanks for filling out this bug report. Before continuing, please make sure that:
      - There is not a similar issue in the open **AND** closed issues
      - It is constantly reproducible
      - If possible, provide logs and/or screenshots.
      
      You can also visit us directly in the Slack Channel to talk to someone directly.

  - type: textarea
    id: description
    attributes:
      label: Describe the bug
      description: A clear an concise description of what the bug is.
      placeholder: Bug Description
    validation:
      required: true
      
  - type: textarea
    id: steps
    attributes:
      label: To Reproduce
      description: Steps to reproduce the behavior. Please verify that a similar bug doesn't already exist.
      placeholder: |
        1. Go to '...'
        2. Click on '...'
        3. Scroll down to '...'
        4. See error
    validation:
      required: true
      
  - type: textarea
    id: expecte
    attributes:
      label: Expected behavior
      description: A clear and concise description of what is expected to happen.
      placeholder: Expected behavior
    validation:
      required: true
      
  - type: input
    id: version
    attributes:
      label: Material Theme Version
      description: Please provide the Material Theme version number.
      placeholder: v7.0.0
    validations:
      required: true
      
  - type: dropdown
    id: ide
    attributes:
      label: IDE
      description: Please provide the IDE(s) where it happened.
      multiple: true
      options:
        - IntelliJ IDEA
        - RubyMine
        - WebStorm
        - PHPStorm
        - Rider
        - PyCharm
        - Android Studio
        - DataGrip
        - Other (AppCode, CLion, GoLang...)
    validations:
      required: true
      
  - type: textarea
    id: system-info
    attributes:
      label: System Info
      description: Other information: OS, Installed Plugins...
      render: shell
      placeholder: |
        Please go to *IntelliJ IDEA -> About IntelliJ IDEA (Mac)* or *Help -> About IntelliJ IDEA (Windows)* and copy the infos to the clipboard and paste it here.
        It should contain:
        * OS (Windows, Linux, Mac)
        * IntelliJ Product + version (IDEA, RubyMine...)
        * Plugin version
        * If needed a list of enabled plugins -->
            validations:
              required: true
              
  - type: textarea
    id: screenshots
    attributes:
      label: Logs/Screenshots
      description: Please use this textarea to append logs and/or screenshots. The more information the easier it will be to fix your issue.
      render: shell
