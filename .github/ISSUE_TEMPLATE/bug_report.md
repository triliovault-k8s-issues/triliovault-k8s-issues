---
name: Bug report
about: Create a report to help us improve
title: ''
labels: ''
assignees: ''

---

## Issue Description

### Preconditions

Describing preconditions is a great source of information for troubleshooting an issue. Provide details on the Kubernetes flavour, Kubernetes version, storage used,  CSI driver version, detailed information on resources created (Target, BackupPlan, Backup, Restore, etc), and TrilioVault for Kubernetes version. Basically, please provide all relevant details that would help a developer set up the same environment as you have.

Example:

```
1. k8s flavour: kops
2. k8s version: 1.17.1
3. storage: AWS EBS
4. CSI version: v0.5.0
5. k8s TrilioVault version: 1.0.1
...
```

### Steps to reproduce

This part of the bug report is the most important, as developers will use this information to reproduce the issue. Issues are more likely to be fixed if it can be reproduced.

Precisely describe each step you have taken to reproduce the issue. Try to include as much information as possible, sometimes even minor differences can be crucial.

Example:

```
1. Create Target named nfs-target
2. Created BackupPlan named mysql-backup-plan
3. Created Backup with name mysql-backup
...

```

### Actual and Expected result

To make sure that everybody involved in resolving the issue are on the same page, precisely describe the result you expected and the actual result you observed after performing the steps.

Example:

```
Expected result:
Backup status changes to Available
Actual result:
Backup status changed to Failed

```

### Support Log Bundle

TrilioVault for Kubernetes provides [Support Log Collector](https://github.com/triliovault-k8s-issues/triliovault-k8s-issues/blob/master/tools/log_collector/README.md) tool, which captures all the necessary information required for our developers to debug your issue. **We strongly recommend you run this utility and upload the zip file created by this tool**
