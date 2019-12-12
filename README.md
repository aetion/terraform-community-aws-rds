## Variables

<table>
<tr><th>Name</th><th>Description</th><th>Type</th><th>Default</th> <th>Required</th></tr>
<tr>
<td>allocated_storage</td>
<td>The allocated storage in gigabytes</td>
<td>

`string`</td>
<td>

n/a</td>
<td>yes</td>
</tr>
<tr>
<td>allow_major_version_upgrade</td>
<td>Indicates that major version upgrades are allowed. Changing this parameter does not result in an outage and the change is asynchronously applied as soon as possible</td>
<td>

`bool`</td>
<td>

`false`</td>
<td>no</td>
</tr>
<tr>
<td>apply_immediately</td>
<td>Specifies whether any database modifications are applied immediately, or during the next maintenance window</td>
<td>

`bool`</td>
<td>

`false`</td>
<td>no</td>
</tr>
<tr>
<td>auto_minor_version_upgrade</td>
<td>Indicates that minor engine upgrades will be applied automatically to the DB instance during the maintenance window</td>
<td>

`bool`</td>
<td>

`true`</td>
<td>no</td>
</tr>
<tr>
<td>availability_zone</td>
<td>The Availability Zone of the RDS instance</td>
<td>

`string`</td>
<td>

`""`</td>
<td>no</td>
</tr>
<tr>
<td>backup_retention_period</td>
<td>The days to retain backups for</td>
<td>

`number`</td>
<td>

`1`</td>
<td>no</td>
</tr>
<tr>
<td>backup_window</td>
<td>The daily time range (in UTC) during which automated backups are created if they are enabled. Example: '09:46-10:16'. Must not overlap with maintenance_window</td>
<td>

`string`</td>
<td>

n/a</td>
<td>yes</td>
</tr>
<tr>
<td>character_set_name</td>
<td>(Optional) The character set name to use for DB encoding in Oracle instances. This can't be changed. See Oracle Character Sets Supported in Amazon RDS for more information</td>
<td>

`string`</td>
<td>

`""`</td>
<td>no</td>
</tr>
<tr>
<td>copy_tags_to_snapshot</td>
<td>On delete, copy all Instance tags to the final snapshot (if final_snapshot_identifier is specified)</td>
<td>

`bool`</td>
<td>

`false`</td>
<td>no</td>
</tr>
<tr>
<td>create_db_instance</td>
<td>Whether to create a database instance</td>
<td>

`bool`</td>
<td>

`true`</td>
<td>no</td>
</tr>
<tr>
<td>create_db_option_group</td>
<td>Whether to create a database option group</td>
<td>

`bool`</td>
<td>

`true`</td>
<td>no</td>
</tr>
<tr>
<td>create_db_parameter_group</td>
<td>Whether to create a database parameter group</td>
<td>

`bool`</td>
<td>

`true`</td>
<td>no</td>
</tr>
<tr>
<td>create_db_subnet_group</td>
<td>Whether to create a database subnet group</td>
<td>

`bool`</td>
<td>

`true`</td>
<td>no</td>
</tr>
<tr>
<td>create_monitoring_role</td>
<td>Create IAM role with a defined name that permits RDS to send enhanced monitoring metrics to CloudWatch Logs.</td>
<td>

`bool`</td>
<td>

`false`</td>
<td>no</td>
</tr>
<tr>
<td>db_depends_on</td>
<td>Hack to add a depends on a module</td>
<td>

`any`</td>
<td>

n/a</td>
<td>yes</td>
</tr>
<tr>
<td>db_subnet_group_name</td>
<td>Name of DB subnet group. DB instance will be created in the VPC associated with the DB subnet group. If unspecified, will be created in the default VPC</td>
<td>

`string`</td>
<td>

`""`</td>
<td>no</td>
</tr>
<tr>
<td>deletion_protection</td>
<td>The database can't be deleted when this value is set to true.</td>
<td>

`bool`</td>
<td>

`false`</td>
<td>no</td>
</tr>
<tr>
<td>enabled_cloudwatch_logs_exports</td>
<td>List of log types to enable for exporting to CloudWatch logs. If omitted, no logs will be exported. Valid values (depending on engine): alert, audit, error, general, listener, slowquery, trace, postgresql (PostgreSQL), upgrade (PostgreSQL).</td>
<td>

`list(string)`</td>
<td>

`[]`</td>
<td>no</td>
</tr>
<tr>
<td>engine</td>
<td>The database engine to use</td>
<td>

`string`</td>
<td>

n/a</td>
<td>yes</td>
</tr>
<tr>
<td>engine_version</td>
<td>The engine version to use</td>
<td>

`string`</td>
<td>

n/a</td>
<td>yes</td>
</tr>
<tr>
<td>family</td>
<td>The family of the DB parameter group</td>
<td>

`string`</td>
<td>

`""`</td>
<td>no</td>
</tr>
<tr>
<td>final_snapshot_identifier</td>
<td>The name of your final DB snapshot when this DB instance is deleted.</td>
<td>

`string`</td>
<td>

n/a</td>
<td>yes</td>
</tr>
<tr>
<td>iam_database_authentication_enabled</td>
<td>Specifies whether or mappings of AWS Identity and Access Management (IAM) accounts to database accounts is enabled</td>
<td>

`bool`</td>
<td>

`false`</td>
<td>no</td>
</tr>
<tr>
<td>identifier</td>
<td>The name of the RDS instance, if omitted, Terraform will assign a random, unique identifier</td>
<td>

`string`</td>
<td>

n/a</td>
<td>yes</td>
</tr>
<tr>
<td>instance_class</td>
<td>The instance type of the RDS instance</td>
<td>

`string`</td>
<td>

n/a</td>
<td>yes</td>
</tr>
<tr>
<td>iops</td>
<td>The amount of provisioned IOPS. Setting this implies a storage_type of 'io1'</td>
<td>

`number`</td>
<td>

`0`</td>
<td>no</td>
</tr>
<tr>
<td>kms_key_id</td>
<td>The ARN for the KMS encryption key. If creating an encrypted replica, set this to the destination KMS ARN. If storage_encrypted is set to true and kms_key_id is not specified the default KMS key created in your account will be used</td>
<td>

`string`</td>
<td>

`""`</td>
<td>no</td>
</tr>
<tr>
<td>license_model</td>
<td>License model information for this DB instance. Optional, but required for some DB engines, i.e. Oracle SE1</td>
<td>

`string`</td>
<td>

`""`</td>
<td>no</td>
</tr>
<tr>
<td>maintenance_window</td>
<td>The window to perform maintenance in. Syntax: 'ddd:hh24:mi-ddd:hh24:mi'. Eg: 'Mon:00:00-Mon:03:00'</td>
<td>

`string`</td>
<td>

n/a</td>
<td>yes</td>
</tr>
<tr>
<td>major_engine_version</td>
<td>Specifies the major version of the engine that this option group should be associated with</td>
<td>

`string`</td>
<td>

`""`</td>
<td>no</td>
</tr>
<tr>
<td>max_allocated_storage</td>
<td>Specifies the value for Storage Autoscaling</td>
<td>

`number`</td>
<td>

`0`</td>
<td>no</td>
</tr>
<tr>
<td>monitoring_interval</td>
<td>The interval, in seconds, between points when Enhanced Monitoring metrics are collected for the DB instance. To disable collecting Enhanced Monitoring metrics, specify 0. The default is 0. Valid Values: 0, 1, 5, 10, 15, 30, 60.</td>
<td>

`number`</td>
<td>

`0`</td>
<td>no</td>
</tr>
<tr>
<td>monitoring_role_arn</td>
<td>The ARN for the IAM role that permits RDS to send enhanced monitoring metrics to CloudWatch Logs. Must be specified if monitoring_interval is non-zero.</td>
<td>

`string`</td>
<td>

`""`</td>
<td>no</td>
</tr>
<tr>
<td>monitoring_role_name</td>
<td>Name of the IAM role which will be created when create_monitoring_role is enabled.</td>
<td>

`string`</td>
<td>

`"rds-monitoring-role"`</td>
<td>no</td>
</tr>
<tr>
<td>multi_az</td>
<td>Specifies if the RDS instance is multi-AZ</td>
<td>

`bool`</td>
<td>

`false`</td>
<td>no</td>
</tr>
<tr>
<td>name</td>
<td>The DB name to create. If omitted, no database is created initially</td>
<td>

`string`</td>
<td>

`""`</td>
<td>no</td>
</tr>
<tr>
<td>option_group_description</td>
<td>The description of the option group</td>
<td>

`string`</td>
<td>

`""`</td>
<td>no</td>
</tr>
<tr>
<td>option_group_name</td>
<td>Name of the DB option group to associate. Setting this automatically disables option_group creation</td>
<td>

`string`</td>
<td>

`""`</td>
<td>no</td>
</tr>
<tr>
<td>options</td>
<td>A list of Options to apply.</td>
<td>

`any`</td>
<td>

`[]`</td>
<td>no</td>
</tr>
<tr>
<td>parameter_group_description</td>
<td>Description of the DB parameter group to create</td>
<td>

`string`</td>
<td>

`""`</td>
<td>no</td>
</tr>
<tr>
<td>parameter_group_name</td>
<td>Name of the DB parameter group to associate or create</td>
<td>

`string`</td>
<td>

`""`</td>
<td>no</td>
</tr>
<tr>
<td>parameters</td>
<td>A list of DB parameters (map) to apply</td>
<td>

`list(map(string))`</td>
<td>

`[]`</td>
<td>no</td>
</tr>
<tr>
<td>password</td>
<td>Password for the master DB user. Note that this may show up in logs, and it will be stored in the state file</td>
<td>

`string`</td>
<td>

n/a</td>
<td>yes</td>
</tr>
<tr>
<td>performance_insights_enabled</td>
<td>Specifies whether Performance Insights are enabled</td>
<td>

`bool`</td>
<td>

`false`</td>
<td>no</td>
</tr>
<tr>
<td>performance_insights_retention_period</td>
<td>The amount of time in days to retain Performance Insights data. Either 7 (7 days) or 731 (2 years).</td>
<td>

`number`</td>
<td>

`7`</td>
<td>no</td>
</tr>
<tr>
<td>port</td>
<td>The port on which the DB accepts connections</td>
<td>

`string`</td>
<td>

n/a</td>
<td>yes</td>
</tr>
<tr>
<td>publicly_accessible</td>
<td>Bool to control if instance is publicly accessible</td>
<td>

`bool`</td>
<td>

`false`</td>
<td>no</td>
</tr>
<tr>
<td>replicate_source_db</td>
<td>Specifies that this resource is a Replicate database, and to use this value as the source database. This correlates to the identifier of another Amazon RDS Database to replicate.</td>
<td>

`string`</td>
<td>

`""`</td>
<td>no</td>
</tr>
<tr>
<td>skip_final_snapshot</td>
<td>Determines whether a final DB snapshot is created before the DB instance is deleted. If true is specified, no DBSnapshot is created. If false is specified, a DB snapshot is created before the DB instance is deleted, using the value from final_snapshot_identifier</td>
<td>

`bool`</td>
<td>

`true`</td>
<td>no</td>
</tr>
<tr>
<td>snapshot_identifier</td>
<td>Specifies whether or not to create this database from a snapshot. This correlates to the snapshot ID you'd find in the RDS console, e.g: rds:production-2015-06-26-06-05.</td>
<td>

`string`</td>
<td>

`""`</td>
<td>no</td>
</tr>
<tr>
<td>storage_encrypted</td>
<td>Specifies whether the DB instance is encrypted</td>
<td>

`bool`</td>
<td>

`false`</td>
<td>no</td>
</tr>
<tr>
<td>storage_type</td>
<td>One of 'standard' (magnetic), 'gp2' (general purpose SSD), or 'io1' (provisioned IOPS SSD). The default is 'io1' if iops is specified, 'standard' if not. Note that this behaviour is different from the AWS web console, where the default is 'gp2'.</td>
<td>

`string`</td>
<td>

`"gp2"`</td>
<td>no</td>
</tr>
<tr>
<td>subnet_ids</td>
<td>A list of VPC subnet IDs</td>
<td>

`list(string)`</td>
<td>

`[]`</td>
<td>no</td>
</tr>
<tr>
<td>tags</td>
<td>A mapping of tags to assign to all resources</td>
<td>

`map(string)`</td>
<td>

`{}`</td>
<td>no</td>
</tr>
<tr>
<td>timeouts</td>
<td>(Optional) Updated Terraform resource management timeouts. Applies to `aws_db_instance` in particular to permit resource management times</td>
<td>

`map(string)`</td>
<td>

```json
{
  "create": "40m",
  "delete": "40m",
  "update": "80m"
}
```
</td>
<td>no</td>
</tr>
<tr>
<td>timezone</td>
<td>(Optional) Time zone of the DB instance. timezone is currently only supported by Microsoft SQL Server. The timezone can only be set on creation. See MSSQL User Guide for more information.</td>
<td>

`string`</td>
<td>

`""`</td>
<td>no</td>
</tr>
<tr>
<td>use_parameter_group_name_prefix</td>
<td>Whether to use the parameter group name prefix or not</td>
<td>

`bool`</td>
<td>

`true`</td>
<td>no</td>
</tr>
<tr>
<td>username</td>
<td>Username for the master DB user</td>
<td>

`string`</td>
<td>

n/a</td>
<td>yes</td>
</tr>
<tr>
<td>vpc_security_group_ids</td>
<td>List of VPC security groups to associate</td>
<td>

`list(string)`</td>
<td>

`[]`</td>
<td>no</td>
</tr>
</table>

## Outputs

| Name | Description |
|------|-------------|
| this\_db\_instance\_address | The address of the RDS instance |
| this\_db\_instance\_arn | The ARN of the RDS instance |
| this\_db\_instance\_availability\_zone | The availability zone of the RDS instance |
| this\_db\_instance\_endpoint | The connection endpoint |
| this\_db\_instance\_hosted\_zone\_id | The canonical hosted zone ID of the DB instance (to be used in a Route 53 Alias record) |
| this\_db\_instance\_id | The RDS instance ID |
| this\_db\_instance\_name | The database name |
| this\_db\_instance\_password | The database password (this password may be old, because Terraform doesn't track it after initial creation) |
| this\_db\_instance\_port | The database port |
| this\_db\_instance\_resource\_id | The RDS Resource ID of this instance |
| this\_db\_instance\_status | The RDS instance status |
| this\_db\_instance\_username | The master username for the database |
| this\_db\_option\_group\_arn | The ARN of the db option group |
| this\_db\_option\_group\_id | The db option group id |
| this\_db\_parameter\_group\_arn | The ARN of the db parameter group |
| this\_db\_parameter\_group\_id | The db parameter group id |
| this\_db\_subnet\_group\_arn | The ARN of the db subnet group |
| this\_db\_subnet\_group\_id | The db subnet group name |
