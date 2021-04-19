---
description: 'La méthode Notify avertit le code confidentiel qu’une modification de qualité est demandée. Cette méthode implémente la méthode IQualityControl :: Notify.'
ms.assetid: 76124321-0d2d-4fee-a08a-4db23078e8df
title: CBaseInputPin. Notify, méthode (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.Notify
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a5ae7ca47c5adc11c87a739e8736ba327dc0b65f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543279"
---
# <a name="cbaseinputpinnotify-method"></a><span data-ttu-id="59b65-104">CBaseInputPin. Notify, méthode</span><span class="sxs-lookup"><span data-stu-id="59b65-104">CBaseInputPin.Notify method</span></span>

<span data-ttu-id="59b65-105">La `Notify` méthode notifie le code confidentiel qu’une modification de qualité est demandée.</span><span class="sxs-lookup"><span data-stu-id="59b65-105">The `Notify` method notifies the pin that a quality change is requested.</span></span> <span data-ttu-id="59b65-106">Cette méthode implémente la méthode [**IQualityControl :: Notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) .</span><span class="sxs-lookup"><span data-stu-id="59b65-106">This method implements the [**IQualityControl::Notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="59b65-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="59b65-107">Syntax</span></span>


```C++
HRESULT Notify(
   IBaseFilter *pSelf,
   Quality     q
);
```



## <a name="parameters"></a><span data-ttu-id="59b65-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="59b65-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="59b65-109">*pSelf*</span><span class="sxs-lookup"><span data-stu-id="59b65-109">*pSelf*</span></span> 
</dt> <dd>

<span data-ttu-id="59b65-110">Pointeur vers le filtre qui envoie le message de contrôle qualité.</span><span class="sxs-lookup"><span data-stu-id="59b65-110">Pointer to the filter that is sending the quality-control message.</span></span>

</dd> <dt>

<span data-ttu-id="59b65-111">*question*</span><span class="sxs-lookup"><span data-stu-id="59b65-111">*q*</span></span> 
</dt> <dd>

<span data-ttu-id="59b65-112">Structure de [**qualité**](/windows/win32/api/strmif/ns-strmif-quality) qui contient le message de contrôle qualité.</span><span class="sxs-lookup"><span data-stu-id="59b65-112">[**Quality**](/windows/win32/api/strmif/ns-strmif-quality) structure that contains the quality-control message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="59b65-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="59b65-113">Return value</span></span>

<span data-ttu-id="59b65-114">Retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="59b65-114">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="59b65-115">Notes</span><span class="sxs-lookup"><span data-stu-id="59b65-115">Remarks</span></span>

<span data-ttu-id="59b65-116">En règle générale, les filtres passent des messages de contrôle qualité à une broche de sortie en amont, et non à une broche d’entrée.</span><span class="sxs-lookup"><span data-stu-id="59b65-116">Filters usually pass quality-control messages to an upstream output pin, not to an input pin.</span></span> <span data-ttu-id="59b65-117">Par conséquent, cette méthode retourne S \_ OK sans rien faire.</span><span class="sxs-lookup"><span data-stu-id="59b65-117">Therefore, this method returns S\_OK without doing anything.</span></span>

## <a name="requirements"></a><span data-ttu-id="59b65-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="59b65-118">Requirements</span></span>



| <span data-ttu-id="59b65-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="59b65-119">Requirement</span></span> | <span data-ttu-id="59b65-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="59b65-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="59b65-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="59b65-121">Header</span></span><br/>  | <dl> <span data-ttu-id="59b65-122"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="59b65-122"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="59b65-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="59b65-123">Library</span></span><br/> | <dl> <span data-ttu-id="59b65-124"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="59b65-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="59b65-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="59b65-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59b65-126">**CBaseInputPin, classe**</span><span class="sxs-lookup"><span data-stu-id="59b65-126">**CBaseInputPin Class**</span></span>](cbaseinputpin.md)
</dt> <dt>

[<span data-ttu-id="59b65-127">Gestion du contrôle de la qualité</span><span class="sxs-lookup"><span data-stu-id="59b65-127">Quality-Control Management</span></span>](quality-control-management.md)
</dt> </dl>

 

 




