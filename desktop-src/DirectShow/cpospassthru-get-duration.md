---
description: 'La méthode obtenir la \_ durée récupère la durée du flux. Cette méthode implémente la méthode IMediaPosition :: obten \_ Duration.'
ms.assetid: 326a8cd3-d05f-49d0-941d-08f9778e9a06
title: Méthode CPosPassThru.get_Duration (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.get_Duration
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: df518a0691a4fe1a6c0443ba93a83e65577efe21
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545654"
---
# <a name="cpospassthruget_duration-method"></a><span data-ttu-id="31099-104">Méthode CPosPassThru. obten \_ Duration</span><span class="sxs-lookup"><span data-stu-id="31099-104">CPosPassThru.get\_Duration method</span></span>

<span data-ttu-id="31099-105">La `get_Duration` méthode récupère la durée du flux.</span><span class="sxs-lookup"><span data-stu-id="31099-105">The `get_Duration` method retrieves the duration of the stream.</span></span> <span data-ttu-id="31099-106">Cette méthode implémente la méthode [**IMediaPosition :: obten \_ Duration**](/windows/desktop/api/Control/nf-control-imediaposition-get_duration) .</span><span class="sxs-lookup"><span data-stu-id="31099-106">This method implements the [**IMediaPosition::get\_Duration**](/windows/desktop/api/Control/nf-control-imediaposition-get_duration) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="31099-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="31099-107">Syntax</span></span>


```C++
HRESULT get_Duration(
   REFTIME *plength
);
```



## <a name="parameters"></a><span data-ttu-id="31099-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="31099-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="31099-109">*plength*</span><span class="sxs-lookup"><span data-stu-id="31099-109">*plength*</span></span> 
</dt> <dd>

<span data-ttu-id="31099-110">Pointeur vers une variable qui reçoit la longueur totale du flux, en secondes.</span><span class="sxs-lookup"><span data-stu-id="31099-110">Pointer to a variable that receives the total stream length, in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="31099-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="31099-111">Return value</span></span>

<span data-ttu-id="31099-112">Retourne la valeur **HRESULT** de la broche connectée.</span><span class="sxs-lookup"><span data-stu-id="31099-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="31099-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="31099-113">Requirements</span></span>



| <span data-ttu-id="31099-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="31099-114">Requirement</span></span> | <span data-ttu-id="31099-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="31099-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="31099-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="31099-116">Header</span></span><br/>  | <dl> <span data-ttu-id="31099-117"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="31099-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="31099-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="31099-118">Library</span></span><br/> | <dl> <span data-ttu-id="31099-119"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="31099-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="31099-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="31099-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31099-121">**CPosPassThru, classe**</span><span class="sxs-lookup"><span data-stu-id="31099-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




