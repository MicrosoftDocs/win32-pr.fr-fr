---
description: 'La méthode Receive reçoit l’exemple de support suivant dans le flux. Cette méthode implémente la méthode IMemInputPin :: Receive.'
ms.assetid: 30fefc7b-7c9c-44cd-b58b-2b275dfa2520
title: CBaseInputPin. Receive, méthode (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.Receive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 10306d5568ae1754105a4367952cef82f931be99
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528397"
---
# <a name="cbaseinputpinreceive-method"></a><span data-ttu-id="e6b99-104">CBaseInputPin. Receive, méthode</span><span class="sxs-lookup"><span data-stu-id="e6b99-104">CBaseInputPin.Receive method</span></span>

<span data-ttu-id="e6b99-105">La `Receive` méthode reçoit l’échantillon de média suivant dans le flux.</span><span class="sxs-lookup"><span data-stu-id="e6b99-105">The `Receive` method receives the next media sample in the stream.</span></span> <span data-ttu-id="e6b99-106">Cette méthode implémente la méthode [**IMemInputPin :: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) .</span><span class="sxs-lookup"><span data-stu-id="e6b99-106">This method implements the [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6b99-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e6b99-107">Syntax</span></span>


```C++
HRESULT Receive(
   IMediaSample *pSample
);
```



## <a name="parameters"></a><span data-ttu-id="e6b99-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e6b99-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6b99-109">*pSample*</span><span class="sxs-lookup"><span data-stu-id="e6b99-109">*pSample*</span></span> 
</dt> <dd>

<span data-ttu-id="e6b99-110">Pointeur vers l’interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) de l’exemple.</span><span class="sxs-lookup"><span data-stu-id="e6b99-110">Pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e6b99-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e6b99-111">Return value</span></span>

<span data-ttu-id="e6b99-112">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e6b99-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="e6b99-113">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="e6b99-113">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="e6b99-114">Code de retour</span><span class="sxs-lookup"><span data-stu-id="e6b99-114">Return code</span></span>                                                                                             | <span data-ttu-id="e6b99-115">Description</span><span class="sxs-lookup"><span data-stu-id="e6b99-115">Description</span></span>                                                |
|---------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <span data-ttu-id="e6b99-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e6b99-116"><dt>**S\_OK**</dt></span></span> </dl>                    | <span data-ttu-id="e6b99-117">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="e6b99-117">Success.</span></span><br/>                                        |
| <dl> <span data-ttu-id="e6b99-118"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="e6b99-118"><dt>**S\_FALSE**</dt></span></span> </dl>                 | <span data-ttu-id="e6b99-119">Le code PIN est en cours de vidage ; l’exemple a été rejeté.</span><span class="sxs-lookup"><span data-stu-id="e6b99-119">Pin is currently flushing; sample was rejected.</span></span><br/> |
| <dl> <span data-ttu-id="e6b99-120"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="e6b99-120"><dt>**E\_POINTER**</dt></span></span> </dl>               | <span data-ttu-id="e6b99-121">Argument de pointeur **null** .</span><span class="sxs-lookup"><span data-stu-id="e6b99-121">**NULL** pointer argument.</span></span><br/>                      |
| <dl> <span data-ttu-id="e6b99-122"><dt>**VFW \_ E \_ INVALIDMEDIATYPE**</dt></span><span class="sxs-lookup"><span data-stu-id="e6b99-122"><dt>**VFW\_E\_INVALIDMEDIATYPE**</dt></span></span> </dl> | <span data-ttu-id="e6b99-123">Type de média non valide.</span><span class="sxs-lookup"><span data-stu-id="e6b99-123">Invalid media type.</span></span><br/>                             |
| <dl> <span data-ttu-id="e6b99-124"><dt>**\_erreur d' \_ exécution VFW E \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e6b99-124"><dt>**VFW\_E\_RUNTIME\_ERROR**</dt></span></span> </dl>   | <span data-ttu-id="e6b99-125">Une erreur d’exécution s’est produite.</span><span class="sxs-lookup"><span data-stu-id="e6b99-125">A run-time error occurred.</span></span><br/>                      |
| <dl> <span data-ttu-id="e6b99-126"><dt>**VFW \_ E \_ état incorrect \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e6b99-126"><dt>**VFW\_E\_WRONG\_STATE**</dt></span></span> </dl>     | <span data-ttu-id="e6b99-127">Le code PIN est arrêté.</span><span class="sxs-lookup"><span data-stu-id="e6b99-127">The pin is stopped.</span></span><br/>                             |



 

## <a name="remarks"></a><span data-ttu-id="e6b99-128">Notes</span><span class="sxs-lookup"><span data-stu-id="e6b99-128">Remarks</span></span>

<span data-ttu-id="e6b99-129">La broche de sortie en amont appelle cette méthode pour remettre un échantillon à la broche d’entrée.</span><span class="sxs-lookup"><span data-stu-id="e6b99-129">The upstream output pin calls this method to deliver a sample to the input pin.</span></span> <span data-ttu-id="e6b99-130">La broche d’entrée doit effectuer l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="e6b99-130">The input pin must do one of the following:</span></span>

-   <span data-ttu-id="e6b99-131">Traitez l’exemple avant de retourner.</span><span class="sxs-lookup"><span data-stu-id="e6b99-131">Process the sample before returning.</span></span>
-   <span data-ttu-id="e6b99-132">Retourner et traiter l’exemple dans un thread de travail.</span><span class="sxs-lookup"><span data-stu-id="e6b99-132">Return, and process the sample in a worker thread.</span></span>
-   <span data-ttu-id="e6b99-133">Rejetez l’exemple.</span><span class="sxs-lookup"><span data-stu-id="e6b99-133">Reject the sample.</span></span>

<span data-ttu-id="e6b99-134">Si le code confidentiel utilise un thread de travail pour traiter l’exemple, ajoutez un décompte de références à l’exemple à l’intérieur de cette méthode.</span><span class="sxs-lookup"><span data-stu-id="e6b99-134">If the pin uses a worker thread to process the sample, add a reference count to the sample inside this method.</span></span> <span data-ttu-id="e6b99-135">Une fois la méthode retournée, la broche amont libère l’exemple.</span><span class="sxs-lookup"><span data-stu-id="e6b99-135">After the method returns, the upstream pin releases the sample.</span></span> <span data-ttu-id="e6b99-136">Lorsque le nombre de références de l’exemple atteint zéro, l’exemple retourne à l’allocateur pour une réutilisation.</span><span class="sxs-lookup"><span data-stu-id="e6b99-136">When the sample's reference count reaches zero, the sample returns to the allocator for re-use.</span></span>

<span data-ttu-id="e6b99-137">Cette méthode est synchrone et peut se bloquer.</span><span class="sxs-lookup"><span data-stu-id="e6b99-137">This method is synchronous and can block.</span></span> <span data-ttu-id="e6b99-138">Si la méthode peut être bloquée, la méthode [**CBaseInputPin :: ReceiveCanBlock**](cbaseinputpin-receivecanblock.md) du pin doit retourner s \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e6b99-138">If the method might block, the pin's [**CBaseInputPin::ReceiveCanBlock**](cbaseinputpin-receivecanblock.md) method should return S\_OK.</span></span>

<span data-ttu-id="e6b99-139">Dans la classe de base, cette méthode effectue les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="e6b99-139">In the base class, this method performs the following steps:</span></span>

1.  <span data-ttu-id="e6b99-140">Appelle la méthode [**CBaseInputPin :: CheckStreaming**](cbaseinputpin-checkstreaming.md) pour vérifier que le code confidentiel peut traiter des exemples maintenant.</span><span class="sxs-lookup"><span data-stu-id="e6b99-140">Calls the [**CBaseInputPin::CheckStreaming**](cbaseinputpin-checkstreaming.md) method to verify that the pin can process samples now.</span></span> <span data-ttu-id="e6b99-141">Si tel n’est pas le cas, par exemple, si le code PIN est arrêté, la méthode échoue.</span><span class="sxs-lookup"><span data-stu-id="e6b99-141">If it cannot for example, if the pin is stopped the method fails.</span></span>
2.  <span data-ttu-id="e6b99-142">Récupère les exemples de propriétés et vérifie si le format a changé (voir ci-dessous).</span><span class="sxs-lookup"><span data-stu-id="e6b99-142">Retrieves the sample properties and checks whether the format has changed (see below).</span></span>
3.  <span data-ttu-id="e6b99-143">Si le format a changé, la méthode appelle la méthode [**CBasePin :: CheckMediaType**](cbasepin-checkmediatype.md) pour déterminer si le nouveau format est acceptable.</span><span class="sxs-lookup"><span data-stu-id="e6b99-143">If the format has changed, the method calls the [**CBasePin::CheckMediaType**](cbasepin-checkmediatype.md) method to determine whether the new format is acceptable.</span></span>
4.  <span data-ttu-id="e6b99-144">Si le nouveau format n’est pas acceptable, la méthode appelle la méthode [**CBasePin :: EndOfStream**](cbasepin-endofstream.md) , publie un \_ événement EC ERRORABORT et retourne un code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="e6b99-144">If the new format is not acceptable, the method calls the [**CBasePin::EndOfStream**](cbasepin-endofstream.md) method, posts an EC\_ERRORABORT event, and returns an error code.</span></span>
5.  <span data-ttu-id="e6b99-145">En supposant qu’il n’y avait pas d’erreur, la méthode retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e6b99-145">Assuming there were no errors, the method returns S\_OK.</span></span>

<span data-ttu-id="e6b99-146">Testez une modification de format comme suit :</span><span class="sxs-lookup"><span data-stu-id="e6b99-146">Test for a format change as follows:</span></span>

-   <span data-ttu-id="e6b99-147">Si l’exemple prend en charge l’interface [**IMediaSample2**](/windows/desktop/api/Strmif/nn-strmif-imediasample2) , vérifiez le membre **dwSampleFlags** de la structure de [**\_ \_ Propriétés am SAMPLE2**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) .</span><span class="sxs-lookup"><span data-stu-id="e6b99-147">If the sample supports the [**IMediaSample2**](/windows/desktop/api/Strmif/nn-strmif-imediasample2) interface, check the **dwSampleFlags** member of the [**AM\_SAMPLE2\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) structure.</span></span> <span data-ttu-id="e6b99-148">Si l' \_ indicateur AM Sample \_ TYPECHANGED est présent, le format a changé.</span><span class="sxs-lookup"><span data-stu-id="e6b99-148">If the AM\_SAMPLE\_TYPECHANGED flag is present, the format has changed.</span></span>
-   <span data-ttu-id="e6b99-149">Sinon, si l’exemple ne prend pas en charge **IMediaSample2**, appelez la méthode [**IMediaSample :: GetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype) .</span><span class="sxs-lookup"><span data-stu-id="e6b99-149">Otherwise, if the sample does not support **IMediaSample2**, call the [**IMediaSample::GetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype) method.</span></span> <span data-ttu-id="e6b99-150">Si la méthode retourne une valeur non **null** , le format a changé.</span><span class="sxs-lookup"><span data-stu-id="e6b99-150">If the method returns a non-**NULL** value, the format has changed.</span></span>

<span data-ttu-id="e6b99-151">Dans la classe de base, cette méthode ne traite pas l’exemple.</span><span class="sxs-lookup"><span data-stu-id="e6b99-151">In the base class, this method does not process the sample.</span></span> <span data-ttu-id="e6b99-152">La classe dérivée doit substituer cette méthode pour effectuer le traitement.</span><span class="sxs-lookup"><span data-stu-id="e6b99-152">The derived class must override this method to perform the processing.</span></span> <span data-ttu-id="e6b99-153">(Ce que cela implique dépend entièrement du filtre.) La classe dérivée doit appeler la méthode de classe de base pour rechercher les erreurs décrites précédemment.</span><span class="sxs-lookup"><span data-stu-id="e6b99-153">(What this entails depends entirely on the filter.) The derived class should call the base-class method, to check for the errors described previously.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6b99-154">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e6b99-154">Requirements</span></span>



| <span data-ttu-id="e6b99-155">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e6b99-155">Requirement</span></span> | <span data-ttu-id="e6b99-156">Valeur</span><span class="sxs-lookup"><span data-stu-id="e6b99-156">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6b99-157">En-tête</span><span class="sxs-lookup"><span data-stu-id="e6b99-157">Header</span></span><br/>  | <dl> <span data-ttu-id="e6b99-158"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e6b99-158"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="e6b99-159">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="e6b99-159">Library</span></span><br/> | <dl> <span data-ttu-id="e6b99-160"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="e6b99-160"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e6b99-161">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e6b99-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6b99-162">**CBaseInputPin, classe**</span><span class="sxs-lookup"><span data-stu-id="e6b99-162">**CBaseInputPin Class**</span></span>](cbaseinputpin.md)
</dt> </dl>

 

 




