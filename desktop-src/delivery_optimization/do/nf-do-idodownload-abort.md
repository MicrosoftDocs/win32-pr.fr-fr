---
title: 'IDODownload :: Abort, méthode'
description: Abandonne le téléchargement.
keywords:
- 'IDODownload :: Abort, méthode'
topic_type:
- apiref
api_name:
- IDODownload.Abort
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: 70ca7d25b702de8cd11214daf5d70491113d2f68959a9d48c5b4d0c97bc97dda
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118543976"
---
# <a name="idodownloadabort-method"></a>IDODownload :: Abort, méthode

Abandonne le téléchargement.

## <a name="syntax"></a>Syntaxe

```cpp
HRESULT Abort();
```

## <a name="return-value"></a>Valeur de retour

Si la fonction est réussie, elle retourne **S_OK**. Sinon, elle retourne un [](/windows/desktop/com/structure-of-com-error-codes) [code d’erreur](/windows/desktop/com/com-error-codes-10)HRESULT.

## <a name="requirements"></a>Configuration requise

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Client minimal pris en charge** | Windows 10, version 1809 \[ Applications Win32 uniquement\] |
| **Serveur minimal pris en charge** | Windows Serveur, version 1809 \[ applications Win32 uniquement\] |
| **En-tête** | Do. h |
