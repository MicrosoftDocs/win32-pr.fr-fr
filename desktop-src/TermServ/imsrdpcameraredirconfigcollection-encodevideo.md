---
title: IMsRdpCameraRedirConfigCollection EncodeVideo, propriété
description: Spécifie si le flux vidéo est au format H. 264 encodé.
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété EncodeVideo
- Services Bureau à distance de la propriété EncodeVideo, interface IMsRdpCameraRedirConfigCollection
- Services Bureau à distance de l’interface IMsRdpCameraRedirConfigCollection, propriété EncodeVideo
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfigCollection.EncodeVideo
- IMsRdpCameraRedirConfigCollection.put_EncodeVideo
- IMsRdpCameraRedirConfigCollection.get_EncodeVideo
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 6b2994f4db3de04f339bb242120b6c63cd2e0c7b
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/19/2020
ms.locfileid: "104108359"
---
# <a name="imsrdpcameraredirconfigcollectionencodevideo-property"></a>IMsRdpCameraRedirConfigCollection :: EncodeVideo, propriété

Spécifie si le flux vidéo est au format H. 264 encodé.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe

```C++
HRESULT put_EncodeVideo(
    [in] VARIANT_BOOL fEncode
);

HRESULT get_EncodeVideo(
    [out, retval] VARIANT_BOOL* pfEncode
);
```

## <a name="property-value"></a>Valeur de la propriété

Valeur qui indique si le flux vidéo est ou non encodé en H. 264.

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