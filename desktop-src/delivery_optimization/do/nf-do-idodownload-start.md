---
title: 'IDODownload :: Start, méthode'
description: Démarre ou reprend un téléchargement.
keywords:
- 'IDODownload :: Start, méthode'
topic_type:
- apiref
api_name:
- IDODownload.Start
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: b2a06de8319ac07983fd13cb8523fa1dcf92365ca9275da80b699b290a4a6435
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117736256"
---
# <a name="idodownloadstart-method"></a>IDODownload :: Start, méthode

Démarre ou reprend un téléchargement, en passant des plages facultatives en tant que pointeur vers [**DO_DOWNLOAD_RANGES_INFO**](ns-do-do_download_range_info.md) structure.

## <a name="syntax"></a>Syntaxe

```cpp
HRESULT Start(
  DO_DOWNLOAD_RANGES_INFO *ranges
);
```

## <a name="parameters"></a>Paramètres

`ranges`

Facultatif. Pointeur vers une structure [**DO_DOWNLOAD_RANGES_INFO**](ns-do-do_download_range_info.md) (pour télécharger uniquement des plages spécifiques du fichier). Pass `nullptr` pour télécharger l’intégralité du fichier.

## <a name="return-value"></a>Valeur renvoyée

Si la fonction est réussie, elle retourne **S_OK**. Sinon, elle retourne un [](/windows/desktop/com/structure-of-com-error-codes) [code d’erreur](/windows/desktop/com/com-error-codes-10)HRESULT.

## <a name="requirements"></a>Configuration requise

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Client minimal pris en charge** | Windows 10, version 1809 \[ Applications Win32 uniquement\] |
| **Serveur minimal pris en charge** | Windows Serveur, version 1809 \[ applications Win32 uniquement\] |
| **En-tête** | Do. h |
