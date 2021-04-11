---
description: 'Obtient l’image non filtrée mise en cache par la méthode IWiaPreview :: GetNewPreview.'
ms.assetid: 121b6866-cca1-4170-9bdf-225491f942f5
title: 'IWiaPreview :: UpdatePreview, méthode (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaPreview.UpdatePreview
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 4a5d469179f341f3bad5d2b9b5ed25a5715be694
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113302"
---
# <a name="iwiapreviewupdatepreview-method"></a><span data-ttu-id="4aa33-103">IWiaPreview :: UpdatePreview, méthode</span><span class="sxs-lookup"><span data-stu-id="4aa33-103">IWiaPreview::UpdatePreview method</span></span>

<span data-ttu-id="4aa33-104">Obtient l’image non filtrée mise en cache par la méthode [**IWiaPreview :: GetNewPreview**](-wia-iwiapreview-getnewpreview.md) .</span><span class="sxs-lookup"><span data-stu-id="4aa33-104">Gets the unfiltered image cached by the [**IWiaPreview::GetNewPreview**](-wia-iwiapreview-getnewpreview.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="4aa33-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4aa33-105">Syntax</span></span>


```C++
HRESULT UpdatePreview(
  [in] LONG      lOptions,
  [in] IWiaItem2 *pChildWiaItem
);
```



## <a name="parameters"></a><span data-ttu-id="4aa33-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4aa33-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4aa33-107">*lOptions* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4aa33-107">*lOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4aa33-108">Type : **long**</span><span class="sxs-lookup"><span data-stu-id="4aa33-108">Type: **LONG**</span></span>

<span data-ttu-id="4aa33-109">Spécifie si l’application requiert que le composant WIA 2,0 Preview transmette une sous-région de l’image mise en cache ou la totalité de l’image mise en cache au filtre de traitement d’image.</span><span class="sxs-lookup"><span data-stu-id="4aa33-109">Specifies whether the application requires the WIA 2.0 Preview Component to pass a sub-region of the cached image or the entire cached image to the image processing filter.</span></span>

<dt>

<span id="WiaPreviewReturnOriginalImage"></span><span id="wiapreviewreturnoriginalimage"></span><span id="WIAPREVIEWRETURNORIGINALIMAGE"></span>

<span data-ttu-id="4aa33-110"><span id="WiaPreviewReturnOriginalImage"></span><span id="wiapreviewreturnoriginalimage"></span><span id="WIAPREVIEWRETURNORIGINALIMAGE"></span>**WiaPreviewReturnOriginalImage**</span><span class="sxs-lookup"><span data-stu-id="4aa33-110"><span id="WiaPreviewReturnOriginalImage"></span><span id="wiapreviewreturnoriginalimage"></span><span id="WIAPREVIEWRETURNORIGINALIMAGE"></span>**WiaPreviewReturnOriginalImage**</span></span>


</dt> <dd>

<span data-ttu-id="4aa33-111">Transmettez la totalité de l’image mise en cache au filtre de traitement d’image.</span><span class="sxs-lookup"><span data-stu-id="4aa33-111">Pass the entire cached image to the image processing filter.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="4aa33-112">*pChildWiaItem* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4aa33-112">*pChildWiaItem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4aa33-113">Tapez : \**[**IWiaItem2**](-wia-iwiaitem2.md) \** _</span><span class="sxs-lookup"><span data-stu-id="4aa33-113">Type: \**[**IWiaItem2**](-wia-iwiaitem2.md)\** _</span></span>

<span data-ttu-id="4aa33-114">Spécifie un pointeur vers l’élément [_ *IWiaItem2* \*](-wia-iwiaitem2.md) , qui est un enfant de l’élément **IWiaItem2** spécifié par le paramètre *pWiaItem2* de la méthode [**IWiaPreview :: GetNewPreview**](-wia-iwiapreview-getnewpreview.md) .</span><span class="sxs-lookup"><span data-stu-id="4aa33-114">Specifies a pointer to the [_ *IWiaItem2*\*](-wia-iwiaitem2.md) item, which is a child of the **IWiaItem2** item specified by the *pWiaItem2* parameter of the [**IWiaPreview::GetNewPreview**](-wia-iwiapreview-getnewpreview.md) method.</span></span> <span data-ttu-id="4aa33-115">Ou, si l’application requiert une version préliminaire de l’ensemble du plateau, spécifie un pointeur vers le paramètre *pWiaItem2* de la méthode **IWiaPreview :: GetNewPreview** .</span><span class="sxs-lookup"><span data-stu-id="4aa33-115">Or, if the application requires a preview of the whole flatbed, specifies a pointer to the *pWiaItem2* parameter of the **IWiaPreview::GetNewPreview** method.</span></span> <span data-ttu-id="4aa33-116">Quand *pChildWiaItem* est un enfant du paramètre *pWiaItem2* de **IWiaPreview :: GetNewPreview**, cet élément enfant est généralement créé par le filtre de segmentation.</span><span class="sxs-lookup"><span data-stu-id="4aa33-116">When *pChildWiaItem* is a child of **IWiaPreview::GetNewPreview**'s *pWiaItem2* parameter, this child item is typically created by the segmentation filter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4aa33-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4aa33-117">Return value</span></span>

<span data-ttu-id="4aa33-118">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="4aa33-118">Type: **HRESULT**</span></span>

<span data-ttu-id="4aa33-119">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="4aa33-119">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="4aa33-120">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4aa33-120">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="4aa33-121">Notes</span><span class="sxs-lookup"><span data-stu-id="4aa33-121">Remarks</span></span>

<span data-ttu-id="4aa33-122">Cette méthode passe l’image mise en cache et non filtrée via le filtre de traitement d’image, qui écrit ensuite les données filtrées dans le flux fourni par l’application.</span><span class="sxs-lookup"><span data-stu-id="4aa33-122">This method passes the cached, unfiltered image through the image processing filter, which then writes the filtered data to the application-provided stream.</span></span> <span data-ttu-id="4aa33-123">Le composant d’aperçu WIA 2,0 récupère ce flux en appelant la méthode [**GetNextStream**](-wia-iwiatransfercallback-getnextstream.md) du filtre de traitement d’image, qui appelle ensuite l’implémentation **GetNextStream** du rappel de l’application.</span><span class="sxs-lookup"><span data-stu-id="4aa33-123">The WIA 2.0 Preview Component retrieves this stream by calling the image processing filter's [**GetNextStream**](-wia-iwiatransfercallback-getnextstream.md) method, which then calls the application callback's **GetNextStream** implementation.</span></span> <span data-ttu-id="4aa33-124">Avant d’appeler **IWiaPreview :: UpdatePreview**, une application doit d’abord appeler [**IWiaPreview :: GetNewPreview**](-wia-iwiapreview-getnewpreview.md) pour acquérir l’image à partir du scanneur ; dans le cas contraire, la méthode retourne une erreur.</span><span class="sxs-lookup"><span data-stu-id="4aa33-124">Before calling **IWiaPreview::UpdatePreview**, an application must first call [**IWiaPreview::GetNewPreview**](-wia-iwiapreview-getnewpreview.md) to acquire the image from the scanner; otherwise, the method returns an error.</span></span>

<span data-ttu-id="4aa33-125">Le composant WIA 2,0 Preview stocke l’image non filtrée téléchargée à partir du pilote.</span><span class="sxs-lookup"><span data-stu-id="4aa33-125">The WIA 2.0 Preview Component stores the unfiltered image downloaded from the driver.</span></span> <span data-ttu-id="4aa33-126">Il est possible que l’élément WIA 2,0 passé dans **IWiaPreview :: UpdatePreview** ne représente qu’une petite zone de l’image téléchargée à partir du pilote.</span><span class="sxs-lookup"><span data-stu-id="4aa33-126">It is possible that the WIA 2.0 item passed into **IWiaPreview::UpdatePreview** represents only a small region of the image downloaded from the driver.</span></span> <span data-ttu-id="4aa33-127">Si c’est le cas, le composant WIA 2,0 Preview supprime en fait cette région de l’image mise en cache avant de la transmettre au filtre de traitement d’image, qui à son tour transmet les données de l’image filtrée à l’application.</span><span class="sxs-lookup"><span data-stu-id="4aa33-127">If this is the case the WIA 2.0 Preview Component actually cuts out this region from the cached image before it passes it to the image processing filter, which in turn passes the filtered image data back to the application.</span></span>

<span data-ttu-id="4aa33-128">Pour qu’une application transmette la totalité de l’image mise en cache au filtre de traitement d’image (qui à son tour la transmet à l’application), elle doit affecter à *lOptions* la valeur **WiaPreviewReturnOriginalImage** lors de l’appel de **IWiaPreview :: UpdatePreview**.</span><span class="sxs-lookup"><span data-stu-id="4aa33-128">For an application to pass the entire cached image to the image processing filter (which in turn passes it to the application), it must set the *lOptions* to **WiaPreviewReturnOriginalImage** when calling **IWiaPreview::UpdatePreview**.</span></span> <span data-ttu-id="4aa33-129">Lors de la définition de *lOptions* sur **WiaPreviewReturnOriginalImage**, l’application doit s’assurer que les paramètres d’étendue ([**WIA \_ IPS \_ XEXTENT**](-wia-wiaitempropscanneritem.md) et **WIA \_ \_ YEXTENT**) de l’élément transmis à **IWiaPreview :: UpdatePreview** correspondent à l’image en cache intégral.</span><span class="sxs-lookup"><span data-stu-id="4aa33-129">When setting *lOptions* to **WiaPreviewReturnOriginalImage**, the application must ensure that the extent settings ([**WIA\_IPS\_XEXTENT**](-wia-wiaitempropscanneritem.md) and **WIA\_IPS\_YEXTENT**) of the item passed into **IWiaPreview::UpdatePreview** matches the full-cached image.</span></span> <span data-ttu-id="4aa33-130">Le filtre de traitement d’image n’a pas besoin d’être différent dans ce cas ; Il filtre simplement l’image, en fonction des propriétés de *pChildWiaItem* (en général, dans ce cas, *pChildWiaItem* est le même élément que celui qui a été passé à [**IWiaPreview :: GetNewPreview**](-wia-iwiapreview-getnewpreview.md)).</span><span class="sxs-lookup"><span data-stu-id="4aa33-130">The image processing filter need not do anything different in this case; it simply filters the image, based on the properties of *pChildWiaItem* (typically in this case *pChildWiaItem* is the same item that was passed to [**IWiaPreview::GetNewPreview**](-wia-iwiapreview-getnewpreview.md)).</span></span> <span data-ttu-id="4aa33-131">Les différentes sous-régions sont ignorées et l’image entière est filtrée à l’aide des mêmes paramètres.</span><span class="sxs-lookup"><span data-stu-id="4aa33-131">The different sub-regions are ignored and the whole image is filtered using the same settings.</span></span> <span data-ttu-id="4aa33-132">Une application peut faire cela pour plusieurs raisons.</span><span class="sxs-lookup"><span data-stu-id="4aa33-132">There are a couple of reasons why an application would do this.</span></span>

1.  <span data-ttu-id="4aa33-133">Il se peut que l’application ne prenne pas en charge la modification des paramètres (tels que la [**\_ \_ luminosité IPS WIA**](-wia-wiaitempropscanneritem.md) et le **\_ \_ contraste des adresses IP WIA**) individuellement pour chaque région que le filtre de segmentation détecte (ou qu’il ne souhaite peut-être même pas utiliser le filtre de segmentation).</span><span class="sxs-lookup"><span data-stu-id="4aa33-133">The application may not support changing the settings (like [**WIA\_IPS\_BRIGHTNESS**](-wia-wiaitempropscanneritem.md) and **WIA\_IPS\_CONTRAST**) individually for each region that the segmentation filter detects (or it may not even want to use the segmentation filter).</span></span> <span data-ttu-id="4aa33-134">Il est plus facile pour l’application d’appeler **IWiaPreview :: UpdatePreview** avec **WiaPreviewReturnOriginalImage** afin qu’elle reçoive toujours l’image complète à partir du composant WIA 2,0 Preview.</span><span class="sxs-lookup"><span data-stu-id="4aa33-134">It is easier for the application to call **IWiaPreview::UpdatePreview** with **WiaPreviewReturnOriginalImage** so that it always receives the full image from the WIA 2.0 Preview Component.</span></span>
2.  <span data-ttu-id="4aa33-135">Le composant WIA 2,0 Preview ne prend pas en charge le format d’image de l’image d’aperçu. dans ce cas, il ne peut pas effectuer les actions nécessaires pour couper la région souhaitée.</span><span class="sxs-lookup"><span data-stu-id="4aa33-135">The WIA 2.0 Preview Component does not support the image format of the preview image, in which case it cannot perform the actions to cut out the desired region.</span></span> <span data-ttu-id="4aa33-136">La prise en charge du format d’image du composant WIA 2,0 Preview est limitée aux formats pour lesquels il existe des encodeurs et des décodeurs GDI+ Windows 1,1 GDI+.</span><span class="sxs-lookup"><span data-stu-id="4aa33-136">The WIA 2.0 Preview Component's image format support is limited to formats for which there are Windows GDI+ 1.1 encoders and decoders.</span></span> <span data-ttu-id="4aa33-137">Ces formats sont des bitmaps (BMP) (bitmap qui comprend BITMAPFILEHEADER), GIF (Graphics Interchange Format), JPEG, PNG (Portable Network Graphics) et TIFF (Tagged Image File Format).</span><span class="sxs-lookup"><span data-stu-id="4aa33-137">These formats are bitmap (BMP) (a bitmap that includes the BITMAPFILEHEADER), Graphics Interchange Format (GIF), JPEG, Portable Network Graphics (PNG), and Tagged Image File Format (TIFF).</span></span>

<span data-ttu-id="4aa33-138">Notez que si l’application transmet **WiaPreviewReturnOriginalImage** à **IWiaPreview :: UpdatePreview**, le composant WIA 2,0 Preview peut prendre en charge n’importe quel format d’image ou de pixel.</span><span class="sxs-lookup"><span data-stu-id="4aa33-138">Note that if the application passes **WiaPreviewReturnOriginalImage** into **IWiaPreview::UpdatePreview**, the WIA 2.0 Preview Component can support any image or pixel format.</span></span>

<span data-ttu-id="4aa33-139">**IWiaPreview :: UpdatePreview** définit la [**propriété \_ \_ preview DPS WIA**](-wia-wiaitempropscannerdevice.md) (et la réinitialise avant qu’elle ne soit retournée, sauf si elle a été définie auparavant).</span><span class="sxs-lookup"><span data-stu-id="4aa33-139">**IWiaPreview::UpdatePreview** sets the [**WIA\_DPS\_PREVIEW**](-wia-wiaitempropscannerdevice.md) property (and resets it before it returns, unless it was set before).</span></span> <span data-ttu-id="4aa33-140">Cela permet au pilote (et au matériel) et au filtre de traitement d’image de savoir que l’élément est une analyse de préversion.</span><span class="sxs-lookup"><span data-stu-id="4aa33-140">This lets the driver (and hardware) as well as the image processing filter, know that the item is a preview scan.</span></span>

<span data-ttu-id="4aa33-141">Une application doit s’assurer *que pChildWiaItem* a le même format d’image (WIA) et la même résolution ([**WIA \_ IPS \_ XRES**](-wia-wiaitempropscanneritem.md) and **WIA \_ IPS \_ YRES**) que *pWiaItem* avait lors de sa transmission dans [**IWiaPreview :: GetNewPreview**](-wia-iwiapreview-getnewpreview.md).[**\_ \_**](-wia-wiaitempropcommonitem.md)</span><span class="sxs-lookup"><span data-stu-id="4aa33-141">An application must ensure that *pChildWiaItem* has the same image format ([**WIA\_IPA\_FORMAT**](-wia-wiaitempropcommonitem.md)) and resolution ([**WIA\_IPS\_XRES**](-wia-wiaitempropscanneritem.md) and **WIA\_IPS\_YRES**) as *pWiaItem* had when it was passed into [**IWiaPreview::GetNewPreview**](-wia-iwiapreview-getnewpreview.md).</span></span> <span data-ttu-id="4aa33-142">Le format de l’élément enfant doit correspondre au format de l’image mise en cache du composant WIA 2,0 Preview (le composant WIA 2,0 Preview n’effectue aucune conversion d’image).</span><span class="sxs-lookup"><span data-stu-id="4aa33-142">The format of the child item must correspond to the format of the WIA 2.0 Preview Component's cached image (the WIA 2.0 Preview Component performs no image conversion).</span></span>

## <a name="examples"></a><span data-ttu-id="4aa33-143">Exemples</span><span class="sxs-lookup"><span data-stu-id="4aa33-143">Examples</span></span>

<span data-ttu-id="4aa33-144">UpdateRegion doit être appelé chaque fois qu’un utilisateur modifie, par exemple, la luminosité ou le contraste pour l’élément enfant représenté par `dwRegionNumber` .</span><span class="sxs-lookup"><span data-stu-id="4aa33-144">UpdateRegion should be called each time a user changes, for example, the brightness or contrast for the child item represented by `dwRegionNumber`.</span></span> <span data-ttu-id="4aa33-145">Cet élément enfant a été créé précédemment par le filtre de segmentation ([**IWiaSegmentationFilter**](-wia-iwiasegmentationfilter.md).</span><span class="sxs-lookup"><span data-stu-id="4aa33-145">This child item has previously been created by the segmentation filter ([**IWiaSegmentationFilter**](-wia-iwiasegmentationfilter.md).</span></span> <span data-ttu-id="4aa33-146">L’image écrite dans l' [IStream](/windows/win32/api/objidl/nn-objidl-istream) est retournée par la méthode [**GetNextStream**](-wia-iwiatransfercallback-getnextstream.md) de l’interface de rappel de transfert.</span><span class="sxs-lookup"><span data-stu-id="4aa33-146">The image written to the [IStream](/windows/win32/api/objidl/nn-objidl-istream) is returned by the transfer callback interface's [**GetNextStream**](-wia-iwiatransfercallback-getnextstream.md) method.</span></span> <span data-ttu-id="4aa33-147">Le code pour GetSubRegionItem est omis dans cet exemple.</span><span class="sxs-lookup"><span data-stu-id="4aa33-147">The code for GetSubRegionItem is omitted in this example.</span></span>

<span data-ttu-id="4aa33-148">Une fois que cette fonction a été appelée, une application redessine généralement la région à l’écran.</span><span class="sxs-lookup"><span data-stu-id="4aa33-148">After this function has been called, an application would typically redraw the region on the screen.</span></span>


```C++
HRESULT
UpdateRegion(
   IN  DWORD dwRegionNumber)
{
   IWiaItem2 *pSubRegion = GetSubRegionItem(dwRegionNumber);

   return m_pWiaPreview->UpdatePreview(0,pSubRegion);
}
```



## <a name="requirements"></a><span data-ttu-id="4aa33-149">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4aa33-149">Requirements</span></span>



| <span data-ttu-id="4aa33-150">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4aa33-150">Requirement</span></span> | <span data-ttu-id="4aa33-151">Valeur</span><span class="sxs-lookup"><span data-stu-id="4aa33-151">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4aa33-152">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4aa33-152">Minimum supported client</span></span><br/> | <span data-ttu-id="4aa33-153">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4aa33-153">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="4aa33-154">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4aa33-154">Minimum supported server</span></span><br/> | <span data-ttu-id="4aa33-155">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4aa33-155">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="4aa33-156">En-tête</span><span class="sxs-lookup"><span data-stu-id="4aa33-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="4aa33-157"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="4aa33-157"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="4aa33-158">MIDL</span><span class="sxs-lookup"><span data-stu-id="4aa33-158">IDL</span></span><br/>                      | <dl> <span data-ttu-id="4aa33-159"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="4aa33-159"><dt>Wia.idl</dt></span></span> </dl> |



 

 
