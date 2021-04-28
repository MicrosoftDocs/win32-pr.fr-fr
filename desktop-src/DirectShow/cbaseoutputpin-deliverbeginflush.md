---
description: 'Méthode CBaseOutputPin. DeliverBeginFlush : la méthode DeliverBeginFlush demande à la broche d’entrée connectée de commencer une opération de vidage.'
ms.assetid: 0d7c7bd7-2a7a-42a4-a0de-60205b62e49c
title: Méthode CBaseOutputPin. DeliverBeginFlush (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.DeliverBeginFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 22dbd2bccf33d9f203d1505106184500b8cae3ba
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099517"
---
# <a name="cbaseoutputpindeliverbeginflush-method"></a><span data-ttu-id="88511-103">Méthode CBaseOutputPin. DeliverBeginFlush</span><span class="sxs-lookup"><span data-stu-id="88511-103">CBaseOutputPin.DeliverBeginFlush method</span></span>

<span data-ttu-id="88511-104">La `DeliverBeginFlush` méthode demande à la broche d’entrée connectée de commencer une opération de vidage.</span><span class="sxs-lookup"><span data-stu-id="88511-104">The `DeliverBeginFlush` method requests the connected input pin to begin a flush operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="88511-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="88511-105">Syntax</span></span>


```C++
virtual HRESULT DeliverBeginFlush();
```



## <a name="parameters"></a><span data-ttu-id="88511-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="88511-106">Parameters</span></span>

<span data-ttu-id="88511-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="88511-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="88511-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="88511-108">Return value</span></span>

<span data-ttu-id="88511-109">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="88511-109">Returns an **HRESULT** value.</span></span> <span data-ttu-id="88511-110">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="88511-110">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="88511-111">Code de retour</span><span class="sxs-lookup"><span data-stu-id="88511-111">Return code</span></span>                                                                                           | <span data-ttu-id="88511-112">Description</span><span class="sxs-lookup"><span data-stu-id="88511-112">Description</span></span>                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="88511-113"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="88511-113"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="88511-114">Réussite.</span><span class="sxs-lookup"><span data-stu-id="88511-114">Success.</span></span><br/>              |
| <dl> <span data-ttu-id="88511-115"><dt>**VFW \_ E \_ non \_ connecté**</dt></span><span class="sxs-lookup"><span data-stu-id="88511-115"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="88511-116">Le pin n’est pas connecté.</span><span class="sxs-lookup"><span data-stu-id="88511-116">Pin is not connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="88511-117">Notes </span><span class="sxs-lookup"><span data-stu-id="88511-117">Remarks</span></span>

<span data-ttu-id="88511-118">Cette méthode appelle la méthode [**IPIN :: BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) sur la broche d’entrée.</span><span class="sxs-lookup"><span data-stu-id="88511-118">This method calls the [**IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) method on the input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="88511-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="88511-119">Requirements</span></span>



| <span data-ttu-id="88511-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="88511-120">Requirement</span></span> | <span data-ttu-id="88511-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="88511-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88511-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="88511-122">Header</span></span><br/>  | <dl> <span data-ttu-id="88511-123"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="88511-123"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="88511-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="88511-124">Library</span></span><br/> | <dl> <span data-ttu-id="88511-125"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="88511-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="88511-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="88511-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88511-127">**CBaseOutputPin, classe**</span><span class="sxs-lookup"><span data-stu-id="88511-127">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 




