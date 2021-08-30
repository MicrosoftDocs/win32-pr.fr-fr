---
title: IDODownload ::P méthode ause
description: Interrompt le téléchargement.
keywords:
- IDODownload ::P méthode ause
topic_type:
- apiref
api_name:
- IDODownload.Pause
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: fd9598cb18790c78b32cddc04afb20e4a1a44efb111f2d562df2c6e1fe3f34fb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119953629"
---
# <a name="idodownloadpause-method"></a>IDODownload ::P méthode ause

Interrompt le téléchargement.

## <a name="syntax"></a>Syntaxe

```cpp
HRESULT Pause();
```

## <a name="return-value"></a>Valeur de retour

Si la fonction est réussie, elle retourne **S_OK**. Sinon, elle retourne un [](/windows/desktop/com/structure-of-com-error-codes) [code d’erreur](/windows/desktop/com/com-error-codes-10)HRESULT.

## <a name="requirements"></a>Configuration requise

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Client minimal pris en charge** | Windows 10, version 1809 \[ Applications Win32 uniquement\] |
| **Serveur minimal pris en charge** | Windows Serveur, version 1809 \[ applications Win32 uniquement\] |
| **En-tête** | Do. h |
