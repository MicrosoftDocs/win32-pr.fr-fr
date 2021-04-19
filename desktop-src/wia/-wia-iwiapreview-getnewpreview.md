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
# <a name="iwiapreviewgetnewpreview-method"></a>IWiaPreview :: GetNewPreview, méthode

Met en cache en interne l’image non filtrée retournée par le pilote.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetNewPreview(
  [in] IWiaItem2            *pWiaItem2,
  [in] LONG                 lFlags,
  [in] IWiaTransferCallback *pWiaTransferCallback
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pWiaItem2* \[ dans\]
</dt> <dd>

Tapez : **[**IWiaItem2**](-wia-iwiaitem2.md) \** _

Spécifie un pointeur vers l’élément [_ *IWiaItem2* *](-wia-iwiaitem2.md) pour l’image.

</dd> <dt>

*lFlags* \[ dans\]
</dt> <dd>

Type : **long**

Actuellement inutilisé. Doit être défini sur zéro (0).

</dd> <dt>

*pWiaTransferCallback* \[ dans\]
</dt> <dd>

Tapez : **[**IWiaTransferCallback**](-wia-iwiatransfercallback.md) \** _

Spécifie un pointeur vers l’interface [_ *IWiaTransferCallback* *](-wia-iwiatransfercallback.md) de l’application appelante.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **HRESULT**

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Notes

Une application doit appeler **IWiaPreview :: GetNewPreview** avant d’appeler [**IWiaPreview ::D etectregions**](-wia-iwiapreview-detectregions.md).

**IWiaPreview :: GetNewPreview** définit la [**propriété \_ \_ preview DPS WIA**](-wia-wiaitempropscannerdevice.md) (et la réinitialise avant qu’elle ne soit retournée, sauf si elle a été définie auparavant). Cela permet au pilote et au matériel, ainsi qu’au filtre de traitement d’image, de savoir que l’élément est une analyse de préversion.

En interne, le composant Windows Image Acquisition (WIA) 2,0 Preview crée une instance du filtre de traitement d’image du pilote en appelant [**GetExtension**](-wia-iwiaitem2-getextension.md) sur *pWiaItem2*. Le composant WIA 2,0 Preview effectue cette création lorsque l’application appelle **IWiaPreview :: GetNewPreview**. Le composant WIA 2,0 Preview initialise également le filtre dans **IWiaPreview :: GetNewPreview**. La même instance de filtre est utilisée par le composant WIA 2,0 Preview lors d’un appel à [**IWiaPreview :: UpdatePreview**](-wia-iwiapreview-updatepreview.md).

Avant d’appeler le composant WIA 2,0 Preview, une application doit appeler [**CheckExtension**](-wia-iwiaitem2-checkextension.md) pour s’assurer que le pilote est fourni avec un filtre de traitement d’image. Elle doit appeler **CheckExtension** sur l’élément qu’elle transmettra à **IWiaPreview :: GetNewPreview**. Il est inutile de fournir des aperçus dynamiques sans filtre de traitement d’image. Si une application appelle **IWiaPreview :: GetNewPreview** pour un pilote sans filtre de traitement d’image, l’appel échoue.

## <a name="examples"></a>Exemples

CheckImgFilter vérifie si le pilote a un filtre de traitement d’image. Avant d’appeler la version préliminaire du composant, une application doit s’assurer que le pilote possède un filtre de traitement d’image.


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



DownloadPreviewImage télécharge les données de l’image à partir du scanneur en appelant la méthode **IWiaPreview :: GetNewPreview** du composant de prévisualisation. Il appelle ensuite DetectSubregions si l’utilisateur de l’application souhaite appeler le filtre de segmentation, ce qui crée un élément enfant sous pWiaItem2 pour chaque région qu’il détecte. Consultez [**DetectRegions**](-wia-iwiasegmentationfilter-detectregions.md) pour la méthode DetectSubregions utilisée dans cet exemple.

Dans cet exemple, l’utilisateur de l’application définit `m_bUseSegmentationFilter` en cliquant sur une case à cocher. Si l’application prend en charge cette option, elle doit d’abord vérifier que le pilote possède un filtre de segmentation en appelant [**CheckExtension**](-wia-iwiaitem2-checkextension.md). Consultez **IWiaPreview :: GetNewPreview** pour l’exemple de méthode CheckImgFilter qui montre comment effectuer cette opération.


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



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 




