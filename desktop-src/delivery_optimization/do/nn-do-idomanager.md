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
ms.openlocfilehash: a8755615e4d2f0fd074117438f8f305dce0cb681
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106513546"
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
| **Client minimal pris en charge** | Windows 10, version 1809 \[ applications Win32 uniquement\] |
| **Serveur minimal pris en charge** | Windows Server, version 1809 \[ applications Win32 uniquement\] |
| **En-tête** | Do. h |