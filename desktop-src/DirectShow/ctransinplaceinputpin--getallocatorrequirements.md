---
description: 'La méthode GetAllocatorRequirements récupère les propriétés Allocator demandées par le code confidentiel. Cette méthode implémente la méthode IMemInputPin :: GetAllocatorRequirements.'
ms.assetid: 1355facc-f863-44b2-9284-8f06f62d39a2
title: Méthode CTransInPlaceInputPin. GetAllocatorRequirements (Transip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceInputPin.GetAllocatorRequirements
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dfa176cd5da0317821996593e19bb90396e82224
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543271"
---
# <a name="ctransinplaceinputpingetallocatorrequirements-method"></a><span data-ttu-id="b602d-104">Méthode CTransInPlaceInputPin. GetAllocatorRequirements</span><span class="sxs-lookup"><span data-stu-id="b602d-104">CTransInPlaceInputPin.GetAllocatorRequirements method</span></span>

<span data-ttu-id="b602d-105">La `GetAllocatorRequirements` méthode récupère les propriétés Allocator demandées par le code confidentiel.</span><span class="sxs-lookup"><span data-stu-id="b602d-105">The `GetAllocatorRequirements` method retrieves the allocator properties requested by the pin.</span></span> <span data-ttu-id="b602d-106">Cette méthode implémente la méthode [**IMemInputPin :: GetAllocatorRequirements**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocatorrequirements) .</span><span class="sxs-lookup"><span data-stu-id="b602d-106">This method implements the [**IMemInputPin::GetAllocatorRequirements**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocatorrequirements) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="b602d-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b602d-107">Syntax</span></span>


```C++
HRESULT GetAllocatorRequirements(
   ALLOCATOR_PROPERTIES *pProps
);
```



## <a name="parameters"></a><span data-ttu-id="b602d-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b602d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b602d-109">*pProps*</span><span class="sxs-lookup"><span data-stu-id="b602d-109">*pProps*</span></span> 
</dt> <dd>

<span data-ttu-id="b602d-110">Pointeur vers une structure de [**\_ Propriétés Allocator**](/windows/win32/api/strmif/ns-strmif-allocator_properties) , qui est remplie avec les spécifications.</span><span class="sxs-lookup"><span data-stu-id="b602d-110">Pointer to an [**ALLOCATOR\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-allocator_properties) structure, which is filled in with the requirements.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b602d-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b602d-111">Return value</span></span>

<span data-ttu-id="b602d-112">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b602d-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="b602d-113">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="b602d-113">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="b602d-114">Code de retour</span><span class="sxs-lookup"><span data-stu-id="b602d-114">Return code</span></span>                                                                               | <span data-ttu-id="b602d-115">Description</span><span class="sxs-lookup"><span data-stu-id="b602d-115">Description</span></span>                                                                                          |
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b602d-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="b602d-116"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="b602d-117">Succès</span><span class="sxs-lookup"><span data-stu-id="b602d-117">Success</span></span><br/>                                                                                   |
| <dl> <span data-ttu-id="b602d-118"><dt>**\_NOTIMPL E**</dt></span><span class="sxs-lookup"><span data-stu-id="b602d-118"><dt>**E\_NOTIMPL**</dt></span></span> </dl> | <span data-ttu-id="b602d-119">La broche de sortie n’est pas connectée ou la broche d’entrée en aval ne prend pas en charge la méthode.</span><span class="sxs-lookup"><span data-stu-id="b602d-119">The output pin is not connected, or the downstream input pin does not support the method.</span></span><br/> |
| <dl> <span data-ttu-id="b602d-120"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="b602d-120"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="b602d-121">Argument de pointeur **null**</span><span class="sxs-lookup"><span data-stu-id="b602d-121">**NULL** pointer argument</span></span><br/>                                                                 |



 

## <a name="remarks"></a><span data-ttu-id="b602d-122">Notes</span><span class="sxs-lookup"><span data-stu-id="b602d-122">Remarks</span></span>

<span data-ttu-id="b602d-123">Si la broche de sortie est connectée, cette méthode passe l’appel à la broche d’entrée en aval.</span><span class="sxs-lookup"><span data-stu-id="b602d-123">If the output pin is connected, this method passes the call to the downstream input pin.</span></span> <span data-ttu-id="b602d-124">Dans le cas contraire, elle retourne E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="b602d-124">Otherwise, it returns E\_NOTIMPL.</span></span>

## <a name="requirements"></a><span data-ttu-id="b602d-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b602d-125">Requirements</span></span>



| <span data-ttu-id="b602d-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b602d-126">Requirement</span></span> | <span data-ttu-id="b602d-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="b602d-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b602d-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="b602d-128">Header</span></span><br/>  | <dl> <span data-ttu-id="b602d-129"><dt>Transip. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b602d-129"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="b602d-130">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b602d-130">Library</span></span><br/> | <dl> <span data-ttu-id="b602d-131"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="b602d-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b602d-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b602d-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b602d-133">**CTransInPlaceInputPin, classe**</span><span class="sxs-lookup"><span data-stu-id="b602d-133">**CTransInPlaceInputPin Class**</span></span>](ctransinplaceinputpin.md)
</dt> </dl>

 

 




