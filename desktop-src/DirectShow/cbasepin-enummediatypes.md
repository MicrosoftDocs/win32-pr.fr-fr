---
description: 'La méthode EnumMediaTypes énumère les types de média préférés du pin. Cette méthode implémente la méthode IPin :: EnumMediaTypes.'
ms.assetid: 0360f9fc-6876-4a54-8de1-bf289e0e10ae
title: Méthode CBasePin. EnumMediaTypes (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.EnumMediaTypes
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 54aaddbbcde26791b6c55665bfbbb7ff62048238
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537098"
---
# <a name="cbasepinenummediatypes-method"></a><span data-ttu-id="e27d4-104">Méthode CBasePin. EnumMediaTypes</span><span class="sxs-lookup"><span data-stu-id="e27d4-104">CBasePin.EnumMediaTypes method</span></span>

<span data-ttu-id="e27d4-105">La `EnumMediaTypes` méthode énumère les types de média préférés du pin.</span><span class="sxs-lookup"><span data-stu-id="e27d4-105">The `EnumMediaTypes` method enumerates the pin's preferred media types.</span></span> <span data-ttu-id="e27d4-106">Cette méthode implémente la méthode [**IPIN :: EnumMediaTypes**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes) .</span><span class="sxs-lookup"><span data-stu-id="e27d4-106">This method implements the [**IPin::EnumMediaTypes**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="e27d4-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e27d4-107">Syntax</span></span>


```C++
HRESULT EnumMediaTypes(
   IEnumMediaTypes **ppEnum
);
```



## <a name="parameters"></a><span data-ttu-id="e27d4-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e27d4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e27d4-109">*ppEnum*</span><span class="sxs-lookup"><span data-stu-id="e27d4-109">*ppEnum*</span></span> 
</dt> <dd>

<span data-ttu-id="e27d4-110">Adresse d’une variable qui reçoit un pointeur vers l’interface [**IEnumMediaTypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) .</span><span class="sxs-lookup"><span data-stu-id="e27d4-110">Address of a variable that receives a pointer to the [**IEnumMediaTypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e27d4-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e27d4-111">Return value</span></span>

<span data-ttu-id="e27d4-112">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e27d4-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="e27d4-113">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="e27d4-113">Possible values include those in the following table.</span></span>



| <span data-ttu-id="e27d4-114">Code de retour</span><span class="sxs-lookup"><span data-stu-id="e27d4-114">Return code</span></span>                                                                                   | <span data-ttu-id="e27d4-115">Description</span><span class="sxs-lookup"><span data-stu-id="e27d4-115">Description</span></span>                           |
|-----------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="e27d4-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e27d4-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="e27d4-117">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="e27d4-117">Success.</span></span><br/>                   |
| <dl> <span data-ttu-id="e27d4-118"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="e27d4-118"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="e27d4-119">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="e27d4-119">Insufficient memory.</span></span><br/>       |
| <dl> <span data-ttu-id="e27d4-120"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="e27d4-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="e27d4-121">Argument de pointeur **null** .</span><span class="sxs-lookup"><span data-stu-id="e27d4-121">**NULL** pointer argument.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e27d4-122">Notes</span><span class="sxs-lookup"><span data-stu-id="e27d4-122">Remarks</span></span>

<span data-ttu-id="e27d4-123">Les broches d’entrée ne sont pas requises pour énumérer les types préférés.</span><span class="sxs-lookup"><span data-stu-id="e27d4-123">Input pins are not required to enumerate any preferred types.</span></span> <span data-ttu-id="e27d4-124">Les broches de sortie doivent énumérer au moins un type préféré.</span><span class="sxs-lookup"><span data-stu-id="e27d4-124">Output pins must enumerate at least one preferred type.</span></span> <span data-ttu-id="e27d4-125">Dans le cas contraire, les deux broches ne peuvent pas avoir de type préféré, ce qui rend impossible la connexion.</span><span class="sxs-lookup"><span data-stu-id="e27d4-125">Otherwise, both pins could lack a preferred type, making a connection impossible.</span></span>

<span data-ttu-id="e27d4-126">L’interface **IEnumMediaTypes** fonctionne comme un énumérateur com standard.</span><span class="sxs-lookup"><span data-stu-id="e27d4-126">The **IEnumMediaTypes** interface works like a standard COM enumerator.</span></span> <span data-ttu-id="e27d4-127">Pour plus d’informations, consultez [énumération d’objets dans un graphique de filtre](enumerating-objects-in-a-filter-graph.md).</span><span class="sxs-lookup"><span data-stu-id="e27d4-127">For more information, see [Enumerating Objects in a Filter Graph](enumerating-objects-in-a-filter-graph.md).</span></span> <span data-ttu-id="e27d4-128">Si la méthode est réussie, l’interface **IEnumMediaTypes** a un nombre de références en attente.</span><span class="sxs-lookup"><span data-stu-id="e27d4-128">If the method succeeds, the **IEnumMediaTypes** interface has an outstanding reference count.</span></span> <span data-ttu-id="e27d4-129">Veillez à le libérer lorsque vous avez terminé.</span><span class="sxs-lookup"><span data-stu-id="e27d4-129">Be sure to release it when you are done.</span></span>

<span data-ttu-id="e27d4-130">La classe de base [**CEnumMediaTypes**](cenummediatypes.md) implémente **IEnumMediaTypes**.</span><span class="sxs-lookup"><span data-stu-id="e27d4-130">The [**CEnumMediaTypes**](cenummediatypes.md) base class implements **IEnumMediaTypes**.</span></span> <span data-ttu-id="e27d4-131">Elle appelle la méthode [**CBasePin :: GetMediaType**](cbasepin-getmediatype.md) du pin pour énumérer les types de médias.</span><span class="sxs-lookup"><span data-stu-id="e27d4-131">It calls the pin's [**CBasePin::GetMediaType**](cbasepin-getmediatype.md) method to enumerate the media types.</span></span>

## <a name="requirements"></a><span data-ttu-id="e27d4-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e27d4-132">Requirements</span></span>



| <span data-ttu-id="e27d4-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e27d4-133">Requirement</span></span> | <span data-ttu-id="e27d4-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="e27d4-134">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e27d4-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="e27d4-135">Header</span></span><br/>  | <dl> <span data-ttu-id="e27d4-136"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e27d4-136"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="e27d4-137">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="e27d4-137">Library</span></span><br/> | <dl> <span data-ttu-id="e27d4-138"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="e27d4-138"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e27d4-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e27d4-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e27d4-140">**CBasePin, classe**</span><span class="sxs-lookup"><span data-stu-id="e27d4-140">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




