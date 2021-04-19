---
description: La méthode CheckTransform vérifie si un type de média d’entrée est compatible avec un type de média de sortie.
ms.assetid: 349145e5-c12d-41df-ae37-7846f8aaa423
title: Méthode CTransformFilter. CheckTransform (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.CheckTransform
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2b3302304e6a0f9df41005f7ed63d9316a3cd410
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106520977"
---
# <a name="ctransformfilterchecktransform-method"></a><span data-ttu-id="859d9-103">Méthode CTransformFilter. CheckTransform</span><span class="sxs-lookup"><span data-stu-id="859d9-103">CTransformFilter.CheckTransform method</span></span>

<span data-ttu-id="859d9-104">La `CheckTransform` méthode vérifie si un type de média d’entrée est compatible avec un type de média de sortie.</span><span class="sxs-lookup"><span data-stu-id="859d9-104">The `CheckTransform` method checks whether an input media type is compatible with an output media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="859d9-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="859d9-105">Syntax</span></span>


```C++
virtual HRESULT CheckTransform(
   const CMediaType *mtIn,
   const CMediaType *mtOut
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="859d9-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="859d9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="859d9-107">*mtIn*</span><span class="sxs-lookup"><span data-stu-id="859d9-107">*mtIn*</span></span> 
</dt> <dd>

<span data-ttu-id="859d9-108">Pointeur vers un objet [**CMediaType**](cmediatype.md) qui spécifie le type d’entrée.</span><span class="sxs-lookup"><span data-stu-id="859d9-108">Pointer to a [**CMediaType**](cmediatype.md) object that specifies the input type.</span></span>

</dd> <dt>

<span data-ttu-id="859d9-109">*mtOut*</span><span class="sxs-lookup"><span data-stu-id="859d9-109">*mtOut*</span></span> 
</dt> <dd>

<span data-ttu-id="859d9-110">Pointeur vers un objet [**CMediaType**](cmediatype.md) qui spécifie le type de sortie.</span><span class="sxs-lookup"><span data-stu-id="859d9-110">Pointer to a [**CMediaType**](cmediatype.md) object that specifies the output type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="859d9-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="859d9-111">Return value</span></span>

<span data-ttu-id="859d9-112">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="859d9-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="859d9-113">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="859d9-113">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="859d9-114">Code de retour</span><span class="sxs-lookup"><span data-stu-id="859d9-114">Return code</span></span>                                                                                                | <span data-ttu-id="859d9-115">Description</span><span class="sxs-lookup"><span data-stu-id="859d9-115">Description</span></span>                                    |
|------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="859d9-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="859d9-116"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="859d9-117">Les types de média sont compatibles.</span><span class="sxs-lookup"><span data-stu-id="859d9-117">The media types are compatible.</span></span><br/>     |
| <dl> <span data-ttu-id="859d9-118"><dt>**TYPE de VFW \_ E \_ \_ non \_ accepté**</dt></span><span class="sxs-lookup"><span data-stu-id="859d9-118"><dt>**VFW\_E\_TYPE\_NOT\_ACCEPTED**</dt></span></span> </dl> | <span data-ttu-id="859d9-119">Les types de média ne sont pas compatibles.</span><span class="sxs-lookup"><span data-stu-id="859d9-119">The media types are not compatible.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="859d9-120">Notes</span><span class="sxs-lookup"><span data-stu-id="859d9-120">Remarks</span></span>

<span data-ttu-id="859d9-121">La classe dérivée doit implémenter cette méthode.</span><span class="sxs-lookup"><span data-stu-id="859d9-121">The derived class must implement this method.</span></span> <span data-ttu-id="859d9-122">Retourne S \_ OK si le filtre peut accepter les deux types de média spécifiés, ou un code d’erreur dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="859d9-122">Return S\_OK if the filter can accept both of the specified media types, or an error code otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="859d9-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="859d9-123">Requirements</span></span>



| <span data-ttu-id="859d9-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="859d9-124">Requirement</span></span> | <span data-ttu-id="859d9-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="859d9-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="859d9-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="859d9-126">Header</span></span><br/>  | <dl> <span data-ttu-id="859d9-127"><dt>Transfrm. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="859d9-127"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="859d9-128">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="859d9-128">Library</span></span><br/> | <dl> <span data-ttu-id="859d9-129"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="859d9-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




