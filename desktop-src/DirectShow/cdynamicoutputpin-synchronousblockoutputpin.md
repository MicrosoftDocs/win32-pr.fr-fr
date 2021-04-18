---
description: La méthode SynchronousBlockOutputPin bloque le code confidentiel. n’est pas retourné tant que le code confidentiel n’est pas bloqué.
ms.assetid: 10fdb788-bc72-4eda-b60b-af83f954d689
title: Méthode CDynamicOutputPin. SynchronousBlockOutputPin (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.SynchronousBlockOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7fff1a0a1f093b97d07c74d7916ef2a7511d0e16
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533238"
---
# <a name="cdynamicoutputpinsynchronousblockoutputpin-method"></a><span data-ttu-id="6cb00-103">Méthode CDynamicOutputPin. SynchronousBlockOutputPin</span><span class="sxs-lookup"><span data-stu-id="6cb00-103">CDynamicOutputPin.SynchronousBlockOutputPin method</span></span>

<span data-ttu-id="6cb00-104">La `SynchronousBlockOutputPin` méthode bloque le code confidentiel ; ne retourne pas tant que le code confidentiel n’est pas bloqué.</span><span class="sxs-lookup"><span data-stu-id="6cb00-104">The `SynchronousBlockOutputPin` method blocks the pin; does not return until the pin is blocked.</span></span>

## <a name="syntax"></a><span data-ttu-id="6cb00-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6cb00-105">Syntax</span></span>


```C++
HRESULT SynchronousBlockOutputPin();
```



## <a name="parameters"></a><span data-ttu-id="6cb00-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6cb00-106">Parameters</span></span>

<span data-ttu-id="6cb00-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="6cb00-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6cb00-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6cb00-108">Return value</span></span>

<span data-ttu-id="6cb00-109">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6cb00-109">Returns an **HRESULT** value.</span></span> <span data-ttu-id="6cb00-110">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="6cb00-110">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="6cb00-111">Code de retour</span><span class="sxs-lookup"><span data-stu-id="6cb00-111">Return code</span></span>                                                                                                                    | <span data-ttu-id="6cb00-112">Description</span><span class="sxs-lookup"><span data-stu-id="6cb00-112">Description</span></span>                                              |
|--------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="6cb00-113"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="6cb00-113"><dt>**S\_OK**</dt></span></span> </dl>                                           | <span data-ttu-id="6cb00-114">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="6cb00-114">Success.</span></span><br/>                                      |
| <dl> <span data-ttu-id="6cb00-115"><dt>**\_code PIN de VFW E \_ \_ déjà \_ bloqué**</dt></span><span class="sxs-lookup"><span data-stu-id="6cb00-115"><dt>**VFW\_E\_PIN\_ALREADY\_BLOCKED**</dt></span></span> </dl>                   | <span data-ttu-id="6cb00-116">Le code PIN est déjà bloqué sur un autre thread.</span><span class="sxs-lookup"><span data-stu-id="6cb00-116">Pin is already blocked on another thread.</span></span><br/>     |
| <dl> <span data-ttu-id="6cb00-117"><dt>**\_ \_ code PIN de VFW E \_ déjà \_ bloqué \_ sur \_ ce \_ thread**</dt></span><span class="sxs-lookup"><span data-stu-id="6cb00-117"><dt>**VFW\_E\_PIN\_ALREADY\_BLOCKED\_ON\_THIS\_THREAD**</dt></span></span> </dl> | <span data-ttu-id="6cb00-118">Le code PIN est déjà bloqué sur le thread appelant.</span><span class="sxs-lookup"><span data-stu-id="6cb00-118">Pin is already blocked on the calling thread.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="6cb00-119">Notes</span><span class="sxs-lookup"><span data-stu-id="6cb00-119">Remarks</span></span>

<span data-ttu-id="6cb00-120">N’appelez pas cette méthode à partir du thread de streaming.</span><span class="sxs-lookup"><span data-stu-id="6cb00-120">Do not call this method from the streaming thread.</span></span>

## <a name="requirements"></a><span data-ttu-id="6cb00-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6cb00-121">Requirements</span></span>



| <span data-ttu-id="6cb00-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6cb00-122">Requirement</span></span> | <span data-ttu-id="6cb00-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="6cb00-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6cb00-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="6cb00-124">Header</span></span><br/>  | <dl> <span data-ttu-id="6cb00-125"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6cb00-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="6cb00-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="6cb00-126">Library</span></span><br/> | <dl> <span data-ttu-id="6cb00-127"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="6cb00-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6cb00-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6cb00-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6cb00-129">**CDynamicOutputPin, classe**</span><span class="sxs-lookup"><span data-stu-id="6cb00-129">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




