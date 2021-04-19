---
description: La méthode OnStopStreaming est appelée lorsque le filtre arrête la diffusion en continu.
ms.assetid: d882fec8-09e1-4d36-a09c-44568e743da3
title: Méthode CBaseRenderer. OnStopStreaming (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.OnStopStreaming
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 417a18ca53240dce0e4ed6d40f551c45c24b0f1c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537124"
---
# <a name="cbaserendereronstopstreaming-method"></a><span data-ttu-id="91ca9-103">Méthode CBaseRenderer. OnStopStreaming</span><span class="sxs-lookup"><span data-stu-id="91ca9-103">CBaseRenderer.OnStopStreaming method</span></span>

<span data-ttu-id="91ca9-104">La `OnStopStreaming` méthode est appelée lorsque le filtre arrête la diffusion en continu.</span><span class="sxs-lookup"><span data-stu-id="91ca9-104">The `OnStopStreaming` method is called when the filter stops streaming.</span></span>

## <a name="syntax"></a><span data-ttu-id="91ca9-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="91ca9-105">Syntax</span></span>


```C++
virtual HRESULT OnStopStreaming();
```



## <a name="parameters"></a><span data-ttu-id="91ca9-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="91ca9-106">Parameters</span></span>

<span data-ttu-id="91ca9-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="91ca9-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="91ca9-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="91ca9-108">Return value</span></span>

<span data-ttu-id="91ca9-109">Retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="91ca9-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="91ca9-110">Notes</span><span class="sxs-lookup"><span data-stu-id="91ca9-110">Remarks</span></span>

<span data-ttu-id="91ca9-111">La méthode [**CBaseRenderer :: StopStreaming**](cbaserenderer-stopstreaming.md) appelle cette méthode.</span><span class="sxs-lookup"><span data-stu-id="91ca9-111">The [**CBaseRenderer::StopStreaming**](cbaserenderer-stopstreaming.md) method calls this method.</span></span> <span data-ttu-id="91ca9-112">Elle ne fait rien dans la classe de base, mais la classe dérivée peut la substituer.</span><span class="sxs-lookup"><span data-stu-id="91ca9-112">It does nothing in the base class, but the derived class can override it.</span></span>

## <a name="requirements"></a><span data-ttu-id="91ca9-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="91ca9-113">Requirements</span></span>



| <span data-ttu-id="91ca9-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="91ca9-114">Requirement</span></span> | <span data-ttu-id="91ca9-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="91ca9-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="91ca9-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="91ca9-116">Header</span></span><br/>  | <dl> <span data-ttu-id="91ca9-117"><dt>Renbase. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="91ca9-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="91ca9-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="91ca9-118">Library</span></span><br/> | <dl> <span data-ttu-id="91ca9-119"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="91ca9-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="91ca9-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="91ca9-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91ca9-121">**CBaseRenderer, classe**</span><span class="sxs-lookup"><span data-stu-id="91ca9-121">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




