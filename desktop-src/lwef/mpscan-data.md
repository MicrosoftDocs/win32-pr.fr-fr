---
title: Structure MPSCAN_DATA (MpClient. h)
description: Analyser les données passées au rappel.
ms.assetid: 6C9AAF1E-7566-43EE-A100-5112E9B8878C
keywords:
- Fonctionnalités d’environnement Windows héritées de la structure MPSCAN_DATA
- PMPSCAN_DATA des fonctionnalités d’environnement Windows héritées du pointeur de structure
topic_type:
- apiref
api_name:
- MPSCAN_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e78508313f102e2baad19cf359a5c3a7c172db0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466942"
---
# <a name="mpscan_data-structure"></a><span data-ttu-id="1e093-105">\_Structure de données MPSCAN</span><span class="sxs-lookup"><span data-stu-id="1e093-105">MPSCAN\_DATA structure</span></span>

<span data-ttu-id="1e093-106">Analyser les données passées au rappel.</span><span class="sxs-lookup"><span data-stu-id="1e093-106">Scan data passed to the callback.</span></span>

<span data-ttu-id="1e093-107">Cette structure contient des statistiques cumulatives sur les menaces et les ressources.</span><span class="sxs-lookup"><span data-stu-id="1e093-107">This structure contains cumulative threat and resource statistics.</span></span> <span data-ttu-id="1e093-108">Ces champs stat sont toujours valides.</span><span class="sxs-lookup"><span data-stu-id="1e093-108">These stat fields are always valid.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e093-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1e093-109">Syntax</span></span>


```C++
typedef struct tagMPSCAN_DATA {
  MPSCAN_TYPE      ScanType;
  PMPRESOURCE_INFO ResourceInfo;
  MPRESOURCE_STATS ResourceStats;
  MPTHREAT_STATS   ThreatStats;
} MPSCAN_DATA, *PMPSCAN_DATA;
```



## <a name="members"></a><span data-ttu-id="1e093-110">Membres</span><span class="sxs-lookup"><span data-stu-id="1e093-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="1e093-111">**ScanType**</span><span class="sxs-lookup"><span data-stu-id="1e093-111">**ScanType**</span></span>
</dt> <dd>

<span data-ttu-id="1e093-112">Type : **[ **MPSCAN \_**](mpscan-type.md)**</span><span class="sxs-lookup"><span data-stu-id="1e093-112">Type: **[**MPSCAN\_TYPE**](mpscan-type.md)**</span></span>

</dd> <dd>

<span data-ttu-id="1e093-113">Type d’analyse.</span><span class="sxs-lookup"><span data-stu-id="1e093-113">Scan type.</span></span>

</dd> <dt>

<span data-ttu-id="1e093-114">**ResourceInfo**</span><span class="sxs-lookup"><span data-stu-id="1e093-114">**ResourceInfo**</span></span>
</dt> <dd>

<span data-ttu-id="1e093-115">Type : **PMPRESOURCE \_ info**</span><span class="sxs-lookup"><span data-stu-id="1e093-115">Type: **PMPRESOURCE\_INFO**</span></span>

</dd> <dd>

<span data-ttu-id="1e093-116">Informations sur la ressource.</span><span class="sxs-lookup"><span data-stu-id="1e093-116">Resource information.</span></span> <span data-ttu-id="1e093-117">Consultez [**MPRESOURCE \_ info**](mpresource-info.md).</span><span class="sxs-lookup"><span data-stu-id="1e093-117">See [**MPRESOURCE\_INFO**](mpresource-info.md).</span></span>

</dd> <dt>

<span data-ttu-id="1e093-118">**ResourceStats**</span><span class="sxs-lookup"><span data-stu-id="1e093-118">**ResourceStats**</span></span>
</dt> <dd>

<span data-ttu-id="1e093-119">Type : **[ **\_ statistiques MPRESOURCE**](mpresource-stats.md)**</span><span class="sxs-lookup"><span data-stu-id="1e093-119">Type: **[**MPRESOURCE\_STATS**](mpresource-stats.md)**</span></span>

</dd> <dd>

<span data-ttu-id="1e093-120">Statistiques cumulatives relatives aux ressources.</span><span class="sxs-lookup"><span data-stu-id="1e093-120">Resource-related cumulative statistics.</span></span>

</dd> <dt>

<span data-ttu-id="1e093-121">**ThreatStats**</span><span class="sxs-lookup"><span data-stu-id="1e093-121">**ThreatStats**</span></span>
</dt> <dd>

<span data-ttu-id="1e093-122">Type : **[ **\_ statistiques MPTHREAT**](mpthreat-stats.md)**</span><span class="sxs-lookup"><span data-stu-id="1e093-122">Type: **[**MPTHREAT\_STATS**](mpthreat-stats.md)**</span></span>

</dd> <dd>

<span data-ttu-id="1e093-123">Statistiques des menaces avec la réussite de l’analyse.</span><span class="sxs-lookup"><span data-stu-id="1e093-123">Threat statistics with successful scan completions.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1e093-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1e093-124">Requirements</span></span>



| <span data-ttu-id="1e093-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1e093-125">Requirement</span></span> | <span data-ttu-id="1e093-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="1e093-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1e093-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1e093-127">Minimum supported client</span></span><br/> | <span data-ttu-id="1e093-128">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1e093-128">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="1e093-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1e093-129">Minimum supported server</span></span><br/> | <span data-ttu-id="1e093-130">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1e093-130">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1e093-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="1e093-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="1e093-132"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="1e093-132"><dt>MpClient.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e093-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1e093-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e093-134">**\_informations MPRESOURCE**</span><span class="sxs-lookup"><span data-stu-id="1e093-134">**MPRESOURCE\_INFO**</span></span>](mpresource-info.md)
</dt> <dt>

[<span data-ttu-id="1e093-135">**statistiques de MPRESOURCE \_**</span><span class="sxs-lookup"><span data-stu-id="1e093-135">**MPRESOURCE\_STATS**</span></span>](mpresource-stats.md)
</dt> <dt>

[<span data-ttu-id="1e093-136">**\_type MPSCAN**</span><span class="sxs-lookup"><span data-stu-id="1e093-136">**MPSCAN\_TYPE**</span></span>](mpscan-type.md)
</dt> <dt>

[<span data-ttu-id="1e093-137">**statistiques de MPTHREAT \_**</span><span class="sxs-lookup"><span data-stu-id="1e093-137">**MPTHREAT\_STATS**</span></span>](mpthreat-stats.md)
</dt> </dl>

 

 





