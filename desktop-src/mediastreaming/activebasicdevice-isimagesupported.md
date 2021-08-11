---
title: ActiveBasicDevice IsImageSupported, propriété (PlayToDevice. h)
description: Obtient une valeur qui indique si l’appareil prend en charge les images.
ms.assetid: FC53B87C-D739-4AD4-9DD3-415AC8692224
keywords:
- API de diffusion multimédia en continu des propriétés IsImageSupported
- API de diffusion multimédia en continu des propriétés IsImageSupported, interface ActiveBasicDevice
- API de diffusion multimédia en continu de l’interface ActiveBasicDevice, propriété IsImageSupported
topic_type:
- apiref
api_name:
- ActiveBasicDevice.IsImageSupported
- ActiveBasicDevice.get_IsImageSupported
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a147c5156f07c6cc6461cafcf8dc778013a7eb3048d1428f854b844d24f5642a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118236710"
---
# <a name="activebasicdeviceisimagesupported-property"></a>ActiveBasicDevice :: IsImageSupported, propriété

Obtient une valeur qui indique si l’appareil prend en charge les images.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_IsImageSupported(
  [out] boolean *value
);
```



## <a name="property-value"></a>Valeur de la propriété

Pointeur vers une **valeur booléenne** qui indique si l’appareil prend en charge les images.

**true** si l’appareil prend en charge les images ; Sinon, **false**.

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

 

