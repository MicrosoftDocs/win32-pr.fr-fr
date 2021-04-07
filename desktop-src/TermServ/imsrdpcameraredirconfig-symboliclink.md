---
title: IMsRdpCameraRedirConfig SymbolicLink, propriété
description: Obtient le lien symbolique de l’interface **KSCATEGORY_VIDEO_CAMERA** pour l’appareil photo.
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété SymbolicLink
- Services Bureau à distance de la propriété SymbolicLink, interface IMsRdpCameraRedirConfig
- Services Bureau à distance de l’interface IMsRdpCameraRedirConfig, propriété SymbolicLink
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfig.SymbolicLink
- IMsRdpCameraRedirConfig.SymbolicLink
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 439ead6fa0868887cc5965205b22236abb5aada6
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/19/2020
ms.locfileid: "103845658"
---
# <a name="imsrdpcameraredirconfigsymboliclink-property"></a>IMsRdpCameraRedirConfig :: SymbolicLink, propriété

Obtient le lien symbolique de l’interface **KSCATEGORY_VIDEO_CAMERA** pour l’appareil photo.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe

```C++
HRESULT get_SymbolicLink(
    [out, retval] BSTR* pSymbolicLink
);
```

## <a name="property-value"></a>Valeur de la propriété

Lien symbolique de l’interface **KSCATEGORY_VIDEO_CAMERA** pour l’appareil photo.

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