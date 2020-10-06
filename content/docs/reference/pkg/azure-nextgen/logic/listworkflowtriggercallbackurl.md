
---
title: "ListWorkflowTriggerCallbackUrl"
title_tag: "Function ListWorkflowTriggerCallbackUrl | Module logic | Package Azure NextGen"
meta_desc: "Explore the ListWorkflowTriggerCallbackUrl function of the logic module, including examples, input properties, output properties, and supporting types. "
---



<!-- WARNING: this file was generated by Pulumi Docs Generator. -->
<!-- Do not edit by hand unless you're certain you know what you are doing! -->




## Using ListWorkflowTriggerCallbackUrl {#using}

{{< chooser language "typescript,python,go,csharp" / >}}


{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">function </span>listWorkflowTriggerCallbackUrl<span class="p">(</span><span class="nx">args</span><span class="p">:</span> <span class="nx">ListWorkflowTriggerCallbackUrlArgs</span><span class="p">, </span><span class="nx">opts</span><span class="p">?:</span> <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#InvokeOptions">InvokeOptions</a></span><span class="p">): Promise&lt;<span class="nx">ListWorkflowTriggerCallbackUrlResult</span>></span></code></pre></div>
{{% /choosable %}}


{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class="k">def </span>list_workflow_trigger_callback_url(</span><span class="nx">resource_group_name</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">, </span><span class="nx">trigger_name</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">, </span><span class="nx">workflow_name</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">, </span><span class="nx">opts</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/python/pulumi/#pulumi.InvokeOptions">Optional[InvokeOptions]</a></span> = None<span class="p">) -&gt;</span> ListWorkflowTriggerCallbackUrlResult</code></pre></div>
{{% /choosable %}}


{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>ListWorkflowTriggerCallbackUrl<span class="p">(</span><span class="nx">ctx</span><span class="p"> *</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v2/go/pulumi?tab=doc#Context">Context</a></span><span class="p">, </span><span class="nx">args</span><span class="p"> *</span><span class="nx">ListWorkflowTriggerCallbackUrlArgs</span><span class="p">, </span><span class="nx">opts</span><span class="p"> ...</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v2/go/pulumi?tab=doc#InvokeOption">InvokeOption</a></span><span class="p">) (*<span class="nx">ListWorkflowTriggerCallbackUrlResult</span>, error)</span></code></pre></div>

{{% /choosable %}}


{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public static class </span><span class="nx">ListWorkflowTriggerCallbackUrl </span><span class="p">{</span><span class="k">
    public static </span>Task&lt;<span class="nx">ListWorkflowTriggerCallbackUrlResult</span>> <span class="p">InvokeAsync(</span><span class="nx">ListWorkflowTriggerCallbackUrlArgs</span><span class="p"> </span><span class="nx">args<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.InvokeOptions.html">InvokeOptions</a></span><span class="p">? </span><span class="nx">opts = null<span class="p">)</span><span class="p">
}</span></code></pre></div>
{{% /choosable %}}



The following arguments are supported:



{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span id="resourcegroupname_csharp">
<a href="#resourcegroupname_csharp" style="color: inherit; text-decoration: inherit;">Resource<wbr>Group<wbr>Name</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">string</a></span>
    </dt>
    <dd>{{% md %}}The resource group name.{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span id="triggername_csharp">
<a href="#triggername_csharp" style="color: inherit; text-decoration: inherit;">Trigger<wbr>Name</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">string</a></span>
    </dt>
    <dd>{{% md %}}The workflow trigger name.{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span id="workflowname_csharp">
<a href="#workflowname_csharp" style="color: inherit; text-decoration: inherit;">Workflow<wbr>Name</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">string</a></span>
    </dt>
    <dd>{{% md %}}The workflow name.{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span id="resourcegroupname_go">
<a href="#resourcegroupname_go" style="color: inherit; text-decoration: inherit;">Resource<wbr>Group<wbr>Name</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://golang.org/pkg/builtin/#string">string</a></span>
    </dt>
    <dd>{{% md %}}The resource group name.{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span id="triggername_go">
<a href="#triggername_go" style="color: inherit; text-decoration: inherit;">Trigger<wbr>Name</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://golang.org/pkg/builtin/#string">string</a></span>
    </dt>
    <dd>{{% md %}}The workflow trigger name.{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span id="workflowname_go">
<a href="#workflowname_go" style="color: inherit; text-decoration: inherit;">Workflow<wbr>Name</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://golang.org/pkg/builtin/#string">string</a></span>
    </dt>
    <dd>{{% md %}}The workflow name.{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span id="resourcegroupname_nodejs">
<a href="#resourcegroupname_nodejs" style="color: inherit; text-decoration: inherit;">resource<wbr>Group<wbr>Name</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/string">string</a></span>
    </dt>
    <dd>{{% md %}}The resource group name.{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span id="triggername_nodejs">
<a href="#triggername_nodejs" style="color: inherit; text-decoration: inherit;">trigger<wbr>Name</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/string">string</a></span>
    </dt>
    <dd>{{% md %}}The workflow trigger name.{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span id="workflowname_nodejs">
<a href="#workflowname_nodejs" style="color: inherit; text-decoration: inherit;">workflow<wbr>Name</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/string">string</a></span>
    </dt>
    <dd>{{% md %}}The workflow name.{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span id="resource_group_name_python">
<a href="#resource_group_name_python" style="color: inherit; text-decoration: inherit;">resource_<wbr>group_<wbr>name</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.python.org/3/library/stdtypes.html">str</a></span>
    </dt>
    <dd>{{% md %}}The resource group name.{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span id="trigger_name_python">
<a href="#trigger_name_python" style="color: inherit; text-decoration: inherit;">trigger_<wbr>name</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.python.org/3/library/stdtypes.html">str</a></span>
    </dt>
    <dd>{{% md %}}The workflow trigger name.{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span id="workflow_name_python">
<a href="#workflow_name_python" style="color: inherit; text-decoration: inherit;">workflow_<wbr>name</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.python.org/3/library/stdtypes.html">str</a></span>
    </dt>
    <dd>{{% md %}}The workflow name.{{% /md %}}</dd>

</dl>
{{% /choosable %}}








## ListWorkflowTriggerCallbackUrl Result {#result}

The following output properties are available:




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span id="basepath_csharp">
<a href="#basepath_csharp" style="color: inherit; text-decoration: inherit;">Base<wbr>Path</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">string</a></span>
    </dt>
    <dd>{{% md %}}Gets the workflow trigger callback URL base path.{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span id="method_csharp">
<a href="#method_csharp" style="color: inherit; text-decoration: inherit;">Method</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">string</a></span>
    </dt>
    <dd>{{% md %}}Gets the workflow trigger callback URL HTTP method.{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span id="relativepath_csharp">
<a href="#relativepath_csharp" style="color: inherit; text-decoration: inherit;">Relative<wbr>Path</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">string</a></span>
    </dt>
    <dd>{{% md %}}Gets the workflow trigger callback URL relative path.{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span id="value_csharp">
<a href="#value_csharp" style="color: inherit; text-decoration: inherit;">Value</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">string</a></span>
    </dt>
    <dd>{{% md %}}Gets the workflow trigger callback URL.{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span id="queries_csharp">
<a href="#queries_csharp" style="color: inherit; text-decoration: inherit;">Queries</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#workflowtriggerlistcallbackurlqueriesresponse">Pulumi.<wbr>Azure<wbr>Next<wbr>Gen.<wbr>Logic.<wbr>Outputs.<wbr>Workflow<wbr>Trigger<wbr>List<wbr>Callback<wbr>Url<wbr>Queries<wbr>Response</a></span>
    </dt>
    <dd>{{% md %}}Gets the workflow trigger callback URL query parameters.{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span id="relativepathparameters_csharp">
<a href="#relativepathparameters_csharp" style="color: inherit; text-decoration: inherit;">Relative<wbr>Path<wbr>Parameters</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">List&lt;string&gt;</a></span>
    </dt>
    <dd>{{% md %}}Gets the workflow trigger callback URL relative path parameters.{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span id="basepath_go">
<a href="#basepath_go" style="color: inherit; text-decoration: inherit;">Base<wbr>Path</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://golang.org/pkg/builtin/#string">string</a></span>
    </dt>
    <dd>{{% md %}}Gets the workflow trigger callback URL base path.{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span id="method_go">
<a href="#method_go" style="color: inherit; text-decoration: inherit;">Method</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://golang.org/pkg/builtin/#string">string</a></span>
    </dt>
    <dd>{{% md %}}Gets the workflow trigger callback URL HTTP method.{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span id="relativepath_go">
<a href="#relativepath_go" style="color: inherit; text-decoration: inherit;">Relative<wbr>Path</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://golang.org/pkg/builtin/#string">string</a></span>
    </dt>
    <dd>{{% md %}}Gets the workflow trigger callback URL relative path.{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span id="value_go">
<a href="#value_go" style="color: inherit; text-decoration: inherit;">Value</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://golang.org/pkg/builtin/#string">string</a></span>
    </dt>
    <dd>{{% md %}}Gets the workflow trigger callback URL.{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span id="queries_go">
<a href="#queries_go" style="color: inherit; text-decoration: inherit;">Queries</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#workflowtriggerlistcallbackurlqueriesresponse">Workflow<wbr>Trigger<wbr>List<wbr>Callback<wbr>Url<wbr>Queries<wbr>Response</a></span>
    </dt>
    <dd>{{% md %}}Gets the workflow trigger callback URL query parameters.{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span id="relativepathparameters_go">
<a href="#relativepathparameters_go" style="color: inherit; text-decoration: inherit;">Relative<wbr>Path<wbr>Parameters</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://golang.org/pkg/builtin/#string">[]string</a></span>
    </dt>
    <dd>{{% md %}}Gets the workflow trigger callback URL relative path parameters.{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span id="basepath_nodejs">
<a href="#basepath_nodejs" style="color: inherit; text-decoration: inherit;">base<wbr>Path</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/string">string</a></span>
    </dt>
    <dd>{{% md %}}Gets the workflow trigger callback URL base path.{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span id="method_nodejs">
<a href="#method_nodejs" style="color: inherit; text-decoration: inherit;">method</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/string">string</a></span>
    </dt>
    <dd>{{% md %}}Gets the workflow trigger callback URL HTTP method.{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span id="relativepath_nodejs">
<a href="#relativepath_nodejs" style="color: inherit; text-decoration: inherit;">relative<wbr>Path</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/string">string</a></span>
    </dt>
    <dd>{{% md %}}Gets the workflow trigger callback URL relative path.{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span id="value_nodejs">
<a href="#value_nodejs" style="color: inherit; text-decoration: inherit;">value</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/string">string</a></span>
    </dt>
    <dd>{{% md %}}Gets the workflow trigger callback URL.{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span id="queries_nodejs">
<a href="#queries_nodejs" style="color: inherit; text-decoration: inherit;">queries</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#workflowtriggerlistcallbackurlqueriesresponse">Workflow<wbr>Trigger<wbr>List<wbr>Callback<wbr>Url<wbr>Queries<wbr>Response</a></span>
    </dt>
    <dd>{{% md %}}Gets the workflow trigger callback URL query parameters.{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span id="relativepathparameters_nodejs">
<a href="#relativepathparameters_nodejs" style="color: inherit; text-decoration: inherit;">relative<wbr>Path<wbr>Parameters</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/string">string[]</a></span>
    </dt>
    <dd>{{% md %}}Gets the workflow trigger callback URL relative path parameters.{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span id="base_path_python">
<a href="#base_path_python" style="color: inherit; text-decoration: inherit;">base_<wbr>path</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.python.org/3/library/stdtypes.html">str</a></span>
    </dt>
    <dd>{{% md %}}Gets the workflow trigger callback URL base path.{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span id="method_python">
<a href="#method_python" style="color: inherit; text-decoration: inherit;">method</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.python.org/3/library/stdtypes.html">str</a></span>
    </dt>
    <dd>{{% md %}}Gets the workflow trigger callback URL HTTP method.{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span id="relative_path_python">
<a href="#relative_path_python" style="color: inherit; text-decoration: inherit;">relative_<wbr>path</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.python.org/3/library/stdtypes.html">str</a></span>
    </dt>
    <dd>{{% md %}}Gets the workflow trigger callback URL relative path.{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span id="value_python">
<a href="#value_python" style="color: inherit; text-decoration: inherit;">value</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.python.org/3/library/stdtypes.html">str</a></span>
    </dt>
    <dd>{{% md %}}Gets the workflow trigger callback URL.{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span id="queries_python">
<a href="#queries_python" style="color: inherit; text-decoration: inherit;">queries</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#workflowtriggerlistcallbackurlqueriesresponse">Dict[Workflow<wbr>Trigger<wbr>List<wbr>Callback<wbr>Url<wbr>Queries<wbr>Response]</a></span>
    </dt>
    <dd>{{% md %}}Gets the workflow trigger callback URL query parameters.{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span id="relative_path_parameters_python">
<a href="#relative_path_parameters_python" style="color: inherit; text-decoration: inherit;">relative_<wbr>path_<wbr>parameters</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.python.org/3/library/stdtypes.html">List[str]</a></span>
    </dt>
    <dd>{{% md %}}Gets the workflow trigger callback URL relative path parameters.{{% /md %}}</dd>

</dl>
{{% /choosable %}}








## Supporting Types


<h4 id="workflowtriggerlistcallbackurlqueriesresponse">Workflow<wbr>Trigger<wbr>List<wbr>Callback<wbr>Url<wbr>Queries<wbr>Response</h4>







{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span id="apiversion_csharp">
<a href="#apiversion_csharp" style="color: inherit; text-decoration: inherit;">Api<wbr>Version</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">string</a></span>
    </dt>
    <dd>{{% md %}}The api version.{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span id="se_csharp">
<a href="#se_csharp" style="color: inherit; text-decoration: inherit;">Se</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">string</a></span>
    </dt>
    <dd>{{% md %}}The SAS timestamp.{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span id="sig_csharp">
<a href="#sig_csharp" style="color: inherit; text-decoration: inherit;">Sig</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">string</a></span>
    </dt>
    <dd>{{% md %}}The SAS signature.{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span id="sp_csharp">
<a href="#sp_csharp" style="color: inherit; text-decoration: inherit;">Sp</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">string</a></span>
    </dt>
    <dd>{{% md %}}The SAS permissions.{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span id="sv_csharp">
<a href="#sv_csharp" style="color: inherit; text-decoration: inherit;">Sv</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">string</a></span>
    </dt>
    <dd>{{% md %}}The SAS version.{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span id="apiversion_go">
<a href="#apiversion_go" style="color: inherit; text-decoration: inherit;">Api<wbr>Version</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://golang.org/pkg/builtin/#string">string</a></span>
    </dt>
    <dd>{{% md %}}The api version.{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span id="se_go">
<a href="#se_go" style="color: inherit; text-decoration: inherit;">Se</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://golang.org/pkg/builtin/#string">string</a></span>
    </dt>
    <dd>{{% md %}}The SAS timestamp.{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span id="sig_go">
<a href="#sig_go" style="color: inherit; text-decoration: inherit;">Sig</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://golang.org/pkg/builtin/#string">string</a></span>
    </dt>
    <dd>{{% md %}}The SAS signature.{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span id="sp_go">
<a href="#sp_go" style="color: inherit; text-decoration: inherit;">Sp</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://golang.org/pkg/builtin/#string">string</a></span>
    </dt>
    <dd>{{% md %}}The SAS permissions.{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span id="sv_go">
<a href="#sv_go" style="color: inherit; text-decoration: inherit;">Sv</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://golang.org/pkg/builtin/#string">string</a></span>
    </dt>
    <dd>{{% md %}}The SAS version.{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span id="apiversion_nodejs">
<a href="#apiversion_nodejs" style="color: inherit; text-decoration: inherit;">api<wbr>Version</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/string">string</a></span>
    </dt>
    <dd>{{% md %}}The api version.{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span id="se_nodejs">
<a href="#se_nodejs" style="color: inherit; text-decoration: inherit;">se</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/string">string</a></span>
    </dt>
    <dd>{{% md %}}The SAS timestamp.{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span id="sig_nodejs">
<a href="#sig_nodejs" style="color: inherit; text-decoration: inherit;">sig</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/string">string</a></span>
    </dt>
    <dd>{{% md %}}The SAS signature.{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span id="sp_nodejs">
<a href="#sp_nodejs" style="color: inherit; text-decoration: inherit;">sp</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/string">string</a></span>
    </dt>
    <dd>{{% md %}}The SAS permissions.{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span id="sv_nodejs">
<a href="#sv_nodejs" style="color: inherit; text-decoration: inherit;">sv</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/string">string</a></span>
    </dt>
    <dd>{{% md %}}The SAS version.{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span id="api_version_python">
<a href="#api_version_python" style="color: inherit; text-decoration: inherit;">api_<wbr>version</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.python.org/3/library/stdtypes.html">str</a></span>
    </dt>
    <dd>{{% md %}}The api version.{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span id="se_python">
<a href="#se_python" style="color: inherit; text-decoration: inherit;">se</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.python.org/3/library/stdtypes.html">str</a></span>
    </dt>
    <dd>{{% md %}}The SAS timestamp.{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span id="sig_python">
<a href="#sig_python" style="color: inherit; text-decoration: inherit;">sig</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.python.org/3/library/stdtypes.html">str</a></span>
    </dt>
    <dd>{{% md %}}The SAS signature.{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span id="sp_python">
<a href="#sp_python" style="color: inherit; text-decoration: inherit;">sp</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.python.org/3/library/stdtypes.html">str</a></span>
    </dt>
    <dd>{{% md %}}The SAS permissions.{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span id="sv_python">
<a href="#sv_python" style="color: inherit; text-decoration: inherit;">sv</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.python.org/3/library/stdtypes.html">str</a></span>
    </dt>
    <dd>{{% md %}}The SAS version.{{% /md %}}</dd>

</dl>
{{% /choosable %}}









<h2 id="package-details">Package Details</h2>
<dl class="package-details">
	<dt>Repository</dt>
	<dd><a href="https://github.com/pulumi/pulumi-azure-nextgen">https://github.com/pulumi/pulumi-azure-nextgen</a></dd>
	<dt>License</dt>
	<dd>Apache-2.0</dd>
</dl>
