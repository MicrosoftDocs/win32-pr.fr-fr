---
description: La fonction ExpertIndicateStatus indique le pourcentage d’achèvement de l’analyse des experts du fichier de capture.
ms.assetid: 6dbaa6d3-6068-4a28-9d9f-bcc7a25da407
title: ExpertIndicateStatus, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExpertIndicateStatus
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: ac707a774b667b96a4d612e9eaf7da2c779c0327
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112239"
---
# <a name="expertindicatestatus-function"></a><span data-ttu-id="1d441-103">ExpertIndicateStatus fonction)</span><span class="sxs-lookup"><span data-stu-id="1d441-103">ExpertIndicateStatus function</span></span>

<span data-ttu-id="1d441-104">La fonction **ExpertIndicateStatus** indique le pourcentage d’achèvement de l’analyse du fichier de capture par l’expert.</span><span class="sxs-lookup"><span data-stu-id="1d441-104">The **ExpertIndicateStatus** function indicates the percentage of completion of the expert's analysis of the capture file.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d441-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1d441-105">Syntax</span></span>


```C++
DWORD WINAPI ExpertIndicateStatus(
  _In_  HEXPERTKEY              hExpertKey,
  _In_  EXPERTSTATUSENUMERATION Status,
  _In_  DWORD                   SubStatus,
  _In_  char                    *sztext,
  _Out_ long                    PercentDone
);
```



## <a name="parameters"></a><span data-ttu-id="1d441-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1d441-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1d441-107">*hExpertKey* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1d441-107">*hExpertKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1d441-108">Identificateur d’expert unique.</span><span class="sxs-lookup"><span data-stu-id="1d441-108">Unique expert identifier.</span></span> <span data-ttu-id="1d441-109">Moniteur réseau transmet *hExpertKey* à l’expert lorsqu’il appelle la fonction [Run](run.md) .</span><span class="sxs-lookup"><span data-stu-id="1d441-109">Network Monitor passes *hExpertKey* to the expert when it calls the [Run](run.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="1d441-110">*État* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1d441-110">*Status* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1d441-111">État actuel de l’analyse.</span><span class="sxs-lookup"><span data-stu-id="1d441-111">Current status of the analysis.</span></span> <span data-ttu-id="1d441-112">Spécifiez l’une des valeurs [EXPERTSTATUSENUMERATION](expertstatusenumeration.md) suivantes.</span><span class="sxs-lookup"><span data-stu-id="1d441-112">Specify one of the following [EXPERTSTATUSENUMERATION](expertstatusenumeration.md) values.</span></span>



| <span data-ttu-id="1d441-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="1d441-113">Value</span></span>                                                                                                                                                                                 | <span data-ttu-id="1d441-114">Signification</span><span class="sxs-lookup"><span data-stu-id="1d441-114">Meaning</span></span>                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <span id="EXPERTSTATUS_INACTIVE"></span><span id="expertstatus_inactive"></span><dl> <span data-ttu-id="1d441-115"><dt>**EXPERTSTATUS \_ inactif**</dt></span><span class="sxs-lookup"><span data-stu-id="1d441-115"><dt>**EXPERTSTATUS\_INACTIVE**</dt></span></span> </dl> | <span data-ttu-id="1d441-116">L’expert n’a jamais démarré.</span><span class="sxs-lookup"><span data-stu-id="1d441-116">The expert never started.</span></span> <br/>                                          |
| <span id="EXPERTSTATUS_STARTING"></span><span id="expertstatus_starting"></span><dl> <span data-ttu-id="1d441-117"><dt>**début de EXPERTSTATUS \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1d441-117"><dt>**EXPERTSTATUS\_STARTING**</dt></span></span> </dl> | <span data-ttu-id="1d441-118">L’expert démarre.</span><span class="sxs-lookup"><span data-stu-id="1d441-118">The expert is starting.</span></span> <br/>                                            |
| <span id="EXPERTSTATUS_RUNNING"></span><span id="expertstatus_running"></span><dl> <span data-ttu-id="1d441-119"><dt>**EXPERTSTATUS \_ en cours d’exécution**</dt></span><span class="sxs-lookup"><span data-stu-id="1d441-119"><dt>**EXPERTSTATUS\_RUNNING**</dt></span></span> </dl>    | <span data-ttu-id="1d441-120">L’expert s’exécute normalement.</span><span class="sxs-lookup"><span data-stu-id="1d441-120">The expert is running normally.</span></span> <br/>                                    |
| <span id="EXPERTSTATUS_PROBLEM"></span><span id="expertstatus_problem"></span><dl> <span data-ttu-id="1d441-121"><dt>**\_problème EXPERTSTATUS**</dt></span><span class="sxs-lookup"><span data-stu-id="1d441-121"><dt>**EXPERTSTATUS\_PROBLEM**</dt></span></span> </dl>    | <span data-ttu-id="1d441-122">Un problème spécifié dans le paramètre SubStatus A arrêté l’expert.</span><span class="sxs-lookup"><span data-stu-id="1d441-122">A problem specified in the SubStatus parameter stopped the expert.</span></span> <br/> |
| <span id="EXPERTSTATUS_ABORTED"></span><span id="expertstatus_aborted"></span><dl> <span data-ttu-id="1d441-123"><dt>**EXPERTSTATUS \_ abandonné**</dt></span><span class="sxs-lookup"><span data-stu-id="1d441-123"><dt>**EXPERTSTATUS\_ABORTED**</dt></span></span> </dl>    | <span data-ttu-id="1d441-124">Moniteur réseau arrêté l’expert.</span><span class="sxs-lookup"><span data-stu-id="1d441-124">Network Monitor stopped the expert.</span></span> <br/>                                |
| <span id="EXPERTSTATUS_DONE"></span><span id="expertstatus_done"></span><dl> <span data-ttu-id="1d441-125"><dt>**EXPERTSTATUS \_ terminé**</dt></span><span class="sxs-lookup"><span data-stu-id="1d441-125"><dt>**EXPERTSTATUS\_DONE**</dt></span></span> </dl>             | <span data-ttu-id="1d441-126">L’expert a terminé l’analyse.</span><span class="sxs-lookup"><span data-stu-id="1d441-126">The expert finished the analysis successfully.</span></span> <br/>                     |



 

</dd> <dt>

<span data-ttu-id="1d441-127">Sous- *État* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1d441-127">*SubStatus* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1d441-128">Extension ou clarification des informations fournies par le paramètre *Status* .</span><span class="sxs-lookup"><span data-stu-id="1d441-128">Extension or clarification of information provided by the *Status* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="1d441-129">*szText* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1d441-129">*sztext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1d441-130">Indicateur d’État Text facultatif.</span><span class="sxs-lookup"><span data-stu-id="1d441-130">Optional text status indicator.</span></span>

<span data-ttu-id="1d441-131">La valeur de ce paramètre peut être **null**.</span><span class="sxs-lookup"><span data-stu-id="1d441-131">This parameter value may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="1d441-132">*PercentDone* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="1d441-132">*PercentDone* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1d441-133">Pourcentage des données de capture traitées par l’expert.</span><span class="sxs-lookup"><span data-stu-id="1d441-133">Percentage of the capture data that the expert has processed.</span></span>

<span data-ttu-id="1d441-134">Lorsque l’expert termine l’analyse d’un fichier de capture, le système définit le pourcentage sur 100.</span><span class="sxs-lookup"><span data-stu-id="1d441-134">When the expert successfully completes analysis of a capture file, the system sets the percentage to 100.</span></span> <span data-ttu-id="1d441-135">Toute valeur supérieure à 99 sera ignorée.</span><span class="sxs-lookup"><span data-stu-id="1d441-135">Any number greater than 99 will be ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1d441-136">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1d441-136">Return value</span></span>

<span data-ttu-id="1d441-137">Si la fonction réussit, la valeur de retour est NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="1d441-137">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="1d441-138">Si la fonction échoue, la valeur de retour est NMERR \_ expert \_ Terminate ; l’expert doit immédiatement nettoyer et retourner sans terminer la capture.</span><span class="sxs-lookup"><span data-stu-id="1d441-138">If the function is unsuccessful, the return value is NMERR\_EXPERT\_TERMINATE; the expert must immediately clean up and return without completing the capture.</span></span>

## <a name="remarks"></a><span data-ttu-id="1d441-139">Notes</span><span class="sxs-lookup"><span data-stu-id="1d441-139">Remarks</span></span>

<span data-ttu-id="1d441-140">La fonction **ExpertIndicateStatus** peut uniquement être appelée par des experts qui implémentent la fonction [exécuter](run.md) ou [configurer](configure.md) l’exportation.</span><span class="sxs-lookup"><span data-stu-id="1d441-140">The **ExpertIndicateStatus** function can only be called by experts that implement the [Run](run.md) or [Configure](configure.md) export function.</span></span>

## <a name="requirements"></a><span data-ttu-id="1d441-141">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1d441-141">Requirements</span></span>



| <span data-ttu-id="1d441-142">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1d441-142">Requirement</span></span> | <span data-ttu-id="1d441-143">Valeur</span><span class="sxs-lookup"><span data-stu-id="1d441-143">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="1d441-144">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1d441-144">Minimum supported client</span></span><br/> | <span data-ttu-id="1d441-145">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1d441-145">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="1d441-146">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1d441-146">Minimum supported server</span></span><br/> | <span data-ttu-id="1d441-147">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1d441-147">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="1d441-148">En-tête</span><span class="sxs-lookup"><span data-stu-id="1d441-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="1d441-149"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="1d441-149"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="1d441-150">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="1d441-150">Library</span></span><br/>                  | <dl> <span data-ttu-id="1d441-151"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1d441-151"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="1d441-152">DLL</span><span class="sxs-lookup"><span data-stu-id="1d441-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1d441-153"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1d441-153"><dt>Nmapi.dll</dt></span></span> </dl> |
