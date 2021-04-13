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
ms.openlocfilehash: 01628ea29895012f60552e696b7f68854f426f8d
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2019
ms.locfileid: "104381283"
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
| **Client minimal pris en charge** | Windows 10, version 1809 \[ applications Win32 uniquement\] |
| **Serveur minimal pris en charge** | Windows Server, version 1809 \[ applications Win32 uniquement\] |
| **En-tête** | Do. h |
