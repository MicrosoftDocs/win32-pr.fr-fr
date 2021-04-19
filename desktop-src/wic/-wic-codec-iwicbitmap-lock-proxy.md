---
description: Fonction proxy pour la méthode Lock.
ms.assetid: c9d67b35-092b-4f0b-a292-879576a046bf
title: IWICBitmap_Lock_Proxy fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmap_Lock_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: cf07a0afc0fbd2629ffe54b543271014d5817d71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516861"
---
# <a name="iwicbitmap_lock_proxy-function"></a>IWICBitmap \_ \_ fonction proxy Lock

Fonction proxy pour la méthode [**Lock**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmap-lock) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT IWICBitmap_Lock_Proxy(
  _In_        IWICBitmap     *THIS_PTR,
  _In_  const WICRect        *prcLock,
  _In_        DWORD          flags,
  _Out_       IWICBitmapLock **ppILock
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Ce \_ PTR* \[ dans\]
</dt> <dd>

Tapez : **[**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) \** _

Pointeur vers cet objet [_ *IWICBitmap* *](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) .

</dd> <dt>

*prcLock* \[ dans\]
</dt> <dd>

Type : **const [**WICRect**](/windows/desktop/api/Wincodec/ns-wincodec-wicrect) \** _

Rectangle auquel accéder.

</dd> <dt>

_flags * \[ dans\]
</dt> <dd>

Type : **DWORD**

Mode d’accès que vous souhaitez obtenir pour le verrou.

</dd> <dt>

*ppILock* \[ à\]
</dt> <dd>

Type : **[ **IWICBitmapLock**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock)\*\***

Pointeur qui reçoit l’emplacement de mémoire verrouillée.

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



 

 




