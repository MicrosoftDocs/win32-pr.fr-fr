---
description: La méthode SendQuality envoie un message de qualité pour indiquer ce que le fournisseur doit faire sur la qualité.
ms.assetid: 9ce11c35-958c-4eda-9130-1139c4074bf7
title: Méthode CBaseVideoRenderer. SendQuality (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.SendQuality
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8a6ae7228be0f3012c49d652d11bf2c1c3bfc181
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523902"
---
# <a name="cbasevideorenderersendquality-method"></a><span data-ttu-id="a2c24-103">Méthode CBaseVideoRenderer. SendQuality</span><span class="sxs-lookup"><span data-stu-id="a2c24-103">CBaseVideoRenderer.SendQuality method</span></span>

<span data-ttu-id="a2c24-104">La `SendQuality` méthode envoie un message de qualité pour indiquer ce que le fournisseur doit faire sur la qualité.</span><span class="sxs-lookup"><span data-stu-id="a2c24-104">The `SendQuality` method sends a quality message to indicate what the supplier should do about quality.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2c24-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a2c24-105">Syntax</span></span>


```C++
virtual HRESULT SendQuality(
   REFERENCE_TIME trLate,
   REFERENCE_TIME trRealStream
);
```



## <a name="parameters"></a><span data-ttu-id="a2c24-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a2c24-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a2c24-107">*trLate*</span><span class="sxs-lookup"><span data-stu-id="a2c24-107">*trLate*</span></span> 
</dt> <dd>

<span data-ttu-id="a2c24-108">Durée pendant laquelle le cadre est en retard.</span><span class="sxs-lookup"><span data-stu-id="a2c24-108">Amount of time by which the frame is late.</span></span>

</dd> <dt>

<span data-ttu-id="a2c24-109">*trRealStream*</span><span class="sxs-lookup"><span data-stu-id="a2c24-109">*trRealStream*</span></span> 
</dt> <dd>

<span data-ttu-id="a2c24-110">Currentstream.</span><span class="sxs-lookup"><span data-stu-id="a2c24-110">Currentstream time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a2c24-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a2c24-111">Return value</span></span>

<span data-ttu-id="a2c24-112">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a2c24-112">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a2c24-113">Notes</span><span class="sxs-lookup"><span data-stu-id="a2c24-113">Remarks</span></span>

<span data-ttu-id="a2c24-114">Cette fonction membre envoie un message de contrôle qualité en amont pour contrôler la gestion de la qualité.</span><span class="sxs-lookup"><span data-stu-id="a2c24-114">This member function sends a quality control message upstream to control quality management.</span></span> <span data-ttu-id="a2c24-115">La nature du message de qualité (c’est-à-dire si vous souhaitez réduire ou augmenter le nombre d’échantillons) est déterminée dans l’implémentation de la gestion de la qualité dans cette classe dérivée (voir [**CBaseVideoRenderer :: ShouldDrawSampleNow**](cbasevideorenderer-shoulddrawsamplenow.md)).</span><span class="sxs-lookup"><span data-stu-id="a2c24-115">The nature of the quality message (that is, whether to reduce or increase the number of samples) is determined in the quality management implementation in this derived class (see [**CBaseVideoRenderer::ShouldDrawSampleNow**](cbasevideorenderer-shoulddrawsamplenow.md)).</span></span>

## <a name="requirements"></a><span data-ttu-id="a2c24-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a2c24-116">Requirements</span></span>



| <span data-ttu-id="a2c24-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a2c24-117">Requirement</span></span> | <span data-ttu-id="a2c24-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="a2c24-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2c24-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="a2c24-119">Header</span></span><br/>  | <dl> <span data-ttu-id="a2c24-120"><dt>Renbase. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a2c24-120"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="a2c24-121">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="a2c24-121">Library</span></span><br/> | <dl> <span data-ttu-id="a2c24-122"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="a2c24-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a2c24-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a2c24-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2c24-124">**CBaseVideoRenderer, classe**</span><span class="sxs-lookup"><span data-stu-id="a2c24-124">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




