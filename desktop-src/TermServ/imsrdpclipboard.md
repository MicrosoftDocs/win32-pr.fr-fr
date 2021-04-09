---
title: IMsRdpClipboard, interface
description: Représente le contrôleur du presse-papiers utilisé pour synchroniser les presse-papiers locaux et distants si la synchronisation manuelle du presse-papiers est activée.
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de l’interface IMsRdpClipboard
- Services Bureau à distance de l’interface IMsRdpClipboard, Description
topic_type:
- apiref
api_name:
- IMsRdpClipboard
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 1baa65264226d5c4bd1e32acbe0666545e79b7a0
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/19/2020
ms.locfileid: "104108367"
---
# <a name="imsrdpclipboard-interface"></a>IMsRdpClipboard, interface

Représente le contrôleur du presse-papiers utilisé pour synchroniser les presse-papiers locaux et distants si la synchronisation manuelle du presse-papiers est activée (autrement dit, la valeur de la propriété [ManualClipboardSyncEnabled](imsrdpextendedsettings-property.md) est définie sur **true**).

## <a name="members"></a>Membres

L’interface **IMsRdpClipboard** hérite de **IUnknown**. **IMsRdpClipboard** a également les types de membres suivants :

- [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IMsRdpClipboard** possède ces méthodes.


| Méthode        | Description      |
|:---------------|:----------------|
| [**CanSyncLocalClipboardToRemoteSession**](imsrdpclipboard-cansynclocalclipboardtoremotesession.md)       |  Indique si le presse-papiers local peut être synchronisé avec la session à distance.                   |
| [**CanSyncRemoteClipboardToLocalSession**](imsrdpclipboard-cansyncremoteclipboardtolocalsession.md)       |  Indique si le presse-papiers distant peut être synchronisé avec la session locale.                   |
| [**SyncLocalClipboardToRemoteSession**](imsrdpclipboard-synclocalclipboardtoremotesession.md)       |  Synchronise le presse-papiers local avec la session à distance.                   |
| [**SyncRemoteClipboardToLocalSession**](imsrdpclipboard-syncremoteclipboardtolocalsession.md)       |   Synchronise le presse-papiers distant avec la session locale.                      |

## <a name="requirements"></a>Configuration requise

| Condition requise | Valeur |
|-------------------------------------|---------------------------------------|
| Client minimal pris en charge| Windows 10, version 1803 (build 17134)      |
| Bibliothèque de types            | MsTscAx.dll                        |
| DLL                  | MsTscAx.dll     |
| IID                      | IID \_ IMsRdpClipboard est défini en tant que 2E769EE8-00C7-43DC-AFD9-235D75B72A40            |

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMsRdpClientNonScriptable7 :: Clipboard**](imsrdpclientnonscriptable7-clipboard.md)
</dt> </dl>
