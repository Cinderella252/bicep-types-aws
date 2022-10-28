# AWS.Batch @ default

## Resource AWS.Batch/ComputeEnvironment@default
* **Valid Scope(s)**: Unknown
### Properties
* **properties**: [AWS.Batch/ComputeEnvironmentProperties](#awsbatchcomputeenvironmentproperties) (Required): properties of the resource

## Resource AWS.Batch/JobQueue@default
* **Valid Scope(s)**: Unknown
### Properties
* **properties**: [AWS.Batch/JobQueueProperties](#awsbatchjobqueueproperties) (Required): properties of the resource

## Resource AWS.Batch/SchedulingPolicy@default
* **Valid Scope(s)**: Unknown
### Properties
* **properties**: [AWS.Batch/SchedulingPolicyProperties](#awsbatchschedulingpolicyproperties): properties of the resource

## AWS.Batch/ComputeEnvironmentProperties
### Properties
* **ComputeEnvironmentArn**: string (ReadOnly)
* **ComputeEnvironmentName**: string
* **ComputeResources**: [ComputeResources](#computeresources)
* **ReplaceComputeEnvironment**: bool (WriteOnly)
* **ServiceRole**: string
* **State**: string
* **Tags**: [ComputeEnvironment_Tags](#computeenvironmenttags): A key-value pair to associate with a resource.
* **Type**: string (Required)
* **UnmanagedvCpus**: int
* **UpdatePolicy**: [UpdatePolicy](#updatepolicy)

## ComputeResources
### Properties
* **AllocationStrategy**: string
* **BidPercentage**: int
* **DesiredvCpus**: int
* **Ec2Configuration**: [Ec2ConfigurationObject](#ec2configurationobject)[]
* **Ec2KeyPair**: string
* **ImageId**: string
* **InstanceRole**: string
* **InstanceTypes**: string[]
* **LaunchTemplate**: [LaunchTemplateSpecification](#launchtemplatespecification)
* **MaxvCpus**: int (Required)
* **MinvCpus**: int
* **PlacementGroup**: string
* **SecurityGroupIds**: string[]
* **SpotIamFleetRole**: string
* **Subnets**: string[] (Required)
* **Tags**: [ComputeEnvironment_Tags](#computeenvironmenttags): A key-value pair to associate with a resource.
* **Type**: string (Required)
* **UpdateToLatestImageVersion**: bool (WriteOnly)

## Ec2ConfigurationObject
### Properties
* **ImageIdOverride**: string
* **ImageType**: string (Required)

## LaunchTemplateSpecification
### Properties
* **LaunchTemplateId**: string
* **LaunchTemplateName**: string
* **Version**: string

## ComputeEnvironment_Tags
### Properties

## ComputeEnvironment_Tags
### Properties

## UpdatePolicy
### Properties
* **JobExecutionTimeoutMinutes**: int
* **TerminateJobsOnUpdate**: bool

## AWS.Batch/JobQueueProperties
### Properties
* **ComputeEnvironmentOrder**: [ComputeEnvironmentOrder](#computeenvironmentorder)[] (Required)
* **JobQueueArn**: [ResourceArn](#resourcearn) (ReadOnly)
* **JobQueueName**: string
* **Priority**: int (Required)
* **SchedulingPolicyArn**: [ResourceArn](#resourcearn)
* **State**: string
* **Tags**: [JobQueue_Tags](#jobqueuetags): A key-value pair to associate with a resource.

## ComputeEnvironmentOrder
### Properties
* **ComputeEnvironment**: string (Required)
* **Order**: int (Required)

## ResourceArn
### Properties

## JobQueue_Tags
### Properties

## AWS.Batch/SchedulingPolicyProperties
### Properties
* **Arn**: [ResourceArn](#resourcearn) (ReadOnly)
* **FairsharePolicy**: [FairsharePolicy](#fairsharepolicy)
* **Name**: string: Name of Scheduling Policy.
* **Tags**: [SchedulingPolicy_Tags](#schedulingpolicytags): A key-value pair to associate with a resource.

## ResourceArn
### Properties

## FairsharePolicy
### Properties
* **ComputeReservation**: int
* **ShareDecaySeconds**: int
* **ShareDistribution**: [ShareAttributes](#shareattributes)[]: List of Share Attributes

## ShareAttributes
### Properties
* **ShareIdentifier**: string
* **WeightFactor**: int

## SchedulingPolicy_Tags
### Properties
