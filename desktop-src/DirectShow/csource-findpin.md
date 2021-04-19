---
description: 'La méthode FindPin récupère le code confidentiel avec l’identificateur spécifié. Cette méthode implémente la méthode IBaseFilter :: FindPin.'
ms.assetid: ad593dbf-ca56-4409-ac6e-1b88908c8cee
title: Méthode CSource. FindPin (source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSource.FindPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9fac8df1e53e4a129b42d1284a19392bc7b58aa2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535853"
---
# <a name="csourcefindpin-method"></a><span data-ttu-id="76870-104">Méthode CSource. FindPin</span><span class="sxs-lookup"><span data-stu-id="76870-104">CSource.FindPin method</span></span>

<span data-ttu-id="76870-105">La `FindPin` méthode récupère le code confidentiel avec l’identificateur spécifié.</span><span class="sxs-lookup"><span data-stu-id="76870-105">The `FindPin` method retrieves the pin with the specified identifier.</span></span> <span data-ttu-id="76870-106">Cette méthode implémente la méthode [**IBaseFilter :: FindPin**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-findpin) .</span><span class="sxs-lookup"><span data-stu-id="76870-106">This method implements the [**IBaseFilter::FindPin**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-findpin) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="76870-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="76870-107">Syntax</span></span>


```C++
HRESULT FindPin(
   LPCWSTR Id,
   IPin    **ppPin
);
```



## <a name="parameters"></a><span data-ttu-id="76870-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="76870-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="76870-109">*Id*</span><span class="sxs-lookup"><span data-stu-id="76870-109">*Id*</span></span> 
</dt> <dd>

<span data-ttu-id="76870-110">Pointeur vers une chaîne terminée par le caractère null qui identifie le code confidentiel.</span><span class="sxs-lookup"><span data-stu-id="76870-110">Pointer to a null-terminated string that identifies the pin.</span></span>

</dd> <dt>

<span data-ttu-id="76870-111">*ppPin*</span><span class="sxs-lookup"><span data-stu-id="76870-111">*ppPin*</span></span> 
</dt> <dd>

<span data-ttu-id="76870-112">Reçoit un pointeur vers l’interface [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin) du pin.</span><span class="sxs-lookup"><span data-stu-id="76870-112">Receives a pointer to the pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span> <span data-ttu-id="76870-113">Si la méthode échoue, \* *ppPin* a la valeur **null** .</span><span class="sxs-lookup"><span data-stu-id="76870-113">If the method fails, \**ppPin* is set to **NULL**</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="76870-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="76870-114">Return value</span></span>

<span data-ttu-id="76870-115">Retourne l’une des valeurs **HRESULT** indiquées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="76870-115">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="76870-116">Code de retour</span><span class="sxs-lookup"><span data-stu-id="76870-116">Return code</span></span>                                                                                       | <span data-ttu-id="76870-117">Description</span><span class="sxs-lookup"><span data-stu-id="76870-117">Description</span></span>                                           |
|---------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <span data-ttu-id="76870-118"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="76870-118"><dt>**S\_OK**</dt></span></span> </dl>              | <span data-ttu-id="76870-119">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="76870-119">Success.</span></span><br/>                                   |
| <dl> <span data-ttu-id="76870-120"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="76870-120"><dt>**E\_POINTER**</dt></span></span> </dl>         | <span data-ttu-id="76870-121">Argument de pointeur **null** .</span><span class="sxs-lookup"><span data-stu-id="76870-121">**NULL** pointer argument.</span></span><br/>                 |
| <dl> <span data-ttu-id="76870-122"><dt>**VFW \_ E \_ \_ introuvable**</dt></span><span class="sxs-lookup"><span data-stu-id="76870-122"><dt>**VFW\_E\_NOT\_FOUND**</dt></span></span> </dl> | <span data-ttu-id="76870-123">Impossible de trouver un code confidentiel avec cet identificateur.</span><span class="sxs-lookup"><span data-stu-id="76870-123">Could not find a pin with this identifier.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="76870-124">Notes</span><span class="sxs-lookup"><span data-stu-id="76870-124">Remarks</span></span>

<span data-ttu-id="76870-125">Le premier pin est toujours nommé « 1 »; le deuxième pin est nommé « 2 ». et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="76870-125">The first pin is always named "1"; the second pin is named "2"; and so forth.</span></span> <span data-ttu-id="76870-126">Pour plus d’informations, consultez [**CSourceStream :: QueryId**](csourcestream-queryid.md).</span><span class="sxs-lookup"><span data-stu-id="76870-126">For more information, see [**CSourceStream::QueryId**](csourcestream-queryid.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="76870-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="76870-127">Requirements</span></span>



| <span data-ttu-id="76870-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="76870-128">Requirement</span></span> | <span data-ttu-id="76870-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="76870-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="76870-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="76870-130">Header</span></span><br/>  | <dl> <span data-ttu-id="76870-131"><dt>Source. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="76870-131"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="76870-132">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="76870-132">Library</span></span><br/> | <dl> <span data-ttu-id="76870-133"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="76870-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="76870-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="76870-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76870-135">**CSource, classe**</span><span class="sxs-lookup"><span data-stu-id="76870-135">**CSource Class**</span></span>](csource.md)
</dt> </dl>

 

 




