---
title: IMsRdpDevice propriété DeviceInstanceId
description: Récupère l’identificateur d’instance d’appareil de l’appareil.
ms.assetid: 54bdda17-39da-4821-9ac3-2ce80f5015f4
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété DeviceInstanceId
- Services Bureau à distance de la propriété DeviceInstanceId, interface IMsRdpDevice
- Services Bureau à distance de l’interface IMsRdpDevice, propriété DeviceInstanceId
topic_type:
- apiref
api_name:
- IMsRdpDevice.DeviceInstanceId
- IMsRdpDevice.get_DeviceInstanceId
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74fd93b775d3fd239435a984cf0f0b7518558f3f57e92525365764da580f499c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118606815"
---
# <a name="imsrdpdevicedeviceinstanceid-property"></a>IMsRdpDevice ::D propriété eviceInstanceId

Récupère l’identificateur d’instance d’appareil de l’appareil.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_DeviceInstanceId(
  [out] BSTR *pDevInstanceId
);
```



## <a name="property-value"></a>Valeur de la propriété

Identificateur de l’instance de l’appareil.

## <a name="error-codes"></a>Codes d’erreur

Si la méthode est réussie, **S \_ OK** est retourné. Toute autre valeur **HRESULT** indique que l’appel a échoué.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                               |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                         |
| Bibliothèque de types<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsRdpDevice est défini en tant que 60c3b9c8-9E92-4f5e-a3e7-604a912093ea<br/>        |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMsRdpDevice**](imsrdpdevice.md)
</dt> </dl>

 

 





