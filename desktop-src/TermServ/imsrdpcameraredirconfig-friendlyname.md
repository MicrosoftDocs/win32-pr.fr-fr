---
title: IMsRdpCameraRedirConfig FriendlyName, propriété
description: Obtient le nom convivial de l’appareil photo.
ms.tgt_platform: multiple
keywords:
- FriendlyName, propriété Services Bureau à distance
- FriendlyName, propriété Services Bureau à distance, interface IMsRdpCameraRedirConfig
- Services Bureau à distance de l’interface IMsRdpCameraRedirConfig, propriété FriendlyName
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfig.FriendlyName
- IMsRdpCameraRedirConfig.get_FriendlyName
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 31d6d775310d23cfe8a9cf8ab95ea56e9e2b2d0e418fc9d1a55d3cf26fcce26e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119737409"
---
# <a name="imsrdpcameraredirconfigfriendlyname-property"></a>IMsRdpCameraRedirConfig :: FriendlyName, propriété

Obtient le nom convivial de l’appareil photo.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe

```C++
HRESULT get_FriendlyName(
    [out, retval] BSTR* pFriendlyName
);
```

## <a name="property-value"></a>Valeur de la propriété

Nom convivial de l’appareil photo.

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