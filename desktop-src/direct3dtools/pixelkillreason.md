---
description: Énumération utilisée pour indiquer la raison pour laquelle un pixel a été rejeté.
MS-HAID: vspixengine.PIXELKILLREASON
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Énumération PIXELKILLREASON
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 43836288-554B-430C-861D-AAC58DE3B282
api_name:
- PIXELKILLREASON
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: f87b072eec1ac98ca68171593765567f5e77e70e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104317705"
---
# <a name="span-idvspixenginepixelkillreasonspanpixelkillreason-enumeration"></a><span data-ttu-id="2915a-103"><span id="vspixengine.pixelkillreason"></span>Énumération PIXELKILLREASON</span><span class="sxs-lookup"><span data-stu-id="2915a-103"><span id="vspixengine.pixelkillreason"></span>PIXELKILLREASON enumeration</span></span>

<span data-ttu-id="2915a-104">Énumération utilisée pour indiquer la raison pour laquelle un pixel a été rejeté.</span><span class="sxs-lookup"><span data-stu-id="2915a-104">An enum used to indicate why a pixel was rejected.</span></span>

## <a name="syntax"></a><span data-ttu-id="2915a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2915a-105">Syntax</span></span>


```C++
};
```

## <a name="constants"></a><span data-ttu-id="2915a-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="2915a-106">Constants</span></span>

<span data-ttu-id="2915a-107"><span id="PKR_NONE"></span><span id="pkr_none"></span>**PKR \_ aucun**</span><span class="sxs-lookup"><span data-stu-id="2915a-107"><span id="PKR_NONE"></span><span id="pkr_none"></span>**PKR\_NONE**</span></span>  
<span data-ttu-id="2915a-108">Valeur qui indique que le pixel n’a pas été rejeté.</span><span class="sxs-lookup"><span data-stu-id="2915a-108">A value that indicates that the pixel was not rejected.</span></span>

<span data-ttu-id="2915a-109"><span id="PKR_SHADERKILL"></span><span id="pkr_shaderkill"></span>**PKR \_ SHADERKILL**</span><span class="sxs-lookup"><span data-stu-id="2915a-109"><span id="PKR_SHADERKILL"></span><span id="pkr_shaderkill"></span>**PKR\_SHADERKILL**</span></span>  
<span data-ttu-id="2915a-110">Valeur qui indique que le pixel a été rejeté car le nuanceur n’a pas été exécuté.</span><span class="sxs-lookup"><span data-stu-id="2915a-110">A value that indicates that the pixel was rejected because the shader didn't run.</span></span>

<span data-ttu-id="2915a-111"><span id="PKR_SCISSORTEST"></span><span id="pkr_scissortest"></span>**PKR \_ SCISSORTEST**</span><span class="sxs-lookup"><span data-stu-id="2915a-111"><span id="PKR_SCISSORTEST"></span><span id="pkr_scissortest"></span>**PKR\_SCISSORTEST**</span></span>  
<span data-ttu-id="2915a-112">Valeur qui indique que le pixel a été rejeté en raison de l’échec du test de la ciseaux.</span><span class="sxs-lookup"><span data-stu-id="2915a-112">A value that indicates that the pixel was rejected because the scissor test failed.</span></span>

<span data-ttu-id="2915a-113"><span id="PKR_ALPHATEST"></span><span id="pkr_alphatest"></span>**PKR \_ ALPHATEST**</span><span class="sxs-lookup"><span data-stu-id="2915a-113"><span id="PKR_ALPHATEST"></span><span id="pkr_alphatest"></span>**PKR\_ALPHATEST**</span></span>  
<span data-ttu-id="2915a-114">Valeur qui indique que le pixel a été rejeté en raison de l’échec du test alpha.</span><span class="sxs-lookup"><span data-stu-id="2915a-114">A value that indicates that the pixel was rejected because the alpha test failed.</span></span>

<span data-ttu-id="2915a-115"><span id="PKR_STENCILTEST"></span><span id="pkr_stenciltest"></span>**PKR \_ STENCILTEST**</span><span class="sxs-lookup"><span data-stu-id="2915a-115"><span id="PKR_STENCILTEST"></span><span id="pkr_stenciltest"></span>**PKR\_STENCILTEST**</span></span>  
<span data-ttu-id="2915a-116">Valeur qui indique que le pixel a été rejeté en raison de l’échec du test du stencil.</span><span class="sxs-lookup"><span data-stu-id="2915a-116">A value that indicates that the pixel was rejected because the stencil test failed.</span></span>

<span data-ttu-id="2915a-117"><span id="PKR_DEPTHTEST"></span><span id="pkr_depthtest"></span>**PKR \_ DEPTHTEST**</span><span class="sxs-lookup"><span data-stu-id="2915a-117"><span id="PKR_DEPTHTEST"></span><span id="pkr_depthtest"></span>**PKR\_DEPTHTEST**</span></span>  
<span data-ttu-id="2915a-118">Valeur qui indique que le pixel a été rejeté en raison de l’échec du test de profondeur.</span><span class="sxs-lookup"><span data-stu-id="2915a-118">A value that indicates that the pixel was rejected because the depth test failed.</span></span>

<span data-ttu-id="2915a-119"><span id="PKR_NOTCOMPUTABLE"></span><span id="pkr_notcomputable"></span>**PKR \_ NOTCOMPUTABLE**</span><span class="sxs-lookup"><span data-stu-id="2915a-119"><span id="PKR_NOTCOMPUTABLE"></span><span id="pkr_notcomputable"></span>**PKR\_NOTCOMPUTABLE**</span></span>  
<span data-ttu-id="2915a-120">Valeur qui indique que l’historique des pixels ne peut pas être calculé.</span><span class="sxs-lookup"><span data-stu-id="2915a-120">A value that indicates that the pixel history can't be computed.</span></span>

<span data-ttu-id="2915a-121"><span id="PKR_ERROR"></span><span id="pkr_error"></span>**\_erreur PKR**</span><span class="sxs-lookup"><span data-stu-id="2915a-121"><span id="PKR_ERROR"></span><span id="pkr_error"></span>**PKR\_ERROR**</span></span>  
<span data-ttu-id="2915a-122">Valeur qui indique que le pixel a été rejeté en raison d’une erreur générale.</span><span class="sxs-lookup"><span data-stu-id="2915a-122">A value that indicates that the pixel was rejected because of a general error.</span></span>

<span data-ttu-id="2915a-123"><span id="PKR_NOINTERSECTION"></span><span id="pkr_nointersection"></span>**nointersection PKR \_**</span><span class="sxs-lookup"><span data-stu-id="2915a-123"><span id="PKR_NOINTERSECTION"></span><span id="pkr_nointersection"></span>**PKR\_NOINTERSECTION**</span></span>  
<span data-ttu-id="2915a-124">Valeur qui indique que le pixel a été rejeté parce que l’appel de dessin ne croise pas le pixel.</span><span class="sxs-lookup"><span data-stu-id="2915a-124">A value that indicates that the pixel was rejected because the draw call does not intersect the pixel.</span></span>

<span data-ttu-id="2915a-125"><span id="PKR_OCCLUDED"></span><span id="pkr_occluded"></span>**PKR \_ bloqués**</span><span class="sxs-lookup"><span data-stu-id="2915a-125"><span id="PKR_OCCLUDED"></span><span id="pkr_occluded"></span>**PKR\_OCCLUDED**</span></span>  
<span data-ttu-id="2915a-126">Valeur qui indique que le pixel a été rejeté car le dessin était bloqués.</span><span class="sxs-lookup"><span data-stu-id="2915a-126">A value that indicates that the pixel was rejected because the draw was occluded.</span></span>

<span data-ttu-id="2915a-127"><span id="PKR_DEPTHSTENCILTEST"></span><span id="pkr_depthstenciltest"></span>**PKR \_ DEPTHSTENCILTEST**</span><span class="sxs-lookup"><span data-stu-id="2915a-127"><span id="PKR_DEPTHSTENCILTEST"></span><span id="pkr_depthstenciltest"></span>**PKR\_DEPTHSTENCILTEST**</span></span>  
<span data-ttu-id="2915a-128">Valeur qui indique que le pixel a été rejeté en raison de l’échec du test de profondeur et du stencil.</span><span class="sxs-lookup"><span data-stu-id="2915a-128">A value that indicates that the pixel was rejected because the depth and stencil test failed.</span></span>

## <a name="requirements"></a><span data-ttu-id="2915a-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2915a-129">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="2915a-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="2915a-130">Header</span></span></p></td><td><span data-ttu-id="2915a-131">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="2915a-131">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



