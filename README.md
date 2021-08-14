# Step Functions |  Twitter Data Pipeline

This repo contains code for a step function definition to be used for orchestrating the twitter data pipeline. It has steps for various ECS tasks
### Raw Ingest Streaming Job
[BuildSomethingCool/TwitterStreamIngest](https://github.com/BuildSomethingCool/TwitterStreamIngest)
### Export from raw table to csv stored in s3
[BuildSomethingCool/DynamoDbExport](https://github.com/BuildSomethingCool/DynamoDbExport)

## The cli_input.json file contains the json input for the start-exectution command for step functions. This json contains the input for the ECS step for step functions. The ${TOPIC_TO_FILTER_ON} placeholder represents which topic to filter tweets for. State Machine is not committed to git

```json
{
    "stateMachineArn": "",
    "input": "{\"input\": {\"topic\": \"${TOPIC_TO_FILTER_ON}\"}}"
}

```
## Usage

```bash
# Start the execution via the AWS CLI
aws stepfunctions start-execution --cli-input-json fileb://cli_input.json
```