---
title: Structure DO_DOWNLOAD_RANGE
description: Identifie une seule plage d’octets à télécharger à partir d’un fichier.
keywords:
- Structure DO_DOWNLOAD_RANGE
topic_type:
- apiref
api_name:
- DO_DOWNLOAD_RANGE
api_location:
- deliveryoptimizationdownloadtypes.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: 0f328565c80350a05cbfb23f178ea3580586f326
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2019
ms.locfileid: "106512292"
---
# <a name="do_download_range-structure"></a>Structure DO_DOWNLOAD_RANGE

La structure **DO_DOWNLOAD_RANGE** identifie une seule plage d’octets à télécharger à partir d’un fichier. La structure **DO_DOWNLOAD_RANGE** est incluse dans **DO_DOWNLOAD_RANGES_INFO** structure pour fournir un tableau de plages à télécharger.

## <a name="syntax"></a>Syntaxe
```cpp
typedef struct _DO_DOWNLOAD_RANGE
{
  UINT64 Offset;
  UINT64 Length;
} DO_DOWNLOAD_RANGE;
```

## <a name="members"></a>Membres

`Offset`

Décalage de base zéro au début de la plage d’octets à télécharger à partir d’un fichier.

`Length`

Longueur de la plage, en octets. Ne spécifiez pas de longueur de zéro octet. Pour indiquer que la plage s’étend jusqu’à la fin du fichier, spécifiez **DO_LENGTH_TO_EOF**.

## <a name="requirements"></a>Configuration requise

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Client minimal pris en charge** | Windows 10, version 1809 \[ applications Win32 uniquement\] |
| **Serveur minimal pris en charge** | Windows Server, version 1809 \[ applications Win32 uniquement\] |
| **En-tête** | DeliveryOptimizationDownloadTypes. h |
