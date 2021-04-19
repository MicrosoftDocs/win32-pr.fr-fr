---
description: Fonction proxy pour la méthode CreateBitmapFromHICON.
ms.assetid: 5df3d9d9-1b23-4f38-b97e-0b77d6db99d8
title: IWICImagingFactory_CreateBitmapFromHICON_Proxy fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateBitmapFromHICON_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 58f9f37dc27c76a9eaa55d6baec52efbb773343e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534059"
---
# <a name="iwicimagingfactory_createbitmapfromhicon_proxy-function"></a>IWICImagingFactory \_ \_ fonction proxy CreateBitmapFromHICON

Fonction proxy pour la méthode [**CreateBitmapFromHICON**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createbitmapfromhicon) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT IWICImagingFactory_CreateBitmapFromHICON_Proxy(
  _In_  IWICImagingFactory *pFactory,
  _In_  HICON              hIcon,
  _Out_ IWICBitmap         **ppIBitmap
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pFactory* \[ dans\]
</dt> <dd>

Tapez : **[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _

</dd> <dt>

_hIcon * \[ dans\]
</dt> <dd>

Type : **HICON**

Handle d’icône à partir duquel créer la nouvelle bitmap.

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



 

 




