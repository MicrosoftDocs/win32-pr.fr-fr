---
title: IMsRdpDeviceV2 propriété IsOptionalDevice
description: Spécifie si l’appareil est facultatif pour la redirection USB.
ms.assetid: a7226c40-7e22-48af-9895-b1fb1f861b58
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété IsOptionalDevice
- Services Bureau à distance de la propriété IsOptionalDevice, interface IMsRdpDeviceV2
- Services Bureau à distance de l’interface IMsRdpDeviceV2, propriété IsOptionalDevice
topic_type:
- apiref
api_name:
- IMsRdpDeviceV2.IsOptionalDevice
- IMsRdpDeviceV2.get_IsOptionalDevice
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81cf24e08b8d6c485d08341769391061261b388b7a69c8e887fa094dfd1f03b5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120125659"
---
# <a name="imsrdpdevicev2isoptionaldevice-property"></a>IMsRdpDeviceV2 :: IsOptionalDevice, propriété

Spécifie si l’appareil est facultatif pour la redirection USB.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_IsOptionalDevice(
  [out, retval] VARIANT_BOOL *pvboolOptionalDevice
);
```



## <a name="property-value"></a>Valeur de la propriété

**true** si l’appareil est un facultatif ; Sinon, **false**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 7 avec SP1<br/>                                                          |
| Serveur minimal pris en charge<br/> | Windows Server 2008 R2 avec SP1<br/>                                             |
| Bibliothèque de types<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsRdpDeviceV2 est défini en tant que 5fb94466-7661-42a8-98b7-01904c11668f<br/>      |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMsRdpDeviceV2**](imsrdpdevicev2.md)
</dt> </dl>

 

 





