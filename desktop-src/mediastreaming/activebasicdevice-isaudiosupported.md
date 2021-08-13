---
title: ActiveBasicDevice IsAudioSupported, propriété (PlayToDevice. h)
description: Obtient une valeur qui indique si l’appareil prend en charge l’audio.
ms.assetid: 22ABB97B-58E7-4C21-B359-C10DFC9C7194
keywords:
- API de diffusion multimédia en continu des propriétés IsAudioSupported
- API de diffusion multimédia en continu des propriétés IsAudioSupported, interface ActiveBasicDevice
- API de diffusion multimédia en continu de l’interface ActiveBasicDevice, propriété IsAudioSupported
topic_type:
- apiref
api_name:
- ActiveBasicDevice.IsAudioSupported
- ActiveBasicDevice.get_IsAudioSupported
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20125114b6cd134d153ad6425af5af410faf524714a2e505a37fbf57dcda21e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119462421"
---
# <a name="activebasicdeviceisaudiosupported-property"></a>ActiveBasicDevice :: IsAudioSupported, propriété

Obtient une valeur qui indique si l’appareil prend en charge l’audio.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_IsAudioSupported(
  [out] boolean *value
);
```



## <a name="property-value"></a>Valeur de la propriété

Pointeur vers une **valeur booléenne** qui indique si l’appareil prend en charge l’audio.

**true** si l’appareil prend en charge l’audio ; Sinon, **false**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8.1 les \[ applications de bureau uniquement\]<br/>                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[Applications de bureau R2 uniquement\]<br/>                                     |
| En-tête<br/>                   | <dl> <dt>PlayToDevice. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>PlayToDevice. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Playtodevice.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))
</dt> </dl>

 

