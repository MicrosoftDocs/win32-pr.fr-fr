---
title: ActiveBasicDevice IsSetNextSourceSupported, propriété (PlayToDevice. h)
description: Obtient une valeur qui indique si la définition de la source suivante est prise en charge.
ms.assetid: 0888A737-D2CC-4259-BC60-9D2B8E8302A0
keywords:
- API de diffusion multimédia en continu des propriétés IsSetNextSourceSupported
- API de diffusion multimédia en continu des propriétés IsSetNextSourceSupported, interface ActiveBasicDevice
- API de diffusion multimédia en continu de l’interface ActiveBasicDevice, propriété IsSetNextSourceSupported
topic_type:
- apiref
api_name:
- ActiveBasicDevice.IsSetNextSourceSupported
- ActiveBasicDevice.get_IsSetNextSourceSupported
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e7db7bc917ab8f901d32772fdc756f11b74f5dfabc2f31d44bfab12aad023e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119952789"
---
# <a name="activebasicdeviceissetnextsourcesupported-property"></a>ActiveBasicDevice :: IsSetNextSourceSupported, propriété

Obtient une valeur qui indique si la définition de la source suivante est prise en charge.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_IsSetNextSourceSupported(
  [out] boolean *value
);
```



## <a name="property-value"></a>Valeur de la propriété

Pointeur vers une **valeur booléenne** qui indique si la définition de la source suivante est prise en charge.

**true** si la définition de la source suivante est prise en charge ; Sinon, **false**.

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

 

