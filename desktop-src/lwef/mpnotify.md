---
title: Énumération MPNOTIFY (MpClient. h)
description: Notifications de rappel possibles.
ms.assetid: CCD0CD89-2C6E-453F-9437-E6ED87AD9F29
keywords:
- MPNOTIFY, énumération des fonctionnalités d’environnement Windows héritées
- Pointeur d’énumération PMPNOTIFY fonctionnalités d’environnement Windows héritées
topic_type:
- apiref
api_name:
- MPNOTIFY
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: afa0eeb6cb1d610f28cc82f578617f7bd71cf886
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511375"
---
# <a name="mpnotify-enumeration"></a><span data-ttu-id="3e239-105">Énumération MPNOTIFY</span><span class="sxs-lookup"><span data-stu-id="3e239-105">MPNOTIFY enumeration</span></span>

<span data-ttu-id="3e239-106">Notifications de rappel possibles.</span><span class="sxs-lookup"><span data-stu-id="3e239-106">Possible callback notifications.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e239-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3e239-107">Syntax</span></span>


```C++
typedef enum tagMPNOTIFY { 
  MPNOTIFY_NONE,
  MPNOTIFY_CALL_START,
  MPNOTIFY_CALL_COMPLETE,
  MPNOTIFY_INTERNAL_FAILURE,
  MPNOTIFY_STATUS_SERVICE_START,
  MPNOTIFY_STATUS_SERVICE_RUNNING,
  MPNOTIFY_STATUS_SERVICE_STOP,
  MPNOTIFY_STATUS_COMPONENT,
  MPNOTIFY_STATUS_CHANGE,
  MPNOTIFY_STATUS_COMPONENT_CONFIGURATION,
  MPNOTIFY_STATUS_EXPIRATION_CHANGE,
  MPNOTIFY_STATUS_OFFLINE_SCAN_CHANGE,
  MPNOTIFY_SCAN_START,
  MPNOTIFY_SCAN_PAUSED,
  MPNOTIFY_SCAN_RESUMED,
  MPNOTIFY_SCAN_CANCEL,
  MPNOTIFY_SCAN_COMPLETE,
  MPNOTIFY_SCAN_PROGRESS,
  MPNOTIFY_SCAN_ERROR,
  MPNOTIFY_SCAN_INFECTED,
  MPNOTIFY_SCAN_MEMORYSTART,
  MPNOTIFY_SCAN_MEMORYCOMPLETE,
  MPNOTIFY_SCAN_SFC_BUILD_START,
  MPNOTIFY_SCAN_SFC_BUILD_COMPLETE,
  MPNOTIFY_SCAN_FASTPATH_START,
  MPNOTIFY_SCAN_FASTPATH_COMPLETE,
  MPNOTIFY_SCAN_FASTPATH_PROGRESS,
  MPNOTIFY_CLEAN_START,
  MPNOTIFY_CLEAN_COMPLETE,
  MPNOTIFY_CLEAN_RESTOREPOINT_START,
  MPNOTIFY_CLEAN_RESTOREPOINT_SUCCEEDED,
  MPNOTIFY_CLEAN_RESTOREPOINT_FAILED,
  MPNOTIFY_CLEAN_THREAT_START,
  MPNOTIFY_CLEAN_THREAT_SUCCEEDED,
  MPNOTIFY_CLEAN_THREAT_FAILED,
  MPNOTIFY_CLEAN_RESOURCE_SUCCEEDED,
  MPNOTIFY_CLEAN_RESOURCE_FAILED,
  MPNOTIFY_CLEAN_THREAT_COMPLETE,
  MPNOTIFY_PRECHECK_START,
  MPNOTIFY_PRECHECK_COMPLETE,
  MPNOTIFY_PRECHECK_RESOURCE_BLOCKED,
  MPNOTIFY_THREAT_DETECTED,
  MPNOTIFY_THREAT_MODIFIED,
  MPNOTIFY_THREAT_CLEAN_SUCCEEDED,
  MPNOTIFY_THREAT_CLEAN_FAILED,
  MPNOTIFY_THREAT_ABANDONED,
  MPNOTIFY_THREAT_CLEAN_EVENT_START,
  MPNOTIFY_THREAT_CLEAN_EVENT_COMPLETE,
  MPNOTIFY_SIGUPDATE_START,
  MPNOTIFY_SIGUPDATE_SEARCH_START,
  MPNOTIFY_SIGUPDATE_SEARCH_COMPLETE,
  MPNOTIFY_SIGUPDATE_SOFTWARE_UPDATE_AVAILABLE,
  MPNOTIFY_SIGUPDATE_DOWNLOAD_START,
  MPNOTIFY_SIGUPDATE_DOWNLOAD_PROGRESS,
  MPNOTIFY_SIGUPDATE_DOWNLOAD_COMPLETE,
  MPNOTIFY_SIGUPDATE_INSTALL_START,
  MPNOTIFY_SIGUPDATE_INSTALL_PROGRESS,
  MPNOTIFY_SIGUPDATE_INSTALL_COMPLETE,
  MPNOTIFY_SIGUPDATE_REBOOT_REQUIRED,
  MPNOTIFY_SIGUPDATE_REQUEST_PROCESSED,
  MPNOTIFY_SIGUPDATE_COMPLETE,
  MPNOTIFY_SAMPLE_START,
  MPNOTIFY_SAMPLE_COMPLETE,
  MPNOTIFY_SAMPLE_ITEM_START,
  MPNOTIFY_SAMPLE_ITEM_SUCCEEDED,
  MPNOTIFY_SAMPLE_ITEM_FAILED,
  MPNOTIFY_RESERVED_DATA,
  MPNOTIFY_FASTPATH_SIG_ADDED,
  MPNOTIFY_FASTPATH_SIG_REMOVED,
  MPNOTIFY_NIS_PRIVATE,
  MPNOTIFY_HEALTH_CHANGE,
  MPNOTIFY_HEALTH_RECOVERY,
  MPNOTIFY_HEALTH_START,
  MPNOTIFY_ENDOFLIFE_CHANGE,
  MPNOTIFY_MALWARETOAST_DATA
} MPNOTIFY, *PMPNOTIFY;
```



## <a name="constants"></a><span data-ttu-id="3e239-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="3e239-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="3e239-109"><span id="MPNOTIFY_NONE"></span><span id="mpnotify_none"></span>**MPNOTIFY \_ aucun**</span><span class="sxs-lookup"><span data-stu-id="3e239-109"><span id="MPNOTIFY_NONE"></span><span id="mpnotify_none"></span>**MPNOTIFY\_NONE**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="3e239-110"><span id="MPNOTIFY_CALL_START"></span><span id="mpnotify_call_start"></span>**début de l' \_ appel MPNOTIFY \_**</span><span class="sxs-lookup"><span data-stu-id="3e239-110"><span id="MPNOTIFY_CALL_START"></span><span id="mpnotify_call_start"></span>**MPNOTIFY\_CALL\_START**</span></span>
</dt> <dd>

<span data-ttu-id="3e239-111">Début de l’appel de notification.</span><span class="sxs-lookup"><span data-stu-id="3e239-111">Notification call start.</span></span>

</dd> <dt>

<span data-ttu-id="3e239-112"><span id="MPNOTIFY_CALL_COMPLETE"></span><span id="mpnotify_call_complete"></span>**\_appel MPNOTIFY \_ terminé**</span><span class="sxs-lookup"><span data-stu-id="3e239-112"><span id="MPNOTIFY_CALL_COMPLETE"></span><span id="mpnotify_call_complete"></span>**MPNOTIFY\_CALL\_COMPLETE**</span></span>
</dt> <dd>

<span data-ttu-id="3e239-113">Appel de notification terminé.</span><span class="sxs-lookup"><span data-stu-id="3e239-113">Notification call completed.</span></span>

</dd> <dt>

<span data-ttu-id="3e239-114"><span id="MPNOTIFY_INTERNAL_FAILURE"></span><span id="mpnotify_internal_failure"></span>**\_échec interne \_ MPNOTIFY**</span><span class="sxs-lookup"><span data-stu-id="3e239-114"><span id="MPNOTIFY_INTERNAL_FAILURE"></span><span id="mpnotify_internal_failure"></span>**MPNOTIFY\_INTERNAL\_FAILURE**</span></span>
</dt> <dd>

<span data-ttu-id="3e239-115">Échec interne générique.</span><span class="sxs-lookup"><span data-stu-id="3e239-115">Generic internal failure.</span></span>

</dd> <dt>

<span data-ttu-id="3e239-116"><span id="MPNOTIFY_STATUS_SERVICE_START"></span><span id="mpnotify_status_service_start"></span>**\_démarrage du \_ service d’État MPNOTIFY \_**</span><span class="sxs-lookup"><span data-stu-id="3e239-116"><span id="MPNOTIFY_STATUS_SERVICE_START"></span><span id="mpnotify_status_service_start"></span>**MPNOTIFY\_STATUS\_SERVICE\_START**</span></span>
</dt> <dd>

<span data-ttu-id="3e239-117">Le service de protection contre les programmes malveillants a démarré.</span><span class="sxs-lookup"><span data-stu-id="3e239-117">Malware protection service has started.</span></span>

</dd> <dt>

<span data-ttu-id="3e239-118"><span id="MPNOTIFY_STATUS_SERVICE_RUNNING"></span><span id="mpnotify_status_service_running"></span>**\_service d’État MPNOTIFY \_ \_ en cours d’exécution**</span><span class="sxs-lookup"><span data-stu-id="3e239-118"><span id="MPNOTIFY_STATUS_SERVICE_RUNNING"></span><span id="mpnotify_status_service_running"></span>**MPNOTIFY\_STATUS\_SERVICE\_RUNNING**</span></span>
</dt> <dd>

<span data-ttu-id="3e239-119">Le service protection contre les programmes malveillants est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="3e239-119">Malware protection service is running.</span></span>

</dd> <dt>

<span data-ttu-id="3e239-120"><span id="MPNOTIFY_STATUS_SERVICE_STOP"></span><span id="mpnotify_status_service_stop"></span>**\_arrêt du \_ service d’État MPNOTIFY \_**</span><span class="sxs-lookup"><span data-stu-id="3e239-120"><span id="MPNOTIFY_STATUS_SERVICE_STOP"></span><span id="mpnotify_status_service_stop"></span>**MPNOTIFY\_STATUS\_SERVICE\_STOP**</span></span>
</dt> <dd>

<span data-ttu-id="3e239-121">Le service de protection contre les programmes malveillants s’est arrêté.</span><span class="sxs-lookup"><span data-stu-id="3e239-121">Malware protection service has stopped.</span></span>

</dd> <dt>

<span data-ttu-id="3e239-122"><span id="MPNOTIFY_STATUS_COMPONENT"></span><span id="mpnotify_status_component"></span>**\_composant d’État MPNOTIFY \_**</span><span class="sxs-lookup"><span data-stu-id="3e239-122"><span id="MPNOTIFY_STATUS_COMPONENT"></span><span id="mpnotify_status_component"></span>**MPNOTIFY\_STATUS\_COMPONENT**</span></span>
</dt> <dd>

<span data-ttu-id="3e239-123">État d’activation/de désactivation de composant particulier.</span><span class="sxs-lookup"><span data-stu-id="3e239-123">Particular component enable/disable status.</span></span>

</dd> <dt>

<span data-ttu-id="3e239-124"><span id="MPNOTIFY_STATUS_CHANGE"></span><span id="mpnotify_status_change"></span>**modification de l’état de MPNOTIFY \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3e239-124"><span id="MPNOTIFY_STATUS_CHANGE"></span><span id="mpnotify_status_change"></span>**MPNOTIFY\_STATUS\_CHANGE**</span></span>
</dt> <dd>

<span data-ttu-id="3e239-125">L’état général du produit a changé.</span><span class="sxs-lookup"><span data-stu-id="3e239-125">Overall product status has changed.</span></span> <span data-ttu-id="3e239-126">Appelez [**MpManagerStatusQueryEx**](mpmanagerstatusqueryex.md) pour obtenir l’état actuel.</span><span class="sxs-lookup"><span data-stu-id="3e239-126">Call [**MpManagerStatusQueryEx**](mpmanagerstatusqueryex.md) to obtain the current status.</span></span>

</dd> <dt>

<span data-ttu-id="3e239-127"><span id="MPNOTIFY_STATUS_COMPONENT_CONFIGURATION"></span><span id="mpnotify_status_component_configuration"></span>**\_configuration du \_ composant d’État MPNOTIFY \_**</span><span class="sxs-lookup"><span data-stu-id="3e239-127"><span id="MPNOTIFY_STATUS_COMPONENT_CONFIGURATION"></span><span id="mpnotify_status_component_configuration"></span>**MPNOTIFY\_STATUS\_COMPONENT\_CONFIGURATION**</span></span>
</dt> <dd>

<span data-ttu-id="3e239-128">Une configuration a été modifiée pour un composant particulier.</span><span class="sxs-lookup"><span data-stu-id="3e239-128">A particular component has changed configuration.</span></span>

</dd> <dt>

<span data-ttu-id="3e239-129"><span id="MPNOTIFY_STATUS_EXPIRATION_CHANGE"></span><span id="mpnotify_status_expiration_change"></span>**\_ \_ modification d’expiration de l’État MPNOTIFY \_**</span><span class="sxs-lookup"><span data-stu-id="3e239-129"><span id="MPNOTIFY_STATUS_EXPIRATION_CHANGE"></span><span id="mpnotify_status_expiration_change"></span>**MPNOTIFY\_STATUS\_EXPIRATION\_CHANGE**</span></span>
</dt> <dd>

<span data-ttu-id="3e239-130">L’état d’expiration du produit a changé.</span><span class="sxs-lookup"><span data-stu-id="3e239-130">Product expiration status has changed.</span></span>

</dd> <dt>

<span data-ttu-id="3e239-131"><span id="MPNOTIFY_STATUS_OFFLINE_SCAN_CHANGE"></span><span id="mpnotify_status_offline_scan_change"></span>**modification de l' \_ État d' \_ analyse hors connexion \_ \_ MPNOTIFY**</span><span class="sxs-lookup"><span data-stu-id="3e239-131"><span id="MPNOTIFY_STATUS_OFFLINE_SCAN_CHANGE"></span><span id="mpnotify_status_offline_scan_change"></span>**MPNOTIFY\_STATUS\_OFFLINE\_SCAN\_CHANGE**</span></span>
</dt> <dd>

<span data-ttu-id="3e239-132">L’état de l’analyse hors connexion requis a changé.</span><span class="sxs-lookup"><span data-stu-id="3e239-132">Offline scan required state changed.</span></span>

</dd> <dt>

<span data-ttu-id="3e239-133"><span id="MPNOTIFY_SCAN_START"></span><span id="mpnotify_scan_start"></span>**début de l' \_ analyse MPNOTIFY \_**</span><span class="sxs-lookup"><span data-stu-id="3e239-133"><span id="MPNOTIFY_SCAN_START"></span><span id="mpnotify_scan_start"></span>**MPNOTIFY\_SCAN\_START**</span></span>
</dt> <dd>

<span data-ttu-id="3e239-134">Début de l’analyse.</span><span class="sxs-lookup"><span data-stu-id="3e239-134">Scan started.</span></span>

</dd> <dt>

<span data-ttu-id="3e239-135"><span id="MPNOTIFY_SCAN_PAUSED"></span><span id="mpnotify_scan_paused"></span>**\_analyse MPNOTIFY \_ suspendue**</span><span class="sxs-lookup"><span data-stu-id="3e239-135"><span id="MPNOTIFY_SCAN_PAUSED"></span><span id="mpnotify_scan_paused"></span>**MPNOTIFY\_SCAN\_PAUSED**</span></span>
</dt> <dd>

<span data-ttu-id="3e239-136">Analyse suspendue.</span><span class="sxs-lookup"><span data-stu-id="3e239-136">Scan paused.</span></span>

</dd> <dt>

<span data-ttu-id="3e239-137"><span id="MPNOTIFY_SCAN_RESUMED"></span><span id="mpnotify_scan_resumed"></span>**\_analyse MPNOTIFY \_ reprise**</span><span class="sxs-lookup"><span data-stu-id="3e239-137"><span id="MPNOTIFY_SCAN_RESUMED"></span><span id="mpnotify_scan_resumed"></span>**MPNOTIFY\_SCAN\_RESUMED**</span></span>
</dt> <dd>

<span data-ttu-id="3e239-138">analyse reprise.</span><span class="sxs-lookup"><span data-stu-id="3e239-138">scan resumed.</span></span>

</dd> <dt>

<span data-ttu-id="3e239-139"><span id="MPNOTIFY_SCAN_CANCEL"></span><span id="mpnotify_scan_cancel"></span>**annulation de l' \_ analyse MPNOTIFY \_**</span><span class="sxs-lookup"><span data-stu-id="3e239-139"><span id="MPNOTIFY_SCAN_CANCEL"></span><span id="mpnotify_scan_cancel"></span>**MPNOTIFY\_SCAN\_CANCEL**</span></span>
</dt> <dd>

<span data-ttu-id="3e239-140">Analyse annulée.</span><span class="sxs-lookup"><span data-stu-id="3e239-140">Scan cancelled.</span></span>

</dd> <dt>

<span data-ttu-id="3e239-141"><span id="MPNOTIFY_SCAN_COMPLETE"></span><span id="mpnotify_scan_complete"></span>**\_analyse MPNOTIFY \_ terminée**</span><span class="sxs-lookup"><span data-stu-id="3e239-141"><span id="MPNOTIFY_SCAN_COMPLETE"></span><span id="mpnotify_scan_complete"></span>**MPNOTIFY\_SCAN\_COMPLETE**</span></span>
</dt> <dd>

<span data-ttu-id="3e239-142">Analyse terminée.</span><span class="sxs-lookup"><span data-stu-id="3e239-142">Scan completed.</span></span>

</dd> <dt>

<span data-ttu-id="3e239-143"><span id="MPNOTIFY_SCAN_PROGRESS"></span><span id="mpnotify_scan_progress"></span>**progression de l' \_ analyse MPNOTIFY \_**</span><span class="sxs-lookup"><span data-stu-id="3e239-143"><span id="MPNOTIFY_SCAN_PROGRESS"></span><span id="mpnotify_scan_progress"></span>**MPNOTIFY\_SCAN\_PROGRESS**</span></span>
</dt> <dd>

<span data-ttu-id="3e239-144">Notification de progression pour la ressource spécifique en cours d’analyse.</span><span class="sxs-lookup"><span data-stu-id="3e239-144">Progress notification for the specific resource being scanned.</span></span>

</dd> <dt>

<span data-ttu-id="3e239-145"><span id="MPNOTIFY_SCAN_ERROR"></span><span id="mpnotify_scan_error"></span>**\_erreur d’analyse MPNOTIFY \_**</span><span class="sxs-lookup"><span data-stu-id="3e239-145"><span id="MPNOTIFY_SCAN_ERROR"></span><span id="mpnotify_scan_error"></span>**MPNOTIFY\_SCAN\_ERROR**</span></span>
</dt> <dd>

<span data-ttu-id="3e239-146">Échec de l’analyse d’une ressource particulière.</span><span class="sxs-lookup"><span data-stu-id="3e239-146">Failure to scan a particular resource.</span></span> <span data-ttu-id="3e239-147">L’analyse continuera toujours.</span><span class="sxs-lookup"><span data-stu-id="3e239-147">Scan will still continue.</span></span>

</dd> <dt>

<span data-ttu-id="3e239-148"><span id="MPNOTIFY_SCAN_INFECTED"></span><span id="mpnotify_scan_infected"></span>**\_analyse MPNOTIFY \_ infectée**</span><span class="sxs-lookup"><span data-stu-id="3e239-148"><span id="MPNOTIFY_SCAN_INFECTED"></span><span id="mpnotify_scan_infected"></span>**MPNOTIFY\_SCAN\_INFECTED**</span></span>
</dt> <dd>

<span data-ttu-id="3e239-149">L’analyse a trouvé une ressource infectée.</span><span class="sxs-lookup"><span data-stu-id="3e239-149">Scan found an infected resource.</span></span>

</dd> <dt>

<span data-ttu-id="3e239-150"><span id="MPNOTIFY_SCAN_MEMORYSTART"></span><span id="mpnotify_scan_memorystart"></span>**MPNOTIFY \_ Scan \_ MEMORYSTART**</span><span class="sxs-lookup"><span data-stu-id="3e239-150"><span id="MPNOTIFY_SCAN_MEMORYSTART"></span><span id="mpnotify_scan_memorystart"></span>**MPNOTIFY\_SCAN\_MEMORYSTART**</span></span>
</dt> <dd>

<span data-ttu-id="3e239-151">La progression de l’analyse pour notifier la mémoire de l’analyse du système a démarré.</span><span class="sxs-lookup"><span data-stu-id="3e239-151">Scan progress to notify memory scan portion of the system scan has started.</span></span>

</dd> <dt>

<span data-ttu-id="3e239-152"><span id="MPNOTIFY_SCAN_MEMORYCOMPLETE"></span><span id="mpnotify_scan_memorycomplete"></span>**MPNOTIFY \_ Scan \_ MEMORYCOMPLETE**</span><span class="sxs-lookup"><span data-stu-id="3e239-152"><span id="MPNOTIFY_SCAN_MEMORYCOMPLETE"></span><span id="mpnotify_scan_memorycomplete"></span>**MPNOTIFY\_SCAN\_MEMORYCOMPLETE**</span></span>
</dt> <dd>

<span data-ttu-id="3e239-153">La progression de l’analyse pour notifier la mémoire de l’analyse du système est terminée.</span><span class="sxs-lookup"><span data-stu-id="3e239-153">Scan progress to notify memory scan portion of the system scan has completed.</span></span>

</dd> <dt>

<span data-ttu-id="3e239-154"><span id="MPNOTIFY_SCAN_SFC_BUILD_START"></span><span id="mpnotify_scan_sfc_build_start"></span>**démarrage de la \_ génération MPNOTIFY Scan \_ SFC \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3e239-154"><span id="MPNOTIFY_SCAN_SFC_BUILD_START"></span><span id="mpnotify_scan_sfc_build_start"></span>**MPNOTIFY\_SCAN\_SFC\_BUILD\_START**</span></span>
</dt> <dd>

<span data-ttu-id="3e239-155">Progression de l’analyse pour notifier la partie de build SFC a démarré.</span><span class="sxs-lookup"><span data-stu-id="3e239-155">Scan progress to notify sfc build portion has started.</span></span>

</dd> <dt>

<span data-ttu-id="3e239-156"><span id="MPNOTIFY_SCAN_SFC_BUILD_COMPLETE"></span><span id="mpnotify_scan_sfc_build_complete"></span>**\_Build SFC d’analyse MPNOTIFY \_ \_ \_ terminée**</span><span class="sxs-lookup"><span data-stu-id="3e239-156"><span id="MPNOTIFY_SCAN_SFC_BUILD_COMPLETE"></span><span id="mpnotify_scan_sfc_build_complete"></span>**MPNOTIFY\_SCAN\_SFC\_BUILD\_COMPLETE**</span></span>
</dt> <dd>

<span data-ttu-id="3e239-157">Progression de l’analyse pour notifier la partie de build SFC terminée.</span><span class="sxs-lookup"><span data-stu-id="3e239-157">Scan progress to notify sfc build portion has completed.</span></span>

</dd> <dt>

<span data-ttu-id="3e239-158"><span id="MPNOTIFY_SCAN_FASTPATH_START"></span><span id="mpnotify_scan_fastpath_start"></span>**démarrage de l' \_ analyse MPNOTIFY \_ FASTPATH \_**</span><span class="sxs-lookup"><span data-stu-id="3e239-158"><span id="MPNOTIFY_SCAN_FASTPATH_START"></span><span id="mpnotify_scan_fastpath_start"></span>**MPNOTIFY\_SCAN\_FASTPATH\_START**</span></span>
</dt> <dd>

<span data-ttu-id="3e239-159">L’analyse FastPath SpyNet a commencé.</span><span class="sxs-lookup"><span data-stu-id="3e239-159">Scan fastpath spynet has begun.</span></span>

</dd> <dt>

<span data-ttu-id="3e239-160"><span id="MPNOTIFY_SCAN_FASTPATH_COMPLETE"></span><span id="mpnotify_scan_fastpath_complete"></span>**\_FASTPATH d’analyse MPNOTIFY \_ \_ terminé**</span><span class="sxs-lookup"><span data-stu-id="3e239-160"><span id="MPNOTIFY_SCAN_FASTPATH_COMPLETE"></span><span id="mpnotify_scan_fastpath_complete"></span>**MPNOTIFY\_SCAN\_FASTPATH\_COMPLETE**</span></span>
</dt> <dd>

<span data-ttu-id="3e239-161">L’analyse FastPath SpyNet est terminée.</span><span class="sxs-lookup"><span data-stu-id="3e239-161">Scan fastpath spynet has ended.</span></span>

</dd> <dt>

<span data-ttu-id="3e239-162"><span id="MPNOTIFY_SCAN_FASTPATH_PROGRESS"></span><span id="mpnotify_scan_fastpath_progress"></span>**progression de l' \_ analyse MPNOTIFY \_ FASTPATH \_**</span><span class="sxs-lookup"><span data-stu-id="3e239-162"><span id="MPNOTIFY_SCAN_FASTPATH_PROGRESS"></span><span id="mpnotify_scan_fastpath_progress"></span>**MPNOTIFY\_SCAN\_FASTPATH\_PROGRESS**</span></span>
</dt> <dd>

<span data-ttu-id="3e239-163">Notification de progression pour les analyses FastPath, utilisée en interne et convertie en **\_ \_ progression de l’analyse MPNOTIFY** pour External.</span><span class="sxs-lookup"><span data-stu-id="3e239-163">Progress notification for fastpath rescans, used internally and converted to **MPNOTIFY\_SCAN\_PROGRESS** for external.</span></span>

</dd> <dt>

<span data-ttu-id="3e239-164"><span id="MPNOTIFY_CLEAN_START"></span><span id="mpnotify_clean_start"></span>**\_démarrage propre \_ MPNOTIFY**</span><span class="sxs-lookup"><span data-stu-id="3e239-164"><span id="MPNOTIFY_CLEAN_START"></span><span id="mpnotify_clean_start"></span>**MPNOTIFY\_CLEAN\_START**</span></span>
</dt> <dd>

<span data-ttu-id="3e239-165">Nettoyage démarré.</span><span class="sxs-lookup"><span data-stu-id="3e239-165">Cleaning started.</span></span>

</dd> <dt>

<span data-ttu-id="3e239-166"><span id="MPNOTIFY_CLEAN_COMPLETE"></span><span id="mpnotify_clean_complete"></span>**MPNOTIFY \_ nettoyage \_ terminé**</span><span class="sxs-lookup"><span data-stu-id="3e239-166"><span id="MPNOTIFY_CLEAN_COMPLETE"></span><span id="mpnotify_clean_complete"></span>**MPNOTIFY\_CLEAN\_COMPLETE**</span></span>
</dt> <dd>

<span data-ttu-id="3e239-167">Nettoyage terminé.</span><span class="sxs-lookup"><span data-stu-id="3e239-167">Cleaning completed.</span></span>

</dd> <dt>

<span data-ttu-id="3e239-168"><span id="MPNOTIFY_CLEAN_RESTOREPOINT_START"></span><span id="mpnotify_clean_restorepoint_start"></span>**MPNOTIFY \_ Clean \_ RESTOREPOINT \_ Start**</span><span class="sxs-lookup"><span data-stu-id="3e239-168"><span id="MPNOTIFY_CLEAN_RESTOREPOINT_START"></span><span id="mpnotify_clean_restorepoint_start"></span>**MPNOTIFY\_CLEAN\_RESTOREPOINT\_START**</span></span>
</dt> <dd>

<span data-ttu-id="3e239-169">Début de la création d’un point de restauration système.</span><span class="sxs-lookup"><span data-stu-id="3e239-169">Started to create a system restore point.</span></span>

</dd> <dt>

<span data-ttu-id="3e239-170"><span id="MPNOTIFY_CLEAN_RESTOREPOINT_SUCCEEDED"></span><span id="mpnotify_clean_restorepoint_succeeded"></span>**MPNOTIFY \_ Clean \_ RESTOREPOINT \_ réussi**</span><span class="sxs-lookup"><span data-stu-id="3e239-170"><span id="MPNOTIFY_CLEAN_RESTOREPOINT_SUCCEEDED"></span><span id="mpnotify_clean_restorepoint_succeeded"></span>**MPNOTIFY\_CLEAN\_RESTOREPOINT\_SUCCEEDED**</span></span>
</dt> <dd>

<span data-ttu-id="3e239-171">Point de restauration système créé avec succès.</span><span class="sxs-lookup"><span data-stu-id="3e239-171">System restore point successfully created.</span></span>

</dd> <dt>

<span data-ttu-id="3e239-172"><span id="MPNOTIFY_CLEAN_RESTOREPOINT_FAILED"></span><span id="mpnotify_clean_restorepoint_failed"></span>**\_échec du nettoyage du \_ RESTOREPOINT MPNOTIFY \_**</span><span class="sxs-lookup"><span data-stu-id="3e239-172"><span id="MPNOTIFY_CLEAN_RESTOREPOINT_FAILED"></span><span id="mpnotify_clean_restorepoint_failed"></span>**MPNOTIFY\_CLEAN\_RESTOREPOINT\_FAILED**</span></span>
</dt> <dd>

<span data-ttu-id="3e239-173">Échec de la création du point de restauration du système.</span><span class="sxs-lookup"><span data-stu-id="3e239-173">System restore point creation failed.</span></span>

</dd> <dt>

<span data-ttu-id="3e239-174"><span id="MPNOTIFY_CLEAN_THREAT_START"></span><span id="mpnotify_clean_threat_start"></span>**\_Démarrer le nettoyage des \_ menaces MPNOTIFY \_**</span><span class="sxs-lookup"><span data-stu-id="3e239-174"><span id="MPNOTIFY_CLEAN_THREAT_START"></span><span id="mpnotify_clean_threat_start"></span>**MPNOTIFY\_CLEAN\_THREAT\_START**</span></span>
</dt> <dd>

<span data-ttu-id="3e239-175">Le nettoyage est lancé pour une menace particulière.</span><span class="sxs-lookup"><span data-stu-id="3e239-175">Cleaning is started for a particular threat.</span></span>

</dd> <dt>

<span data-ttu-id="3e239-176"><span id="MPNOTIFY_CLEAN_THREAT_SUCCEEDED"></span><span id="mpnotify_clean_threat_succeeded"></span>**MPNOTIFY \_ Clean \_ Threat \_ a réussi**</span><span class="sxs-lookup"><span data-stu-id="3e239-176"><span id="MPNOTIFY_CLEAN_THREAT_SUCCEEDED"></span><span id="mpnotify_clean_threat_succeeded"></span>**MPNOTIFY\_CLEAN\_THREAT\_SUCCEEDED**</span></span>
</dt> <dd>

<span data-ttu-id="3e239-177">Le nettoyage a réussi pour une menace particulière.</span><span class="sxs-lookup"><span data-stu-id="3e239-177">Cleaning is succeeded for a particular threat.</span></span>

</dd> <dt>

<span data-ttu-id="3e239-178"><span id="MPNOTIFY_CLEAN_THREAT_FAILED"></span><span id="mpnotify_clean_threat_failed"></span>**échec du nettoyage de la \_ \_ menace MPNOTIFY \_**</span><span class="sxs-lookup"><span data-stu-id="3e239-178"><span id="MPNOTIFY_CLEAN_THREAT_FAILED"></span><span id="mpnotify_clean_threat_failed"></span>**MPNOTIFY\_CLEAN\_THREAT\_FAILED**</span></span>
</dt> <dd>

<span data-ttu-id="3e239-179">Le nettoyage a échoué pour une menace particulière.</span><span class="sxs-lookup"><span data-stu-id="3e239-179">Cleaning has failed for a particular threat.</span></span> <span data-ttu-id="3e239-180">**Erreur \_ Le code d’erreur « menace de point de gestion \_ \_ \_ introuvable** » indique que la menace n’a pas été trouvée (et qu’elle n’a pas pu être nettoyée).</span><span class="sxs-lookup"><span data-stu-id="3e239-180">**ERROR\_MP\_THREAT\_NOT\_FOUND** error code indicates that the threat was not found (and was not a failure to clean).</span></span>

</dd> <dt>

<span data-ttu-id="3e239-181"><span id="MPNOTIFY_CLEAN_RESOURCE_SUCCEEDED"></span><span id="mpnotify_clean_resource_succeeded"></span>**\_ressource de nettoyage MPNOTIFY \_ \_ réussie**</span><span class="sxs-lookup"><span data-stu-id="3e239-181"><span id="MPNOTIFY_CLEAN_RESOURCE_SUCCEEDED"></span><span id="mpnotify_clean_resource_succeeded"></span>**MPNOTIFY\_CLEAN\_RESOURCE\_SUCCEEDED**</span></span>
</dt> <dd>

<span data-ttu-id="3e239-182">Le nettoyage a réussi pour une ressource particulière.</span><span class="sxs-lookup"><span data-stu-id="3e239-182">Cleaning is succeeded for a particular resource.</span></span>

</dd> <dt>

<span data-ttu-id="3e239-183"><span id="MPNOTIFY_CLEAN_RESOURCE_FAILED"></span><span id="mpnotify_clean_resource_failed"></span>**échec du nettoyage de la \_ \_ ressource MPNOTIFY \_**</span><span class="sxs-lookup"><span data-stu-id="3e239-183"><span id="MPNOTIFY_CLEAN_RESOURCE_FAILED"></span><span id="mpnotify_clean_resource_failed"></span>**MPNOTIFY\_CLEAN\_RESOURCE\_FAILED**</span></span>
</dt> <dd>

<span data-ttu-id="3e239-184">Le nettoyage a échoué pour une ressource particulière.</span><span class="sxs-lookup"><span data-stu-id="3e239-184">Cleaning has failed for a particular resource.</span></span>

</dd> <dt>

<span data-ttu-id="3e239-185"><span id="MPNOTIFY_CLEAN_THREAT_COMPLETE"></span><span id="mpnotify_clean_threat_complete"></span>**nettoyage de la \_ \_ menace MPNOTIFY \_ terminé**</span><span class="sxs-lookup"><span data-stu-id="3e239-185"><span id="MPNOTIFY_CLEAN_THREAT_COMPLETE"></span><span id="mpnotify_clean_threat_complete"></span>**MPNOTIFY\_CLEAN\_THREAT\_COMPLETE**</span></span>
</dt> <dd>

<span data-ttu-id="3e239-186">Le nettoyage s’est terminé pour une menace particulière.</span><span class="sxs-lookup"><span data-stu-id="3e239-186">Cleaning has completed for a particular threat.</span></span>

</dd> <dt>

<span data-ttu-id="3e239-187"><span id="MPNOTIFY_PRECHECK_START"></span><span id="mpnotify_precheck_start"></span>**démarrage de la \_ PRÉVÉRIFICATION MPNOTIFY \_**</span><span class="sxs-lookup"><span data-stu-id="3e239-187"><span id="MPNOTIFY_PRECHECK_START"></span><span id="mpnotify_precheck_start"></span>**MPNOTIFY\_PRECHECK\_START**</span></span>
</dt> <dd>

<span data-ttu-id="3e239-188">Nettoyage de la prévérification démarré.</span><span class="sxs-lookup"><span data-stu-id="3e239-188">Clean precheck started.</span></span>

</dd> <dt>

<span data-ttu-id="3e239-189"><span id="MPNOTIFY_PRECHECK_COMPLETE"></span><span id="mpnotify_precheck_complete"></span>**prévérification de MPNOTIFY \_ \_ terminée**</span><span class="sxs-lookup"><span data-stu-id="3e239-189"><span id="MPNOTIFY_PRECHECK_COMPLETE"></span><span id="mpnotify_precheck_complete"></span>**MPNOTIFY\_PRECHECK\_COMPLETE**</span></span>
</dt> <dd>

<span data-ttu-id="3e239-190">La prévérification du nettoyage est terminée.</span><span class="sxs-lookup"><span data-stu-id="3e239-190">Clean precheck completed.</span></span>

</dd> <dt>

<span data-ttu-id="3e239-191"><span id="MPNOTIFY_PRECHECK_RESOURCE_BLOCKED"></span><span id="mpnotify_precheck_resource_blocked"></span>**\_ressource de PRÉVÉRIFICATION MPNOTIFY \_ \_ bloquée**</span><span class="sxs-lookup"><span data-stu-id="3e239-191"><span id="MPNOTIFY_PRECHECK_RESOURCE_BLOCKED"></span><span id="mpnotify_precheck_resource_blocked"></span>**MPNOTIFY\_PRECHECK\_RESOURCE\_BLOCKED**</span></span>
</dt> <dd>

<span data-ttu-id="3e239-192">La prévérification propre a détecté une ressource bloquée.</span><span class="sxs-lookup"><span data-stu-id="3e239-192">Clean precheck detected blocked resource.</span></span>

</dd> <dt>

<span data-ttu-id="3e239-193"><span id="MPNOTIFY_THREAT_DETECTED"></span><span id="mpnotify_threat_detected"></span>**\_menace MPNOTIFY \_ détectée**</span><span class="sxs-lookup"><span data-stu-id="3e239-193"><span id="MPNOTIFY_THREAT_DETECTED"></span><span id="mpnotify_threat_detected"></span>**MPNOTIFY\_THREAT\_DETECTED**</span></span>
</dt> <dd>

<span data-ttu-id="3e239-194">Nouvelle menace détectée dans le système.</span><span class="sxs-lookup"><span data-stu-id="3e239-194">New threat detected in system.</span></span>

</dd> <dt>

<span data-ttu-id="3e239-195"><span id="MPNOTIFY_THREAT_MODIFIED"></span><span id="mpnotify_threat_modified"></span>**\_menace MPNOTIFY \_ modifiée**</span><span class="sxs-lookup"><span data-stu-id="3e239-195"><span id="MPNOTIFY_THREAT_MODIFIED"></span><span id="mpnotify_threat_modified"></span>**MPNOTIFY\_THREAT\_MODIFIED**</span></span>
</dt> <dd>

<span data-ttu-id="3e239-196">Informations sur les menaces modifiées.</span><span class="sxs-lookup"><span data-stu-id="3e239-196">Threat information modified.</span></span> <span data-ttu-id="3e239-197">Par exemple, une nouvelle ressource a été ajoutée.</span><span class="sxs-lookup"><span data-stu-id="3e239-197">For example, a new resource was added.</span></span>

</dd> <dt>

<span data-ttu-id="3e239-198"><span id="MPNOTIFY_THREAT_CLEAN_SUCCEEDED"></span><span id="mpnotify_threat_clean_succeeded"></span>**le \_ nettoyage de la menace MPNOTIFY \_ \_ a réussi**</span><span class="sxs-lookup"><span data-stu-id="3e239-198"><span id="MPNOTIFY_THREAT_CLEAN_SUCCEEDED"></span><span id="mpnotify_threat_clean_succeeded"></span>**MPNOTIFY\_THREAT\_CLEAN\_SUCCEEDED**</span></span>
</dt> <dd>

<span data-ttu-id="3e239-199">Action de nettoyage réussie pour une menace.</span><span class="sxs-lookup"><span data-stu-id="3e239-199">Cleaning action succeeded for a threat.</span></span>

</dd> <dt>

<span data-ttu-id="3e239-200"><span id="MPNOTIFY_THREAT_CLEAN_FAILED"></span><span id="mpnotify_threat_clean_failed"></span>**échec du nettoyage de la \_ menace MPNOTIFY \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3e239-200"><span id="MPNOTIFY_THREAT_CLEAN_FAILED"></span><span id="mpnotify_threat_clean_failed"></span>**MPNOTIFY\_THREAT\_CLEAN\_FAILED**</span></span>
</dt> <dd>

<span data-ttu-id="3e239-201">Échec de l’action de nettoyage pour une menace.</span><span class="sxs-lookup"><span data-stu-id="3e239-201">Cleaning action failed for a threat.</span></span> <span data-ttu-id="3e239-202">**Erreur \_ Le code d’erreur « menace de point de gestion \_ \_ \_ introuvable** » indique que la menace n’a pas été trouvée (et qu’elle n’a pas pu être nettoyée).</span><span class="sxs-lookup"><span data-stu-id="3e239-202">**ERROR\_MP\_THREAT\_NOT\_FOUND** error code indicates that the threat was not found (and was not a failure to clean).</span></span>

</dd> <dt>

<span data-ttu-id="3e239-203"><span id="MPNOTIFY_THREAT_ABANDONED"></span><span id="mpnotify_threat_abandoned"></span>**\_menace MPNOTIFY \_ abandonnée**</span><span class="sxs-lookup"><span data-stu-id="3e239-203"><span id="MPNOTIFY_THREAT_ABANDONED"></span><span id="mpnotify_threat_abandoned"></span>**MPNOTIFY\_THREAT\_ABANDONED**</span></span>
</dt> <dd>

<span data-ttu-id="3e239-204">Aucune correction n’a eu lieu avant l’arrêt du service.</span><span class="sxs-lookup"><span data-stu-id="3e239-204">No remediation occurred before the service was stopped.</span></span>

</dd> <dt>

<span data-ttu-id="3e239-205"><span id="MPNOTIFY_THREAT_CLEAN_EVENT_START"></span><span id="mpnotify_threat_clean_event_start"></span>**démarrage de l’événement de nettoyage des \_ menaces MPNOTIFY \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3e239-205"><span id="MPNOTIFY_THREAT_CLEAN_EVENT_START"></span><span id="mpnotify_threat_clean_event_start"></span>**MPNOTIFY\_THREAT\_CLEAN\_EVENT\_START**</span></span>
</dt> <dd>

<span data-ttu-id="3e239-206">Une action de nettoyage a été démarrée.</span><span class="sxs-lookup"><span data-stu-id="3e239-206">A cleaning action has been started.</span></span>

</dd> <dt>

<span data-ttu-id="3e239-207"><span id="MPNOTIFY_THREAT_CLEAN_EVENT_COMPLETE"></span><span id="mpnotify_threat_clean_event_complete"></span>**événement de nettoyage de la \_ menace MPNOTIFY \_ \_ \_ terminé**</span><span class="sxs-lookup"><span data-stu-id="3e239-207"><span id="MPNOTIFY_THREAT_CLEAN_EVENT_COMPLETE"></span><span id="mpnotify_threat_clean_event_complete"></span>**MPNOTIFY\_THREAT\_CLEAN\_EVENT\_COMPLETE**</span></span>
</dt> <dd>

<span data-ttu-id="3e239-208">Une action de nettoyage est terminée.</span><span class="sxs-lookup"><span data-stu-id="3e239-208">A cleaning action has ended.</span></span>

</dd> <dt>

<span data-ttu-id="3e239-209"><span id="MPNOTIFY_SIGUPDATE_START"></span><span id="mpnotify_sigupdate_start"></span>**MPNOTIFY \_ SIGUPDATE \_ Start**</span><span class="sxs-lookup"><span data-stu-id="3e239-209"><span id="MPNOTIFY_SIGUPDATE_START"></span><span id="mpnotify_sigupdate_start"></span>**MPNOTIFY\_SIGUPDATE\_START**</span></span>
</dt> <dd>

<span data-ttu-id="3e239-210">Mise à jour de signature démarrée.</span><span class="sxs-lookup"><span data-stu-id="3e239-210">Signature update started.</span></span>

</dd> <dt>

<span data-ttu-id="3e239-211"><span id="MPNOTIFY_SIGUPDATE_SEARCH_START"></span><span id="mpnotify_sigupdate_search_start"></span>**début de la \_ recherche MPNOTIFY SIGUPDATE \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3e239-211"><span id="MPNOTIFY_SIGUPDATE_SEARCH_START"></span><span id="mpnotify_sigupdate_search_start"></span>**MPNOTIFY\_SIGUPDATE\_SEARCH\_START**</span></span>
</dt> <dd>

<span data-ttu-id="3e239-212">Recherche des mises à jour démarrées.</span><span class="sxs-lookup"><span data-stu-id="3e239-212">Search for updates started.</span></span>

</dd> <dt>

<span data-ttu-id="3e239-213"><span id="MPNOTIFY_SIGUPDATE_SEARCH_COMPLETE"></span><span id="mpnotify_sigupdate_search_complete"></span>**recherche de MPNOTIFY \_ SIGUPDATE \_ \_ terminée**</span><span class="sxs-lookup"><span data-stu-id="3e239-213"><span id="MPNOTIFY_SIGUPDATE_SEARCH_COMPLETE"></span><span id="mpnotify_sigupdate_search_complete"></span>**MPNOTIFY\_SIGUPDATE\_SEARCH\_COMPLETE**</span></span>
</dt> <dd>

<span data-ttu-id="3e239-214">Recherche des mises à jour terminées.</span><span class="sxs-lookup"><span data-stu-id="3e239-214">Search for updates completed.</span></span>

</dd> <dt>

<span data-ttu-id="3e239-215"><span id="MPNOTIFY_SIGUPDATE_SOFTWARE_UPDATE_AVAILABLE"></span><span id="mpnotify_sigupdate_software_update_available"></span>**\_ \_ \_ mise à jour logicielle MPNOTIFY SIGUPDATE \_ disponible**</span><span class="sxs-lookup"><span data-stu-id="3e239-215"><span id="MPNOTIFY_SIGUPDATE_SOFTWARE_UPDATE_AVAILABLE"></span><span id="mpnotify_sigupdate_software_update_available"></span>**MPNOTIFY\_SIGUPDATE\_SOFTWARE\_UPDATE\_AVAILABLE**</span></span>
</dt> <dd>

<span data-ttu-id="3e239-216">Mise à jour logicielle disponible.</span><span class="sxs-lookup"><span data-stu-id="3e239-216">Software update available.</span></span>

</dd> <dt>

<span data-ttu-id="3e239-217"><span id="MPNOTIFY_SIGUPDATE_DOWNLOAD_START"></span><span id="mpnotify_sigupdate_download_start"></span>**démarrage du téléchargement de MPNOTIFY \_ SIGUPDATE \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3e239-217"><span id="MPNOTIFY_SIGUPDATE_DOWNLOAD_START"></span><span id="mpnotify_sigupdate_download_start"></span>**MPNOTIFY\_SIGUPDATE\_DOWNLOAD\_START**</span></span>
</dt> <dd>

<span data-ttu-id="3e239-218">Téléchargement démarré.</span><span class="sxs-lookup"><span data-stu-id="3e239-218">Download started.</span></span>

</dd> <dt>

<span data-ttu-id="3e239-219"><span id="MPNOTIFY_SIGUPDATE_DOWNLOAD_PROGRESS"></span><span id="mpnotify_sigupdate_download_progress"></span>**progression du téléchargement de MPNOTIFY \_ SIGUPDATE \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3e239-219"><span id="MPNOTIFY_SIGUPDATE_DOWNLOAD_PROGRESS"></span><span id="mpnotify_sigupdate_download_progress"></span>**MPNOTIFY\_SIGUPDATE\_DOWNLOAD\_PROGRESS**</span></span>
</dt> <dd>

<span data-ttu-id="3e239-220">Téléchargement en cours.</span><span class="sxs-lookup"><span data-stu-id="3e239-220">Download in progress.</span></span> <span data-ttu-id="3e239-221">Les données de rappel contiennent la progression.</span><span class="sxs-lookup"><span data-stu-id="3e239-221">Callback data contains progress.</span></span>

</dd> <dt>

<span data-ttu-id="3e239-222"><span id="MPNOTIFY_SIGUPDATE_DOWNLOAD_COMPLETE"></span><span id="mpnotify_sigupdate_download_complete"></span>**Téléchargement de MPNOTIFY \_ SIGUPDATE \_ \_ terminé**</span><span class="sxs-lookup"><span data-stu-id="3e239-222"><span id="MPNOTIFY_SIGUPDATE_DOWNLOAD_COMPLETE"></span><span id="mpnotify_sigupdate_download_complete"></span>**MPNOTIFY\_SIGUPDATE\_DOWNLOAD\_COMPLETE**</span></span>
</dt> <dd>

<span data-ttu-id="3e239-223">Téléchargement terminé.</span><span class="sxs-lookup"><span data-stu-id="3e239-223">Download completed.</span></span>

</dd> <dt>

<span data-ttu-id="3e239-224"><span id="MPNOTIFY_SIGUPDATE_INSTALL_START"></span><span id="mpnotify_sigupdate_install_start"></span>**démarrage de l’installation de MPNOTIFY \_ SIGUPDATE \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3e239-224"><span id="MPNOTIFY_SIGUPDATE_INSTALL_START"></span><span id="mpnotify_sigupdate_install_start"></span>**MPNOTIFY\_SIGUPDATE\_INSTALL\_START**</span></span>
</dt> <dd>

<span data-ttu-id="3e239-225">Installation démarrée.</span><span class="sxs-lookup"><span data-stu-id="3e239-225">Installation started.</span></span>

</dd> <dt>

<span data-ttu-id="3e239-226"><span id="MPNOTIFY_SIGUPDATE_INSTALL_PROGRESS"></span><span id="mpnotify_sigupdate_install_progress"></span>**progression de l’installation de MPNOTIFY \_ SIGUPDATE \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3e239-226"><span id="MPNOTIFY_SIGUPDATE_INSTALL_PROGRESS"></span><span id="mpnotify_sigupdate_install_progress"></span>**MPNOTIFY\_SIGUPDATE\_INSTALL\_PROGRESS**</span></span>
</dt> <dd>

<span data-ttu-id="3e239-227">Installation en cours.</span><span class="sxs-lookup"><span data-stu-id="3e239-227">Installation in progress.</span></span> <span data-ttu-id="3e239-228">Les données de rappel contiennent la progression.</span><span class="sxs-lookup"><span data-stu-id="3e239-228">Callback data contains progress.</span></span>

</dd> <dt>

<span data-ttu-id="3e239-229"><span id="MPNOTIFY_SIGUPDATE_INSTALL_COMPLETE"></span><span id="mpnotify_sigupdate_install_complete"></span>**installation de MPNOTIFY \_ SIGUPDATE \_ \_ terminée**</span><span class="sxs-lookup"><span data-stu-id="3e239-229"><span id="MPNOTIFY_SIGUPDATE_INSTALL_COMPLETE"></span><span id="mpnotify_sigupdate_install_complete"></span>**MPNOTIFY\_SIGUPDATE\_INSTALL\_COMPLETE**</span></span>
</dt> <dd>

<span data-ttu-id="3e239-230">Installation terminée.</span><span class="sxs-lookup"><span data-stu-id="3e239-230">Installation complete.</span></span>

</dd> <dt>

<span data-ttu-id="3e239-231"><span id="MPNOTIFY_SIGUPDATE_REBOOT_REQUIRED"></span><span id="mpnotify_sigupdate_reboot_required"></span>**redémarrage de MPNOTIFY \_ SIGUPDATE \_ \_ requis**</span><span class="sxs-lookup"><span data-stu-id="3e239-231"><span id="MPNOTIFY_SIGUPDATE_REBOOT_REQUIRED"></span><span id="mpnotify_sigupdate_reboot_required"></span>**MPNOTIFY\_SIGUPDATE\_REBOOT\_REQUIRED**</span></span>
</dt> <dd>

<span data-ttu-id="3e239-232">La mise à jour nécessite un redémarrage.</span><span class="sxs-lookup"><span data-stu-id="3e239-232">Update requires reboot.</span></span>

</dd> <dt>

<span data-ttu-id="3e239-233"><span id="MPNOTIFY_SIGUPDATE_REQUEST_PROCESSED"></span><span id="mpnotify_sigupdate_request_processed"></span>**\_requête MPNOTIFY \_ SIGUPDATE \_ traitée**</span><span class="sxs-lookup"><span data-stu-id="3e239-233"><span id="MPNOTIFY_SIGUPDATE_REQUEST_PROCESSED"></span><span id="mpnotify_sigupdate_request_processed"></span>**MPNOTIFY\_SIGUPDATE\_REQUEST\_PROCESSED**</span></span>
</dt> <dd>

<span data-ttu-id="3e239-234">Le service a traité une demande de mise à jour de signature.</span><span class="sxs-lookup"><span data-stu-id="3e239-234">Service processed a signature update request.</span></span> <span data-ttu-id="3e239-235">L’échec ou la réussite est indiqué par **HRESULT** dans les données de rappel.</span><span class="sxs-lookup"><span data-stu-id="3e239-235">Failure or success is indicated by **hResult** in the callback data.</span></span>

</dd> <dt>

<span data-ttu-id="3e239-236"><span id="MPNOTIFY_SIGUPDATE_COMPLETE"></span><span id="mpnotify_sigupdate_complete"></span>**MPNOTIFY \_ SIGUPDATE \_ terminé**</span><span class="sxs-lookup"><span data-stu-id="3e239-236"><span id="MPNOTIFY_SIGUPDATE_COMPLETE"></span><span id="mpnotify_sigupdate_complete"></span>**MPNOTIFY\_SIGUPDATE\_COMPLETE**</span></span>
</dt> <dd>

<span data-ttu-id="3e239-237">Mise à jour terminée.</span><span class="sxs-lookup"><span data-stu-id="3e239-237">Update complete.</span></span> <span data-ttu-id="3e239-238">**S \_ L’État FALSe** indique qu’aucune mise à jour n’était nécessaire.</span><span class="sxs-lookup"><span data-stu-id="3e239-238">**S\_FALSE** status indicates that no updates were needed.</span></span>

</dd> <dt>

<span data-ttu-id="3e239-239"><span id="MPNOTIFY_SAMPLE_START"></span><span id="mpnotify_sample_start"></span>**MPNOTIFY \_ exemple de \_ démarrage**</span><span class="sxs-lookup"><span data-stu-id="3e239-239"><span id="MPNOTIFY_SAMPLE_START"></span><span id="mpnotify_sample_start"></span>**MPNOTIFY\_SAMPLE\_START**</span></span>
</dt> <dd>

<span data-ttu-id="3e239-240">L’exemple de soumission a démarré.</span><span class="sxs-lookup"><span data-stu-id="3e239-240">Sample submission started.</span></span>

</dd> <dt>

<span data-ttu-id="3e239-241"><span id="MPNOTIFY_SAMPLE_COMPLETE"></span><span id="mpnotify_sample_complete"></span>**\_exemple MPNOTIFY \_ terminé**</span><span class="sxs-lookup"><span data-stu-id="3e239-241"><span id="MPNOTIFY_SAMPLE_COMPLETE"></span><span id="mpnotify_sample_complete"></span>**MPNOTIFY\_SAMPLE\_COMPLETE**</span></span>
</dt> <dd>

<span data-ttu-id="3e239-242">Exemple d’envoi terminé.</span><span class="sxs-lookup"><span data-stu-id="3e239-242">Sample submission completed.</span></span>

</dd> <dt>

<span data-ttu-id="3e239-243"><span id="MPNOTIFY_SAMPLE_ITEM_START"></span><span id="mpnotify_sample_item_start"></span>**début de l' \_ exemple d' \_ élément MPNOTIFY \_**</span><span class="sxs-lookup"><span data-stu-id="3e239-243"><span id="MPNOTIFY_SAMPLE_ITEM_START"></span><span id="mpnotify_sample_item_start"></span>**MPNOTIFY\_SAMPLE\_ITEM\_START**</span></span>
</dt> <dd>

<span data-ttu-id="3e239-244">L’exemple d’envoi d’un élément spécifique a démarré.</span><span class="sxs-lookup"><span data-stu-id="3e239-244">Specific sample item submission started.</span></span> <span data-ttu-id="3e239-245">Un exemple d’index d’élément est disponible dans [**MPSAMPLE \_ Data**](mpsample-data.md).</span><span class="sxs-lookup"><span data-stu-id="3e239-245">Sample item index is available in [**MPSAMPLE\_DATA**](mpsample-data.md).</span></span>

</dd> <dt>

<span data-ttu-id="3e239-246"><span id="MPNOTIFY_SAMPLE_ITEM_SUCCEEDED"></span><span id="mpnotify_sample_item_succeeded"></span>**\_exemple d' \_ élément MPNOTIFY \_ réussi**</span><span class="sxs-lookup"><span data-stu-id="3e239-246"><span id="MPNOTIFY_SAMPLE_ITEM_SUCCEEDED"></span><span id="mpnotify_sample_item_succeeded"></span>**MPNOTIFY\_SAMPLE\_ITEM\_SUCCEEDED**</span></span>
</dt> <dd>

<span data-ttu-id="3e239-247">L’envoi d’un élément d’exemple spécifique a réussi.</span><span class="sxs-lookup"><span data-stu-id="3e239-247">Specific sample item submission succeeded.</span></span>

</dd> <dt>

<span data-ttu-id="3e239-248"><span id="MPNOTIFY_SAMPLE_ITEM_FAILED"></span><span id="mpnotify_sample_item_failed"></span>**échec de l' \_ exemple d' \_ élément MPNOTIFY \_**</span><span class="sxs-lookup"><span data-stu-id="3e239-248"><span id="MPNOTIFY_SAMPLE_ITEM_FAILED"></span><span id="mpnotify_sample_item_failed"></span>**MPNOTIFY\_SAMPLE\_ITEM\_FAILED**</span></span>
</dt> <dd>

<span data-ttu-id="3e239-249">Échec de l’envoi d’un exemple d’élément spécifique.</span><span class="sxs-lookup"><span data-stu-id="3e239-249">Specific sample item submission failed.</span></span> <span data-ttu-id="3e239-250">Le code d’erreur est disponible dans les [**\_ données MPCALLBACK**](mpcallback-data.md).</span><span class="sxs-lookup"><span data-stu-id="3e239-250">Error code is available in [**MPCALLBACK\_DATA**](mpcallback-data.md).</span></span>

</dd> <dt>

<span data-ttu-id="3e239-251"><span id="MPNOTIFY_RESERVED_DATA"></span><span id="mpnotify_reserved_data"></span>**\_données réservées MPNOTIFY \_**</span><span class="sxs-lookup"><span data-stu-id="3e239-251"><span id="MPNOTIFY_RESERVED_DATA"></span><span id="mpnotify_reserved_data"></span>**MPNOTIFY\_RESERVED\_DATA**</span></span>
</dt> <dd>

<span data-ttu-id="3e239-252">Données réservées internes.</span><span class="sxs-lookup"><span data-stu-id="3e239-252">Internal reserved data.</span></span>

</dd> <dt>

<span data-ttu-id="3e239-253"><span id="MPNOTIFY_FASTPATH_SIG_ADDED"></span><span id="mpnotify_fastpath_sig_added"></span>**MPNOTIFY \_ FASTPATH \_ SIG \_ ajouté**</span><span class="sxs-lookup"><span data-stu-id="3e239-253"><span id="MPNOTIFY_FASTPATH_SIG_ADDED"></span><span id="mpnotify_fastpath_sig_added"></span>**MPNOTIFY\_FASTPATH\_SIG\_ADDED**</span></span>
</dt> <dd>

<span data-ttu-id="3e239-254">Une signature FastPath a ajouté ou désactivé une signature.</span><span class="sxs-lookup"><span data-stu-id="3e239-254">A Fastpath signature has either added or disabled a signature.</span></span>

</dd> <dt>

<span data-ttu-id="3e239-255"><span id="MPNOTIFY_FASTPATH_SIG_REMOVED"></span><span id="mpnotify_fastpath_sig_removed"></span>**MPNOTIFY \_ FASTPATH \_ SIG \_ supprimé**</span><span class="sxs-lookup"><span data-stu-id="3e239-255"><span id="MPNOTIFY_FASTPATH_SIG_REMOVED"></span><span id="mpnotify_fastpath_sig_removed"></span>**MPNOTIFY\_FASTPATH\_SIG\_REMOVED**</span></span>
</dt> <dd>

<span data-ttu-id="3e239-256">Une signature de FastPath a été supprimée.</span><span class="sxs-lookup"><span data-stu-id="3e239-256">A FastPath signature has been removed.</span></span>

</dd> <dt>

<span data-ttu-id="3e239-257"><span id="MPNOTIFY_NIS_PRIVATE"></span><span id="mpnotify_nis_private"></span>**MPNOTIFY \_ NIS \_ privé**</span><span class="sxs-lookup"><span data-stu-id="3e239-257"><span id="MPNOTIFY_NIS_PRIVATE"></span><span id="mpnotify_nis_private"></span>**MPNOTIFY\_NIS\_PRIVATE**</span></span>
</dt> <dd>

<span data-ttu-id="3e239-258">Notifications en vertu privé NIS.</span><span class="sxs-lookup"><span data-stu-id="3e239-258">NIS private notifcations.</span></span> <span data-ttu-id="3e239-259">Aucun partenaire ne doit s’inscrire pour cela.</span><span class="sxs-lookup"><span data-stu-id="3e239-259">No partners should register for this.</span></span>

</dd> <dt>

<span data-ttu-id="3e239-260"><span id="MPNOTIFY_HEALTH_CHANGE"></span><span id="mpnotify_health_change"></span>**MPNOTIFY \_ modification de l’intégrité \_**</span><span class="sxs-lookup"><span data-stu-id="3e239-260"><span id="MPNOTIFY_HEALTH_CHANGE"></span><span id="mpnotify_health_change"></span>**MPNOTIFY\_HEALTH\_CHANGE**</span></span>
</dt> <dd>

<span data-ttu-id="3e239-261">Le service AM est entré dans un nouvel État.</span><span class="sxs-lookup"><span data-stu-id="3e239-261">The AM service has entered a new state.</span></span>

</dd> <dt>

<span data-ttu-id="3e239-262"><span id="MPNOTIFY_HEALTH_RECOVERY"></span><span id="mpnotify_health_recovery"></span>**\_récupération d’intégrité MPNOTIFY \_**</span><span class="sxs-lookup"><span data-stu-id="3e239-262"><span id="MPNOTIFY_HEALTH_RECOVERY"></span><span id="mpnotify_health_recovery"></span>**MPNOTIFY\_HEALTH\_RECOVERY**</span></span>
</dt> <dd>

<span data-ttu-id="3e239-263">Le service AM a récupéré d’un État.</span><span class="sxs-lookup"><span data-stu-id="3e239-263">The AM service has recovered from a state.</span></span>

</dd> <dt>

<span data-ttu-id="3e239-264"><span id="MPNOTIFY_HEALTH_START"></span><span id="mpnotify_health_start"></span>**démarrage de l’intégrité de MPNOTIFY \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3e239-264"><span id="MPNOTIFY_HEALTH_START"></span><span id="mpnotify_health_start"></span>**MPNOTIFY\_HEALTH\_START**</span></span>
</dt> <dd>

<span data-ttu-id="3e239-265">Le service AM a initialisé l’intégrité du système.</span><span class="sxs-lookup"><span data-stu-id="3e239-265">The AM service has initialized the health of the system.</span></span>

</dd> <dt>

<span data-ttu-id="3e239-266"><span id="MPNOTIFY_ENDOFLIFE_CHANGE"></span><span id="mpnotify_endoflife_change"></span>**modification de MPNOTIFY \_ ENDOFLIFE \_**</span><span class="sxs-lookup"><span data-stu-id="3e239-266"><span id="MPNOTIFY_ENDOFLIFE_CHANGE"></span><span id="mpnotify_endoflife_change"></span>**MPNOTIFY\_ENDOFLIFE\_CHANGE**</span></span>
</dt> <dd>

<span data-ttu-id="3e239-267">Les dates d’expiration de la « fin de vie » pour le service AM ont changé.</span><span class="sxs-lookup"><span data-stu-id="3e239-267">The "End Of Life" expiry dates for the AM service have changed.</span></span>

</dd> <dt>

<span data-ttu-id="3e239-268"><span id="MPNOTIFY_MALWARETOAST_DATA"></span><span id="mpnotify_malwaretoast_data"></span>**MPNOTIFY \_ MALWARETOAST \_ données**</span><span class="sxs-lookup"><span data-stu-id="3e239-268"><span id="MPNOTIFY_MALWARETOAST_DATA"></span><span id="mpnotify_malwaretoast_data"></span>**MPNOTIFY\_MALWARETOAST\_DATA**</span></span>
</dt> <dd>

<span data-ttu-id="3e239-269">Le service AM a rencontré un programme malveillant qui a peut-être provoqué une modification des paramètres critiques sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="3e239-269">The AM service has encountered malware that might have caused critical settings change in the machine.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3e239-270">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3e239-270">Requirements</span></span>



| <span data-ttu-id="3e239-271">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3e239-271">Requirement</span></span> | <span data-ttu-id="3e239-272">Valeur</span><span class="sxs-lookup"><span data-stu-id="3e239-272">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3e239-273">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3e239-273">Minimum supported client</span></span><br/> | <span data-ttu-id="3e239-274">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3e239-274">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="3e239-275">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3e239-275">Minimum supported server</span></span><br/> | <span data-ttu-id="3e239-276">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3e239-276">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3e239-277">En-tête</span><span class="sxs-lookup"><span data-stu-id="3e239-277">Header</span></span><br/>                   | <dl> <span data-ttu-id="3e239-278"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="3e239-278"><dt>MpClient.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3e239-279">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3e239-279">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e239-280">**MpManagerStatusQueryEx**</span><span class="sxs-lookup"><span data-stu-id="3e239-280">**MpManagerStatusQueryEx**</span></span>](mpmanagerstatusqueryex.md)
</dt> <dt>

[<span data-ttu-id="3e239-281">**\_données MPCALLBACK**</span><span class="sxs-lookup"><span data-stu-id="3e239-281">**MPCALLBACK\_DATA**</span></span>](mpcallback-data.md)
</dt> <dt>

[<span data-ttu-id="3e239-282">**\_données MPSAMPLE**</span><span class="sxs-lookup"><span data-stu-id="3e239-282">**MPSAMPLE\_DATA**</span></span>](mpsample-data.md)
</dt> </dl>

 

 





