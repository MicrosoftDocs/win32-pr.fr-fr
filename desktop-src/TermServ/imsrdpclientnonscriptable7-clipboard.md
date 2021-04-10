---
title: IMsRdpClientNonScriptable7 Clipboard, propriété
description: Obtient le contrôleur du presse-papiers utilisé pour synchroniser les presse-papiers locaux et distants si la synchronisation manuelle du presse-papiers est activée.
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de propriétés du presse-papiers
- Propriété Clipboard Services Bureau à distance, interface IMsRdpClientNonScriptable7
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable7, propriété Clipboard
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable7.Clipboard
- IMsRdpClientNonScriptable7.get_Clipboard
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 770930eb780b3ce8684608ffcdc0c13c1630cab0
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/19/2020
ms.locfileid: "103949937"
---
# <a name="imsrdpclientnonscriptable7clipboard-property"></a>IMsRdpClientNonScriptable7 :: Clipboard, propriété

Obtient le contrôleur du presse-papiers utilisé pour synchroniser les presse-papiers locaux et distants si la synchronisation manuelle du presse-papiers est activée.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe

```C++
HRESULT get_Clipboard(
  [out, retval] IMsRdpClipboard** ppClipboard
);
```

## <a name="property-value"></a>Valeur de la propriété

[IMsRdpClipboard](imsrdpclipboard.md) qui représente le contrôleur du presse-papiers utilisé pour synchroniser les presse-papiers locaux et distants si la synchronisation manuelle du presse-papiers est activée (autrement dit, la valeur de la propriété [ManualClipboardSyncEnabled](imsrdpextendedsettings-property.md) est définie sur **true**).

## <a name="requirements"></a>Configuration requise

| Condition requise | Valeur |
|-------------------------------------|---------------------------------------|
| Client minimal pris en charge| Windows 10, version 1803 (build 17134)      |
| Bibliothèque de types            | MsTscAx.dll                        |
| DLL                  | MsTscAx.dll     |
| IID                      | IID \_ IMsRdpClientNonScriptable7 est défini en tant que 71B4A60A-fe21-46D8-A39B-8E32BA0C5ECC          |

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMsRdpClientNonScriptable7**](imsrdpclientnonscriptable7.md)
</dt> </dl>