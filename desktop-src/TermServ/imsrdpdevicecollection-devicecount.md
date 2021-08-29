---
title: IMsRdpDeviceCollection propriété DeviceCount
description: Récupère le nombre d’objets dans la collection. | IMsRdpDeviceCollection propriété DeviceCount
ms.assetid: dc44f3b8-52c4-4e5f-a633-ea7555fd01dd
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété DeviceCount
- Services Bureau à distance de la propriété DeviceCount, interface IMsRdpDeviceCollection
- Services Bureau à distance de l’interface IMsRdpDeviceCollection, propriété DeviceCount
topic_type:
- apiref
api_name:
- IMsRdpDeviceCollection.DeviceCount
- IMsRdpDeviceCollection.get_DeviceCount
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f178cb7dd72ece90a85fe558f371f3d0b63b3c233a1e43054fe4f72f09850003
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120033059"
---
# <a name="imsrdpdevicecollectiondevicecount-property"></a>IMsRdpDeviceCollection ::D propriété eviceCount

Récupère le nombre d’objets dans la collection.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_DeviceCount(
  [out] ULONG *pDeviceCount
);
```



## <a name="property-value"></a>Valeur de la propriété

Nombre d’objets.

## <a name="error-codes"></a>Codes d’erreur

Si la méthode est réussie, **S \_ OK** est retourné. Toute autre valeur **HRESULT** indique que l’appel a échoué.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                  |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                            |
| Bibliothèque de types<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>    |
| IID<br/>                      | IID \_ IMsRdpDeviceCollection est défini comme 56540617-D281-488C-8738-6a8fdf64a118<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMsRdpDeviceCollection**](imsrdpdevicecollection.md)
</dt> </dl>

 

 





