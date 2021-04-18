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
# <a name="do_download_range-structure"></a><span data-ttu-id="b49d5-104">Structure DO_DOWNLOAD_RANGE</span><span class="sxs-lookup"><span data-stu-id="b49d5-104">DO_DOWNLOAD_RANGE structure</span></span>

<span data-ttu-id="b49d5-105">La structure **DO_DOWNLOAD_RANGE** identifie une seule plage d’octets à télécharger à partir d’un fichier.</span><span class="sxs-lookup"><span data-stu-id="b49d5-105">The **DO_DOWNLOAD_RANGE** structure identifies a single range of bytes to download from a file.</span></span> <span data-ttu-id="b49d5-106">La structure **DO_DOWNLOAD_RANGE** est incluse dans **DO_DOWNLOAD_RANGES_INFO** structure pour fournir un tableau de plages à télécharger.</span><span class="sxs-lookup"><span data-stu-id="b49d5-106">The **DO_DOWNLOAD_RANGE** structure is included within **DO_DOWNLOAD_RANGES_INFO** structure to provide an array of ranges to download.</span></span>

## <a name="syntax"></a><span data-ttu-id="b49d5-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b49d5-107">Syntax</span></span>
```cpp
typedef struct _DO_DOWNLOAD_RANGE
{
  UINT64 Offset;
  UINT64 Length;
} DO_DOWNLOAD_RANGE;
```

## <a name="members"></a><span data-ttu-id="b49d5-108">Membres</span><span class="sxs-lookup"><span data-stu-id="b49d5-108">Members</span></span>

`Offset`

<span data-ttu-id="b49d5-109">Décalage de base zéro au début de la plage d’octets à télécharger à partir d’un fichier.</span><span class="sxs-lookup"><span data-stu-id="b49d5-109">Zero-based offset to the beginning of the range of bytes to download from a file.</span></span>

`Length`

<span data-ttu-id="b49d5-110">Longueur de la plage, en octets.</span><span class="sxs-lookup"><span data-stu-id="b49d5-110">The length of the range, in bytes.</span></span> <span data-ttu-id="b49d5-111">Ne spécifiez pas de longueur de zéro octet.</span><span class="sxs-lookup"><span data-stu-id="b49d5-111">Do not specify a zero-byte length.</span></span> <span data-ttu-id="b49d5-112">Pour indiquer que la plage s’étend jusqu’à la fin du fichier, spécifiez **DO_LENGTH_TO_EOF**.</span><span class="sxs-lookup"><span data-stu-id="b49d5-112">To indicate that the range extends to the end of the file, specify **DO_LENGTH_TO_EOF**.</span></span>

## <a name="requirements"></a><span data-ttu-id="b49d5-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b49d5-113">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="b49d5-114">**Client minimal pris en charge**</span><span class="sxs-lookup"><span data-stu-id="b49d5-114">**Minimum supported client**</span></span> | <span data-ttu-id="b49d5-115">Windows 10, version 1809 \[ applications Win32 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b49d5-115">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="b49d5-116">**Serveur minimal pris en charge**</span><span class="sxs-lookup"><span data-stu-id="b49d5-116">**Minimum supported server**</span></span> | <span data-ttu-id="b49d5-117">Windows Server, version 1809 \[ applications Win32 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b49d5-117">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="b49d5-118">**En-tête**</span><span class="sxs-lookup"><span data-stu-id="b49d5-118">**Header**</span></span> | <span data-ttu-id="b49d5-119">DeliveryOptimizationDownloadTypes. h</span><span class="sxs-lookup"><span data-stu-id="b49d5-119">DeliveryOptimizationDownloadTypes.h</span></span> |
