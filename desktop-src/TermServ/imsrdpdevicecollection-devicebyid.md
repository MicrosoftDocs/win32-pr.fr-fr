---
title: IMsRdpDeviceCollection propriété DeviceById
description: Récupère l’appareil avec l’identificateur spécifié.
ms.assetid: b64e83fa-5a94-4080-8efa-45cbfe5ceb88
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété DeviceById
- Services Bureau à distance de la propriété DeviceById, interface IMsRdpDeviceCollection
- Services Bureau à distance de l’interface IMsRdpDeviceCollection, propriété DeviceById
topic_type:
- apiref
api_name:
- IMsRdpDeviceCollection.DeviceById
- IMsRdpDeviceCollection.get_DeviceById
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 228e3c7cf03457ca740d4a415257008988215077
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465130"
---
# <a name="imsrdpdevicecollectiondevicebyid-property"></a>IMsRdpDeviceCollection ::D propriété eviceById

Récupère l’appareil avec l’identificateur spécifié.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_DeviceById(
  [in]          BSTR devInstanceId,
  [out, retval] IMsRdpDevice **ppDevice
);
```



## <a name="property-value"></a>Valeur de la propriété

Pointeur d’interface [**IMsRdpDevice**](imsrdpdevice.md) .

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

 

 





