---
title: Append (objet Stream-Output HLSL DirectX)
description: Ajoutez Geometry-Shader-output Data à un flux existant.
ms.assetid: 7df51383-7fc7-4a6f-aaa2-6c929f0443a3
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 19d767f3c501cc42e21bbc44a196ba08cd6f1883
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120184"
---
# <a name="append-directx-hlsl-stream-output-object"></a><span data-ttu-id="f258e-103">Append (objet Stream-Output HLSL DirectX)</span><span class="sxs-lookup"><span data-stu-id="f258e-103">Append (DirectX HLSL Stream-Output Object)</span></span>

<span data-ttu-id="f258e-104">Ajoutez Geometry-Shader-output Data à un flux existant.</span><span class="sxs-lookup"><span data-stu-id="f258e-104">Append geometry-shader-output data to an existing stream.</span></span>

<span data-ttu-id="f258e-105">Append ( *StreamDataType*);</span><span class="sxs-lookup"><span data-stu-id="f258e-105">Append( *StreamDataType*);</span></span>



 

## <a name="parameters"></a><span data-ttu-id="f258e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f258e-106">Parameters</span></span>



| <span data-ttu-id="f258e-107">Élément</span><span class="sxs-lookup"><span data-stu-id="f258e-107">Item</span></span>                                                                                                                             | <span data-ttu-id="f258e-108">Description</span><span class="sxs-lookup"><span data-stu-id="f258e-108">Description</span></span>                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f258e-109"><span id="StreamDataType"></span><span id="streamdatatype"></span><span id="STREAMDATATYPE"></span>**StreamDataType**</span><span class="sxs-lookup"><span data-stu-id="f258e-109"><span id="StreamDataType"></span><span id="streamdatatype"></span><span id="STREAMDATATYPE"></span>**StreamDataType**</span></span><br/> | <span data-ttu-id="f258e-110">Description de l’entrée de données.</span><span class="sxs-lookup"><span data-stu-id="f258e-110">A data input description.</span></span> <span data-ttu-id="f258e-111">Cette description doit correspondre au paramètre de modèle Stream-Object appelé [DataType](dx-graphics-hlsl-so-type.md).</span><span class="sxs-lookup"><span data-stu-id="f258e-111">This description must match the stream-object template parameter called [DataType](dx-graphics-hlsl-so-type.md).</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="f258e-112">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="f258e-112">Return Value</span></span>

<span data-ttu-id="f258e-113">None</span><span class="sxs-lookup"><span data-stu-id="f258e-113">None</span></span>

## <a name="example"></a><span data-ttu-id="f258e-114">Exemple</span><span class="sxs-lookup"><span data-stu-id="f258e-114">Example</span></span>

<span data-ttu-id="f258e-115">Cet extrait de code (à partir de l' [exemple CubeMapGS](https://msdn.microsoft.com/library/Ee416398(v=VS.85).aspx)) illustre un exemple partiel d’ajout de primitives de bandes de triangles à un objet de sortie de flux.</span><span class="sxs-lookup"><span data-stu-id="f258e-115">This code snippet (from the [CubeMapGS Sample](https://msdn.microsoft.com/library/Ee416398(v=VS.85).aspx)) shows a partial example of appending triangle strip primitives to a stream-output object.</span></span>


```
[maxvertexcount(18)]
void GS_CubeMap( triangle GS_CUBEMAP_IN input[3], 
                 inout TriangleStream<PS_CUBEMAP_IN> CubeMapStream )
{
    for( int f = 0; f < 6; ++f )
    {
        // Compute screen coordinates
        PS_CUBEMAP_IN output;
        output.RTIndex = f;
        for( int v = 0; v < 3; v++ )
        {
            output.Pos = mul( input[v].Pos, g_mViewCM[f] );
            output.Pos = mul( output.Pos, mProj );
            output.Tex = input[v].Tex;
            CubeMapStream.Append( output );
        }
        CubeMapStream.RestartStrip();
    }
}
```



## <a name="minimum-shader-model"></a><span data-ttu-id="f258e-116">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="f258e-116">Minimum Shader Model</span></span>

<span data-ttu-id="f258e-117">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="f258e-117">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="f258e-118">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="f258e-118">Shader Model</span></span>                                              | <span data-ttu-id="f258e-119">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="f258e-119">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="f258e-120">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="f258e-120">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="f258e-121">yes</span><span class="sxs-lookup"><span data-stu-id="f258e-121">yes</span></span>       |
| [<span data-ttu-id="f258e-122">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f258e-122">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="f258e-123">Non</span><span class="sxs-lookup"><span data-stu-id="f258e-123">no</span></span>        |
| [<span data-ttu-id="f258e-124">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f258e-124">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="f258e-125">Non</span><span class="sxs-lookup"><span data-stu-id="f258e-125">no</span></span>        |
| [<span data-ttu-id="f258e-126">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f258e-126">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="f258e-127">Non</span><span class="sxs-lookup"><span data-stu-id="f258e-127">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="f258e-128">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f258e-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f258e-129">Stream-sortie (objet)</span><span class="sxs-lookup"><span data-stu-id="f258e-129">Stream-Output Object</span></span>](dx-graphics-hlsl-so-type.md)
</dt> </dl>

 

 





