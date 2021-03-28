---
title: Objet Stream-Output
description: Un objet de sortie de flux est un objet basé sur un modèle qui diffuse en continu des données à partir de l’étape Geometry-Shader. Utilisez la syntaxe suivante pour déclarer un objet de sortie de flux.
ms.assetid: 07a5489c-c238-4466-9282-5b168448aff7
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 98063ddb45633dda6c897abf0f82f29a394c3f95
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382108"
---
# <a name="stream-output-object"></a><span data-ttu-id="48368-104">Objet Stream-Output</span><span class="sxs-lookup"><span data-stu-id="48368-104">Stream-Output Object</span></span>

<span data-ttu-id="48368-105">Un objet de sortie de flux est un objet basé sur un modèle qui diffuse en continu des données à partir de l' [étape Geometry-Shader](/previous-versions//bb205146(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="48368-105">A stream-output object is a templated object that streams data out of the [geometry-shader stage](/previous-versions//bb205146(v=vs.85)).</span></span> <span data-ttu-id="48368-106">Utilisez la syntaxe suivante pour déclarer un objet de sortie de flux.</span><span class="sxs-lookup"><span data-stu-id="48368-106">Use the following syntax to declare a stream-output object.</span></span>



| <span data-ttu-id="48368-107">INOUT *StreamOutputObject* < nom de *type de données* >  *;*</span><span class="sxs-lookup"><span data-stu-id="48368-107">inout *StreamOutputObject*<*DataType*> *Name;*</span></span> |
|------------------------------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="48368-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="48368-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="48368-109"><span id="StreamOutputObject___________________________DataType_________________________________________Name"></span><span id="streamoutputobject___________________________datatype_________________________________________name"></span><span id="STREAMOUTPUTOBJECT___________________________DATATYPE_________________________________________NAME"></span>*StreamOutputObject*  <  *Type de données*  >    *Nom*</span><span class="sxs-lookup"><span data-stu-id="48368-109"><span id="StreamOutputObject___________________________DataType_________________________________________Name"></span><span id="streamoutputobject___________________________datatype_________________________________________name"></span><span id="STREAMOUTPUTOBJECT___________________________DATATYPE_________________________________________NAME"></span>*StreamOutputObject* < *DataType* >   *Name*</span></span>
</dt> <dd>

<span data-ttu-id="48368-110">Déclaration de l’objet de sortie de flux (SO).</span><span class="sxs-lookup"><span data-stu-id="48368-110">The stream-output object (SO) declaration.</span></span>



| <span data-ttu-id="48368-111">Types d’objets Stream-Output</span><span class="sxs-lookup"><span data-stu-id="48368-111">Stream-Output Object Types</span></span> | <span data-ttu-id="48368-112">Description</span><span class="sxs-lookup"><span data-stu-id="48368-112">Description</span></span>                       |
|----------------------------|-----------------------------------|
| <span data-ttu-id="48368-113">*PointStream*</span><span class="sxs-lookup"><span data-stu-id="48368-113">*PointStream*</span></span>              | <span data-ttu-id="48368-114">Séquence de primitives de point</span><span class="sxs-lookup"><span data-stu-id="48368-114">A sequence of point primitives</span></span>    |
| <span data-ttu-id="48368-115">*LineStream*</span><span class="sxs-lookup"><span data-stu-id="48368-115">*LineStream*</span></span>               | <span data-ttu-id="48368-116">Séquence de primitives de ligne</span><span class="sxs-lookup"><span data-stu-id="48368-116">A sequence of line primitives</span></span>     |
| <span data-ttu-id="48368-117">*TriangleStream*</span><span class="sxs-lookup"><span data-stu-id="48368-117">*TriangleStream*</span></span>           | <span data-ttu-id="48368-118">Une séquence de primitives de triangle</span><span class="sxs-lookup"><span data-stu-id="48368-118">A sequence of triangle primitives</span></span> |



 

<span data-ttu-id="48368-119">Type de données *DataType* -output ; peut être n’importe quel [type de données HLSL](dx-graphics-hlsl-data-types.md).</span><span class="sxs-lookup"><span data-stu-id="48368-119">*DataType* - Output data type; can be any [HLSL data type](dx-graphics-hlsl-data-types.md).</span></span> <span data-ttu-id="48368-120">Doit être entouré des crochets pointus.</span><span class="sxs-lookup"><span data-stu-id="48368-120">Must be surrounded by the angle brackets.</span></span>

<span data-ttu-id="48368-121">*Nom-nom* de la variable ; chaîne ASCII qui identifie l’objet de façon unique.</span><span class="sxs-lookup"><span data-stu-id="48368-121">*Name* - Variable name; an ASCII string that uniquely identifies the object.</span></span>

</dd> </dl>

## <a name="example"></a><span data-ttu-id="48368-122">Exemple</span><span class="sxs-lookup"><span data-stu-id="48368-122">Example</span></span>

<span data-ttu-id="48368-123">Il s’agit d’un exemple de déclaration d’objet de sortie de flux qui diffuse en continu des primitives de triangle dont les données sont définies par l' \_ carte cubique PS \_ dans la structure.</span><span class="sxs-lookup"><span data-stu-id="48368-123">This is an example of a stream-output object declaration that streams out triangle primitives whose data is defined by the PS\_CUBEMAP\_IN structure.</span></span> <span data-ttu-id="48368-124">Le nuanceur Geometry est limité à la génération de 18 vertex.</span><span class="sxs-lookup"><span data-stu-id="48368-124">The geometry-shader is limited to generating 18 vertices.</span></span>


```
struct PS_CUBEMAP_IN
{
    float4 Pos : SV_POSITION;     // Projection coord
    float2 Tex : TEXCOORD0;       // Texture coord
    uint RTIndex : SV_RenderTargetArrayIndex;
};

[maxvertexcount(18)]
void main( inout TriangleStream<PS_CUBEMAP_IN> CubeMapStream, triangle PS_CUBEMAP_INT[3] )
{
    ...
}
```



<span data-ttu-id="48368-125">Il s’agit d’un extrait de code de l' [exemple CubeMapGS](https://msdn.microsoft.com/library/Ee416398(v=VS.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="48368-125">This is a code snippet from the [CubeMapGS Sample](https://msdn.microsoft.com/library/Ee416398(v=VS.85).aspx).</span></span>

## <a name="stream-output-object-methods"></a><span data-ttu-id="48368-126">Méthodes d’objet Stream-Output</span><span class="sxs-lookup"><span data-stu-id="48368-126">Stream-Output Object Methods</span></span>

<span data-ttu-id="48368-127">Utilisez la syntaxe suivante pour appeler des méthodes d’objet de sortie de flux.</span><span class="sxs-lookup"><span data-stu-id="48368-127">Use the following syntax to call stream-output-object methods.</span></span>


```
Object.Method
```



<span data-ttu-id="48368-128">Les méthodes suivantes sont implémentées.</span><span class="sxs-lookup"><span data-stu-id="48368-128">The following methods are implemented.</span></span>



| <span data-ttu-id="48368-129">Méthodes</span><span class="sxs-lookup"><span data-stu-id="48368-129">Methods</span></span>                                              | <span data-ttu-id="48368-130">Description</span><span class="sxs-lookup"><span data-stu-id="48368-130">Description</span></span>                                                      |
|------------------------------------------------------|------------------------------------------------------------------|
| [<span data-ttu-id="48368-131">Append</span><span class="sxs-lookup"><span data-stu-id="48368-131">Append</span></span>](dx-graphics-hlsl-so-append.md)             | <span data-ttu-id="48368-132">Ajoute des données de sortie à un flux existant.</span><span class="sxs-lookup"><span data-stu-id="48368-132">Append output data to an existing stream.</span></span>                        |
| [<span data-ttu-id="48368-133">RestartStrip</span><span class="sxs-lookup"><span data-stu-id="48368-133">RestartStrip</span></span>](dx-graphics-hlsl-so-restartstrip.md) | <span data-ttu-id="48368-134">Mettez fin à la bande primitive actuelle et démarrez une nouvelle bande primitive.</span><span class="sxs-lookup"><span data-stu-id="48368-134">End the current primitive strip and start a new primitive strip.</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="48368-135">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="48368-135">Minimum Shader Model</span></span>

<span data-ttu-id="48368-136">Cet objet est pris en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="48368-136">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="48368-137">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="48368-137">Shader Model</span></span>                                                        | <span data-ttu-id="48368-138">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="48368-138">Supported</span></span> |
|---------------------------------------------------------------------|-----------|
| <span data-ttu-id="48368-139">[Nuancier modèle 4](dx-graphics-hlsl-sm4.md) et modèles de nuanceur supérieurs</span><span class="sxs-lookup"><span data-stu-id="48368-139">[Shader Model 4](dx-graphics-hlsl-sm4.md) and higher shader models</span></span> | <span data-ttu-id="48368-140">Oui</span><span class="sxs-lookup"><span data-stu-id="48368-140">yes</span></span>       |



 

## <a name="related-topics"></a><span data-ttu-id="48368-141">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="48368-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="48368-142">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="48368-142">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 