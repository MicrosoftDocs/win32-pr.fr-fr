---
description: 'Méthode CTransformFilter. GetMediaType : la méthode GetMediaType récupère un type de média préféré pour la broche de sortie.'
ms.assetid: 9a1b123b-aa8a-4bf0-a926-466ded24e506
title: Méthode CTransformFilter. GetMediaType (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.GetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6415b8e3d8ae4e292b7e2592b123120927081ea8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095117"
---
# <a name="ctransformfiltergetmediatype-method"></a><span data-ttu-id="4aa05-103">Méthode CTransformFilter. GetMediaType</span><span class="sxs-lookup"><span data-stu-id="4aa05-103">CTransformFilter.GetMediaType method</span></span>

<span data-ttu-id="4aa05-104">La `GetMediaType` méthode récupère un type de média par défaut pour la broche de sortie.</span><span class="sxs-lookup"><span data-stu-id="4aa05-104">The `GetMediaType` method retrieves a preferred media type for the output pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="4aa05-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4aa05-105">Syntax</span></span>


```C++
virtual HRESULT GetMediaType(
   int        iPosition,
   CMediaType *pMediaType
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="4aa05-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4aa05-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4aa05-107">*iPosition*</span><span class="sxs-lookup"><span data-stu-id="4aa05-107">*iPosition*</span></span> 
</dt> <dd>

<span data-ttu-id="4aa05-108">Valeur d’index de base zéro.</span><span class="sxs-lookup"><span data-stu-id="4aa05-108">Zero-based index value.</span></span>

</dd> <dt>

<span data-ttu-id="4aa05-109">*pMediaType*</span><span class="sxs-lookup"><span data-stu-id="4aa05-109">*pMediaType*</span></span> 
</dt> <dd>

<span data-ttu-id="4aa05-110">Pointeur vers un objet [**CMediaType**](cmediatype.md) qui reçoit le type de média.</span><span class="sxs-lookup"><span data-stu-id="4aa05-110">Pointer to a [**CMediaType**](cmediatype.md) object that receives the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4aa05-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="4aa05-111">Return value</span></span>

<span data-ttu-id="4aa05-112">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4aa05-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="4aa05-113">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="4aa05-113">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="4aa05-114">Code de retour</span><span class="sxs-lookup"><span data-stu-id="4aa05-114">Return code</span></span>                                                                                            | <span data-ttu-id="4aa05-115">Description</span><span class="sxs-lookup"><span data-stu-id="4aa05-115">Description</span></span>                      |
|--------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="4aa05-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="4aa05-116"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="4aa05-117">Réussite.</span><span class="sxs-lookup"><span data-stu-id="4aa05-117">Success.</span></span><br/>              |
| <dl> <span data-ttu-id="4aa05-118"><dt>**VFW \_ S \_ n’a \_ plus d' \_ éléments**</dt></span><span class="sxs-lookup"><span data-stu-id="4aa05-118"><dt>**VFW\_S\_NO\_MORE\_ITEMS**</dt></span></span> </dl> | <span data-ttu-id="4aa05-119">Index hors limites.</span><span class="sxs-lookup"><span data-stu-id="4aa05-119">Index out of range.</span></span><br/>   |
| <dl> <span data-ttu-id="4aa05-120"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="4aa05-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl>           | <span data-ttu-id="4aa05-121">Index inférieur à zéro.</span><span class="sxs-lookup"><span data-stu-id="4aa05-121">Index less than zero.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="4aa05-122">Notes </span><span class="sxs-lookup"><span data-stu-id="4aa05-122">Remarks</span></span>

<span data-ttu-id="4aa05-123">La méthode [**CTransformOutputPin :: GetMediaType**](ctransformoutputpin-getmediatype.md) de la broche de sortie appelle cette méthode.</span><span class="sxs-lookup"><span data-stu-id="4aa05-123">The output pin's [**CTransformOutputPin::GetMediaType**](ctransformoutputpin-getmediatype.md) method calls this method.</span></span> <span data-ttu-id="4aa05-124">La classe dérivée doit implémenter cette méthode.</span><span class="sxs-lookup"><span data-stu-id="4aa05-124">The derived class must implement this method.</span></span> <span data-ttu-id="4aa05-125">Pour plus d’informations, consultez [**CBasePin :: GetMediaType**](cbasepin-getmediatype.md).</span><span class="sxs-lookup"><span data-stu-id="4aa05-125">For more information, see [**CBasePin::GetMediaType**](cbasepin-getmediatype.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4aa05-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4aa05-126">Requirements</span></span>



| <span data-ttu-id="4aa05-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4aa05-127">Requirement</span></span> | <span data-ttu-id="4aa05-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="4aa05-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4aa05-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="4aa05-129">Header</span></span><br/>  | <dl> <span data-ttu-id="4aa05-130"><dt>Transfrm. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4aa05-130"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="4aa05-131">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="4aa05-131">Library</span></span><br/> | <dl> <span data-ttu-id="4aa05-132"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="4aa05-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4aa05-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4aa05-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4aa05-134">**CTransformFilter, classe**</span><span class="sxs-lookup"><span data-stu-id="4aa05-134">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




