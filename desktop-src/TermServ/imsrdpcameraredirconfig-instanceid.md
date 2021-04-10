---
title: IMsRdpCameraRedirConfig InstanceId, propriété
description: Obtient l’ID d’instance de l’appareil photo.
ms.tgt_platform: multiple
keywords:
- Propriété InstanceId Services Bureau à distance
- InstanceId, propriété Services Bureau à distance, IMsRdpCameraRedirConfig, interface
- Services Bureau à distance de l’interface IMsRdpCameraRedirConfig, propriété InstanceId
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfig.InstanceId
- IMsRdpCameraRedirConfig.get_InstanceId
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 42654e84f64b25a051a78963339ca95d4ebf760f
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/19/2020
ms.locfileid: "104200635"
---
# <a name="imsrdpcameraredirconfiginstanceid-property"></a>IMsRdpCameraRedirConfig :: InstanceId, propriété

Obtient l’ID d’instance de l’appareil photo.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe

```C++
HRESULT get_InstanceId(
    [out, retval] BSTR* pInstanceId
);
```

## <a name="property-value"></a>Valeur de la propriété

ID d’instance de l’appareil photo.

## <a name="requirements"></a>Configuration requise

| Condition requise | Valeur |
|-------------------------------------|---------------------------------------|
| Client minimal pris en charge| Windows 10, version 1803 (build 17134)      |
| Bibliothèque de types            | MsTscAx.dll                        |
| DLL                  | MsTscAx.dll     |
| IID                      | IID \_ IMsRdpCameraRedirConfig est défini comme 09750604-D625-47C1-9FCD-F09F735705D7            |

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMsRdpCameraRedirConfig**](imsrdpcameraredirconfig.md)
</dt> </dl>