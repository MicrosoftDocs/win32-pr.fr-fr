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
# <a name="do_download_range_info-structure"></a><span data-ttu-id="25fff-104">Structure DO_DOWNLOAD_RANGE_INFO</span><span class="sxs-lookup"><span data-stu-id="25fff-104">DO_DOWNLOAD_RANGE_INFO structure</span></span>

<span data-ttu-id="25fff-105">La structure **DO_DOWNLOAD_RANGE_INFO** identifie un tableau de plages d’octets à télécharger à partir d’un fichier.</span><span class="sxs-lookup"><span data-stu-id="25fff-105">The **DO_DOWNLOAD_RANGE_INFO** structure identifies an array of ranges of bytes to download from a file.</span></span> <span data-ttu-id="25fff-106">Elle est généralement passée comme argument facultatif à la fonction **IDODownload :: Start** .</span><span class="sxs-lookup"><span data-stu-id="25fff-106">It is typically passed as an optional argument to the **IDODownload::Start** function.</span></span>

## <a name="syntax"></a><span data-ttu-id="25fff-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="25fff-107">Syntax</span></span>
```cpp
typedef struct _DO_DOWNLOAD_RANGES_INFO
{
  UINT RangeCount;
  [size_is(RangeCount)] DO_DOWNLOAD_RANGE Ranges[];
} DO_DOWNLOAD_RANGES_INFO;
```

## <a name="members"></a><span data-ttu-id="25fff-108">Membres</span><span class="sxs-lookup"><span data-stu-id="25fff-108">Members</span></span>

`RangeCount`

<span data-ttu-id="25fff-109">Nombre d’éléments dans les plages.</span><span class="sxs-lookup"><span data-stu-id="25fff-109">Number of elements in Ranges.</span></span>

`Ranges`

<span data-ttu-id="25fff-110">Tableau d’une ou de plusieurs structures de **DO_DOWNLOAD_RANGE** qui spécifient les plages à télécharger.</span><span class="sxs-lookup"><span data-stu-id="25fff-110">Array of one or more **DO_DOWNLOAD_RANGE** structures that specify the ranges to download.</span></span>

## <a name="requirements"></a><span data-ttu-id="25fff-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="25fff-111">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="25fff-112">**Client minimal pris en charge**</span><span class="sxs-lookup"><span data-stu-id="25fff-112">**Minimum supported client**</span></span> | <span data-ttu-id="25fff-113">Windows 10, version 1809 \[ applications Win32 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="25fff-113">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="25fff-114">**Serveur minimal pris en charge**</span><span class="sxs-lookup"><span data-stu-id="25fff-114">**Minimum supported server**</span></span> | <span data-ttu-id="25fff-115">Windows Server, version 1809 \[ applications Win32 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="25fff-115">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="25fff-116">**En-tête**</span><span class="sxs-lookup"><span data-stu-id="25fff-116">**Header**</span></span> | <span data-ttu-id="25fff-117">Do. h</span><span class="sxs-lookup"><span data-stu-id="25fff-117">Do.h</span></span> |
