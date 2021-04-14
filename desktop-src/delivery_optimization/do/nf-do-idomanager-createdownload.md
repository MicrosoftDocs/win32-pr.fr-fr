---
title: 'IDOManager :: CreateDownload, méthode'
description: Crée un nouveau téléchargement.
keywords:
- 'IDOManager :: CreateDownload, méthode'
topic_type:
- apiref
api_name:
- IDOManager.CreateDownload
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: b79bf0a1c5602fafea113585dfe6e8ca5b01057c
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2019
ms.locfileid: "104381285"
---
# <a name="idomanagercreatedownload-method"></a>IDOManager :: CreateDownload, méthode

Crée un nouveau téléchargement.

## <a name="syntax"></a>Syntaxe

```cpp
HRESULT CreateDownload(
  IDODownload **download
);
```

## <a name="parameters"></a>Paramètres

`download`

Adresse d’un pointeur d’interface **IDODownload** .

## <a name="return-value"></a>Valeur renvoyée

Si la fonction est réussie, elle retourne **S_OK**. Sinon, elle retourne un [](/windows/desktop/com/structure-of-com-error-codes) [code d’erreur](/windows/desktop/com/com-error-codes-10)HRESULT.

## <a name="requirements"></a>Configuration requise

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Client minimal pris en charge** | Windows 10, version 1809 \[ applications Win32 uniquement\] |
| **Serveur minimal pris en charge** | Windows Server, version 1809 \[ applications Win32 uniquement\] |
| **En-tête** | Do. h |
