---
title: ActiveBasicDevice IsMuteSupported, propriété (PlayToDevice. h)
description: Obtient une valeur qui indique si l’appareil prend en charge le silence de l’audio.
ms.assetid: FF4B533F-B416-4DBE-BF86-FA34E785FFA2
keywords:
- API de diffusion multimédia en continu des propriétés IsMuteSupported
- API de diffusion multimédia en continu des propriétés IsMuteSupported, interface ActiveBasicDevice
- API de diffusion multimédia en continu de l’interface ActiveBasicDevice, propriété IsMuteSupported
topic_type:
- apiref
api_name:
- ActiveBasicDevice.IsMuteSupported
- ActiveBasicDevice.get_IsMuteSupported
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0fad8352504a6c950bb76206f05c77c5baa9f3baed2f1144a1d6c165e380a4b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118236647"
---
# <a name="activebasicdeviceismutesupported-property"></a>ActiveBasicDevice :: IsMuteSupported, propriété

Obtient une valeur qui indique si l’appareil prend en charge le silence de l’audio.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_IsMuteSupported(
  [out] boolean *value
);
```



## <a name="property-value"></a>Valeur de la propriété

Pointeur vers une **valeur booléenne** qui indique si l’appareil prend en charge le silence de l’audio.

**true** si l’appareil prend en charge le silence de l’audio ; Sinon, **false**.

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

 

