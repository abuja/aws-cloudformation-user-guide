# AWS::ElasticLoadBalancingV2::LoadBalancer LoadBalancerAttribute<a name="aws-properties-elasticloadbalancingv2-loadbalancer-loadbalancerattributes"></a>

Specifies an attribute for an Application Load Balancer or a Network Load Balancer\.

## Syntax<a name="aws-properties-elasticloadbalancingv2-loadbalancer-loadbalancerattributes-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-elasticloadbalancingv2-loadbalancer-loadbalancerattributes-syntax.json"></a>

```
{
  "[Key](#cfn-elasticloadbalancingv2-loadbalancer-loadbalancerattributes-key)" : String,
  "[Value](#cfn-elasticloadbalancingv2-loadbalancer-loadbalancerattributes-value)" : String
}
```

### YAML<a name="aws-properties-elasticloadbalancingv2-loadbalancer-loadbalancerattributes-syntax.yaml"></a>

```
  [Key](#cfn-elasticloadbalancingv2-loadbalancer-loadbalancerattributes-key): String
  [Value](#cfn-elasticloadbalancingv2-loadbalancer-loadbalancerattributes-value): String
```

## Properties<a name="aws-properties-elasticloadbalancingv2-loadbalancer-loadbalancerattributes-properties"></a>

`Key`  <a name="cfn-elasticloadbalancingv2-loadbalancer-loadbalancerattributes-key"></a>
The name of the attribute\.  
The following attributes are supported by both Application Load Balancers and Network Load Balancers:  
+  `access_logs.s3.enabled` \- Indicates whether access logs are enabled\. The value is `true` or `false`\. The default is `false`\.
+  `access_logs.s3.bucket` \- The name of the S3 bucket for the access logs\. This attribute is required if access logs are enabled\. The bucket must exist in the same region as the load balancer and have a bucket policy that grants Elastic Load Balancing permissions to write to the bucket\.
+  `access_logs.s3.prefix` \- The prefix for the location in the S3 bucket for the access logs\.
+  `deletion_protection.enabled` \- Indicates whether deletion protection is enabled\. The value is `true` or `false`\. The default is `false`\.
The following attributes are supported by only Application Load Balancers:  
+  `idle_timeout.timeout_seconds` \- The idle timeout value, in seconds\. The valid range is 1\-4000 seconds\. The default is 60 seconds\.
+  `routing.http2.enabled` \- Indicates whether HTTP/2 is enabled\. The value is `true` or `false`\. The default is `true`\.
The following attributes are supported by only Network Load Balancers:  
+  `load_balancing.cross_zone.enabled` \- Indicates whether cross\-zone load balancing is enabled\. The value is `true` or `false`\. The default is `false`\.
*Required*: No  
*Type*: String  
*Maximum*: `256`  
*Pattern*: `^[a-zA-Z0-9._]+$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Value`  <a name="cfn-elasticloadbalancingv2-loadbalancer-loadbalancerattributes-value"></a>
The value of the attribute\.  
*Required*: No  
*Type*: String  
*Maximum*: `1024`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See Also<a name="aws-properties-elasticloadbalancingv2-loadbalancer-loadbalancerattributes--seealso"></a>
+  [ModifyLoadBalancerAttributes](https://docs.aws.amazon.com/elasticloadbalancing/latest/APIReference/API_ModifyLoadBalancerAttributes.html) in the *Elastic Load Balancing API Reference \(version 2015\-12\-01\)* 
+  [Load Balancer Attributes](https://docs.aws.amazon.com/elasticloadbalancing/latest/application/application-load-balancers.html#load-balancer-attributes) in the *User Guide for Application Load Balancers* 
+  [Load Balancer Attributes](https://docs.aws.amazon.com/elasticloadbalancing/latest/network/network-load-balancers.html#load-balancer-attributes) in the *User Guide for Network Load Balancers* 