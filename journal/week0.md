# Week 0 — Billing and Architecture
# JOURNALING

# Create a User 
I created a user and assigned Billing and Admin policy to it from my root account. My user account Adaeze_Ontario_BootCamp1 is what I will be using for the bootcamp to do my hands-on projects.


# Create a budget
I was able to create a budget of $10 in my AWS console just so I know my spend limit when I reach the $10 and I do not over board with my spendng. Attached is an image of it.
![Image of the budget alarm I created](main/_docs/assets/Budget.png)
I also run the budget using CLI in my Gitpod account and you can confirm the coomands under my budget.json. Below is the command I run.
{
    "BudgetLimit": {
        "Amount": "1",
        "Unit": "USD"
    },
    "BudgetName": "One Dollar Budget",
    "BudgetType": "COST",
    "CostFilters": {
        "TagKeyValue": [
            "user:Key$value1",
            "user:Key$value2"
        ]
    },
    "CostTypes": {
        "IncludeCredit": true,
        "IncludeDiscount": true,
        "IncludeOtherSubscription": true,
        "IncludeRecurring": true,
        "IncludeRefund": true,
        "IncludeSubscription": true,
        "IncludeSupport": true,
        "IncludeTax": true,
        "IncludeUpfront": true,
        "UseBlended": false
    },
    "TimePeriod": {
        "Start": 1477958399,
        "End": 3706473600
    },
    "TimeUnit": "MONTHLY"
}

# Install AWS CLI in my Gitpod Account
My Gitpod is linked to my GitHub account and so, the commands I run in the Gitpod, I made sure to commit them to my GitHub account.
I installed my AWS CLI via my gitpod with the following command

tasks:
  - name: aws-cli
    env:
      AWS_CLI_AUTO_PROMPT: on-partial
    init: |
      cd /workspace
      curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip"
      unzip awscliv2.zip
      sudo ./aws/install
      cd $THEIA_WORKSPACE_ROOT
vscode:
  extensions:
    - 42Crunch.vscode-openapi
