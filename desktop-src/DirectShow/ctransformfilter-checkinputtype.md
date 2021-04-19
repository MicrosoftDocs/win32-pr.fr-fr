---
description: La méthode CheckInputType vérifie si un type de média spécifié est acceptable pour l’entrée.
ms.assetid: 11f156f7-add2-45be-a0d3-05d21f596b89
title: Méthode CTransformFilter. CheckInputType (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.CheckInputType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 63c48a0502ee074b0940f85386dca0619a3ad12d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543788"
---
# <a name="ctransformfiltercheckinputtype-method"></a><span data-ttu-id="48c6e-103">Méthode CTransformFilter. CheckInputType</span><span class="sxs-lookup"><span data-stu-id="48c6e-103">CTransformFilter.CheckInputType method</span></span>

<span data-ttu-id="48c6e-104">La `CheckInputType` méthode vérifie si un type de média spécifié est acceptable pour l’entrée.</span><span class="sxs-lookup"><span data-stu-id="48c6e-104">The `CheckInputType` method checks whether a specified media type is acceptable for input.</span></span>

## <a name="syntax"></a><span data-ttu-id="48c6e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="48c6e-105">Syntax</span></span>


```C++
virtual HRESULT CheckInputType(
   const CMediaType *mtIn
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="48c6e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="48c6e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="48c6e-107">*mtIn*</span><span class="sxs-lookup"><span data-stu-id="48c6e-107">*mtIn*</span></span> 
</dt> <dd>

<span data-ttu-id="48c6e-108">Pointeur vers un objet [**CMediaType**](cmediatype.md) qui spécifie le type de média.</span><span class="sxs-lookup"><span data-stu-id="48c6e-108">Pointer to a [**CMediaType**](cmediatype.md) object that specifies the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="48c6e-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="48c6e-109">Return value</span></span>

<span data-ttu-id="48c6e-110">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="48c6e-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="48c6e-111">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="48c6e-111">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="48c6e-112">Code de retour</span><span class="sxs-lookup"><span data-stu-id="48c6e-112">Return code</span></span>                                                                                                | <span data-ttu-id="48c6e-113">Description</span><span class="sxs-lookup"><span data-stu-id="48c6e-113">Description</span></span>                              |
|------------------------------------------------------------------------------------------------------------|------------------------------------------|
| <dl> <span data-ttu-id="48c6e-114"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="48c6e-114"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="48c6e-115">Le type de média est acceptable.</span><span class="sxs-lookup"><span data-stu-id="48c6e-115">Media type is acceptable.</span></span><br/>     |
| <dl> <span data-ttu-id="48c6e-116"><dt>**TYPE de VFW \_ E \_ \_ non \_ accepté**</dt></span><span class="sxs-lookup"><span data-stu-id="48c6e-116"><dt>**VFW\_E\_TYPE\_NOT\_ACCEPTED**</dt></span></span> </dl> | <span data-ttu-id="48c6e-117">Le type de média n’est pas acceptable.</span><span class="sxs-lookup"><span data-stu-id="48c6e-117">Media type is not acceptable.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="48c6e-118">Notes</span><span class="sxs-lookup"><span data-stu-id="48c6e-118">Remarks</span></span>

<span data-ttu-id="48c6e-119">La classe dérivée doit implémenter cette méthode.</span><span class="sxs-lookup"><span data-stu-id="48c6e-119">The derived class must implement this method.</span></span> <span data-ttu-id="48c6e-120">Retourne S \_ OK si le format d’entrée proposé est acceptable, ou un code d’erreur dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="48c6e-120">Return S\_OK if the proposed input format is acceptable, or an error code otherwise.</span></span>

<span data-ttu-id="48c6e-121">Cette méthode n’a pas besoin de vérifier que le format d’entrée est compatible avec le format de sortie (le cas échéant).</span><span class="sxs-lookup"><span data-stu-id="48c6e-121">This method does not need to verify that the input format is compatible with the output format (if any).</span></span> <span data-ttu-id="48c6e-122">La broche d’entrée vérifie cela en appelant la méthode [**CheckTransform**](ctransformfilter-checktransform.md) .</span><span class="sxs-lookup"><span data-stu-id="48c6e-122">The input pin verifies that by calling the [**CheckTransform**](ctransformfilter-checktransform.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="48c6e-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="48c6e-123">Requirements</span></span>



| <span data-ttu-id="48c6e-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="48c6e-124">Requirement</span></span> | <span data-ttu-id="48c6e-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="48c6e-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="48c6e-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="48c6e-126">Header</span></span><br/>  | <dl> <span data-ttu-id="48c6e-127"><dt>Transfrm. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="48c6e-127"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="48c6e-128">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="48c6e-128">Library</span></span><br/> | <dl> <span data-ttu-id="48c6e-129"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="48c6e-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="48c6e-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="48c6e-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48c6e-131">**CTransformFilter, classe**</span><span class="sxs-lookup"><span data-stu-id="48c6e-131">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




