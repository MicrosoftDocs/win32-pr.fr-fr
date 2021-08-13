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
ms.openlocfilehash: 46496360d7b54bed837ba287d604233a9fac98ee13807744b4adbfb52e9934d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119450259"
---
# <a name="iwiasegmentationfilterdetectregions-method"></a>IWiaSegmentationFilter ::D méthode etectRegions

Détermine les sous-régions d’une image disposées sur le plateau à plat afin que chacune des sous-régions puisse être acquise dans un élément d’image séparé.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT DetectRegions(
  [in] LONG      lFlags,
  [in] IStream   *pInputStream,
  [in] IWiaItem2 *pWiaItem2
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lFlags* \[ dans\]
</dt> <dd>

Type : **long**

Actuellement inutilisé. Doit être défini sur zéro (0).

</dd> <dt>

*pInputStream* \[ dans\]
</dt> <dd>

Type : **[IStream](/windows/win32/api/objidl/nn-objidl-istream)\***

Spécifie un pointeur vers l’image [IStream](/windows/win32/api/objidl/nn-objidl-istream) preview.

</dd> <dt>

*pWiaItem2* \[ dans\]
</dt> <dd>

Type : **[ **IWiaItem2**](-wia-iwiaitem2.md)\***

Spécifie un pointeur vers l’élément [**IWiaItem2**](-wia-iwiaitem2.md) pour lequel *pInputStream* a été acquis. Le filtre de segmentation crée des éléments enfants pour cet élément.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **HRESULT**

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Remarques

Cette méthode détermine les sous-régions de l’image représentée par pInputStream. Pour chaque sous-région qu’il détecte, il crée un élément enfant pour l’élément [**IWiaItem2**](-wia-iwiaitem2.md) spécifié dans le paramètre *pWiaItem2* . Pour chaque élément enfant, le filtre de segmentation doit définir des valeurs pour le rectangle englobant de la zone à analyser, à l’aide des [**constantes de propriété d’élément WIA du scanneur**](-wia-wiaitempropscanneritem.md)suivantes.

-   [**\_adresses IP WIA, \_ xpos**](-wia-wiaitempropscanneritem.md)
-   [**\_Posy IPS \_ WIA**](-wia-wiaitempropscanneritem.md)
-   [**\_XEXTENT IPS \_ WIA**](-wia-wiaitempropscanneritem.md)
-   [**\_YEXTENT IPS \_ WIA**](-wia-wiaitempropscanneritem.md)

Un filtre plus avancé peut également nécessiter d’autres [**constantes de propriété d’élément de scanneur WIA**](-wia-wiaitempropscanneritem.md) , telles que la suppression d’une déformation des adresses IP WIA **\_ \_ \_ X** et les **adresses IP WIA avec la \_ \_ réalignement \_ Y**, si le pilote prend en charge l’annulation de l’inclinaison.

Si l’application appelle **IWiaSegmentationFilter ::D etectregions** plusieurs fois, l’application doit d’abord supprimer les éléments enfants créés par le dernier appel à **IWiaSegmentationFilter ::D etectregions**.

Si une application modifie des propriétés en *pWiaItem2*, entre l’acquisition de l’image dans *pInputStream* et son appel à **IWiaSegmentationFilter ::D etectregions**, les propriétés d’origine (autrement dit, les propriétés de l’élément lors de l’acquisition du flux) doivent être restaurées. Cela peut être effectué par [**GetPropertyStream**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiapropertystorage-getpropertystream) et [**SetPropertyStream**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiapropertystorage-setpropertystream).

L’application doit réinitialiser l' [IStream](/windows/win32/api/objidl/nn-objidl-istream) si son appel passe le même flux dans le filtre de segmentation plusieurs fois. L’application doit également réinitialiser le flux après le téléchargement initial et avant d’appeler **IWiaSegmentationFilter ::D etectregions**.

## <a name="examples"></a>Exemples

La segmentation effectue la détection de la région sur le flux ( `pImageStream` ) passé dans DetectSubregions. Consultez la méthode [**GetExtension**](-wia-iwiaitem2-getextension.md) pour CreateSegmentationFilter utilisée dans cet exemple.


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



DownloadPreviewImage télécharge les données de l’image à partir du scanneur en appelant la méthode [**GetNewPreview**](-wia-iwiapreview-getnewpreview.md) du composant de prévisualisation. Il appelle ensuite DetectSubregions si l’utilisateur de l’application souhaite appeler le filtre de segmentation, ce qui crée un élément enfant sous pWiaItem2 pour chaque région qu’il détecte. Consultez **IWiaSegmentationFilter ::D etectregions** pour la méthode DetectSubregions utilisée dans cet exemple.

Dans cet exemple, l’utilisateur de l’application définit `m_bUseSegmentationFilter` en cliquant sur une case à cocher. Si l’application prend en charge cette option, elle doit d’abord vérifier que le pilote possède un filtre de segmentation en appelant [**CheckExtension**](-wia-iwiaitem2-checkextension.md). Consultez [**GetNewPreview**](-wia-iwiapreview-getnewpreview.md) pour obtenir l’exemple de méthode CheckImgFilter qui montre comment procéder.


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



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 
