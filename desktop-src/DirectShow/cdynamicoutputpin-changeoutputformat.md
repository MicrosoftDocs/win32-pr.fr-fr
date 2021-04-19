---
description: La méthode ChangeOutputFormat modifie dynamiquement le type de média pour la connexion et fournit de nouvelles informations de segment.
ms.assetid: d1204ca0-a489-48a0-8fe5-3ade04f51c93
title: Méthode CDynamicOutputPin. ChangeOutputFormat (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.ChangeOutputFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 57421b2fd9624d9798037151a5656343e386a497
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526884"
---
# <a name="cdynamicoutputpinchangeoutputformat-method"></a><span data-ttu-id="9c988-103">Méthode CDynamicOutputPin. ChangeOutputFormat</span><span class="sxs-lookup"><span data-stu-id="9c988-103">CDynamicOutputPin.ChangeOutputFormat method</span></span>

<span data-ttu-id="9c988-104">La `ChangeOutputFormat` méthode modifie dynamiquement le type de média pour la connexion et fournit de nouvelles informations de segment.</span><span class="sxs-lookup"><span data-stu-id="9c988-104">The `ChangeOutputFormat` method dynamically changes the media type for the connection, and delivers new segment information.</span></span> <span data-ttu-id="9c988-105">La modification peut se produire pendant l’exécution du graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="9c988-105">The change can occur while the filter graph is running.</span></span> <span data-ttu-id="9c988-106">Une fois cette méthode appelée, les exemples avec l’ancien type de média ne peuvent pas être remis.</span><span class="sxs-lookup"><span data-stu-id="9c988-106">Once this method is called, samples with the old media type cannot be delivered.</span></span> <span data-ttu-id="9c988-107">L’appelant doit s’assurer qu’aucun ancien échantillon n’est en attente.</span><span class="sxs-lookup"><span data-stu-id="9c988-107">The caller must ensure that no old samples are pending.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c988-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9c988-108">Syntax</span></span>


```C++
HRESULT ChangeOutputFormat(
   const AM_MEDIA_TYPE  *pmt,
         REFERENCE_TIME tSegmentStart,
         REFERENCE_TIME tSegmentStop,
         double         dSegmentRate
);
```



## <a name="parameters"></a><span data-ttu-id="9c988-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9c988-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9c988-110">*crédit*</span><span class="sxs-lookup"><span data-stu-id="9c988-110">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="9c988-111">Pointeur vers une structure de [**\_ \_ type de média am**](/windows/win32/api/strmif/ns-strmif-am_media_type) qui spécifie le type de média.</span><span class="sxs-lookup"><span data-stu-id="9c988-111">Pointer to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure that specifies the media type.</span></span>

</dd> <dt>

<span data-ttu-id="9c988-112">*tSegmentStart*</span><span class="sxs-lookup"><span data-stu-id="9c988-112">*tSegmentStart*</span></span> 
</dt> <dd>

<span data-ttu-id="9c988-113">Heure de début du segment.</span><span class="sxs-lookup"><span data-stu-id="9c988-113">Start time of the segment.</span></span>

</dd> <dt>

<span data-ttu-id="9c988-114">*tSegmentStop*</span><span class="sxs-lookup"><span data-stu-id="9c988-114">*tSegmentStop*</span></span> 
</dt> <dd>

<span data-ttu-id="9c988-115">Heure d’arrêt du segment.</span><span class="sxs-lookup"><span data-stu-id="9c988-115">Stop time of the segment.</span></span>

</dd> <dt>

<span data-ttu-id="9c988-116">*dSegmentRate*</span><span class="sxs-lookup"><span data-stu-id="9c988-116">*dSegmentRate*</span></span> 
</dt> <dd>

<span data-ttu-id="9c988-117">Taux de segment.</span><span class="sxs-lookup"><span data-stu-id="9c988-117">Segment rate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9c988-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9c988-118">Return value</span></span>

<span data-ttu-id="9c988-119">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="9c988-119">Returns an **HRESULT** value.</span></span> <span data-ttu-id="9c988-120">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="9c988-120">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="9c988-121">Code de retour</span><span class="sxs-lookup"><span data-stu-id="9c988-121">Return code</span></span>                                                                                           | <span data-ttu-id="9c988-122">Description</span><span class="sxs-lookup"><span data-stu-id="9c988-122">Description</span></span>                                                                                                                              |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9c988-123"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="9c988-123"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="9c988-124">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="9c988-124">Success.</span></span><br/>                                                                                                                      |
| <dl> <span data-ttu-id="9c988-125"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="9c988-125"><dt>**E\_FAIL**</dt></span></span> </dl>                | <span data-ttu-id="9c988-126">Échec.</span><span class="sxs-lookup"><span data-stu-id="9c988-126">Failure.</span></span> <span data-ttu-id="9c988-127">Le filtre propriétaire n’a peut-être pas appelé [**CDynamicOutputPin :: SetConfigInfo**](cdynamicoutputpin-setconfiginfo.md).</span><span class="sxs-lookup"><span data-stu-id="9c988-127">Possibly the owning filter did not call [**CDynamicOutputPin::SetConfigInfo**](cdynamicoutputpin-setconfiginfo.md).</span></span><br/> |
| <dl> <span data-ttu-id="9c988-128"><dt>**VFW \_ E \_ non \_ connecté**</dt></span><span class="sxs-lookup"><span data-stu-id="9c988-128"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="9c988-129">Le pin n’est pas connecté.</span><span class="sxs-lookup"><span data-stu-id="9c988-129">The pin is not connected.</span></span><br/>                                                                                                     |



 

## <a name="remarks"></a><span data-ttu-id="9c988-130">Notes</span><span class="sxs-lookup"><span data-stu-id="9c988-130">Remarks</span></span>

<span data-ttu-id="9c988-131">Cette méthode modifie le type de format pendant que le filtre est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="9c988-131">This method changes the format type while the filter is running.</span></span> <span data-ttu-id="9c988-132">Si le code pin en aval accepte le nouveau format, aucune reconnexion n’est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="9c988-132">If the downstream pin accepts the new format, no reconnection is necessary.</span></span> <span data-ttu-id="9c988-133">Dans le cas contraire, la méthode tente de reconnecter le code confidentiel.</span><span class="sxs-lookup"><span data-stu-id="9c988-133">Otherwise, the method attempts to reconnect the pin.</span></span> <span data-ttu-id="9c988-134">Si la méthode modifie correctement le format, il remet les nouvelles informations sur le segment.</span><span class="sxs-lookup"><span data-stu-id="9c988-134">If the method successfully changes the format, it delivers the new segment information.</span></span> <span data-ttu-id="9c988-135">Cette méthode appelle la méthode [**CDynamicOutputPin :: ChangeMediaType**](cdynamicoutputpin-changemediatype.md) pour effectuer la modification de format.</span><span class="sxs-lookup"><span data-stu-id="9c988-135">This method calls the [**CDynamicOutputPin::ChangeMediaType**](cdynamicoutputpin-changemediatype.md) method to perform the format change.</span></span>

<span data-ttu-id="9c988-136">Vous devez appeler la méthode [**CDynamicOutputPin :: StartUsingOutputPin**](cdynamicoutputpin-startusingoutputpin.md) avant d’appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="9c988-136">You must call the [**CDynamicOutputPin::StartUsingOutputPin**](cdynamicoutputpin-startusingoutputpin.md) method before calling this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="9c988-137">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9c988-137">Requirements</span></span>



| <span data-ttu-id="9c988-138">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9c988-138">Requirement</span></span> | <span data-ttu-id="9c988-139">Valeur</span><span class="sxs-lookup"><span data-stu-id="9c988-139">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9c988-140">En-tête</span><span class="sxs-lookup"><span data-stu-id="9c988-140">Header</span></span><br/>  | <dl> <span data-ttu-id="9c988-141"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9c988-141"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="9c988-142">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="9c988-142">Library</span></span><br/> | <dl> <span data-ttu-id="9c988-143"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="9c988-143"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9c988-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9c988-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c988-145">**CDynamicOutputPin, classe**</span><span class="sxs-lookup"><span data-stu-id="9c988-145">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




