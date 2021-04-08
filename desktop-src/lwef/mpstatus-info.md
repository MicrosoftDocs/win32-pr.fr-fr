---
title: Structure MPSTATUS_INFO (MpClient. h)
description: Informations d’État pour le gestionnaire de protection contre les programmes malveillants.
ms.assetid: 614F14EC-64CC-4E3F-8A89-42AA1E0DC95D
keywords:
- Fonctionnalités d’environnement Windows héritées de la structure MPSTATUS_INFO
- PMPSTATUS_INFO des fonctionnalités d’environnement Windows héritées du pointeur de structure
topic_type:
- apiref
api_name:
- MPSTATUS_INFO
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efe31981f819d85d13457553beb1ce3c869b98bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740132"
---
# <a name="mpstatus_info-structure"></a><span data-ttu-id="81f74-105">\_Structure d’informations MPSTATUS</span><span class="sxs-lookup"><span data-stu-id="81f74-105">MPSTATUS\_INFO structure</span></span>

<span data-ttu-id="81f74-106">Informations d’État pour le gestionnaire de protection contre les programmes malveillants.</span><span class="sxs-lookup"><span data-stu-id="81f74-106">Status information for the malware protection manager.</span></span>

## <a name="syntax"></a><span data-ttu-id="81f74-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="81f74-107">Syntax</span></span>


```C++
typedef struct tagMPSTATUS_INFO {
  DWORD               ProductStatus;
  MPSCAN_RESULT       LastQuickScan;
  MPSCAN_RESULT       LastFullScan;
  MPTHREAT_STATS      ThreatStats;
  MPTHREAT_STATS_DATA ThreatState[MP_THREAT_STAT_MAX_VALUE+1];
  MPCOMPONENT_STATUS  Component[MPCOMPONENT_MAXVALUE+1];
  ULARGE_INTEGER      ProductExpirationTime;
} MPSTATUS_INFO, *PMPSTATUS_INFO;
```



## <a name="members"></a><span data-ttu-id="81f74-108">Membres</span><span class="sxs-lookup"><span data-stu-id="81f74-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="81f74-109">**ProductStatus**</span><span class="sxs-lookup"><span data-stu-id="81f74-109">**ProductStatus**</span></span>
</dt> <dd>

<span data-ttu-id="81f74-110">Type : **DWORD**</span><span class="sxs-lookup"><span data-stu-id="81f74-110">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="81f74-111">État général du produit.</span><span class="sxs-lookup"><span data-stu-id="81f74-111">Overall product status.</span></span> <span data-ttu-id="81f74-112">Il s’agit d’une combinaison de bits indicateurs à partir de l' [**\_ indicateur MPSTATUS**](mpstatus-flag.md).</span><span class="sxs-lookup"><span data-stu-id="81f74-112">This is a combination of bit flags from [**MPSTATUS\_FLAG**](mpstatus-flag.md).</span></span>

</dd> <dt>

<span data-ttu-id="81f74-113">**LastQuickScan**</span><span class="sxs-lookup"><span data-stu-id="81f74-113">**LastQuickScan**</span></span>
</dt> <dd>

<span data-ttu-id="81f74-114">Type : **[ **MPSCAN \_ result**](mpscan-result.md)**</span><span class="sxs-lookup"><span data-stu-id="81f74-114">Type: **[**MPSCAN\_RESULT**](mpscan-result.md)**</span></span>

</dd> <dd>

<span data-ttu-id="81f74-115">Résultats de la dernière analyse par le gestionnaire de protection contre les programmes malveillants.</span><span class="sxs-lookup"><span data-stu-id="81f74-115">Results of the last scan by the malware protection manager.</span></span> <span data-ttu-id="81f74-116">Consultez [**\_ résultat de MPSCAN**](mpscan-result.md).</span><span class="sxs-lookup"><span data-stu-id="81f74-116">See [**MPSCAN\_RESULT**](mpscan-result.md).</span></span>

</dd> <dt>

<span data-ttu-id="81f74-117">**LastFullScan**</span><span class="sxs-lookup"><span data-stu-id="81f74-117">**LastFullScan**</span></span>
</dt> <dd>

<span data-ttu-id="81f74-118">Type : **[ **MPSCAN \_ result**](mpscan-result.md)**</span><span class="sxs-lookup"><span data-stu-id="81f74-118">Type: **[**MPSCAN\_RESULT**](mpscan-result.md)**</span></span>

</dd> <dd>

<span data-ttu-id="81f74-119">Résultats de la dernière analyse complète par le gestionnaire de protection contre les programmes malveillants.</span><span class="sxs-lookup"><span data-stu-id="81f74-119">Results of the last full scan by the malware protection manager.</span></span> <span data-ttu-id="81f74-120">Consultez [**\_ résultat de MPSCAN**](mpscan-result.md).</span><span class="sxs-lookup"><span data-stu-id="81f74-120">See [**MPSCAN\_RESULT**](mpscan-result.md).</span></span>

</dd> <dt>

<span data-ttu-id="81f74-121">**ThreatStats**</span><span class="sxs-lookup"><span data-stu-id="81f74-121">**ThreatStats**</span></span>
</dt> <dd>

<span data-ttu-id="81f74-122">Type : **[ **\_ statistiques MPTHREAT**](mpthreat-stats.md)**</span><span class="sxs-lookup"><span data-stu-id="81f74-122">Type: **[**MPTHREAT\_STATS**](mpthreat-stats.md)**</span></span>

</dd> <dd>

<span data-ttu-id="81f74-123">Statistiques actives sur les menaces.</span><span class="sxs-lookup"><span data-stu-id="81f74-123">Active threat statistics.</span></span> <span data-ttu-id="81f74-124">Consultez [**MPTHREAT \_ Statistics**](mpthreat-stats.md).</span><span class="sxs-lookup"><span data-stu-id="81f74-124">See [**MPTHREAT\_STATS**](mpthreat-stats.md).</span></span>

</dd> <dt>

<span data-ttu-id="81f74-125">**ThreatState**</span><span class="sxs-lookup"><span data-stu-id="81f74-125">**ThreatState**</span></span>
</dt> <dd>

<span data-ttu-id="81f74-126">Type : **[**MPTHREAT \_ stats \_ Data**](mpthreat-stats-data.md) \[ MP \_ Threat \_ Stat \_ Max \_ value + 1\]**</span><span class="sxs-lookup"><span data-stu-id="81f74-126">Type: **[**MPTHREAT\_STATS\_DATA**](mpthreat-stats-data.md)\[MP\_THREAT\_STAT\_MAX\_VALUE+1\]**</span></span>

</dd> <dd>

<span data-ttu-id="81f74-127">Données de statistiques supplémentaires sur les menaces, telles que le nombre de menaces.</span><span class="sxs-lookup"><span data-stu-id="81f74-127">Additional threat statistics data, such as the number of threats.</span></span> <span data-ttu-id="81f74-128">Consultez [**\_ \_ données statistiques MPTHREAT**](mpthreat-stats-data.md).</span><span class="sxs-lookup"><span data-stu-id="81f74-128">See [**MPTHREAT\_STATS\_DATA**](mpthreat-stats-data.md).</span></span>

</dd> <dt>

<span data-ttu-id="81f74-129">**Composant**</span><span class="sxs-lookup"><span data-stu-id="81f74-129">**Component**</span></span>
</dt> <dd>

<span data-ttu-id="81f74-130">Type : **[**MPCOMPONENT \_ Status**](mpcomponent-status.md) \[ MPCOMPONENT \_ MaxValue + 1\]**</span><span class="sxs-lookup"><span data-stu-id="81f74-130">Type: **[**MPCOMPONENT\_STATUS**](mpcomponent-status.md)\[MPCOMPONENT\_MAXVALUE+1\]**</span></span>

</dd> <dd>

<span data-ttu-id="81f74-131">Tableau d’États pour plusieurs composants.</span><span class="sxs-lookup"><span data-stu-id="81f74-131">An array of statuses for multiple components.</span></span> <span data-ttu-id="81f74-132">Utilisez une valeur de l’énumération [**MPCOMPONENT \_ ID**](mpcomponent-id.md) en tant qu’index dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="81f74-132">Use a value from the [**MPCOMPONENT\_ID**](mpcomponent-id.md) enumeration as an index into the array.</span></span>

</dd> <dt>

<span data-ttu-id="81f74-133">**ProductExpirationTime**</span><span class="sxs-lookup"><span data-stu-id="81f74-133">**ProductExpirationTime**</span></span>
</dt> <dd>

<span data-ttu-id="81f74-134">Type : **\_ entier ULARGE**</span><span class="sxs-lookup"><span data-stu-id="81f74-134">Type: **ULARGE\_INTEGER**</span></span>

</dd> <dd>

<span data-ttu-id="81f74-135">Horodateur d’expiration du produit dans UNC.</span><span class="sxs-lookup"><span data-stu-id="81f74-135">Product expiration timestamp in UNC.</span></span> <span data-ttu-id="81f74-136">Cela est valide uniquement si l’état d’expiration est défini.</span><span class="sxs-lookup"><span data-stu-id="81f74-136">This is valid only if the expiration status is set.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="81f74-137">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="81f74-137">Requirements</span></span>



| <span data-ttu-id="81f74-138">Condition requise</span><span class="sxs-lookup"><span data-stu-id="81f74-138">Requirement</span></span> | <span data-ttu-id="81f74-139">Valeur</span><span class="sxs-lookup"><span data-stu-id="81f74-139">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="81f74-140">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="81f74-140">Minimum supported client</span></span><br/> | <span data-ttu-id="81f74-141">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="81f74-141">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="81f74-142">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="81f74-142">Minimum supported server</span></span><br/> | <span data-ttu-id="81f74-143">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="81f74-143">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="81f74-144">En-tête</span><span class="sxs-lookup"><span data-stu-id="81f74-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="81f74-145"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="81f74-145"><dt>MpClient.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81f74-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="81f74-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81f74-147">**\_ID MPCOMPONENT**</span><span class="sxs-lookup"><span data-stu-id="81f74-147">**MPCOMPONENT\_ID**</span></span>](mpcomponent-id.md)
</dt> <dt>

[<span data-ttu-id="81f74-148">**État de MPCOMPONENT \_**</span><span class="sxs-lookup"><span data-stu-id="81f74-148">**MPCOMPONENT\_STATUS**</span></span>](mpcomponent-status.md)
</dt> <dt>

[<span data-ttu-id="81f74-149">**résultat de MPSCAN \_**</span><span class="sxs-lookup"><span data-stu-id="81f74-149">**MPSCAN\_RESULT**</span></span>](mpscan-result.md)
</dt> <dt>

[<span data-ttu-id="81f74-150">**\_indicateur MPSTATUS**</span><span class="sxs-lookup"><span data-stu-id="81f74-150">**MPSTATUS\_FLAG**</span></span>](mpstatus-flag.md)
</dt> <dt>

[<span data-ttu-id="81f74-151">**statistiques de MPTHREAT \_**</span><span class="sxs-lookup"><span data-stu-id="81f74-151">**MPTHREAT\_STATS**</span></span>](mpthreat-stats.md)
</dt> <dt>

[<span data-ttu-id="81f74-152">**\_données statistiques \_ MPTHREAT**</span><span class="sxs-lookup"><span data-stu-id="81f74-152">**MPTHREAT\_STATS\_DATA**</span></span>](mpthreat-stats-data.md)
</dt> </dl>

 

 





