# Issue Reporting Guidelines

To maintain an effective bugfix workflow and ensure issues are resolved in a timely manner, we kindly ask all reporters to follow guidelines described below.

Before creating an issue, please do the following:

- Make sure you have understood the product terminologies and concepts well by following our [TrilioVault For Kubernetes](https://docs.trilio.io) documentation
- Make sure the behavior you are reporting is really a bug, not a feature.
-  Check the  [existing issues](https://github.com/triliovault-k8s-issues/triliovault-k8s-issues/issues)  to make sure you are not duplicating somebody’s work.
- Make sure your environment successfully passes our [preflight check](https://github.com/triliovault-k8s-issues/triliovault-k8s-issues/blob/master/tools/preflight/README.md). Our solution is dependent on CSI, so these preflight checks are focused around testing the operations of your CSI installation. Please run this preflight check tool, if not have done already. Make sure it passes all the checks.
- GitHub is intended for free teir and basic tier users to report on issues. There are no account management services associated with GitHub. Enterprise users should report any issues directly to their respective customer success manager.

If you are sure that the problem you are experiencing is caused by a bug, file a new issue in a Github issue tracker following the recommendations below.
- 
# Issue Template

Higher level of detail in the report increases chances that someone will be able to reproduce the issue. It is hard to advice on any problems which can not be replicated. This is why we strongly advice to follow this template while reporting the issue.

## Title

Title is a vital part of a bug report for developers to triage and quickly identify a unique issue. A well written title should contain a clear, brief explanation of the issue, making emphasis on the most important points.

Good example:

> Unable to backup mysql helm chart

Unclear example:

> Can't backup.

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
