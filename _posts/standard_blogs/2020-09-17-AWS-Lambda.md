---
layout: 	default
title:  	AWS Lambda
date:   	2020-09-17
categories: Posts Coding
author: 	Jordan
permalink: 	/Mary-has-a-little-Lambda
---


## This blog follows along with one of the interactive labs from the Generation Re/Start AWS Certified Cloud Practitioner course. We were tasked with creating a text file to be placed in an S3 bucket on AWS and a Lambda function that would trigger whenever a new object entered the bucket, take a word count of the file and use SNS to send an email/text alert with this information.


 
I'd actually already written the python code for the word counter and created an S3 bucket and a text file (accessible from the AWS CLI) back when I tried to do the lab the first time, but I had ran out of time and when I tried it again I wasn't granted access to perform any activities via the CLI or the management console. Thinking it may just be because I'd just ran the time down on the lab and restarted it, maybe it hadn't configured yet and I've spent a long time working on this now anyway, I'll do something else. A few days passed and after resetting the lab and refreshing the page I tried again but it still wouldn't let me access anything, saying the access keys weren't valid even though I triple-checked and reconfigured the CLI but it wasn't having it, so I tried another lab and it was having the exact same issue.

After a LOT of googling, different forums, restarting the browser and my whole computer, trying different commands and generally puzzling over why the access keys weren't granting me access even though everything I found was telling me they matched, I found myself in the `configure` file in the `.aws` folder from the ec2-user home directory and found that, although the `aws_access_key_id` and the `aws_secret_access_key` that I had been checking were correct, the file did not include an `aws_session_token` and once I added that I was finally able to perform functions again! This problem persists every time I launch a new lab but now I know the solution it's a 10 second fix, and actually gave me an early awareness of the security breach at the start of the lab to detect a hack in your account (where they added another set of keys for access) so it's definitely a location worth being hammered into my head to check for who has access every time I launch a lab now.

Anyways, after several hours over about a week of just troubleshooting why I wasn't being given access to AWS functions, I'm back on task with the lab! The first new hurdle to become apparent is that I've coded my script to be ran as a python script from a directory to read the word count of another file in that directory and it wouldn't be quite as simple to do this as a Lambda function. To approach this, I first just added my text file to the S3 bucket I made using the *aws s3 cp* command  and then started working on the Lambda function.

I initially pasted in the word counter I had coded into the python Lambda function, but it just failed and failed no matter what I tried to change or edit to make like the [tutorial][tutorial] that I saw on youtube, so eventually I just deleted it all and decided it would be easier to take an existing, working Lambda function and then modify it to my needs. I quickly found a script that counted the number of lines of a file in an S3 bucket so copied that into my function, replaced the bucket and file names with mine and it passed the test! The only issue now is that this wasn't what I wanted it to do, it wasn't being triggered and there was no SNS involvement... By playing with the code in the Lambda function, testing the result of changing various bits and seeing what error occurred when commenting out different lines, I was able to integrate the working Lambda function with my word counter code and had a Lambda function that would return a sentence telling you the word count of the file it had checked!!! This is the code I used for the Lambda:

{% highlight ruby %}

import boto3

def lambda_handler(event, context):
    s3 = boto3.client('s3')
    data = s3.get_object(Bucket='748unicorns', Key='unicorns.txt')
    contents = data['Body'].read()
    words = contents.split()
    return "The word count in the file 'unicorns.txt' is " + str(len(words))

{% endhighlight%}


Now I had the main bit in the middle, I just needed to slap a bit of bread either side of my filling and call it a sandwich. This was pretty easy to do with how AWS is set up and within 20 minutes on my first time creating a Lambda function without just following step-by-step instructions, I was able to add the trigger for when any file was added to the bucket (via any of the available commands) and set the output as a quick to set up SNS topic with 2 sbscriptions: my email and number for an SMS. With this, my Lambda function was complete! I tested it and recieved both the email and SMS notifications with the word count, changed the contents of the file and reuploaded it and got new messages with the updated word count!

For the lab, we were meant to create a file and have the Lambda specifically read that file and as an extra thing, I did try to make it so the function would count the words of whatever file was added but I didn't manage to get that to work. I was trying to substitute `unicorns.txt` as the `Key` with some form of wildcard (like *) to work no matter what the file was called but as I said, this didn't work and I couldn't find a way to do it before the lab session expired yet again but I'm sure it's just another simple little trick that I haven't seen yet but I will be on the lookout!!

Well that was longer than I was expecting! When I start working on actual projects I'll have to make folders for each with a collection of blog posts in as I work on the project over time, I should be able to use the simple bit of code I have to cycle through blog titles and filter them through project based tags to display the other blogs for that project on the page too!

Till next time,

¡JaBlog!


[tutorial]: https://youtu.be/6LvtSmJhVRE

[back](./)
