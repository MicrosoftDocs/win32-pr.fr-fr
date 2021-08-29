---
title: IMsRdpDeviceV2 propriété DeviceText
description: Contient le texte de l’appareil.
ms.assetid: 2a67e8d4-2af3-4738-ade2-a79800aea4a1
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété DeviceText
- Services Bureau à distance de la propriété DeviceText, interface IMsRdpDeviceV2
- Services Bureau à distance de l’interface IMsRdpDeviceV2, propriété DeviceText
topic_type:
- apiref
api_name:
- IMsRdpDeviceV2.DeviceText
- IMsRdpDeviceV2.get_DeviceText
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ed156a56215c859455cd16cb5d4ae0396eb24a0b62c8b9ae0ee6d5a43bd2ad3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119138602"
---
# <a name="imsrdpdevicev2devicetext-property"></a>IMsRdpDeviceV2 ::D propriété eviceText

Contient le texte de l’appareil. il s’agit du nom que Windows affiche à l’utilisateur.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_DeviceText(
  [out, retval] BSTR *pDeviceText
);
```



## <a name="property-value"></a>Valeur de la propriété

Nom complet du périphérique.

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

 

 





