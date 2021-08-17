---
title: 'IDODownloadStatusCallback :: OnStatusChange, méthode'
description: Appelle votre implémentation de cette méthode chaque fois qu’un état de téléchargement a changé.
keywords:
- 'IDODownloadStatusCallback :: OnStatusChange, méthode'
topic_type:
- apiref
api_name:
- IDODownloadStatusCallback.OnStatusChange
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: 0395b6bc64ad3abe102a0a4f0dc7afd8e8d59f336949a3b97eaf683a4f4900cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117736216"
---
# <a name="idodownloadstatuscallbackonstatuschange-method"></a>IDODownloadStatusCallback :: OnStatusChange, méthode

Appelle votre implémentation de cette méthode chaque fois qu’un état de téléchargement a changé.

## <a name="syntax"></a>Syntaxe

```cpp
HRESULT OnStatusChange(
  IDODownload *download,
  DO_DOWNLOAD_STATUS *status
);
```

## <a name="parameters"></a>Paramètres

`download`

Pointeur vers l’interface **IDODownload** dont l’État a changé.

`status`

Pointeur vers une structure **DO_DOWNLOAD_STATUS** contenant l’état du téléchargement.

## <a name="return-value"></a>Valeur renvoyée

Si la fonction est réussie, elle retourne **S_OK**. Sinon, elle retourne un [](/windows/desktop/com/structure-of-com-error-codes) [code d’erreur](/windows/desktop/com/com-error-codes-10)HRESULT.

## <a name="requirements"></a>Configuration requise

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Client minimal pris en charge** | Windows 10, version 1809 \[ Applications Win32 uniquement\] |
| **Serveur minimal pris en charge** | Windows Serveur, version 1809 \[ applications Win32 uniquement\] |
| **En-tête** | Do. h |
