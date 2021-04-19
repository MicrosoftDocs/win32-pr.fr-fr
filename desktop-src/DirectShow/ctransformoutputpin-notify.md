---
description: 'La méthode Notify avertit le code confidentiel qu’une modification de qualité est demandée. Cette méthode implémente la méthode IQualityControl :: Notify.'
ms.assetid: cdb93eef-90d5-4111-a3d4-175903f44a13
title: CTransformOutputPin. Notify, méthode (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin.Notify
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d6ace7e25f1413f6e17a4d19ef937732ea8c689a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539990"
---
# <a name="ctransformoutputpinnotify-method"></a><span data-ttu-id="2c792-104">CTransformOutputPin. Notify, méthode</span><span class="sxs-lookup"><span data-stu-id="2c792-104">CTransformOutputPin.Notify method</span></span>

<span data-ttu-id="2c792-105">La `Notify` méthode notifie le code confidentiel qu’une modification de qualité est demandée.</span><span class="sxs-lookup"><span data-stu-id="2c792-105">The `Notify` method notifies the pin that a quality change is requested.</span></span> <span data-ttu-id="2c792-106">Cette méthode implémente la méthode [**IQualityControl :: Notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) .</span><span class="sxs-lookup"><span data-stu-id="2c792-106">This method implements the [**IQualityControl::Notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c792-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2c792-107">Syntax</span></span>


```C++
HRESULT Notify(
   IBaseFilter *pSelf,
   Quality     q
);
```



## <a name="parameters"></a><span data-ttu-id="2c792-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2c792-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c792-109">*pSelf*</span><span class="sxs-lookup"><span data-stu-id="2c792-109">*pSelf*</span></span> 
</dt> <dd>

<span data-ttu-id="2c792-110">Pointeur vers l’interface [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) du filtre qui a fourni le message de contrôle de qualité.</span><span class="sxs-lookup"><span data-stu-id="2c792-110">Pointer to the [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) interface of the filter that delivered the quality control message.</span></span>

</dd> <dt>

<span data-ttu-id="2c792-111">*question*</span><span class="sxs-lookup"><span data-stu-id="2c792-111">*q*</span></span> 
</dt> <dd>

<span data-ttu-id="2c792-112">Structure de [**qualité**](/windows/win32/api/strmif/ns-strmif-quality) qui contient le message de contrôle qualité.</span><span class="sxs-lookup"><span data-stu-id="2c792-112">[**Quality**](/windows/win32/api/strmif/ns-strmif-quality) structure that contains the quality control message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c792-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2c792-113">Return value</span></span>

<span data-ttu-id="2c792-114">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="2c792-114">Returns an **HRESULT** value.</span></span> <span data-ttu-id="2c792-115">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="2c792-115">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="2c792-116">Code de retour</span><span class="sxs-lookup"><span data-stu-id="2c792-116">Return code</span></span>                                                                                       | <span data-ttu-id="2c792-117">Description</span><span class="sxs-lookup"><span data-stu-id="2c792-117">Description</span></span>                                                |
|---------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <span data-ttu-id="2c792-118"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="2c792-118"><dt>**S\_OK**</dt></span></span> </dl>              | <span data-ttu-id="2c792-119">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="2c792-119">Success.</span></span><br/>                                        |
| <dl> <span data-ttu-id="2c792-120"><dt>**VFW \_ E \_ \_ introuvable**</dt></span><span class="sxs-lookup"><span data-stu-id="2c792-120"><dt>**VFW\_E\_NOT\_FOUND**</dt></span></span> </dl> | <span data-ttu-id="2c792-121">Impossible de trouver un objet pour accepter le message.</span><span class="sxs-lookup"><span data-stu-id="2c792-121">Could not find an object to accept the message.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="2c792-122">Notes</span><span class="sxs-lookup"><span data-stu-id="2c792-122">Remarks</span></span>

<span data-ttu-id="2c792-123">Cette méthode appelle la méthode [**CTransformFilter :: AlterQuality**](ctransformfilter-alterquality.md) du filtre.</span><span class="sxs-lookup"><span data-stu-id="2c792-123">This method calls the filter's [**CTransformFilter::AlterQuality**](ctransformfilter-alterquality.md) method.</span></span> <span data-ttu-id="2c792-124">Si le filtre ne gère pas le message de qualité, cette méthode appelle la méthode [**CBaseInputPin ::P assnotify**](cbaseinputpin-passnotify.md) sur la broche d’entrée du filtre.</span><span class="sxs-lookup"><span data-stu-id="2c792-124">If the filter does not handle the quality message, this method calls the [**CBaseInputPin::PassNotify**](cbaseinputpin-passnotify.md) method on the filter's input pin.</span></span> <span data-ttu-id="2c792-125">La méthode **PassNotify** transmet le message de qualité en amont (ou à un gestionnaire de qualité personnalisé, le cas échéant).</span><span class="sxs-lookup"><span data-stu-id="2c792-125">The **PassNotify** method passes the quality message upstream (or to a custom quality manager, if one was installed).</span></span>

## <a name="requirements"></a><span data-ttu-id="2c792-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2c792-126">Requirements</span></span>



| <span data-ttu-id="2c792-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2c792-127">Requirement</span></span> | <span data-ttu-id="2c792-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="2c792-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c792-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="2c792-129">Header</span></span><br/>  | <dl> <span data-ttu-id="2c792-130"><dt>Transfrm. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2c792-130"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="2c792-131">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="2c792-131">Library</span></span><br/> | <dl> <span data-ttu-id="2c792-132"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="2c792-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




