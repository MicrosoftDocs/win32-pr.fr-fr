---
title: IMsRdpCameraRedirConfig ParentInstanceId, propriété
description: Obtient l’ID d’instance d’appareil parent de l’appareil photo.
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété ParentInstanceId
- Services Bureau à distance de la propriété ParentInstanceId, interface IMsRdpCameraRedirConfig
- Services Bureau à distance de l’interface IMsRdpCameraRedirConfig, propriété ParentInstanceId
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfig.ParentInstanceId
- IMsRdpCameraRedirConfig.get_ParentInstanceId
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 149e4f536996376193596db6c4fd4cf659637c05bb92e3afcdb7ee78c480b893
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119574559"
---
# <a name="imsrdpcameraredirconfigparentinstanceid-property"></a>IMsRdpCameraRedirConfig ::P propriété arentInstanceId

Obtient l’ID d’instance d’appareil parent de l’appareil photo.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe

```C++
HRESULT get_ParentInstanceId(
    [out, retval] BSTR* pParentInstanceId
);
```

## <a name="property-value"></a>Valeur de la propriété

ID d’instance d’appareil parent de l’appareil photo.

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