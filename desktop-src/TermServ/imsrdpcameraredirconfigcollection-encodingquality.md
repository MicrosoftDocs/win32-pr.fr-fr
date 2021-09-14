---
title: IMsRdpCameraRedirConfigCollection EncodingQuality, propriété
description: Spécifie la qualité d’encodage (vitesse de transmission).
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété EncodingQuality
- Services Bureau à distance de la propriété EncodingQuality, interface IMsRdpCameraRedirConfigCollection
- Services Bureau à distance de l’interface IMsRdpCameraRedirConfigCollection, propriété EncodingQuality
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfigCollection.EncodingQuality
- IMsRdpCameraRedirConfigCollection.put_EncodingQuality
- IMsRdpCameraRedirConfigCollection.get_EncodingQuality
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: d8044c2fb70233243a3a74d8dc5faac96873cb48
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126916987"
---
# <a name="imsrdpcameraredirconfigcollectionencodingquality-property"></a>IMsRdpCameraRedirConfigCollection :: EncodingQuality, propriété

Spécifie la qualité d’encodage (vitesse de transmission).

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe

```C++
HRESULT put_EncodingQuality(
    [in] CameraRedirEncodingQuality encodingQuality
);

HRESULT get_EncodingQuality(
    [out, retval] CameraRedirEncodingQuality* pEncodingQuality
);
```

## <a name="property-value"></a>Valeur de la propriété

L’une des valeurs d’énumération **CameraRedirEncodingQuality** suivantes qui spécifient la qualité d’encodage (vitesse de transmission).

| Nom du membre enum | Valeur |
|-----------------|--------|
| encodingQualityLow | 0x0000 |
| encodingQualityMedium | 0x0001 |
| encodingQualityHigh | 0x0002 |

## <a name="requirements"></a>Spécifications

| Condition requise | Valeur |
|-------------------------------------|---------------------------------------|
| Client minimal pris en charge| Windows 10, version 1803 (build 17134)      |
| Bibliothèque de types            | MsTscAx.dll                        |
| DLL                  | MsTscAx.dll     |
| IID                      | IID \_ IMsRdpCameraRedirConfigCollection est défini en tant que AE45252B-aaab-4504-B681-649D6073A37A          |

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMsRdpCameraRedirConfigCollection**](imsrdpcameraredirconfigcollection.md)
</dt> </dl>