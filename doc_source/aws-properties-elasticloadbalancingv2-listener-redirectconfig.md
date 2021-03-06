# Elastic Load Balancing Listener RedirectConfig<a name="aws-properties-elasticloadbalancingv2-listener-redirectconfig"></a>

<a name="aws-properties-elasticloadbalancingv2-listener-redirectconfig-description"></a>The `RedirectConfig` property type specifies information about a redirect action\.

<a name="aws-properties-elasticloadbalancingv2-listener-redirectconfig-inheritance"></a> `RedirectConfig` is a property of the [Elastic Load Balancing Listener Action](aws-properties-elasticloadbalancingv2-listener-defaultactions.md) property type\.

## Syntax<a name="aws-properties-elasticloadbalancingv2-listener-redirectconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-elasticloadbalancingv2-listener-redirectconfig-syntax.json"></a>

```
{
  "[Host](#cfn-elasticloadbalancingv2-listener-redirectconfig-host)" : String,
  "[Path](#cfn-elasticloadbalancingv2-listener-redirectconfig-path)" : Integer,
  "[Port](#cfn-elasticloadbalancingv2-listener-redirectconfig-port)" : Integer,
  "[Protocol](#cfn-elasticloadbalancingv2-listener-redirectconfig-protocol)" : String,
  "[Query](#cfn-elasticloadbalancingv2-listener-redirectconfig-query)" : Integer,
  "[StatusCode](#cfn-elasticloadbalancingv2-listener-redirectconfig-statuscode)" : Integer
}
```

### YAML<a name="aws-properties-elasticloadbalancingv2-listener-redirectconfig-syntax.yaml"></a>

```
[Host](#cfn-elasticloadbalancingv2-listener-redirectconfig-host): String
[Path](#cfn-elasticloadbalancingv2-listener-redirectconfig-path): String
[Port](#cfn-elasticloadbalancingv2-listener-redirectconfig-port): String
[Protocol](#cfn-elasticloadbalancingv2-listener-redirectconfig-protocol): String
[Query](#cfn-elasticloadbalancingv2-listener-redirectconfig-query): String
[StatusCode](#cfn-elasticloadbalancingv2-listener-redirectconfig-statuscode): String
```

## Properties<a name="aws-properties-elasticloadbalancingv2-listener-redirectconfig-properties"></a>

`Host`  <a name="cfn-elasticloadbalancingv2-listener-redirectconfig-host"></a>
The hostname\. This component is not percent\-encoded\. The hostname can contain \#\{host\}\.  
Length Constraints: Minimum length of 1\. Maximum length of 128\.  
 *Required*: No  
 *Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Path`  <a name="cfn-elasticloadbalancingv2-listener-redirectconfig-path"></a>
The absolute path, starting with the leading "/"\. This component is not percent\-encoded\. The path can contain \#\{host\}, \#\{path\}, and \#\{port\}\.  
Length Constraints: Minimum length of 1\. Maximum length of 128\.  
 *Required*: No  
 *Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Port`  <a name="cfn-elasticloadbalancingv2-listener-redirectconfig-port"></a>
The port\. You can specify a value from 1 to 65535 or \#\{port\}\.  
 *Required*: No  
 *Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Protocol`  <a name="cfn-elasticloadbalancingv2-listener-redirectconfig-protocol"></a>
The protocol\. You can specify HTTP, HTTPS, or \#\{protocol\}\. You can redirect HTTP to HTTP, HTTP to HTTPS, and HTTPS to HTTPS\. You cannot redirect HTTPS to HTTP\.  
Pattern: `^(HTTPS?|#\{protocol\})$`  
 *Required*: No  
 *Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Query`  <a name="cfn-elasticloadbalancingv2-listener-redirectconfig-query"></a>
The query parameters, URL\-encoded when necessary, but not percent\-encoded\. Do not include the leading "?", as it is automatically added\. You can specify any of the reserved keywords\.  
Length Constraints: Minimum length of 0\. Maximum length of 128\.  
 *Required*: No  
 *Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`StatusCode`  <a name="cfn-elasticloadbalancingv2-listener-redirectconfig-statuscode"></a>
The HTTP redirect code\. The redirect is either permanent \(HTTP 301\) or temporary \(HTTP 302\)\.  
Valid Values: `HTTP_301` \| `HTTP_302`  
 *Required*: Yes  
 *Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

## See Also<a name="aws-properties-elasticloadbalancingv2-listener-redirectconfig-seealso"></a>
+ [RedirectActionConfig](https://docs.aws.amazon.com/elasticloadbalancing/latest/APIReference/API_RedirectActionConfig.html) in the *Elastic Load Balancing API Reference version 2015\-12\-01*