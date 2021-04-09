---
title: Interface IDODownloadInternal
description: Utilisé pour récupérer ou définir les propriétés de téléchargement étendues.
keywords:
- Interface IDODownloadInternal
topic_type:
- apiref
api_name:
- IDODownloadInternal
api_location:
- do.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/29/2019
ms.openlocfilehash: 89dcf0e397e9761c1b156a4ad4b245209cf50020
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102016"
---
# <a name="idodownloadinternal-interface"></a>Interface IDODownloadInternal

> [!IMPORTANT]
> L’interface **IDODownloadInternal** est déconseillée. Utilisez plutôt l’interface [IDODownload](../do/nn-do-idodownload.md) .

L’interface **IDODownloadInternal** est utilisée pour récupérer ou définir des propriétés de téléchargement étendues.

## <a name="methods"></a>Méthodes

L’interface **IDODownloadInternal** possède ces méthodes.

| Méthode | Description |
| ---- |:---- |
| [IDODownloadInternal::GetPropertyEx](./nf-dodownloadinternal-idodownloadinternal-getpropertyex.md) | Récupère un pointeur vers un **Variant** qui contient une valeur de propriété de téléchargement étendue spécifique. |
| [IDODownloadInternal::SetPropertyEx](./nf-dodownloadinternal-idodownloadinternal-setpropertyex.md) | Définit une propriété de téléchargement étendue. La méthode accepte un pointeur vers un **Variant** qui contient une valeur de propriété spécifique à appliquer au téléchargement. |

## <a name="requirements"></a>Configuration requise

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Client minimal pris en charge** | Windows 10, version 1809 \[ applications Win32 uniquement\] |
| **Serveur minimal pris en charge** | Windows Server, version 1809 \[ applications Win32 uniquement\] |
| **En-tête** | DODownloadInternal. h |