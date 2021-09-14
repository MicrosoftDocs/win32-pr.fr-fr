---
title: IMsRdpCameraRedirConfigCollection Count, propriété
description: Retourne le nombre d’objets IMsRdpCameraRedirConfig dans la collection.
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété Count
- Services Bureau à distance de la propriété Count, interface IMsRdpCameraRedirConfigCollection
- Services Bureau à distance de l’interface IMsRdpCameraRedirConfigCollection, propriété Count
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfigCollection.Count
- IMsRdpCameraRedirConfigCollection.get_Count
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 31927428b709136de87f436ad92cc6a78fa9795a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126916999"
---
# <a name="imsrdpcameraredirconfigcollectioncount-property"></a>IMsRdpCameraRedirConfigCollection :: Count, propriété

Retourne le nombre d’objets [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) dans la collection.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe

```C++
HRESULT get_Count(
    [out, retval] ULONG *pCount
);
```

## <a name="property-value"></a>Valeur de la propriété

Nombre d’objets [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) dans la collection.

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