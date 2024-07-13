# Amazon Bedrock and Claude Deep Dive Workshop

This hands-on workshop, aimed at developers and solution builders, introduces how to leverage foundation models (FMs) e.g. Titan and Claude 3 through [Amazon Bedrock](https://aws.amazon.com/bedrock/).

Labs include:

- **01 - Text Generation** \[Estimated time to complete - 20 mins\]
    - Text generation with Bedrock
    - Text summarization with Titan and Claude
    - QnA with Titan
- **02 - RAG and Knowledge bases** \[Estimated time to complete - 45 mins\]
    - Simple RAG with Claude 3 and LangChain
    - Managed RAG retrieve and generate example
    - Langchain RAG retrieve and generate example
- **03 - Image and Multimodal** \[Estimated time to complete - 45 mins\]
    - Image understanding & visual QA
    - Bedrock Titan Multimodal embeddings
    - Multimodal RAG
- **04 - Tool Use** \[Estimated time to complete - 45 mins\]
    - Tool use workflow
    - Chatbot with tool use
- **05 - Agents** \[Estimated time to complete - 30 mins\]
    - Restaurant agent
    - Agent with action and knowledge base
- **06 - Security and Gorvernance** \[Estimated time to complete - 30 mins\]
    - Bedrock guardrails

## Getting started

### Choose a notebook environment

This workshop is presented as a series of **Python notebooks**, which you can run from the environment of your choice:

- For a fully-managed environment with rich AI/ML features, we'd recommend using [SageMaker Studio](https://aws.amazon.com/sagemaker/studio/). To get started quickly, you can refer to the [instructions for domain quick setup](https://docs.aws.amazon.com/sagemaker/latest/dg/onboard-quick-start.html).
- For a fully-managed but more basic experience, you could instead [create a SageMaker Notebook Instance](https://docs.aws.amazon.com/sagemaker/latest/dg/howitworks-create-ws.html).
- If you prefer to use your existing (local or other) notebook environment, make sure it has [credentials for calling AWS](https://docs.aws.amazon.com/cli/latest/userguide/cli-chap-configure.html).


### Enable AWS IAM permissions for Bedrock

The AWS identity you assume from your notebook environment (which is the [*Studio/notebook Execution Role*](https://docs.aws.amazon.com/sagemaker/latest/dg/sagemaker-roles.html) from SageMaker, or could be a role or IAM User for self-managed notebooks), must have sufficient [AWS IAM permissions](https://docs.aws.amazon.com/IAM/latest/UserGuide/access_policies.html) to call the Amazon Bedrock service.

To grant Bedrock access to your identity, you can:

- Open the [AWS IAM Console](https://us-east-1.console.aws.amazon.com/iam/home?#)
- Find your [Role](https://us-east-1.console.aws.amazon.com/iamv2/home?#/roles) (if using SageMaker or otherwise assuming an IAM Role), or else [User](https://us-east-1.console.aws.amazon.com/iamv2/home?#/users)
- Select *Add Permissions > Create Inline Policy* to attach new inline permissions, open the *JSON* editor and paste in the below example policy:

```
{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Sid": "BedrockFullAccess",
            "Effect": "Allow",
            "Action": ["bedrock:*"],
            "Resource": "*"
        }
    ]
}
```

> ⚠️ **Note:** With Amazon SageMaker, your notebook execution role will typically be *separate* from the user or role that you log in to the AWS Console with. If you'd like to explore the AWS Console for Amazon Bedrock, you'll need to grant permissions to your Console user/role too. You can run the notebooks anywhere as long as you have access to the AWS Bedrock service and have appropriate credentials

For more information on the fine-grained action and resource permissions in Bedrock, check out the Bedrock Developer Guide.


### Clone and use the notebooks

> ℹ️ **Note:** In SageMaker Studio, you can open a "System Terminal" to run these commands by clicking *File > New > Terminal*

Once your notebook environment is set up, clone this workshop repository into it.

```sh
git clone https://github.com/aws-east-ai/Bedrock-Claude-Deep-Dive-Workshop
cd Bedrock-Claude-Deep-Dive-Workshop
```


You're now ready to explore the lab notebooks! Start with [00_Prerequisites/01_bedrock_basics.ipynb](00_Prerequisites/01_bedrock_basics.ipynb) for details on how to install the Bedrock SDKs, create a client, and start calling the APIs from Python.
