---
description: La méthode AlterQuality avertit le filtre qu’une modification de qualité est demandée.
ms.assetid: 46743d6b-65cf-4d63-8913-114277d76da4
title: Méthode CTransformFilter. AlterQuality (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.AlterQuality
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 592fc67dd5cee5e4f76b8171b6e842532d71371b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106520833"
---
# <a name="ctransformfilteralterquality-method"></a><span data-ttu-id="8f665-103">Méthode CTransformFilter. AlterQuality</span><span class="sxs-lookup"><span data-stu-id="8f665-103">CTransformFilter.AlterQuality method</span></span>

<span data-ttu-id="8f665-104">La `AlterQuality` méthode notifie le filtre qu’une modification de qualité est demandée.</span><span class="sxs-lookup"><span data-stu-id="8f665-104">The `AlterQuality` method notifies the filter that a quality change is requested.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f665-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8f665-105">Syntax</span></span>


```C++
virtual HRESULT AlterQuality(
   Quality q
);
```



## <a name="parameters"></a><span data-ttu-id="8f665-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8f665-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8f665-107">*question*</span><span class="sxs-lookup"><span data-stu-id="8f665-107">*q*</span></span> 
</dt> <dd>

<span data-ttu-id="8f665-108">Structure de [**qualité**](/windows/win32/api/strmif/ns-strmif-quality) qui contient le message de contrôle qualité.</span><span class="sxs-lookup"><span data-stu-id="8f665-108">[**Quality**](/windows/win32/api/strmif/ns-strmif-quality) structure that contains the quality control message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8f665-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8f665-109">Return value</span></span>

<span data-ttu-id="8f665-110">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="8f665-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="8f665-111">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="8f665-111">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="8f665-112">Code de retour</span><span class="sxs-lookup"><span data-stu-id="8f665-112">Return code</span></span>                                                                             | <span data-ttu-id="8f665-113">Description</span><span class="sxs-lookup"><span data-stu-id="8f665-113">Description</span></span>                                                                           |
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="8f665-114"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="8f665-114"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="8f665-115">Le message de qualité n’a pas été géré.</span><span class="sxs-lookup"><span data-stu-id="8f665-115">Did not handle the quality message.</span></span> <span data-ttu-id="8f665-116">Le message doit être passé en amont.</span><span class="sxs-lookup"><span data-stu-id="8f665-116">The message should be passed upstream.</span></span><br/> |
| <dl> <span data-ttu-id="8f665-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="8f665-117"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="8f665-118">Le message de qualité a été géré.</span><span class="sxs-lookup"><span data-stu-id="8f665-118">Handled the quality message.</span></span> <span data-ttu-id="8f665-119">Aucune action supplémentaire n’est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="8f665-119">No further action is necessary.</span></span><br/>               |



 

## <a name="remarks"></a><span data-ttu-id="8f665-120">Notes</span><span class="sxs-lookup"><span data-stu-id="8f665-120">Remarks</span></span>

<span data-ttu-id="8f665-121">Substituez cette méthode si le filtre peut effectuer un contrôle de qualité.</span><span class="sxs-lookup"><span data-stu-id="8f665-121">Override this method if the filter can perform quality control.</span></span> <span data-ttu-id="8f665-122">Pour plus d’informations, consultez [gestion du contrôle qualité](quality-control-management.md).</span><span class="sxs-lookup"><span data-stu-id="8f665-122">For more information, see [Quality-Control Management](quality-control-management.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8f665-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8f665-123">Requirements</span></span>



| <span data-ttu-id="8f665-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8f665-124">Requirement</span></span> | <span data-ttu-id="8f665-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="8f665-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f665-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="8f665-126">Header</span></span><br/>  | <dl> <span data-ttu-id="8f665-127"><dt>Transfrm. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8f665-127"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="8f665-128">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="8f665-128">Library</span></span><br/> | <dl> <span data-ttu-id="8f665-129"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="8f665-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8f665-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8f665-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f665-131">**CTransformFilter, classe**</span><span class="sxs-lookup"><span data-stu-id="8f665-131">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




