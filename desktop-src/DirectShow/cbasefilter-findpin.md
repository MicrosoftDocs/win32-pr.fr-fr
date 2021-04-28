---
description: 'Méthode CBaseFilter. FindPin : la méthode FindPin récupère le code confidentiel avec l’identificateur spécifié. Cette méthode implémente la méthode IBaseFilter :: FindPin.'
ms.assetid: 152e4ff3-2809-4c57-b9c8-f51fc50b3703
title: Méthode CBaseFilter. FindPin (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.FindPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2bbef9b051a42597b2585a432f544eead4e2e0a1
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099817"
---
# <a name="cbasefilterfindpin-method"></a><span data-ttu-id="f21b1-104">Méthode CBaseFilter. FindPin</span><span class="sxs-lookup"><span data-stu-id="f21b1-104">CBaseFilter.FindPin method</span></span>

<span data-ttu-id="f21b1-105">La `FindPin` méthode récupère le code confidentiel avec l’identificateur spécifié.</span><span class="sxs-lookup"><span data-stu-id="f21b1-105">The `FindPin` method retrieves the pin with the specified identifier.</span></span> <span data-ttu-id="f21b1-106">Cette méthode implémente la méthode [**IBaseFilter :: FindPin**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-findpin) .</span><span class="sxs-lookup"><span data-stu-id="f21b1-106">This method implements the [**IBaseFilter::FindPin**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-findpin) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="f21b1-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f21b1-107">Syntax</span></span>


```C++
HRESULT FindPin(
   LPCWSTR Id,
   IPin    **ppPin
);
```



## <a name="parameters"></a><span data-ttu-id="f21b1-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f21b1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f21b1-109">*Id*</span><span class="sxs-lookup"><span data-stu-id="f21b1-109">*Id*</span></span> 
</dt> <dd>

<span data-ttu-id="f21b1-110">Pointeur vers une chaîne Unicode de constante, terminée par un caractère null, qui identifie le code confidentiel.</span><span class="sxs-lookup"><span data-stu-id="f21b1-110">Pointer to a constant, null-terminated Unicode string that identifies the pin.</span></span>

</dd> <dt>

<span data-ttu-id="f21b1-111">*ppPin*</span><span class="sxs-lookup"><span data-stu-id="f21b1-111">*ppPin*</span></span> 
</dt> <dd>

<span data-ttu-id="f21b1-112">Adresse d’une variable qui reçoit un pointeur vers l’interface [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin) du pin.</span><span class="sxs-lookup"><span data-stu-id="f21b1-112">Address of a variable that receives a pointer to the pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f21b1-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="f21b1-113">Return value</span></span>

<span data-ttu-id="f21b1-114">Retourne l’une des valeurs **HRESULT** suivantes.</span><span class="sxs-lookup"><span data-stu-id="f21b1-114">Returns one of the following **HRESULT** values.</span></span>



| <span data-ttu-id="f21b1-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="f21b1-115">Return code</span></span>                                                                                       | <span data-ttu-id="f21b1-116">Description</span><span class="sxs-lookup"><span data-stu-id="f21b1-116">Description</span></span>                               |
|---------------------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="f21b1-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f21b1-117"><dt>**S\_OK**</dt></span></span> </dl>              | <span data-ttu-id="f21b1-118">Réussite.</span><span class="sxs-lookup"><span data-stu-id="f21b1-118">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="f21b1-119"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="f21b1-119"><dt>**E\_POINTER**</dt></span></span> </dl>         | <span data-ttu-id="f21b1-120">Argument de pointeur **null** .</span><span class="sxs-lookup"><span data-stu-id="f21b1-120">**NULL** pointer argument.</span></span><br/>     |
| <dl> <span data-ttu-id="f21b1-121"><dt>**VFW \_ E \_ \_ introuvable**</dt></span><span class="sxs-lookup"><span data-stu-id="f21b1-121"><dt>**VFW\_E\_NOT\_FOUND**</dt></span></span> </dl> | <span data-ttu-id="f21b1-122">Impossible de trouver un code PIN correspondant.</span><span class="sxs-lookup"><span data-stu-id="f21b1-122">Could not find a matching pin.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f21b1-123">Notes </span><span class="sxs-lookup"><span data-stu-id="f21b1-123">Remarks</span></span>

<span data-ttu-id="f21b1-124">Cette méthode appelle la méthode [**CBasePin :: Name**](cbasepin-name.md) pour comparer le nom de chaque pin à la chaîne spécifiée par le paramètre *ID* .</span><span class="sxs-lookup"><span data-stu-id="f21b1-124">This method calls the [**CBasePin::Name**](cbasepin-name.md) method to compare each pin's name against the string specified by the *Id* parameter.</span></span>

<span data-ttu-id="f21b1-125">Si la méthode est réussie, l’interface **IPIN** a un nombre de références en attente.</span><span class="sxs-lookup"><span data-stu-id="f21b1-125">If the method succeeds, the **IPin** interface has an outstanding reference count.</span></span> <span data-ttu-id="f21b1-126">Veillez à le libérer lorsque vous avez terminé.</span><span class="sxs-lookup"><span data-stu-id="f21b1-126">Be sure to release it when you are done.</span></span>

## <a name="requirements"></a><span data-ttu-id="f21b1-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f21b1-127">Requirements</span></span>



| <span data-ttu-id="f21b1-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f21b1-128">Requirement</span></span> | <span data-ttu-id="f21b1-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="f21b1-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f21b1-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="f21b1-130">Header</span></span><br/>  | <dl> <span data-ttu-id="f21b1-131"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f21b1-131"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="f21b1-132">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f21b1-132">Library</span></span><br/> | <dl> <span data-ttu-id="f21b1-133"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="f21b1-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f21b1-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f21b1-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f21b1-135">**CBaseFilter, classe**</span><span class="sxs-lookup"><span data-stu-id="f21b1-135">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




