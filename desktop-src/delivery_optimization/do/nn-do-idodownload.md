---
title: Interface IDODownload
description: Utilisé pour démarrer et gérer un téléchargement.
keywords:
- Interface IDODownload
topic_type:
- apiref
api_name:
- IDODownload
api_location:
- do.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: 356d6ae2e01f91eae94d9d2ff01a39dd49708eb73a7287d8c176b4231654a74a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118543816"
---
# <a name="idodownload-interface"></a>Interface IDODownload

L’interface **IDODownload** est utilisée pour démarrer et gérer un téléchargement.

## <a name="methods"></a>Méthodes

L’interface **IDODownload** possède ces méthodes.

| Méthode | Description |
| ---- |:---- |
| [IDODownload :: Abort](./nf-do-idomanager-createdownload.md) | Abandonne le téléchargement. |
| [IDODownload :: Finalize](./nf-do-idodownload-finalize.md) | Finalise le téléchargement. |
| [IDODownload :: GetProperty](./nf-do-idodownload-getproperty.md) | Récupère un pointeur vers un **Variant** qui contient une propriété de téléchargement spécifique. |
| [IDODownload :: GetStatus](./nf-do-idodownload-getstatus.md) | Récupère un pointeur vers une structure **DO_DOWNLOAD_STATUS** qui reflète l’état actuel du téléchargement. |
| [IDODownload ::P ause](./nf-do-idodownload-pause.md) | Interrompt le téléchargement. |
| [IDODownload :: SetProperty](./nf-do-idodownload-setproperty.md) | Définit une propriété de téléchargement. |
| [IDODownload :: Start](./nf-do-idodownload-start.md) | Démarre ou reprend un téléchargement. |

## <a name="requirements"></a>Configuration requise

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Client minimal pris en charge** | Windows 10, version 1809 \[ Applications Win32 uniquement\] |
| **Serveur minimal pris en charge** | Windows Serveur, version 1809 \[ applications Win32 uniquement\] |
| **En-tête** | Do. h |