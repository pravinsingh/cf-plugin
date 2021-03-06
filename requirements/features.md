### Authoring valid templates

- [x] As a developer,
  - I want the specification of, and validation of supported AWS resource types, 
  - (such as ```AWS::EC2::Instance```),
  - So I can ensure valid resource elements in the template.

- [x] As a developer,
  - I want the specification of, and validation of the supported types for Parameters in a template, 
  - (such as 'String', as well as AWS-specific parameter types such as ```AWS::EC2::KeyPair::KeyPairName```),
  - So I can specify Property elements accurately in the template.

- As a developer,
  - I want assistance with validating Parameter values in a template,
  - (including ```AllowedPattern```, ```AllowedValues```, ```ConstraintDescription```, and so on),
  - So I can specify Property elements accurately in the template.

- As a developer,
  - I want to get a listing of, and description of various Property keys required for an AWS resource type,
  - (such as ```ImageId```, ```InstanceType```, etc. for ```AWS::EC2::Instance```),
  - So I can ensure valid resource elements in the template.

- As a developer,
  - I want the specification of, and validation of supported values for properties in a resource element for an AWS resource type,
  - when such values belong to an enumeration,
  - (such as the allowed values: [```host```, ```default```] for the property ```Affinity``` for a resource of type ```AWS::EC2::Instance```),
  - So I can ensure valid resource elements in the template.

- As a developer,
  - I want assistance with values for properties in a resource element for an AWS resource type,
  - where values refer to resource configuration from the user's AWS account(s),
  - (such as the values of ```ImageId``` property for a resource of type ```AWS::EC2::Instance```),
  - So I can ensure valid resource elements in the template.
  
- As a developer,
  - I want the specification of, and validation of the required, conditionally required, optional, or mutually exclusive Property keys for an AWS resource type,
  - [x] (such as 'ImageId' is required for 'AWS::EC2::Instance'),
  - [x] (such as 'InstanceInitiatedShutdownBehavior' is optional for 'AWS::EC2::Instance'),
  - [ ] (such as 'SecurityGroupIds' is conditionally required when specifying a VPC Security Group for 'AWS::EC2::Instance'),
  - [ ] (such as a value of 'dedicated' or 'host' is only allowed for 'Tenancy' if the resource of Type 'AWS::EC2::Instance' is being launched in a VPC, therefore requiring one or more of "SecurityGroupIds" and/or "SubnetId", etc.),
  - [ ] (such as: specify either the 'NetworkInterfaces' property or 'SubnetId' property, but not both for 'AWS::EC2::Instance'),
  - So I can ensure valid resource elements in the template.

- [x] As a developer,
  - I want assistance on, as well as validation of the particular syntax applicable to declaring Property values in a template, 
  - (such as 'scalar' values of Type 'String', lists, and intrinsic functions including references),
  - So I can ensure valid resource elements in the template.

- [x] As a developer,
  - I want assistance on, as well as validation of embedded Property types for Property values for a resource,
  - (such as the embedded property type 'EC2 Network Interface' for the property 'NetworkInterfaces' for 'AWS::EC2::Instance')
  - So I can ensure valid resource elements in the template. 

- [ ] As a developer,
  - I want assistance on, as well as validation of the particular Attributes available for a given Resource type,
  - When the same Resource is referenced (by logical Id) as part of an Output element,
  - So I can ensure valid output elements in the template

### Creating and managing stacks

- [ ] As a user of a CloudFormation template,
  - I want to generate a stub file for Parameters required for a template,
  - So I can rapidly supply all of the parameter values required to create a stack from the template.

- [ ] As a developer,
  - I want to automatically validate the parameter values supplied for a template, against any requirements that can be verified offline,
  - So I can screen for inaccurate parameter values before attempting to create stacks.

### Visual aspects

- [ ] As a developer,
  - I want to visually distinguish between various elements of a template,
  - So I can understand templates at a glance.

- [ ] The various elements of a CloudFormation template are as follows:
  - Top-level elements: Parameters, Mappings, Resources, Metadata, Outputs, etc.
  - Resource logical Ids: declaration, as well as references
  - Property names, property values, pseudo-parameters
  - Intrinsic functions
  - Return values for a resource element

- [ ] As a developer or user of a CloudFormation template,
  - I want to be alerted to possible issues with a template with visual and descriptive warnings,
  - So I can respond to these warnings and make any necessary changes to the template.

- [ ] Warnings may indicate the presence of errors around:
  - missing elements or Property
  - typos with well-known elements
  - incorrect values for a Resource Type, or a Property value, or a Parameter property, etc.
  - references to missing elements, or misspelt references

### Navigation

- [ ] As a developer,
  - I want to identify all references to an element (such as a resource, or a parameter) in a template,
  - So I can identify the usage of such elements across the template.

- [ ] As a developer,
  - I want to navigate to (and between) any and all references to an element in the template (such as a resource, or a parameter), and the declaration of such element
  - So I can work with either the references or the declaration of such elements.

### Refactoring

- [ ] As a developer,
  - I want to rename a Resource (logical id) or a Parameter (name), and get assistance in renaming any references to the same,
  - So I can rapidly make changes to template elements in a consistent fashion.

- [ ] As a developer,
  - I want to know whether changes to a particular Property for a given Resource will result in stack updates that involve either "No interruption", "Some interruption", or "Replacement",
  - So I can decide on how to make template changes with reference to the impact on existing stacks that may be updated for the template changes.
