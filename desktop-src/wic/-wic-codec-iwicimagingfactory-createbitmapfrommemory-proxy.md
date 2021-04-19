---
description: Fonction proxy pour la méthode CreateBitmapFromMemory.
ms.assetid: 5aa455d5-23e3-4738-b028-b84da0fb0c50
title: IWICImagingFactory_CreateBitmapFromMemory_Proxy fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateBitmapFromMemory_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 79893952bb6dcdbab6c4a1cea4f57355831d31c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106535535"
---
# <a name="iwicimagingfactory_createbitmapfrommemory_proxy-function"></a>IWICImagingFactory \_ \_ fonction proxy CreateBitmapFromMemory

Fonction proxy pour la méthode [**CreateBitmapFromMemory**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createbitmapfrommemory) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT IWICImagingFactory_CreateBitmapFromMemory_Proxy(
  _In_  IWICImagingFactory    *pFactory,
  _In_  UINT                  uiWidth,
  _In_  UINT                  uiHeight,
  _In_  REFWICPixelFormatGUID pixelFormat,
  _In_  UINT                  cbStride,
  _In_  UINT                  cbBufferSize,
  _In_  BYTE                  *pbBuffer,
  _Out_ IWICBitmap            **ppIBitmap
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pFactory* \[ dans\]
</dt> <dd>

Tapez : **[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _

</dd> <dt>

_uiWidth * \[ dans\]
</dt> <dd>

Type : **uint**

Largeur de la nouvelle bitmap.

</dd> <dt>

*uiHeight* \[ dans\]
</dt> <dd>

Type : **uint**

Hauteur de la nouvelle bitmap.

</dd> <dt>

*PixelFormat* \[ dans\]
</dt> <dd>

Type : **REFWICPixelFormatGUID**

Format de pixel de la nouvelle bitmap.

</dd> <dt>

*cbStride* \[ dans\]
</dt> <dd>

Type : **uint**

[*Stride*](/windows) des données de pixels données.

</dd> <dt>

*cbBufferSize* \[ dans\]
</dt> <dd>

Type : **uint**

Taille de *pbBuffer*.

</dd> <dt>

*pbBuffer* \[ dans\]
</dt> <dd>

Type : **Byte \** _

Mémoire tampon utilisée pour créer l’image bitmap.

</dd> <dt>

_ppIBitmap * \[ out\]
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



 

