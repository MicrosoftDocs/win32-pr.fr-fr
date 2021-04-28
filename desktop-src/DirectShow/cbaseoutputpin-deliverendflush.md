---
description: 'Méthode CBaseOutputPin. DeliverEndFlush : la méthode DeliverEndFlush demande à la broche d’entrée connectée de terminer une opération de vidage.'
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
ms.openlocfilehash: 5f3fd5c1bc686ee5c0b4ff0cd1285a5114b93049
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096177"
---
# <a name="cbaseoutputpindeliverendflush-method"></a><span data-ttu-id="00d7c-103">Méthode CBaseOutputPin. DeliverEndFlush</span><span class="sxs-lookup"><span data-stu-id="00d7c-103">CBaseOutputPin.DeliverEndFlush method</span></span>

<span data-ttu-id="00d7c-104">La `DeliverEndFlush` méthode demande à la broche d’entrée connectée de terminer une opération de vidage.</span><span class="sxs-lookup"><span data-stu-id="00d7c-104">The `DeliverEndFlush` method requests the connected input pin to end a flush operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="00d7c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="00d7c-105">Syntax</span></span>


```C++
virtual HRESULT DeliverEndFlush();
```



## <a name="parameters"></a><span data-ttu-id="00d7c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="00d7c-106">Parameters</span></span>

<span data-ttu-id="00d7c-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="00d7c-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="00d7c-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="00d7c-108">Return value</span></span>

<span data-ttu-id="00d7c-109">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="00d7c-109">Returns an **HRESULT** value.</span></span> <span data-ttu-id="00d7c-110">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="00d7c-110">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="00d7c-111">Code de retour</span><span class="sxs-lookup"><span data-stu-id="00d7c-111">Return code</span></span>                                                                                           | <span data-ttu-id="00d7c-112">Description</span><span class="sxs-lookup"><span data-stu-id="00d7c-112">Description</span></span>                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="00d7c-113"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="00d7c-113"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="00d7c-114">Réussite.</span><span class="sxs-lookup"><span data-stu-id="00d7c-114">Success.</span></span><br/>              |
| <dl> <span data-ttu-id="00d7c-115"><dt>**VFW \_ E \_ non \_ connecté**</dt></span><span class="sxs-lookup"><span data-stu-id="00d7c-115"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="00d7c-116">Le pin n’est pas connecté.</span><span class="sxs-lookup"><span data-stu-id="00d7c-116">Pin is not connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="00d7c-117">Notes </span><span class="sxs-lookup"><span data-stu-id="00d7c-117">Remarks</span></span>

<span data-ttu-id="00d7c-118">Cette méthode appelle la méthode [**IPIN :: EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) sur la broche d’entrée.</span><span class="sxs-lookup"><span data-stu-id="00d7c-118">This method calls the [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) method on the input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="00d7c-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="00d7c-119">Requirements</span></span>



| <span data-ttu-id="00d7c-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="00d7c-120">Requirement</span></span> | <span data-ttu-id="00d7c-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="00d7c-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="00d7c-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="00d7c-122">Header</span></span><br/>  | <dl> <span data-ttu-id="00d7c-123"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="00d7c-123"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="00d7c-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="00d7c-124">Library</span></span><br/> | <dl> <span data-ttu-id="00d7c-125"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="00d7c-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="00d7c-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="00d7c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00d7c-127">**CBaseOutputPin, classe**</span><span class="sxs-lookup"><span data-stu-id="00d7c-127">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 




