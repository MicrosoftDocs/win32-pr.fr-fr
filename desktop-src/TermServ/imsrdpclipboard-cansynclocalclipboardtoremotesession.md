---
title: IMsRdpClipboard CanSyncLocalClipboardToRemoteSession, méthode
description: Indique si le presse-papiers local peut être synchronisé avec la session à distance.
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode CanSyncLocalClipboardToRemoteSession
- Méthode CanSyncLocalClipboardToRemoteSession Services Bureau à distance, interface IMsRdpClipboard
- Services Bureau à distance de l’interface IMsRdpClipboard, méthode CanSyncLocalClipboardToRemoteSession
topic_type:
- apiref
api_name:
- IMsRdpClipboard.CanSyncLocalClipboardToRemoteSession
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: dabc12064ff43a2bb64a562d1aa3050681f46c31dd2698154beb1dafe3cfd85e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118606914"
---
# <a name="imsrdpclipboardcansynclocalclipboardtoremotesession-method"></a>IMsRdpClipboard :: CanSyncLocalClipboardToRemoteSession, méthode

Indique si le presse-papiers local peut être synchronisé avec la session à distance.

## <a name="syntax"></a>Syntaxe

```C++
HRESULT CanSyncLocalClipboardToRemoteSession(
  [out, retval] VARIANT_BOOL* pfSync
);
```

## <a name="parameters"></a>Paramètres

**True** si le presse-papiers local peut être synchronisé avec la session à distance ; Sinon, **false**.

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