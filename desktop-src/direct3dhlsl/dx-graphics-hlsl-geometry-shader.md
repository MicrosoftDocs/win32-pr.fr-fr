---
title: Objet Geometry-Shader
description: Un objet de nuanceur Geometry traite les primitives entières. Pour déclarer un objet Geometry-Shader, utilisez la syntaxe ci-après.
ms.assetid: d5c1c22b-6fa6-40a8-900f-6d74f74468c1
keywords:
- maxvertexcount (DirectX HLSL)
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: dadb0e8bb3ddda16305ac701b34523668bd9c1a5
ms.sourcegitcommit: 477b1efe7d9c2f91d5f2ac588a20edf348b1c734
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2019
ms.locfileid: "103679369"
---
# <a name="geometry-shader-object"></a><span data-ttu-id="d5289-105">Objet Geometry-Shader</span><span class="sxs-lookup"><span data-stu-id="d5289-105">Geometry-Shader Object</span></span>

<span data-ttu-id="d5289-106">Un objet de nuanceur Geometry traite les primitives entières.</span><span class="sxs-lookup"><span data-stu-id="d5289-106">A geometry-shader object processes entire primitives.</span></span> <span data-ttu-id="d5289-107">Pour déclarer un objet Geometry-Shader, utilisez la syntaxe ci-après.</span><span class="sxs-lookup"><span data-stu-id="d5289-107">Use the following syntax to declare a geometry-shader object.</span></span>



|                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5289-108">\[maxvertexcount (*NumVerts*) \] void *ShaderName* ( *PrimitiveType nom du type de données \[ \] NumElements*, INOUT *StreamOutputObject* );</span><span class="sxs-lookup"><span data-stu-id="d5289-108">\[maxvertexcount(*NumVerts*)\] void *ShaderName* (   *PrimitiveType DataType Name \[ NumElements \]*,   inout *StreamOutputObject*  );</span></span> |



 

## <a name="parameters"></a><span data-ttu-id="d5289-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d5289-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5289-110"><span id="_maxvertexcount_NumVerts__"></span><span id="_maxvertexcount_numverts__"></span><span id="_MAXVERTEXCOUNT_NUMVERTS__"></span>\[maxvertexcount (*NumVerts*)\]</span><span class="sxs-lookup"><span data-stu-id="d5289-110"><span id="_maxvertexcount_NumVerts__"></span><span id="_maxvertexcount_numverts__"></span><span id="_MAXVERTEXCOUNT_NUMVERTS__"></span>\[maxvertexcount(*NumVerts*)\]</span></span>
</dt> <dd>

<span data-ttu-id="d5289-111">\[dans une \] déclaration pour le nombre maximal de vertex à créer.</span><span class="sxs-lookup"><span data-stu-id="d5289-111">\[in\] Declaration for the maximum number of vertices to create.</span></span>

-   <span data-ttu-id="d5289-112">\[maxvertexcount () \] -mot clé required ; les crochets et les parenthèses sont des caractères requis pour une syntaxe correcte.</span><span class="sxs-lookup"><span data-stu-id="d5289-112">\[maxvertexcount()\] - required keyword; brackets and parenthesis are required characters for correct syntax.</span></span>
-   <span data-ttu-id="d5289-113">*NumVerts* : nombre entier représentant le nombre de vertex.</span><span class="sxs-lookup"><span data-stu-id="d5289-113">*NumVerts* - An integer number representing the number of vertices.</span></span>

</dd> <dt>

<span data-ttu-id="d5289-114"><span id="ShaderName"></span><span id="shadername"></span><span id="SHADERNAME"></span>*ShaderName*</span><span class="sxs-lookup"><span data-stu-id="d5289-114"><span id="ShaderName"></span><span id="shadername"></span><span id="SHADERNAME"></span>*ShaderName*</span></span>
</dt> <dd>

<span data-ttu-id="d5289-115">\[dans \] une chaîne ASCII qui contient un nom unique pour la fonction Geometry-Shader.</span><span class="sxs-lookup"><span data-stu-id="d5289-115">\[in\] An ASCII string that contains a unique name for the geometry-shader function.</span></span>

</dd> <dt>

<span data-ttu-id="d5289-116"><span id="PrimitiveType_DataType_Name___NumElements__"></span><span id="primitivetype_datatype_name___numelements__"></span><span id="PRIMITIVETYPE_DATATYPE_NAME___NUMELEMENTS__"></span>*Nom de type de données PrimitiveType \[ NumElements \]*</span><span class="sxs-lookup"><span data-stu-id="d5289-116"><span id="PrimitiveType_DataType_Name___NumElements__"></span><span id="primitivetype_datatype_name___numelements__"></span><span id="PRIMITIVETYPE_DATATYPE_NAME___NUMELEMENTS__"></span>*PrimitiveType DataType Name \[ NumElements \]*</span></span>
</dt> <dd>

<span data-ttu-id="d5289-117">*PrimitiveType* -type primitif, qui détermine l’ordre des données Primitives.</span><span class="sxs-lookup"><span data-stu-id="d5289-117">*PrimitiveType* - Primitive type, which determines the order of the primitive data.</span></span>



| <span data-ttu-id="d5289-118">Type primitif</span><span class="sxs-lookup"><span data-stu-id="d5289-118">Primitive Type</span></span> | <span data-ttu-id="d5289-119">Description</span><span class="sxs-lookup"><span data-stu-id="d5289-119">Description</span></span>                                                   |
|----------------|---------------------------------------------------------------|
| <span data-ttu-id="d5289-120">*point*</span><span class="sxs-lookup"><span data-stu-id="d5289-120">*point*</span></span>        | <span data-ttu-id="d5289-121">Liste des points</span><span class="sxs-lookup"><span data-stu-id="d5289-121">Point list</span></span>                                                    |
| <span data-ttu-id="d5289-122">*spline*</span><span class="sxs-lookup"><span data-stu-id="d5289-122">*line*</span></span>         | <span data-ttu-id="d5289-123">Liste de lignes ou de lignes</span><span class="sxs-lookup"><span data-stu-id="d5289-123">Line list or line strip</span></span>                                       |
| <span data-ttu-id="d5289-124">*placé*</span><span class="sxs-lookup"><span data-stu-id="d5289-124">*triangle*</span></span>     | <span data-ttu-id="d5289-125">Liste de triangles ou bande triangulaire</span><span class="sxs-lookup"><span data-stu-id="d5289-125">Triangle list or triangle strip</span></span>                               |
| <span data-ttu-id="d5289-126">*lineadj*</span><span class="sxs-lookup"><span data-stu-id="d5289-126">*lineadj*</span></span>      | <span data-ttu-id="d5289-127">Liste des lignes avec contiguïté ou frange avec contiguïté</span><span class="sxs-lookup"><span data-stu-id="d5289-127">Line list with adjacency or line strip with adjacency</span></span>         |
| <span data-ttu-id="d5289-128">*triangleadj*</span><span class="sxs-lookup"><span data-stu-id="d5289-128">*triangleadj*</span></span>  | <span data-ttu-id="d5289-129">Liste de triangles avec contiguïté ou bande triangulaire avec contiguïté</span><span class="sxs-lookup"><span data-stu-id="d5289-129">Triangle list with adjacency or triangle strip with adjacency</span></span> |



 

<span data-ttu-id="d5289-130">*Type de données*  -  \[ dans \] un type de données d’entrée, peut être n’importe quel [type de données HLSL](dx-graphics-hlsl-data-types.md).</span><span class="sxs-lookup"><span data-stu-id="d5289-130">*DataType* - \[in\] An input data type; can be any [HLSL data type](dx-graphics-hlsl-data-types.md).</span></span>

<span data-ttu-id="d5289-131">*Nom* -argument Name ; Il s’agit d’une chaîne ASCII.</span><span class="sxs-lookup"><span data-stu-id="d5289-131">*Name* - Argument name; this is an ASCII string.</span></span>

<span data-ttu-id="d5289-132">*NumElements* : taille du tableau de l’entrée, qui dépend du *PrimitiveType* , comme indiqué dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="d5289-132">*NumElements* - Array size of the input, which depends on the *PrimitiveType* as shown in the following table.</span></span>

| <span data-ttu-id="d5289-133">Type primitif</span><span class="sxs-lookup"><span data-stu-id="d5289-133">Primitive Type</span></span> | <span data-ttu-id="d5289-134">NumElements</span><span class="sxs-lookup"><span data-stu-id="d5289-134">NumElements</span></span>                                                                                                  |
|----------------|--------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5289-135">*point*</span><span class="sxs-lookup"><span data-stu-id="d5289-135">*point*</span></span>        | <span data-ttu-id="d5289-136">\[1\]</span><span class="sxs-lookup"><span data-stu-id="d5289-136">\[1\]</span></span><br/> <span data-ttu-id="d5289-137">Vous ne pouvez utiliser qu’un seul point à la fois.</span><span class="sxs-lookup"><span data-stu-id="d5289-137">You operate on only one point at a time.</span></span><br/>                                         |
| <span data-ttu-id="d5289-138">*spline*</span><span class="sxs-lookup"><span data-stu-id="d5289-138">*line*</span></span>         | <span data-ttu-id="d5289-139">\[2\]</span><span class="sxs-lookup"><span data-stu-id="d5289-139">\[2\]</span></span><br/> <span data-ttu-id="d5289-140">Une ligne requiert deux vertex.</span><span class="sxs-lookup"><span data-stu-id="d5289-140">A line requires two vertices.</span></span><br/>                                                    |
| <span data-ttu-id="d5289-141">*placé*</span><span class="sxs-lookup"><span data-stu-id="d5289-141">*triangle*</span></span>     | <span data-ttu-id="d5289-142">\[3\]</span><span class="sxs-lookup"><span data-stu-id="d5289-142">\[3\]</span></span><br/> <span data-ttu-id="d5289-143">Un triangle requiert trois vertex.</span><span class="sxs-lookup"><span data-stu-id="d5289-143">A triangle requires three vertices.</span></span><br/>                                              |
| <span data-ttu-id="d5289-144">*lineadj*</span><span class="sxs-lookup"><span data-stu-id="d5289-144">*lineadj*</span></span>      | <span data-ttu-id="d5289-145">\[4\]</span><span class="sxs-lookup"><span data-stu-id="d5289-145">\[4\]</span></span><br/> <span data-ttu-id="d5289-146">Un lineadj a deux extrémités ; par conséquent, il requiert quatre vertex.</span><span class="sxs-lookup"><span data-stu-id="d5289-146">A lineadj has two ends; therefore, it requires four vertices.</span></span><br/>                    |
| <span data-ttu-id="d5289-147">*triangleadj*</span><span class="sxs-lookup"><span data-stu-id="d5289-147">*triangleadj*</span></span>  | <span data-ttu-id="d5289-148">\[6\]</span><span class="sxs-lookup"><span data-stu-id="d5289-148">\[6\]</span></span><br/> <span data-ttu-id="d5289-149">Une bordure triangleadj trois triangles supplémentaires ; par conséquent, il requiert six vertex.</span><span class="sxs-lookup"><span data-stu-id="d5289-149">A triangleadj borders three more triangles; therefore, it requires six vertices.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="d5289-150"><span id="StreamOutputObject"></span><span id="streamoutputobject"></span><span id="STREAMOUTPUTOBJECT"></span>*StreamOutputObject*</span><span class="sxs-lookup"><span data-stu-id="d5289-150"><span id="StreamOutputObject"></span><span id="streamoutputobject"></span><span id="STREAMOUTPUTOBJECT"></span>*StreamOutputObject*</span></span>
</dt> <dd>

<span data-ttu-id="d5289-151">Déclaration de l' [objet de sortie de flux](dx-graphics-hlsl-so-type.md).</span><span class="sxs-lookup"><span data-stu-id="d5289-151">The declaration of the [stream-output object](dx-graphics-hlsl-so-type.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5289-152">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="d5289-152">Return Value</span></span>

<span data-ttu-id="d5289-153">None</span><span class="sxs-lookup"><span data-stu-id="d5289-153">None</span></span>

## <a name="remarks"></a><span data-ttu-id="d5289-154">Notes</span><span class="sxs-lookup"><span data-stu-id="d5289-154">Remarks</span></span>

<span data-ttu-id="d5289-155">Le diagramme suivant montre les différents types primitifs pour un objet de nuanceur Geometry.</span><span class="sxs-lookup"><span data-stu-id="d5289-155">The following diagram shows the various primitive types for a geometry shader object.</span></span>

![illustration des différents types primitifs pour un objet de nuanceur Geometry](images/d3d11-gsinputs1.png)

<span data-ttu-id="d5289-157">Le diagramme suivant illustre les appels de nuanceur Geometry.</span><span class="sxs-lookup"><span data-stu-id="d5289-157">The following diagram shows geometry shader invocations.</span></span>

![illustration des appels de nuanceur Geometry](images/d3d11-gsinputs2.png)

## <a name="examples"></a><span data-ttu-id="d5289-159">Exemples</span><span class="sxs-lookup"><span data-stu-id="d5289-159">Examples</span></span>

<span data-ttu-id="d5289-160">Cet exemple est issu de l’exercice 1 de l' [atelier 4,0 de l’atelier du modèle de nuanceur Direct3D 10](https://msdn.microsoft.com/library/Ee416554(v=VS.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="d5289-160">This example is from exercise 1 from the [Direct3D 10 Shader Model 4.0 Workshop](https://msdn.microsoft.com/library/Ee416554(v=VS.85).aspx).</span></span>


```
[maxvertexcount(3)]
void GSScene( triangleadj GSSceneIn input[6], inout TriangleStream<PSSceneIn> OutputStream )
{   
    PSSceneIn output = (PSSceneIn)0;

    for( uint i=0; i<6; i+=2 )
    {
        output.Pos = input[i].Pos;
        output.Norm = input[i].Norm;
        output.Tex = input[i].Tex;
        
        OutputStream.Append( output );
    }
    
    OutputStream.RestartStrip();
}
```



## <a name="minimum-shader-model"></a><span data-ttu-id="d5289-161">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="d5289-161">Minimum Shader Model</span></span>

<span data-ttu-id="d5289-162">Cet objet est pris en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="d5289-162">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="d5289-163">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="d5289-163">Shader Model</span></span>                                                        | <span data-ttu-id="d5289-164">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="d5289-164">Supported</span></span> |
|---------------------------------------------------------------------|-----------|
| <span data-ttu-id="d5289-165">[Nuancier modèle 4](dx-graphics-hlsl-sm4.md) et modèles de nuanceur supérieurs</span><span class="sxs-lookup"><span data-stu-id="d5289-165">[Shader Model 4](dx-graphics-hlsl-sm4.md) and higher shader models</span></span> | <span data-ttu-id="d5289-166">Oui</span><span class="sxs-lookup"><span data-stu-id="d5289-166">yes</span></span>       |



 

## <a name="related-topics"></a><span data-ttu-id="d5289-167">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d5289-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d5289-168">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="d5289-168">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 





