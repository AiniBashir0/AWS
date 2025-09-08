## Amazon Data Lifecycle Manager (DLM) = Service that automates creation, retention, and deletion of EBS snapshots and EBS-backed AMIs.

#### Benefits:

- Automates backup scheduling.
- Saves storage cost (delete old snapshots automatically).
- Improves compliance & disaster recovery.
- Works using Lifecycle Policies → define rules for when to create, retain, and delete snapshots.
- volume > tags > key- ENV, value- test
- go to lifecycle policy > custom policy > resources- volume > target resources tags (Key- ENV, value- test) > description > next> create


### EBS Recyclebin
- snapshot ? recyclebin > resoucres > restore (deleted snapshot)
