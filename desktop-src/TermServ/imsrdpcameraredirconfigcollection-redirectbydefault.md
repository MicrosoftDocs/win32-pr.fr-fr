---
title: IMsRdpCameraRedirConfigCollection EncodeVideo, propriété
description: Spécifie si une nouvelle caméra est redirigée par défaut.
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété RedirectByDefault
- Services Bureau à distance de la propriété RedirectByDefault, interface IMsRdpCameraRedirConfigCollection
- Services Bureau à distance de l’interface IMsRdpCameraRedirConfigCollection, propriété RedirectByDefault
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfigCollection.RedirectByDefault
- IMsRdpCameraRedirConfigCollection.put_RedirectByDefault
- IMsRdpCameraRedirConfigCollection.get_RedirectByDefault
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 810af200eefee0008aea21af684c02b6d31325eb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126916980"
---
# <a name="imsrdpcameraredirconfigcollectionredirectbydefault-property"></a>IMsRdpCameraRedirConfigCollection :: RedirectByDefault, propriété

Spécifie si une nouvelle caméra est redirigée par défaut.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe

```C++
HRESULT put_RedirectByDefault(
    [in] VARIANT_BOOL fRedirect
);

HRESULT get_RedirectByDefault(
    [out, retval] VARIANT_BOOL* pfRedirect
);
```

## <a name="property-value"></a>Valeur de la propriété

Valeur qui indique si une nouvelle caméra est redirigée par défaut.

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