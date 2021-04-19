---
title: Structure DO_DOWNLOAD_STATUS
description: Permet d’obtenir l’état d’un téléchargement spécifique.
keywords:
- Structure DO_DOWNLOAD_STATUS
topic_type:
- apiref
api_name:
- DO_DOWNLOAD_STATUS
api_location:
- do.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: 5e113bb4866ef1033886dbb1579d21aa296d0e5e
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2019
ms.locfileid: "106510862"
---
# <a name="do_download_status-structure"></a>Structure DO_DOWNLOAD_STATUS

La structure **DO_DOWNLOAD_STATUS** permet d’obtenir l’état d’un téléchargement spécifique. Elle est obtenue en appelant la fonction **IDODownload :: GetStatus** .

## <a name="syntax"></a>Syntaxe
```cpp
typedef struct _DO_DOWNLOAD_STATUS
{
  UINT64 BytesTotal;
  UINT64 BytesTransferred;
  DODownloadState State;
  HRESULT Error;
  HRESULT ExtendedError;
} DO_DOWNLOAD_STATUS;
```

## <a name="members"></a>Membres

`BytesTotal`

Nombre total d’octets à télécharger.

`BytesTransferred`

Nombre d’octets qui ont déjà été téléchargés.

`State`

État de téléchargement actuel tel que défini par l’énumération **DODownloadState** .

`Error`

Informations d’erreur (le cas échéant) associées au téléchargement en cours.

`ExtendedError`

Informations d’erreur étendues (si elles existent) associées au téléchargement en cours.

## <a name="requirements"></a>Configuration requise

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Client minimal pris en charge** | Windows 10, version 1809 \[ applications Win32 uniquement\] |
| **Serveur minimal pris en charge** | Windows Server, version 1809 \[ applications Win32 uniquement\] |
| **En-tête** | Do. h |
