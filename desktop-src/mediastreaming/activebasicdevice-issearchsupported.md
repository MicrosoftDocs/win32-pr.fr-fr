---
title: ActiveBasicDevice IsSearchSupported, propriété (PlayToDevice. h)
description: Obtient une valeur qui indique si l’appareil prend en charge la recherche.
ms.assetid: 091D467A-1FF6-4635-BF89-4E62AC9C660A
keywords:
- API de diffusion multimédia en continu des propriétés IsSearchSupported
- API de diffusion multimédia en continu des propriétés IsSearchSupported, interface ActiveBasicDevice
- API de diffusion multimédia en continu de l’interface ActiveBasicDevice, propriété IsSearchSupported
topic_type:
- apiref
api_name:
- ActiveBasicDevice.IsSearchSupported
- ActiveBasicDevice.get_IsSearchSupported
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff97b20697388b1e3079f6993b97b948fa12091e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385207"
---
# <a name="activebasicdeviceissearchsupported-property"></a>ActiveBasicDevice :: IsSearchSupported, propriété

Obtient une valeur qui indique si l’appareil prend en charge la recherche.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_IsSearchSupported(
  [out] boolean *value
);
```



## <a name="property-value"></a>Valeur de la propriété

Pointeur vers une **valeur booléenne** qui indique si l’appareil prend en charge la recherche.

**true** si l’appareil prend en charge la recherche ; Sinon, **false**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8.1 les \[ applications de bureau uniquement\]<br/>                                                |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 R2 \[ uniquement\]<br/>                                     |
| En-tête<br/>                   | <dl> <dt>PlayToDevice. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>PlayToDevice. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Playtodevice.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))
</dt> </dl>

 

