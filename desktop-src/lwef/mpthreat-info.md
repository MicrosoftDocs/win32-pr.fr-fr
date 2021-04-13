---
title: Structure MPTHREAT_INFO (MpClient. h)
description: Contient des informations sur une menace.
ms.assetid: ED2A0BDB-0E7C-479D-ADA1-95B9A259F57E
keywords:
- Fonctionnalités d’environnement Windows héritées de la structure MPTHREAT_INFO
- PMPTHREAT_INFO des fonctionnalités d’environnement Windows héritées du pointeur de structure
topic_type:
- apiref
api_name:
- MPTHREAT_INFO
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfa850a4293006a2f4b107a3f2579fdc14c1ea6e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466655"
---
# <a name="mpthreat_info-structure"></a><span data-ttu-id="181c1-105">\_Structure d’informations MPTHREAT</span><span class="sxs-lookup"><span data-stu-id="181c1-105">MPTHREAT\_INFO structure</span></span>

<span data-ttu-id="181c1-106">Contient des informations sur une menace.</span><span class="sxs-lookup"><span data-stu-id="181c1-106">Contains information about a threat.</span></span>

## <a name="syntax"></a><span data-ttu-id="181c1-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="181c1-107">Syntax</span></span>


```C++
typedef struct tagMPTHREAT_INFO {
  MPTHREAT_ID           ThreatID;
  GUID                  DetectionID;
  MP_MIDL_STRING LPWSTR Name;
  MPTHREAT_TYPE         ThreatType;
  MPTHREAT_SEVERITY     ThreatCriticality;
  MPTHREAT_CATEGORY     ThreatCategory;
  DWORD                 ThreatShortDescriptionID;
  DWORD                 ThreatAdviseDescriptionID;
  MPTHREAT_STATUS       ThreatStatus;
  DWORD                 SuggestedActionCount;
  MPTHREAT_ACTION       SuggestedActionArray[MP_MAX_SUGGESTIONS];
  DWORD                 ResourceCount;
  PMPRESOURCE_INFO      *ResourceList[ResourceCount];
  ULARGE_INTEGER        ThreatStatusTime;
  HRESULT               ThreatStatusCode;
  MPTHREAT_DETECTION    ThreatDetection;
  GUID                  QuarantineGuid;
  MPEXECUTION_STATUS    ExecutionStatus;
  union {
    PMPTHREAT_INFOEX_UNUSED   pKnownBad;
    PMPTHREAT_INFOEX_BEHAVIOR pBehavior;
    PMPTHREAT_INFOEX_UNUSED   pUnknown;
    PMPTHREAT_INFOEX_UNUSED   pKnownGood;
    PMPTHREAT_INFOEX_NIS      pNis;
  } Data;
  MPDETECTION_STATE     State;
  MP_MIDL_STRING LPWSTR DetectionUser;
  MPSOURCE              DetectionSource;
  MP_MIDL_STRING LPWSTR ProcessName;
  MPDETECTION_ORIGIN    DetectionOrigin;
  DWORD                 reserved1;
  ULARGE_INTEGER        DetectionTime;
  MPEXECUTION_STATUS    PreExecutionStatus;
  ULARGE_INTEGER        RemediationTime;
  MPEXECUTION_STATUS    PostExecutionStatus;
  BOOL                  CriticalFailure;
  DWORD                 NonCriticalReason;
  MP_MIDL_STRING LPWSTR RemediationUser;
  DWORD                 RemediationResourceCount;
  PMPRESOURCE_INFO      RemediationResourceList[RemediationResourceCount];
  BOOL                  FailureResolved;
  MPRESOLVED_REASON     ResolvedReason;
  DWORD                 AdditionalActions;
  DWORD                 ResolvedActions;
  DWORD                 dwThreatStatusFlag;
} MPTHREAT_INFO, *PMPTHREAT_INFO;
```



## <a name="members"></a><span data-ttu-id="181c1-108">Membres</span><span class="sxs-lookup"><span data-stu-id="181c1-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="181c1-109">**ThreatID**</span><span class="sxs-lookup"><span data-stu-id="181c1-109">**ThreatID**</span></span>
</dt> <dd>

<span data-ttu-id="181c1-110">Type : **\_ ID MPTHREAT**</span><span class="sxs-lookup"><span data-stu-id="181c1-110">Type: **MPTHREAT\_ID**</span></span>

</dd> <dd>

<span data-ttu-id="181c1-111">Identificateur de la menace.</span><span class="sxs-lookup"><span data-stu-id="181c1-111">Threat identifier.</span></span> <span data-ttu-id="181c1-112">Le bit supérieur est défini pour identifier les menaces liées à l’antivirus.</span><span class="sxs-lookup"><span data-stu-id="181c1-112">Upper bit is set to identify antivirus-related threats.</span></span>

</dd> <dt>

<span data-ttu-id="181c1-113">**DetectionID**</span><span class="sxs-lookup"><span data-stu-id="181c1-113">**DetectionID**</span></span>
</dt> <dd>

<span data-ttu-id="181c1-114">Type : **GUID**</span><span class="sxs-lookup"><span data-stu-id="181c1-114">Type: **GUID**</span></span>

</dd> <dd>

<span data-ttu-id="181c1-115">ID de détection.</span><span class="sxs-lookup"><span data-stu-id="181c1-115">Detection ID.</span></span>

</dd> <dt>

<span data-ttu-id="181c1-116">**Nom**</span><span class="sxs-lookup"><span data-stu-id="181c1-116">**Name**</span></span>
</dt> <dd>

<span data-ttu-id="181c1-117">Type : **MP \_ MIDL \_ String** de type LPWStr</span><span class="sxs-lookup"><span data-stu-id="181c1-117">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="181c1-118">Nom de la menace.</span><span class="sxs-lookup"><span data-stu-id="181c1-118">Threat name.</span></span>

</dd> <dt>

<span data-ttu-id="181c1-119">**ThreatType**</span><span class="sxs-lookup"><span data-stu-id="181c1-119">**ThreatType**</span></span>
</dt> <dd>

<span data-ttu-id="181c1-120">Type : **[ **MPTHREAT \_**](mpthreat-type.md)**</span><span class="sxs-lookup"><span data-stu-id="181c1-120">Type: **[**MPTHREAT\_TYPE**](mpthreat-type.md)**</span></span>

</dd> <dd>

<span data-ttu-id="181c1-121">Type de menace.</span><span class="sxs-lookup"><span data-stu-id="181c1-121">Threat type.</span></span> <span data-ttu-id="181c1-122">Permet de faire la distinction entre différents types de menaces, tels que connu, inconnu ou bien connu.</span><span class="sxs-lookup"><span data-stu-id="181c1-122">Used to differentiate among different threat types such as known bad, unknown, or known good.</span></span> <span data-ttu-id="181c1-123">Consultez [**\_ type MPTHREAT**](mpthreat-type.md).</span><span class="sxs-lookup"><span data-stu-id="181c1-123">See [**MPTHREAT\_TYPE**](mpthreat-type.md).</span></span>

</dd> <dt>

<span data-ttu-id="181c1-124">**ThreatCriticality**</span><span class="sxs-lookup"><span data-stu-id="181c1-124">**ThreatCriticality**</span></span>
</dt> <dd>

<span data-ttu-id="181c1-125">Type : **[ **MPTHREAT \_ Severity**](mpthreat-severity.md)**</span><span class="sxs-lookup"><span data-stu-id="181c1-125">Type: **[**MPTHREAT\_SEVERITY**](mpthreat-severity.md)**</span></span>

</dd> <dd>

<span data-ttu-id="181c1-126">Gravité des menaces.</span><span class="sxs-lookup"><span data-stu-id="181c1-126">Threat criticality.</span></span> <span data-ttu-id="181c1-127">Consultez [**\_ gravité MPTHREAT**](mpthreat-severity.md).</span><span class="sxs-lookup"><span data-stu-id="181c1-127">See [**MPTHREAT\_SEVERITY**](mpthreat-severity.md).</span></span>

</dd> <dt>

<span data-ttu-id="181c1-128">**ThreatCategory**</span><span class="sxs-lookup"><span data-stu-id="181c1-128">**ThreatCategory**</span></span>
</dt> <dd>

<span data-ttu-id="181c1-129">Type : **[ **MPTHREAT \_ Category**](mpthreat-category.md)**</span><span class="sxs-lookup"><span data-stu-id="181c1-129">Type: **[**MPTHREAT\_CATEGORY**](mpthreat-category.md)**</span></span>

</dd> <dd>

<span data-ttu-id="181c1-130">Catégorie de menace, comme un cheval de Troie ou un enregistreur d’enregistreur.</span><span class="sxs-lookup"><span data-stu-id="181c1-130">Threat category, such as a trojan or a keylogger.</span></span> <span data-ttu-id="181c1-131">Consultez [**la \_ catégorie MPTHREAT**](mpthreat-category.md).</span><span class="sxs-lookup"><span data-stu-id="181c1-131">See [**MPTHREAT\_CATEGORY**](mpthreat-category.md).</span></span>

</dd> <dt>

<span data-ttu-id="181c1-132">**ThreatShortDescriptionID**</span><span class="sxs-lookup"><span data-stu-id="181c1-132">**ThreatShortDescriptionID**</span></span>
</dt> <dd>

<span data-ttu-id="181c1-133">Type : **DWORD**</span><span class="sxs-lookup"><span data-stu-id="181c1-133">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="181c1-134">ID de description brève de la menace.</span><span class="sxs-lookup"><span data-stu-id="181c1-134">Threat short description ID.</span></span>

</dd> <dt>

<span data-ttu-id="181c1-135">**ThreatAdviseDescriptionID**</span><span class="sxs-lookup"><span data-stu-id="181c1-135">**ThreatAdviseDescriptionID**</span></span>
</dt> <dd>

<span data-ttu-id="181c1-136">Type : **DWORD**</span><span class="sxs-lookup"><span data-stu-id="181c1-136">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="181c1-137">ID de description de l’avis de menace.</span><span class="sxs-lookup"><span data-stu-id="181c1-137">Threat advise description ID.</span></span>

</dd> <dt>

<span data-ttu-id="181c1-138">**ThreatStatus**</span><span class="sxs-lookup"><span data-stu-id="181c1-138">**ThreatStatus**</span></span>
</dt> <dd>

<span data-ttu-id="181c1-139">Type : **[ **MPTHREAT \_ Status**](mpthreat-status.md)**</span><span class="sxs-lookup"><span data-stu-id="181c1-139">Type: **[**MPTHREAT\_STATUS**](mpthreat-status.md)**</span></span>

</dd> <dd>

<span data-ttu-id="181c1-140">État de la menace, tel que détecté, nettoyé ou mis en quarantaine.</span><span class="sxs-lookup"><span data-stu-id="181c1-140">Threat status such as detected, cleaned, or quarantined.</span></span> <span data-ttu-id="181c1-141">Consultez [**l' \_ État de MPTHREAT**](mpthreat-status.md).</span><span class="sxs-lookup"><span data-stu-id="181c1-141">See [**MPTHREAT\_STATUS**](mpthreat-status.md).</span></span>

</dd> <dt>

<span data-ttu-id="181c1-142">**SuggestedActionCount**</span><span class="sxs-lookup"><span data-stu-id="181c1-142">**SuggestedActionCount**</span></span>
</dt> <dd>

<span data-ttu-id="181c1-143">Type : **DWORD**</span><span class="sxs-lookup"><span data-stu-id="181c1-143">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="181c1-144">Nombre d’actions suggérées dans **SuggestedActionArray**.</span><span class="sxs-lookup"><span data-stu-id="181c1-144">Count of suggested actions in **SuggestedActionArray**.</span></span>

</dd> <dt>

<span data-ttu-id="181c1-145">**SuggestedActionArray**</span><span class="sxs-lookup"><span data-stu-id="181c1-145">**SuggestedActionArray**</span></span>
</dt> <dd>

<span data-ttu-id="181c1-146">Type : **[**\_ actions MPTHREAT action**](mpthreat-action.md) \[ MP \_ Max \_ suggestions\]**</span><span class="sxs-lookup"><span data-stu-id="181c1-146">Type: **[**MPTHREAT\_ACTION**](mpthreat-action.md)\[MP\_MAX\_SUGGESTIONS\]**</span></span>

</dd> <dd>

<span data-ttu-id="181c1-147">Tableau d’actions suggérées.</span><span class="sxs-lookup"><span data-stu-id="181c1-147">Array of suggested actions.</span></span> <span data-ttu-id="181c1-148">Consultez [**\_ action MPTHREAT**](mpthreat-action.md).</span><span class="sxs-lookup"><span data-stu-id="181c1-148">See [**MPTHREAT\_ACTION**](mpthreat-action.md).</span></span>

</dd> <dt>

<span data-ttu-id="181c1-149">**ResourceCount**</span><span class="sxs-lookup"><span data-stu-id="181c1-149">**ResourceCount**</span></span>
</dt> <dd>

<span data-ttu-id="181c1-150">Type : **DWORD**</span><span class="sxs-lookup"><span data-stu-id="181c1-150">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="181c1-151">Nombre de ressources dans **ResourceList**.</span><span class="sxs-lookup"><span data-stu-id="181c1-151">Count of resources in **ResourceList**.</span></span>

</dd> <dt>

<span data-ttu-id="181c1-152">**ResourceList**</span><span class="sxs-lookup"><span data-stu-id="181c1-152">**ResourceList**</span></span>
</dt> <dd>

<span data-ttu-id="181c1-153">Type : \**PMPRESOURCE \_ info \** _</span><span class="sxs-lookup"><span data-stu-id="181c1-153">Type: \**PMPRESOURCE\_INFO\** _</span></span>

</dd> <dd>

<span data-ttu-id="181c1-154">Liste des ressources identifiées par la menace.</span><span class="sxs-lookup"><span data-stu-id="181c1-154">List of resources identified with the threat.</span></span> <span data-ttu-id="181c1-155">Consultez [_ *MPRESOURCE \_ info* \*](mpresource-info.md).</span><span class="sxs-lookup"><span data-stu-id="181c1-155">See [_ *MPRESOURCE\_INFO*\*](mpresource-info.md).</span></span>

</dd> <dt>

<span data-ttu-id="181c1-156">**ThreatStatusTime**</span><span class="sxs-lookup"><span data-stu-id="181c1-156">**ThreatStatusTime**</span></span>
</dt> <dd>

<span data-ttu-id="181c1-157">Type : **\_ entier ULARGE**</span><span class="sxs-lookup"><span data-stu-id="181c1-157">Type: **ULARGE\_INTEGER**</span></span>

</dd> <dd>

<span data-ttu-id="181c1-158">Heure de la dernière modification de l’état de la menace.</span><span class="sxs-lookup"><span data-stu-id="181c1-158">Time when threat status last changed.</span></span>

</dd> <dt>

<span data-ttu-id="181c1-159">**ThreatStatusCode**</span><span class="sxs-lookup"><span data-stu-id="181c1-159">**ThreatStatusCode**</span></span>
</dt> <dd>

<span data-ttu-id="181c1-160">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="181c1-160">Type: **HRESULT**</span></span>

</dd> <dd>

<span data-ttu-id="181c1-161">Code d’état associé à l’état de la menace.</span><span class="sxs-lookup"><span data-stu-id="181c1-161">Status code associated with the threat status.</span></span>

</dd> <dt>

<span data-ttu-id="181c1-162">**ThreatDetection**</span><span class="sxs-lookup"><span data-stu-id="181c1-162">**ThreatDetection**</span></span>
</dt> <dd>

<span data-ttu-id="181c1-163">Type : **[ **\_ détection MPTHREAT**](mpthreat-detection.md)**</span><span class="sxs-lookup"><span data-stu-id="181c1-163">Type: **[**MPTHREAT\_DETECTION**](mpthreat-detection.md)**</span></span>

</dd> <dd>

<span data-ttu-id="181c1-164">Type de détection des menaces, par exemple concret, suspect ou générique.</span><span class="sxs-lookup"><span data-stu-id="181c1-164">Threat detection type, such as concrete, suspicious, or generic.</span></span> <span data-ttu-id="181c1-165">Consultez [**MPTHREAT \_ Detection**](mpthreat-detection.md).</span><span class="sxs-lookup"><span data-stu-id="181c1-165">See [**MPTHREAT\_DETECTION**](mpthreat-detection.md).</span></span>

</dd> <dt>

<span data-ttu-id="181c1-166">**QuarantineGuid**</span><span class="sxs-lookup"><span data-stu-id="181c1-166">**QuarantineGuid**</span></span>
</dt> <dd>

<span data-ttu-id="181c1-167">Type : **GUID**</span><span class="sxs-lookup"><span data-stu-id="181c1-167">Type: **GUID**</span></span>

</dd> <dd>

<span data-ttu-id="181c1-168">GUID de mise en quarantaine.</span><span class="sxs-lookup"><span data-stu-id="181c1-168">Quarantine guid.</span></span>

</dd> <dt>

<span data-ttu-id="181c1-169">**ExecutionStatus**</span><span class="sxs-lookup"><span data-stu-id="181c1-169">**ExecutionStatus**</span></span>
</dt> <dd>

<span data-ttu-id="181c1-170">Type : **[ **MPEXECUTION \_ Status**](mpexecution-status.md)**</span><span class="sxs-lookup"><span data-stu-id="181c1-170">Type: **[**MPEXECUTION\_STATUS**](mpexecution-status.md)**</span></span>

</dd> <dd>

<span data-ttu-id="181c1-171">État de l’exécution de la menace, tel que inconnu, bloqué ou actif.</span><span class="sxs-lookup"><span data-stu-id="181c1-171">Execution status of the threat, such as not known, blocked, or active.</span></span> <span data-ttu-id="181c1-172">Consultez [**l' \_ État de MPEXECUTION**](mpexecution-status.md).</span><span class="sxs-lookup"><span data-stu-id="181c1-172">See [**MPEXECUTION\_STATUS**](mpexecution-status.md).</span></span>

</dd> <dt>

<span data-ttu-id="181c1-173">**Données**</span><span class="sxs-lookup"><span data-stu-id="181c1-173">**Data**</span></span>
</dt> <dd>

<span data-ttu-id="181c1-174">Informations supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="181c1-174">Extra information.</span></span> <span data-ttu-id="181c1-175">Le pointeur vers la structure appropriée dépend de la valeur de **ThreatType**.</span><span class="sxs-lookup"><span data-stu-id="181c1-175">The pointer to the appropriate structure depends on the value of **ThreatType**.</span></span>

<dl> <dt>

<span data-ttu-id="181c1-176">**pKnownBad**</span><span class="sxs-lookup"><span data-stu-id="181c1-176">**pKnownBad**</span></span>
</dt> <dd>

<span data-ttu-id="181c1-177">Type : **PMPTHREAT \_ INFOEX \_ inutilisé**</span><span class="sxs-lookup"><span data-stu-id="181c1-177">Type: **PMPTHREAT\_INFOEX\_UNUSED**</span></span>

</dd> <dd>

<span data-ttu-id="181c1-178">Lorsque **ThreatType**  ==  **MPTHREAT, \_ tapez \_ KNOWNBAD**.</span><span class="sxs-lookup"><span data-stu-id="181c1-178">When **ThreatType** == **MPTHREAT\_TYPE\_KNOWNBAD**.</span></span> <span data-ttu-id="181c1-179">Consultez [**MPTHREAT \_ INFOEX \_ inutilisé**](mpthreat-infoex-unused.md).</span><span class="sxs-lookup"><span data-stu-id="181c1-179">See [**MPTHREAT\_INFOEX\_UNUSED**](mpthreat-infoex-unused.md).</span></span>

</dd> <dt>

<span data-ttu-id="181c1-180">**pBehavior**</span><span class="sxs-lookup"><span data-stu-id="181c1-180">**pBehavior**</span></span>
</dt> <dd>

<span data-ttu-id="181c1-181">Type : **PMPTHREAT \_ INFOEX \_ BEHAVIOR**</span><span class="sxs-lookup"><span data-stu-id="181c1-181">Type: **PMPTHREAT\_INFOEX\_BEHAVIOR**</span></span>

</dd> <dd>

<span data-ttu-id="181c1-182">Lorsque le  ==  **\_ \_ comportement de type ThreatType MPTHREAT**.</span><span class="sxs-lookup"><span data-stu-id="181c1-182">When **ThreatType** == **MPTHREAT\_TYPE\_BEHAVIOR**.</span></span> <span data-ttu-id="181c1-183">Consultez [**\_ \_ comportement de MPTHREAT INFOEX**](mpthreat-infoex-behavior.md).</span><span class="sxs-lookup"><span data-stu-id="181c1-183">See [**MPTHREAT\_INFOEX\_BEHAVIOR**](mpthreat-infoex-behavior.md).</span></span>

</dd> <dt>

<span data-ttu-id="181c1-184">**pUnknown**</span><span class="sxs-lookup"><span data-stu-id="181c1-184">**pUnknown**</span></span>
</dt> <dd>

<span data-ttu-id="181c1-185">Type : **PMPTHREAT \_ INFOEX \_ inutilisé**</span><span class="sxs-lookup"><span data-stu-id="181c1-185">Type: **PMPTHREAT\_INFOEX\_UNUSED**</span></span>

</dd> <dd>

<span data-ttu-id="181c1-186">Quand le type **ThreatType**  ==  **MPTHREAT est \_ \_ inconnu**.</span><span class="sxs-lookup"><span data-stu-id="181c1-186">When **ThreatType** == **MPTHREAT\_TYPE\_UNKNOWN**.</span></span> <span data-ttu-id="181c1-187">Consultez [**MPTHREAT \_ INFOEX \_ inutilisé**](mpthreat-infoex-unused.md).</span><span class="sxs-lookup"><span data-stu-id="181c1-187">See [**MPTHREAT\_INFOEX\_UNUSED**](mpthreat-infoex-unused.md).</span></span>

</dd> <dt>

<span data-ttu-id="181c1-188">**pKnownGood**</span><span class="sxs-lookup"><span data-stu-id="181c1-188">**pKnownGood**</span></span>
</dt> <dd>

<span data-ttu-id="181c1-189">Type : **PMPTHREAT \_ INFOEX \_ inutilisé**</span><span class="sxs-lookup"><span data-stu-id="181c1-189">Type: **PMPTHREAT\_INFOEX\_UNUSED**</span></span>

</dd> <dd>

<span data-ttu-id="181c1-190">Lorsque **ThreatType** = = MPTHREAT \_ \_ , tapez KNOWNGOOD.</span><span class="sxs-lookup"><span data-stu-id="181c1-190">When **ThreatType** == MPTHREAT\_TYPE\_KNOWNGOOD.</span></span> <span data-ttu-id="181c1-191">Consultez [**MPTHREAT \_ INFOEX \_ inutilisé**](mpthreat-infoex-unused.md).</span><span class="sxs-lookup"><span data-stu-id="181c1-191">See [**MPTHREAT\_INFOEX\_UNUSED**](mpthreat-infoex-unused.md).</span></span>

</dd> <dt>

<span data-ttu-id="181c1-192">**pNis**</span><span class="sxs-lookup"><span data-stu-id="181c1-192">**pNis**</span></span>
</dt> <dd>

<span data-ttu-id="181c1-193">Type : **PMPTHREAT \_ INFOEX \_ NIS**</span><span class="sxs-lookup"><span data-stu-id="181c1-193">Type: **PMPTHREAT\_INFOEX\_NIS**</span></span>

</dd> <dd>

<span data-ttu-id="181c1-194">Lorsque **ThreatType**  ==  **MPTHREAT \_ type \_ NIS**.</span><span class="sxs-lookup"><span data-stu-id="181c1-194">When **ThreatType** == **MPTHREAT\_TYPE\_NIS**.</span></span> <span data-ttu-id="181c1-195">Consultez [**MPTHREAT \_ INFOEX \_ NIS**](mpthreat-infoex-nis.md).</span><span class="sxs-lookup"><span data-stu-id="181c1-195">See [**MPTHREAT\_INFOEX\_NIS**](mpthreat-infoex-nis.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="181c1-196">**State**</span><span class="sxs-lookup"><span data-stu-id="181c1-196">**State**</span></span>
</dt> <dd>

<span data-ttu-id="181c1-197">Type : **[ **MPDETECTION \_ State**](mpdetection-state.md)**</span><span class="sxs-lookup"><span data-stu-id="181c1-197">Type: **[**MPDETECTION\_STATE**](mpdetection-state.md)**</span></span>

</dd> <dd>

<span data-ttu-id="181c1-198">État actuel de la détection.</span><span class="sxs-lookup"><span data-stu-id="181c1-198">The current state of the detection.</span></span> <span data-ttu-id="181c1-199">Consultez [**\_ État de MPDETECTION**](mpdetection-state.md).</span><span class="sxs-lookup"><span data-stu-id="181c1-199">See [**MPDETECTION\_STATE**](mpdetection-state.md).</span></span>

</dd> <dt>

<span data-ttu-id="181c1-200">**DetectionUser**</span><span class="sxs-lookup"><span data-stu-id="181c1-200">**DetectionUser**</span></span>
</dt> <dd>

<span data-ttu-id="181c1-201">Type : **MP \_ MIDL \_ String** de type LPWStr</span><span class="sxs-lookup"><span data-stu-id="181c1-201">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="181c1-202">Utilisateur associé à la détection, au format « domaine/utilisateur ».</span><span class="sxs-lookup"><span data-stu-id="181c1-202">The user associated with the detection, in the format "domain/user".</span></span>

</dd> <dt>

<span data-ttu-id="181c1-203">**DetectionSource**</span><span class="sxs-lookup"><span data-stu-id="181c1-203">**DetectionSource**</span></span>
</dt> <dd>

<span data-ttu-id="181c1-204">Type : **[ **MPSOURCE**](mpsource.md)**</span><span class="sxs-lookup"><span data-stu-id="181c1-204">Type: **[**MPSOURCE**](mpsource.md)**</span></span>

</dd> <dd>

<span data-ttu-id="181c1-205">Source de la détection.</span><span class="sxs-lookup"><span data-stu-id="181c1-205">The source of the detection.</span></span> <span data-ttu-id="181c1-206">Consultez [**MPSOURCE**](mpsource.md).</span><span class="sxs-lookup"><span data-stu-id="181c1-206">See [**MPSOURCE**](mpsource.md).</span></span>

</dd> <dt>

<span data-ttu-id="181c1-207">**ProcessName**</span><span class="sxs-lookup"><span data-stu-id="181c1-207">**ProcessName**</span></span>
</dt> <dd>

<span data-ttu-id="181c1-208">Type : **MP \_ MIDL \_ String** de type LPWStr</span><span class="sxs-lookup"><span data-stu-id="181c1-208">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="181c1-209">Nom du processus associé à la détection.</span><span class="sxs-lookup"><span data-stu-id="181c1-209">Process name associated with the detection.</span></span>

</dd> <dt>

<span data-ttu-id="181c1-210">**DetectionOrigin**</span><span class="sxs-lookup"><span data-stu-id="181c1-210">**DetectionOrigin**</span></span>
</dt> <dd>

<span data-ttu-id="181c1-211">Type : **[ **MPDETECTION \_ origin**](mpdetection-origin.md)**</span><span class="sxs-lookup"><span data-stu-id="181c1-211">Type: **[**MPDETECTION\_ORIGIN**](mpdetection-origin.md)**</span></span>

</dd> <dd>

<span data-ttu-id="181c1-212">Origine de la détection, telle que local ou réseau.</span><span class="sxs-lookup"><span data-stu-id="181c1-212">The origin of the detection, such as local or network.</span></span> <span data-ttu-id="181c1-213">Consultez [**MPDETECTION \_ origin**](mpdetection-origin.md).</span><span class="sxs-lookup"><span data-stu-id="181c1-213">See [**MPDETECTION\_ORIGIN**](mpdetection-origin.md).</span></span>

</dd> <dt>

<span data-ttu-id="181c1-214">**Reserved1**</span><span class="sxs-lookup"><span data-stu-id="181c1-214">**reserved1**</span></span>
</dt> <dd>

<span data-ttu-id="181c1-215">Type : **DWORD**</span><span class="sxs-lookup"><span data-stu-id="181c1-215">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="181c1-216">Métadonnées réservées sur la détection.</span><span class="sxs-lookup"><span data-stu-id="181c1-216">Reserved metadata about the detection.</span></span>

</dd> <dt>

<span data-ttu-id="181c1-217">**DetectionTime**</span><span class="sxs-lookup"><span data-stu-id="181c1-217">**DetectionTime**</span></span>
</dt> <dd>

<span data-ttu-id="181c1-218">Type : **\_ entier ULARGE**</span><span class="sxs-lookup"><span data-stu-id="181c1-218">Type: **ULARGE\_INTEGER**</span></span>

</dd> <dd>

<span data-ttu-id="181c1-219">Heure de la détection initiale.</span><span class="sxs-lookup"><span data-stu-id="181c1-219">The time of the initial detection.</span></span>

</dd> <dt>

<span data-ttu-id="181c1-220">**PreExecutionStatus**</span><span class="sxs-lookup"><span data-stu-id="181c1-220">**PreExecutionStatus**</span></span>
</dt> <dd>

<span data-ttu-id="181c1-221">Type : **[ **MPEXECUTION \_ Status**](mpexecution-status.md)**</span><span class="sxs-lookup"><span data-stu-id="181c1-221">Type: **[**MPEXECUTION\_STATUS**](mpexecution-status.md)**</span></span>

</dd> <dd>

<span data-ttu-id="181c1-222">État de l’exécution juste avant la correction.</span><span class="sxs-lookup"><span data-stu-id="181c1-222">Execution status right before remediation.</span></span> <span data-ttu-id="181c1-223">Consultez [**l' \_ État de MPEXECUTION**](mpexecution-status.md).</span><span class="sxs-lookup"><span data-stu-id="181c1-223">See [**MPEXECUTION\_STATUS**](mpexecution-status.md).</span></span>

</dd> <dt>

<span data-ttu-id="181c1-224">**RemediationTime**</span><span class="sxs-lookup"><span data-stu-id="181c1-224">**RemediationTime**</span></span>
</dt> <dd>

<span data-ttu-id="181c1-225">Type : **\_ entier ULARGE**</span><span class="sxs-lookup"><span data-stu-id="181c1-225">Type: **ULARGE\_INTEGER**</span></span>

</dd> <dd>

<span data-ttu-id="181c1-226">La mise à jour de l’heure s’est produite.</span><span class="sxs-lookup"><span data-stu-id="181c1-226">The time remediation occured.</span></span>

</dd> <dt>

<span data-ttu-id="181c1-227">**PostExecutionStatus**</span><span class="sxs-lookup"><span data-stu-id="181c1-227">**PostExecutionStatus**</span></span>
</dt> <dd>

<span data-ttu-id="181c1-228">Type : **[ **MPEXECUTION \_ Status**](mpexecution-status.md)**</span><span class="sxs-lookup"><span data-stu-id="181c1-228">Type: **[**MPEXECUTION\_STATUS**](mpexecution-status.md)**</span></span>

</dd> <dd>

<span data-ttu-id="181c1-229">État de l’exécution après la correction.</span><span class="sxs-lookup"><span data-stu-id="181c1-229">Execution status after remediation.</span></span> <span data-ttu-id="181c1-230">Consultez [**l' \_ État de MPEXECUTION**](mpexecution-status.md).</span><span class="sxs-lookup"><span data-stu-id="181c1-230">See [**MPEXECUTION\_STATUS**](mpexecution-status.md).</span></span>

</dd> <dt>

<span data-ttu-id="181c1-231">**CriticalFailure**</span><span class="sxs-lookup"><span data-stu-id="181c1-231">**CriticalFailure**</span></span>
</dt> <dd>

<span data-ttu-id="181c1-232">Type : **bool**</span><span class="sxs-lookup"><span data-stu-id="181c1-232">Type: **BOOL**</span></span>

</dd> <dd>

<span data-ttu-id="181c1-233">True si l’échec de la correction était critique.</span><span class="sxs-lookup"><span data-stu-id="181c1-233">True if the remediation failure was critical.</span></span>

</dd> <dt>

<span data-ttu-id="181c1-234">**NonCriticalReason**</span><span class="sxs-lookup"><span data-stu-id="181c1-234">**NonCriticalReason**</span></span>
</dt> <dd>

<span data-ttu-id="181c1-235">Type : **DWORD**</span><span class="sxs-lookup"><span data-stu-id="181c1-235">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="181c1-236">La raison de l’échec de la mise à jour n’est pas critique.</span><span class="sxs-lookup"><span data-stu-id="181c1-236">The reason the remediation failure is not critical.</span></span> <span data-ttu-id="181c1-237">Il n’est pas garanti que cela soit pris en charge à l’avenir.</span><span class="sxs-lookup"><span data-stu-id="181c1-237">This is not guaranteed to be supported in the future.</span></span>

</dd> <dt>

<span data-ttu-id="181c1-238">**RemediationUser**</span><span class="sxs-lookup"><span data-stu-id="181c1-238">**RemediationUser**</span></span>
</dt> <dd>

<span data-ttu-id="181c1-239">Type : **MP \_ MIDL \_ String** de type LPWStr</span><span class="sxs-lookup"><span data-stu-id="181c1-239">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="181c1-240">Utilisateur qui a demandé la mise à jour, au format « domaine/utilisateur ».</span><span class="sxs-lookup"><span data-stu-id="181c1-240">User that requested the remediation, in the format "domain/user".</span></span>

</dd> <dt>

<span data-ttu-id="181c1-241">**RemediationResourceCount**</span><span class="sxs-lookup"><span data-stu-id="181c1-241">**RemediationResourceCount**</span></span>
</dt> <dd>

<span data-ttu-id="181c1-242">Type : **DWORD**</span><span class="sxs-lookup"><span data-stu-id="181c1-242">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="181c1-243">Nombre de ressources dans **RemediationResourceList**.</span><span class="sxs-lookup"><span data-stu-id="181c1-243">Count of resources in **RemediationResourceList**.</span></span>

</dd> <dt>

<span data-ttu-id="181c1-244">**RemediationResourceList**</span><span class="sxs-lookup"><span data-stu-id="181c1-244">**RemediationResourceList**</span></span>
</dt> <dd>

<span data-ttu-id="181c1-245">Type : **PMPRESOURCE \_ info \[ RemediationResourceCount \]**</span><span class="sxs-lookup"><span data-stu-id="181c1-245">Type: **PMPRESOURCE\_INFO\[RemediationResourceCount\]**</span></span>

</dd> <dd>

<span data-ttu-id="181c1-246">Liste des ressources qui ont échoué lors de la mise à jour.</span><span class="sxs-lookup"><span data-stu-id="181c1-246">List of resources that failed during remediation.</span></span> <span data-ttu-id="181c1-247">Consultez [**MPRESOURCE \_ info**](mpresource-info.md).</span><span class="sxs-lookup"><span data-stu-id="181c1-247">See [**MPRESOURCE\_INFO**](mpresource-info.md).</span></span>

</dd> <dt>

<span data-ttu-id="181c1-248">**FailureResolved**</span><span class="sxs-lookup"><span data-stu-id="181c1-248">**FailureResolved**</span></span>
</dt> <dd>

<span data-ttu-id="181c1-249">Type : **bool**</span><span class="sxs-lookup"><span data-stu-id="181c1-249">Type: **BOOL**</span></span>

</dd> <dd>

<span data-ttu-id="181c1-250">True si l’échec de la correction a été résolu.</span><span class="sxs-lookup"><span data-stu-id="181c1-250">True if remediation failure been resolved.</span></span> <span data-ttu-id="181c1-251">Le compartiment est alors déplacé vers l’achèvement ou une action supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="181c1-251">This will move the bucket to either complete or an additional action.</span></span>

</dd> <dt>

<span data-ttu-id="181c1-252">**ResolvedReason**</span><span class="sxs-lookup"><span data-stu-id="181c1-252">**ResolvedReason**</span></span>
</dt> <dd>

<span data-ttu-id="181c1-253">Type : **[ **\_ raison MPRESOLVED**](mpresolved-reason.md)**</span><span class="sxs-lookup"><span data-stu-id="181c1-253">Type: **[**MPRESOLVED\_REASON**](mpresolved-reason.md)**</span></span>

</dd> <dd>

<span data-ttu-id="181c1-254">Raison de la résolution de l’échec de la correction.</span><span class="sxs-lookup"><span data-stu-id="181c1-254">Reason for remediation failure being resolved.</span></span> <span data-ttu-id="181c1-255">C’est la raison pour laquelle la détection a été déplacée de échec vers action supplémentaire ou terminée.</span><span class="sxs-lookup"><span data-stu-id="181c1-255">This is the reason the detection moved from failed to additional action or finished.</span></span> <span data-ttu-id="181c1-256">Consultez [**la \_ raison MPRESOLVED**](mpresolved-reason.md).</span><span class="sxs-lookup"><span data-stu-id="181c1-256">See [**MPRESOLVED\_REASON**](mpresolved-reason.md).</span></span>

</dd> <dt>

<span data-ttu-id="181c1-257">**AdditionalActions**</span><span class="sxs-lookup"><span data-stu-id="181c1-257">**AdditionalActions**</span></span>
</dt> <dd>

<span data-ttu-id="181c1-258">Type : **DWORD**</span><span class="sxs-lookup"><span data-stu-id="181c1-258">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="181c1-259">Actions supplémentaires requises.</span><span class="sxs-lookup"><span data-stu-id="181c1-259">Are additional actions required.</span></span>

</dd> <dt>

<span data-ttu-id="181c1-260">**ResolvedActions**</span><span class="sxs-lookup"><span data-stu-id="181c1-260">**ResolvedActions**</span></span>
</dt> <dd>

<span data-ttu-id="181c1-261">Type : **DWORD**</span><span class="sxs-lookup"><span data-stu-id="181c1-261">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="181c1-262">Toutes les actions supplémentaires qui ont été effectuées.</span><span class="sxs-lookup"><span data-stu-id="181c1-262">Any additional actions that have been performed.</span></span>

</dd> <dt>

<span data-ttu-id="181c1-263">**dwThreatStatusFlag**</span><span class="sxs-lookup"><span data-stu-id="181c1-263">**dwThreatStatusFlag**</span></span>
</dt> <dd>

<span data-ttu-id="181c1-264">Type : **DWORD**</span><span class="sxs-lookup"><span data-stu-id="181c1-264">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="181c1-265">Informations supplémentaires sur la détection des menaces.</span><span class="sxs-lookup"><span data-stu-id="181c1-265">Additonal information about the threat detection.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="181c1-266">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="181c1-266">Requirements</span></span>



| <span data-ttu-id="181c1-267">Condition requise</span><span class="sxs-lookup"><span data-stu-id="181c1-267">Requirement</span></span> | <span data-ttu-id="181c1-268">Valeur</span><span class="sxs-lookup"><span data-stu-id="181c1-268">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="181c1-269">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="181c1-269">Minimum supported client</span></span><br/> | <span data-ttu-id="181c1-270">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="181c1-270">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="181c1-271">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="181c1-271">Minimum supported server</span></span><br/> | <span data-ttu-id="181c1-272">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="181c1-272">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="181c1-273">En-tête</span><span class="sxs-lookup"><span data-stu-id="181c1-273">Header</span></span><br/>                   | <dl> <span data-ttu-id="181c1-274"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="181c1-274"><dt>MpClient.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="181c1-275">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="181c1-275">See also</span></span>

<dl> <dt>

[<span data-ttu-id="181c1-276">**MpFreeMemory**</span><span class="sxs-lookup"><span data-stu-id="181c1-276">**MpFreeMemory**</span></span>](mpfreememory.md)
</dt> <dt>

[<span data-ttu-id="181c1-277">**MpThreatEnumerate**</span><span class="sxs-lookup"><span data-stu-id="181c1-277">**MpThreatEnumerate**</span></span>](mpthreatenumerate.md)
</dt> <dt>

[<span data-ttu-id="181c1-278">**MpThreatQuery**</span><span class="sxs-lookup"><span data-stu-id="181c1-278">**MpThreatQuery**</span></span>](mpthreatquery.md)
</dt> <dt>

[<span data-ttu-id="181c1-279">**MPDETECTION \_ origine**</span><span class="sxs-lookup"><span data-stu-id="181c1-279">**MPDETECTION\_ORIGIN**</span></span>](mpdetection-origin.md)
</dt> <dt>

[<span data-ttu-id="181c1-280">**État de MPDETECTION \_**</span><span class="sxs-lookup"><span data-stu-id="181c1-280">**MPDETECTION\_STATE**</span></span>](mpdetection-state.md)
</dt> <dt>

[<span data-ttu-id="181c1-281">**État de MPEXECUTION \_**</span><span class="sxs-lookup"><span data-stu-id="181c1-281">**MPEXECUTION\_STATUS**</span></span>](mpexecution-status.md)
</dt> <dt>

[<span data-ttu-id="181c1-282">**\_raison MPRESOLVED**</span><span class="sxs-lookup"><span data-stu-id="181c1-282">**MPRESOLVED\_REASON**</span></span>](mpresolved-reason.md)
</dt> <dt>

[<span data-ttu-id="181c1-283">**\_informations MPRESOURCE**</span><span class="sxs-lookup"><span data-stu-id="181c1-283">**MPRESOURCE\_INFO**</span></span>](mpresource-info.md)
</dt> <dt>

[<span data-ttu-id="181c1-284">**MPSOURCE**</span><span class="sxs-lookup"><span data-stu-id="181c1-284">**MPSOURCE**</span></span>](mpsource.md)
</dt> <dt>

[<span data-ttu-id="181c1-285">**\_action MPTHREAT**</span><span class="sxs-lookup"><span data-stu-id="181c1-285">**MPTHREAT\_ACTION**</span></span>](mpthreat-action.md)
</dt> <dt>

[<span data-ttu-id="181c1-286">**\_catégorie MPTHREAT**</span><span class="sxs-lookup"><span data-stu-id="181c1-286">**MPTHREAT\_CATEGORY**</span></span>](mpthreat-category.md)
</dt> <dt>

[<span data-ttu-id="181c1-287">**\_détection MPTHREAT**</span><span class="sxs-lookup"><span data-stu-id="181c1-287">**MPTHREAT\_DETECTION**</span></span>](mpthreat-detection.md)
</dt> <dt>

[<span data-ttu-id="181c1-288">**comportement de MPTHREAT \_ INFOEX \_**</span><span class="sxs-lookup"><span data-stu-id="181c1-288">**MPTHREAT\_INFOEX\_BEHAVIOR**</span></span>](mpthreat-infoex-behavior.md)
</dt> <dt>

[<span data-ttu-id="181c1-289">**MPTHREAT \_ INFOEX \_ NIS**</span><span class="sxs-lookup"><span data-stu-id="181c1-289">**MPTHREAT\_INFOEX\_NIS**</span></span>](mpthreat-infoex-nis.md)
</dt> <dt>

[<span data-ttu-id="181c1-290">**MPTHREAT \_ INFOEX \_ inutilisé**</span><span class="sxs-lookup"><span data-stu-id="181c1-290">**MPTHREAT\_INFOEX\_UNUSED**</span></span>](mpthreat-infoex-unused.md)
</dt> <dt>

[<span data-ttu-id="181c1-291">**\_gravité MPTHREAT**</span><span class="sxs-lookup"><span data-stu-id="181c1-291">**MPTHREAT\_SEVERITY**</span></span>](mpthreat-severity.md)
</dt> <dt>

[<span data-ttu-id="181c1-292">**État de MPTHREAT \_**</span><span class="sxs-lookup"><span data-stu-id="181c1-292">**MPTHREAT\_STATUS**</span></span>](mpthreat-status.md)
</dt> <dt>

[<span data-ttu-id="181c1-293">**\_type MPTHREAT**</span><span class="sxs-lookup"><span data-stu-id="181c1-293">**MPTHREAT\_TYPE**</span></span>](mpthreat-type.md)
</dt> </dl>

 

 





