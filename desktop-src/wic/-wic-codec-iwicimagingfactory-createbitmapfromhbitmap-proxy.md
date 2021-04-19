---
description: Fonction proxy pour la méthode CreateBitmapFromHBITMAP.
ms.assetid: e4e9a6b4-00d9-4f87-aeec-f2c02c3f44ab
title: IWICImagingFactory_CreateBitmapFromHBITMAP_Proxy fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateBitmapFromHBITMAP_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 6599a9699e6fb83c1678cd0360f906cc8e0668c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106523366"
---
# <a name="iwicimagingfactory_createbitmapfromhbitmap_proxy-function"></a>IWICImagingFactory \_ \_ fonction proxy CreateBitmapFromHBITMAP

Fonction proxy pour la méthode [**CreateBitmapFromHBITMAP**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createbitmapfromhbitmap) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT IWICImagingFactory_CreateBitmapFromHBITMAP_Proxy(
  _In_  IWICImagingFactory          *pFactory,
  _In_  HBITMAP                     hBitmap,
  _In_  HPALETTE                    hPalette,
  _In_  WICBitmapAlphaChannelOption options,
  _Out_ IWICBitmap                  **ppIBitmap
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pFactory* \[ dans\]
</dt> <dd>

Tapez : **[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _

</dd> <dt>

_hBitmap * \[ dans\]
</dt> <dd>

Type : **HBITMAP**

Handle de bitmap à partir duquel créer l’image bitmap.

</dd> <dt>

*HPALETTE* \[ dans\]
</dt> <dd>

Type : **HPALETTE**

Handle de palette utilisé pour créer l’image bitmap.

</dd> <dt>

*options* \[ dans\]
</dt> <dd>

Type : **[ **WICBitmapAlphaChannelOption**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapalphachanneloption)**

Options de canal alpha pour créer l’image bitmap.

</dd> <dt>

*ppIBitmap* \[ à\]
</dt> <dd>

Type : **[ **IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)\*\***

Pointeur qui reçoit un pointeur vers la nouvelle bitmap.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **HRESULT**

Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Notes

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows XP avec SP2, applications de \[ Bureau Windows Vista uniquement\]<br/>                                                                                              |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                                                                                             |
| DLL<br/>                      | <dl> <dt>Windowscodecs.dll ; </dt> <dt>Wincodec. lib</dt> </dl> |



 

 




