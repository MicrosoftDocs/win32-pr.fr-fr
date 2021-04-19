---
title: Énumération MPSTATUS_FLAG (MpClient. h)
description: Indicateurs de bits d’état de produit globaux possibles.
ms.assetid: BF2E6506-E76A-4785-8E91-99937B413548
keywords:
- MPSTATUS_FLAG énumération des fonctionnalités d’environnement Windows héritées
- PMPSTATUS_FLAG des fonctionnalités d’environnement Windows héritées d’un pointeur d’énumération
topic_type:
- apiref
api_name:
- MPSTATUS_FLAG
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c7175980c09c63938be04626091c31b53335756
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509100"
---
# <a name="mpstatus_flag-enumeration"></a><span data-ttu-id="db69b-105">\_Énumération de l’indicateur MPSTATUS</span><span class="sxs-lookup"><span data-stu-id="db69b-105">MPSTATUS\_FLAG enumeration</span></span>

<span data-ttu-id="db69b-106">Indicateurs de bits d’état de produit globaux possibles.</span><span class="sxs-lookup"><span data-stu-id="db69b-106">Possible overall product status bit flags.</span></span>

## <a name="syntax"></a><span data-ttu-id="db69b-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="db69b-107">Syntax</span></span>


```C++
typedef enum tagMPSTATUS_FLAG { 
  MP_STATUS_FLAG_NONE                           = 0,
  MP_STATUS_FLAG_SERVICE_UNAVAILABLE            = 1 << 0,
  MP_STATUS_FLAG_MPENGINE_UNAVAILABLE           = 1 << 1,
  MP_STATUS_FLAG_THREAT_FULLSCAN_REQUIRED       = 1 << 2,
  MP_STATUS_FLAG_THREAT_REBOOT_REQUIRED         = 1 << 3,
  MP_STATUS_FLAG_THREAT_MANUAL_STEPS_REQUIRED   = 1 << 4,
  MP_STATUS_FLAG_DUE_AV_SIGNATURE               = 1 << 5,
  MP_STATUS_FLAG_DUE_AS_SIGNATURE               = 1 << 6,
  MP_STATUS_FLAG_DUE_QUICK_SCAN                 = 1 << 7,
  MP_STATUS_FLAG_DUE_FULL_SCAN                  = 1 << 8,
  MP_STATUS_FLAG_INPROGRESS_SYSTEM_SCAN         = 1 << 9,
  MP_STATUS_FLAG_INPROGRESS_ROUTINE_CLEANING    = 1 << 10,
  MP_STATUS_FLAG_DUE_SAMPLES                    = 1 << 11,
  MP_STATUS_FLAG_EVALUATION_MODE                = 1 << 12,
  MP_STATUS_FLAG_NONGENUINE                     = 1 << 13,
  MP_STATUS_FLAG_PRODUCT_EXPIRED                = 1 << 14,
  MP_STATUS_FLAG_THREAT_CALLISTO_REQUIRED       = 1 << 15,
  MP_STATUS_FLAG_SERVICE_ON_SYSTEM_SHUTDOWN     = 1 << 16,
  MP_STATUS_FLAG_SERVICE_CRITICAL_FAILURE       = 1 << 17,
  MP_STATUS_FLAG_SERVICE_NON_CRITICAL_FAILURE   = 1 << 18,
  MP_STATUS_FLAG_HEALTH_INITIALIZED             = 1 << 19,
  MP_STATUS_FLAG_DUE_PLATFORM_UPDATE            = 1 << 20,
  MP_STATUS_FLAG_INPROGRESS_PLATFORM_UPDATE     = 1 << 21,
  MP_STATUS_FLAG_PLATFORM_ABOUT_TO_BE_OUTDATED  = 1 << 22,
  MP_STATUS_FLAG_END_OF_LIFE                    = 1 << 23,
  MP_STATUS_FLAG_MAX                            = 1 << 23,
  MP_STATUS_FLAG_ALL                            = (1 << 24)-1
} MPSTATUS_FLAG, *PMPSTATUS_FLAG;
```



## <a name="constants"></a><span data-ttu-id="db69b-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="db69b-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="db69b-109"><span id="MP_STATUS_FLAG_NONE"></span><span id="mp_status_flag_none"></span>**indicateur d’état de Pack d' \_ état \_ \_ aucun**</span><span class="sxs-lookup"><span data-stu-id="db69b-109"><span id="MP_STATUS_FLAG_NONE"></span><span id="mp_status_flag_none"></span>**MP\_STATUS\_FLAG\_NONE**</span></span>
</dt> <dd>

<span data-ttu-id="db69b-110">Aucun indicateur d’état défini (État non initialisé).</span><span class="sxs-lookup"><span data-stu-id="db69b-110">No status flags set (non-initialized state).</span></span>

</dd> <dt>

<span data-ttu-id="db69b-111"><span id="MP_STATUS_FLAG_SERVICE_UNAVAILABLE"></span><span id="mp_status_flag_service_unavailable"></span>**SERVICE d’indicateur d’État du pack d’accès \_ \_ \_ \_ non disponible**</span><span class="sxs-lookup"><span data-stu-id="db69b-111"><span id="MP_STATUS_FLAG_SERVICE_UNAVAILABLE"></span><span id="mp_status_flag_service_unavailable"></span>**MP\_STATUS\_FLAG\_SERVICE\_UNAVAILABLE**</span></span>
</dt> <dd>

<span data-ttu-id="db69b-112">Le service n’est pas en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="db69b-112">Service not running.</span></span>

</dd> <dt>

<span data-ttu-id="db69b-113"><span id="MP_STATUS_FLAG_MPENGINE_UNAVAILABLE"></span><span id="mp_status_flag_mpengine_unavailable"></span>**indicateur d’État du pack d' \_ \_ \_ MPENGINE \_ non disponible**</span><span class="sxs-lookup"><span data-stu-id="db69b-113"><span id="MP_STATUS_FLAG_MPENGINE_UNAVAILABLE"></span><span id="mp_status_flag_mpengine_unavailable"></span>**MP\_STATUS\_FLAG\_MPENGINE\_UNAVAILABLE**</span></span>
</dt> <dd>

<span data-ttu-id="db69b-114">Service démarré sans moteur de protection contre les programmes malveillants.</span><span class="sxs-lookup"><span data-stu-id="db69b-114">Service started without any malware protection engine.</span></span>

</dd> <dt>

<span data-ttu-id="db69b-115"><span id="MP_STATUS_FLAG_THREAT_FULLSCAN_REQUIRED"></span><span id="mp_status_flag_threat_fullscan_required"></span>**indicateur d’État du point de gestion- \_ \_ FULLSCAN des \_ menaces \_ \_ requis**</span><span class="sxs-lookup"><span data-stu-id="db69b-115"><span id="MP_STATUS_FLAG_THREAT_FULLSCAN_REQUIRED"></span><span id="mp_status_flag_threat_fullscan_required"></span>**MP\_STATUS\_FLAG\_THREAT\_FULLSCAN\_REQUIRED**</span></span>
</dt> <dd>

<span data-ttu-id="db69b-116">Analyse complète en attente en raison d’une menace.</span><span class="sxs-lookup"><span data-stu-id="db69b-116">Pending full scan due to threat action.</span></span>

</dd> <dt>

<span data-ttu-id="db69b-117"><span id="MP_STATUS_FLAG_THREAT_REBOOT_REQUIRED"></span><span id="mp_status_flag_threat_reboot_required"></span>**indicateur d’État du pack d' \_ état- \_ \_ \_ redémarrage des menaces \_ requis**</span><span class="sxs-lookup"><span data-stu-id="db69b-117"><span id="MP_STATUS_FLAG_THREAT_REBOOT_REQUIRED"></span><span id="mp_status_flag_threat_reboot_required"></span>**MP\_STATUS\_FLAG\_THREAT\_REBOOT\_REQUIRED**</span></span>
</dt> <dd>

<span data-ttu-id="db69b-118">Redémarrage en attente en raison d’une menace.</span><span class="sxs-lookup"><span data-stu-id="db69b-118">Pending reboot due to threat action.</span></span>

</dd> <dt>

<span data-ttu-id="db69b-119"><span id="MP_STATUS_FLAG_THREAT_MANUAL_STEPS_REQUIRED"></span><span id="mp_status_flag_threat_manual_steps_required"></span>**indicateur d’État du pack d' \_ état \_ \_ \_ étapes manuelles des menaces \_ \_ requises**</span><span class="sxs-lookup"><span data-stu-id="db69b-119"><span id="MP_STATUS_FLAG_THREAT_MANUAL_STEPS_REQUIRED"></span><span id="mp_status_flag_threat_manual_steps_required"></span>**MP\_STATUS\_FLAG\_THREAT\_MANUAL\_STEPS\_REQUIRED**</span></span>
</dt> <dd>

<span data-ttu-id="db69b-120">Étapes manuelles en attente en raison de l’action de la menace.</span><span class="sxs-lookup"><span data-stu-id="db69b-120">Pending manual steps due to threat action.</span></span>

</dd> <dt>

<span data-ttu-id="db69b-121"><span id="MP_STATUS_FLAG_DUE_AV_SIGNATURE"></span><span id="mp_status_flag_due_av_signature"></span>**indicateur d’État du point de gestion, \_ \_ \_ \_ signature AV due \_**</span><span class="sxs-lookup"><span data-stu-id="db69b-121"><span id="MP_STATUS_FLAG_DUE_AV_SIGNATURE"></span><span id="mp_status_flag_due_av_signature"></span>**MP\_STATUS\_FLAG\_DUE\_AV\_SIGNATURE**</span></span>
</dt> <dd>

<span data-ttu-id="db69b-122">Signatures antivirus obsolètes.</span><span class="sxs-lookup"><span data-stu-id="db69b-122">Antivirus signatures out of date.</span></span>

</dd> <dt>

<span data-ttu-id="db69b-123"><span id="MP_STATUS_FLAG_DUE_AS_SIGNATURE"></span><span id="mp_status_flag_due_as_signature"></span>**indicateur d’État du pack d' \_ \_ \_ attente en raison \_ de la \_ signature**</span><span class="sxs-lookup"><span data-stu-id="db69b-123"><span id="MP_STATUS_FLAG_DUE_AS_SIGNATURE"></span><span id="mp_status_flag_due_as_signature"></span>**MP\_STATUS\_FLAG\_DUE\_AS\_SIGNATURE**</span></span>
</dt> <dd>

<span data-ttu-id="db69b-124">Signatures anti-espion obsolètes.</span><span class="sxs-lookup"><span data-stu-id="db69b-124">Antispyware signatures out of date.</span></span>

</dd> <dt>

<span data-ttu-id="db69b-125"><span id="MP_STATUS_FLAG_DUE_QUICK_SCAN"></span><span id="mp_status_flag_due_quick_scan"></span>**indicateur d’État du pack d' \_ \_ \_ analyse en raison d’une \_ \_ analyse rapide**</span><span class="sxs-lookup"><span data-stu-id="db69b-125"><span id="MP_STATUS_FLAG_DUE_QUICK_SCAN"></span><span id="mp_status_flag_due_quick_scan"></span>**MP\_STATUS\_FLAG\_DUE\_QUICK\_SCAN**</span></span>
</dt> <dd>

<span data-ttu-id="db69b-126">Aucune analyse rapide ne s’est produite pendant une période spécifiée.</span><span class="sxs-lookup"><span data-stu-id="db69b-126">No quick scan has happened for a specified period.</span></span>

</dd> <dt>

<span data-ttu-id="db69b-127"><span id="MP_STATUS_FLAG_DUE_FULL_SCAN"></span><span id="mp_status_flag_due_full_scan"></span>**indicateur d’État du pack d' \_ \_ \_ analyse en raison d' \_ une \_ analyse complète**</span><span class="sxs-lookup"><span data-stu-id="db69b-127"><span id="MP_STATUS_FLAG_DUE_FULL_SCAN"></span><span id="mp_status_flag_due_full_scan"></span>**MP\_STATUS\_FLAG\_DUE\_FULL\_SCAN**</span></span>
</dt> <dd>

<span data-ttu-id="db69b-128">aucune analyse complète n’a eu lieu pendant une période spécifiée</span><span class="sxs-lookup"><span data-stu-id="db69b-128">no full scan has happened for a specified period</span></span>

</dd> <dt>

<span data-ttu-id="db69b-129"><span id="MP_STATUS_FLAG_INPROGRESS_SYSTEM_SCAN"></span><span id="mp_status_flag_inprogress_system_scan"></span>**analyse du système en cours d’indicateur d’État du pack d' \_ \_ \_ \_ \_ analyse**</span><span class="sxs-lookup"><span data-stu-id="db69b-129"><span id="MP_STATUS_FLAG_INPROGRESS_SYSTEM_SCAN"></span><span id="mp_status_flag_inprogress_system_scan"></span>**MP\_STATUS\_FLAG\_INPROGRESS\_SYSTEM\_SCAN**</span></span>
</dt> <dd>

<span data-ttu-id="db69b-130">Analyse initiée par le système en cours.</span><span class="sxs-lookup"><span data-stu-id="db69b-130">System-initiated scan in progress.</span></span>

</dd> <dt>

<span data-ttu-id="db69b-131"><span id="MP_STATUS_FLAG_INPROGRESS_ROUTINE_CLEANING"></span><span id="mp_status_flag_inprogress_routine_cleaning"></span>**nettoyage de la routine de l’indicateur d’État du pack d' \_ état \_ \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="db69b-131"><span id="MP_STATUS_FLAG_INPROGRESS_ROUTINE_CLEANING"></span><span id="mp_status_flag_inprogress_routine_cleaning"></span>**MP\_STATUS\_FLAG\_INPROGRESS\_ROUTINE\_CLEANING**</span></span>
</dt> <dd>

<span data-ttu-id="db69b-132">Nettoyage initié par le système en cours.</span><span class="sxs-lookup"><span data-stu-id="db69b-132">System-initiated clean in progress.</span></span>

</dd> <dt>

<span data-ttu-id="db69b-133"><span id="MP_STATUS_FLAG_DUE_SAMPLES"></span><span id="mp_status_flag_due_samples"></span>**exemples d’état de Pack d' \_ \_ \_ attente \_**</span><span class="sxs-lookup"><span data-stu-id="db69b-133"><span id="MP_STATUS_FLAG_DUE_SAMPLES"></span><span id="mp_status_flag_due_samples"></span>**MP\_STATUS\_FLAG\_DUE\_SAMPLES**</span></span>
</dt> <dd>

<span data-ttu-id="db69b-134">Des exemples sont en attente d’envoi.</span><span class="sxs-lookup"><span data-stu-id="db69b-134">There are samples pending submission.</span></span>

</dd> <dt>

<span data-ttu-id="db69b-135"><span id="MP_STATUS_FLAG_EVALUATION_MODE"></span><span id="mp_status_flag_evaluation_mode"></span>**MODE d’évaluation de l' \_ indicateur d’État MP \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="db69b-135"><span id="MP_STATUS_FLAG_EVALUATION_MODE"></span><span id="mp_status_flag_evaluation_mode"></span>**MP\_STATUS\_FLAG\_EVALUATION\_MODE**</span></span>
</dt> <dd>

<span data-ttu-id="db69b-136">Le produit est en cours d’exécution en mode évaluation.</span><span class="sxs-lookup"><span data-stu-id="db69b-136">Product is running in evaluation mode.</span></span>

</dd> <dt>

<span data-ttu-id="db69b-137"><span id="MP_STATUS_FLAG_NONGENUINE"></span><span id="mp_status_flag_nongenuine"></span>**indicateur d’état de point de gestion pas \_ \_ \_ authentique**</span><span class="sxs-lookup"><span data-stu-id="db69b-137"><span id="MP_STATUS_FLAG_NONGENUINE"></span><span id="mp_status_flag_nongenuine"></span>**MP\_STATUS\_FLAG\_NONGENUINE**</span></span>
</dt> <dd>

<span data-ttu-id="db69b-138">Le produit est en cours d’exécution en mode Windows non authentique.</span><span class="sxs-lookup"><span data-stu-id="db69b-138">Product is running in non-genuine Windows mode.</span></span>

</dd> <dt>

<span data-ttu-id="db69b-139"><span id="MP_STATUS_FLAG_PRODUCT_EXPIRED"></span><span id="mp_status_flag_product_expired"></span>**indicateur d’État du pack d' \_ État du \_ \_ produit \_ expiré**</span><span class="sxs-lookup"><span data-stu-id="db69b-139"><span id="MP_STATUS_FLAG_PRODUCT_EXPIRED"></span><span id="mp_status_flag_product_expired"></span>**MP\_STATUS\_FLAG\_PRODUCT\_EXPIRED**</span></span>
</dt> <dd>

<span data-ttu-id="db69b-140">Le produit a expiré.</span><span class="sxs-lookup"><span data-stu-id="db69b-140">Product expired.</span></span>

</dd> <dt>

<span data-ttu-id="db69b-141"><span id="MP_STATUS_FLAG_THREAT_CALLISTO_REQUIRED"></span><span id="mp_status_flag_threat_callisto_required"></span>**\_indicateur d’État MP \_ \_ Threat \_ Callisto \_ requis**</span><span class="sxs-lookup"><span data-stu-id="db69b-141"><span id="MP_STATUS_FLAG_THREAT_CALLISTO_REQUIRED"></span><span id="mp_status_flag_threat_callisto_required"></span>**MP\_STATUS\_FLAG\_THREAT\_CALLISTO\_REQUIRED**</span></span>
</dt> <dd>

<span data-ttu-id="db69b-142">Analyse hors ligne Callisto requise.</span><span class="sxs-lookup"><span data-stu-id="db69b-142">Callisto off-line scan required.</span></span>

</dd> <dt>

<span data-ttu-id="db69b-143"><span id="MP_STATUS_FLAG_SERVICE_ON_SYSTEM_SHUTDOWN"></span><span id="mp_status_flag_service_on_system_shutdown"></span>**\_ \_ \_ service \_ d’indicateur d’État du point de gestion à l' \_ arrêt du système \_**</span><span class="sxs-lookup"><span data-stu-id="db69b-143"><span id="MP_STATUS_FLAG_SERVICE_ON_SYSTEM_SHUTDOWN"></span><span id="mp_status_flag_service_on_system_shutdown"></span>**MP\_STATUS\_FLAG\_SERVICE\_ON\_SYSTEM\_SHUTDOWN**</span></span>
</dt> <dd>

<span data-ttu-id="db69b-144">Le service s’arrête dans le cadre de l’arrêt du système.</span><span class="sxs-lookup"><span data-stu-id="db69b-144">Service is shutting down as part of system shutdown.</span></span>

</dd> <dt>

<span data-ttu-id="db69b-145"><span id="MP_STATUS_FLAG_SERVICE_CRITICAL_FAILURE"></span><span id="mp_status_flag_service_critical_failure"></span>**\_ \_ \_ défaillance critique du service d’indicateur \_ d’État du pack d’accès \_**</span><span class="sxs-lookup"><span data-stu-id="db69b-145"><span id="MP_STATUS_FLAG_SERVICE_CRITICAL_FAILURE"></span><span id="mp_status_flag_service_critical_failure"></span>**MP\_STATUS\_FLAG\_SERVICE\_CRITICAL\_FAILURE**</span></span>
</dt> <dd>

<span data-ttu-id="db69b-146">Échec critique de la correction des menaces.</span><span class="sxs-lookup"><span data-stu-id="db69b-146">Threat remediation failed critically.</span></span>

</dd> <dt>

<span data-ttu-id="db69b-147"><span id="MP_STATUS_FLAG_SERVICE_NON_CRITICAL_FAILURE"></span><span id="mp_status_flag_service_non_critical_failure"></span>**\_ \_ \_ \_ \_ défaillance non critique du service d’indicateur d’état \_ du point de gestion**</span><span class="sxs-lookup"><span data-stu-id="db69b-147"><span id="MP_STATUS_FLAG_SERVICE_NON_CRITICAL_FAILURE"></span><span id="mp_status_flag_service_non_critical_failure"></span>**MP\_STATUS\_FLAG\_SERVICE\_NON\_CRITICAL\_FAILURE**</span></span>
</dt> <dd>

<span data-ttu-id="db69b-148">Échec de la correction de la menace non critique.</span><span class="sxs-lookup"><span data-stu-id="db69b-148">Threat remediation failed non-critically.</span></span>

</dd> <dt>

<span data-ttu-id="db69b-149"><span id="MP_STATUS_FLAG_HEALTH_INITIALIZED"></span><span id="mp_status_flag_health_initialized"></span>**\_intégrité de \_ l’indicateur d’État du point de gestion \_ \_ initialisée**</span><span class="sxs-lookup"><span data-stu-id="db69b-149"><span id="MP_STATUS_FLAG_HEALTH_INITIALIZED"></span><span id="mp_status_flag_health_initialized"></span>**MP\_STATUS\_FLAG\_HEALTH\_INITIALIZED**</span></span>
</dt> <dd>

<span data-ttu-id="db69b-150">Aucun indicateur d’état défini (état bien initialisé).</span><span class="sxs-lookup"><span data-stu-id="db69b-150">No status flags set (well-initialized state).</span></span>

</dd> <dt>

<span data-ttu-id="db69b-151"><span id="MP_STATUS_FLAG_DUE_PLATFORM_UPDATE"></span><span id="mp_status_flag_due_platform_update"></span>**\_indicateur d’État MP en raison de la \_ \_ \_ \_ mise à jour de la plateforme**</span><span class="sxs-lookup"><span data-stu-id="db69b-151"><span id="MP_STATUS_FLAG_DUE_PLATFORM_UPDATE"></span><span id="mp_status_flag_due_platform_update"></span>**MP\_STATUS\_FLAG\_DUE\_PLATFORM\_UPDATE**</span></span>
</dt> <dd>

<span data-ttu-id="db69b-152">La plateforme est obsolète.</span><span class="sxs-lookup"><span data-stu-id="db69b-152">The platform is out of date.</span></span>

</dd> <dt>

<span data-ttu-id="db69b-153"><span id="MP_STATUS_FLAG_INPROGRESS_PLATFORM_UPDATE"></span><span id="mp_status_flag_inprogress_platform_update"></span>**\_ \_ \_ \_ \_ mise à jour de la plateforme en cours d’indicateur d’État MP**</span><span class="sxs-lookup"><span data-stu-id="db69b-153"><span id="MP_STATUS_FLAG_INPROGRESS_PLATFORM_UPDATE"></span><span id="mp_status_flag_inprogress_platform_update"></span>**MP\_STATUS\_FLAG\_INPROGRESS\_PLATFORM\_UPDATE**</span></span>
</dt> <dd>

<span data-ttu-id="db69b-154">Mise à jour de la plateforme en cours.</span><span class="sxs-lookup"><span data-stu-id="db69b-154">Platform update is in progress.</span></span>

</dd> <dt>

<span data-ttu-id="db69b-155"><span id="MP_STATUS_FLAG_PLATFORM_ABOUT_TO_BE_OUTDATED"></span><span id="mp_status_flag_platform_about_to_be_outdated"></span>**\_ \_ plateforme d’indicateur d’État MP sur le point \_ \_ \_ d' \_ être \_ obsolète**</span><span class="sxs-lookup"><span data-stu-id="db69b-155"><span id="MP_STATUS_FLAG_PLATFORM_ABOUT_TO_BE_OUTDATED"></span><span id="mp_status_flag_platform_about_to_be_outdated"></span>**MP\_STATUS\_FLAG\_PLATFORM\_ABOUT\_TO\_BE\_OUTDATED**</span></span>
</dt> <dd>

<span data-ttu-id="db69b-156">La plateforme est sur le paragraphe obsolète</span><span class="sxs-lookup"><span data-stu-id="db69b-156">The platform is about to be outdated</span></span>

</dd> <dt>

<span data-ttu-id="db69b-157"><span id="MP_STATUS_FLAG_END_OF_LIFE"></span><span id="mp_status_flag_end_of_life"></span>**\_ \_ \_ fin \_ de vie de l’indicateur d’État MP \_**</span><span class="sxs-lookup"><span data-stu-id="db69b-157"><span id="MP_STATUS_FLAG_END_OF_LIFE"></span><span id="mp_status_flag_end_of_life"></span>**MP\_STATUS\_FLAG\_END\_OF\_LIFE**</span></span>
</dt> <dd>

<span data-ttu-id="db69b-158">La fin de la signature ou de la plateforme est passée ou en attente.</span><span class="sxs-lookup"><span data-stu-id="db69b-158">The signature or platform end of life is past or is pending.</span></span>

</dd> <dt>

<span data-ttu-id="db69b-159"><span id="MP_STATUS_FLAG_MAX"></span><span id="mp_status_flag_max"></span>**\_indicateur d’État MP \_ \_ Max.**</span><span class="sxs-lookup"><span data-stu-id="db69b-159"><span id="MP_STATUS_FLAG_MAX"></span><span id="mp_status_flag_max"></span>**MP\_STATUS\_FLAG\_MAX**</span></span>
</dt> <dd>

<span data-ttu-id="db69b-160">Indicateur de nombre maximal valide.</span><span class="sxs-lookup"><span data-stu-id="db69b-160">Maximum valid flag.</span></span>

</dd> <dt>

<span data-ttu-id="db69b-161"><span id="MP_STATUS_FLAG_ALL"></span><span id="mp_status_flag_all"></span>**\_indicateur d’État du point de gestion \_ \_**</span><span class="sxs-lookup"><span data-stu-id="db69b-161"><span id="MP_STATUS_FLAG_ALL"></span><span id="mp_status_flag_all"></span>**MP\_STATUS\_FLAG\_ALL**</span></span>
</dt> <dd>

<span data-ttu-id="db69b-162">Valeur maximale possible.</span><span class="sxs-lookup"><span data-stu-id="db69b-162">Maximum value possible.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="db69b-163">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="db69b-163">Requirements</span></span>



| <span data-ttu-id="db69b-164">Condition requise</span><span class="sxs-lookup"><span data-stu-id="db69b-164">Requirement</span></span> | <span data-ttu-id="db69b-165">Valeur</span><span class="sxs-lookup"><span data-stu-id="db69b-165">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="db69b-166">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="db69b-166">Minimum supported client</span></span><br/> | <span data-ttu-id="db69b-167">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="db69b-167">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="db69b-168">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="db69b-168">Minimum supported server</span></span><br/> | <span data-ttu-id="db69b-169">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="db69b-169">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="db69b-170">En-tête</span><span class="sxs-lookup"><span data-stu-id="db69b-170">Header</span></span><br/>                   | <dl> <span data-ttu-id="db69b-171"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="db69b-171"><dt>MpClient.h</dt></span></span> </dl> |



 

 





