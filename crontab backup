#!/bin/bash

#command to grab unqiue s3 bucket name
bucket=$(aws s3 ls | grep crontab | awk {'print $3'})

aws s3 cp /var/spool/cron/root  s3://$bucket/cron-`date +"%Y-%m-%d"`-`/usr/bin/ec2-tag Name`
