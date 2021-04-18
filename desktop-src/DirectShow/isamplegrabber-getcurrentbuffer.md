---
description: La méthode GetCurrentBuffer récupère une copie de la mémoire tampon associée à l’exemple le plus récent.
ms.assetid: 08550c82-4711-4725-9cd0-19b43cf4c92e
title: 'ISampleGrabber :: GetCurrentBuffer, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabber.GetCurrentBuffer
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: d4df4c825761b42533590f10432bf62e5e4e0298
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543255"
---
# <a name="isamplegrabbergetcurrentbuffer-method"></a><span data-ttu-id="f03d8-103">ISampleGrabber :: GetCurrentBuffer, méthode</span><span class="sxs-lookup"><span data-stu-id="f03d8-103">ISampleGrabber::GetCurrentBuffer method</span></span>

> [!Note]  
> <span data-ttu-id="f03d8-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="f03d8-104">\[Deprecated.</span></span> <span data-ttu-id="f03d8-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="f03d8-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="f03d8-106">La méthode **GetCurrentBuffer** récupère une copie de la mémoire tampon associée à l’exemple le plus récent.</span><span class="sxs-lookup"><span data-stu-id="f03d8-106">The **GetCurrentBuffer** method retrieves a copy of the buffer associated with the most recent sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="f03d8-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f03d8-107">Syntax</span></span>


```C++
HRESULT GetCurrentBuffer(
  [in, out] long *pBufferSize,
  [out]     long *pBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="f03d8-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f03d8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f03d8-109">*pBufferSize* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="f03d8-109">*pBufferSize* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f03d8-110">Pointeur vers la taille de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="f03d8-110">Pointer to the size of the buffer.</span></span> <span data-ttu-id="f03d8-111">Si *pbuffer* a la **valeur null**, ce paramètre reçoit la taille de mémoire tampon requise, en octets.</span><span class="sxs-lookup"><span data-stu-id="f03d8-111">If *pBuffer* is **NULL**, this parameter receives the required buffer size, in bytes.</span></span> <span data-ttu-id="f03d8-112">Si *pbuffer* n’a pas la **valeur null**, définissez ce paramètre sur la taille de la mémoire tampon, en octets.</span><span class="sxs-lookup"><span data-stu-id="f03d8-112">If *pBuffer* is not **NULL**, set this parameter equal to the size of the buffer, in bytes.</span></span> <span data-ttu-id="f03d8-113">Lors de la sortie, le paramètre reçoit le nombre d’octets qui ont été copiés dans la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="f03d8-113">On output, the parameter receives the number of bytes that were copied into the buffer.</span></span> <span data-ttu-id="f03d8-114">Cette valeur peut être inférieure à la taille de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="f03d8-114">This value might be smaller than the size of the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="f03d8-115">*pbuffer* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="f03d8-115">*pBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f03d8-116">Pointeur vers un tableau d’octets de taille *pBufferSize* ou **null**.</span><span class="sxs-lookup"><span data-stu-id="f03d8-116">Pointer to an array of bytes of size *pBufferSize*, or **NULL**.</span></span> <span data-ttu-id="f03d8-117">Si ce paramètre n’est pas **null**, la mémoire tampon en cours est copiée dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="f03d8-117">If this parameter is not **NULL**, the current buffer is copied into the array.</span></span> <span data-ttu-id="f03d8-118">Si ce paramètre a la **valeur null**, le paramètre *pBufferSize* reçoit la taille de mémoire tampon requise.</span><span class="sxs-lookup"><span data-stu-id="f03d8-118">If this parameter is **NULL**, the *pBufferSize* parameter receives the required buffer size.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f03d8-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f03d8-119">Return value</span></span>

<span data-ttu-id="f03d8-120">Retourne l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="f03d8-120">Returns one of the following values.</span></span>



| <span data-ttu-id="f03d8-121">Code de retour</span><span class="sxs-lookup"><span data-stu-id="f03d8-121">Return code</span></span>                                                                                           | <span data-ttu-id="f03d8-122">Description</span><span class="sxs-lookup"><span data-stu-id="f03d8-122">Description</span></span>                                                                                                                  |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f03d8-123"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="f03d8-123"><dt>**E\_INVALIDARG**</dt></span></span> </dl>          | <span data-ttu-id="f03d8-124">Les exemples ne sont pas mis en mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="f03d8-124">Samples are not being buffered.</span></span> <span data-ttu-id="f03d8-125">Appelez [**ISampleGrabber :: SetBufferSamples**](isamplegrabber-setbuffersamples.md).</span><span class="sxs-lookup"><span data-stu-id="f03d8-125">Call [**ISampleGrabber::SetBufferSamples**](isamplegrabber-setbuffersamples.md).</span></span><br/> |
| <dl> <span data-ttu-id="f03d8-126"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="f03d8-126"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>         | <span data-ttu-id="f03d8-127">La mémoire tampon spécifiée n’est pas assez grande.</span><span class="sxs-lookup"><span data-stu-id="f03d8-127">The specified buffer is not large enough.</span></span><br/>                                                                         |
| <dl> <span data-ttu-id="f03d8-128"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="f03d8-128"><dt>**E\_POINTER**</dt></span></span> </dl>             | <span data-ttu-id="f03d8-129">Argument de pointeur **null** .</span><span class="sxs-lookup"><span data-stu-id="f03d8-129">**NULL** pointer argument.</span></span><br/>                                                                                        |
| <dl> <span data-ttu-id="f03d8-130"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f03d8-130"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="f03d8-131">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="f03d8-131">Success.</span></span><br/>                                                                                                          |
| <dl> <span data-ttu-id="f03d8-132"><dt>**VFW \_ E \_ non \_ connecté**</dt></span><span class="sxs-lookup"><span data-stu-id="f03d8-132"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="f03d8-133">Le filtre n’est pas connecté.</span><span class="sxs-lookup"><span data-stu-id="f03d8-133">The filter is not connected.</span></span><br/>                                                                                      |
| <dl> <span data-ttu-id="f03d8-134"><dt>**VFW \_ E \_ état incorrect \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f03d8-134"><dt>**VFW\_E\_WRONG\_STATE**</dt></span></span> </dl>   | <span data-ttu-id="f03d8-135">Le filtre n’a pas encore reçu d’exemples.</span><span class="sxs-lookup"><span data-stu-id="f03d8-135">The filter has not received any samples yet.</span></span> <span data-ttu-id="f03d8-136">Pour remettre un exemple, exécutez ou suspendez le graphique.</span><span class="sxs-lookup"><span data-stu-id="f03d8-136">To deliver a sample, run or pause the graph.</span></span><br/>                         |



 

## <a name="remarks"></a><span data-ttu-id="f03d8-137">Notes</span><span class="sxs-lookup"><span data-stu-id="f03d8-137">Remarks</span></span>

<span data-ttu-id="f03d8-138">Pour activer la mise en mémoire tampon, appelez [**ISampleGrabber :: SetBufferSamples**](isamplegrabber-setbuffersamples.md) avec la valeur **true**.</span><span class="sxs-lookup"><span data-stu-id="f03d8-138">To activate buffering, call [**ISampleGrabber::SetBufferSamples**](isamplegrabber-setbuffersamples.md) with a value of **TRUE**.</span></span>

<span data-ttu-id="f03d8-139">Appelez cette méthode deux fois.</span><span class="sxs-lookup"><span data-stu-id="f03d8-139">Call this method twice.</span></span> <span data-ttu-id="f03d8-140">Lors du premier appel, affectez à *pbuffer* la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="f03d8-140">On the first call, set *pBuffer* to **NULL**.</span></span> <span data-ttu-id="f03d8-141">La taille de la mémoire tampon est retournée dans *pBufferSize*.</span><span class="sxs-lookup"><span data-stu-id="f03d8-141">The size of the buffer is returned in *pBufferSize*.</span></span> <span data-ttu-id="f03d8-142">Allouez ensuite un tableau et rappelez la méthode.</span><span class="sxs-lookup"><span data-stu-id="f03d8-142">Then allocate an array and call the method again.</span></span> <span data-ttu-id="f03d8-143">Lors du deuxième appel, transmettez la taille du tableau dans *pBufferSize* et transmettez l’adresse du tableau dans *pbuffer*.</span><span class="sxs-lookup"><span data-stu-id="f03d8-143">On the second call, pass the size of the array in *pBufferSize*, and pass the address of the array in *pBuffer*.</span></span> <span data-ttu-id="f03d8-144">Si le tableau n’est pas assez grand, la méthode retourne E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="f03d8-144">If the array is not large enough, the method returns E\_OUTOFMEMORY.</span></span>

<span data-ttu-id="f03d8-145">Le paramètre *pbuffer* est typé comme pointeur **long** , mais le contenu de la mémoire tampon dépend du format des données.</span><span class="sxs-lookup"><span data-stu-id="f03d8-145">The *pBuffer* parameter is typed as a **long** pointer, but the contents of the buffer depend on the format of the data.</span></span> <span data-ttu-id="f03d8-146">Appelez [**ISampleGrabber :: GetConnectedMediaType**](isamplegrabber-getconnectedmediatype.md) pour accéder au type de média du format.</span><span class="sxs-lookup"><span data-stu-id="f03d8-146">Call [**ISampleGrabber::GetConnectedMediaType**](isamplegrabber-getconnectedmediatype.md) to get the media type of the format.</span></span>

<span data-ttu-id="f03d8-147">N’appelez pas cette méthode pendant que le graphique de filtre est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="f03d8-147">Do not call this method while the filter graph is running.</span></span> <span data-ttu-id="f03d8-148">Lorsque le graphique de filtre est en cours d’exécution, le filtre d’accrochage remplace le contenu de la mémoire tampon à chaque fois qu’il reçoit un nouvel exemple.</span><span class="sxs-lookup"><span data-stu-id="f03d8-148">While the filter graph is running, the Sample Grabber filter overwrites the contents of the buffer whenever it receives a new sample.</span></span> <span data-ttu-id="f03d8-149">La meilleure façon d’utiliser cette méthode consiste à utiliser le « mode à une seule capture », qui arrête le graphique après avoir reçu le premier exemple.</span><span class="sxs-lookup"><span data-stu-id="f03d8-149">The best way to use this method is to use "one-shot mode," which stops the graph after receiving the first sample.</span></span> <span data-ttu-id="f03d8-150">Pour définir le mode d’une seule capture, appelez [**ISampleGrabber :: SetOneShot**](isamplegrabber-setoneshot.md).</span><span class="sxs-lookup"><span data-stu-id="f03d8-150">To set one-shot mode, call [**ISampleGrabber::SetOneShot**](isamplegrabber-setoneshot.md).</span></span>

<span data-ttu-id="f03d8-151">Le filtre ne met pas en mémoire tampon des exemples de préroll, ou des exemples dans lesquels le membre **dwStreamId** de la structure de [**\_ \_ Propriétés am SAMPLE2**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) est autre chose que le \_ média de flux \_ .</span><span class="sxs-lookup"><span data-stu-id="f03d8-151">The filter does not buffer preroll samples, or samples in which the **dwStreamId** member of the [**AM\_SAMPLE2\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) structure is anything other than AM\_STREAM\_MEDIA.</span></span>

> [!Note]  
> <span data-ttu-id="f03d8-152">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="f03d8-152">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="f03d8-153">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="f03d8-153">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="f03d8-154">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="f03d8-154">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f03d8-155">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f03d8-155">Requirements</span></span>



| <span data-ttu-id="f03d8-156">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f03d8-156">Requirement</span></span> | <span data-ttu-id="f03d8-157">Valeur</span><span class="sxs-lookup"><span data-stu-id="f03d8-157">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f03d8-158">En-tête</span><span class="sxs-lookup"><span data-stu-id="f03d8-158">Header</span></span><br/>  | <dl> <span data-ttu-id="f03d8-159"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="f03d8-159"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="f03d8-160">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f03d8-160">Library</span></span><br/> | <dl> <span data-ttu-id="f03d8-161"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f03d8-161"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f03d8-162">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f03d8-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f03d8-163">Utilisation de l’exemple d’accrochage</span><span class="sxs-lookup"><span data-stu-id="f03d8-163">Using the Sample Grabber</span></span>](using-the-sample-grabber.md)
</dt> <dt>

[<span data-ttu-id="f03d8-164">**Interface ISampleGrabber**</span><span class="sxs-lookup"><span data-stu-id="f03d8-164">**ISampleGrabber Interface**</span></span>](isamplegrabber.md)
</dt> </dl>

 

 




