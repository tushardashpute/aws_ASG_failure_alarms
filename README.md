# aws_ASG_failure_alarms
ASG alarms using sns and cloudwatch

If ASG is not able to scale due to any problem then we should must be notified about the issue. You can be notified when Amazon EC2 Auto Scaling is launching or terminating the EC2 instances in your Auto Scaling group as well.

- Configure Amazon SNS notifications for Amazon EC2 Auto Scaling
1. Create an Amazon SNS topic
2. Subscribe to the Amazon SNS topic
3. Confirm your Amazon SNS subscription
4. Configure your Auto Scaling group to send notifications
5. Test the notification

1. Create an Amazon SNS topic

<img width="1504" alt="image" src="https://user-images.githubusercontent.com/74225291/175783650-96de7775-f4e7-4c0f-8935-74a79543db0f.png">

<img width="1504" alt="image" src="https://user-images.githubusercontent.com/74225291/175783685-b46f6c9d-cc86-43f3-882f-9c5f89ab4c3a.png">

2. Subscribe to the Amazon SNS topic

<img width="1504" alt="image" src="https://user-images.githubusercontent.com/74225291/175783734-67fd0589-546a-4ed7-a7ce-ef3af9068ba5.png">

<img width="1474" alt="image" src="https://user-images.githubusercontent.com/74225291/175783804-2d75cdc9-d378-4335-8bc6-b35c5682bf9e.png">

3. Confirm your Amazon SNS subscription

<img width="1191" alt="image" src="https://user-images.githubusercontent.com/74225291/175783826-0c383cde-8155-47d4-81ba-8f39b62e9e18.png">

Amazon SNS sends a confirmation email to the email address you specified in the previous step.

Make sure that you open the email from AWS Notifications and choose the link to confirm the subscription before you continue with the next step.

<img width="1198" alt="image" src="https://user-images.githubusercontent.com/74225291/175783865-94f9eac7-8257-4442-b4bb-5cce800c941c.png">

4. Configure your Auto Scaling group to send notifications

<img width="1224" alt="image" src="https://user-images.githubusercontent.com/74225291/175783975-639bb3f5-d8da-49e1-acbf-5c9dbc0f2065.png">

<img width="1256" alt="image" src="https://user-images.githubusercontent.com/74225291/175784077-41efacc5-8b28-4f17-bb1b-fa7559826e79.png">


Here we have ASG group already inplace, but here issue is attached target group asg-alarm-test-1 to the ASG someone deleted but its still associated with ASG due to which scaling is not working.

<img width="1268" alt="image" src="https://user-images.githubusercontent.com/74225291/175784126-32da17f7-2c8f-4d0b-8555-c65e3b9174c7.png">

<img width="789" alt="image" src="https://user-images.githubusercontent.com/74225291/175784143-2d1d9a4e-579d-4173-9235-93da9f900d11.png">

<img width="1224" alt="image" src="https://user-images.githubusercontent.com/74225291/175783975-639bb3f5-d8da-49e1-acbf-5c9dbc0f2065.png">

<img width="1240" alt="image" src="https://user-images.githubusercontent.com/74225291/175784159-3900370f-2d1b-4cf7-b7de-fb6d02f7f19f.png">

<img width="1224" alt="image" src="https://user-images.githubusercontent.com/74225291/175783975-639bb3f5-d8da-49e1-acbf-5c9dbc0f2065.png">

Now if I try to change the instance count of ASG, then it will failed.

<img width="1499" alt="image" src="https://user-images.githubusercontent.com/74225291/175784283-5a4a592c-f6fb-4ae6-84c3-033e6f149c28.png">

<img width="1224" alt="image" src="https://user-images.githubusercontent.com/74225291/175783975-639bb3f5-d8da-49e1-acbf-5c9dbc0f2065.png">

We will notified on the mail for the same.

![Uploading image.png…]()

<img width="1224" alt="image" src="https://user-images.githubusercontent.com/74225291/175783975-639bb3f5-d8da-49e1-acbf-5c9dbc0f2065.png">
