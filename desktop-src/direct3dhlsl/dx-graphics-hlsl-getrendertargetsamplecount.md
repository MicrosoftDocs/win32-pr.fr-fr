---
title: GetRenderTargetSampleCount
description: Obtient le nombre d’échantillons pour une cible de rendu.
ms.assetid: e813134e-c58c-4845-b519-c1074993801e
keywords:
- HLSL GetRenderTargetSampleCount
topic_type:
- apiref
api_name:
- GetRenderTargetSampleCount
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 96c159a2ed63684b4bad2cbc6fa789c2dbd76edf
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104462586"
---
# <a name="getrendertargetsamplecount"></a><span data-ttu-id="c7d0f-104">GetRenderTargetSampleCount</span><span class="sxs-lookup"><span data-stu-id="c7d0f-104">GetRenderTargetSampleCount</span></span>

<span data-ttu-id="c7d0f-105">Obtient le nombre d’échantillons pour une cible de rendu.</span><span class="sxs-lookup"><span data-stu-id="c7d0f-105">Gets the number of samples for a render target.</span></span>



| <span data-ttu-id="c7d0f-106">*Uint* GetRenderTargetSampleCount()</span><span class="sxs-lookup"><span data-stu-id="c7d0f-106">*UINT* GetRenderTargetSampleCount()</span></span> |
|-------------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="c7d0f-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c7d0f-107">Parameters</span></span>



| <span data-ttu-id="c7d0f-108">Élément</span><span class="sxs-lookup"><span data-stu-id="c7d0f-108">Item</span></span>                                                                                 | <span data-ttu-id="c7d0f-109">Description</span><span class="sxs-lookup"><span data-stu-id="c7d0f-109">Description</span></span> |
|--------------------------------------------------------------------------------------|-------------|
| <span data-ttu-id="c7d0f-110"><span id="None"></span><span id="none"></span><span id="NONE"></span>None</span><span class="sxs-lookup"><span data-stu-id="c7d0f-110"><span id="None"></span><span id="none"></span><span id="NONE"></span>None</span></span><br/> |             |



 

## <a name="return-value"></a><span data-ttu-id="c7d0f-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="c7d0f-111">Return Value</span></span>

<span data-ttu-id="c7d0f-112">Nombre d’échantillons.</span><span class="sxs-lookup"><span data-stu-id="c7d0f-112">The number of samples.</span></span>

## <a name="remarks"></a><span data-ttu-id="c7d0f-113">Notes</span><span class="sxs-lookup"><span data-stu-id="c7d0f-113">Remarks</span></span>

<span data-ttu-id="c7d0f-114">Utilisez cette fonction et [**GetRenderTargetSamplePosition**](dx-graphics-hlsl-getrendertargetsampleposition.md) pour déterminer le nombre et la position des emplacements d’échantillonnage pour une cible de rendu.</span><span class="sxs-lookup"><span data-stu-id="c7d0f-114">Use this function and [**GetRenderTargetSamplePosition**](dx-graphics-hlsl-getrendertargetsampleposition.md) to find out the number and position of the sampling locations for a render target.</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="c7d0f-115">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="c7d0f-115">Minimum Shader Model</span></span>

<span data-ttu-id="c7d0f-116">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="c7d0f-116">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="c7d0f-117">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="c7d0f-117">Shader Model</span></span>                                                        | <span data-ttu-id="c7d0f-118">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="c7d0f-118">Supported</span></span> |
|---------------------------------------------------------------------|-----------|
| <span data-ttu-id="c7d0f-119">[Nuancier modèle 4](dx-graphics-hlsl-sm4.md) et modèles de nuanceur supérieurs</span><span class="sxs-lookup"><span data-stu-id="c7d0f-119">[Shader Model 4](dx-graphics-hlsl-sm4.md) and higher shader models</span></span> | <span data-ttu-id="c7d0f-120">Oui</span><span class="sxs-lookup"><span data-stu-id="c7d0f-120">yes</span></span>       |
| [<span data-ttu-id="c7d0f-121">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c7d0f-121">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md)           | <span data-ttu-id="c7d0f-122">non</span><span class="sxs-lookup"><span data-stu-id="c7d0f-122">no</span></span>        |
| [<span data-ttu-id="c7d0f-123">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c7d0f-123">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md)           | <span data-ttu-id="c7d0f-124">non</span><span class="sxs-lookup"><span data-stu-id="c7d0f-124">no</span></span>        |
| [<span data-ttu-id="c7d0f-125">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c7d0f-125">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)           | <span data-ttu-id="c7d0f-126">non</span><span class="sxs-lookup"><span data-stu-id="c7d0f-126">no</span></span>        |



 

## <a name="see-also"></a><span data-ttu-id="c7d0f-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c7d0f-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7d0f-128">**Fonctions intrinsèques (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="c7d0f-128">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

 





