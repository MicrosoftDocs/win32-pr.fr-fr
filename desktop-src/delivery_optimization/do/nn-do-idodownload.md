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
ms.openlocfilehash: ec2f74ce7daae6f612297d21e15e6993fcd78382
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315263"
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
| **Client minimal pris en charge** | Windows 10, version 1809 \[ applications Win32 uniquement\] |
| **Serveur minimal pris en charge** | Windows Server, version 1809 \[ applications Win32 uniquement\] |
| **En-tête** | Do. h |