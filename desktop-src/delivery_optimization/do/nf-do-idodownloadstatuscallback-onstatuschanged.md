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
ms.openlocfilehash: 9abf13969a6183f98102792b9bcf7a3329ca243d
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2019
ms.locfileid: "104030642"
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
| **Client minimal pris en charge** | Windows 10, version 1809 \[ applications Win32 uniquement\] |
| **Serveur minimal pris en charge** | Windows Server, version 1809 \[ applications Win32 uniquement\] |
| **En-tête** | Do. h |
