---
description: Détermine les sous-régions d’une image disposées sur le plateau à plat afin que chacune des sous-régions puisse être acquise dans un élément d’image séparé.
ms.assetid: 899d61f0-2dd8-4a68-827e-89e85ebb5143
title: IWiaSegmentationFilter ::D méthode etectRegions (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaSegmentationFilter.DetectRegions
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 94fe2f5076e9ff7cc0de0f7c916f6edacf2d03fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113299"
---
# <a name="iwiasegmentationfilterdetectregions-method"></a><span data-ttu-id="cc1df-103">IWiaSegmentationFilter ::D méthode etectRegions</span><span class="sxs-lookup"><span data-stu-id="cc1df-103">IWiaSegmentationFilter::DetectRegions method</span></span>

<span data-ttu-id="cc1df-104">Détermine les sous-régions d’une image disposées sur le plateau à plat afin que chacune des sous-régions puisse être acquise dans un élément d’image séparé.</span><span class="sxs-lookup"><span data-stu-id="cc1df-104">Determines the sub-regions of an image laid out on the flatbed platen so that each of sub-region can be acquired into a separate image item.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc1df-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cc1df-105">Syntax</span></span>


```C++
HRESULT DetectRegions(
  [in] LONG      lFlags,
  [in] IStream   *pInputStream,
  [in] IWiaItem2 *pWiaItem2
);
```



## <a name="parameters"></a><span data-ttu-id="cc1df-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cc1df-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc1df-107">*lFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cc1df-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc1df-108">Type : **long**</span><span class="sxs-lookup"><span data-stu-id="cc1df-108">Type: **LONG**</span></span>

<span data-ttu-id="cc1df-109">Actuellement inutilisé.</span><span class="sxs-lookup"><span data-stu-id="cc1df-109">Currently unused.</span></span> <span data-ttu-id="cc1df-110">Doit être défini sur zéro (0).</span><span class="sxs-lookup"><span data-stu-id="cc1df-110">Should be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="cc1df-111">*pInputStream* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cc1df-111">*pInputStream* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc1df-112">Type : \**[IStream](/windows/win32/api/objidl/nn-objidl-istream) \** _</span><span class="sxs-lookup"><span data-stu-id="cc1df-112">Type: \**[IStream](/windows/win32/api/objidl/nn-objidl-istream)\** _</span></span>

<span data-ttu-id="cc1df-113">Spécifie un pointeur vers l’image [IStream](/windows/win32/api/objidl/nn-objidl-istream) preview.</span><span class="sxs-lookup"><span data-stu-id="cc1df-113">Specifies a pointer to the [IStream](/windows/win32/api/objidl/nn-objidl-istream) preview image.</span></span>

</dd> <dt>

<span data-ttu-id="cc1df-114">_pWiaItem2 \* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cc1df-114">_pWiaItem2\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc1df-115">Tapez : \**[**IWiaItem2**](-wia-iwiaitem2.md) \** _</span><span class="sxs-lookup"><span data-stu-id="cc1df-115">Type: \**[**IWiaItem2**](-wia-iwiaitem2.md)\** _</span></span>

<span data-ttu-id="cc1df-116">Spécifie un pointeur vers l’élément [_ *IWiaItem2* \*](-wia-iwiaitem2.md) pour lequel *pInputStream* a été acquis.</span><span class="sxs-lookup"><span data-stu-id="cc1df-116">Specifies a pointer to the [_ *IWiaItem2*\*](-wia-iwiaitem2.md) item for which *pInputStream* was acquired.</span></span> <span data-ttu-id="cc1df-117">Le filtre de segmentation crée des éléments enfants pour cet élément.</span><span class="sxs-lookup"><span data-stu-id="cc1df-117">The segmentation filter creates child items for this item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cc1df-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="cc1df-118">Return value</span></span>

<span data-ttu-id="cc1df-119">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="cc1df-119">Type: **HRESULT**</span></span>

<span data-ttu-id="cc1df-120">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="cc1df-120">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="cc1df-121">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="cc1df-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="cc1df-122">Notes</span><span class="sxs-lookup"><span data-stu-id="cc1df-122">Remarks</span></span>

<span data-ttu-id="cc1df-123">Cette méthode détermine les sous-régions de l’image représentée par pInputStream.</span><span class="sxs-lookup"><span data-stu-id="cc1df-123">This method determines the sub-regions of the image represented by pInputStream.</span></span> <span data-ttu-id="cc1df-124">Pour chaque sous-région qu’il détecte, il crée un élément enfant pour l’élément [**IWiaItem2**](-wia-iwiaitem2.md) spécifié dans le paramètre *pWiaItem2* .</span><span class="sxs-lookup"><span data-stu-id="cc1df-124">For each sub-region that it detects, it creates a child item for the [**IWiaItem2**](-wia-iwiaitem2.md) item specified in the *pWiaItem2* parameter.</span></span> <span data-ttu-id="cc1df-125">Pour chaque élément enfant, le filtre de segmentation doit définir des valeurs pour le rectangle englobant de la zone à analyser, à l’aide des [**constantes de propriété d’élément WIA du scanneur**](-wia-wiaitempropscanneritem.md)suivantes.</span><span class="sxs-lookup"><span data-stu-id="cc1df-125">For each child item, the segmentation filter must set values for the bounding rectangle of the area to scan, using the following [**Scanner WIA Item Property Constants**](-wia-wiaitempropscanneritem.md).</span></span>

-   [<span data-ttu-id="cc1df-126">**\_adresses IP WIA, \_ xpos**</span><span class="sxs-lookup"><span data-stu-id="cc1df-126">**WIA\_IPS\_XPOS**</span></span>](-wia-wiaitempropscanneritem.md)
-   [<span data-ttu-id="cc1df-127">**\_Posy IPS \_ WIA**</span><span class="sxs-lookup"><span data-stu-id="cc1df-127">**WIA\_IPS\_YPOS**</span></span>](-wia-wiaitempropscanneritem.md)
-   [<span data-ttu-id="cc1df-128">**\_XEXTENT IPS \_ WIA**</span><span class="sxs-lookup"><span data-stu-id="cc1df-128">**WIA\_IPS\_XEXTENT**</span></span>](-wia-wiaitempropscanneritem.md)
-   [<span data-ttu-id="cc1df-129">**\_YEXTENT IPS \_ WIA**</span><span class="sxs-lookup"><span data-stu-id="cc1df-129">**WIA\_IPS\_YEXTENT**</span></span>](-wia-wiaitempropscanneritem.md)

<span data-ttu-id="cc1df-130">Un filtre plus avancé peut également nécessiter d’autres [**constantes de propriété d’élément de scanneur WIA**](-wia-wiaitempropscanneritem.md) , telles que la suppression d’une déformation des adresses IP WIA **\_ \_ \_ X** et les **adresses IP WIA avec la \_ \_ réalignement \_ Y**, si le pilote prend en charge l’annulation de l’inclinaison.</span><span class="sxs-lookup"><span data-stu-id="cc1df-130">A more advanced filter may also require other [**Scanner WIA Item Property Constants**](-wia-wiaitempropscanneritem.md) such as **WIA\_IPS\_DESKEW\_X** and **WIA\_IPS\_DESKEW\_Y**, if the driver supports de-skewing.</span></span>

<span data-ttu-id="cc1df-131">Si l’application appelle **IWiaSegmentationFilter ::D etectregions** plusieurs fois, l’application doit d’abord supprimer les éléments enfants créés par le dernier appel à **IWiaSegmentationFilter ::D etectregions**.</span><span class="sxs-lookup"><span data-stu-id="cc1df-131">If the application calls **IWiaSegmentationFilter::DetectRegions** more than once, the application must first delete the child items created by the last call to **IWiaSegmentationFilter::DetectRegions**.</span></span>

<span data-ttu-id="cc1df-132">Si une application modifie des propriétés en *pWiaItem2*, entre l’acquisition de l’image dans *pInputStream* et son appel à **IWiaSegmentationFilter ::D etectregions**, les propriétés d’origine (autrement dit, les propriétés de l’élément lors de l’acquisition du flux) doivent être restaurées.</span><span class="sxs-lookup"><span data-stu-id="cc1df-132">If an application changes any properties into *pWiaItem2*, between acquiring the image into *pInputStream* and its call to **IWiaSegmentationFilter::DetectRegions**, the original properties (that is, the properties the item had when the stream was acquired) must be restored.</span></span> <span data-ttu-id="cc1df-133">Cela peut être effectué par [**GetPropertyStream**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiapropertystorage-getpropertystream) et [**SetPropertyStream**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiapropertystorage-setpropertystream).</span><span class="sxs-lookup"><span data-stu-id="cc1df-133">This can be done by [**GetPropertyStream**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiapropertystorage-getpropertystream) and [**SetPropertyStream**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiapropertystorage-setpropertystream).</span></span>

<span data-ttu-id="cc1df-134">L’application doit réinitialiser l' [IStream](/windows/win32/api/objidl/nn-objidl-istream) si son appel passe le même flux dans le filtre de segmentation plusieurs fois.</span><span class="sxs-lookup"><span data-stu-id="cc1df-134">The application must reset the [IStream](/windows/win32/api/objidl/nn-objidl-istream) if its call passes the same stream into the segmentation filter more than once.</span></span> <span data-ttu-id="cc1df-135">L’application doit également réinitialiser le flux après le téléchargement initial et avant d’appeler **IWiaSegmentationFilter ::D etectregions**.</span><span class="sxs-lookup"><span data-stu-id="cc1df-135">The application must also reset the stream after the initial download and before calling **IWiaSegmentationFilter::DetectRegions**.</span></span>

## <a name="examples"></a><span data-ttu-id="cc1df-136">Exemples</span><span class="sxs-lookup"><span data-stu-id="cc1df-136">Examples</span></span>

<span data-ttu-id="cc1df-137">La segmentation effectue la détection de la région sur le flux ( `pImageStream` ) passé dans DetectSubregions.</span><span class="sxs-lookup"><span data-stu-id="cc1df-137">The segmentation performs region detection on the stream (`pImageStream`) passed into DetectSubregions.</span></span> <span data-ttu-id="cc1df-138">Consultez la méthode [**GetExtension**](-wia-iwiaitem2-getextension.md) pour CreateSegmentationFilter utilisée dans cet exemple.</span><span class="sxs-lookup"><span data-stu-id="cc1df-138">See the [**GetExtension**](-wia-iwiaitem2-getextension.md) for CreateSegmentationFilter method used in this example.</span></span>


```C++
HRESULT
DetectSubregions(
   IN IStream   *pImageStream,
   IN IWiaItem2 *pWiaItem2)
{
   HRESULT                 hr                  = S_OK;
   IWiaSegmentationFilter* pSegmentationFilter = NULL;

   if (!pWiaItem2 || !pImageStream)
   {
      hr = E_INVALIDARG;
   }

   if (SUCCEEDED(hr))
   {
      hr = CreateSegmentationFilter(pWiaItem2, &pSegmentationFilter);
   }

   if (SUCCEEDED(hr))
   {
      hr = pSegmentationFilter->DetectRegions(0,pImageStream, pWiaItem2); 
   }

   if (pSegmentationFilter)
   {
      pSegmentationFilter->Release();
      pSegmentationFilter = NULL;
   }

   return hr;
}
```



<span data-ttu-id="cc1df-139">DownloadPreviewImage télécharge les données de l’image à partir du scanneur en appelant la méthode [**GetNewPreview**](-wia-iwiapreview-getnewpreview.md) du composant de prévisualisation.</span><span class="sxs-lookup"><span data-stu-id="cc1df-139">DownloadPreviewImage downloads image data from the scanner by calling the preview component's [**GetNewPreview**](-wia-iwiapreview-getnewpreview.md) method.</span></span> <span data-ttu-id="cc1df-140">Il appelle ensuite DetectSubregions si l’utilisateur de l’application souhaite appeler le filtre de segmentation, ce qui crée un élément enfant sous pWiaItem2 pour chaque région qu’il détecte.</span><span class="sxs-lookup"><span data-stu-id="cc1df-140">It then calls DetectSubregions if the application user wants to invoke the segmentation filter, which creates a child item under pWiaItem2 for each region it detects.</span></span> <span data-ttu-id="cc1df-141">Consultez **IWiaSegmentationFilter ::D etectregions** pour la méthode DetectSubregions utilisée dans cet exemple.</span><span class="sxs-lookup"><span data-stu-id="cc1df-141">See **IWiaSegmentationFilter::DetectRegions** for the DetectSubregions method used in this example.</span></span>

<span data-ttu-id="cc1df-142">Dans cet exemple, l’utilisateur de l’application définit `m_bUseSegmentationFilter` en cliquant sur une case à cocher.</span><span class="sxs-lookup"><span data-stu-id="cc1df-142">In this example, the application user sets `m_bUseSegmentationFilter` by clicking a check box.</span></span> <span data-ttu-id="cc1df-143">Si l’application prend en charge cette option, elle doit d’abord vérifier que le pilote possède un filtre de segmentation en appelant [**CheckExtension**](-wia-iwiaitem2-checkextension.md).</span><span class="sxs-lookup"><span data-stu-id="cc1df-143">If the application supports this, it should first check that the driver has a segmentation filter by calling [**CheckExtension**](-wia-iwiaitem2-checkextension.md).</span></span> <span data-ttu-id="cc1df-144">Consultez [**GetNewPreview**](-wia-iwiapreview-getnewpreview.md) pour obtenir l’exemple de méthode CheckImgFilter qui montre comment procéder.</span><span class="sxs-lookup"><span data-stu-id="cc1df-144">See [**GetNewPreview**](-wia-iwiapreview-getnewpreview.md) for the CheckImgFilter method example that shows how this can be done.</span></span>


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
         // The constructor of AppWiaTransferCallback sets the reference count 
         // to 1.
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
         // Do not create an instance of preview component if the driver 
         // does not come with an image-processing filter.
         // You can use a segmentation filter, however, if the driver
         // comes with one (omitted here).
      }
   }

   return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="cc1df-145">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cc1df-145">Requirements</span></span>



| <span data-ttu-id="cc1df-146">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cc1df-146">Requirement</span></span> | <span data-ttu-id="cc1df-147">Valeur</span><span class="sxs-lookup"><span data-stu-id="cc1df-147">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="cc1df-148">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cc1df-148">Minimum supported client</span></span><br/> | <span data-ttu-id="cc1df-149">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cc1df-149">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="cc1df-150">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cc1df-150">Minimum supported server</span></span><br/> | <span data-ttu-id="cc1df-151">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cc1df-151">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="cc1df-152">En-tête</span><span class="sxs-lookup"><span data-stu-id="cc1df-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="cc1df-153"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="cc1df-153"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="cc1df-154">MIDL</span><span class="sxs-lookup"><span data-stu-id="cc1df-154">IDL</span></span><br/>                      | <dl> <span data-ttu-id="cc1df-155"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="cc1df-155"><dt>Wia.idl</dt></span></span> </dl> |



 

 
