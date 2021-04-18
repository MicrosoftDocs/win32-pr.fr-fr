---
description: La méthode DisplayPinInfo suit une connexion de code confidentiel pendant le débogage.
ms.assetid: 3c1aa5ab-7f6b-4518-abf3-b5138f6267ee
title: Méthode CBasePin. DisplayPinInfo (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.DisplayPinInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ea563ca07eaea6b6974a831726918866414a33b9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540532"
---
# <a name="cbasepindisplaypininfo-method"></a><span data-ttu-id="5479e-103">Méthode CBasePin. DisplayPinInfo</span><span class="sxs-lookup"><span data-stu-id="5479e-103">CBasePin.DisplayPinInfo method</span></span>

<span data-ttu-id="5479e-104">La `DisplayPinInfo` méthode effectue le suivi d’une connexion de code confidentiel pendant le débogage.</span><span class="sxs-lookup"><span data-stu-id="5479e-104">The `DisplayPinInfo` method traces a pin connection during debugging.</span></span>

## <a name="syntax"></a><span data-ttu-id="5479e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5479e-105">Syntax</span></span>


```C++
void DisplayPinInfo(
   IPin *pReceivePin
);
```



## <a name="parameters"></a><span data-ttu-id="5479e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5479e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5479e-107">*pReceivePin*</span><span class="sxs-lookup"><span data-stu-id="5479e-107">*pReceivePin*</span></span> 
</dt> <dd>

<span data-ttu-id="5479e-108">Pointeur vers le code confidentiel de réception.</span><span class="sxs-lookup"><span data-stu-id="5479e-108">Pointer to the receiving pin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5479e-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5479e-109">Return value</span></span>

<span data-ttu-id="5479e-110">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="5479e-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5479e-111">Notes</span><span class="sxs-lookup"><span data-stu-id="5479e-111">Remarks</span></span>

<span data-ttu-id="5479e-112">Dans les versions Debug, cette méthode appelle la fonction [**DbgLog**](dbglog.md) pour effectuer le suivi d’une tentative de connexion.</span><span class="sxs-lookup"><span data-stu-id="5479e-112">In debug builds, this method calls the [**DbgLog**](dbglog.md) function to trace a connection attempt.</span></span> <span data-ttu-id="5479e-113">Dans les versions commerciales, cette méthode n’a aucun effet.</span><span class="sxs-lookup"><span data-stu-id="5479e-113">In retail builds, this method does nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="5479e-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5479e-114">Requirements</span></span>



| <span data-ttu-id="5479e-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5479e-115">Requirement</span></span> | <span data-ttu-id="5479e-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="5479e-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5479e-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="5479e-117">Header</span></span><br/>  | <dl> <span data-ttu-id="5479e-118"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5479e-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="5479e-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="5479e-119">Library</span></span><br/> | <dl> <span data-ttu-id="5479e-120"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="5479e-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5479e-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5479e-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5479e-122">**CBasePin, classe**</span><span class="sxs-lookup"><span data-stu-id="5479e-122">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




