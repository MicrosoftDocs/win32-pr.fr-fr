---
description: La méthode PassNotify transmet un message de contrôle qualité à l’objet approprié.
ms.assetid: dbc9a4b7-a522-4fbf-8e3a-af50e11c1d80
title: Méthode CBaseInputPin. PassNotify (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.PassNotify
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 36316815ae1d9fde1a18fb36029da92ae6263f20
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525202"
---
# <a name="cbaseinputpinpassnotify-method"></a><span data-ttu-id="ef485-103">Méthode CBaseInputPin. PassNotify</span><span class="sxs-lookup"><span data-stu-id="ef485-103">CBaseInputPin.PassNotify method</span></span>

<span data-ttu-id="ef485-104">La `PassNotify` méthode passe un message de contrôle qualité à l’objet approprié.</span><span class="sxs-lookup"><span data-stu-id="ef485-104">The `PassNotify` method passes a quality-control message to the appropriate object.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef485-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ef485-105">Syntax</span></span>


```C++
HRESULT PassNotify(
   Quality q
);
```



## <a name="parameters"></a><span data-ttu-id="ef485-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ef485-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef485-107">*question*</span><span class="sxs-lookup"><span data-stu-id="ef485-107">*q*</span></span> 
</dt> <dd>

<span data-ttu-id="ef485-108">Structure de [**qualité**](/windows/win32/api/strmif/ns-strmif-quality) qui contient le message de contrôle qualité.</span><span class="sxs-lookup"><span data-stu-id="ef485-108">[**Quality**](/windows/win32/api/strmif/ns-strmif-quality) structure that contains the quality-control message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ef485-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ef485-109">Return value</span></span>

<span data-ttu-id="ef485-110">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ef485-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="ef485-111">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="ef485-111">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="ef485-112">Code de retour</span><span class="sxs-lookup"><span data-stu-id="ef485-112">Return code</span></span>                                                                                       | <span data-ttu-id="ef485-113">Description</span><span class="sxs-lookup"><span data-stu-id="ef485-113">Description</span></span>                                                |
|---------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <span data-ttu-id="ef485-114"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ef485-114"><dt>**S\_OK**</dt></span></span> </dl>              | <span data-ttu-id="ef485-115">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="ef485-115">Success.</span></span><br/>                                        |
| <dl> <span data-ttu-id="ef485-116"><dt>**VFW \_ E \_ \_ introuvable**</dt></span><span class="sxs-lookup"><span data-stu-id="ef485-116"><dt>**VFW\_E\_NOT\_FOUND**</dt></span></span> </dl> | <span data-ttu-id="ef485-117">Impossible de trouver un objet pour accepter le message.</span><span class="sxs-lookup"><span data-stu-id="ef485-117">Could not find an object to accept the message.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ef485-118">Notes</span><span class="sxs-lookup"><span data-stu-id="ef485-118">Remarks</span></span>

<span data-ttu-id="ef485-119">Appelez cette méthode si le filtre ne gère pas les messages de contrôle de qualité.</span><span class="sxs-lookup"><span data-stu-id="ef485-119">Call this method if the filter does not handle quality-control messages.</span></span> <span data-ttu-id="ef485-120">Cette méthode transmet le message à l’un des objets suivants, par ordre de préférence :</span><span class="sxs-lookup"><span data-stu-id="ef485-120">This method passes the message to one of the following objects, in order of preference:</span></span>

-   <span data-ttu-id="ef485-121">Gestionnaire de contrôle de qualité externe, si la méthode [**IQualityControl :: SetSink**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-setsink) a été appelée.</span><span class="sxs-lookup"><span data-stu-id="ef485-121">An external quality-control manager, if the [**IQualityControl::SetSink**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-setsink) method was called.</span></span>
-   <span data-ttu-id="ef485-122">Broche de sortie en amont.</span><span class="sxs-lookup"><span data-stu-id="ef485-122">The upstream output pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="ef485-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ef485-123">Requirements</span></span>



| <span data-ttu-id="ef485-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ef485-124">Requirement</span></span> | <span data-ttu-id="ef485-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="ef485-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef485-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="ef485-126">Header</span></span><br/>  | <dl> <span data-ttu-id="ef485-127"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ef485-127"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="ef485-128">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ef485-128">Library</span></span><br/> | <dl> <span data-ttu-id="ef485-129"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="ef485-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ef485-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ef485-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef485-131">**CBaseInputPin, classe**</span><span class="sxs-lookup"><span data-stu-id="ef485-131">**CBaseInputPin Class**</span></span>](cbaseinputpin.md)
</dt> <dt>

[<span data-ttu-id="ef485-132">Gestion du contrôle de la qualité</span><span class="sxs-lookup"><span data-stu-id="ef485-132">Quality-Control Management</span></span>](quality-control-management.md)
</dt> </dl>

 

 




