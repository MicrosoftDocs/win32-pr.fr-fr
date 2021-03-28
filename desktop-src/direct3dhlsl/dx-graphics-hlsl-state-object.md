---
title: Objets d’état
description: Utilisez le langage HLSL pour définir des objets d’État.
ms.assetid: a02432dc-f354-48c0-a7ac-1ff502f3b1d1
ms.topic: article
ms.date: 2/2/2021
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 53bfc903f8bc1be56962e912b1c82f02faaf0c44
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "104991865"
---
# <a name="state-objects"></a><span data-ttu-id="4babc-103">Objets d’état</span><span class="sxs-lookup"><span data-stu-id="4babc-103">State Objects</span></span>

<span data-ttu-id="4babc-104">Avec les modèles de nuanceur 6,3 et versions ultérieures, les applications ont la possibilité de définir des objets d’État DXR directement dans le code du nuanceur HLSL en plus de l’utilisation des API Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="4babc-104">With shader models 6.3 and later, applications have the convenience and flexibility of being able to define DXR state objects directly in HLSL shader code in addition to using Direct3D 12 APIs.</span></span>

<span data-ttu-id="4babc-105">En langage HLSL, les objets d’État sont déclarés avec la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="4babc-105">In HLSL, state objects are declared with this syntax:</span></span>

``` syntax
Type Name = 
{ 
    Field1,
    Field2,
    ...
};
```



| <span data-ttu-id="4babc-106">Élément</span><span class="sxs-lookup"><span data-stu-id="4babc-106">Item</span></span>                                                                                         | <span data-ttu-id="4babc-107">Description</span><span class="sxs-lookup"><span data-stu-id="4babc-107">Description</span></span>                                                                            |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4babc-108"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>**Entrer**</span><span class="sxs-lookup"><span data-stu-id="4babc-108"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>**Type**</span></span><br/>     | <span data-ttu-id="4babc-109">Identifie le type de sous-objet.</span><span class="sxs-lookup"><span data-stu-id="4babc-109">Identifies the type of subobject.</span></span> <span data-ttu-id="4babc-110">Doit être l’un des types de sous-objets HLSL pris en charge.</span><span class="sxs-lookup"><span data-stu-id="4babc-110">Must be one of the supported HLSL subobject types.</span></span><br/>     |
| <span data-ttu-id="4babc-111"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**Nomme**</span><span class="sxs-lookup"><span data-stu-id="4babc-111"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**Name**</span></span><br/>     | <span data-ttu-id="4babc-112">Chaîne ASCII qui identifie de façon unique le nom de la variable.</span><span class="sxs-lookup"><span data-stu-id="4babc-112">An ASCII string that uniquely identifies the variable name.</span></span><br/>                 |
| <span data-ttu-id="4babc-113"><span id="Field"></span><span id="field"></span><span id="FIELD"></span>**Champ [1, 2,...]**</span><span class="sxs-lookup"><span data-stu-id="4babc-113"><span id="Field"></span><span id="field"></span><span id="FIELD"></span>**Field[1, 2, ...]**</span></span><br/> | <span data-ttu-id="4babc-114">Champs du sous-objet.</span><span class="sxs-lookup"><span data-stu-id="4babc-114">Fields of the subobject.</span></span> <span data-ttu-id="4babc-115">Les champs spécifiques pour chaque type de sous-objet sont décrits ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="4babc-115">Specific fields for each type of subobject are described below.</span></span><br/> |




<span data-ttu-id="4babc-116">Liste des types de sous-objets :</span><span class="sxs-lookup"><span data-stu-id="4babc-116">List of subobject types:</span></span>
-   [<span data-ttu-id="4babc-117">StateObjectConfig</span><span class="sxs-lookup"><span data-stu-id="4babc-117">StateObjectConfig</span></span>](#stateobjectconfig)
-   [<span data-ttu-id="4babc-118">GlobalRootSignature</span><span class="sxs-lookup"><span data-stu-id="4babc-118">GlobalRootSignature</span></span>](#globalrootsignature)
-   [<span data-ttu-id="4babc-119">LocalRootSignature</span><span class="sxs-lookup"><span data-stu-id="4babc-119">LocalRootSignature</span></span>](#localrootsignature)
-   [<span data-ttu-id="4babc-120">SubobjectToExportsAssocation</span><span class="sxs-lookup"><span data-stu-id="4babc-120">SubobjectToExportsAssocation</span></span>](#subobjecttoexportsassocation)
-   [<span data-ttu-id="4babc-121">RaytracingShaderConfig</span><span class="sxs-lookup"><span data-stu-id="4babc-121">RaytracingShaderConfig</span></span>](#raytracingshaderconfig)
-   [<span data-ttu-id="4babc-122">RaytracingPipelineConfig</span><span class="sxs-lookup"><span data-stu-id="4babc-122">RaytracingPipelineConfig</span></span>](#raytracingpipelineconfig)
-   [<span data-ttu-id="4babc-123">TriangleHitGroup</span><span class="sxs-lookup"><span data-stu-id="4babc-123">TriangleHitGroup</span></span>](#trianglehitgroup)
-   [<span data-ttu-id="4babc-124">ProceduralPrimitiveHitGroup</span><span class="sxs-lookup"><span data-stu-id="4babc-124">ProceduralPrimitiveHitGroup</span></span>](#proceduralprimitivehitgroup)

## <a name="stateobjectconfig"></a><span data-ttu-id="4babc-125">StateObjectConfig</span><span class="sxs-lookup"><span data-stu-id="4babc-125">StateObjectConfig</span></span>

<span data-ttu-id="4babc-126">Le type de sous-objet StateObjectConfig correspond à une structure [D3D12_STATE_OBJECT_CONFIG](/windows/win32/api/d3d12/ns-d3d12-d3d12_state_object_config) .</span><span class="sxs-lookup"><span data-stu-id="4babc-126">The StateObjectConfig subobject type corresponds to a [D3D12_STATE_OBJECT_CONFIG](/windows/win32/api/d3d12/ns-d3d12-d3d12_state_object_config) structure.</span></span>

<span data-ttu-id="4babc-127">Il a un champ, un indicateur de bits, qui est l’un des</span><span class="sxs-lookup"><span data-stu-id="4babc-127">It has one field, a bitwise flag, which is one or both of</span></span>

* <span data-ttu-id="4babc-128">STATE_OBJECT_FLAGS_ALLOW_LOCAL_DEPENDENCIES_ON_EXTERNAL_DEFINITONS</span><span class="sxs-lookup"><span data-stu-id="4babc-128">STATE_OBJECT_FLAGS_ALLOW_LOCAL_DEPENDENCIES_ON_EXTERNAL_DEFINITONS</span></span>
* <span data-ttu-id="4babc-129">STATE_OBJECT_FLAGS_ALLOW_EXTERNAL_DEPENDENCIES_ON_LOCAL_DEFINITIONS</span><span class="sxs-lookup"><span data-stu-id="4babc-129">STATE_OBJECT_FLAGS_ALLOW_EXTERNAL_DEPENDENCIES_ON_LOCAL_DEFINITIONS</span></span>

<span data-ttu-id="4babc-130">ou zéro pour aucun d’entre eux.</span><span class="sxs-lookup"><span data-stu-id="4babc-130">or, zero for neither of them.</span></span>

<span data-ttu-id="4babc-131">Exemple :</span><span class="sxs-lookup"><span data-stu-id="4babc-131">Example:</span></span>

```
StateObjectConfig MyStateObjectConfig = 
{ 
    STATE_OBJECT_FLAGS_ALLOW_LOCAL_DEPENDENCIES_ON_EXTERNAL_DEFINITONS
};
```

## <a name="globalrootsignature"></a><span data-ttu-id="4babc-132">GlobalRootSignature</span><span class="sxs-lookup"><span data-stu-id="4babc-132">GlobalRootSignature</span></span>
<span data-ttu-id="4babc-133">Un GlobalRootSignature correspond à une structure [D3D12_GLOBAL_ROOT_SIGNATURE](/windows/win32/api/d3d12/ns-d3d12-d3d12_global_root_signature) .</span><span class="sxs-lookup"><span data-stu-id="4babc-133">A GlobalRootSignature corresponds to a [D3D12_GLOBAL_ROOT_SIGNATURE](/windows/win32/api/d3d12/ns-d3d12-d3d12_global_root_signature) structure.</span></span>

<span data-ttu-id="4babc-134">Les champs sont constitués d’un certain nombre de chaînes décrivant les parties de la signature racine.</span><span class="sxs-lookup"><span data-stu-id="4babc-134">The fields consist of some number of strings describing the parts of the root signature.</span></span> <span data-ttu-id="4babc-135">Pour plus d’informations, consultez [spécification de signatures racines en langage HLSL](../direct3d12/specifying-root-signatures-in-hlsl.md).</span><span class="sxs-lookup"><span data-stu-id="4babc-135">For reference on this, see [Specifying Root Signatures in HLSL](../direct3d12/specifying-root-signatures-in-hlsl.md).</span></span>

<span data-ttu-id="4babc-136">Exemple :</span><span class="sxs-lookup"><span data-stu-id="4babc-136">Example:</span></span>
```
GlobalRootSignature MyGlobalRootSignature =
{
    "DescriptorTable(UAV(u0)),"                     // Output texture
    "SRV(t0),"                                      // Acceleration structure
    "CBV(b0),"                                      // Scene constants
    "DescriptorTable(SRV(t1, numDescriptors = 2))"  // Static index and vertex buffers.
};
```

## <a name="localrootsignature"></a><span data-ttu-id="4babc-137">LocalRootSignature</span><span class="sxs-lookup"><span data-stu-id="4babc-137">LocalRootSignature</span></span>
<span data-ttu-id="4babc-138">Un LocalRootSignature correspond à une structure [D3D12_LOCAL_ROOT_SIGNATURE](/windows/win32/api/d3d12/ns-d3d12-d3d12_local_root_signature) .</span><span class="sxs-lookup"><span data-stu-id="4babc-138">A LocalRootSignature corresponds to a [D3D12_LOCAL_ROOT_SIGNATURE](/windows/win32/api/d3d12/ns-d3d12-d3d12_local_root_signature) structure.</span></span>

<span data-ttu-id="4babc-139">Tout comme le sous-objet signature racine globale, les champs se composent d’un certain nombre de chaînes décrivant les parties de la signature racine.</span><span class="sxs-lookup"><span data-stu-id="4babc-139">Just like the global root signature subobject, the fields consist of some number of strings describing the parts of the root signature.</span></span> <span data-ttu-id="4babc-140">Pour plus d’informations, consultez [spécification de signatures racines en langage HLSL](../direct3d12/specifying-root-signatures-in-hlsl.md).</span><span class="sxs-lookup"><span data-stu-id="4babc-140">For reference on this, see [Specifying Root Signatures in HLSL](../direct3d12/specifying-root-signatures-in-hlsl.md).</span></span>

<span data-ttu-id="4babc-141">Exemple :</span><span class="sxs-lookup"><span data-stu-id="4babc-141">Example:</span></span>
```
LocalRootSignature MyLocalRootSignature = 
{
    "RootConstants(num32BitConstants = 4, b1)"  // Cube constants 
};
```

## <a name="subobjecttoexportsassocation"></a><span data-ttu-id="4babc-142">SubobjectToExportsAssocation</span><span class="sxs-lookup"><span data-stu-id="4babc-142">SubobjectToExportsAssocation</span></span>
<span data-ttu-id="4babc-143">Par défaut, un sous-objet simplement déclaré dans la même bibliothèque qu’une exportation est en mesure de s’appliquer à cette exportation.</span><span class="sxs-lookup"><span data-stu-id="4babc-143">By default, a subobject merely declared in the same library as an export is able to apply to that export.</span></span> <span data-ttu-id="4babc-144">Toutefois, les applications ont la possibilité de la remplacer et d’obtenir des informations spécifiques sur le type de sous-objet utilisé pour l’exportation.</span><span class="sxs-lookup"><span data-stu-id="4babc-144">However, applications have the ability to override that and get specific about what subobject goes with which export.</span></span> <span data-ttu-id="4babc-145">En langage HLSL, cette « association explicite » s’effectue à l’aide de SubobjectToExportsAssocation.</span><span class="sxs-lookup"><span data-stu-id="4babc-145">In HLSL, this "explicit association" is done using SubobjectToExportsAssocation.</span></span>

<span data-ttu-id="4babc-146">Un SubobjectToExportsAssocation correspond à une structure [D3D12_DXIL_SUBOBJECT_TO_EXPORTS_ASSOCIATION ](/windows/win32/api/d3d12/ns-d3d12-d3d12_dxil_subobject_to_exports_association) .</span><span class="sxs-lookup"><span data-stu-id="4babc-146">A SubobjectToExportsAssocation corresponds to a [D3D12_DXIL_SUBOBJECT_TO_EXPORTS_ASSOCIATION ](/windows/win32/api/d3d12/ns-d3d12-d3d12_dxil_subobject_to_exports_association) structure.</span></span>

<span data-ttu-id="4babc-147">Ce sous-objet est déclaré avec la syntaxe</span><span class="sxs-lookup"><span data-stu-id="4babc-147">This subobject is declared with the syntax</span></span>

``` syntax
SubobjectToExportsAssocation Name = 
{ 
    SubobjectName,
    Exports
};
```

| <span data-ttu-id="4babc-148">Élément</span><span class="sxs-lookup"><span data-stu-id="4babc-148">Item</span></span>                                                                                         | <span data-ttu-id="4babc-149">Description</span><span class="sxs-lookup"><span data-stu-id="4babc-149">Description</span></span>                                                                            |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4babc-150"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**Nomme**</span><span class="sxs-lookup"><span data-stu-id="4babc-150"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**Name**</span></span><br/>     | <span data-ttu-id="4babc-151">Chaîne ASCII qui identifie de façon unique le nom de la variable.</span><span class="sxs-lookup"><span data-stu-id="4babc-151">An ASCII string that uniquely identifies the variable name.</span></span><br/>                 |
| <span data-ttu-id="4babc-152"><span id="SubobjectName"></span><span id="subobjectname"></span><span id="SUBOBJECTNAME"></span>**SubobjectName**</span><span class="sxs-lookup"><span data-stu-id="4babc-152"><span id="SubobjectName"></span><span id="subobjectname"></span><span id="SUBOBJECTNAME"></span>**SubobjectName**</span></span><br/>     | <span data-ttu-id="4babc-153">Chaîne qui identifie un sous-objet exporté.</span><span class="sxs-lookup"><span data-stu-id="4babc-153">String which identifies an exported subobject.</span></span><br/> |
| <span data-ttu-id="4babc-154"><span id="Exports"></span><span id="exports"></span><span id="EXPORTS"></span>**Ventes**</span><span class="sxs-lookup"><span data-stu-id="4babc-154"><span id="Exports"></span><span id="exports"></span><span id="EXPORTS"></span>**Exports**</span></span><br/> | <span data-ttu-id="4babc-155">Chaîne contenant une liste d’exportations délimitées par des points-virgules.</span><span class="sxs-lookup"><span data-stu-id="4babc-155">String containing a semicolon-delimited list of exports.</span></span><br/> |


<span data-ttu-id="4babc-156">Exemple :</span><span class="sxs-lookup"><span data-stu-id="4babc-156">Example:</span></span>
```
SubobjectToExportsAssociation MyLocalRootSignatureAssociation =
{
    "MyLocalRootSignature",    // Subobject name
    "MyHitGroup;MyMissShader"  // Exports association 
};
```

<span data-ttu-id="4babc-157">Notez que les deux champs utilisent des noms *exportés* .</span><span class="sxs-lookup"><span data-stu-id="4babc-157">Note that both fields use *exported* names.</span></span> <span data-ttu-id="4babc-158">Un nom exporté peut être différent du nom d’origine en langage HLSL, si l’application choisit d’effectuer une exportation-attribution d’un nouveau nom.</span><span class="sxs-lookup"><span data-stu-id="4babc-158">An exported name may be different from the original name in HLSL, if the application chooses to do export-renaming.</span></span>

## <a name="raytracingshaderconfig"></a><span data-ttu-id="4babc-159">RaytracingShaderConfig</span><span class="sxs-lookup"><span data-stu-id="4babc-159">RaytracingShaderConfig</span></span>

<span data-ttu-id="4babc-160">Un RaytracingShaderConfig correspond à une structure [D3D12_RAYTRACING_SHADER_CONFIG](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_shader_config) .</span><span class="sxs-lookup"><span data-stu-id="4babc-160">A RaytracingShaderConfig corresponds to a [D3D12_RAYTRACING_SHADER_CONFIG](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_shader_config) structure.</span></span>

<span data-ttu-id="4babc-161">Ce sous-objet est déclaré avec la syntaxe</span><span class="sxs-lookup"><span data-stu-id="4babc-161">This subobject is declared with the syntax</span></span>

``` syntax
RaytracingShaderConfig Name = 
{ 
    MaxPayloadSize,
    MaxAttributeSize
};
```

| <span data-ttu-id="4babc-162">Élément</span><span class="sxs-lookup"><span data-stu-id="4babc-162">Item</span></span>                                                                                         | <span data-ttu-id="4babc-163">Description</span><span class="sxs-lookup"><span data-stu-id="4babc-163">Description</span></span>                                                                            |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4babc-164"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**Nomme**</span><span class="sxs-lookup"><span data-stu-id="4babc-164"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**Name**</span></span><br/>     | <span data-ttu-id="4babc-165">Chaîne ASCII qui identifie de façon unique le nom de la variable.</span><span class="sxs-lookup"><span data-stu-id="4babc-165">An ASCII string that uniquely identifies the variable name.</span></span><br/>                 |
| <span data-ttu-id="4babc-166"><span id="MaxPayloadSize"></span><span id="maxpayloadsize"></span><span id="MAXPAYLOADSIZE"></span>**MaxPayloadSize**</span><span class="sxs-lookup"><span data-stu-id="4babc-166"><span id="MaxPayloadSize"></span><span id="maxpayloadsize"></span><span id="MAXPAYLOADSIZE"></span>**MaxPayloadSize**</span></span><br/>     | <span data-ttu-id="4babc-167">Valeur numérique pour le stockage maximal pour les scalaires (comptée comme 4 octets chacun) dans les charges utiles de Ray pour les nuanceurs de Raytracing associés.</span><span class="sxs-lookup"><span data-stu-id="4babc-167">Numerical value for the maximum storage for scalars (counted as 4 bytes each) in ray payloads for associated raytracing shaders.</span></span><br/> |
| <span data-ttu-id="4babc-168"><span id="MaxAttributeSize"></span><span id="maxattributesize"></span><span id="MAXATTRIBUTESIZE"></span>**MaxAttributeSize**</span><span class="sxs-lookup"><span data-stu-id="4babc-168"><span id="MaxAttributeSize"></span><span id="maxattributesize"></span><span id="MAXATTRIBUTESIZE"></span>**MaxAttributeSize**</span></span><br/> | <span data-ttu-id="4babc-169">Valeur numérique pour le nombre maximal de scalaires (comptant 4 octets chacun) qui peut être utilisé pour les attributs des nuanceurs Raytracing associés.</span><span class="sxs-lookup"><span data-stu-id="4babc-169">Numerical value for the maximum number of scalars (counted as 4 bytes each) that can be used for attributes in associated raytracing shaders.</span></span> <span data-ttu-id="4babc-170">La valeur ne peut pas dépasser [D3D12_RAYTRACING_MAX_ATTRIBUTE_SIZE_IN_BYTES](../direct3d12/constants.md).</span><span class="sxs-lookup"><span data-stu-id="4babc-170">The value cannot exceed [D3D12_RAYTRACING_MAX_ATTRIBUTE_SIZE_IN_BYTES](../direct3d12/constants.md).</span></span><br/> |


<span data-ttu-id="4babc-171">Exemple :</span><span class="sxs-lookup"><span data-stu-id="4babc-171">Example:</span></span>
```
RaytracingShaderConfig MyShaderConfig =
{
    16,  // Max payload size
    8    // Max attribute size
};
```

## <a name="raytracingpipelineconfig"></a><span data-ttu-id="4babc-172">RaytracingPipelineConfig</span><span class="sxs-lookup"><span data-stu-id="4babc-172">RaytracingPipelineConfig</span></span>

<span data-ttu-id="4babc-173">Un RaytracingPipelineConfig correspond à une structure [D3D12_RAYTRACING_PIPELINE_CONFIG](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_pipeline_config) .</span><span class="sxs-lookup"><span data-stu-id="4babc-173">A RaytracingPipelineConfig corresponds to a [D3D12_RAYTRACING_PIPELINE_CONFIG](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_pipeline_config) structure.</span></span>

<span data-ttu-id="4babc-174">Ce sous-objet est déclaré avec la syntaxe</span><span class="sxs-lookup"><span data-stu-id="4babc-174">This subobject is declared with the syntax</span></span>

``` syntax
RaytracingPipelineConfig Name = 
{ 
    MaxTraceRecursionDepth
};
```

| <span data-ttu-id="4babc-175">Élément</span><span class="sxs-lookup"><span data-stu-id="4babc-175">Item</span></span>                                                                                         | <span data-ttu-id="4babc-176">Description</span><span class="sxs-lookup"><span data-stu-id="4babc-176">Description</span></span>                                                                            |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4babc-177"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**Nomme**</span><span class="sxs-lookup"><span data-stu-id="4babc-177"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**Name**</span></span><br/>     | <span data-ttu-id="4babc-178">Chaîne ASCII qui identifie de façon unique le nom de la variable.</span><span class="sxs-lookup"><span data-stu-id="4babc-178">An ASCII string that uniquely identifies the variable name.</span></span><br/>                 |
| <span data-ttu-id="4babc-179"><span id="MaxTraceRecursionDepth"></span><span id="maxtracerecursiondepth"></span><span id="MAXTRACERECURSIONDEPTH"></span>**MaxTraceRecursionDepth**</span><span class="sxs-lookup"><span data-stu-id="4babc-179"><span id="MaxTraceRecursionDepth"></span><span id="maxtracerecursiondepth"></span><span id="MAXTRACERECURSIONDEPTH"></span>**MaxTraceRecursionDepth**</span></span><br/>     | <span data-ttu-id="4babc-180">Limite numérique à utiliser pour la récursivité de rayon dans le pipeline Raytracing.</span><span class="sxs-lookup"><span data-stu-id="4babc-180">Numerical limit to use for ray recursion in the raytracing pipeline.</span></span> <span data-ttu-id="4babc-181">Il s’agit d’un nombre compris entre 0 et 31, inclus.</span><span class="sxs-lookup"><span data-stu-id="4babc-181">It is a number between 0 and 31, inclusive.</span></span> <br/> |


<span data-ttu-id="4babc-182">Exemple :</span><span class="sxs-lookup"><span data-stu-id="4babc-182">Example:</span></span>
```
RaytracingPipelineConfig MyPipelineConfig =
{
    1  // Max trace recursion depth
};
```
<span data-ttu-id="4babc-183">Étant donné qu’il y a un coût de performance pour la récursivité Raytracing, les applications doivent utiliser la profondeur de récursivité la plus faible nécessaire pour les résultats souhaités.</span><span class="sxs-lookup"><span data-stu-id="4babc-183">Since there is a performance cost to raytracing recursion, applications should use the lowest recursion depth needed for the desired results.</span></span>

<span data-ttu-id="4babc-184">Si les appels de nuanceur n’ont pas encore atteint la profondeur maximale de récursivité, ils peuvent appeler [TraceRay](../direct3d12/traceray-function.md) un nombre quelconque de fois.</span><span class="sxs-lookup"><span data-stu-id="4babc-184">If shader invocations haven't yet reached the maximum recursion depth, they can call [TraceRay](../direct3d12/traceray-function.md) any number of times.</span></span> <span data-ttu-id="4babc-185">Toutefois, s’ils atteignent ou dépassent la profondeur maximale de récursivité, l’appel de TraceRay met l’appareil en état de suppression.</span><span class="sxs-lookup"><span data-stu-id="4babc-185">But if they reach or exceed the maximum recursion depth, calling TraceRay puts the device into removed state.</span></span> <span data-ttu-id="4babc-186">Par conséquent, les nuanceurs Raytracing doivent veiller à arrêter d’appeler TraceRay s’ils ont atteint ou dépassé la profondeur maximale de récursivité.</span><span class="sxs-lookup"><span data-stu-id="4babc-186">Therefore, raytracing shaders should take care to stop calling TraceRay if they've met or exceeded the maximum recursion depth.</span></span>

## <a name="trianglehitgroup"></a><span data-ttu-id="4babc-187">TriangleHitGroup</span><span class="sxs-lookup"><span data-stu-id="4babc-187">TriangleHitGroup</span></span>

<span data-ttu-id="4babc-188">Un TriangleHitGroup correspond à une structure [D3D12_HIT_GROUP_DESC](/windows/win32/api/d3d12/ns-d3d12-d3d12_hit_group_desc) dont le champ de type est défini sur [D3D12_HIT_GROUP_TYPE_TRIANGLES](/windows/win32/api/d3d12/ne-d3d12-d3d12_hit_group_type#constants).</span><span class="sxs-lookup"><span data-stu-id="4babc-188">A TriangleHitGroup corresponds to a [D3D12_HIT_GROUP_DESC](/windows/win32/api/d3d12/ns-d3d12-d3d12_hit_group_desc) structure whose Type field is set to [D3D12_HIT_GROUP_TYPE_TRIANGLES](/windows/win32/api/d3d12/ne-d3d12-d3d12_hit_group_type#constants).</span></span>

<span data-ttu-id="4babc-189">Ce sous-objet est déclaré avec la syntaxe</span><span class="sxs-lookup"><span data-stu-id="4babc-189">This subobject is declared with the syntax</span></span>

``` syntax
TriangleHitGroup Name = 
{ 
    AnyHitShader,
    ClosestHitShader
};
```

| <span data-ttu-id="4babc-190">Élément</span><span class="sxs-lookup"><span data-stu-id="4babc-190">Item</span></span>                                                                                         | <span data-ttu-id="4babc-191">Description</span><span class="sxs-lookup"><span data-stu-id="4babc-191">Description</span></span>                                                                            |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4babc-192"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**Nomme**</span><span class="sxs-lookup"><span data-stu-id="4babc-192"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**Name**</span></span><br/>     | <span data-ttu-id="4babc-193">Chaîne ASCII qui identifie de façon unique le nom de la variable.</span><span class="sxs-lookup"><span data-stu-id="4babc-193">An ASCII string that uniquely identifies the variable name.</span></span><br/>                 |
| <span data-ttu-id="4babc-194"><span id="AnyHitShader"></span><span id="anyhitshader"></span><span id="ANYHITSHADER"></span>**AnyHitShader**</span><span class="sxs-lookup"><span data-stu-id="4babc-194"><span id="AnyHitShader"></span><span id="anyhitshader"></span><span id="ANYHITSHADER"></span>**AnyHitShader**</span></span><br/>     | <span data-ttu-id="4babc-195">Nom de chaîne du nuanceur anyhit pour le groupe d’accès ou une chaîne vide.</span><span class="sxs-lookup"><span data-stu-id="4babc-195">String name of the anyhit shader for the hit group, or an empty string.</span></span><br/> |
| <span data-ttu-id="4babc-196"><span id="ClosestHitShader"></span><span id="closesthitshader"></span><span id="CLOSESTHITSHADER"></span>**ClosestHitShader**</span><span class="sxs-lookup"><span data-stu-id="4babc-196"><span id="ClosestHitShader"></span><span id="closesthitshader"></span><span id="CLOSESTHITSHADER"></span>**ClosestHitShader**</span></span><br/> | <span data-ttu-id="4babc-197">Nom de chaîne du nuanceur de correspondance le plus proche pour le groupe d’accès ou une chaîne vide.</span><span class="sxs-lookup"><span data-stu-id="4babc-197">String name of the closest hit shader for the hit group, or an empty string.</span></span><br/> |


<span data-ttu-id="4babc-198">Exemple :</span><span class="sxs-lookup"><span data-stu-id="4babc-198">Example:</span></span>
```
TriangleHitGroup MyHitGroup =
{
    "",                    // AnyHit
    "MyClosestHitShader",  // ClosestHit
};
```

<span data-ttu-id="4babc-199">Notez que les deux champs utilisent des noms *exportés* .</span><span class="sxs-lookup"><span data-stu-id="4babc-199">Note that both fields use *exported* names.</span></span> <span data-ttu-id="4babc-200">Un nom exporté peut être différent du nom d’origine en langage HLSL, si l’application choisit d’effectuer une exportation-attribution d’un nouveau nom.</span><span class="sxs-lookup"><span data-stu-id="4babc-200">An exported name may be different from the original name in HLSL, if the application chooses to do export-renaming.</span></span>

## <a name="proceduralprimitivehitgroup"></a><span data-ttu-id="4babc-201">ProceduralPrimitiveHitGroup</span><span class="sxs-lookup"><span data-stu-id="4babc-201">ProceduralPrimitiveHitGroup</span></span>

<span data-ttu-id="4babc-202">Un ProceduralPrimitiveHitGroup correspond à une structure [D3D12_HIT_GROUP_DESC](/windows/win32/api/d3d12/ns-d3d12-d3d12_hit_group_desc) dont le champ de type est défini sur [D3D12_HIT_GROUP_TYPE_PROCEDURAL_PRIMITIVE](/windows/win32/api/d3d12/ne-d3d12-d3d12_hit_group_type#constants).</span><span class="sxs-lookup"><span data-stu-id="4babc-202">A ProceduralPrimitiveHitGroup corresponds to a [D3D12_HIT_GROUP_DESC](/windows/win32/api/d3d12/ns-d3d12-d3d12_hit_group_desc) structure whose Type field is set to [D3D12_HIT_GROUP_TYPE_PROCEDURAL_PRIMITIVE](/windows/win32/api/d3d12/ne-d3d12-d3d12_hit_group_type#constants).</span></span>

<span data-ttu-id="4babc-203">Ce sous-objet est déclaré avec la syntaxe</span><span class="sxs-lookup"><span data-stu-id="4babc-203">This subobject is declared with the syntax</span></span>

``` syntax
ProceduralPrimitiveHitGroup Name = 
{ 
    AnyHitShader,
    ClosestHitShader,
    IntersectionShader
};
```

| <span data-ttu-id="4babc-204">Élément</span><span class="sxs-lookup"><span data-stu-id="4babc-204">Item</span></span>                                                                                         | <span data-ttu-id="4babc-205">Description</span><span class="sxs-lookup"><span data-stu-id="4babc-205">Description</span></span>                                                                            |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4babc-206"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**Nomme**</span><span class="sxs-lookup"><span data-stu-id="4babc-206"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**Name**</span></span><br/>     | <span data-ttu-id="4babc-207">Chaîne ASCII qui identifie de façon unique le nom de la variable.</span><span class="sxs-lookup"><span data-stu-id="4babc-207">An ASCII string that uniquely identifies the variable name.</span></span><br/>                 |
| <span data-ttu-id="4babc-208"><span id="AnyHitShader"></span><span id="anyhitshader"></span><span id="ANYHITSHADER"></span>**AnyHitShader**</span><span class="sxs-lookup"><span data-stu-id="4babc-208"><span id="AnyHitShader"></span><span id="anyhitshader"></span><span id="ANYHITSHADER"></span>**AnyHitShader**</span></span><br/>     | <span data-ttu-id="4babc-209">Nom de chaîne du nuanceur anyhit pour le groupe d’accès ou une chaîne vide.</span><span class="sxs-lookup"><span data-stu-id="4babc-209">String name of the anyhit shader for the hit group, or an empty string.</span></span><br/> |
| <span data-ttu-id="4babc-210"><span id="ClosestHitShader"></span><span id="closesthitshader"></span><span id="CLOSESTHITSHADER"></span>**ClosestHitShader**</span><span class="sxs-lookup"><span data-stu-id="4babc-210"><span id="ClosestHitShader"></span><span id="closesthitshader"></span><span id="CLOSESTHITSHADER"></span>**ClosestHitShader**</span></span><br/> | <span data-ttu-id="4babc-211">Nom de chaîne du nuanceur de correspondance le plus proche pour le groupe d’accès ou une chaîne vide.</span><span class="sxs-lookup"><span data-stu-id="4babc-211">String name of the closest hit shader for the hit group, or an empty string.</span></span><br/> |
| <span data-ttu-id="4babc-212"><span id="IntersectionShader"></span><span id="intersectionshader"></span><span id="INTERSECTIONSHADER"></span>**IntersectionShader**</span><span class="sxs-lookup"><span data-stu-id="4babc-212"><span id="IntersectionShader"></span><span id="intersectionshader"></span><span id="INTERSECTIONSHADER"></span>**IntersectionShader**</span></span><br/> | <span data-ttu-id="4babc-213">Nom de chaîne du nuanceur d’intersection pour le groupe d’accès ou une chaîne vide.</span><span class="sxs-lookup"><span data-stu-id="4babc-213">String name of the intersection shader for the hit group, or an empty string.</span></span><br/> |


<span data-ttu-id="4babc-214">Exemple :</span><span class="sxs-lookup"><span data-stu-id="4babc-214">Example:</span></span>
```
ProceduralPrimitiveHitGroup MyProceduralHitGroup
{
    "MyAnyHit",       // AnyHit
    "MyClosestHit",   // ClosestHit
    "MyIntersection"  // Intersection
};

```

<span data-ttu-id="4babc-215">Notez que les trois champs utilisent des noms *exportés* .</span><span class="sxs-lookup"><span data-stu-id="4babc-215">Note that the three fields use *exported* names.</span></span> <span data-ttu-id="4babc-216">Un nom exporté peut être différent du nom d’origine en langage HLSL, si l’application choisit d’effectuer une exportation-attribution d’un nouveau nom.</span><span class="sxs-lookup"><span data-stu-id="4babc-216">An exported name may be different from the original name in HLSL, if the application chooses to do export-renaming.</span></span>

## <a name="remarks"></a><span data-ttu-id="4babc-217">Notes</span><span class="sxs-lookup"><span data-stu-id="4babc-217">Remarks</span></span>

<span data-ttu-id="4babc-218">Les sous-objets ont la notion d' « Association », ou « quel sous-objet va utiliser l’exportation ».</span><span class="sxs-lookup"><span data-stu-id="4babc-218">Subobjects have the notion of "association", or "which subobject goes with which export".</span></span>

<span data-ttu-id="4babc-219">Lorsque vous spécifiez des sous-objets à l’aide du code du nuanceur, le choix de « quel sous-objet va utiliser pour l’exportation » suit les règles comme indiqué dans la [spécification DXR](https://microsoft.github.io/DirectX-Specs/d3d/Raytracing.html#subobject-association-behavior).</span><span class="sxs-lookup"><span data-stu-id="4babc-219">When specifying subobjects through shader code, the choice of "which subobject goes with which export" follows the rules as outlined in the [DXR specification](https://microsoft.github.io/DirectX-Specs/d3d/Raytracing.html#subobject-association-behavior).</span></span> <span data-ttu-id="4babc-220">En particulier, supposez qu’une application a une exportation.</span><span class="sxs-lookup"><span data-stu-id="4babc-220">In particular, suppose an application has some export.</span></span> <span data-ttu-id="4babc-221">Si une application associe cette exportation à la signature racine A par le biais du code du nuanceur et de la signature racine B par le biais du code de l’application, B est celui qui est utilisé.</span><span class="sxs-lookup"><span data-stu-id="4babc-221">If an application associates that export with root signature A through shader-code and root signature B through application code, B is the one that gets used.</span></span> <span data-ttu-id="4babc-222">La conception de « use B » au lieu de « produire une erreur » donne aux applications la possibilité de remplacer facilement les associations DXIL à l’aide du code d’application, au lieu de devoir recompiler les nuanceurs pour résoudre les problèmes de correspondance.</span><span class="sxs-lookup"><span data-stu-id="4babc-222">The design of "use B" instead of "produce an error" gives applications the ability to conveniently override DXIL associations using application code, rather than be forced to recompile shaders to resolve mismatching things.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4babc-223">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4babc-223">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4babc-224">Le billet de blog du développeur DirectX « nouveauté de D3D12 – DirectX Raytracing (DXR) prend désormais en charge les sous-objets de bibliothèque »</span><span class="sxs-lookup"><span data-stu-id="4babc-224">DirectX Developer Blog post "New in D3D12 – DirectX Raytracing (DXR) now supports library subobjects"</span></span>](https://devblogs.microsoft.com/directx/dxr-library-subobjects/)

[<span data-ttu-id="4babc-225">Spécifications fonctionnelles de DirectX Raytracing (DXR)</span><span class="sxs-lookup"><span data-stu-id="4babc-225">DirectX Raytracing (DXR) Functional Spec</span></span>](https://microsoft.github.io/DirectX-Specs/d3d/Raytracing.html)

[<span data-ttu-id="4babc-226">Exemple : D3D12RaytracingLibrarySubobjects</span><span class="sxs-lookup"><span data-stu-id="4babc-226">Sample: D3D12RaytracingLibrarySubobjects</span></span>](https://github.com/Microsoft/DirectX-Graphics-Samples/tree/develop/Samples/Desktop/D3D12Raytracing/src/D3D12RaytracingLibrarySubobjects)

</dt> </dl>