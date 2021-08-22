---
title: IMsRdpCameraRedirConfigCollection ByIndex, propriété
description: Retourne un objet IMsRdpCameraRedirConfig par son index dans la collection.
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété ByIndex
- Services Bureau à distance de la propriété ByIndex, interface IMsRdpCameraRedirConfigCollection
- Services Bureau à distance de l’interface IMsRdpCameraRedirConfigCollection, propriété ByIndex
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfigCollection.ByIndex
- IMsRdpCameraRedirConfigCollection.get_ByIndex
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 375c0b110975c6ca791bbbe1f61a5b597b00316242484cd68ef018b7ef4ea88b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119138962"
---
# <a name="imsrdpcameraredirconfigcollectionbyindex-property"></a>IMsRdpCameraRedirConfigCollection :: ByIndex, propriété

Retourne un objet [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) par son index dans la collection.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe

```C++
HRESULT get_ByIndex(
    [in]            ULONG index,
    [out, retval]   IMsRdpCameraRedirConfig** ppConfig
);
```

## <a name="property-value"></a>Valeur de la propriété

Objet [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) qui correspond à l’index spécifié.

## <a name="requirements"></a>Configuration requise

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