# AWS IoT Greengrass ResourceDefinition SecretsManagerSecretResourceData<a name="aws-properties-greengrass-resourcedefinition-secretsmanagersecretresourcedata"></a>

<a name="aws-properties-greengrass-resourcedefinition-secretsmanagersecretresourcedata-description"></a>Settings for a secret resource, which references a secret from Secrets Manager\. AWS IoT Greengrass stores a local, encrypted copy of the secret on the Greengrass core, where it can be securely accessed by connectors and Lambda functions\. For more information, see [Deploy Secrets to the AWS IoT Greengrass Core](https://docs.aws.amazon.com/greengrass/latest/developerguide/secrets.html) in the *AWS IoT Greengrass Developer Guide*\.

<a name="aws-properties-greengrass-resourcedefinition-secretsmanagersecretresourcedata-inheritance"></a> In an AWS CloudFormation template, `SecretsManagerSecretResourceData` can be used in the [ResourceDataContainer](aws-properties-greengrass-resourcedefinition-resourcedatacontainer.md) property type\.

## Syntax<a name="aws-properties-greengrass-resourcedefinition-secretsmanagersecretresourcedata-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-greengrass-resourcedefinition-secretsmanagersecretresourcedata-syntax.json"></a>

```
{
  "[ARN](#cfn-greengrass-resourcedefinition-secretsmanagersecretresourcedata-arn)" : String,
  "[AdditionalStagingLabelsToDownload](#cfn-greengrass-resourcedefinition-secretsmanagersecretresourcedata-additionalstaginglabelstodownload)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-greengrass-resourcedefinition-secretsmanagersecretresourcedata-syntax.yaml"></a>

```
[ARN](#cfn-greengrass-resourcedefinition-secretsmanagersecretresourcedata-arn): String
[AdditionalStagingLabelsToDownload](#cfn-greengrass-resourcedefinition-secretsmanagersecretresourcedata-additionalstaginglabelstodownload): 
  - String
```

## Properties<a name="aws-properties-greengrass-resourcedefinition-secretsmanagersecretresourcedata-properties"></a>

`ARN`  <a name="cfn-greengrass-resourcedefinition-secretsmanagersecretresourcedata-arn"></a>
The Amazon Resource Name \(ARN\) of the Secrets Manager secret to make available on the core\. The value of the secret's latest version \(represented by the `AWSCURRENT` staging label\) is included by default\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`AdditionalStagingLabelsToDownload`  <a name="cfn-greengrass-resourcedefinition-secretsmanagersecretresourcedata-additionalstaginglabelstodownload"></a>
The staging labels whose values you want to make available on the core, in addition to `AWSCURRENT`\.  
 *Required*: No  
 *Type*: List of String values  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

## See Also<a name="aws-properties-greengrass-resourcedefinition-secretsmanagersecretresourcedata-seealso"></a>
+ [SecretsManagerSecretResourceData](https://docs.aws.amazon.com/greengrass/latest/apireference/definitions-secretsmanagersecretresourcedata.html) in the *AWS IoT Greengrass API Reference*
+ [AWS IoT Greengrass Developer Guide](https://docs.aws.amazon.com/greengrass/latest/developerguide/)