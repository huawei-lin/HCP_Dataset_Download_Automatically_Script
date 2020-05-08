# README

This script can download the HCP dataset automatically.

```
subjects.txt  - subjects number list
```

## How to use

Look at [boto3 Docs](https://boto3.amazonaws.com/v1/documentation/api/latest/guide/quickstart.html#installation)

First, boto3 should be downloaded.
```
pip install boto3
```

If you have the [AWS CLI](http://aws.amazon.com/cli/) installed, then you can use it to configure your credentials file.

```
aws configure

aws_access_key_id = YOUR_ACCESS_KEY
aws_secret_access_key = YOUR_SECRET_KEY
```

The key come from [HCP dataset](https://db.humanconnectome.org/), and you should click the button of 'Amazon S3 Access enabled'.

## Detail
In this script, I want to download some files whose name include `_RL.nii.gz` or `_LR.nii.gz` in `HCP_1200/{$subject_number}/MNINonLinear/Results/tfMRI*`.

You can change the `keyList = bucket.objects.filter(Prefix = {$your_filter})` to filter files.

And, you can change the `trycnt` variable to change the number of retry.

## About

If you meet some problem, please touch with me.

Email: winsoul@foxmail.com.
