---
description: 'La méthode EndFlush termine une opération de vidage. Implémente la méthode IPin :: EndFlush.'
ms.assetid: d4110eb4-26c5-4312-b33f-4af31e1bf2ae
title: Méthode CBaseInputPin. EndFlush (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.EndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 403ee5aa100309084090dc241724067f9dd3aa5c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545396"
---
# <a name="cbaseinputpinendflush-method"></a><span data-ttu-id="f0dea-104">Méthode CBaseInputPin. EndFlush</span><span class="sxs-lookup"><span data-stu-id="f0dea-104">CBaseInputPin.EndFlush method</span></span>

<span data-ttu-id="f0dea-105">La `EndFlush` méthode termine une opération de vidage.</span><span class="sxs-lookup"><span data-stu-id="f0dea-105">The `EndFlush` method ends a flush operation.</span></span> <span data-ttu-id="f0dea-106">Implémente la méthode [**IPIN :: EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) .</span><span class="sxs-lookup"><span data-stu-id="f0dea-106">Implements the [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0dea-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f0dea-107">Syntax</span></span>


```C++
HRESULT EndFlush();
```



## <a name="parameters"></a><span data-ttu-id="f0dea-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f0dea-108">Parameters</span></span>

<span data-ttu-id="f0dea-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="f0dea-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f0dea-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f0dea-110">Return value</span></span>

<span data-ttu-id="f0dea-111">Retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f0dea-111">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="f0dea-112">Notes</span><span class="sxs-lookup"><span data-stu-id="f0dea-112">Remarks</span></span>

<span data-ttu-id="f0dea-113">Cette méthode affecte à l’indicateur [**CBaseInputPin :: m \_ BFlushing**](cbaseinputpin-m-bflushing.md) la **valeur true**, ce qui permet à la méthode [**CBaseInputPin :: Receive**](cbaseinputpin-receive.md) d’accepter des exemples.</span><span class="sxs-lookup"><span data-stu-id="f0dea-113">This method sets the [**CBaseInputPin::m\_bFlushing**](cbaseinputpin-m-bflushing.md) flag to **TRUE**, which enables the [**CBaseInputPin::Receive**](cbaseinputpin-receive.md) method to accept samples.</span></span>

<span data-ttu-id="f0dea-114">La classe dérivée doit substituer cette méthode et effectuer les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="f0dea-114">The derived class must override this method and perform the following steps:</span></span>

1.  <span data-ttu-id="f0dea-115">Libérez toutes les données mises en mémoire tampon et attendez que tous les échantillons en file d’attente soient ignorés.</span><span class="sxs-lookup"><span data-stu-id="f0dea-115">Free any buffered data and wait for all queued samples to be discarded.</span></span>
2.  <span data-ttu-id="f0dea-116">Effacez toutes les notifications d' [**\_ achèvement EC**](ec-complete.md) en attente.</span><span class="sxs-lookup"><span data-stu-id="f0dea-116">Clear any pending [**EC\_COMPLETE**](ec-complete.md) notifications.</span></span>
3.  <span data-ttu-id="f0dea-117">Appelez la méthode de la classe de base.</span><span class="sxs-lookup"><span data-stu-id="f0dea-117">Call the base class method.</span></span>
4.  <span data-ttu-id="f0dea-118">Appelez [**IPIN :: EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) sur les broches d’entrée en aval.</span><span class="sxs-lookup"><span data-stu-id="f0dea-118">Call [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) on downstream input pins.</span></span> <span data-ttu-id="f0dea-119">Si le pin n’a pas encore remis d’exemples de supports en aval, vous pouvez ignorer cette étape.</span><span class="sxs-lookup"><span data-stu-id="f0dea-119">If the pin has not yet delivered any media samples downstream, you can skip this step.</span></span> <span data-ttu-id="f0dea-120">Si vos broches de sortie dérivent de la classe [**CBaseOutputPin**](cbaseoutputpin.md) , vous pouvez appeler la méthode [**CBaseOutputPin ::D eliverendflush**](cbaseoutputpin-deliverendflush.md) .</span><span class="sxs-lookup"><span data-stu-id="f0dea-120">If your output pins derive from the [**CBaseOutputPin**](cbaseoutputpin.md) class, you can call the [**CBaseOutputPin::DeliverEndFlush**](cbaseoutputpin-deliverendflush.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="f0dea-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f0dea-121">Requirements</span></span>



| <span data-ttu-id="f0dea-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f0dea-122">Requirement</span></span> | <span data-ttu-id="f0dea-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="f0dea-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0dea-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="f0dea-124">Header</span></span><br/>  | <dl> <span data-ttu-id="f0dea-125"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f0dea-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="f0dea-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f0dea-126">Library</span></span><br/> | <dl> <span data-ttu-id="f0dea-127"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="f0dea-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f0dea-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f0dea-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0dea-129">**CBaseInputPin, classe**</span><span class="sxs-lookup"><span data-stu-id="f0dea-129">**CBaseInputPin Class**</span></span>](cbaseinputpin.md)
</dt> </dl>

 

 




