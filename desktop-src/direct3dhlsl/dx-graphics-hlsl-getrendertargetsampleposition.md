---
title: GetRenderTargetSamplePosition
description: Obtient la position d’échantillonnage (x, y) pour un exemple d’index donné.
ms.assetid: 07f14d1c-4fe5-4838-acce-d664cdc641e6
keywords:
- HLSL GetRenderTargetSamplePosition
topic_type:
- apiref
api_name:
- GetRenderTargetSamplePosition
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c31bc829f8990517ddbea8be7c25eead413ab666
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120574"
---
# <a name="getrendertargetsampleposition"></a><span data-ttu-id="0da1a-104">GetRenderTargetSamplePosition</span><span class="sxs-lookup"><span data-stu-id="0da1a-104">GetRenderTargetSamplePosition</span></span>

<span data-ttu-id="0da1a-105">Obtient la position d’échantillonnage (x, y) pour un exemple d’index donné.</span><span class="sxs-lookup"><span data-stu-id="0da1a-105">Gets the sampling position (x,y) for a given sample index.</span></span>

<span data-ttu-id="0da1a-106">float<2> GetRenderTargetSamplePosition (dans int<1> index</span><span class="sxs-lookup"><span data-stu-id="0da1a-106">float<2> GetRenderTargetSamplePosition( in int<1> Index</span></span><br/><span data-ttu-id="0da1a-107">);</span><span class="sxs-lookup"><span data-stu-id="0da1a-107">);</span></span>



 

## <a name="parameters"></a><span data-ttu-id="0da1a-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0da1a-108">Parameters</span></span>



| <span data-ttu-id="0da1a-109">Élément</span><span class="sxs-lookup"><span data-stu-id="0da1a-109">Item</span></span>                                                                                       | <span data-ttu-id="0da1a-110">Description</span><span class="sxs-lookup"><span data-stu-id="0da1a-110">Description</span></span>                                  |
|--------------------------------------------------------------------------------------------|----------------------------------------------|
| <span data-ttu-id="0da1a-111"><span id="Index"></span><span id="index"></span><span id="INDEX"></span>*Évaluer*</span><span class="sxs-lookup"><span data-stu-id="0da1a-111"><span id="Index"></span><span id="index"></span><span id="INDEX"></span>*Index*</span></span><br/> | <span data-ttu-id="0da1a-112">\[dans \] un exemple d’index de base zéro.</span><span class="sxs-lookup"><span data-stu-id="0da1a-112">\[in\] A zero-based sample index.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="0da1a-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="0da1a-113">Return Value</span></span>

<span data-ttu-id="0da1a-114">Position (x, y) de l’échantillon donné.</span><span class="sxs-lookup"><span data-stu-id="0da1a-114">The (x,y) position of the given sample.</span></span>

## <a name="remarks"></a><span data-ttu-id="0da1a-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="0da1a-115">Remarks</span></span>

<span data-ttu-id="0da1a-116">Utilisez cette fonction et [**GetRenderTargetSampleCount**](dx-graphics-hlsl-getrendertargetsamplecount.md) pour déterminer le nombre et la position des emplacements d’échantillonnage pour une cible de rendu.</span><span class="sxs-lookup"><span data-stu-id="0da1a-116">Use this function and [**GetRenderTargetSampleCount**](dx-graphics-hlsl-getrendertargetsamplecount.md) to find out the number and position of the sampling locations for a render target.</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="0da1a-117">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="0da1a-117">Minimum Shader Model</span></span>

<span data-ttu-id="0da1a-118">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="0da1a-118">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="0da1a-119">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="0da1a-119">Shader Model</span></span>                                                        | <span data-ttu-id="0da1a-120">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="0da1a-120">Supported</span></span> |
|---------------------------------------------------------------------|-----------|
| <span data-ttu-id="0da1a-121">[Nuancier modèle 4](dx-graphics-hlsl-sm4.md) et modèles de nuanceur supérieurs</span><span class="sxs-lookup"><span data-stu-id="0da1a-121">[Shader Model 4](dx-graphics-hlsl-sm4.md) and higher shader models</span></span> | <span data-ttu-id="0da1a-122">yes</span><span class="sxs-lookup"><span data-stu-id="0da1a-122">yes</span></span>       |
| [<span data-ttu-id="0da1a-123">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0da1a-123">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md)           | <span data-ttu-id="0da1a-124">Non</span><span class="sxs-lookup"><span data-stu-id="0da1a-124">no</span></span>        |
| [<span data-ttu-id="0da1a-125">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0da1a-125">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md)           | <span data-ttu-id="0da1a-126">Non</span><span class="sxs-lookup"><span data-stu-id="0da1a-126">no</span></span>        |
| [<span data-ttu-id="0da1a-127">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0da1a-127">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)           | <span data-ttu-id="0da1a-128">Non</span><span class="sxs-lookup"><span data-stu-id="0da1a-128">no</span></span>        |



 

## <a name="see-also"></a><span data-ttu-id="0da1a-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0da1a-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0da1a-130">**Fonctions intrinsèques (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="0da1a-130">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

 





