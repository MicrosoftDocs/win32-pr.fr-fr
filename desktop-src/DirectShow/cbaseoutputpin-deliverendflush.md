---
description: La méthode DeliverEndFlush demande à la broche d’entrée connectée de terminer une opération de vidage.
ms.assetid: 9f1fd76c-dba7-41c5-b098-9735e4f2571b
title: Méthode CBaseOutputPin. DeliverEndFlush (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.DeliverEndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cb9b92947f2452b8755109c4b83cb21afa119461
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528977"
---
# <a name="cbaseoutputpindeliverendflush-method"></a><span data-ttu-id="0cc17-103">Méthode CBaseOutputPin. DeliverEndFlush</span><span class="sxs-lookup"><span data-stu-id="0cc17-103">CBaseOutputPin.DeliverEndFlush method</span></span>

<span data-ttu-id="0cc17-104">La `DeliverEndFlush` méthode demande à la broche d’entrée connectée de terminer une opération de vidage.</span><span class="sxs-lookup"><span data-stu-id="0cc17-104">The `DeliverEndFlush` method requests the connected input pin to end a flush operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="0cc17-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0cc17-105">Syntax</span></span>


```C++
virtual HRESULT DeliverEndFlush();
```



## <a name="parameters"></a><span data-ttu-id="0cc17-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0cc17-106">Parameters</span></span>

<span data-ttu-id="0cc17-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="0cc17-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0cc17-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0cc17-108">Return value</span></span>

<span data-ttu-id="0cc17-109">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0cc17-109">Returns an **HRESULT** value.</span></span> <span data-ttu-id="0cc17-110">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="0cc17-110">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="0cc17-111">Code de retour</span><span class="sxs-lookup"><span data-stu-id="0cc17-111">Return code</span></span>                                                                                           | <span data-ttu-id="0cc17-112">Description</span><span class="sxs-lookup"><span data-stu-id="0cc17-112">Description</span></span>                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="0cc17-113"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="0cc17-113"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="0cc17-114">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="0cc17-114">Success.</span></span><br/>              |
| <dl> <span data-ttu-id="0cc17-115"><dt>**VFW \_ E \_ non \_ connecté**</dt></span><span class="sxs-lookup"><span data-stu-id="0cc17-115"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="0cc17-116">Le pin n’est pas connecté.</span><span class="sxs-lookup"><span data-stu-id="0cc17-116">Pin is not connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="0cc17-117">Notes</span><span class="sxs-lookup"><span data-stu-id="0cc17-117">Remarks</span></span>

<span data-ttu-id="0cc17-118">Cette méthode appelle la méthode [**IPIN :: EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) sur la broche d’entrée.</span><span class="sxs-lookup"><span data-stu-id="0cc17-118">This method calls the [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) method on the input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="0cc17-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0cc17-119">Requirements</span></span>



| <span data-ttu-id="0cc17-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0cc17-120">Requirement</span></span> | <span data-ttu-id="0cc17-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="0cc17-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0cc17-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="0cc17-122">Header</span></span><br/>  | <dl> <span data-ttu-id="0cc17-123"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0cc17-123"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="0cc17-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="0cc17-124">Library</span></span><br/> | <dl> <span data-ttu-id="0cc17-125"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="0cc17-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0cc17-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0cc17-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0cc17-127">**CBaseOutputPin, classe**</span><span class="sxs-lookup"><span data-stu-id="0cc17-127">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 




