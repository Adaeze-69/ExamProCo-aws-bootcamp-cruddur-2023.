# Week 0 — Billing and Architecture
# JOURNALING

# Create a User in my AWS Root Account
I created a user and assigned Billing and Admin policy to it from my root account. My user account Adaeze_Ontario_BootCamp1 is what I will be using for the bootcamp to do my hands-on projects.


# Create a budget
I was able to create a budget of $10 in my AWS console just so I know my spend limit when I reach the $10 and I do not over board with my spendng. Attached is an image of it.

![Image of the budget alarm I created](assets/Budget.png)
I also run the budget using CLI in my Gitpod account and you can confirm the coomands under my budget.json. Below is the command I run.
```
aws budgets create-budget --account-id MY ID --budget file://pera1.json --notifications-with-subscribers file://pera2.json

```

# Install AWS CLI in my Gitpod Account
My Gitpod is linked to my GitHub account and so, the commands I run in the Gitpod, I made sure to commit them to my GitHub account.
I installed my AWS CLI via my gitpod with the following command

```
url "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip"
unzip awscliv2.zip
sudo ./aws/install

```

Output of Command

```
{
    "UserId": "AKIASH3YIYXYN5FLCBFJ",
    "Account": "154334184944",
    "Arn": "arn:aws:iam::154334184944:user/Adaeze_Ontario_BootCamp1"
}
```
    
  # Cruddur- Logical Architectural Diagram
  I created a Logical Architectural diagram for the Crudder Application in a detailed form I am working on in this cause of this bootcamp. I am using servicess like S3 bucket,DNS,Load Balancer, App Sync, Amazon Dynamo DB and a host of others. Below is the image of the diagram but you can find the link to my diagram in [my Lucid Chart here](https://lucid.app/lucidchart/3f4b4426-2636-4e54-b51f-98f6ca1811aa/edit?viewport_loc=-1242%2C160%2C4314%2C2005%2C0_0&invitationId=inv_9dfcd7bd-60b5-491d-90e7-780cb5bcc978)

# Conceptual Diagram of Cruddur on Napkin
I drew a conceptual diagram on a napkin showing how few of the services will be used to set up the Cruddur application. Services like momento, messaging system,database,timeline service and a couple of other services were illustrated in it. Below is the diagram illustration.
**image here**
