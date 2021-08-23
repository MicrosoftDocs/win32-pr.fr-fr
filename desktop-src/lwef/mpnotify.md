---
title: Énumération MPNOTIFY (MpClient. h)
description: Notifications de rappel possibles.
ms.assetid: CCD0CD89-2C6E-453F-9437-E6ED87AD9F29
keywords:
- MPNOTIFY, énumération des fonctionnalités d’environnement Windows héritées
- PMPNOTIFY, pointeur d’énumération de l’héritage Windows fonctionnalités d’environnement
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
ms.openlocfilehash: ed62a9f868aa39cbc0cfc7702afc99849005a22106892696eca857ffb20673af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118747787"
---
# <a name="mpnotify-enumeration"></a>Énumération MPNOTIFY

Notifications de rappel possibles.

## <a name="syntax"></a>Syntaxe


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



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="MPNOTIFY_NONE"></span><span id="mpnotify_none"></span>**MPNOTIFY \_ aucun**
</dt> <dd></dd> <dt>

<span id="MPNOTIFY_CALL_START"></span><span id="mpnotify_call_start"></span>**début de l' \_ appel MPNOTIFY \_**
</dt> <dd>

Début de l’appel de notification.

</dd> <dt>

<span id="MPNOTIFY_CALL_COMPLETE"></span><span id="mpnotify_call_complete"></span>**\_appel MPNOTIFY \_ terminé**
</dt> <dd>

Appel de notification terminé.

</dd> <dt>

<span id="MPNOTIFY_INTERNAL_FAILURE"></span><span id="mpnotify_internal_failure"></span>**\_échec interne \_ MPNOTIFY**
</dt> <dd>

Échec interne générique.

</dd> <dt>

<span id="MPNOTIFY_STATUS_SERVICE_START"></span><span id="mpnotify_status_service_start"></span>**\_démarrage du \_ service d’État MPNOTIFY \_**
</dt> <dd>

Le service de protection contre les programmes malveillants a démarré.

</dd> <dt>

<span id="MPNOTIFY_STATUS_SERVICE_RUNNING"></span><span id="mpnotify_status_service_running"></span>**\_service d’État MPNOTIFY \_ \_ en cours d’exécution**
</dt> <dd>

Le service protection contre les programmes malveillants est en cours d’exécution.

</dd> <dt>

<span id="MPNOTIFY_STATUS_SERVICE_STOP"></span><span id="mpnotify_status_service_stop"></span>**\_arrêt du \_ service d’État MPNOTIFY \_**
</dt> <dd>

Le service de protection contre les programmes malveillants s’est arrêté.

</dd> <dt>

<span id="MPNOTIFY_STATUS_COMPONENT"></span><span id="mpnotify_status_component"></span>**\_composant d’État MPNOTIFY \_**
</dt> <dd>

État d’activation/de désactivation de composant particulier.

</dd> <dt>

<span id="MPNOTIFY_STATUS_CHANGE"></span><span id="mpnotify_status_change"></span>**modification de l’état de MPNOTIFY \_ \_**
</dt> <dd>

L’état général du produit a changé. Appelez [**MpManagerStatusQueryEx**](mpmanagerstatusqueryex.md) pour obtenir l’état actuel.

</dd> <dt>

<span id="MPNOTIFY_STATUS_COMPONENT_CONFIGURATION"></span><span id="mpnotify_status_component_configuration"></span>**\_configuration du \_ composant d’État MPNOTIFY \_**
</dt> <dd>

Une configuration a été modifiée pour un composant particulier.

</dd> <dt>

<span id="MPNOTIFY_STATUS_EXPIRATION_CHANGE"></span><span id="mpnotify_status_expiration_change"></span>**\_ \_ modification d’expiration de l’État MPNOTIFY \_**
</dt> <dd>

L’état d’expiration du produit a changé.

</dd> <dt>

<span id="MPNOTIFY_STATUS_OFFLINE_SCAN_CHANGE"></span><span id="mpnotify_status_offline_scan_change"></span>**modification de l' \_ État d' \_ analyse hors connexion \_ \_ MPNOTIFY**
</dt> <dd>

L’état de l’analyse hors connexion requis a changé.

</dd> <dt>

<span id="MPNOTIFY_SCAN_START"></span><span id="mpnotify_scan_start"></span>**début de l' \_ analyse MPNOTIFY \_**
</dt> <dd>

Début de l’analyse.

</dd> <dt>

<span id="MPNOTIFY_SCAN_PAUSED"></span><span id="mpnotify_scan_paused"></span>**\_analyse MPNOTIFY \_ suspendue**
</dt> <dd>

Analyse suspendue.

</dd> <dt>

<span id="MPNOTIFY_SCAN_RESUMED"></span><span id="mpnotify_scan_resumed"></span>**\_analyse MPNOTIFY \_ reprise**
</dt> <dd>

analyse reprise.

</dd> <dt>

<span id="MPNOTIFY_SCAN_CANCEL"></span><span id="mpnotify_scan_cancel"></span>**annulation de l' \_ analyse MPNOTIFY \_**
</dt> <dd>

Analyse annulée.

</dd> <dt>

<span id="MPNOTIFY_SCAN_COMPLETE"></span><span id="mpnotify_scan_complete"></span>**\_analyse MPNOTIFY \_ terminée**
</dt> <dd>

Analyse terminée.

</dd> <dt>

<span id="MPNOTIFY_SCAN_PROGRESS"></span><span id="mpnotify_scan_progress"></span>**progression de l' \_ analyse MPNOTIFY \_**
</dt> <dd>

Notification de progression pour la ressource spécifique en cours d’analyse.

</dd> <dt>

<span id="MPNOTIFY_SCAN_ERROR"></span><span id="mpnotify_scan_error"></span>**\_erreur d’analyse MPNOTIFY \_**
</dt> <dd>

Échec de l’analyse d’une ressource particulière. L’analyse continuera toujours.

</dd> <dt>

<span id="MPNOTIFY_SCAN_INFECTED"></span><span id="mpnotify_scan_infected"></span>**\_analyse MPNOTIFY \_ infectée**
</dt> <dd>

L’analyse a trouvé une ressource infectée.

</dd> <dt>

<span id="MPNOTIFY_SCAN_MEMORYSTART"></span><span id="mpnotify_scan_memorystart"></span>**MPNOTIFY \_ Scan \_ MEMORYSTART**
</dt> <dd>

La progression de l’analyse pour notifier la mémoire de l’analyse du système a démarré.

</dd> <dt>

<span id="MPNOTIFY_SCAN_MEMORYCOMPLETE"></span><span id="mpnotify_scan_memorycomplete"></span>**MPNOTIFY \_ Scan \_ MEMORYCOMPLETE**
</dt> <dd>

La progression de l’analyse pour notifier la mémoire de l’analyse du système est terminée.

</dd> <dt>

<span id="MPNOTIFY_SCAN_SFC_BUILD_START"></span><span id="mpnotify_scan_sfc_build_start"></span>**démarrage de la \_ génération MPNOTIFY Scan \_ SFC \_ \_**
</dt> <dd>

Progression de l’analyse pour notifier la partie de build SFC a démarré.

</dd> <dt>

<span id="MPNOTIFY_SCAN_SFC_BUILD_COMPLETE"></span><span id="mpnotify_scan_sfc_build_complete"></span>**\_Build SFC d’analyse MPNOTIFY \_ \_ \_ terminée**
</dt> <dd>

Progression de l’analyse pour notifier la partie de build SFC terminée.

</dd> <dt>

<span id="MPNOTIFY_SCAN_FASTPATH_START"></span><span id="mpnotify_scan_fastpath_start"></span>**démarrage de l' \_ analyse MPNOTIFY \_ FASTPATH \_**
</dt> <dd>

L’analyse FastPath SpyNet a commencé.

</dd> <dt>

<span id="MPNOTIFY_SCAN_FASTPATH_COMPLETE"></span><span id="mpnotify_scan_fastpath_complete"></span>**\_FASTPATH d’analyse MPNOTIFY \_ \_ terminé**
</dt> <dd>

L’analyse FastPath SpyNet est terminée.

</dd> <dt>

<span id="MPNOTIFY_SCAN_FASTPATH_PROGRESS"></span><span id="mpnotify_scan_fastpath_progress"></span>**progression de l' \_ analyse MPNOTIFY \_ FASTPATH \_**
</dt> <dd>

Notification de progression pour les analyses FastPath, utilisée en interne et convertie en **\_ \_ progression de l’analyse MPNOTIFY** pour External.

</dd> <dt>

<span id="MPNOTIFY_CLEAN_START"></span><span id="mpnotify_clean_start"></span>**\_démarrage propre \_ MPNOTIFY**
</dt> <dd>

Nettoyage démarré.

</dd> <dt>

<span id="MPNOTIFY_CLEAN_COMPLETE"></span><span id="mpnotify_clean_complete"></span>**MPNOTIFY \_ nettoyage \_ terminé**
</dt> <dd>

Nettoyage terminé.

</dd> <dt>

<span id="MPNOTIFY_CLEAN_RESTOREPOINT_START"></span><span id="mpnotify_clean_restorepoint_start"></span>**MPNOTIFY \_ Clean \_ RESTOREPOINT \_ Start**
</dt> <dd>

Début de la création d’un point de restauration système.

</dd> <dt>

<span id="MPNOTIFY_CLEAN_RESTOREPOINT_SUCCEEDED"></span><span id="mpnotify_clean_restorepoint_succeeded"></span>**MPNOTIFY \_ Clean \_ RESTOREPOINT \_ réussi**
</dt> <dd>

Point de restauration système créé avec succès.

</dd> <dt>

<span id="MPNOTIFY_CLEAN_RESTOREPOINT_FAILED"></span><span id="mpnotify_clean_restorepoint_failed"></span>**\_échec du nettoyage du \_ RESTOREPOINT MPNOTIFY \_**
</dt> <dd>

Échec de la création du point de restauration du système.

</dd> <dt>

<span id="MPNOTIFY_CLEAN_THREAT_START"></span><span id="mpnotify_clean_threat_start"></span>**\_Démarrer le nettoyage des \_ menaces MPNOTIFY \_**
</dt> <dd>

Le nettoyage est lancé pour une menace particulière.

</dd> <dt>

<span id="MPNOTIFY_CLEAN_THREAT_SUCCEEDED"></span><span id="mpnotify_clean_threat_succeeded"></span>**MPNOTIFY \_ Clean \_ Threat \_ a réussi**
</dt> <dd>

Le nettoyage a réussi pour une menace particulière.

</dd> <dt>

<span id="MPNOTIFY_CLEAN_THREAT_FAILED"></span><span id="mpnotify_clean_threat_failed"></span>**échec du nettoyage de la \_ \_ menace MPNOTIFY \_**
</dt> <dd>

Le nettoyage a échoué pour une menace particulière. **Erreur \_ Le code d’erreur « menace de point de gestion \_ \_ \_ introuvable** » indique que la menace n’a pas été trouvée (et qu’elle n’a pas pu être nettoyée).

</dd> <dt>

<span id="MPNOTIFY_CLEAN_RESOURCE_SUCCEEDED"></span><span id="mpnotify_clean_resource_succeeded"></span>**\_ressource de nettoyage MPNOTIFY \_ \_ réussie**
</dt> <dd>

Le nettoyage a réussi pour une ressource particulière.

</dd> <dt>

<span id="MPNOTIFY_CLEAN_RESOURCE_FAILED"></span><span id="mpnotify_clean_resource_failed"></span>**échec du nettoyage de la \_ \_ ressource MPNOTIFY \_**
</dt> <dd>

Le nettoyage a échoué pour une ressource particulière.

</dd> <dt>

<span id="MPNOTIFY_CLEAN_THREAT_COMPLETE"></span><span id="mpnotify_clean_threat_complete"></span>**nettoyage de la \_ \_ menace MPNOTIFY \_ terminé**
</dt> <dd>

Le nettoyage s’est terminé pour une menace particulière.

</dd> <dt>

<span id="MPNOTIFY_PRECHECK_START"></span><span id="mpnotify_precheck_start"></span>**démarrage de la \_ PRÉVÉRIFICATION MPNOTIFY \_**
</dt> <dd>

Nettoyage de la prévérification démarré.

</dd> <dt>

<span id="MPNOTIFY_PRECHECK_COMPLETE"></span><span id="mpnotify_precheck_complete"></span>**prévérification de MPNOTIFY \_ \_ terminée**
</dt> <dd>

La prévérification du nettoyage est terminée.

</dd> <dt>

<span id="MPNOTIFY_PRECHECK_RESOURCE_BLOCKED"></span><span id="mpnotify_precheck_resource_blocked"></span>**\_ressource de PRÉVÉRIFICATION MPNOTIFY \_ \_ bloquée**
</dt> <dd>

La prévérification propre a détecté une ressource bloquée.

</dd> <dt>

<span id="MPNOTIFY_THREAT_DETECTED"></span><span id="mpnotify_threat_detected"></span>**\_menace MPNOTIFY \_ détectée**
</dt> <dd>

Nouvelle menace détectée dans le système.

</dd> <dt>

<span id="MPNOTIFY_THREAT_MODIFIED"></span><span id="mpnotify_threat_modified"></span>**\_menace MPNOTIFY \_ modifiée**
</dt> <dd>

Informations sur les menaces modifiées. Par exemple, une nouvelle ressource a été ajoutée.

</dd> <dt>

<span id="MPNOTIFY_THREAT_CLEAN_SUCCEEDED"></span><span id="mpnotify_threat_clean_succeeded"></span>**le \_ nettoyage de la menace MPNOTIFY \_ \_ a réussi**
</dt> <dd>

Action de nettoyage réussie pour une menace.

</dd> <dt>

<span id="MPNOTIFY_THREAT_CLEAN_FAILED"></span><span id="mpnotify_threat_clean_failed"></span>**échec du nettoyage de la \_ menace MPNOTIFY \_ \_**
</dt> <dd>

Échec de l’action de nettoyage pour une menace. **Erreur \_ Le code d’erreur « menace de point de gestion \_ \_ \_ introuvable** » indique que la menace n’a pas été trouvée (et qu’elle n’a pas pu être nettoyée).

</dd> <dt>

<span id="MPNOTIFY_THREAT_ABANDONED"></span><span id="mpnotify_threat_abandoned"></span>**\_menace MPNOTIFY \_ abandonnée**
</dt> <dd>

Aucune correction n’a eu lieu avant l’arrêt du service.

</dd> <dt>

<span id="MPNOTIFY_THREAT_CLEAN_EVENT_START"></span><span id="mpnotify_threat_clean_event_start"></span>**démarrage de l’événement de nettoyage des \_ menaces MPNOTIFY \_ \_ \_**
</dt> <dd>

Une action de nettoyage a été démarrée.

</dd> <dt>

<span id="MPNOTIFY_THREAT_CLEAN_EVENT_COMPLETE"></span><span id="mpnotify_threat_clean_event_complete"></span>**événement de nettoyage de la \_ menace MPNOTIFY \_ \_ \_ terminé**
</dt> <dd>

Une action de nettoyage est terminée.

</dd> <dt>

<span id="MPNOTIFY_SIGUPDATE_START"></span><span id="mpnotify_sigupdate_start"></span>**MPNOTIFY \_ SIGUPDATE \_ Start**
</dt> <dd>

Mise à jour de signature démarrée.

</dd> <dt>

<span id="MPNOTIFY_SIGUPDATE_SEARCH_START"></span><span id="mpnotify_sigupdate_search_start"></span>**début de la \_ recherche MPNOTIFY SIGUPDATE \_ \_**
</dt> <dd>

Recherche des mises à jour démarrées.

</dd> <dt>

<span id="MPNOTIFY_SIGUPDATE_SEARCH_COMPLETE"></span><span id="mpnotify_sigupdate_search_complete"></span>**recherche de MPNOTIFY \_ SIGUPDATE \_ \_ terminée**
</dt> <dd>

Recherche des mises à jour terminées.

</dd> <dt>

<span id="MPNOTIFY_SIGUPDATE_SOFTWARE_UPDATE_AVAILABLE"></span><span id="mpnotify_sigupdate_software_update_available"></span>**\_ \_ \_ mise à jour logicielle MPNOTIFY SIGUPDATE \_ disponible**
</dt> <dd>

Mise à jour logicielle disponible.

</dd> <dt>

<span id="MPNOTIFY_SIGUPDATE_DOWNLOAD_START"></span><span id="mpnotify_sigupdate_download_start"></span>**démarrage du téléchargement de MPNOTIFY \_ SIGUPDATE \_ \_**
</dt> <dd>

Téléchargement démarré.

</dd> <dt>

<span id="MPNOTIFY_SIGUPDATE_DOWNLOAD_PROGRESS"></span><span id="mpnotify_sigupdate_download_progress"></span>**progression du téléchargement de MPNOTIFY \_ SIGUPDATE \_ \_**
</dt> <dd>

Téléchargement en cours. Les données de rappel contiennent la progression.

</dd> <dt>

<span id="MPNOTIFY_SIGUPDATE_DOWNLOAD_COMPLETE"></span><span id="mpnotify_sigupdate_download_complete"></span>**Téléchargement de MPNOTIFY \_ SIGUPDATE \_ \_ terminé**
</dt> <dd>

Téléchargement terminé.

</dd> <dt>

<span id="MPNOTIFY_SIGUPDATE_INSTALL_START"></span><span id="mpnotify_sigupdate_install_start"></span>**démarrage de l’installation de MPNOTIFY \_ SIGUPDATE \_ \_**
</dt> <dd>

Installation démarrée.

</dd> <dt>

<span id="MPNOTIFY_SIGUPDATE_INSTALL_PROGRESS"></span><span id="mpnotify_sigupdate_install_progress"></span>**progression de l’installation de MPNOTIFY \_ SIGUPDATE \_ \_**
</dt> <dd>

Installation en cours. Les données de rappel contiennent la progression.

</dd> <dt>

<span id="MPNOTIFY_SIGUPDATE_INSTALL_COMPLETE"></span><span id="mpnotify_sigupdate_install_complete"></span>**installation de MPNOTIFY \_ SIGUPDATE \_ \_ terminée**
</dt> <dd>

Installation terminée.

</dd> <dt>

<span id="MPNOTIFY_SIGUPDATE_REBOOT_REQUIRED"></span><span id="mpnotify_sigupdate_reboot_required"></span>**redémarrage de MPNOTIFY \_ SIGUPDATE \_ \_ requis**
</dt> <dd>

La mise à jour nécessite un redémarrage.

</dd> <dt>

<span id="MPNOTIFY_SIGUPDATE_REQUEST_PROCESSED"></span><span id="mpnotify_sigupdate_request_processed"></span>**\_requête MPNOTIFY \_ SIGUPDATE \_ traitée**
</dt> <dd>

Le service a traité une demande de mise à jour de signature. L’échec ou la réussite est indiqué par **HRESULT** dans les données de rappel.

</dd> <dt>

<span id="MPNOTIFY_SIGUPDATE_COMPLETE"></span><span id="mpnotify_sigupdate_complete"></span>**MPNOTIFY \_ SIGUPDATE \_ terminé**
</dt> <dd>

Mise à jour terminée. **S \_ L’État FALSe** indique qu’aucune mise à jour n’était nécessaire.

</dd> <dt>

<span id="MPNOTIFY_SAMPLE_START"></span><span id="mpnotify_sample_start"></span>**MPNOTIFY \_ exemple de \_ démarrage**
</dt> <dd>

L’exemple de soumission a démarré.

</dd> <dt>

<span id="MPNOTIFY_SAMPLE_COMPLETE"></span><span id="mpnotify_sample_complete"></span>**\_exemple MPNOTIFY \_ terminé**
</dt> <dd>

Exemple d’envoi terminé.

</dd> <dt>

<span id="MPNOTIFY_SAMPLE_ITEM_START"></span><span id="mpnotify_sample_item_start"></span>**début de l' \_ exemple d' \_ élément MPNOTIFY \_**
</dt> <dd>

L’exemple d’envoi d’un élément spécifique a démarré. Un exemple d’index d’élément est disponible dans [**MPSAMPLE \_ Data**](mpsample-data.md).

</dd> <dt>

<span id="MPNOTIFY_SAMPLE_ITEM_SUCCEEDED"></span><span id="mpnotify_sample_item_succeeded"></span>**\_exemple d' \_ élément MPNOTIFY \_ réussi**
</dt> <dd>

L’envoi d’un élément d’exemple spécifique a réussi.

</dd> <dt>

<span id="MPNOTIFY_SAMPLE_ITEM_FAILED"></span><span id="mpnotify_sample_item_failed"></span>**échec de l' \_ exemple d' \_ élément MPNOTIFY \_**
</dt> <dd>

Échec de l’envoi d’un exemple d’élément spécifique. Le code d’erreur est disponible dans les [**\_ données MPCALLBACK**](mpcallback-data.md).

</dd> <dt>

<span id="MPNOTIFY_RESERVED_DATA"></span><span id="mpnotify_reserved_data"></span>**\_données réservées MPNOTIFY \_**
</dt> <dd>

Données réservées internes.

</dd> <dt>

<span id="MPNOTIFY_FASTPATH_SIG_ADDED"></span><span id="mpnotify_fastpath_sig_added"></span>**MPNOTIFY \_ FASTPATH \_ SIG \_ ajouté**
</dt> <dd>

Une signature FastPath a ajouté ou désactivé une signature.

</dd> <dt>

<span id="MPNOTIFY_FASTPATH_SIG_REMOVED"></span><span id="mpnotify_fastpath_sig_removed"></span>**MPNOTIFY \_ FASTPATH \_ SIG \_ supprimé**
</dt> <dd>

Une signature de FastPath a été supprimée.

</dd> <dt>

<span id="MPNOTIFY_NIS_PRIVATE"></span><span id="mpnotify_nis_private"></span>**MPNOTIFY \_ NIS \_ privé**
</dt> <dd>

Notifications en vertu privé NIS. Aucun partenaire ne doit s’inscrire pour cela.

</dd> <dt>

<span id="MPNOTIFY_HEALTH_CHANGE"></span><span id="mpnotify_health_change"></span>**MPNOTIFY \_ modification de l’intégrité \_**
</dt> <dd>

Le service AM est entré dans un nouvel État.

</dd> <dt>

<span id="MPNOTIFY_HEALTH_RECOVERY"></span><span id="mpnotify_health_recovery"></span>**\_récupération d’intégrité MPNOTIFY \_**
</dt> <dd>

Le service AM a récupéré d’un État.

</dd> <dt>

<span id="MPNOTIFY_HEALTH_START"></span><span id="mpnotify_health_start"></span>**démarrage de l’intégrité de MPNOTIFY \_ \_**
</dt> <dd>

Le service AM a initialisé l’intégrité du système.

</dd> <dt>

<span id="MPNOTIFY_ENDOFLIFE_CHANGE"></span><span id="mpnotify_endoflife_change"></span>**modification de MPNOTIFY \_ ENDOFLIFE \_**
</dt> <dd>

Les dates d’expiration de la « fin de vie » pour le service AM ont changé.

</dd> <dt>

<span id="MPNOTIFY_MALWARETOAST_DATA"></span><span id="mpnotify_malwaretoast_data"></span>**MPNOTIFY \_ MALWARETOAST \_ données**
</dt> <dd>

Le service AM a rencontré un programme malveillant qui a peut-être provoqué une modification des paramètres critiques sur l’ordinateur.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau uniquement\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MpManagerStatusQueryEx**](mpmanagerstatusqueryex.md)
</dt> <dt>

[**\_données MPCALLBACK**](mpcallback-data.md)
</dt> <dt>

[**\_données MPSAMPLE**](mpsample-data.md)
</dt> </dl>

 

 





