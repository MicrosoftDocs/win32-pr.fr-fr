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
# <a name="state-objects"></a>Objets d’état

Avec les modèles de nuanceur 6,3 et versions ultérieures, les applications ont la possibilité de définir des objets d’État DXR directement dans le code du nuanceur HLSL en plus de l’utilisation des API Direct3D 12.

En langage HLSL, les objets d’État sont déclarés avec la syntaxe suivante :

``` syntax
Type Name = 
{ 
    Field1,
    Field2,
    ...
};
```



| Élément                                                                                         | Description                                                                            |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Type"></span><span id="type"></span><span id="TYPE"></span>**Entrer**<br/>     | Identifie le type de sous-objet. Doit être l’un des types de sous-objets HLSL pris en charge.<br/>     |
| <span id="Name"></span><span id="name"></span><span id="NAME"></span>**Nomme**<br/>     | Chaîne ASCII qui identifie de façon unique le nom de la variable.<br/>                 |
| <span id="Field"></span><span id="field"></span><span id="FIELD"></span>**Champ [1, 2,...]**<br/> | Champs du sous-objet. Les champs spécifiques pour chaque type de sous-objet sont décrits ci-dessous.<br/> |




Liste des types de sous-objets :
-   [StateObjectConfig](#stateobjectconfig)
-   [GlobalRootSignature](#globalrootsignature)
-   [LocalRootSignature](#localrootsignature)
-   [SubobjectToExportsAssocation](#subobjecttoexportsassocation)
-   [RaytracingShaderConfig](#raytracingshaderconfig)
-   [RaytracingPipelineConfig](#raytracingpipelineconfig)
-   [TriangleHitGroup](#trianglehitgroup)
-   [ProceduralPrimitiveHitGroup](#proceduralprimitivehitgroup)

## <a name="stateobjectconfig"></a>StateObjectConfig

Le type de sous-objet StateObjectConfig correspond à une structure [D3D12_STATE_OBJECT_CONFIG](/windows/win32/api/d3d12/ns-d3d12-d3d12_state_object_config) .

Il a un champ, un indicateur de bits, qui est l’un des

* STATE_OBJECT_FLAGS_ALLOW_LOCAL_DEPENDENCIES_ON_EXTERNAL_DEFINITONS
* STATE_OBJECT_FLAGS_ALLOW_EXTERNAL_DEPENDENCIES_ON_LOCAL_DEFINITIONS

ou zéro pour aucun d’entre eux.

Exemple :

```
StateObjectConfig MyStateObjectConfig = 
{ 
    STATE_OBJECT_FLAGS_ALLOW_LOCAL_DEPENDENCIES_ON_EXTERNAL_DEFINITONS
};
```

## <a name="globalrootsignature"></a>GlobalRootSignature
Un GlobalRootSignature correspond à une structure [D3D12_GLOBAL_ROOT_SIGNATURE](/windows/win32/api/d3d12/ns-d3d12-d3d12_global_root_signature) .

Les champs sont constitués d’un certain nombre de chaînes décrivant les parties de la signature racine. Pour plus d’informations, consultez [spécification de signatures racines en langage HLSL](../direct3d12/specifying-root-signatures-in-hlsl.md).

Exemple :
```
GlobalRootSignature MyGlobalRootSignature =
{
    "DescriptorTable(UAV(u0)),"                     // Output texture
    "SRV(t0),"                                      // Acceleration structure
    "CBV(b0),"                                      // Scene constants
    "DescriptorTable(SRV(t1, numDescriptors = 2))"  // Static index and vertex buffers.
};
```

## <a name="localrootsignature"></a>LocalRootSignature
Un LocalRootSignature correspond à une structure [D3D12_LOCAL_ROOT_SIGNATURE](/windows/win32/api/d3d12/ns-d3d12-d3d12_local_root_signature) .

Tout comme le sous-objet signature racine globale, les champs se composent d’un certain nombre de chaînes décrivant les parties de la signature racine. Pour plus d’informations, consultez [spécification de signatures racines en langage HLSL](../direct3d12/specifying-root-signatures-in-hlsl.md).

Exemple :
```
LocalRootSignature MyLocalRootSignature = 
{
    "RootConstants(num32BitConstants = 4, b1)"  // Cube constants 
};
```

## <a name="subobjecttoexportsassocation"></a>SubobjectToExportsAssocation
Par défaut, un sous-objet simplement déclaré dans la même bibliothèque qu’une exportation est en mesure de s’appliquer à cette exportation. Toutefois, les applications ont la possibilité de la remplacer et d’obtenir des informations spécifiques sur le type de sous-objet utilisé pour l’exportation. En langage HLSL, cette « association explicite » s’effectue à l’aide de SubobjectToExportsAssocation.

Un SubobjectToExportsAssocation correspond à une structure [D3D12_DXIL_SUBOBJECT_TO_EXPORTS_ASSOCIATION ](/windows/win32/api/d3d12/ns-d3d12-d3d12_dxil_subobject_to_exports_association) .

Ce sous-objet est déclaré avec la syntaxe

``` syntax
SubobjectToExportsAssocation Name = 
{ 
    SubobjectName,
    Exports
};
```

| Élément                                                                                         | Description                                                                            |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Name"></span><span id="name"></span><span id="NAME"></span>**Nomme**<br/>     | Chaîne ASCII qui identifie de façon unique le nom de la variable.<br/>                 |
| <span id="SubobjectName"></span><span id="subobjectname"></span><span id="SUBOBJECTNAME"></span>**SubobjectName**<br/>     | Chaîne qui identifie un sous-objet exporté.<br/> |
| <span id="Exports"></span><span id="exports"></span><span id="EXPORTS"></span>**Ventes**<br/> | Chaîne contenant une liste d’exportations délimitées par des points-virgules.<br/> |


Exemple :
```
SubobjectToExportsAssociation MyLocalRootSignatureAssociation =
{
    "MyLocalRootSignature",    // Subobject name
    "MyHitGroup;MyMissShader"  // Exports association 
};
```

Notez que les deux champs utilisent des noms *exportés* . Un nom exporté peut être différent du nom d’origine en langage HLSL, si l’application choisit d’effectuer une exportation-attribution d’un nouveau nom.

## <a name="raytracingshaderconfig"></a>RaytracingShaderConfig

Un RaytracingShaderConfig correspond à une structure [D3D12_RAYTRACING_SHADER_CONFIG](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_shader_config) .

Ce sous-objet est déclaré avec la syntaxe

``` syntax
RaytracingShaderConfig Name = 
{ 
    MaxPayloadSize,
    MaxAttributeSize
};
```

| Élément                                                                                         | Description                                                                            |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Name"></span><span id="name"></span><span id="NAME"></span>**Nomme**<br/>     | Chaîne ASCII qui identifie de façon unique le nom de la variable.<br/>                 |
| <span id="MaxPayloadSize"></span><span id="maxpayloadsize"></span><span id="MAXPAYLOADSIZE"></span>**MaxPayloadSize**<br/>     | Valeur numérique pour le stockage maximal pour les scalaires (comptée comme 4 octets chacun) dans les charges utiles de Ray pour les nuanceurs de Raytracing associés.<br/> |
| <span id="MaxAttributeSize"></span><span id="maxattributesize"></span><span id="MAXATTRIBUTESIZE"></span>**MaxAttributeSize**<br/> | Valeur numérique pour le nombre maximal de scalaires (comptant 4 octets chacun) qui peut être utilisé pour les attributs des nuanceurs Raytracing associés. La valeur ne peut pas dépasser [D3D12_RAYTRACING_MAX_ATTRIBUTE_SIZE_IN_BYTES](../direct3d12/constants.md).<br/> |


Exemple :
```
RaytracingShaderConfig MyShaderConfig =
{
    16,  // Max payload size
    8    // Max attribute size
};
```

## <a name="raytracingpipelineconfig"></a>RaytracingPipelineConfig

Un RaytracingPipelineConfig correspond à une structure [D3D12_RAYTRACING_PIPELINE_CONFIG](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_pipeline_config) .

Ce sous-objet est déclaré avec la syntaxe

``` syntax
RaytracingPipelineConfig Name = 
{ 
    MaxTraceRecursionDepth
};
```

| Élément                                                                                         | Description                                                                            |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Name"></span><span id="name"></span><span id="NAME"></span>**Nomme**<br/>     | Chaîne ASCII qui identifie de façon unique le nom de la variable.<br/>                 |
| <span id="MaxTraceRecursionDepth"></span><span id="maxtracerecursiondepth"></span><span id="MAXTRACERECURSIONDEPTH"></span>**MaxTraceRecursionDepth**<br/>     | Limite numérique à utiliser pour la récursivité de rayon dans le pipeline Raytracing. Il s’agit d’un nombre compris entre 0 et 31, inclus. <br/> |


Exemple :
```
RaytracingPipelineConfig MyPipelineConfig =
{
    1  // Max trace recursion depth
};
```
Étant donné qu’il y a un coût de performance pour la récursivité Raytracing, les applications doivent utiliser la profondeur de récursivité la plus faible nécessaire pour les résultats souhaités.

Si les appels de nuanceur n’ont pas encore atteint la profondeur maximale de récursivité, ils peuvent appeler [TraceRay](../direct3d12/traceray-function.md) un nombre quelconque de fois. Toutefois, s’ils atteignent ou dépassent la profondeur maximale de récursivité, l’appel de TraceRay met l’appareil en état de suppression. Par conséquent, les nuanceurs Raytracing doivent veiller à arrêter d’appeler TraceRay s’ils ont atteint ou dépassé la profondeur maximale de récursivité.

## <a name="trianglehitgroup"></a>TriangleHitGroup

Un TriangleHitGroup correspond à une structure [D3D12_HIT_GROUP_DESC](/windows/win32/api/d3d12/ns-d3d12-d3d12_hit_group_desc) dont le champ de type est défini sur [D3D12_HIT_GROUP_TYPE_TRIANGLES](/windows/win32/api/d3d12/ne-d3d12-d3d12_hit_group_type#constants).

Ce sous-objet est déclaré avec la syntaxe

``` syntax
TriangleHitGroup Name = 
{ 
    AnyHitShader,
    ClosestHitShader
};
```

| Élément                                                                                         | Description                                                                            |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Name"></span><span id="name"></span><span id="NAME"></span>**Nomme**<br/>     | Chaîne ASCII qui identifie de façon unique le nom de la variable.<br/>                 |
| <span id="AnyHitShader"></span><span id="anyhitshader"></span><span id="ANYHITSHADER"></span>**AnyHitShader**<br/>     | Nom de chaîne du nuanceur anyhit pour le groupe d’accès ou une chaîne vide.<br/> |
| <span id="ClosestHitShader"></span><span id="closesthitshader"></span><span id="CLOSESTHITSHADER"></span>**ClosestHitShader**<br/> | Nom de chaîne du nuanceur de correspondance le plus proche pour le groupe d’accès ou une chaîne vide.<br/> |


Exemple :
```
TriangleHitGroup MyHitGroup =
{
    "",                    // AnyHit
    "MyClosestHitShader",  // ClosestHit
};
```

Notez que les deux champs utilisent des noms *exportés* . Un nom exporté peut être différent du nom d’origine en langage HLSL, si l’application choisit d’effectuer une exportation-attribution d’un nouveau nom.

## <a name="proceduralprimitivehitgroup"></a>ProceduralPrimitiveHitGroup

Un ProceduralPrimitiveHitGroup correspond à une structure [D3D12_HIT_GROUP_DESC](/windows/win32/api/d3d12/ns-d3d12-d3d12_hit_group_desc) dont le champ de type est défini sur [D3D12_HIT_GROUP_TYPE_PROCEDURAL_PRIMITIVE](/windows/win32/api/d3d12/ne-d3d12-d3d12_hit_group_type#constants).

Ce sous-objet est déclaré avec la syntaxe

``` syntax
ProceduralPrimitiveHitGroup Name = 
{ 
    AnyHitShader,
    ClosestHitShader,
    IntersectionShader
};
```

| Élément                                                                                         | Description                                                                            |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Name"></span><span id="name"></span><span id="NAME"></span>**Nomme**<br/>     | Chaîne ASCII qui identifie de façon unique le nom de la variable.<br/>                 |
| <span id="AnyHitShader"></span><span id="anyhitshader"></span><span id="ANYHITSHADER"></span>**AnyHitShader**<br/>     | Nom de chaîne du nuanceur anyhit pour le groupe d’accès ou une chaîne vide.<br/> |
| <span id="ClosestHitShader"></span><span id="closesthitshader"></span><span id="CLOSESTHITSHADER"></span>**ClosestHitShader**<br/> | Nom de chaîne du nuanceur de correspondance le plus proche pour le groupe d’accès ou une chaîne vide.<br/> |
| <span id="IntersectionShader"></span><span id="intersectionshader"></span><span id="INTERSECTIONSHADER"></span>**IntersectionShader**<br/> | Nom de chaîne du nuanceur d’intersection pour le groupe d’accès ou une chaîne vide.<br/> |


Exemple :
```
ProceduralPrimitiveHitGroup MyProceduralHitGroup
{
    "MyAnyHit",       // AnyHit
    "MyClosestHit",   // ClosestHit
    "MyIntersection"  // Intersection
};

```

Notez que les trois champs utilisent des noms *exportés* . Un nom exporté peut être différent du nom d’origine en langage HLSL, si l’application choisit d’effectuer une exportation-attribution d’un nouveau nom.

## <a name="remarks"></a>Notes

Les sous-objets ont la notion d' « Association », ou « quel sous-objet va utiliser l’exportation ».

Lorsque vous spécifiez des sous-objets à l’aide du code du nuanceur, le choix de « quel sous-objet va utiliser pour l’exportation » suit les règles comme indiqué dans la [spécification DXR](https://microsoft.github.io/DirectX-Specs/d3d/Raytracing.html#subobject-association-behavior). En particulier, supposez qu’une application a une exportation. Si une application associe cette exportation à la signature racine A par le biais du code du nuanceur et de la signature racine B par le biais du code de l’application, B est celui qui est utilisé. La conception de « use B » au lieu de « produire une erreur » donne aux applications la possibilité de remplacer facilement les associations DXIL à l’aide du code d’application, au lieu de devoir recompiler les nuanceurs pour résoudre les problèmes de correspondance.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Le billet de blog du développeur DirectX « nouveauté de D3D12 – DirectX Raytracing (DXR) prend désormais en charge les sous-objets de bibliothèque »](https://devblogs.microsoft.com/directx/dxr-library-subobjects/)

[Spécifications fonctionnelles de DirectX Raytracing (DXR)](https://microsoft.github.io/DirectX-Specs/d3d/Raytracing.html)

[Exemple : D3D12RaytracingLibrarySubobjects](https://github.com/Microsoft/DirectX-Graphics-Samples/tree/develop/Samples/Desktop/D3D12Raytracing/src/D3D12RaytracingLibrarySubobjects)

</dt> </dl>