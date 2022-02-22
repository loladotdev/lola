# Lola

This is an issues-only repo for [Lola](https://www.lola.dev).

Issues or feature requests can be [filed](https://github.com/loladotdev/dev/issues/new/choose) within this repo.

## FAQ

### How can I get access to Lola?
We are currently in an invite-only developer preview. You can request access [here](https://www.lola.dev/preview/).

### What platforms are supported?
Lola runs on Windows, macOS & Linux (Ubuntu 20.04).

### How does Lola connect to my AWS account?

Lola uses the [profiles](https://docs.aws.amazon.com/cli/latest/userguide/cli-configure-files.html) stored in the `.aws` folder in your home directory exactly as the official AWS CLI does. Lola only reads this file to set up the SDK we [use](https://github.com/aws/aws-sdk-cpp#aws-sdk-for-c). Lola supports AWS SSO and other credential providers like `aws-vault` to keep your account secure.

### What permissions does Lola need?

The minimal policy for Lola looks like this:

```
{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Sid": "LolaMinimal",
            "Effect": "Allow",
            "Action": [
                "iam:ListAccountAliases",
                "logs:DescribeLogGroups",
                "logs:DescribeLogStreams",
                "logs:FilterLogEvents",
                "logs:GetLogEvents",
                "lambda:ListFunctions",
                "lambda:GetFunction",
                "dynamodb:ListTables",
                "dynamodb:DescribeTable",
                "cloudformation:DescribeStacks",
                "s3:ListAllMyBuckets",
                "apigateway:GET"
            ],
            "Resource": "*"
        }
    ]
}

```

If you want to use Lola for only one resource type (i.e. Cloudwatch Logs) you can do that:

```
{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Sid": "LolaJustLogs",
            "Effect": "Allow",
            "Action": [
                "iam:ListAccountAliases",
                "logs:DescribeLogGroups",
                "logs:DescribeLogStreams",
                "logs:FilterLogEvents",
                "logs:GetLogEvents"
            ],
            "Resource": "*"
        }
    ]
}
```
