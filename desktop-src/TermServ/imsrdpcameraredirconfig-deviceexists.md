---
title: IMsRdpCameraRedirConfig DeviceExists property
description: Spécifie si le périphérique de l’appareil photo existe actuellement (c’est-à-dire que l’appareil photo est connecté).
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété DeviceExists
- Services Bureau à distance de la propriété DeviceExists, interface IMsRdpCameraRedirConfig
- Services Bureau à distance de l’interface IMsRdpCameraRedirConfig, propriété DeviceExists
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfig.DeviceExists
- IMsRdpCameraRedirConfig.get_DeviceExists
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 617c91491d88736ca60218d71f9dd5aa02ad0f9faeefdda6b872ba9262cec587
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119990659"
---
# <a name="imsrdpcameraredirconfigdeviceexists-property"></a>IMsRdpCameraRedirConfig ::D propriété eviceExists

Spécifie si le périphérique de l’appareil photo existe actuellement (c’est-à-dire que l’appareil photo est connecté).

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe

```C++
HRESULT get_DeviceExists(
    [out, retval] VARIANT_BOOL* pfExists
);
```

## <a name="property-value"></a>Valeur de la propriété

Valeur qui indique si le périphérique de l’appareil photo existe actuellement (c’est-à-dire que l’appareil photo est connecté).

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