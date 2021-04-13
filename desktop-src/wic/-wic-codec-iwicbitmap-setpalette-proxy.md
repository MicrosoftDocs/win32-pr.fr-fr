---
description: Fonction proxy pour la méthode SetPalette.
ms.assetid: 3fd60833-7f21-4654-883a-2dd88c403bc8
title: IWICBitmap_SetPalette_Proxy fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmap_SetPalette_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: d683dda81d52818bfc7d878d044af9b4e09869b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525941"
---
# <a name="iwicbitmap_setpalette_proxy-function"></a>IWICBitmap \_ \_ fonction proxy SetPalette

Fonction proxy pour la méthode [**SetPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmap-setpalette) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT IWICBitmap_SetPalette_Proxy(
  _In_ IWICBitmap  *THIS_PTR,
  _In_ IWICPalette *pIPalette
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Ce \_ PTR* \[ dans\]
</dt> <dd>

Tapez : **[**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) \** _

Pointeur vers cet objet [_ *IWICBitmap* *](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) .

</dd> <dt>

*pIPalette* \[ dans\]
</dt> <dd>

Tapez : **[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) \** _

Palette à utiliser pour la conversion.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : _ *HRESULT**

Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Notes

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows XP avec SP2, applications de \[ Bureau Windows Vista uniquement\]<br/>                                                                                              |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                                                                                             |
| DLL<br/>                      | <dl> <dt>Windowscodecs.dll ; </dt> <dt>Wincodec. lib</dt> </dl> |



 

 




