---
description: 'Méthode CBasePin. GetMediaType : la méthode GetMediaType récupère un type de média préféré, par valeur d’index.'
ms.assetid: 96f102b0-e2d1-49a1-84af-aa4622cae2a9
title: Méthode CBasePin. GetMediaType (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.GetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 186f2eddbedf4eb0565a4ca66ff4ed7e5b080090
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099367"
---
# <a name="cbasepingetmediatype-method"></a><span data-ttu-id="4f52b-103">Méthode CBasePin. GetMediaType</span><span class="sxs-lookup"><span data-stu-id="4f52b-103">CBasePin.GetMediaType method</span></span>

<span data-ttu-id="4f52b-104">La `GetMediaType` méthode récupère un type de média préféré, par valeur d’index.</span><span class="sxs-lookup"><span data-stu-id="4f52b-104">The `GetMediaType` method retrieves a preferred media type, by index value.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f52b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4f52b-105">Syntax</span></span>


```C++
virtual HRESULT GetMediaType(
   int        iPosition,
   CMediaType *pMediaType
);
```



## <a name="parameters"></a><span data-ttu-id="4f52b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4f52b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4f52b-107">*iPosition*</span><span class="sxs-lookup"><span data-stu-id="4f52b-107">*iPosition*</span></span> 
</dt> <dd>

<span data-ttu-id="4f52b-108">Valeur d’index de base zéro.</span><span class="sxs-lookup"><span data-stu-id="4f52b-108">Zero-based index value.</span></span>

</dd> <dt>

<span data-ttu-id="4f52b-109">*pMediaType*</span><span class="sxs-lookup"><span data-stu-id="4f52b-109">*pMediaType*</span></span> 
</dt> <dd>

<span data-ttu-id="4f52b-110">Pointeur vers un objet [**CMediaType**](cmediatype.md) qui reçoit le type de média.</span><span class="sxs-lookup"><span data-stu-id="4f52b-110">Pointer to a [**CMediaType**](cmediatype.md) object that receives the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4f52b-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="4f52b-111">Return value</span></span>

<span data-ttu-id="4f52b-112">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4f52b-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="4f52b-113">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="4f52b-113">Possible values include those in the following table.</span></span>



| <span data-ttu-id="4f52b-114">Code de retour</span><span class="sxs-lookup"><span data-stu-id="4f52b-114">Return code</span></span>                                                                                            | <span data-ttu-id="4f52b-115">Description</span><span class="sxs-lookup"><span data-stu-id="4f52b-115">Description</span></span>                      |
|--------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="4f52b-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="4f52b-116"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="4f52b-117">Réussite.</span><span class="sxs-lookup"><span data-stu-id="4f52b-117">Success.</span></span><br/>              |
| <dl> <span data-ttu-id="4f52b-118"><dt>**VFW \_ S \_ n’a \_ plus d' \_ éléments**</dt></span><span class="sxs-lookup"><span data-stu-id="4f52b-118"><dt>**VFW\_S\_NO\_MORE\_ITEMS**</dt></span></span> </dl> | <span data-ttu-id="4f52b-119">Index hors limites.</span><span class="sxs-lookup"><span data-stu-id="4f52b-119">Index out of range.</span></span><br/>   |
| <dl> <span data-ttu-id="4f52b-120"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="4f52b-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl>           | <span data-ttu-id="4f52b-121">Index inférieur à zéro.</span><span class="sxs-lookup"><span data-stu-id="4f52b-121">Index less than zero.</span></span><br/> |
| <dl> <span data-ttu-id="4f52b-122"><dt>**E \_ inattendu**</dt></span><span class="sxs-lookup"><span data-stu-id="4f52b-122"><dt>**E\_UNEXPECTED**</dt></span></span> </dl>           | <span data-ttu-id="4f52b-123">Erreur inattendue.</span><span class="sxs-lookup"><span data-stu-id="4f52b-123">Unexpected error.</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="4f52b-124">Notes </span><span class="sxs-lookup"><span data-stu-id="4f52b-124">Remarks</span></span>

<span data-ttu-id="4f52b-125">Dans la liste des types de média préférés du pin, cette méthode retourne le type avec une valeur d’index de *iPosition*.</span><span class="sxs-lookup"><span data-stu-id="4f52b-125">From the pin's list of preferred media types, this method returns the type with an index value of *iPosition*.</span></span> <span data-ttu-id="4f52b-126">La classe [**CEnumMediaTypes**](cenummediatypes.md) appelle cette méthode pour énumérer les types de média préférés.</span><span class="sxs-lookup"><span data-stu-id="4f52b-126">The [**CEnumMediaTypes**](cenummediatypes.md) class calls this method to enumerate preferred media types.</span></span>

<span data-ttu-id="4f52b-127">La classe de base retourne E \_ inattendue.</span><span class="sxs-lookup"><span data-stu-id="4f52b-127">The base class returns E\_UNEXPECTED.</span></span> <span data-ttu-id="4f52b-128">Substituez cette méthode dans votre classe dérivée.</span><span class="sxs-lookup"><span data-stu-id="4f52b-128">Override this method in your derived class.</span></span>

## <a name="requirements"></a><span data-ttu-id="4f52b-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4f52b-129">Requirements</span></span>



| <span data-ttu-id="4f52b-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4f52b-130">Requirement</span></span> | <span data-ttu-id="4f52b-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="4f52b-131">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f52b-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="4f52b-132">Header</span></span><br/>  | <dl> <span data-ttu-id="4f52b-133"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4f52b-133"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="4f52b-134">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="4f52b-134">Library</span></span><br/> | <dl> <span data-ttu-id="4f52b-135"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="4f52b-135"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4f52b-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4f52b-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f52b-137">**CBasePin, classe**</span><span class="sxs-lookup"><span data-stu-id="4f52b-137">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




