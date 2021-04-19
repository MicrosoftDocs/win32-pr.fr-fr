---
description: La méthode FindPin récupère le code confidentiel avec l’identificateur spécifié.
ms.assetid: d07a298f-ddb0-44eb-85ca-81735875cdf3
title: Méthode CBaseRenderer. FindPin (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.FindPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d6e6789a91f34d95933ae7869e1588eeb14b6006
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530328"
---
# <a name="cbaserendererfindpin-method"></a><span data-ttu-id="2c28a-103">Méthode CBaseRenderer. FindPin</span><span class="sxs-lookup"><span data-stu-id="2c28a-103">CBaseRenderer.FindPin method</span></span>

<span data-ttu-id="2c28a-104">La `FindPin` méthode récupère le code confidentiel avec l’identificateur spécifié.</span><span class="sxs-lookup"><span data-stu-id="2c28a-104">The `FindPin` method retrieves the pin with the specified identifier.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c28a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2c28a-105">Syntax</span></span>


```C++
HRESULT FindPin(
   LPCWSTR Id,
   IPin    **ppPin
);
```



## <a name="parameters"></a><span data-ttu-id="2c28a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2c28a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c28a-107">*Id*</span><span class="sxs-lookup"><span data-stu-id="2c28a-107">*Id*</span></span> 
</dt> <dd>

<span data-ttu-id="2c28a-108">Pointeur vers une chaîne de caractères larges se terminant par null qui identifie le code confidentiel.</span><span class="sxs-lookup"><span data-stu-id="2c28a-108">Pointer to a constant, null-terminated wide-character string that identifies the pin.</span></span> <span data-ttu-id="2c28a-109">Doit être L "in".</span><span class="sxs-lookup"><span data-stu-id="2c28a-109">Must be L"In".</span></span>

</dd> <dt>

<span data-ttu-id="2c28a-110">*ppPin*</span><span class="sxs-lookup"><span data-stu-id="2c28a-110">*ppPin*</span></span> 
</dt> <dd>

<span data-ttu-id="2c28a-111">Adresse d’une variable qui reçoit un pointeur vers l’interface [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin) du pin.</span><span class="sxs-lookup"><span data-stu-id="2c28a-111">Address of a variable that receives a pointer to the pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span> <span data-ttu-id="2c28a-112">Si la méthode échoue, *\* ppPin* a la valeur **null**.</span><span class="sxs-lookup"><span data-stu-id="2c28a-112">If the method fails, *\*ppPin* is set to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c28a-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2c28a-113">Return value</span></span>

<span data-ttu-id="2c28a-114">Retourne l’une des valeurs **HRESULT** indiquées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="2c28a-114">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="2c28a-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="2c28a-115">Return code</span></span>                                                                                       | <span data-ttu-id="2c28a-116">Description</span><span class="sxs-lookup"><span data-stu-id="2c28a-116">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="2c28a-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="2c28a-117"><dt>**S\_OK**</dt></span></span> </dl>              | <span data-ttu-id="2c28a-118">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="2c28a-118">Success.</span></span><br/>                   |
| <dl> <span data-ttu-id="2c28a-119"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="2c28a-119"><dt>**E\_POINTER**</dt></span></span> </dl>         | <span data-ttu-id="2c28a-120">Argument de pointeur **null** .</span><span class="sxs-lookup"><span data-stu-id="2c28a-120">**NULL** pointer argument.</span></span><br/> |
| <dl> <span data-ttu-id="2c28a-121"><dt>**VFW \_ E \_ \_ introuvable**</dt></span><span class="sxs-lookup"><span data-stu-id="2c28a-121"><dt>**VFW\_E\_NOT\_FOUND**</dt></span></span> </dl> | <span data-ttu-id="2c28a-122">Introuvable.</span><span class="sxs-lookup"><span data-stu-id="2c28a-122">Not found.</span></span><br/>                 |



 

## <a name="remarks"></a><span data-ttu-id="2c28a-123">Notes</span><span class="sxs-lookup"><span data-stu-id="2c28a-123">Remarks</span></span>

<span data-ttu-id="2c28a-124">Cette méthode remplace la méthode [**CBaseFilter :: FindPin**](cbasefilter-findpin.md) .</span><span class="sxs-lookup"><span data-stu-id="2c28a-124">This method overrides the [**CBaseFilter::FindPin**](cbasefilter-findpin.md) method.</span></span> <span data-ttu-id="2c28a-125">La seule broche du filtre (la broche d’entrée) est nommée « in ».</span><span class="sxs-lookup"><span data-stu-id="2c28a-125">The filter's only pin (the input pin) is named "In".</span></span>

## <a name="requirements"></a><span data-ttu-id="2c28a-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2c28a-126">Requirements</span></span>



| <span data-ttu-id="2c28a-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2c28a-127">Requirement</span></span> | <span data-ttu-id="2c28a-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="2c28a-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c28a-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="2c28a-129">Header</span></span><br/>  | <dl> <span data-ttu-id="2c28a-130"><dt>Renbase. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2c28a-130"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="2c28a-131">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="2c28a-131">Library</span></span><br/> | <dl> <span data-ttu-id="2c28a-132"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="2c28a-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c28a-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2c28a-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c28a-134">**CBaseRenderer, classe**</span><span class="sxs-lookup"><span data-stu-id="2c28a-134">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




