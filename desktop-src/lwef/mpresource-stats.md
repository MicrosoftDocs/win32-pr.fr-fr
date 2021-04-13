---
title: Structure MPRESOURCE_STATS (MpClient. h)
description: Statistiques relatives aux ressources.
ms.assetid: D1DC4BC9-911D-448C-A421-11D2F51F0A61
keywords:
- Fonctionnalités d’environnement Windows héritées de la structure MPRESOURCE_STATS
- PMPRESOURCE_STATS des fonctionnalités d’environnement Windows héritées du pointeur de structure
topic_type:
- apiref
api_name:
- MPRESOURCE_STATS
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: afbe1ce6734aabd1093f7acd886af757c51ed83e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465935"
---
# <a name="mpresource_stats-structure"></a><span data-ttu-id="a3512-105">MPRESOURCE, \_ structure des statistiques</span><span class="sxs-lookup"><span data-stu-id="a3512-105">MPRESOURCE\_STATS structure</span></span>

<span data-ttu-id="a3512-106">Statistiques relatives aux ressources.</span><span class="sxs-lookup"><span data-stu-id="a3512-106">Resource-related statistics.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3512-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a3512-107">Syntax</span></span>


```C++
typedef struct tagMPRESOURCE_STATS {
  DWORD  PPMProgress;
  UINT64 ProcessCount;
  UINT64 FileCount;
  UINT64 FileBytesCount;
  UINT64 RegKeyCount;
  UINT64 Reserved[4];
} MPRESOURCE_STATS, *PMPRESOURCE_STATS;
```



## <a name="members"></a><span data-ttu-id="a3512-108">Membres</span><span class="sxs-lookup"><span data-stu-id="a3512-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="a3512-109">**PPMProgress**</span><span class="sxs-lookup"><span data-stu-id="a3512-109">**PPMProgress**</span></span>
</dt> <dd>

<span data-ttu-id="a3512-110">Type : **DWORD**</span><span class="sxs-lookup"><span data-stu-id="a3512-110">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="a3512-111">Progression approximative de l’analyse en ppm (parties par million).</span><span class="sxs-lookup"><span data-stu-id="a3512-111">Approximate progress for scan in ppm (parts per million).</span></span> <span data-ttu-id="a3512-112">Défini sur **MPPROGRESS \_ non valide** si les informations de progression ne sont pas disponibles.</span><span class="sxs-lookup"><span data-stu-id="a3512-112">Set to **MPPROGRESS\_INVALID** if progress information is not available.</span></span>

</dd> <dt>

<span data-ttu-id="a3512-113">**ProcessCount**</span><span class="sxs-lookup"><span data-stu-id="a3512-113">**ProcessCount**</span></span>
</dt> <dd>

<span data-ttu-id="a3512-114">Type : **UINT64**</span><span class="sxs-lookup"><span data-stu-id="a3512-114">Type: **UINT64**</span></span>

</dd> <dd>

<span data-ttu-id="a3512-115">Nombre de processus analysés.</span><span class="sxs-lookup"><span data-stu-id="a3512-115">Number of processes scanned.</span></span>

</dd> <dt>

<span data-ttu-id="a3512-116">**FileCount**</span><span class="sxs-lookup"><span data-stu-id="a3512-116">**FileCount**</span></span>
</dt> <dd>

<span data-ttu-id="a3512-117">Type : **UINT64**</span><span class="sxs-lookup"><span data-stu-id="a3512-117">Type: **UINT64**</span></span>

</dd> <dd>

<span data-ttu-id="a3512-118">Nombre de fichiers analysés.</span><span class="sxs-lookup"><span data-stu-id="a3512-118">Number of files scanned.</span></span>

</dd> <dt>

<span data-ttu-id="a3512-119">**FileBytesCount**</span><span class="sxs-lookup"><span data-stu-id="a3512-119">**FileBytesCount**</span></span>
</dt> <dd>

<span data-ttu-id="a3512-120">Type : **UINT64**</span><span class="sxs-lookup"><span data-stu-id="a3512-120">Type: **UINT64**</span></span>

</dd> <dd>

<span data-ttu-id="a3512-121">Nombre d’octets analysés pour les fichiers.</span><span class="sxs-lookup"><span data-stu-id="a3512-121">Number of bytes scanned for files.</span></span>

</dd> <dt>

<span data-ttu-id="a3512-122">**RegKeyCount**</span><span class="sxs-lookup"><span data-stu-id="a3512-122">**RegKeyCount**</span></span>
</dt> <dd>

<span data-ttu-id="a3512-123">Type : **UINT64**</span><span class="sxs-lookup"><span data-stu-id="a3512-123">Type: **UINT64**</span></span>

</dd> <dd>

<span data-ttu-id="a3512-124">Nombre de RegKeys analysés.</span><span class="sxs-lookup"><span data-stu-id="a3512-124">Number of RegKeys scanned.</span></span>

</dd> <dt>

<span data-ttu-id="a3512-125">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="a3512-125">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="a3512-126">Type : **UINT64 \[ 4 \]**</span><span class="sxs-lookup"><span data-stu-id="a3512-126">Type: **UINT64\[4\]**</span></span>

</dd> <dd>

<span data-ttu-id="a3512-127">Champs réservés pour une utilisation ultérieure.</span><span class="sxs-lookup"><span data-stu-id="a3512-127">Fields reserved for future use.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a3512-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a3512-128">Requirements</span></span>



| <span data-ttu-id="a3512-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a3512-129">Requirement</span></span> | <span data-ttu-id="a3512-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="a3512-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a3512-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a3512-131">Minimum supported client</span></span><br/> | <span data-ttu-id="a3512-132">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a3512-132">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="a3512-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a3512-133">Minimum supported server</span></span><br/> | <span data-ttu-id="a3512-134">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a3512-134">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a3512-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="a3512-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="a3512-136"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="a3512-136"><dt>MpClient.h</dt></span></span> </dl> |



 

 





