---
description: 'Méthode CBasePin. EnumMediaTypes : la méthode EnumMediaTypes énumère les types de média préférés du pin. Cette méthode implémente la méthode IPin :: EnumMediaTypes.'
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
ms.openlocfilehash: c68fe1ab83724149dcd2fb58a60e9c6950d887ca
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099387"
---
# <a name="cbasepinenummediatypes-method"></a><span data-ttu-id="8f8d7-104">Méthode CBasePin. EnumMediaTypes</span><span class="sxs-lookup"><span data-stu-id="8f8d7-104">CBasePin.EnumMediaTypes method</span></span>

<span data-ttu-id="8f8d7-105">La `EnumMediaTypes` méthode énumère les types de média préférés du pin.</span><span class="sxs-lookup"><span data-stu-id="8f8d7-105">The `EnumMediaTypes` method enumerates the pin's preferred media types.</span></span> <span data-ttu-id="8f8d7-106">Cette méthode implémente la méthode [**IPIN :: EnumMediaTypes**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes) .</span><span class="sxs-lookup"><span data-stu-id="8f8d7-106">This method implements the [**IPin::EnumMediaTypes**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f8d7-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8f8d7-107">Syntax</span></span>


```C++
HRESULT EnumMediaTypes(
   IEnumMediaTypes **ppEnum
);
```



## <a name="parameters"></a><span data-ttu-id="8f8d7-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8f8d7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8f8d7-109">*ppEnum*</span><span class="sxs-lookup"><span data-stu-id="8f8d7-109">*ppEnum*</span></span> 
</dt> <dd>

<span data-ttu-id="8f8d7-110">Adresse d’une variable qui reçoit un pointeur vers l’interface [**IEnumMediaTypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) .</span><span class="sxs-lookup"><span data-stu-id="8f8d7-110">Address of a variable that receives a pointer to the [**IEnumMediaTypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8f8d7-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="8f8d7-111">Return value</span></span>

<span data-ttu-id="8f8d7-112">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="8f8d7-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="8f8d7-113">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="8f8d7-113">Possible values include those in the following table.</span></span>



| <span data-ttu-id="8f8d7-114">Code de retour</span><span class="sxs-lookup"><span data-stu-id="8f8d7-114">Return code</span></span>                                                                                   | <span data-ttu-id="8f8d7-115">Description</span><span class="sxs-lookup"><span data-stu-id="8f8d7-115">Description</span></span>                           |
|-----------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="8f8d7-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="8f8d7-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="8f8d7-117">Réussite.</span><span class="sxs-lookup"><span data-stu-id="8f8d7-117">Success.</span></span><br/>                   |
| <dl> <span data-ttu-id="8f8d7-118"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="8f8d7-118"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="8f8d7-119">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="8f8d7-119">Insufficient memory.</span></span><br/>       |
| <dl> <span data-ttu-id="8f8d7-120"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="8f8d7-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="8f8d7-121">Argument de pointeur **null** .</span><span class="sxs-lookup"><span data-stu-id="8f8d7-121">**NULL** pointer argument.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="8f8d7-122">Notes </span><span class="sxs-lookup"><span data-stu-id="8f8d7-122">Remarks</span></span>

<span data-ttu-id="8f8d7-123">Les broches d’entrée ne sont pas requises pour énumérer les types préférés.</span><span class="sxs-lookup"><span data-stu-id="8f8d7-123">Input pins are not required to enumerate any preferred types.</span></span> <span data-ttu-id="8f8d7-124">Les broches de sortie doivent énumérer au moins un type préféré.</span><span class="sxs-lookup"><span data-stu-id="8f8d7-124">Output pins must enumerate at least one preferred type.</span></span> <span data-ttu-id="8f8d7-125">Dans le cas contraire, les deux broches ne peuvent pas avoir de type préféré, ce qui rend impossible la connexion.</span><span class="sxs-lookup"><span data-stu-id="8f8d7-125">Otherwise, both pins could lack a preferred type, making a connection impossible.</span></span>

<span data-ttu-id="8f8d7-126">L’interface **IEnumMediaTypes** fonctionne comme un énumérateur com standard.</span><span class="sxs-lookup"><span data-stu-id="8f8d7-126">The **IEnumMediaTypes** interface works like a standard COM enumerator.</span></span> <span data-ttu-id="8f8d7-127">Pour plus d’informations, consultez [énumération d’objets dans un graphique de filtre](enumerating-objects-in-a-filter-graph.md).</span><span class="sxs-lookup"><span data-stu-id="8f8d7-127">For more information, see [Enumerating Objects in a Filter Graph](enumerating-objects-in-a-filter-graph.md).</span></span> <span data-ttu-id="8f8d7-128">Si la méthode est réussie, l’interface **IEnumMediaTypes** a un nombre de références en attente.</span><span class="sxs-lookup"><span data-stu-id="8f8d7-128">If the method succeeds, the **IEnumMediaTypes** interface has an outstanding reference count.</span></span> <span data-ttu-id="8f8d7-129">Veillez à le libérer lorsque vous avez terminé.</span><span class="sxs-lookup"><span data-stu-id="8f8d7-129">Be sure to release it when you are done.</span></span>

<span data-ttu-id="8f8d7-130">La classe de base [**CEnumMediaTypes**](cenummediatypes.md) implémente **IEnumMediaTypes**.</span><span class="sxs-lookup"><span data-stu-id="8f8d7-130">The [**CEnumMediaTypes**](cenummediatypes.md) base class implements **IEnumMediaTypes**.</span></span> <span data-ttu-id="8f8d7-131">Elle appelle la méthode [**CBasePin :: GetMediaType**](cbasepin-getmediatype.md) du pin pour énumérer les types de médias.</span><span class="sxs-lookup"><span data-stu-id="8f8d7-131">It calls the pin's [**CBasePin::GetMediaType**](cbasepin-getmediatype.md) method to enumerate the media types.</span></span>

## <a name="requirements"></a><span data-ttu-id="8f8d7-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8f8d7-132">Requirements</span></span>



| <span data-ttu-id="8f8d7-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8f8d7-133">Requirement</span></span> | <span data-ttu-id="8f8d7-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="8f8d7-134">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f8d7-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="8f8d7-135">Header</span></span><br/>  | <dl> <span data-ttu-id="8f8d7-136"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8f8d7-136"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="8f8d7-137">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="8f8d7-137">Library</span></span><br/> | <dl> <span data-ttu-id="8f8d7-138"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="8f8d7-138"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8f8d7-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8f8d7-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f8d7-140">**CBasePin, classe**</span><span class="sxs-lookup"><span data-stu-id="8f8d7-140">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




