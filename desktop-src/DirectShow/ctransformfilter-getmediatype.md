---
description: La méthode GetMediaType récupère un type de média par défaut pour la broche de sortie.
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
ms.openlocfilehash: ba751e291a1ffa8e030be7e77cfd456956718baa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540010"
---
# <a name="ctransformfiltergetmediatype-method"></a><span data-ttu-id="6044a-103">Méthode CTransformFilter. GetMediaType</span><span class="sxs-lookup"><span data-stu-id="6044a-103">CTransformFilter.GetMediaType method</span></span>

<span data-ttu-id="6044a-104">La `GetMediaType` méthode récupère un type de média par défaut pour la broche de sortie.</span><span class="sxs-lookup"><span data-stu-id="6044a-104">The `GetMediaType` method retrieves a preferred media type for the output pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="6044a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6044a-105">Syntax</span></span>


```C++
virtual HRESULT GetMediaType(
   int        iPosition,
   CMediaType *pMediaType
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="6044a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6044a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6044a-107">*iPosition*</span><span class="sxs-lookup"><span data-stu-id="6044a-107">*iPosition*</span></span> 
</dt> <dd>

<span data-ttu-id="6044a-108">Valeur d’index de base zéro.</span><span class="sxs-lookup"><span data-stu-id="6044a-108">Zero-based index value.</span></span>

</dd> <dt>

<span data-ttu-id="6044a-109">*pMediaType*</span><span class="sxs-lookup"><span data-stu-id="6044a-109">*pMediaType*</span></span> 
</dt> <dd>

<span data-ttu-id="6044a-110">Pointeur vers un objet [**CMediaType**](cmediatype.md) qui reçoit le type de média.</span><span class="sxs-lookup"><span data-stu-id="6044a-110">Pointer to a [**CMediaType**](cmediatype.md) object that receives the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6044a-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6044a-111">Return value</span></span>

<span data-ttu-id="6044a-112">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6044a-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="6044a-113">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="6044a-113">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="6044a-114">Code de retour</span><span class="sxs-lookup"><span data-stu-id="6044a-114">Return code</span></span>                                                                                            | <span data-ttu-id="6044a-115">Description</span><span class="sxs-lookup"><span data-stu-id="6044a-115">Description</span></span>                      |
|--------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="6044a-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="6044a-116"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="6044a-117">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="6044a-117">Success.</span></span><br/>              |
| <dl> <span data-ttu-id="6044a-118"><dt>**VFW \_ S \_ n’a \_ plus d' \_ éléments**</dt></span><span class="sxs-lookup"><span data-stu-id="6044a-118"><dt>**VFW\_S\_NO\_MORE\_ITEMS**</dt></span></span> </dl> | <span data-ttu-id="6044a-119">Index hors limites.</span><span class="sxs-lookup"><span data-stu-id="6044a-119">Index out of range.</span></span><br/>   |
| <dl> <span data-ttu-id="6044a-120"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="6044a-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl>           | <span data-ttu-id="6044a-121">Index inférieur à zéro.</span><span class="sxs-lookup"><span data-stu-id="6044a-121">Index less than zero.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="6044a-122">Notes</span><span class="sxs-lookup"><span data-stu-id="6044a-122">Remarks</span></span>

<span data-ttu-id="6044a-123">La méthode [**CTransformOutputPin :: GetMediaType**](ctransformoutputpin-getmediatype.md) de la broche de sortie appelle cette méthode.</span><span class="sxs-lookup"><span data-stu-id="6044a-123">The output pin's [**CTransformOutputPin::GetMediaType**](ctransformoutputpin-getmediatype.md) method calls this method.</span></span> <span data-ttu-id="6044a-124">La classe dérivée doit implémenter cette méthode.</span><span class="sxs-lookup"><span data-stu-id="6044a-124">The derived class must implement this method.</span></span> <span data-ttu-id="6044a-125">Pour plus d’informations, consultez [**CBasePin :: GetMediaType**](cbasepin-getmediatype.md).</span><span class="sxs-lookup"><span data-stu-id="6044a-125">For more information, see [**CBasePin::GetMediaType**](cbasepin-getmediatype.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6044a-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6044a-126">Requirements</span></span>



| <span data-ttu-id="6044a-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6044a-127">Requirement</span></span> | <span data-ttu-id="6044a-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="6044a-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6044a-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="6044a-129">Header</span></span><br/>  | <dl> <span data-ttu-id="6044a-130"><dt>Transfrm. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6044a-130"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="6044a-131">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="6044a-131">Library</span></span><br/> | <dl> <span data-ttu-id="6044a-132"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="6044a-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6044a-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6044a-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6044a-134">**CTransformFilter, classe**</span><span class="sxs-lookup"><span data-stu-id="6044a-134">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




