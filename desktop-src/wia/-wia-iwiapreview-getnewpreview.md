---
description: Met en cache en interne l’image non filtrée retournée par le pilote.
ms.assetid: 09cb242d-d1d6-4130-8b49-0770940471d8
title: 'IWiaPreview :: GetNewPreview, méthode (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaPreview.GetNewPreview
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: c3f1251e7ec1b98d43e616c1ff6f2b3b2aacd8b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514193"
---
# <a name="iwiapreviewgetnewpreview-method"></a><span data-ttu-id="50a91-103">IWiaPreview :: GetNewPreview, méthode</span><span class="sxs-lookup"><span data-stu-id="50a91-103">IWiaPreview::GetNewPreview method</span></span>

<span data-ttu-id="50a91-104">Met en cache en interne l’image non filtrée retournée par le pilote.</span><span class="sxs-lookup"><span data-stu-id="50a91-104">Caches internally the unfiltered image returned from the driver.</span></span>

## <a name="syntax"></a><span data-ttu-id="50a91-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="50a91-105">Syntax</span></span>


```C++
HRESULT GetNewPreview(
  [in] IWiaItem2            *pWiaItem2,
  [in] LONG                 lFlags,
  [in] IWiaTransferCallback *pWiaTransferCallback
);
```



## <a name="parameters"></a><span data-ttu-id="50a91-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="50a91-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50a91-107">*pWiaItem2* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="50a91-107">*pWiaItem2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50a91-108">Tapez : \**[**IWiaItem2**](-wia-iwiaitem2.md) \** _</span><span class="sxs-lookup"><span data-stu-id="50a91-108">Type: \**[**IWiaItem2**](-wia-iwiaitem2.md)\** _</span></span>

<span data-ttu-id="50a91-109">Spécifie un pointeur vers l’élément [_ *IWiaItem2* \*](-wia-iwiaitem2.md) pour l’image.</span><span class="sxs-lookup"><span data-stu-id="50a91-109">Specifies a pointer to the [_ *IWiaItem2*\*](-wia-iwiaitem2.md) item for the image.</span></span>

</dd> <dt>

<span data-ttu-id="50a91-110">*lFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="50a91-110">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50a91-111">Type : **long**</span><span class="sxs-lookup"><span data-stu-id="50a91-111">Type: **LONG**</span></span>

<span data-ttu-id="50a91-112">Actuellement inutilisé.</span><span class="sxs-lookup"><span data-stu-id="50a91-112">Currently unused.</span></span> <span data-ttu-id="50a91-113">Doit être défini sur zéro (0).</span><span class="sxs-lookup"><span data-stu-id="50a91-113">Should be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="50a91-114">*pWiaTransferCallback* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="50a91-114">*pWiaTransferCallback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50a91-115">Tapez : \**[**IWiaTransferCallback**](-wia-iwiatransfercallback.md) \** _</span><span class="sxs-lookup"><span data-stu-id="50a91-115">Type: \**[**IWiaTransferCallback**](-wia-iwiatransfercallback.md)\** _</span></span>

<span data-ttu-id="50a91-116">Spécifie un pointeur vers l’interface [_ *IWiaTransferCallback* \*](-wia-iwiatransfercallback.md) de l’application appelante.</span><span class="sxs-lookup"><span data-stu-id="50a91-116">Specifies a pointer to the calling application's [_ *IWiaTransferCallback*\*](-wia-iwiatransfercallback.md) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="50a91-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="50a91-117">Return value</span></span>

<span data-ttu-id="50a91-118">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="50a91-118">Type: **HRESULT**</span></span>

<span data-ttu-id="50a91-119">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="50a91-119">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="50a91-120">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="50a91-120">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="50a91-121">Notes</span><span class="sxs-lookup"><span data-stu-id="50a91-121">Remarks</span></span>

<span data-ttu-id="50a91-122">Une application doit appeler **IWiaPreview :: GetNewPreview** avant d’appeler [**IWiaPreview ::D etectregions**](-wia-iwiapreview-detectregions.md).</span><span class="sxs-lookup"><span data-stu-id="50a91-122">An application must call **IWiaPreview::GetNewPreview** before it calls [**IWiaPreview::DetectRegions**](-wia-iwiapreview-detectregions.md).</span></span>

<span data-ttu-id="50a91-123">**IWiaPreview :: GetNewPreview** définit la [**propriété \_ \_ preview DPS WIA**](-wia-wiaitempropscannerdevice.md) (et la réinitialise avant qu’elle ne soit retournée, sauf si elle a été définie auparavant).</span><span class="sxs-lookup"><span data-stu-id="50a91-123">**IWiaPreview::GetNewPreview** sets the [**WIA\_DPS\_PREVIEW**](-wia-wiaitempropscannerdevice.md) property (and resets it before it returns, unless it was set before).</span></span> <span data-ttu-id="50a91-124">Cela permet au pilote et au matériel, ainsi qu’au filtre de traitement d’image, de savoir que l’élément est une analyse de préversion.</span><span class="sxs-lookup"><span data-stu-id="50a91-124">This lets the driver and hardware, as well as the image processing filter, know that the item is a preview scan.</span></span>

<span data-ttu-id="50a91-125">En interne, le composant Windows Image Acquisition (WIA) 2,0 Preview crée une instance du filtre de traitement d’image du pilote en appelant [**GetExtension**](-wia-iwiaitem2-getextension.md) sur *pWiaItem2*.</span><span class="sxs-lookup"><span data-stu-id="50a91-125">Internally, the Windows Image Acquisition (WIA) 2.0 preview component creates an instance of the driver's image processing filter by calling [**GetExtension**](-wia-iwiaitem2-getextension.md) on *pWiaItem2*.</span></span> <span data-ttu-id="50a91-126">Le composant WIA 2,0 Preview effectue cette création lorsque l’application appelle **IWiaPreview :: GetNewPreview**.</span><span class="sxs-lookup"><span data-stu-id="50a91-126">The WIA 2.0 preview component does this when the application calls **IWiaPreview::GetNewPreview**.</span></span> <span data-ttu-id="50a91-127">Le composant WIA 2,0 Preview initialise également le filtre dans **IWiaPreview :: GetNewPreview**.</span><span class="sxs-lookup"><span data-stu-id="50a91-127">The WIA 2.0 preview component also initializes the filter in **IWiaPreview::GetNewPreview**.</span></span> <span data-ttu-id="50a91-128">La même instance de filtre est utilisée par le composant WIA 2,0 Preview lors d’un appel à [**IWiaPreview :: UpdatePreview**](-wia-iwiapreview-updatepreview.md).</span><span class="sxs-lookup"><span data-stu-id="50a91-128">The same filter instance is used by the WIA 2.0 preview component during a call to [**IWiaPreview::UpdatePreview**](-wia-iwiapreview-updatepreview.md).</span></span>

<span data-ttu-id="50a91-129">Avant d’appeler le composant WIA 2,0 Preview, une application doit appeler [**CheckExtension**](-wia-iwiaitem2-checkextension.md) pour s’assurer que le pilote est fourni avec un filtre de traitement d’image.</span><span class="sxs-lookup"><span data-stu-id="50a91-129">Before calling into the WIA 2.0 preview component, an application should call [**CheckExtension**](-wia-iwiaitem2-checkextension.md) to make sure that the driver comes with an image processing filter.</span></span> <span data-ttu-id="50a91-130">Elle doit appeler **CheckExtension** sur l’élément qu’elle transmettra à **IWiaPreview :: GetNewPreview**.</span><span class="sxs-lookup"><span data-stu-id="50a91-130">It should call **CheckExtension** on the item that it would pass to **IWiaPreview::GetNewPreview**.</span></span> <span data-ttu-id="50a91-131">Il est inutile de fournir des aperçus dynamiques sans filtre de traitement d’image.</span><span class="sxs-lookup"><span data-stu-id="50a91-131">It is useless to provide live previews without an image processing filter.</span></span> <span data-ttu-id="50a91-132">Si une application appelle **IWiaPreview :: GetNewPreview** pour un pilote sans filtre de traitement d’image, l’appel échoue.</span><span class="sxs-lookup"><span data-stu-id="50a91-132">If an application calls **IWiaPreview::GetNewPreview** for a driver without an image processing filter, the call will fail.</span></span>

## <a name="examples"></a><span data-ttu-id="50a91-133">Exemples</span><span class="sxs-lookup"><span data-stu-id="50a91-133">Examples</span></span>

<span data-ttu-id="50a91-134">CheckImgFilter vérifie si le pilote a un filtre de traitement d’image.</span><span class="sxs-lookup"><span data-stu-id="50a91-134">CheckImgFilter checks if the driver has an image processing filter.</span></span> <span data-ttu-id="50a91-135">Avant d’appeler la version préliminaire du composant, une application doit s’assurer que le pilote possède un filtre de traitement d’image.</span><span class="sxs-lookup"><span data-stu-id="50a91-135">Before calling into the preview component, an application should ensure that the driver has an image processing filter.</span></span>


```C++
HRESULT
CheckImgFilter(
   IN  IWiaItem2 *pWiaItem2,
   OUT BOOL      *pbHasImgFilter)
{
   HRESULT     hr = S_OK;

   if (!pWiaItem2 || !pbHasImgFilter)
   {
      hr = E_INVALIDARG;
   }

   if (SUCCEEDED(hr))
   {
     *pbHasImgFilter = FALSE;
   }

   if (SUCCEEDED(hr))
   {
      BSTR    bstrFilterString = SysAllocString(WIA_IMAGEPROC_FILTER_STR);

      if (bstrFilterString)
      {
         hr = pWiaItem2->CheckExtension(0,
                                        bstrFilterString,
                                        IID_IWiaSegmentationFilter,
                                        pbHasImgFilter);

         SysFreeString(bstrFilterString);
         bstrFilterString = NULL;
      }
      else
      {
         hr = E_OUTOFMEMORY;
      }
   }

   return hr;

}
```



<span data-ttu-id="50a91-136">DownloadPreviewImage télécharge les données de l’image à partir du scanneur en appelant la méthode **IWiaPreview :: GetNewPreview** du composant de prévisualisation.</span><span class="sxs-lookup"><span data-stu-id="50a91-136">DownloadPreviewImage downloads image data from the scanner by calling the preview component's **IWiaPreview::GetNewPreview** method.</span></span> <span data-ttu-id="50a91-137">Il appelle ensuite DetectSubregions si l’utilisateur de l’application souhaite appeler le filtre de segmentation, ce qui crée un élément enfant sous pWiaItem2 pour chaque région qu’il détecte.</span><span class="sxs-lookup"><span data-stu-id="50a91-137">It then calls DetectSubregions if the application user wants to invoke the segmentation filter, which creates a child item under pWiaItem2 for each region it detects.</span></span> <span data-ttu-id="50a91-138">Consultez [**DetectRegions**](-wia-iwiasegmentationfilter-detectregions.md) pour la méthode DetectSubregions utilisée dans cet exemple.</span><span class="sxs-lookup"><span data-stu-id="50a91-138">See [**DetectRegions**](-wia-iwiasegmentationfilter-detectregions.md) for the DetectSubregions method used in this example.</span></span>

<span data-ttu-id="50a91-139">Dans cet exemple, l’utilisateur de l’application définit `m_bUseSegmentationFilter` en cliquant sur une case à cocher.</span><span class="sxs-lookup"><span data-stu-id="50a91-139">In this example, the application user sets `m_bUseSegmentationFilter` by clicking a check box.</span></span> <span data-ttu-id="50a91-140">Si l’application prend en charge cette option, elle doit d’abord vérifier que le pilote possède un filtre de segmentation en appelant [**CheckExtension**](-wia-iwiaitem2-checkextension.md).</span><span class="sxs-lookup"><span data-stu-id="50a91-140">If the application supports this, it should first check that the driver has a segmentation filter by calling [**CheckExtension**](-wia-iwiaitem2-checkextension.md).</span></span> <span data-ttu-id="50a91-141">Consultez **IWiaPreview :: GetNewPreview** pour l’exemple de méthode CheckImgFilter qui montre comment effectuer cette opération.</span><span class="sxs-lookup"><span data-stu-id="50a91-141">See **IWiaPreview::GetNewPreview** for the CheckImgFilter method example that shows how this can be done.</span></span>


```C++
HRESULT
DownloadPreviewImage(
   IN IWiaItem2 *pWiaFlatbedItem2)
{
   HRESULT hr              = S_OK;
   BOOL    bHasImgFilter   = FALSE;

   IWiaTransferCallback *pAppWiaTransferCallback = NULL;

   hr = CheckImgFilter(pWiaFlatbedItem2, &bHasImgFilter)

   if (SUCCEEDED(hr))
   {
      if (bHasImgFilter)
      {
         IWiaPreview *pWiaPreview = NULL;

         // In this example, the AppWiaTransferCallback class implements 
         // the IWiaTransferCallback interface.  
         // The constructor of AppWiaTransferCallback sets the reference count to 1.
         pAppWiaTransferCallback = new AppWiaTransferCallback();

         hr = pAppWiaTransferCallback ? S_OK : E_OUTOFMEMORY;

         if (SUCCEEDED(hr))
         {
            // Acquire image from scanner
            hr = m_pWiaPreview->GetNewPreview(pWiaFlatbedItem2,
                                              0,
                                              pAppWiaTransferCallback);    
         }

         //
         // Check the application UI for whether the user wants
         // to use the segmentation filter indicated by the value 
         // of m_bUseSegmentationFilter.
         //
         // m_FlatbedPreviewStream is the stream that
         // AppWiaTransferCallback::GetNextStream returned for the
         // flatbed item.
         // This stream is where the image data is stored after
         // the successful return of GetNewPreview.
         // The stream is passed into the segmentation filter
         // for region detection.
         if (SUCCEEDED(hr) && m_bUseSegmentationFilter)
         {
            DetectSubregions(m_FlatbedPreviewStream, pWiaFlatbedItem2);
         }

         if (pAppWiaTransferCallback)
         {
            // If the call to GetNewPreview was successful, the
            // preview component calls AddRef on the callback so
            // this call doesn't delete the object.

            pAppWiaTransferCallback->Release();
         }

      }
      else
      {
         // Do not create an instance of preview component if the driver does
         // not come with an image processing filter.
         // You can use segmentation filter, however, if the driver
         // comes with one (omitted here).
      }
   }

   return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="50a91-142">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="50a91-142">Requirements</span></span>



| <span data-ttu-id="50a91-143">Condition requise</span><span class="sxs-lookup"><span data-stu-id="50a91-143">Requirement</span></span> | <span data-ttu-id="50a91-144">Valeur</span><span class="sxs-lookup"><span data-stu-id="50a91-144">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="50a91-145">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="50a91-145">Minimum supported client</span></span><br/> | <span data-ttu-id="50a91-146">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="50a91-146">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="50a91-147">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="50a91-147">Minimum supported server</span></span><br/> | <span data-ttu-id="50a91-148">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="50a91-148">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="50a91-149">En-tête</span><span class="sxs-lookup"><span data-stu-id="50a91-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="50a91-150"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="50a91-150"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="50a91-151">MIDL</span><span class="sxs-lookup"><span data-stu-id="50a91-151">IDL</span></span><br/>                      | <dl> <span data-ttu-id="50a91-152"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="50a91-152"><dt>Wia.idl</dt></span></span> </dl> |



 

 




