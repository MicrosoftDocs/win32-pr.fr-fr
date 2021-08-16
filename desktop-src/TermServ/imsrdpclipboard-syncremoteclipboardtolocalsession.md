---
title: IMsRdpClipboard SyncRemoteClipboardToLocalSession, méthode
description: Synchronise le presse-papiers distant avec la session locale.
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SyncRemoteClipboardToLocalSession
- Méthode SyncRemoteClipboardToLocalSession Services Bureau à distance, interface IMsRdpClipboard
- Services Bureau à distance de l’interface IMsRdpClipboard, méthode SyncRemoteClipboardToLocalSession
topic_type:
- apiref
api_name:
- IMsRdpClipboard.SyncRemoteClipboardToLocalSession
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: e1e56a67504ab3182ed6ccaba97591e8259d6e46b6ebdd3bdc06fbaf63c170f0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119000819"
---
# <a name="imsrdpclipboardsyncremoteclipboardtolocalsession-method"></a>IMsRdpClipboard :: SyncRemoteClipboardToLocalSession, méthode

Synchronise le presse-papiers distant avec la session locale.

## <a name="syntax"></a>Syntaxe

```C++
HRESULT SyncRemoteClipboardToLocalSession();
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