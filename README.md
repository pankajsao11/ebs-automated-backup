## Method 1: Using Amazon Data Lifecycle Manager (DLM)

Goto "Elastic Block Store", click on "Lifecycle Manager" > Create a Lifecycle Policy
![image](https://github.com/user-attachments/assets/61a5b303-429e-40bf-a1a9-749e8daab233)

## Configure Policy Details

> Select "EBS snapshot policy" as the policy type.
> Give your policy a description.
> Choose the resource type (volume or instance).
> Use tags to target the volumes you want to back up.

![image](https://github.com/user-attachments/assets/da842486-55b9-4871-9953-49bf89a6219d)

## Set the Schedule

> Define how often you want snapshots to be taken (e.g., daily, weekly).
> Set the time for snapshot creation.
> Choose your preferred time zone.
> Specify how long you want to keep the snapshots.
> You can set a count-based or age-based retention rule.
Note: The timezone shows UTC but we need to set as per our current timezone/time. No need to convert the time in UTC etc.
![image](https://github.com/user-attachments/assets/42796d3c-41cb-47f3-8d54-2d3cacceaf86)

## Add Tags to Snapshots (Optional)

> Add tags to your snapshots for easier management.

## Enable Cross-Region Copy (Optional)
If needed, set up cross-region copying for disaster recovery.

![image](https://github.com/user-attachments/assets/29fd2bd0-fb20-40b5-85f9-e02bd81da325)

## Review And Create
![image](https://github.com/user-attachments/assets/d7a48720-9583-4404-be97-3da7f5a44f4b)

Final results:
Same region snapshot -
![image](https://github.com/user-attachments/assets/2290e3ad-cbfb-4750-a8bf-d7c8b59a1eea)

Cross region snapshot -
![image](https://github.com/user-attachments/assets/b19f9cc1-198b-4bb1-9ef8-11d14e4b354d)

## Method 2: Using AWS Backup

Create backup plan > Choose Plan Options > Select "Build a new plan" or use an existing template.
Give your plan a name.

![image](https://github.com/user-attachments/assets/b9a290a9-a3dd-4962-b9ff-bb26f87b9faa)

## Configure Backup Rule

> Set the backup frequency (hourly, daily, weekly, monthly).
> Define the backup window.
> Set retention period.
> Choose a lifecycle policy for cold storage transition (optional).

![image](https://github.com/user-attachments/assets/9fe417c9-c0ab-4b69-aa3e-552e6ffe0e8d)

