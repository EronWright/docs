
---
title: "DomainExtension"
block_external_search_index: true
---



HTTPS listeners of guaranteed-performance SLB support configuring multiple certificates, allowing you to forward requests with different domain names to different backend servers.
Please refer to the [documentation](https://www.alibabacloud.com/help/doc-detail/85956.htm?spm=a2c63.p38356.b99.40.1c881563Co8p6w) for details.

> **NOTE:** Available in 1.60.0+

> **NOTE:** The instance with shared loadBalancerSpec doesn't support domainExtension.

## Example Usage

```typescript
import * as pulumi from "@pulumi/pulumi";
import * as alicloud from "@pulumi/alicloud";

const instance = new alicloud.slb.LoadBalancer("instance", {
    internet: true,
    internetChargeType: "PayByTraffic",
});
const foo = new alicloud.slb.ServerCertificate("foo", {
    privateKey: `-----BEGIN RSA PRIVATE KEY-----
MIIEowIBAAKCAQEAyjCheapjf7qDI3R9w/Gj0XFDgNLPK2aWIRvM25BdY/IB2KAf
xQ7zOxu3X1bMo2zMCzsSrwIVrxx0qRM/7e4AfkHcKwDIjCcBprQp164dhFol4GpT
HtcuGv0+Ue6vpuE9cxQE3/pG5x1n5EhheFu2+lAaGh/vUrUPeQp6szX/9qfzn+/k
tF8wsRV8PBiFc2ZNMRXupRyc2qtOn95r86w/uK6TuerU1L64E2P5+tYLBWT+39Ai
diUIenjURThFEn8Srvw8v/iLEMaKwiWNkOfWQH96166gzddOI8PT5cJy5an2c90T
DgzegVo8RPK70bU9KjH7gH79YIwXVmTdIVGAUQIDAQABAoIBAE1J4a/8biR5S3/W
G+03BYQeY8tuyjqw8FqfoeOcf9agwAvqybouSNQjeCk9qOQfxq/UWQQFK/zQR9gJ
v7pX7GBXFK5rkj3g+0SaQhRsPmRFgY0Tl8qGPt2aSKRRNVv5ZeADmwlzRn86QmiF
Mp0rkfqFfDTYWEepZszCML0ouzuxsW/9tq7rvtSjsgATNt31B3vFa3D3JBi31jUh
5nfR9A3bATze7mQw3byEDiVl5ASRDgYyur403P1fDnMy9DBHZ8NaPOsFF6OBpJal
BJsG5z00hll5PFN2jfmBQKlvAeU7wfwqdaSnGHOfqf2DeTTaFjIQ4gUhRn/m6pLo
6kXttLECgYEA9sng0Qz/TcPFfM4tQ1gyvB1cKnnGIwg1FP8sfUjbbEgjaHhA224S
k3BxtX2Kq6fhTXuwusAFc6OVMAZ76FgrQ5K4Ci7+DTsrF28z4b8td+p+lO/DxgP9
lTgN+ddsiTOV4fUef9Z3yY0Zr0CnBUMbQYRaV2UIbCdiB0G4V/bt9TsCgYEA0bya
Oo9wGI0RJV0bYP7qwO74Ra1/i1viWbRlS7jU37Q+AZstrlKcQ5CTPzOjKFKMiUzl
4miWacZ0/q2n+Mvd7NbXGXTLijahnyOYKaHJYyh4oBymfkgAifRstE0Ki9gdvArb
/I+emC0GvLSyfGN8UUeDJs4NmqdEXGqjo2JOV+MCgYALFv1MR5o9Y1u/hQBRs2fs
PiGDIx+9OUQxYloccyaxEfjNXAIGGkcpavchIbgWiJ++PJ2vdquIC8TLeK8evL+M
9M3iX0Q5UfxYvD2HmnCvn9D6Xl/cyRcfGnq+TGjrLW9BzSMGuZt+aiHKV0xqFx7l
bc4leTvMqGRmURS4lzcQOwKBgQCDzA/i4sYfN25h21tcHXSpnsG3D2rJyQi5NCo/
ZjunA92/JqOTGuiFcLGHEszhhtY3ZXJET1LNz18vtzKJnpqrvOnYXlOVW/U+SqDQ
8JDb1c/PVZGuY1KrXkR9HLiW3kz5IJ3S3PFdUVYdeTN8BQxXCyg4V12nJJtJs912
y0zN3wKBgGDS6YttCN6aI4EOABYE8fI1EYQ7vhfiYsaWGWSR1l6bQey7KR6M1ACz
ZzMASNyytVt12yXE4/Emv6/pYqigbDLfL1zQJSLJ3EHJYTh2RxjR+AaGDudYFG/T
liQ9YXhV5Iu2x1pNwrtFnssDdaaGpfA7l3xC00BL7Z+SAJyI4QKA
-----END RSA PRIVATE KEY-----`,
    serverCertificate: `-----BEGIN CERTIFICATE-----
MIIDdjCCAl4CCQCcm+erkcKN7DANBgkqhkiG9w0BAQsFADB9MQswCQYDVQQGEwJj
bjELMAkGA1UECAwCYmoxEDAOBgNVBAcMB2JlaWppbmcxDzANBgNVBAoMBmFsaXl1
bjELMAkGA1UECwwCc2MxFTATBgNVBAMMDHd3dy50ZXN0LmNvbTEaMBgGCSqGSIb3
DQEJARYLMTIzQDEyMy5jb20wHhcNMTkwNDI2MDM0ODAxWhcNMjQwNDI1MDM0ODAx
WjB9MQswCQYDVQQGEwJjbjELMAkGA1UECAwCYmoxEDAOBgNVBAcMB2JlaWppbmcx
DzANBgNVBAoMBmFsaXl1bjELMAkGA1UECwwCc2MxFTATBgNVBAMMDHd3dy50ZXN0
LmNvbTEaMBgGCSqGSIb3DQEJARYLMTIzQDEyMy5jb20wggEiMA0GCSqGSIb3DQEB
AQUAA4IBDwAwggEKAoIBAQDKMKF5qmN/uoMjdH3D8aPRcUOA0s8rZpYhG8zbkF1j
8gHYoB/FDvM7G7dfVsyjbMwLOxKvAhWvHHSpEz/t7gB+QdwrAMiMJwGmtCnXrh2E
WiXgalMe1y4a/T5R7q+m4T1zFATf+kbnHWfkSGF4W7b6UBoaH+9StQ95CnqzNf/2
p/Of7+S0XzCxFXw8GIVzZk0xFe6lHJzaq06f3mvzrD+4rpO56tTUvrgTY/n61gsF
ZP7f0CJ2JQh6eNRFOEUSfxKu/Dy/+IsQxorCJY2Q59ZAf3rXrqDN104jw9PlwnLl
qfZz3RMODN6BWjxE8rvRtT0qMfuAfv1gjBdWZN0hUYBRAgMBAAEwDQYJKoZIhvcN
AQELBQADggEBAABzo82TxGp5poVkd5pLWj5ACgcBv8Cs6oH9D+4Jz9BmyuBUsQXh
2aG0hQAe1mU61C9konsl/GTW8umJQ4M4lYEztXXwMf5PlBMGwebM0ZbSGg6jKtZg
WCgJ3eP/FMmyXGL5Jji5+e09eObhUDVle4tdi0On97zBoz85W02rgWFAqZJwiEAP
t+c7jX7uOSBq2/38iGStlrX5yB1at/gJXXiA5CL5OtlR3Okvb0/QH37efO1Nu39m
lFi0ODPAVyXjVypAiLguDxPn6AtDTdk9Iw9B19OD4NrzNRWgSSX5vuxo/VcRcgWk
3gEe9Ca0ZKN20q9XgthAiFFjl1S9ZgdA6Zc=
-----END CERTIFICATE-----`,
});
const https = new alicloud.slb.Listener("https", {
    backendPort: 80,
    bandwidth: 10,
    cookie: "testslblistenercookie",
    cookieTimeout: 86400,
    frontendPort: 443,
    healthCheck: "on",
    healthCheckConnectPort: 20,
    healthCheckHttpCode: "http_2xx,http_3xx",
    healthCheckInterval: 5,
    healthCheckTimeout: 8,
    healthCheckUri: "/cons",
    healthyThreshold: 8,
    loadBalancerId: instance.id,
    protocol: "https",
    sslCertificateId: foo.id,
    stickySession: "on",
    stickySessionType: "insert",
    unhealthyThreshold: 8,
});
const example1 = new alicloud.slb.DomainExtension("example1", {
    domain: "www.test.com",
    frontendPort: https.frontendPort,
    loadBalancerId: instance.id,
    serverCertificateId: foo.id,
});
```

> This content is derived from https://github.com/terraform-providers/terraform-provider-alicloud/blob/master/website/docs/r/slb_domain_extension.html.markdown.



## Create a DomainExtension Resource

{{< chooser language "javascript,typescript,python,go,csharp" / >}}

{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">new </span><span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/alicloud/slb/#DomainExtension">DomainExtension</a></span><span class="p">(</span><span class="nx">name</span>: <span class="nx"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/string">string</a></span><span class="p">, </span><span class="nx">args</span>: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/alicloud/slb/#DomainExtensionArgs">DomainExtensionArgs</a></span><span class="p">, </span><span class="nx">opts</span>?: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions">pulumi.CustomResourceOptions</a></span><span class="p">);</span></code></pre></div>
{{% /choosable %}}

{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class="k">def </span><span class="nf">DomainExtension</span><span class="p">(resource_name, opts=None, </span>delete_protection_validation=None<span class="p">, </span>domain=None<span class="p">, </span>frontend_port=None<span class="p">, </span>load_balancer_id=None<span class="p">, </span>server_certificate_id=None<span class="p">, __props__=None);</span></code></pre></div>
{{% /choosable %}}

{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>NewDomainExtension<span class="p">(</span><span class="nx">ctx</span> *<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#Context">pulumi.Context</a></span><span class="p">, </span><span class="nx">name</span> <span class="nx"><a href="https://golang.org/pkg/builtin/#string">string</a></span><span class="p">, </span><span class="nx">args</span> <span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-alicloud/sdk/go/alicloud/slb?tab=doc#DomainExtensionArgs">DomainExtensionArgs</a></span><span class="p">, </span><span class="nx">opts</span> ...<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#ResourceOption">pulumi.ResourceOption</a></span><span class="p">) (*<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-alicloud/sdk/go/alicloud/slb?tab=doc#DomainExtension">DomainExtension</a></span>, error)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Alicloud/Pulumi.Alicloud.Slb.DomainExtension.html">DomainExtension</a></span><span class="p">(</span><span class="nx"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">string</a></span> <span class="nx">name<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Alicloud/Pulumi.Alicloud.Slb.DomainExtensionArgs.html">DomainExtensionArgs</a></span> <span class="nx">args<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span>? <span class="nx">opts = null<span class="p">)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language nodejs %}}

<dl class="resources-properties">
    <dt class="property-required" title="Required">
        <span>name</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>The unique name of the resource.</dd>
    <dt class="property-optional" title="Optional">
        <span>args</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>The arguments to use to populate this resource's properties.</dd>
    <dt class="property-optional" title="Optional">
        <span>opts</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>A bag of options that control this resource's behavior.</dd>
</dl>

{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties">
    <dt class="property-required" title="Required">
        <span>name</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>The unique name of the resource.</dd>
    <dt class="property-optional" title="Optional">
        <span>opts</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>A bag of options that control this resource's behavior.</dd>
</dl>
{{% /choosable %}}

{{% choosable language go %}}

<dl class="resources-properties">
    <dt class="property-required" title="Required">
        <span>name</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>The unique name of the resource.</dd>
    <dt class="property-optional" title="Optional">
        <span>args</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>The arguments to use to populate this resource's properties.</dd>
    <dt class="property-optional" title="Optional">
        <span>opts</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>A bag of options that control this resource's behavior.</dd>
</dl>

{{% /choosable %}}

{{% choosable language csharp %}}

<dl class="resources-properties">
    <dt class="property-required" title="Required">
        <span>name</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>The unique name of the resource.</dd>
    <dt class="property-optional" title="Optional">
        <span>args</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>The arguments to use to populate this resource's properties.</dd>
    <dt class="property-optional" title="Optional">
        <span>opts</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>A bag of options that control this resource's behavior.</dd>
</dl>

{{% /choosable %}}

#### Resource Arguments




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Delete<wbr>Protection<wbr>Validation</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Checking DeleteProtection of SLB instance before deleting. If true, this resource will not be deleted when its SLB instance enabled DeleteProtection. Default to false.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Domain</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The domain name,
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Frontend<wbr>Port</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The frontend port used by the HTTPS listener of the SLB instance. Valid values: 1–65535.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Load<wbr>Balancer<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of the SLB instance.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Server<wbr>Certificate<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of the certificate used by the domain name.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Delete<wbr>Protection<wbr>Validation</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Checking DeleteProtection of SLB instance before deleting. If true, this resource will not be deleted when its SLB instance enabled DeleteProtection. Default to false.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Domain</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The domain name,
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Frontend<wbr>Port</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The frontend port used by the HTTPS listener of the SLB instance. Valid values: 1–65535.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Load<wbr>Balancer<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of the SLB instance.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Server<wbr>Certificate<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of the certificate used by the domain name.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>delete<wbr>Protection<wbr>Validation</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Checking DeleteProtection of SLB instance before deleting. If true, this resource will not be deleted when its SLB instance enabled DeleteProtection. Default to false.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>domain</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The domain name,
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>frontend<wbr>Port</span>
        <span class="property-indicator"></span>
        <span class="property-type">number</span>
    </dt>
    <dd>{{% md %}}The frontend port used by the HTTPS listener of the SLB instance. Valid values: 1–65535.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>load<wbr>Balancer<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of the SLB instance.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>server<wbr>Certificate<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of the certificate used by the domain name.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>delete_<wbr>protection_<wbr>validation</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Checking DeleteProtection of SLB instance before deleting. If true, this resource will not be deleted when its SLB instance enabled DeleteProtection. Default to false.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>domain</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The domain name,
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>frontend_<wbr>port</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}The frontend port used by the HTTPS listener of the SLB instance. Valid values: 1–65535.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>load_<wbr>balancer_<wbr>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The ID of the SLB instance.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>server_<wbr>certificate_<wbr>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The ID of the certificate used by the domain name.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}







## DomainExtension Output Properties

The following output properties are available:




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>Delete<wbr>Protection<wbr>Validation</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Checking DeleteProtection of SLB instance before deleting. If true, this resource will not be deleted when its SLB instance enabled DeleteProtection. Default to false.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Domain</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The domain name,
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Frontend<wbr>Port</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The frontend port used by the HTTPS listener of the SLB instance. Valid values: 1–65535.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Load<wbr>Balancer<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of the SLB instance.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Server<wbr>Certificate<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of the certificate used by the domain name.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>Delete<wbr>Protection<wbr>Validation</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Checking DeleteProtection of SLB instance before deleting. If true, this resource will not be deleted when its SLB instance enabled DeleteProtection. Default to false.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Domain</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The domain name,
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Frontend<wbr>Port</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The frontend port used by the HTTPS listener of the SLB instance. Valid values: 1–65535.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Load<wbr>Balancer<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of the SLB instance.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Server<wbr>Certificate<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of the certificate used by the domain name.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>delete<wbr>Protection<wbr>Validation</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Checking DeleteProtection of SLB instance before deleting. If true, this resource will not be deleted when its SLB instance enabled DeleteProtection. Default to false.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>domain</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The domain name,
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>frontend<wbr>Port</span>
        <span class="property-indicator"></span>
        <span class="property-type">number</span>
    </dt>
    <dd>{{% md %}}The frontend port used by the HTTPS listener of the SLB instance. Valid values: 1–65535.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>load<wbr>Balancer<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of the SLB instance.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>server<wbr>Certificate<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of the certificate used by the domain name.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>delete_<wbr>protection_<wbr>validation</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Checking DeleteProtection of SLB instance before deleting. If true, this resource will not be deleted when its SLB instance enabled DeleteProtection. Default to false.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>domain</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The domain name,
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>frontend_<wbr>port</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}The frontend port used by the HTTPS listener of the SLB instance. Valid values: 1–65535.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>load_<wbr>balancer_<wbr>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The ID of the SLB instance.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>server_<wbr>certificate_<wbr>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The ID of the certificate used by the domain name.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}








## Look up an Existing DomainExtension Resource

Get an existing DomainExtension resource's state with the given name, ID, and optional extra properties used to qualify the lookup.

{{< chooser language "javascript,typescript,python,go,csharp  " / >}}

{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">public static </span><span class="nf">get</span><span class="p">(</span><span class="nx">name</span>: <span class="nx"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/string">string</a></span><span class="p">, </span><span class="nx">id</span>: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#ID">Input&lt;ID&gt;</a></span><span class="p">, </span><span class="nx">state</span>?: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/alicloud/slb/#DomainExtensionState">DomainExtensionState</a></span><span class="p">, </span><span class="nx">opts</span>?: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions">CustomResourceOptions</a></span><span class="p">): </span><span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/alicloud/slb/#DomainExtension">DomainExtension</a></span></code></pre></div>
{{% /choosable %}}

{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class="k">static </span><span class="nf">get</span><span class="p">(resource_name, id, opts=None, </span>delete_protection_validation=None<span class="p">, </span>domain=None<span class="p">, </span>frontend_port=None<span class="p">, </span>load_balancer_id=None<span class="p">, </span>server_certificate_id=None<span class="p">, __props__=None);</span></code></pre></div>
{{% /choosable %}}

{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>GetDomainExtension<span class="p">(</span><span class="nx">ctx</span> *<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#Context">Context</a></span><span class="p">, </span><span class="nx">name</span> <span class="nx"><a href="https://golang.org/pkg/builtin/#string">string</a></span><span class="p">, </span><span class="nx">id</span> <span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#IDInput">IDInput</a></span><span class="p">, </span><span class="nx">state</span> *<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-alicloud/sdk/go/alicloud/slb?tab=doc#DomainExtensionState">DomainExtensionState</a></span><span class="p">, </span><span class="nx">opts</span> ...<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#ResourceOption">ResourceOption</a></span><span class="p">) (*<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-alicloud/sdk/go/alicloud/slb?tab=doc#DomainExtension">DomainExtension</a></span>, error)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public static </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Alicloud/Pulumi.Alicloud.Slb.DomainExtension.html">DomainExtension</a></span><span class="nf"> Get</span><span class="p">(</span><span class="nx"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">string</a></span> <span class="nx">name<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.Input.html">Input&lt;string&gt;</a></span> <span class="nx">id<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Alicloud/Pulumi.Alicloud.Slb.DomainExtensionState.html">DomainExtensionState</a></span>? <span class="nx">state<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span>? <span class="nx">opts = null<span class="p">)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language nodejs %}}

<dl class="resources-properties">
    <dt class="property-required" title="Required">
        <span>name</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>The unique name of the resulting resource.</dd>
    <dt class="property-required" title="Required">
        <span>id</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>The <em>unique</em> provider ID of the resource to lookup.</dd>
    <dt class="property-optional" title="Optional">
        <span>state</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>Any extra arguments used during the lookup.</dd>
    <dt class="property-optional" title="Optional">
        <span>opts</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>A bag of options that control this resource's behavior.</dd>
</dl>

{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties">
    <dt class="property-required" title="Required">
        <span>resource_name</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>The unique name of the resulting resource.</dd>
    <dt class="property-required" title="Optional">
        <span>id</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>The <em>unique</em> provider ID of the resource to lookup.</dd>
</dl>
{{% /choosable %}}

{{% choosable language go %}}

<dl class="resources-properties">
    <dt class="property-required" title="Required">
        <span>name</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>The unique name of the resulting resource.</dd>
    <dt class="property-required" title="Required">
        <span>id</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>The <em>unique</em> provider ID of the resource to lookup.</dd>
    <dt class="property-optional" title="Optional">
        <span>state</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>Any extra arguments used during the lookup.</dd>
    <dt class="property-optional" title="Optional">
        <span>opts</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>A bag of options that control this resource's behavior.</dd>
</dl>

{{% /choosable %}}

{{% choosable language csharp %}}

<dl class="resources-properties">
    <dt class="property-required" title="Required">
        <span>name</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>The unique name of the resulting resource.</dd>
    <dt class="property-required" title="Required">
        <span>id</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>The <em>unique</em> provider ID of the resource to lookup.</dd>
    <dt class="property-optional" title="Optional">
        <span>state</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>Any extra arguments used during the lookup.</dd>
    <dt class="property-optional" title="Optional">
        <span>opts</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>A bag of options that control this resource's behavior.</dd>
</dl>

{{% /choosable %}}

The following state arguments are supported:



{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Delete<wbr>Protection<wbr>Validation</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Checking DeleteProtection of SLB instance before deleting. If true, this resource will not be deleted when its SLB instance enabled DeleteProtection. Default to false.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Domain</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The domain name,
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Frontend<wbr>Port</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}The frontend port used by the HTTPS listener of the SLB instance. Valid values: 1–65535.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Load<wbr>Balancer<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The ID of the SLB instance.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Server<wbr>Certificate<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The ID of the certificate used by the domain name.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Delete<wbr>Protection<wbr>Validation</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Checking DeleteProtection of SLB instance before deleting. If true, this resource will not be deleted when its SLB instance enabled DeleteProtection. Default to false.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Domain</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The domain name,
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Frontend<wbr>Port</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}The frontend port used by the HTTPS listener of the SLB instance. Valid values: 1–65535.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Load<wbr>Balancer<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The ID of the SLB instance.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Server<wbr>Certificate<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The ID of the certificate used by the domain name.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>delete<wbr>Protection<wbr>Validation</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Checking DeleteProtection of SLB instance before deleting. If true, this resource will not be deleted when its SLB instance enabled DeleteProtection. Default to false.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>domain</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The domain name,
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>frontend<wbr>Port</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}The frontend port used by the HTTPS listener of the SLB instance. Valid values: 1–65535.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>load<wbr>Balancer<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The ID of the SLB instance.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>server<wbr>Certificate<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The ID of the certificate used by the domain name.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>delete_<wbr>protection_<wbr>validation</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Checking DeleteProtection of SLB instance before deleting. If true, this resource will not be deleted when its SLB instance enabled DeleteProtection. Default to false.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>domain</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The domain name,
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>frontend_<wbr>port</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}The frontend port used by the HTTPS listener of the SLB instance. Valid values: 1–65535.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>load_<wbr>balancer_<wbr>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The ID of the SLB instance.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>server_<wbr>certificate_<wbr>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The ID of the certificate used by the domain name.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}











<h3>Package Details</h3>
<dl class="package-details">
	<dt>Repository</dt>
	<dd><a href="https://github.com/pulumi/pulumi-alicloud">https://github.com/pulumi/pulumi-alicloud</a></dd>
	<dt>License</dt>
	<dd>Apache-2.0</dd>
    
</dl>
