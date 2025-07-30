# AWS Cloud Cost Optimization - Identifying Stale Resources

## Identifying Stale EBS Snapshots

In this example, we'll create a Lambda function that identifies EBS snapshots that are no longer associated with any active EC2 instance and deletes them to save on storage costs.

### Description:

The Lambda function fetches all EBS snapshots owned by the same account ('self') and also retrieves a list of active EC2 instances (running and stopped). For each snapshot, it checks if the associated volume (if exists) is not associated with any active instance. If it finds a stale snapshot, it deletes it, effectively optimizing storage costs.


<img width="1875" height="697" alt="Screenshot 2025-07-30 115743" src="https://github.com/user-attachments/assets/5b6527b1-bf0c-4b24-af72-0a6528d08d78" />

<img width="1661" height="772" alt="Screenshot 2025-07-30 115030" src="https://github.com/user-attachments/assets/eb83d1bb-715e-4f3b-9ead-7ae3ad87b65e" />

<img width="1697" height="744" alt="Screenshot 2025-07-30 115140" src="https://github.com/user-attachments/assets/26c24cd7-e8ee-43a4-bfbd-93c9874da004" />

<img width="1367" height="650" alt="Screenshot 2025-07-30 115250" src="https://github.com/user-attachments/assets/ca16e0b4-eec1-4271-a92b-f70f5c1eda8d" />

<img width="1799" height="724" alt="Screenshot 2025-07-30 115630" src="https://github.com/user-attachments/assets/a3a797fc-06ec-40c4-8846-0f34430dc335" />






