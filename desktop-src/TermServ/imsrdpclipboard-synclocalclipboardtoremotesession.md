---
title: IMsRdpClipboard SyncLocalClipboardToRemoteSession, méthode
description: Synchronise le presse-papiers local avec la session à distance.
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SyncLocalClipboardToRemoteSession
- Méthode SyncLocalClipboardToRemoteSession Services Bureau à distance, interface IMsRdpClipboard
- Services Bureau à distance de l’interface IMsRdpClipboard, méthode SyncLocalClipboardToRemoteSession
topic_type:
- apiref
api_name:
- IMsRdpClipboard.SyncLocalClipboardToRemoteSession
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 516782dcb86dd02b0d3fd31fee5cc463a64b0e86726c826a855e245f37ba5908
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118606904"
---
# <a name="imsrdpclipboardsynclocalclipboardtoremotesession-method"></a>IMsRdpClipboard :: SyncLocalClipboardToRemoteSession, méthode

Synchronise le presse-papiers local avec la session à distance.

## <a name="syntax"></a>Syntaxe

```C++
HRESULT SyncLocalClipboardToRemoteSession();
```

## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne **S \_ OK** en cas de réussite.

## <a name="requirements"></a>Configuration requise

| Condition requise | Valeur |
|-------------------------------------|---------------------------------------|
| Client minimal pris en charge| Windows 10, version 1803 (build 17134)      |
| Bibliothèque de types            | MsTscAx.dll                        |
| DLL                  | MsTscAx.dll     |
| IID                      | IID \_ IMsRdpClipboard est défini en tant que 2E769EE8-00C7-43DC-AFD9-235D75B72A40          |

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMsRdpClipboard**](imsrdpclipboard.md)
</dt> </dl>
