---
description: 'Vérifie si une extension spécifiée est disponible sur l’ordinateur et si elle peut être utilisée par la méthode IWiaItem2 :: GetExtension.'
ms.assetid: 672f6418-4ce3-4570-a412-fe639c9f5eb8
title: 'IWiaItem2 :: CheckExtension, méthode (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.CheckExtension
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 50240fbf10155fae555c6cd2e30bf8c86c571b8d52b86e02eab9f5bb11ac17ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118965578"
---
# <a name="iwiaitem2checkextension-method"></a>IWiaItem2 :: CheckExtension, méthode

Vérifie si une extension spécifiée est disponible sur l’ordinateur et si elle peut être utilisée par la méthode [**IWiaItem2 :: GetExtension**](-wia-iwiaitem2-getextension.md) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT CheckExtension(
  [in]  LONG   lFlags,
  [in]  BSTR   bstrName,
  [in]  REFIID riidExtensionInterface,
  [out] BOOL   *pbExtensionExists
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

Spécifie le nom de l'extension.

</dd> <dt>

*riidExtensionInterface* \[ dans\]
</dt> <dd>

Type : **REFIID**

Actuellement inutilisé.

</dd> <dt>

*pbExtensionExists* \[ à\]
</dt> <dd>

Type : **bool \***

Reçoit un pointeur vers un **booléen**.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**FAUSSES**


</dt> <dd>

L’extension spécifiée n’est pas disponible.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**:**


</dt> <dd>

L’extension spécifiée est disponible.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **HRESULT**

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Remarques

À l’aide de cette méthode, les applications peuvent vérifier si une extension est disponible avant d’appeler la méthode [**IWiaItem2 :: GetExtension**](-wia-iwiaitem2-getextension.md) . En outre, l’application peut vérifier les extensions qui sont disponibles sans co-créer chacune d’elles, puis choisir celle qui doit être utilisée.

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



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 




