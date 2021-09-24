---
title: 'IDODownloadStatusCallback :: OnStatusChange, méthode'
description: L’optimisation de la distribution appelle votre implémentation de cette méthode chaque fois qu’un état de téléchargement a changé.
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
ms.openlocfilehash: 6dcb30690736cb2bd2548fbd5f84cf580d317eff
ms.sourcegitcommit: 2c13d0f1620f7c089687ef1d97e8c1d22e5d537a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "128519913"
---
# <a name="idodownloadstatuscallbackonstatuschange-method"></a>IDODownloadStatusCallback :: OnStatusChange, méthode

L’optimisation de la distribution appelle votre implémentation de cette méthode chaque fois qu’un état de téléchargement a changé.

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
