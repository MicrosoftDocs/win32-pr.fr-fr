---
title: 'IDODownload :: Finalize, méthode'
description: Finalise le téléchargement.
keywords:
- 'IDODownload :: Finalize, méthode'
topic_type:
- apiref
api_name:
- IDODownload.Finalize
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: 620b8cf1671c18f2e4a79a798fac366d61c9e09f5a83ecda2c1ade531c6a558a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119636031"
---
# <a name="idodownloadfinalize-method"></a>IDODownload :: Finalize, méthode

Finalise le téléchargement. Une fois finalisé, un téléchargement ne peut pas être repris en appelant **Start**.

## <a name="syntax"></a>Syntaxe

```cpp
HRESULT Finalize();
```

## <a name="return-value"></a>Valeur de retour

Si la fonction est réussie, elle retourne **S_OK**. Sinon, elle retourne un [](/windows/desktop/com/structure-of-com-error-codes) [code d’erreur](/windows/desktop/com/com-error-codes-10)HRESULT.

## <a name="requirements"></a>Configuration requise

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Client minimal pris en charge** | Windows 10, version 1809 \[ Applications Win32 uniquement\] |
| **Serveur minimal pris en charge** | Windows Serveur, version 1809 \[ applications Win32 uniquement\] |
| **En-tête** | Do. h |
