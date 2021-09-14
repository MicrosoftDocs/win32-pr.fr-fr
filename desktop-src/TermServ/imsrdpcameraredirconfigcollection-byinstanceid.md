---
title: IMsRdpCameraRedirConfigCollection ByInstanceId, propriété
description: Retourne un objet IMsRdpCameraRedirConfig de la collection qui correspond à l’ID d’instance spécifié.
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété ByInstanceId
- Services Bureau à distance de la propriété ByInstanceId, interface IMsRdpCameraRedirConfigCollection
- Services Bureau à distance de l’interface IMsRdpCameraRedirConfigCollection, propriété ByInstanceId
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfigCollection.ByInstanceId
- IMsRdpCameraRedirConfigCollection.get_ByInstanceId
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: d90cb7d2f309a3df9e354ace04a840b667e5569b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126917012"
---
# <a name="imsrdpcameraredirconfigcollectionbyinstanceid-property"></a>IMsRdpCameraRedirConfigCollection :: ByInstanceId, propriété

Retourne un objet [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) de la collection qui correspond à l’ID d’instance spécifié.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe

```C++
HRESULT get_ByInstanceId(
    [in]          BSTR instanceId,
    [out, retval] IMsRdpCameraRedirConfig** ppConfig
);
```

## <a name="property-value"></a>Valeur de la propriété

Objet [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) qui correspond à l’ID d’instance spécifié.

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