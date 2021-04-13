---
title: ActiveBasicDevice PhysicalNetworkInterface, propriété (PlayToDevice. h)
description: Obtient l’ID de l’interface réseau physique.
ms.assetid: F426462F-CE26-4EE1-B679-A4C80B2919A5
keywords:
- API de diffusion multimédia en continu des propriétés PhysicalNetworkInterface
- API de diffusion multimédia en continu des propriétés PhysicalNetworkInterface, interface ActiveBasicDevice
- API de diffusion multimédia en continu de l’interface ActiveBasicDevice, propriété PhysicalNetworkInterface
topic_type:
- apiref
api_name:
- ActiveBasicDevice.PhysicalNetworkInterface
- ActiveBasicDevice.get_PhysicalNetworkInterface
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 479618ed4d22a3d78a351fb88fcb1108a27c618f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465742"
---
# <a name="activebasicdevicephysicalnetworkinterface-property"></a>ActiveBasicDevice ::P propriété hysicalNetworkInterface

Obtient l’ID de l’interface réseau physique.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_PhysicalNetworkInterface(
  [out] GUID *value
);
```



## <a name="property-value"></a>Valeur de la propriété

Pointeur vers un **GUID** qui spécifie l’ID de l’interface réseau physique.

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

 

