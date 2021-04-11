---
title: Constantes d’État du travail d’impression ADSI (Adssts. h)
description: Les constantes suivantes sont utilisées avec la propriété IADsPrintJobOperations. Status pour indiquer l’état d’un travail d’impression.
ms.assetid: 44a981cc-1098-4b6d-8332-e678953c9112
ms.tgt_platform: multiple
topic_type:
- apiref
api_name:
- ADS_JOB_PAUSED
- ADS_JOB_ERROR
- ADS_JOB_DELETING
- ADS_JOB_SPOOLING
- ADS_JOB_PRINTING
- ADS_JOB_OFFLINE
- ADS_JOB_PAPEROUT
- ADS_JOB_PRINTED
- ADS_JOB_DELETED
api_location:
- Adssts.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c51e83393aa0322ef142ee45b4a893f980293ded
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942574"
---
# <a name="adsi-print-job-status-constants"></a><span data-ttu-id="01a1e-103">Constantes d’État du travail d’impression ADSI</span><span class="sxs-lookup"><span data-stu-id="01a1e-103">ADSI Print Job Status Constants</span></span>

<span data-ttu-id="01a1e-104">Les constantes suivantes sont utilisées avec la propriété [**IADsPrintJobOperations. Status**](iadsprintjoboperations-property-methods.md) pour indiquer l’état d’un travail d’impression.</span><span class="sxs-lookup"><span data-stu-id="01a1e-104">The following constants are used with the [**IADsPrintJobOperations.Status**](iadsprintjoboperations-property-methods.md) property to indicate the status of a print job.</span></span>

<dl> <dt>

<span data-ttu-id="01a1e-105"><span id="ADS_JOB_PAUSED"></span><span id="ads_job_paused"></span>**\_travail ADS \_ suspendu**</span><span class="sxs-lookup"><span data-stu-id="01a1e-105"><span id="ADS_JOB_PAUSED"></span><span id="ads_job_paused"></span>**ADS\_JOB\_PAUSED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01a1e-106">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="01a1e-106">1 (0x1)</span></span>
</dt> <dt>



<span data-ttu-id="01a1e-107">Le travail d'impression est suspendu.</span><span class="sxs-lookup"><span data-stu-id="01a1e-107">The print job is paused.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="01a1e-108"><span id="ADS_JOB_ERROR"></span><span id="ads_job_error"></span>**\_erreur de tâche ADS \_**</span><span class="sxs-lookup"><span data-stu-id="01a1e-108"><span id="ADS_JOB_ERROR"></span><span id="ads_job_error"></span>**ADS\_JOB\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01a1e-109">2 (0X2)</span><span class="sxs-lookup"><span data-stu-id="01a1e-109">2 (0x2)</span></span>
</dt> <dt>



<span data-ttu-id="01a1e-110">Une erreur est survenue.</span><span class="sxs-lookup"><span data-stu-id="01a1e-110">An error occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="01a1e-111"><span id="ADS_JOB_DELETING"></span><span id="ads_job_deleting"></span>**suppression d’un \_ travail ADS \_**</span><span class="sxs-lookup"><span data-stu-id="01a1e-111"><span id="ADS_JOB_DELETING"></span><span id="ads_job_deleting"></span>**ADS\_JOB\_DELETING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01a1e-112">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="01a1e-112">4 (0x4)</span></span>
</dt> <dt>



<span data-ttu-id="01a1e-113">Le travail d’impression est en cours de suppression.</span><span class="sxs-lookup"><span data-stu-id="01a1e-113">The print job is being deleted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="01a1e-114"><span id="ADS_JOB_SPOOLING"></span><span id="ads_job_spooling"></span>**mise en file d’attente des \_ travaux ADS \_**</span><span class="sxs-lookup"><span data-stu-id="01a1e-114"><span id="ADS_JOB_SPOOLING"></span><span id="ads_job_spooling"></span>**ADS\_JOB\_SPOOLING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01a1e-115">8 (0x8)</span><span class="sxs-lookup"><span data-stu-id="01a1e-115">8 (0x8)</span></span>
</dt> <dt>



<span data-ttu-id="01a1e-116">Le travail d’impression est mis en attente.</span><span class="sxs-lookup"><span data-stu-id="01a1e-116">The print job is being spooled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="01a1e-117"><span id="ADS_JOB_PRINTING"></span><span id="ads_job_printing"></span>**\_impression des travaux ADS \_**</span><span class="sxs-lookup"><span data-stu-id="01a1e-117"><span id="ADS_JOB_PRINTING"></span><span id="ads_job_printing"></span>**ADS\_JOB\_PRINTING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01a1e-118">16 (0x10)</span><span class="sxs-lookup"><span data-stu-id="01a1e-118">16 (0x10)</span></span>
</dt> <dt>



<span data-ttu-id="01a1e-119">Le travail d’impression est en cours d’impression.</span><span class="sxs-lookup"><span data-stu-id="01a1e-119">The print job is being printed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="01a1e-120"><span id="ADS_JOB_OFFLINE"></span><span id="ads_job_offline"></span>**\_travail ADS \_ hors connexion**</span><span class="sxs-lookup"><span data-stu-id="01a1e-120"><span id="ADS_JOB_OFFLINE"></span><span id="ads_job_offline"></span>**ADS\_JOB\_OFFLINE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01a1e-121">32 (0x20)</span><span class="sxs-lookup"><span data-stu-id="01a1e-121">32 (0x20)</span></span>
</dt> <dt>



<span data-ttu-id="01a1e-122">L'imprimante est hors connexion.</span><span class="sxs-lookup"><span data-stu-id="01a1e-122">The printer is offline.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="01a1e-123"><span id="ADS_JOB_PAPEROUT"></span><span id="ads_job_paperout"></span>**\_PAPEROUT de travail ADS \_**</span><span class="sxs-lookup"><span data-stu-id="01a1e-123"><span id="ADS_JOB_PAPEROUT"></span><span id="ads_job_paperout"></span>**ADS\_JOB\_PAPEROUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01a1e-124">64 (0x40)</span><span class="sxs-lookup"><span data-stu-id="01a1e-124">64 (0x40)</span></span>
</dt> <dt>



<span data-ttu-id="01a1e-125">L’imprimante n’est plus imprimée.</span><span class="sxs-lookup"><span data-stu-id="01a1e-125">The printer is out of paper.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="01a1e-126"><span id="ADS_JOB_PRINTED"></span><span id="ads_job_printed"></span>**\_travail ADS \_ imprimé**</span><span class="sxs-lookup"><span data-stu-id="01a1e-126"><span id="ADS_JOB_PRINTED"></span><span id="ads_job_printed"></span>**ADS\_JOB\_PRINTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01a1e-127">128 (0x80)</span><span class="sxs-lookup"><span data-stu-id="01a1e-127">128 (0x80)</span></span>
</dt> <dt>



<span data-ttu-id="01a1e-128">Le travail d’impression a été imprimé.</span><span class="sxs-lookup"><span data-stu-id="01a1e-128">The print job has been printed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="01a1e-129"><span id="ADS_JOB_DELETED"></span><span id="ads_job_deleted"></span>**\_travail ADS \_ supprimé**</span><span class="sxs-lookup"><span data-stu-id="01a1e-129"><span id="ADS_JOB_DELETED"></span><span id="ads_job_deleted"></span>**ADS\_JOB\_DELETED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01a1e-130">256 (0x100)</span><span class="sxs-lookup"><span data-stu-id="01a1e-130">256 (0x100)</span></span>
</dt> <dt>



<span data-ttu-id="01a1e-131">Le travail d’impression a été supprimé.</span><span class="sxs-lookup"><span data-stu-id="01a1e-131">The print job has been deleted.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="01a1e-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="01a1e-132">Requirements</span></span>



| <span data-ttu-id="01a1e-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="01a1e-133">Requirement</span></span> | <span data-ttu-id="01a1e-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="01a1e-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="01a1e-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="01a1e-135">Minimum supported client</span></span><br/> | <span data-ttu-id="01a1e-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="01a1e-136">Windows Vista</span></span><br/>                                                            |
| <span data-ttu-id="01a1e-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="01a1e-137">Minimum supported server</span></span><br/> | <span data-ttu-id="01a1e-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="01a1e-138">Windows Server 2008</span></span><br/>                                                      |
| <span data-ttu-id="01a1e-139">En-tête</span><span class="sxs-lookup"><span data-stu-id="01a1e-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="01a1e-140"><dt>Adssts. h</dt></span><span class="sxs-lookup"><span data-stu-id="01a1e-140"><dt>Adssts.h</dt></span></span> </dl> |



 

 





