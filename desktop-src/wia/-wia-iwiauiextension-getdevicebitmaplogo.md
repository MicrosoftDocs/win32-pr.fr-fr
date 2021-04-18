---
description: Obtient un logo de bitmap personnalisé pour l’appareil.
ms.assetid: 56b3c7c9-64f4-4853-9eb7-d876d02a851f
title: 'IWiaUIExtension :: GetDeviceBitmapLogo, méthode (Wiadevd. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaUIExtension.GetDeviceBitmapLogo
api_type:
- COM
api_location:
- Wiadevd.h
ms.openlocfilehash: 51db237c93a2167eb3c4bdae648f9d79da13319a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106512984"
---
# <a name="iwiauiextensiongetdevicebitmaplogo-method"></a>IWiaUIExtension :: GetDeviceBitmapLogo, méthode

Obtient un logo de bitmap personnalisé pour l’appareil.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetDeviceBitmapLogo(
  [in]  BSTR    bstrDeviceId,
  [out] HBITMAP *phBitmap,
  [in]  ULONG   nMaxWidth,
  [in]  ULONG   nMaxHeight
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*bstrDeviceId* \[ dans\]
</dt> <dd>

Type : **BSTR**

Spécifie l’ID d’appareil de l’appareil WIA pour lequel l’icône doit être obtenue.

</dd> <dt>

*phBitmap* \[ à\]
</dt> <dd>

Type : **HBITMAP \** _

Pointe vers un emplacement de mémoire qui recevra un handle pour le logo bitmap de l’appareil.

</dd> <dt>

_nMaxWidth * \[ dans\]
</dt> <dd>

Type : **ULong**

Spécifie la largeur souhaitée de la bitmap.

</dd> <dt>

*nMaxHeight* \[ dans\]
</dt> <dd>

Type : **ULong**

Spécifie la hauteur souhaitée de la bitmap.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **HRESULT**

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                 |
| En-tête<br/>                   | <dl> <dt>Wiadevd. h</dt> </dl> |



 

 




