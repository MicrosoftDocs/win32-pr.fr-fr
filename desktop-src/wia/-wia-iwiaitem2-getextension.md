---
description: obtient les interfaces d’extension qui peuvent provenir d’un pilote de périphérique Windows acquisition d’images (WIA) 2,0.
ms.assetid: 70f20f33-905c-4a88-8065-1cf876e98302
title: 'IWiaItem2 :: GetExtension, méthode (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.GetExtension
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 2fea4c4b9a2dd909b7ec49097ee94664b47f7e47
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127526488"
---
# <a name="iwiaitem2getextension-method"></a>IWiaItem2 :: GetExtension, méthode

obtient les interfaces d’extension qui peuvent provenir d’un pilote de périphérique Windows acquisition d’images (WIA) 2,0.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetExtension(
  [in]  LONG   lFlags,
  [in]  BSTR   bstrName,
  [in]  REFIID riidExtensionInterface,
  [out] VOID   **ppOut
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lFlags* \[ dans\]
</dt> <dd>

Type : **long**

Actuellement inutilisé. Doit être défini sur zéro (0).

</dd> <dt>

*bstrName* \[ dans\]
</dt> <dd>

Type : **BSTR**

Spécifie le nom de l’extension vers laquelle l’application appelante requiert un pointeur.

<dt>

<span id="SegmentationFilter"></span><span id="segmentationfilter"></span><span id="SEGMENTATIONFILTER"></span>

<span id="SegmentationFilter"></span><span id="segmentationfilter"></span><span id="SEGMENTATIONFILTER"></span>**SegmentationFilter**


</dt> <dd>

Extension du filtre de segmentation. Il s’agit actuellement de la seule valeur valide pour ce paramètre.

</dd> </dl> </dd> <dt>

*riidExtensionInterface* \[ dans\]
</dt> <dd>

Type : **REFIID**

Spécifie l’identificateur de l’interface d’extension.

</dd> <dt>

*ppOut* \[ à\]
</dt> <dd>

Type : **void \* \***

Reçoit l’adresse d’un pointeur vers l’interface d’extension.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **HRESULT**

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Remarques

Une application appelle cette méthode pour créer un objet d’extension qui implémente l’une des interfaces d’extension de pilote WIA 2,0. **IWiaItem2 :: GetExtension** stocke l’adresse de l’interface d’extension de l’objet d’extension dans le paramètre *riidExtensionInterface* . L’application utilise ensuite le pointeur d’interface pour appeler ses méthodes.

Les applications doivent appeler la méthode [IUnknown :: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) sur les pointeurs d’interface qu’elles reçoivent via le paramètre *riidExtensionInterface* .

## <a name="examples"></a>Exemples

CreateSegmentationFilter crée une instance du filtre de segmentation du pilote ([**IWiaSegmentationFilter**](-wia-iwiasegmentationfilter.md)) en appelant **IWiaItem2 :: GetExtension** sur l’interface [**IWiaItem2**](-wia-iwiaitem2.md) passée.


```C++
HRESULT
CreateSegmentationFilter(
   IWiaItem2               *pWiaItem2,
   IWiaSegmentationFilter  **ppSegmentationFilter)
{
   HRESULT                 hr         = S_OK;
   IWiaSegmentationFilter *pSegFilter = NULL;
    
   if (!pWiaItem2 || !ppSegmentationFilter)
   {
      hr = E_INVALIDARG;
   }

   if (SUCCEEDED(hr))
   {
      BSTR    bstrFilterString = SysAllocString(WIA_SEGMENTATION_FILTER_STR);

      if (bstrFilterString)
      {
         hr = pWiaItem2->GetExtension(0,
                                      bstrFilterString,
                                      IID_IWiaSegmentationFilter,
                                      (void**)&pSegFilter);
         SysFreeString(bstrFilterString);
         bstrFilterString = NULL;
      }
      else
      {
         hr = E_OUTOFMEMORY;
      }
   }

   if (SUCCEEDED(hr))
   {
     *ppSegmentationFilter = pSegFilter;
      pSegFilter = NULL;
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



 

 
