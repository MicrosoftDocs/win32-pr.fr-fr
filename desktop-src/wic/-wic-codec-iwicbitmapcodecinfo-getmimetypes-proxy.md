---
description: Fonction proxy pour la méthode GetMimeTypes.
ms.assetid: 9d05624f-da08-4475-933b-faa12bec9012
title: IWICBitmapCodecInfo_GetMimeTypes_Proxy fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapCodecInfo_GetMimeTypes_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: eb00b2ae3cd935171a9333a55a76038ef9ae2ed8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525935"
---
# <a name="iwicbitmapcodecinfo_getmimetypes_proxy-function"></a>IWICBitmapCodecInfo \_ \_ fonction proxy GetMimeTypes

Fonction proxy pour la méthode [**GetMimeTypes**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecinfo-getmimetypes) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT IWICBitmapCodecInfo_GetMimeTypes_Proxy(
  _In_  IWICBitmapCodecInfo *THIS_PTR,
  _In_  UINT                cchMimeTypes,
  _Out_ WCHAR               *wzMimeTypes,
  _Out_ UINT                *pcchActual
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Ce \_ PTR* \[ dans\]
</dt> <dd>

Tapez : **[**IWICBitmapCodecInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) \** _

Pointeur vers cet objet [_ *IWICBitmapCodecInfo* *](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) .

</dd> <dt>

*cchMimeTypes* \[ dans\]
</dt> <dd>

Type : **uint**

Taille de la mémoire tampon des types MIME.

</dd> <dt>

*wzMimeTypes* \[ à\]
</dt> <dd>

Type : **WCHAR \** _

Pointeur qui reçoit les types MIME associés au codec.

</dd> <dt>

_pcchActual * \[ out\]
</dt> <dd>

Type : **uint \** _

Taille réelle de la mémoire tampon nécessaire pour récupérer tous les types MIME associés au codec.

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



 

 




