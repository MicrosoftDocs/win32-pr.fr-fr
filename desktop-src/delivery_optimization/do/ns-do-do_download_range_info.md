---
title: Structure DO_DOWNLOAD_RANGE_INFO
description: Identifie un tableau de plages d’octets à télécharger à partir d’un fichier.
keywords:
- Structure DO_DOWNLOAD_RANGE_INFO
topic_type:
- apiref
api_name:
- DO_DOWNLOAD_RANGE_INFO
api_location:
- do.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: 30df22c7232ad1d28315e8152396ddd92bdab9a7cbf67d748af134c0f0760c33
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118543743"
---
# <a name="do_download_range_info-structure"></a>Structure DO_DOWNLOAD_RANGE_INFO

La structure **DO_DOWNLOAD_RANGE_INFO** identifie un tableau de plages d’octets à télécharger à partir d’un fichier. Elle est généralement passée comme argument facultatif à la fonction **IDODownload :: Start** .

## <a name="syntax"></a>Syntaxe
```cpp
typedef struct _DO_DOWNLOAD_RANGES_INFO
{
  UINT RangeCount;
  [size_is(RangeCount)] DO_DOWNLOAD_RANGE Ranges[];
} DO_DOWNLOAD_RANGES_INFO;
```

## <a name="members"></a>Membres

`RangeCount`

Nombre d’éléments dans les plages.

`Ranges`

Tableau d’une ou de plusieurs structures de **DO_DOWNLOAD_RANGE** qui spécifient les plages à télécharger.

## <a name="requirements"></a>Configuration requise

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Client minimal pris en charge** | Windows 10, version 1809 \[ Applications Win32 uniquement\] |
| **Serveur minimal pris en charge** | Windows Serveur, version 1809 \[ applications Win32 uniquement\] |
| **En-tête** | Do. h |
