---
title: Structure MPSCAN_RESULT (MpClient. h)
description: Résultats d’une analyse.
ms.assetid: 9031A371-092A-4175-BE1D-90442A5BED2D
keywords:
- Fonctionnalités d’environnement Windows héritées de la structure MPSCAN_RESULT
- PMPSCAN_RESULT des fonctionnalités d’environnement Windows héritées du pointeur de structure
topic_type:
- apiref
api_name:
- MPSCAN_RESULT
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7be60df7993732bafcd7c44ac2fb581c111aed6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104200584"
---
# <a name="mpscan_result-structure"></a><span data-ttu-id="41c35-105">\_Structure de résultat MPSCAN</span><span class="sxs-lookup"><span data-stu-id="41c35-105">MPSCAN\_RESULT structure</span></span>

<span data-ttu-id="41c35-106">Résultats d’une analyse.</span><span class="sxs-lookup"><span data-stu-id="41c35-106">The results of a scan.</span></span>

## <a name="syntax"></a><span data-ttu-id="41c35-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="41c35-107">Syntax</span></span>


```C++
typedef struct tagMPSCAN_RESULT {
  MPSCAN_TYPE      ScanType;
  MPSOURCE         Source;
  GUID             ScanGuid;
  ULARGE_INTEGER   StartTime;
  ULARGE_INTEGER   EndTime;
  MPTHREAT_STATS   ThreatStats;
  MPRESOURCE_STATS ResourceStats;
  ULONGLONG        SignatureVersion;
} MPSCAN_RESULT, *PMPSCAN_RESULT;
```



## <a name="members"></a><span data-ttu-id="41c35-108">Membres</span><span class="sxs-lookup"><span data-stu-id="41c35-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="41c35-109">**ScanType**</span><span class="sxs-lookup"><span data-stu-id="41c35-109">**ScanType**</span></span>
</dt> <dd>

<span data-ttu-id="41c35-110">Type : **[ **MPSCAN \_**](mpscan-type.md)**</span><span class="sxs-lookup"><span data-stu-id="41c35-110">Type: **[**MPSCAN\_TYPE**](mpscan-type.md)**</span></span>

</dd> <dd>

<span data-ttu-id="41c35-111">Type d’analyse.</span><span class="sxs-lookup"><span data-stu-id="41c35-111">Scan type.</span></span> <span data-ttu-id="41c35-112">Consultez [**\_ type MPSCAN**](mpscan-type.md).</span><span class="sxs-lookup"><span data-stu-id="41c35-112">See [**MPSCAN\_TYPE**](mpscan-type.md).</span></span>

</dd> <dt>

<span data-ttu-id="41c35-113">**Source**</span><span class="sxs-lookup"><span data-stu-id="41c35-113">**Source**</span></span>
</dt> <dd>

<span data-ttu-id="41c35-114">Type : **[ **MPSOURCE**](mpsource.md)**</span><span class="sxs-lookup"><span data-stu-id="41c35-114">Type: **[**MPSOURCE**](mpsource.md)**</span></span>

</dd> <dd>

<span data-ttu-id="41c35-115">Source d’analyse, telle que l’utilisateur ou le système initié.</span><span class="sxs-lookup"><span data-stu-id="41c35-115">Scan source, such as user or system initiated.</span></span> <span data-ttu-id="41c35-116">Consultez [**MPSOURCE**](mpsource.md).</span><span class="sxs-lookup"><span data-stu-id="41c35-116">See [**MPSOURCE**](mpsource.md).</span></span>

</dd> <dt>

<span data-ttu-id="41c35-117">**ScanGuid**</span><span class="sxs-lookup"><span data-stu-id="41c35-117">**ScanGuid**</span></span>
</dt> <dd>

<span data-ttu-id="41c35-118">Type : **GUID**</span><span class="sxs-lookup"><span data-stu-id="41c35-118">Type: **GUID**</span></span>

</dd> <dd>

<span data-ttu-id="41c35-119">Identificateur d’analyse.</span><span class="sxs-lookup"><span data-stu-id="41c35-119">Scan identifier.</span></span>

</dd> <dt>

<span data-ttu-id="41c35-120">**StartTime**</span><span class="sxs-lookup"><span data-stu-id="41c35-120">**StartTime**</span></span>
</dt> <dd>

<span data-ttu-id="41c35-121">Type : **\_ entier ULARGE**</span><span class="sxs-lookup"><span data-stu-id="41c35-121">Type: **ULARGE\_INTEGER**</span></span>

</dd> <dd>

<span data-ttu-id="41c35-122">Heure de début de l’analyse.</span><span class="sxs-lookup"><span data-stu-id="41c35-122">Scan start time.</span></span>

</dd> <dt>

<span data-ttu-id="41c35-123">**EndTime**</span><span class="sxs-lookup"><span data-stu-id="41c35-123">**EndTime**</span></span>
</dt> <dd>

<span data-ttu-id="41c35-124">Type : **\_ entier ULARGE**</span><span class="sxs-lookup"><span data-stu-id="41c35-124">Type: **ULARGE\_INTEGER**</span></span>

</dd> <dd>

<span data-ttu-id="41c35-125">Heure de fin de l’analyse.</span><span class="sxs-lookup"><span data-stu-id="41c35-125">Scan end time.</span></span>

</dd> <dt>

<span data-ttu-id="41c35-126">**ThreatStats**</span><span class="sxs-lookup"><span data-stu-id="41c35-126">**ThreatStats**</span></span>
</dt> <dd>

<span data-ttu-id="41c35-127">Type : **[ **\_ statistiques MPTHREAT**](mpthreat-stats.md)**</span><span class="sxs-lookup"><span data-stu-id="41c35-127">Type: **[**MPTHREAT\_STATS**](mpthreat-stats.md)**</span></span>

</dd> <dd>

<span data-ttu-id="41c35-128">Statistiques relatives aux menaces.</span><span class="sxs-lookup"><span data-stu-id="41c35-128">Threat-related statistics.</span></span> <span data-ttu-id="41c35-129">Consultez [**MPTHREAT \_ Statistics**](mpthreat-stats.md).</span><span class="sxs-lookup"><span data-stu-id="41c35-129">See [**MPTHREAT\_STATS**](mpthreat-stats.md).</span></span>

</dd> <dt>

<span data-ttu-id="41c35-130">**ResourceStats**</span><span class="sxs-lookup"><span data-stu-id="41c35-130">**ResourceStats**</span></span>
</dt> <dd>

<span data-ttu-id="41c35-131">Type : **[ **\_ statistiques MPRESOURCE**](mpresource-stats.md)**</span><span class="sxs-lookup"><span data-stu-id="41c35-131">Type: **[**MPRESOURCE\_STATS**](mpresource-stats.md)**</span></span>

</dd> <dd>

<span data-ttu-id="41c35-132">Statistiques relatives aux ressources.</span><span class="sxs-lookup"><span data-stu-id="41c35-132">Resource-related statistics.</span></span> <span data-ttu-id="41c35-133">Consultez [**MPRESOURCE \_ Statistics**](mpresource-stats.md).</span><span class="sxs-lookup"><span data-stu-id="41c35-133">See [**MPRESOURCE\_STATS**](mpresource-stats.md).</span></span>

</dd> <dt>

<span data-ttu-id="41c35-134">**SignatureVersion**</span><span class="sxs-lookup"><span data-stu-id="41c35-134">**SignatureVersion**</span></span>
</dt> <dd>

<span data-ttu-id="41c35-135">Type : **ULONGLONG**</span><span class="sxs-lookup"><span data-stu-id="41c35-135">Type: **ULONGLONG**</span></span>

</dd> <dd>

<span data-ttu-id="41c35-136">Version de signature utilisée pour l’analyse.</span><span class="sxs-lookup"><span data-stu-id="41c35-136">Version of signature used for scan.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="41c35-137">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="41c35-137">Requirements</span></span>



| <span data-ttu-id="41c35-138">Condition requise</span><span class="sxs-lookup"><span data-stu-id="41c35-138">Requirement</span></span> | <span data-ttu-id="41c35-139">Valeur</span><span class="sxs-lookup"><span data-stu-id="41c35-139">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="41c35-140">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="41c35-140">Minimum supported client</span></span><br/> | <span data-ttu-id="41c35-141">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="41c35-141">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="41c35-142">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="41c35-142">Minimum supported server</span></span><br/> | <span data-ttu-id="41c35-143">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="41c35-143">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="41c35-144">En-tête</span><span class="sxs-lookup"><span data-stu-id="41c35-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="41c35-145"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="41c35-145"><dt>MpClient.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="41c35-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="41c35-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41c35-147">**statistiques de MPRESOURCE \_**</span><span class="sxs-lookup"><span data-stu-id="41c35-147">**MPRESOURCE\_STATS**</span></span>](mpresource-stats.md)
</dt> <dt>

[<span data-ttu-id="41c35-148">**\_type MPSCAN**</span><span class="sxs-lookup"><span data-stu-id="41c35-148">**MPSCAN\_TYPE**</span></span>](mpscan-type.md)
</dt> <dt>

[<span data-ttu-id="41c35-149">**MPSOURCE**</span><span class="sxs-lookup"><span data-stu-id="41c35-149">**MPSOURCE**</span></span>](mpsource.md)
</dt> <dt>

[<span data-ttu-id="41c35-150">**statistiques de MPTHREAT \_**</span><span class="sxs-lookup"><span data-stu-id="41c35-150">**MPTHREAT\_STATS**</span></span>](mpthreat-stats.md)
</dt> </dl>

 

 





