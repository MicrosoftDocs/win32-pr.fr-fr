---
title: IMsRdpClipboard CanSyncRemoteClipboardToLocalSession, méthode
description: Indique si le presse-papiers distant peut être synchronisé avec la session locale.
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode CanSyncRemoteClipboardToLocalSession
- Méthode CanSyncRemoteClipboardToLocalSession Services Bureau à distance, interface IMsRdpClipboard
- Services Bureau à distance de l’interface IMsRdpClipboard, méthode CanSyncRemoteClipboardToLocalSession
topic_type:
- apiref
api_name:
- IMsRdpClipboard.CanSyncRemoteClipboardToLocalSession
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: ebb20057e3a312dbe0b24856c47ad2a7ef1b7292
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/19/2020
ms.locfileid: "106514901"
---
# <a name="imsrdpclipboardcansyncremoteclipboardtolocalsession-method"></a>IMsRdpClipboard :: CanSyncRemoteClipboardToLocalSession, méthode

Indique si le presse-papiers distant peut être synchronisé avec la session locale.

## <a name="syntax"></a>Syntaxe

```C++
HRESULT CanSyncRemoteClipboardToLocalSession(
  [out, retval] VARIANT_BOOL* pfSync
);
```

## <a name="parameters"></a>Paramètres

**True** si le presse-papiers distant peut être synchronisé avec la session locale ; Sinon, **false**.

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