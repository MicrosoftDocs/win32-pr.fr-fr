---
description: Fonction proxy pour la méthode InitializePredefined.
ms.assetid: 78137d43-c32f-4d60-b289-2e2154cf4d1e
title: IWICPalette_InitializePredefined_Proxy fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICPalette_InitializePredefined_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 4ae1113dfba184490347bb8e255a0751884fd36c81cb8bbe337af771cd01d2ff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119812189"
---
# <a name="iwicpalette_initializepredefined_proxy-function"></a>IWICPalette \_ \_ fonction proxy InitializePredefined

Fonction proxy pour la méthode [**InitializePredefined**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpalette-initializepredefined) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT IWICPalette_InitializePredefined_Proxy(
  _In_ IWICPalette          *THIS_PTR,
  _In_ WICBitmapPaletteType ePaletteType,
  _In_ BOOL                 fAddTransparentColor
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Ce \_ PTR* \[ dans\]
</dt> <dd>

Type : **[ **IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\***

Pointeur vers cet objet [**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) .

</dd> <dt>

*ePaletteType* \[ dans\]
</dt> <dd>

Type : **[ **WICBitmapPaletteType**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmappalettetype)**

Type de palette prédéfinie souhaité.

</dd> <dt>

*fAddTransparentColor* \[ dans\]
</dt> <dd>

Type : **bool**

Couleur tranparent facultative à ajouter à la palette. Si aucune couleur transparente n’est nécessaire, utilisez 0.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **HRESULT**

Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Notes

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows XP avec SP2, Windows les \[ applications de bureau Vista uniquement\]<br/>                                                                                              |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                                                                                             |
| DLL<br/>                      | <dl> <dt>Windowscodecs.dll ; </dt> <dt>Wincodec. lib</dt> </dl> |



 

 




