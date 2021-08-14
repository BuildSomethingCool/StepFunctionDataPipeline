# Step Functions |  Twitter Data Pipeline

This repo contains code for a step function definition to be used for orchestrating the twitter data pipeline. It has steps for various ECS tasks
### License
[BuildSomethingCool/TwitterStreamIngest](https://github.com/BuildSomethingCool/TwitterStreamIngest)
### License
[BuildSomethingCool/DynamoDbExport](https://github.com/BuildSomethingCool/DynamoDbExport)

## The sf_input.json file contains the json input for the step function. The input.topic key represents which topic to filter tweets for

```json
{
    "input": {
        "topic": "LA Lakers"
    }
}
```
## Usage

```bash
# TODO
```