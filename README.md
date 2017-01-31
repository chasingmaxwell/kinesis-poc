# kinesis-poc

This is a proof of concept package which demonstrates posting a record to an AWS kinesis stream.

## Install

`composer require global chasingmaxwell/kinesis-poc`

## Configure

Add a yaml configuration file to to the `~/.config/kinesis-poc` directory with the following contents:

```yml
# The awsKinesisClient object will be passed to the KinesisClient factory.
# Available options: http://docs.aws.amazon.com/aws-sdk-php/v2/guide/configuration.html#client-configuration-options
kinesisClientOptions:
  profile: # An AWS credentials profile to use for API requests.
```

The name of the file is not important. In fact, you can include as many configuration files as you would like in this directory and they will be merged together in alphabetical order.

## Usage

`putKinesisRecord -s [Stream Name] -d [Record Data] -p [Partition Key]`
