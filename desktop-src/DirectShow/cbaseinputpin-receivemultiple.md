---
description: 'La méthode ReceiveMultiple reçoit un tableau d’exemples. Cette méthode implémente la méthode IMemInputPin :: ReceiveMultiple.'
ms.assetid: 21e757c7-f623-4ccb-8e37-512ee4dd7aa7
title: Méthode CBaseInputPin. ReceiveMultiple (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.ReceiveMultiple
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5725b7d8b70c8f7c61eb44231812997a903ba41a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526468"
---
# <a name="cbaseinputpinreceivemultiple-method"></a><span data-ttu-id="4d601-104">Méthode CBaseInputPin. ReceiveMultiple</span><span class="sxs-lookup"><span data-stu-id="4d601-104">CBaseInputPin.ReceiveMultiple method</span></span>

<span data-ttu-id="4d601-105">La `ReceiveMultiple` méthode reçoit un tableau d’exemples.</span><span class="sxs-lookup"><span data-stu-id="4d601-105">The `ReceiveMultiple` method receives an array of samples.</span></span> <span data-ttu-id="4d601-106">Cette méthode implémente la méthode [**IMemInputPin :: ReceiveMultiple**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple) .</span><span class="sxs-lookup"><span data-stu-id="4d601-106">This method implements the [**IMemInputPin::ReceiveMultiple**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d601-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4d601-107">Syntax</span></span>


```C++
HRESULT ReceiveMultiple(
   IMediaSample **pSamples,
   long         nSamples,
   long         *nSamplesProcessed
);
```



## <a name="parameters"></a><span data-ttu-id="4d601-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4d601-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4d601-109">*pSamples*</span><span class="sxs-lookup"><span data-stu-id="4d601-109">*pSamples*</span></span> 
</dt> <dd>

<span data-ttu-id="4d601-110">Adresse d’un tableau de pointeurs [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) , de taille *nSamples*.</span><span class="sxs-lookup"><span data-stu-id="4d601-110">Address of an array of [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) pointers, of size *nSamples*.</span></span>

</dd> <dt>

<span data-ttu-id="4d601-111">*nSamples*</span><span class="sxs-lookup"><span data-stu-id="4d601-111">*nSamples*</span></span> 
</dt> <dd>

<span data-ttu-id="4d601-112">Nombre d’échantillons à traiter.</span><span class="sxs-lookup"><span data-stu-id="4d601-112">Number of samples to process.</span></span>

</dd> <dt>

<span data-ttu-id="4d601-113">*nSamplesProcessed*</span><span class="sxs-lookup"><span data-stu-id="4d601-113">*nSamplesProcessed*</span></span> 
</dt> <dd>

<span data-ttu-id="4d601-114">Pointeur vers une variable qui reçoit le nombre d’exemples qui ont été traités.</span><span class="sxs-lookup"><span data-stu-id="4d601-114">Pointer to a variable that receives the number of samples that were processed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4d601-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4d601-115">Return value</span></span>

<span data-ttu-id="4d601-116">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4d601-116">Returns an **HRESULT** value.</span></span> <span data-ttu-id="4d601-117">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="4d601-117">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="4d601-118">Code de retour</span><span class="sxs-lookup"><span data-stu-id="4d601-118">Return code</span></span>                                                                                             | <span data-ttu-id="4d601-119">Description</span><span class="sxs-lookup"><span data-stu-id="4d601-119">Description</span></span>                                                |
|---------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <span data-ttu-id="4d601-120"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="4d601-120"><dt>**S\_OK**</dt></span></span> </dl>                    | <span data-ttu-id="4d601-121">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="4d601-121">Success.</span></span><br/>                                        |
| <dl> <span data-ttu-id="4d601-122"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="4d601-122"><dt>**S\_FALSE**</dt></span></span> </dl>                 | <span data-ttu-id="4d601-123">Le code PIN est en cours de vidage ; l’exemple a été rejeté.</span><span class="sxs-lookup"><span data-stu-id="4d601-123">Pin is currently flushing; sample was rejected.</span></span><br/> |
| <dl> <span data-ttu-id="4d601-124"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="4d601-124"><dt>**E\_POINTER**</dt></span></span> </dl>               | <span data-ttu-id="4d601-125">Argument de pointeur **null** .</span><span class="sxs-lookup"><span data-stu-id="4d601-125">**NULL** pointer argument.</span></span><br/>                      |
| <dl> <span data-ttu-id="4d601-126"><dt>**VFW \_ E \_ INVALIDMEDIATYPE**</dt></span><span class="sxs-lookup"><span data-stu-id="4d601-126"><dt>**VFW\_E\_INVALIDMEDIATYPE**</dt></span></span> </dl> | <span data-ttu-id="4d601-127">Type de média non valide.</span><span class="sxs-lookup"><span data-stu-id="4d601-127">Invalid media type.</span></span><br/>                             |
| <dl> <span data-ttu-id="4d601-128"><dt>**\_erreur d' \_ exécution VFW E \_**</dt></span><span class="sxs-lookup"><span data-stu-id="4d601-128"><dt>**VFW\_E\_RUNTIME\_ERROR**</dt></span></span> </dl>   | <span data-ttu-id="4d601-129">Une erreur d’exécution s’est produite.</span><span class="sxs-lookup"><span data-stu-id="4d601-129">A run-time error occurred.</span></span><br/>                      |
| <dl> <span data-ttu-id="4d601-130"><dt>**VFW \_ E \_ état incorrect \_**</dt></span><span class="sxs-lookup"><span data-stu-id="4d601-130"><dt>**VFW\_E\_WRONG\_STATE**</dt></span></span> </dl>     | <span data-ttu-id="4d601-131">Le code PIN est arrêté.</span><span class="sxs-lookup"><span data-stu-id="4d601-131">The pin is stopped.</span></span><br/>                             |



 

## <a name="remarks"></a><span data-ttu-id="4d601-132">Notes</span><span class="sxs-lookup"><span data-stu-id="4d601-132">Remarks</span></span>

<span data-ttu-id="4d601-133">Cette méthode se comporte comme la méthode [**CBaseInputPin :: Receive**](cbaseinputpin-receive.md) , mais reçoit un tableau d’exemples.</span><span class="sxs-lookup"><span data-stu-id="4d601-133">This method behaves like the [**CBaseInputPin::Receive**](cbaseinputpin-receive.md) method, but receives an array of samples.</span></span> <span data-ttu-id="4d601-134">Dans la classe de base, la méthode parcourt le tableau et appelle **Receive** avec chaque exemple.</span><span class="sxs-lookup"><span data-stu-id="4d601-134">In the base class, the method loops through the array and calls **Receive** with each sample.</span></span> <span data-ttu-id="4d601-135">Substituez cette fonction si votre filtre peut traiter des lots d’exemples plus efficacement que les traiter un par un.</span><span class="sxs-lookup"><span data-stu-id="4d601-135">Override this function if your filter can process batches of samples more efficiently than processing them one at a time.</span></span>

## <a name="requirements"></a><span data-ttu-id="4d601-136">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4d601-136">Requirements</span></span>



| <span data-ttu-id="4d601-137">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4d601-137">Requirement</span></span> | <span data-ttu-id="4d601-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="4d601-138">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d601-139">En-tête</span><span class="sxs-lookup"><span data-stu-id="4d601-139">Header</span></span><br/>  | <dl> <span data-ttu-id="4d601-140"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4d601-140"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="4d601-141">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="4d601-141">Library</span></span><br/> | <dl> <span data-ttu-id="4d601-142"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="4d601-142"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4d601-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4d601-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d601-144">**CBaseInputPin, classe**</span><span class="sxs-lookup"><span data-stu-id="4d601-144">**CBaseInputPin Class**</span></span>](cbaseinputpin.md)
</dt> </dl>

 

 




