---
title: Interface IDOManager
description: Utilisé pour créer un nouveau téléchargement et énumérer les téléchargements existants.
keywords:
- Interface IDOManager
topic_type:
- apiref
api_name:
- IDOManager
api_location:
- do.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: 5fff72067c69345a9852718c377b179d16f398c0eb3b84c73ca82c3af1b08a71
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047087"
---
# <a name="idomanager-interface"></a>Interface IDOManager

L’interface **IDOManager** est utilisée pour créer un nouveau téléchargement et énumérer les téléchargements existants.

## <a name="methods"></a>Méthodes

L’interface **IDOManager** possède ces méthodes.

| Méthode | Description |
| ---- |:---- |
| [IDOManager::CreateDownload](./nf-do-idomanager-createdownload.md) | Crée un nouveau téléchargement. |
| [IDOManager::EnumDownloads](./nf-do-idomanager-enumdownloads.md) | Récupère un pointeur d’interface vers un objet énumérateur utilisé pour énumérer les téléchargements existants. |

## <a name="requirements"></a>Configuration requise

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Client minimal pris en charge** | Windows 10, version 1809 \[ Applications Win32 uniquement\] |
| **Serveur minimal pris en charge** | Windows Serveur, version 1809 \[ applications Win32 uniquement\] |
| **En-tête** | Do. h |