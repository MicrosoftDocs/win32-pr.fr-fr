---
description: 'La méthode suivante récupère un nombre spécifié de codes confidentiels dans la séquence d’énumération. Cette méthode implémente la méthode IEnumPins :: Next.'
ms.assetid: c38fbd32-7d83-43ec-a105-4a7cb515b471
title: Méthode CEnumPins. Next (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CEnumPins.Next
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 612dcd638939b34803b7296babf7445a07cdad22
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106534770"
---
# <a name="cenumpinsnext-method"></a><span data-ttu-id="a6cab-104">CEnumPins. Next, méthode</span><span class="sxs-lookup"><span data-stu-id="a6cab-104">CEnumPins.Next method</span></span>

<span data-ttu-id="a6cab-105">La méthode suivante récupère un nombre spécifié de codes confidentiels dans la séquence d’énumération.</span><span class="sxs-lookup"><span data-stu-id="a6cab-105">The Next method retrieves a specified number of pins in the enumeration sequence.</span></span> <span data-ttu-id="a6cab-106">Cette méthode implémente la méthode [**IEnumPins :: Next**](/windows/desktop/api/Strmif/nf-strmif-ienumpins-next) .</span><span class="sxs-lookup"><span data-stu-id="a6cab-106">This method implements the [**IEnumPins::Next**](/windows/desktop/api/Strmif/nf-strmif-ienumpins-next) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6cab-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a6cab-107">Syntax</span></span>


```C++
HRESULT Next(
   ULONG cPins,
   IPin  **ppPins,
   ULONG *pcFetched
);
```



## <a name="parameters"></a><span data-ttu-id="a6cab-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a6cab-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a6cab-109">*cPins*</span><span class="sxs-lookup"><span data-stu-id="a6cab-109">*cPins*</span></span> 
</dt> <dd>

<span data-ttu-id="a6cab-110">Nombre de codes confidentiels à récupérer.</span><span class="sxs-lookup"><span data-stu-id="a6cab-110">Number of pins to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="a6cab-111">*ppPins*</span><span class="sxs-lookup"><span data-stu-id="a6cab-111">*ppPins*</span></span> 
</dt> <dd>

<span data-ttu-id="a6cab-112">Tableau de taille *cPins* qui est rempli avec les pointeurs [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin) .</span><span class="sxs-lookup"><span data-stu-id="a6cab-112">Array of size *cPins* that is filled with [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) pointers.</span></span>

</dd> <dt>

<span data-ttu-id="a6cab-113">*pcFetched*</span><span class="sxs-lookup"><span data-stu-id="a6cab-113">*pcFetched*</span></span> 
</dt> <dd>

<span data-ttu-id="a6cab-114">Pointeur vers une variable qui reçoit le nombre de codes confidentiels récupérés.</span><span class="sxs-lookup"><span data-stu-id="a6cab-114">Pointer to a variable that receives the number of pins retrieved.</span></span> <span data-ttu-id="a6cab-115">Peut avoir la **valeur null** si *cPins* est 1.</span><span class="sxs-lookup"><span data-stu-id="a6cab-115">Can be **NULL** if *cPins* is 1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a6cab-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a6cab-116">Return value</span></span>

<span data-ttu-id="a6cab-117">Retourne l’une des valeurs **HRESULT** indiquées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="a6cab-117">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="a6cab-118">Code de retour</span><span class="sxs-lookup"><span data-stu-id="a6cab-118">Return code</span></span>                                                                                                | <span data-ttu-id="a6cab-119">Description</span><span class="sxs-lookup"><span data-stu-id="a6cab-119">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a6cab-120"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="a6cab-120"><dt>**S\_FALSE**</dt></span></span> </dl>                    | <span data-ttu-id="a6cab-121">N’a pas récupéré autant de codes confidentiels que nécessaire.</span><span class="sxs-lookup"><span data-stu-id="a6cab-121">Did not retrieve as many pins as requested.</span></span><br/>                                 |
| <dl> <span data-ttu-id="a6cab-122"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="a6cab-122"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="a6cab-123">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="a6cab-123">Success.</span></span><br/>                                                                    |
| <dl> <span data-ttu-id="a6cab-124"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="a6cab-124"><dt>**E\_INVALIDARG**</dt></span></span> </dl>               | <span data-ttu-id="a6cab-125">Argument non valide.</span><span class="sxs-lookup"><span data-stu-id="a6cab-125">Invalid argument.</span></span><br/>                                                           |
| <dl> <span data-ttu-id="a6cab-126"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="a6cab-126"><dt>**E\_POINTER**</dt></span></span> </dl>                  | <span data-ttu-id="a6cab-127">Argument de pointeur **null** .</span><span class="sxs-lookup"><span data-stu-id="a6cab-127">**NULL** pointer argument.</span></span><br/>                                                  |
| <dl> <span data-ttu-id="a6cab-128"><dt>**VFW \_ E \_ enum \_ non \_ \_ synchronisé**</dt></span><span class="sxs-lookup"><span data-stu-id="a6cab-128"><dt>**VFW\_E\_ENUM\_OUT\_OF\_SYNC**</dt></span></span> </dl> | <span data-ttu-id="a6cab-129">L’état du filtre a changé et est désormais incohérent avec l’énumérateur.</span><span class="sxs-lookup"><span data-stu-id="a6cab-129">The filter's state has changed and is now inconsistent with the enumerator.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a6cab-130">Notes</span><span class="sxs-lookup"><span data-stu-id="a6cab-130">Remarks</span></span>

<span data-ttu-id="a6cab-131">Cette méthode récupère les pointeurs vers le nombre spécifié de broches, en démarrant à la position actuelle dans l’énumération, et les place dans le tableau spécifié.</span><span class="sxs-lookup"><span data-stu-id="a6cab-131">This method retrieves pointers to the specified number of pins, starting at the current position in the enumeration, and places them in the specified array.</span></span>

<span data-ttu-id="a6cab-132">Cette méthode appelle la méthode [**CBaseFilter :: GetPin**](cbasefilter-getpin.md) du filtre pour récupérer les broches.</span><span class="sxs-lookup"><span data-stu-id="a6cab-132">This method calls the filter's [**CBaseFilter::GetPin**](cbasefilter-getpin.md) method to retrieve the pins.</span></span>

<span data-ttu-id="a6cab-133">Si la méthode est réussie, les pointeurs **IPIN** ont tous des décomptes de références en attente.</span><span class="sxs-lookup"><span data-stu-id="a6cab-133">If the method succeeds, the **IPin** pointers all have outstanding reference counts.</span></span> <span data-ttu-id="a6cab-134">Veillez à les libérer une fois que vous avez terminé.</span><span class="sxs-lookup"><span data-stu-id="a6cab-134">Be sure to release them when you are done.</span></span>

## <a name="requirements"></a><span data-ttu-id="a6cab-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a6cab-135">Requirements</span></span>



| <span data-ttu-id="a6cab-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a6cab-136">Requirement</span></span> | <span data-ttu-id="a6cab-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="a6cab-137">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a6cab-138">En-tête</span><span class="sxs-lookup"><span data-stu-id="a6cab-138">Header</span></span><br/>  | <dl> <span data-ttu-id="a6cab-139"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a6cab-139"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="a6cab-140">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="a6cab-140">Library</span></span><br/> | <dl> <span data-ttu-id="a6cab-141"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="a6cab-141"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a6cab-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a6cab-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6cab-143">**CEnumPins, classe**</span><span class="sxs-lookup"><span data-stu-id="a6cab-143">**CEnumPins Class**</span></span>](cenumpins.md)
</dt> </dl>

 

 




