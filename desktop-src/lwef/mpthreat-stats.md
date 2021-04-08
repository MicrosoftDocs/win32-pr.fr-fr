---
title: Structure MPTHREAT_STATS (MpClient. h)
description: Statistiques relatives aux menaces.
ms.assetid: 78B7E2A8-1BB4-4610-8E90-1F8ECBE740A8
keywords:
- Fonctionnalités d’environnement Windows héritées de la structure MPTHREAT_STATS
- PMPTHREAT_STATS des fonctionnalités d’environnement Windows héritées du pointeur de structure
topic_type:
- apiref
api_name:
- MPTHREAT_STATS
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21a2eef7acde5fbeac2cf9951dfad3e6923ccea2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843501"
---
# <a name="mpthreat_stats-structure"></a><span data-ttu-id="52c9f-105">MPTHREAT, \_ structure des statistiques</span><span class="sxs-lookup"><span data-stu-id="52c9f-105">MPTHREAT\_STATS structure</span></span>

<span data-ttu-id="52c9f-106">Statistiques relatives aux menaces.</span><span class="sxs-lookup"><span data-stu-id="52c9f-106">Threat-related statistics.</span></span>

## <a name="syntax"></a><span data-ttu-id="52c9f-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="52c9f-107">Syntax</span></span>


```C++
typedef struct tagMPTHREAT_STATS {
  UINT ThreatCount;
  UINT SuspiciousThreatCount;
  UINT Reserved[4];
} MPTHREAT_STATS, *PMPTHREAT_STATS;
```



## <a name="members"></a><span data-ttu-id="52c9f-108">Membres</span><span class="sxs-lookup"><span data-stu-id="52c9f-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="52c9f-109">**ThreatCount**</span><span class="sxs-lookup"><span data-stu-id="52c9f-109">**ThreatCount**</span></span>
</dt> <dd>

<span data-ttu-id="52c9f-110">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="52c9f-110">Type: **UINT**</span></span>

</dd> <dd>

<span data-ttu-id="52c9f-111">Nombre de menaces détectées.</span><span class="sxs-lookup"><span data-stu-id="52c9f-111">Number of threats detected.</span></span>

</dd> <dt>

<span data-ttu-id="52c9f-112">**SuspiciousThreatCount**</span><span class="sxs-lookup"><span data-stu-id="52c9f-112">**SuspiciousThreatCount**</span></span>
</dt> <dd>

<span data-ttu-id="52c9f-113">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="52c9f-113">Type: **UINT**</span></span>

</dd> <dd>

<span data-ttu-id="52c9f-114">Nombre de menaces détectées avec l’analyse du comportement.</span><span class="sxs-lookup"><span data-stu-id="52c9f-114">Number of threats detected with behavior monitoring.</span></span>

</dd> <dt>

<span data-ttu-id="52c9f-115">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="52c9f-115">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="52c9f-116">Type : **uint \[ 4 \]**</span><span class="sxs-lookup"><span data-stu-id="52c9f-116">Type: **UINT\[4\]**</span></span>

</dd> <dd>

<span data-ttu-id="52c9f-117">Champs réservés pour une utilisation ultérieure.</span><span class="sxs-lookup"><span data-stu-id="52c9f-117">Fields reserved for future use.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="52c9f-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="52c9f-118">Requirements</span></span>



| <span data-ttu-id="52c9f-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="52c9f-119">Requirement</span></span> | <span data-ttu-id="52c9f-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="52c9f-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="52c9f-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="52c9f-121">Minimum supported client</span></span><br/> | <span data-ttu-id="52c9f-122">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="52c9f-122">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="52c9f-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="52c9f-123">Minimum supported server</span></span><br/> | <span data-ttu-id="52c9f-124">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="52c9f-124">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="52c9f-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="52c9f-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="52c9f-126"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="52c9f-126"><dt>MpClient.h</dt></span></span> </dl> |



 

 





