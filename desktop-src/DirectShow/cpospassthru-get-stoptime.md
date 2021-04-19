---
description: 'La \_ méthode obtenir StopTime récupère l’heure à laquelle la lecture s’arrête, par rapport à la durée du flux. Cette méthode implémente la méthode IMediaPosition :: obten \_ StopTime.'
ms.assetid: 0ca3f047-ac43-419e-a1ed-b406f89f7af7
title: Méthode CPosPassThru.get_StopTime (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.get_StopTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 227b054a9737c06e56f7311acc7e0093766608b7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532609"
---
# <a name="cpospassthruget_stoptime-method"></a><span data-ttu-id="37009-104">Méthode CPosPassThru. obten \_ StopTime</span><span class="sxs-lookup"><span data-stu-id="37009-104">CPosPassThru.get\_StopTime method</span></span>

<span data-ttu-id="37009-105">La `get_StopTime` méthode récupère l’heure à laquelle la lecture s’arrêtera, par rapport à la durée du flux.</span><span class="sxs-lookup"><span data-stu-id="37009-105">The `get_StopTime` method retrieves the time at which the playback will stop, relative to the duration of the stream.</span></span> <span data-ttu-id="37009-106">Cette méthode implémente la méthode [**IMediaPosition :: obten \_ StopTime**](/windows/desktop/api/Control/nf-control-imediaposition-get_stoptime) .</span><span class="sxs-lookup"><span data-stu-id="37009-106">This method implements the [**IMediaPosition::get\_StopTime**](/windows/desktop/api/Control/nf-control-imediaposition-get_stoptime) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="37009-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="37009-107">Syntax</span></span>


```C++
HRESULT get_StopTime(
   REFTIME *pllTime
);
```



## <a name="parameters"></a><span data-ttu-id="37009-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="37009-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="37009-109">*pllTime*</span><span class="sxs-lookup"><span data-stu-id="37009-109">*pllTime*</span></span> 
</dt> <dd>

<span data-ttu-id="37009-110">Pointeur vers une variable qui reçoit le temps d’arrêt, en secondes.</span><span class="sxs-lookup"><span data-stu-id="37009-110">Pointer to a variable that receives the stop time, in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="37009-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="37009-111">Return value</span></span>

<span data-ttu-id="37009-112">Retourne la valeur **HRESULT** de la broche connectée.</span><span class="sxs-lookup"><span data-stu-id="37009-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="37009-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="37009-113">Requirements</span></span>



| <span data-ttu-id="37009-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="37009-114">Requirement</span></span> | <span data-ttu-id="37009-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="37009-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37009-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="37009-116">Header</span></span><br/>  | <dl> <span data-ttu-id="37009-117"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="37009-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="37009-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="37009-118">Library</span></span><br/> | <dl> <span data-ttu-id="37009-119"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="37009-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="37009-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="37009-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37009-121">**CPosPassThru, classe**</span><span class="sxs-lookup"><span data-stu-id="37009-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




