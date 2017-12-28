# AWS::Elasticsearch::Domain<a name="aws-resource-elasticsearch-domain"></a>

The `AWS::Elasticsearch::Domain` resource creates an Amazon Elasticsearch Service \(Amazon ES\) domain that encapsulates the Amazon ES engine instances\. For more information, see [CreateElasticsearchDomain](http://docs.aws.amazon.com/elasticsearch-service/latest/developerguide/es-configuration-api.html#es-configuration-api-actions-createelasticsearchdomain) in the *Amazon Elasticsearch Service Developer Guide*\.


+ [Syntax](#aws-resource-elasticsearch-domain-syntax)
+ [Properties](#w3ab2c21c10d611b9)
+ [Return Values](#w3ab2c21c10d611c11)
+ [Examples](#aws-resource-elasticsearch-domain-examples)

## Syntax<a name="aws-resource-elasticsearch-domain-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-elasticsearch-domain-syntax.json"></a>

```
{
  "Type" : "AWS::Elasticsearch::Domain",
  "Properties" : {
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticsearch-domain-accesspolicies)" : JSON object,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticsearch-domain-advancedoptions)" : { String:String, ... },
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticsearch-domain-domainname)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticsearch-domain-ebsoptions)" : EBSOptions,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticsearch-domain-elasticsearchclusterconfig)" : ElasticsearchClusterConfig,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticsearch-domain-elasticsearchversion)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticsearch-domain-snapshotoptions)" : SnapshotOptions,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticsearch-domain-tags)" : [ Resource Tag, ... ],
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticsearch-domain-vpcoptions)" : VPCOptions
  }
}
```

### YAML<a name="aws-resource-elasticsearch-domain-syntax.yaml"></a>

```
Type: "AWS::Elasticsearch::Domain"
Properties: 
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticsearch-domain-accesspolicies): JSON object
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticsearch-domain-advancedoptions):
    String: String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticsearch-domain-domainname): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticsearch-domain-ebsoptions):
    EBSOptions
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticsearch-domain-elasticsearchclusterconfig):
    ElasticsearchClusterConfig
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticsearch-domain-elasticsearchversion): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticsearch-domain-snapshotoptions):
    SnapshotOptions
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticsearch-domain-tags):
    - Resource Tag
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticsearch-domain-vpcoptions): 
    VPCOptions
```

## Properties<a name="w3ab2c21c10d611b9"></a>

`AccessPolicies`  
An AWS Identity and Access Management \(IAM\) policy document that specifies who can access the Amazon ES domain and their permissions\. For more information, see [Configuring Access Policies](http://docs.aws.amazon.com/elasticsearch-service/latest/developerguide/es-createupdatedomains.html#es-createdomain-configure-access-policies) in the *Amazon Elasticsearch Service Developer Guide*\.  
*Required: *No  
*Type*: JSON object  
*Update requires*: No interruption

`AdvancedOptions`  
Additional options to specify for the Amazon ES domain\. For more information, see [Configuring Advanced Options](http://docs.aws.amazon.com/elasticsearch-service/latest/developerguide/es-createupdatedomains.html#es-createdomain-configure-advanced-options) in the *Amazon Elasticsearch Service Developer Guide*\.  
*Required: *No  
*Type*: A JSON object that consists of a string key\-value pair, such as:  

```
{
  "rest.action.multi.allow_explicit_index": "true"
}
```
*Update requires*: Replacement

`DomainName`  
A name for the Amazon ES domain\. For valid values, see the [DomainName](http://docs.aws.amazon.com/elasticsearch-service/latest/developerguide/es-configuration-api.html#es-configuration-api-datatypes-domainname) data type in the *Amazon Elasticsearch Service Developer Guide*\.  
If you don't specify a name, AWS CloudFormation generates a unique physical ID and uses that ID for the domain name\. For more information, see [Name Type](aws-properties-name.md)\.  
If you specify a name, you cannot perform updates that require replacement of this resource\. You can perform updates that require no or some interruption\. If you must replace the resource, specify a new name\.
*Required: *No  
*Type*: String  
*Update requires*: Replacement

`EBSOptions`  
The configurations of Amazon Elastic Block Store \(Amazon EBS\) volumes that are attached to data nodes in the Amazon ES domain\. For more information, see [Configuring EBS\-based Storage](http://docs.aws.amazon.com/elasticsearch-service/latest/developerguide/es-createupdatedomains.html#es-createdomain-configure-ebs) in the *Amazon Elasticsearch Service Developer Guide*\.  
*Required: *No  
*Type*: [Amazon ES Domain EBSOptions](aws-properties-elasticsearch-domain-ebsoptions.md)  
*Update requires*: No interruption

`ElasticsearchClusterConfig`  
The cluster configuration for the Amazon ES domain\. You can specify options such as the instance type and the number of instances\. For more information, see [Configuring Amazon ES Domains](http://docs.aws.amazon.com/elasticsearch-service/latest/developerguide/es-createupdatedomains.html#es-createdomains-configure-cluster-cli) in the *Amazon Elasticsearch Service Developer Guide*\.  
*Required: *No  
*Type*: [Amazon ES Domain ElasticsearchClusterConfig](aws-properties-elasticsearch-domain-elasticsearchclusterconfig.md)  
*Update requires*: No interruption

`ElasticsearchVersion`  
The version of Elasticsearch to use, such as `2.3`\. For information about the versions that Amazon ES supports, see the `Elasticsearch-Version` parameter for the [CreateElasticsearchDomain](http://docs.aws.amazon.com/elasticsearch-service/latest/developerguide/es-configuration-api.html#es-configuration-api-actions-createelasticsearchdomain) action in the *Amazon Elasticsearch Service Developer Guide*\.  
*Required: *No  
*Type*: String  
*Update requires*: Replacement

`SnapshotOptions`  
The automated snapshot configuration for the Amazon ES domain indices\.  
*Required: *No  
*Type*: [Amazon ES Domain SnapshotOptions](aws-properties-elasticsearch-domain-snapshotoptions.md)  
*Update requires*: No interruption

`Tags`  
An arbitrary set of tags \(key–value pairs\) to associate with the Amazon ES domain\.  
*Required: *No  
*Type*:   
*Update requires*: No interruption

`VPCOptions`  
The virtual private cloud \(VPC\) configuration for the Amazon ES domain\. For more information, see [VPC Support for Amazon Elasticsearch Service Domains](http://docs.aws.amazon.com/elasticsearch-service/latest/developerguide/es-vpc.html) in the *Amazon Elasticsearch Service Developer Guide*\.  
 *Required*: No  
 *Type*: [Amazon ES Domain VPCOptions](aws-properties-elasticsearch-domain-vpcoptions.md)  
 *Update requires*: No interruption 

## Return Values<a name="w3ab2c21c10d611c11"></a>

### Ref<a name="w3ab2c21c10d611c11b2"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the resource name, such as `mystack-elasticsea-abc1d2efg3h4`\.

For more information about using the `Ref` function, see Ref\.

### Fn::GetAtt<a name="w3ab2c21c10d611c11b4"></a>

`Fn::GetAtt` returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

`DomainArn`  
The Amazon Resource Name \(ARN\) of the domain, such as `arn:aws:es:us-west-2:123456789012:domain/mystack-elasti-1ab2cdefghij`\.

`DomainEndpoint`  
The domain\-specific endpoint that's used to submit index, search, and data upload requests to an Amazon ES domain, such as `search-mystack-elasti-1ab2cdefghij-ab1c2deckoyb3hofw7wpqa3cm.us-west-2.es.amazonaws.com`\.

For more information about using `Fn::GetAtt`, see Fn::GetAtt\.

## Examples<a name="aws-resource-elasticsearch-domain-examples"></a>

### <a name="w3ab2c21c10d611c13b2"></a>

The following examples create an Amazon ES domain that contains two data nodes and three master nodes\. Automated snapshots of the indices are taken daily between midnight and 1:00 AM \(UTC\)\. The access policy permits the IAM user `es-user` to take all Amazon ES actions on the domain, such as `es:UpdateElasticsearchDomainConfig`\.

#### JSON<a name="aws-resource-elasticsearch-domain-example.json"></a>

```
"ElasticsearchDomain": {
  "Type": "AWS::Elasticsearch::Domain",
  "Properties": {
    "DomainName": "test",
    "ElasticsearchClusterConfig": {
      "DedicatedMasterEnabled": "true",
      "InstanceCount": "2",
      "ZoneAwarenessEnabled": "true",
      "InstanceType": "m3.medium.elasticsearch",
      "DedicatedMasterType": "m3.medium.elasticsearch",
      "DedicatedMasterCount": "3"
    },
    "EBSOptions": {
      "EBSEnabled": true,
      "Iops": 0,
      "VolumeSize": 20,
      "VolumeType": "gp2"
    },
    "SnapshotOptions": {
      "AutomatedSnapshotStartHour": "0"
    },
    "AccessPolicies": {
      "Version": "2012-10-17",
      "Statement": [{
        "Effect": "Allow",
        "Principal": {
          "AWS": "arn:aws:iam::123456789012:user/es-user"
        },
        "Action": "es:*",
        "Resource": "arn:aws:es:us-east-1:123456789012:domain/test/*"
      }]
    },
    "AdvancedOptions": {
      "rest.action.multi.allow_explicit_index": "true"
    }
  }
}
```

#### YAML<a name="aws-resource-elasticsearch-domain-example.yaml"></a>

```
ElasticsearchDomain: 
  Type: "AWS::Elasticsearch::Domain"
  Properties:
    DomainName: "test"
    ElasticsearchClusterConfig: 
      DedicatedMasterEnabled: "true"
      InstanceCount: "2"
      ZoneAwarenessEnabled: "true"
      InstanceType: "m3.medium.elasticsearch"
      DedicatedMasterType: "m3.medium.elasticsearch"
      DedicatedMasterCount: "3"
    EBSOptions: 
      EBSEnabled: true
      Iops: 0
      VolumeSize: 20
      VolumeType: "gp2"
    SnapshotOptions: 
      AutomatedSnapshotStartHour: "0"
    AccessPolicies: 
      Version: "2012-10-17"
      Statement: 
        - 
          Effect: "Allow"
          Principal: 
            AWS: "arn:aws:iam::123456789012:user/es-user"
          Action: "es:*"
          Resource: "arn:aws:es:us-east-1:846973539254:domain/test/*"
    AdvancedOptions: 
      rest.action.multi.allow_explicit_index: "true"
```

### <a name="aws-resource-elasticsearch-domain-example2"></a>

The following example creates a domain with VPC options\.

#### JSON<a name="aws-resource-elasticsearch-domain-example2.json"></a>

```
{
  "AWSTemplateFormatVersion": "2010-09-09",
  "Description": "ElasticsearchDomain resource",
  "Parameters": {
    "DomainName" : {
      "Description" : "User defined Elasticsearch Domain name",
      "Type" : "String"
    },
    "ElasticsearchVersion" : {
      "Description" : "User defined Elasticsearch Version",
      "Type" : "String"
    },
    "InstanceType" : {
      "Type" : "String"
    },
    "AvailabilityZone" : {
      "Type" : "String"
    },
    "CidrBlock" : {
      "Type" : "String"
    },
    "GroupDescription" : {
      "Type" : "String"
    },
    "SGName" : {
      "Type" : "String"
    }
  },
  "Resources": {
    "ElasticsearchDomain": {
      "Type": "AWS::Elasticsearch::Domain",
      "Properties": {
        "DomainName": { "Ref": "DomainName" },
        "ElasticsearchVersion": { "Ref": "ElasticsearchVersion" },
        "ElasticsearchClusterConfig": {
          "InstanceCount": "1",
          "InstanceType": { "Ref": "InstanceType" }
        },
        "EBSOptions": {
          "EBSEnabled" : "true",
          "Iops" : 0,
          "VolumeSize" : 10,
          "VolumeType" : "standard"
        },
        "SnapshotOptions": {
          "AutomatedSnapshotStartHour": "0"
        },
        "AccessPolicies": {
          "Version": "2012-10-17",
          "Statement": [{
            "Effect": "Deny",
            "Principal": {
              "AWS": "*"
            },
            "Action": "es:*",
            "Resource": "*"
          }]
        },
        "AdvancedOptions": {
          "rest.action.multi.allow_explicit_index": "true"
        },
        "Tags": [{
          "Key": "foo",
          "Value": "bar"
        }],
        "VPCOptions" : {
          "SubnetIds" : [
            {"Ref" : "subnet"}
          ],
          "SecurityGroupIds" : [
            {"Ref" : "mySecurityGroup"}
          ]
        }
      }
    },
    "vpc" : {
      "Type" : "AWS::EC2::VPC",
      "Properties" : {
        "CidrBlock" : "10.0.0.0/16"
      }
    },
    "subnet" : {
      "Type" : "AWS::EC2::Subnet",
      "Properties" : {
        "VpcId" : {"Ref": "vpc"},
        "CidrBlock" : {"Ref" : "CidrBlock"},
        "AvailabilityZone" : {"Ref" : "AvailabilityZone"}
      }
    },
    "mySecurityGroup": {
      "Type": "AWS::EC2::SecurityGroup",
      "Properties": {
        "GroupDescription": {"Ref" : "GroupDescription"},
        "VpcId" : {"Ref" : "vpc"},
        "GroupName": {"Ref" : "SGName"},
        "SecurityGroupIngress": [
          {
            "FromPort": "443",
            "IpProtocol": "tcp",
            "ToPort": "443",
            "CidrIp": "0.0.0.0/0"
          }
        ]
      }
    }
  },
  "Outputs": {
    "DomainArn": {
      "Value": {
        "Fn::GetAtt": ["ElasticsearchDomain", "DomainArn"]
      }
    },
    "DomainEndpoint": {
      "Value": {
        "Fn::GetAtt": ["ElasticsearchDomain", "DomainEndpoint"]
      }
    },
    "SecurityGroupId": {
      "Value": {
        "Ref": "mySecurityGroup"
      }
    },
    "SubnetId": {
      "Value": {
        "Ref": "subnet"
      }
    }
  }
}
```

#### YAML<a name="aws-resource-elasticsearch-domain-example2.yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Description: ElasticsearchDomain resource
Parameters:
  DomainName:
    Description: User defined Elasticsearch Domain name
    Type: String
  ElasticsearchVersion:
    Description: User defined Elasticsearch Version
    Type: String
  InstanceType:
    Type: String
  AvailabilityZone:
    Type: String
  CidrBlock:
    Type: String
  GroupDescription:
    Type: String
  SGName:
    Type: String
Resources:
  ElasticsearchDomain:
    Type: 'AWS::Elasticsearch::Domain'
    Properties:
      DomainName: !Ref DomainName
      ElasticsearchVersion: !Ref ElasticsearchVersion
      ElasticsearchClusterConfig:
        InstanceCount: '1'
        InstanceType: !Ref InstanceType
      EBSOptions:
        EBSEnabled: 'true'
        Iops: 0
        VolumeSize: 10
        VolumeType: standard
      SnapshotOptions:
        AutomatedSnapshotStartHour: '0'
      AccessPolicies:
        Version: 2012-10-17
        Statement:
          - Effect: Deny
            Principal:
              AWS: '*'
            Action: 'es:*'
            Resource: '*'
      AdvancedOptions:
        rest.action.multi.allow_explicit_index: 'true'
      Tags:
        - Key: foo
          Value: bar
      VPCOptions:
        SubnetIds:
          - !Ref subnet
        SecurityGroupIds:
          - !Ref mySecurityGroup
  vpc:
    Type: 'AWS::EC2::VPC'
    Properties:
      CidrBlock: 10.0.0.0/16
  subnet:
    Type: 'AWS::EC2::Subnet'
    Properties:
      VpcId: !Ref vpc
      CidrBlock: !Ref CidrBlock
      AvailabilityZone: !Ref AvailabilityZone
  mySecurityGroup:
    Type: 'AWS::EC2::SecurityGroup'
    Properties:
      GroupDescription: !Ref GroupDescription
      VpcId: !Ref vpc
      GroupName: !Ref SGName
      SecurityGroupIngress:
        - FromPort: '443'
          IpProtocol: tcp
          ToPort: '443'
          CidrIp: 0.0.0.0/0
Outputs:
  DomainArn:
    Value: !GetAtt ElasticsearchDomain.DomainArn
  DomainEndpoint:
    Value: !GetAtt ElasticsearchDomain.DomainEndpoint
  SecurityGroupId:
    Value: !Ref mySecurityGroup
  SubnetId:
    Value: !Ref subnet
```