---
title: 'IDODownload :: GetStatus, méthode'
description: Récupère un pointeur vers une structure **DO_DOWNLOAD_STATUS** qui reflète l’état actuel du téléchargement.
keywords:
- 'IDODownload :: GetStatus, méthode'
topic_type:
- apiref
api_name:
- IDODownload.GetStatus
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: e3a5aec5e35187a51865e074dae26ff012b75dfa3a41ffd13a8bed7371515fab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047107"
---
# <a name="idodownloadgetstatus-method"></a>IDODownload :: GetStatus, méthode

Récupère un pointeur vers une structure **DO_DOWNLOAD_STATUS** qui reflète l’état actuel du téléchargement.

## <a name="syntax"></a>Syntaxe

```cpp
HRESULT GetStatus(
  DO_DOWNLOAD_STATUS *status
);
```

## <a name="parameters"></a>Paramètres

`status`

Pointeur vers une structure **DO_DOWNLOAD_STATUS** .

## <a name="return-value"></a>Valeur renvoyée

Si la fonction est réussie, elle retourne **S_OK**. Sinon, elle retourne un [](/windows/desktop/com/structure-of-com-error-codes) [code d’erreur](/windows/desktop/com/com-error-codes-10)HRESULT.

## <a name="requirements"></a>Configuration requise

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Client minimal pris en charge** | Windows 10, version 1809 \[ Applications Win32 uniquement\] |
| **Serveur minimal pris en charge** | Windows Serveur, version 1809 \[ applications Win32 uniquement\] |
| **En-tête** | Do. h |
