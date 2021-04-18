---
description: 'La méthode Notify avertit le code confidentiel qu’une modification de qualité est demandée. Cette méthode implémente la méthode IQualityControl :: Notify.'
ms.assetid: 5e9394d9-8d3c-4091-b45f-345a3f7270db
title: CBasePin. Notify, méthode (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.Notify
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f34ea630a461226c32b9d827b2b91dcd0874cac7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532878"
---
# <a name="cbasepinnotify-method"></a><span data-ttu-id="60ffa-104">CBasePin. Notify, méthode</span><span class="sxs-lookup"><span data-stu-id="60ffa-104">CBasePin.Notify method</span></span>

<span data-ttu-id="60ffa-105">La `Notify` méthode notifie le code confidentiel qu’une modification de qualité est demandée.</span><span class="sxs-lookup"><span data-stu-id="60ffa-105">The `Notify` method notifies the pin that a quality change is requested.</span></span> <span data-ttu-id="60ffa-106">Cette méthode implémente la méthode [**IQualityControl :: Notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) .</span><span class="sxs-lookup"><span data-stu-id="60ffa-106">This method implements the [**IQualityControl::Notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="60ffa-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="60ffa-107">Syntax</span></span>


```C++
HRESULT Notify(
   IBaseFilter *pSelf,
   Quality     q
);
```



## <a name="parameters"></a><span data-ttu-id="60ffa-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="60ffa-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="60ffa-109">*pSelf*</span><span class="sxs-lookup"><span data-stu-id="60ffa-109">*pSelf*</span></span> 
</dt> <dd>

<span data-ttu-id="60ffa-110">Pointeur vers l’interface [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) du filtre qui a fourni le message de contrôle qualité.</span><span class="sxs-lookup"><span data-stu-id="60ffa-110">Pointer to the [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) interface of the filter that delivered the quality-control message.</span></span>

</dd> <dt>

<span data-ttu-id="60ffa-111">*question*</span><span class="sxs-lookup"><span data-stu-id="60ffa-111">*q*</span></span> 
</dt> <dd>

<span data-ttu-id="60ffa-112">Spécifie une structure de [**qualité**](/windows/win32/api/strmif/ns-strmif-quality) qui contient le message de contrôle qualité.</span><span class="sxs-lookup"><span data-stu-id="60ffa-112">Specifies a [**Quality**](/windows/win32/api/strmif/ns-strmif-quality) structure that contains the quality-control message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="60ffa-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="60ffa-113">Return value</span></span>

<span data-ttu-id="60ffa-114">La classe de base retourne E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="60ffa-114">The base class returns E\_NOTIMPL.</span></span>

## <a name="remarks"></a><span data-ttu-id="60ffa-115">Notes</span><span class="sxs-lookup"><span data-stu-id="60ffa-115">Remarks</span></span>

<span data-ttu-id="60ffa-116">Les broches de sortie doivent remplacer cette méthode pour accepter des messages de contrôle qualité.</span><span class="sxs-lookup"><span data-stu-id="60ffa-116">Output pins should override this method to accept quality-control messages.</span></span>

<span data-ttu-id="60ffa-117">Si un gestionnaire de qualité externe a été installé (voir [**CBasePin :: SetSink**](cbasepin-setsink.md)), transmettez le message à ce gestionnaire de qualité.</span><span class="sxs-lookup"><span data-stu-id="60ffa-117">If an external quality manager was installed (see [**CBasePin::SetSink**](cbasepin-setsink.md)), pass the message to that quality manager.</span></span> <span data-ttu-id="60ffa-118">Dans le cas contraire, le filtre doit gérer le message lui-même ou passer le message en amont.</span><span class="sxs-lookup"><span data-stu-id="60ffa-118">Otherwise, the filter should handle the message itself, or pass the message upstream.</span></span> <span data-ttu-id="60ffa-119">Pour plus d’informations, consultez [gestion du contrôle qualité](quality-control-management.md).</span><span class="sxs-lookup"><span data-stu-id="60ffa-119">For more information, see [Quality-Control Management](quality-control-management.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="60ffa-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="60ffa-120">Requirements</span></span>



| <span data-ttu-id="60ffa-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="60ffa-121">Requirement</span></span> | <span data-ttu-id="60ffa-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="60ffa-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="60ffa-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="60ffa-123">Header</span></span><br/>  | <dl> <span data-ttu-id="60ffa-124"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="60ffa-124"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="60ffa-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="60ffa-125">Library</span></span><br/> | <dl> <span data-ttu-id="60ffa-126"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="60ffa-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="60ffa-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="60ffa-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60ffa-128">**CBasePin, classe**</span><span class="sxs-lookup"><span data-stu-id="60ffa-128">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




