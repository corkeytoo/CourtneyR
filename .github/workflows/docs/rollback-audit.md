# Rollback & Audit Trail

## Rollback Strategy
- If a deployment causes critical issues in production, we roll back to the last known good version.
- Rollback is triggered manually by the on-call engineer or release manager.
- The rollback script uses the previously deployed build artifact or tagged release.

## Rollback Procedure
1. Identify the last successful deployment (build ID or Git tag).
2. Execute the rollback script with the previous version identifier.
3. Verify application health (monitoring, smoke tests).
4. Record the incident and actions taken in the change log.

## Audit Trail
- All deployments and rollbacks are executed through GitHub Actions.
- Each run stores logs, timestamps, and who triggered the workflow.
- Git tags and release notes provide additional history for what code was deployed.
- Change and incident details are stored in this repository for compliance and review.
