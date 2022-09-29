## OneStepCloser - To move away from unemployment

Login
Signup
Logout
Delete Account
Update User
Update Password

Set Goals?
Create interview process? -> goal / step in a goal
Company profile
Calendar? Not building a calendar, but we can mess around with dates
Status of goal
Steps Definition - By user


Models

User
Goal
Step
Company
Process

User
username: String|required|unique|min: 3|max: 16
name: String|max: 50
password: String|required
email: String|required|must-be-valid-email|unique

Goal
title: String|required|min: 3|max: 20
deadline: Date|required|min:Tomorrow|max: 100 years from now
description: String

Step
title: String|required|min: 3|max: 20
description: String
goal: Goal (Relationship / Reference)

Company
name: String|required|min: 3|max: 60
desireability: ['Hell Nah', 'Meh', 'Please Say Yes']
website: String

Process
name: String|required|min: 3|max: 60
isRemote: Boolean|false by default
status: Step (Relationship / Reference)
notes: String
nextInteraction: Date|nullable
salary: String
location: String
company: Company (Relationship / Reference)
url: String