---
description: 'La méthode EnumPins énumère les codes confidentiels sur ce filtre. Cette méthode implémente la méthode IBaseFilter :: EnumPins.'
ms.assetid: c1015ed3-658f-4f96-a1fb-e04b81a9ddb5
title: Méthode CBaseFilter. EnumPins (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.EnumPins
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 66a0f88a9749ba1dabb982e2f275da8a4be2a422
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537577"
---
# <a name="cbasefilterenumpins-method"></a><span data-ttu-id="f0bdf-104">Méthode CBaseFilter. EnumPins</span><span class="sxs-lookup"><span data-stu-id="f0bdf-104">CBaseFilter.EnumPins method</span></span>

<span data-ttu-id="f0bdf-105">La `EnumPins` méthode énumère les broches sur ce filtre.</span><span class="sxs-lookup"><span data-stu-id="f0bdf-105">The `EnumPins` method enumerates the pins on this filter.</span></span> <span data-ttu-id="f0bdf-106">Cette méthode implémente la méthode [**IBaseFilter :: EnumPins**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-enumpins) .</span><span class="sxs-lookup"><span data-stu-id="f0bdf-106">This method implements the [**IBaseFilter::EnumPins**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-enumpins) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0bdf-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f0bdf-107">Syntax</span></span>


```C++
HRESULT EnumPins(
   IEnumPins **ppEnum
);
```



## <a name="parameters"></a><span data-ttu-id="f0bdf-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f0bdf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0bdf-109">*ppEnum*</span><span class="sxs-lookup"><span data-stu-id="f0bdf-109">*ppEnum*</span></span> 
</dt> <dd>

<span data-ttu-id="f0bdf-110">Adresse d’une variable qui reçoit un pointeur vers l’interface [**IEnumPins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) .</span><span class="sxs-lookup"><span data-stu-id="f0bdf-110">Address of a variable that receives a pointer to the [**IEnumPins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f0bdf-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f0bdf-111">Return value</span></span>

<span data-ttu-id="f0bdf-112">Retourne l’une des valeurs **HRESULT** suivantes.</span><span class="sxs-lookup"><span data-stu-id="f0bdf-112">Returns one of the following **HRESULT** values.</span></span>



| <span data-ttu-id="f0bdf-113">Code de retour</span><span class="sxs-lookup"><span data-stu-id="f0bdf-113">Return code</span></span>                                                                                   | <span data-ttu-id="f0bdf-114">Description</span><span class="sxs-lookup"><span data-stu-id="f0bdf-114">Description</span></span>                          |
|-----------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <span data-ttu-id="f0bdf-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f0bdf-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="f0bdf-116">Succès</span><span class="sxs-lookup"><span data-stu-id="f0bdf-116">Success</span></span><br/>                   |
| <dl> <span data-ttu-id="f0bdf-117"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="f0bdf-117"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="f0bdf-118">Mémoire insuffisante</span><span class="sxs-lookup"><span data-stu-id="f0bdf-118">Insufficient memory</span></span><br/>       |
| <dl> <span data-ttu-id="f0bdf-119"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="f0bdf-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="f0bdf-120">Argument de pointeur **null**</span><span class="sxs-lookup"><span data-stu-id="f0bdf-120">**NULL** pointer argument</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f0bdf-121">Notes</span><span class="sxs-lookup"><span data-stu-id="f0bdf-121">Remarks</span></span>

<span data-ttu-id="f0bdf-122">Cette méthode crée une instance de la classe de base [**CEnumPins**](cenumpins.md) et retourne un pointeur vers cet objet, de type **IEnumPins**.</span><span class="sxs-lookup"><span data-stu-id="f0bdf-122">This method creates an instance of the [**CEnumPins**](cenumpins.md) base class, and returns a pointer to that object, of type **IEnumPins**.</span></span> <span data-ttu-id="f0bdf-123">La classe **CEnumPins** appelle la méthode [**CBaseFilter :: GetPin**](cbasefilter-getpin.md) du filtre pour énumérer les broches sur le filtre.</span><span class="sxs-lookup"><span data-stu-id="f0bdf-123">The **CEnumPins** class calls the filter's [**CBaseFilter::GetPin**](cbasefilter-getpin.md) method to enumerate the pins on the filter.</span></span>

<span data-ttu-id="f0bdf-124">Si cette méthode est réussie, l’interface **IEnumPins** a un nombre de références en attente.</span><span class="sxs-lookup"><span data-stu-id="f0bdf-124">If this method succeeds, the **IEnumPins** interface has an outstanding reference count.</span></span> <span data-ttu-id="f0bdf-125">L’appelant doit libérer l’interface.</span><span class="sxs-lookup"><span data-stu-id="f0bdf-125">The caller must release the interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="f0bdf-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f0bdf-126">Requirements</span></span>



| <span data-ttu-id="f0bdf-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f0bdf-127">Requirement</span></span> | <span data-ttu-id="f0bdf-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="f0bdf-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0bdf-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="f0bdf-129">Header</span></span><br/>  | <dl> <span data-ttu-id="f0bdf-130"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f0bdf-130"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="f0bdf-131">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f0bdf-131">Library</span></span><br/> | <dl> <span data-ttu-id="f0bdf-132"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="f0bdf-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f0bdf-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f0bdf-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0bdf-134">**CBaseFilter, classe**</span><span class="sxs-lookup"><span data-stu-id="f0bdf-134">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




