---
title: Valeurs retournées
description: Les constantes ci-dessous représentent des valeurs de retour que l’optimisation de remise (DO) génère et des valeurs de retour HTTP qui EFFECTUEnt des captures.
ms.assetid: 68AC4581-C748-49AB-A588-15816E534756
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e16dc435fa22268d92c4403709a5444b1b87e325d66429da853844fd7f836b40
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118101850"
---
# <a name="do-return-values"></a>Valeurs retournées

Les constantes ci-dessous représentent des valeurs de retour que l’optimisation de remise (DO) génère et des valeurs de retour HTTP qui EFFECTUEnt des captures. toutes les autres valeurs de retour que vous pouvez recevoir sont COM, RPC, ou converties Windows les valeurs de retour (utilisez la macro [HRESULT_FROM_WIN32](/windows/win32/api/winerror/nf-winerror-hresult_from_win32) pour convertir les valeurs de retour Windows en valeurs HRESULT).

<dl> <dt>

<span id="DO_E_NO_SERVICE__0x80d01001_"></span><span id="do_e_no_service__0x80d01001_"></span><span id="DO_E_NO_SERVICE__0X80D01001_"></span>DO_E_NO_SERVICE (0x80d01001)
</dt> <dd>

L’optimisation de la distribution n’a pas pu fournir le service.

</dd> <dt>

<span id="DO_E_DOWNLOAD_NO_PROGRESS__0x80d02002_"></span><span id="do_e_download_no_progress__0x80d02002_"></span><span id="DO_E_DOWNLOAD_NO_PROGRESS__0X80D02002_"></span>DO_E_DOWNLOAD_NO_PROGRESS (0x80d02002)
</dt> <dd>

Le téléchargement d’un fichier n’a vu aucune progression au cours de la période définie.

</dd> <dt>

<span id="DO_E_JOB_NOT_FOUND__0x80d02003_"></span><span id="do_e_job_not_found__0x80d02003_"></span><span id="DO_E_JOB_NOT_FOUND__0X80D02003_"></span>DO_E_JOB_NOT_FOUND (0x80d02003)
</dt> <dd>

La tâche est introuvable, il attend la présence d’un travail.

</dd> <dt>

<span id="DO_E_JOB_EMPTY__0x80d02004_"></span><span id="do_e_job_empty__0x80d02004_"></span><span id="DO_E_JOB_EMPTY__0X80D02004_"></span>DO_E_JOB_EMPTY (0x80d02004)
</dt> <dd>

Il n’y avait aucun fichier dans le travail, en attendant au moins un fichier.

</dd> <dt>

<span id="DO_E_LOCALPATH_NOT_SET__0x80d0200d_"></span><span id="do_e_localpath_not_set__0x80d0200d_"></span><span id="DO_E_LOCALPATH_NOT_SET__0X80D0200D_"></span>DO_E_LOCALPATH_NOT_SET (0x80d0200d)
</dt> <dd>

Aucun chemin d’accès au fichier local n’est spécifié pour ce téléchargement.

</dd> <dt>

<span id="DO_E_FILE_NOT_AVAILABLE__0x80d02010_"></span><span id="do_e_file_not_available__0x80d02010_"></span><span id="DO_E_FILE_NOT_AVAILABLE__0X80D02010_"></span>DO_E_FILE_NOT_AVAILABLE (0x80d02010)
</dt> <dd>

Aucun fichier n’est disponible, car aucune URL n’a généré une erreur.

</dd> <dt>

<span id="DO_E_UNKNOWN_PROPERTY_ID__0x80d02011_"></span><span id="do_e_unknown_property_id__0x80d02011_"></span><span id="DO_E_UNKNOWN_PROPERTY_ID__0X80D02011_"></span>DO_E_UNKNOWN_PROPERTY_ID (0x80d02011)
</dt> <dd>

SetProperty () ou GetProperty () appelé avec un ID de propriété inconnu.

</dd> <dt>

<span id="DO_E_READ_ONLY_PROPERTY__0x80d02012_"></span><span id="do_e_read_only_property__0x80d02012_"></span><span id="DO_E_READ_ONLY_PROPERTY__0X80D02012_"></span>DO_E_READ_ONLY_PROPERTY (0x80d02012)
</dt> <dd>

Impossible d’appeler SetProperty () sur une propriété en lecture seule.

</dd> <dt>

<span id="DO_E_INVALID_STATE__0x80d02013_"></span><span id="do_e_invalid_state__0x80d02013_"></span><span id="DO_E_INVALID_STATE__0X80D02013_"></span>DO_E_INVALID_STATE (0x80d02013)
</dt> <dd>

L’opération demandée n’est pas autorisée dans l’état actuel du travail. Le travail a peut-être été annulé ou a terminé son transfert.

</dd> <dt>

<span id="DO_E_ERROR_INFORMATION_UNAVAILABLE__0x80d02014_"></span><span id="do_e_error_information_unavailable__0x80d02014_"></span><span id="DO_E_ERROR_INFORMATION_UNAVAILABLE__0X80D02014_"></span>DO_E_ERROR_INFORMATION_UNAVAILABLE (0x80d02014)
</dt> <dd>

Aucune erreur ne s’est produite.

</dd> <dt>

<span id="DO_E_NO_DOWNLOAD_EXTSETTINGS__0x80d03002_"></span><span id="do_e_no_download_extsettings__0x80d03002_"></span><span id="DO_E_NO_DOWNLOAD_EXTSETTINGS__0X80D03002_"></span>DO_E_NO_DOWNLOAD_EXTSETTINGS (0x80d03002)
</dt> <dd>

Le travail de téléchargement n’est pas autorisé en raison des paramètres utilisateur/administrateur.

</dd> <dt>

<span id="DO_E_BLOCKED_BY_COST_TRANSFER_POLICY__0x80d03801_"></span><span id="do_e_blocked_by_cost_transfer_policy__0x80d03801_"></span><span id="DO_E_BLOCKED_BY_COST_TRANSFER_POLICY__0X80D03801_"></span>DO_E_BLOCKED_BY_COST_TRANSFER_POLICY (0x80d03801)
</dt> <dd>

Suspendez le travail en raison de restrictions de stratégie de coût.

</dd> <dt>

<span id="DO_E_BLOCKED_BY_CELLULAR_POLICY__0x80d03803_"></span><span id="do_e_blocked_by_cellular_policy__0x80d03803_"></span><span id="DO_E_BLOCKED_BY_CELLULAR_POLICY__0X80D03803_"></span>DO_E_BLOCKED_BY_CELLULAR_POLICY (0x80d03803)
</dt> <dd>

Suspendez le travail en raison de la détection des restrictions de réseau cellulaire et de stratégie.

</dd> <dt>

<span id="DO_E_BLOCKED_BY_POWER_STATE__0x80d03804_"></span><span id="do_e_blocked_by_power_state__0x80d03804_"></span><span id="DO_E_BLOCKED_BY_POWER_STATE__0X80D03804_"></span>DO_E_BLOCKED_BY_POWER_STATE (0x80d03804)
</dt> <dd>

La tâche a été suspendue en raison de la détection du changement d’état d’alimentation en mode non AC.

</dd> <dt>

<span id="DO_E_BLOCKED_BY_NO_NETWORK__0x80d03805_"></span><span id="do_e_blocked_by_no_network__0x80d03805_"></span><span id="DO_E_BLOCKED_BY_NO_NETWORK__0X80D03805_"></span>DO_E_BLOCKED_BY_NO_NETWORK (0x80d03805)
</dt> <dd>

Interrompez le travail en raison d’une perte de connectivité réseau.

</dd> <dt>

<span id="DO_E_BLOCKED_BY_VPN_POLICY__0x80d03807_"></span><span id="do_e_blocked_by_vpn_policy__0x80d03807_"></span><span id="DO_E_BLOCKED_BY_VPN_POLICY__0X80D03807_"></span>DO_E_BLOCKED_BY_VPN_POLICY (0x80d03807)
</dt> <dd>

La tâche terminée a été suspendue en raison de la détection du réseau VPN.

</dd> <dt>

<span id="DO_E_BLOCKED_BY_CRITICAL_MEMORY_USAGE__0x80d03808_"></span><span id="do_e_blocked_by_critical_memory_usage__0x80d03808_"></span><span id="DO_E_BLOCKED_BY_CRITICAL_MEMORY_USAGE__0X80D03808_"></span>DO_E_BLOCKED_BY_CRITICAL_MEMORY_USAGE (0x80d03808)
</dt> <dd>

La tâche terminée a été suspendue en raison de la détection de l’utilisation de la mémoire critique sur le système.

</dd> <dt>

<span id="DO_E_HTTP_BLOCKSIZE_MISMATCH__0x80d05001_"></span><span id="do_e_http_blocksize_mismatch__0x80d05001_"></span><span id="DO_E_HTTP_BLOCKSIZE_MISMATCH__0X80D05001_"></span>DO_E_HTTP_BLOCKSIZE_MISMATCH (0x80d05001)
</dt> <dd>

Le serveur HTTP a retourné une réponse dont la taille des données n’est pas égale à ce qui a été demandé.

</dd> <dt>

<span id="DO_E_INVALID_RANGE__0x80d05010_"></span><span id="do_e_invalid_range__0x80d05010_"></span><span id="DO_E_INVALID_RANGE__0X80D05010_"></span>DO_E_INVALID_RANGE (0x80d05010)
</dt> <dd>

La plage d’octets spécifiée n’est pas valide.

</dd> <dt>

<span id="DO_E_INSUFFICIENT_RANGE_SUPPORT__0x80d05011_"></span><span id="do_e_insufficient_range_support__0x80d05011_"></span><span id="DO_E_INSUFFICIENT_RANGE_SUPPORT__0X80D05011_"></span>DO_E_INSUFFICIENT_RANGE_SUPPORT (0x80d05011)
</dt> <dd>

Le serveur ne prend pas en charge le protocole HTTP requis. L’optimisation de la remise (DO) requiert que le serveur prenne en charge l’en-tête de protocole Range.

</dd> <dt>

<span id="DO_E_OVERLAPPING_RANGES__0x80d05012_"></span><span id="do_e_overlapping_ranges__0x80d05012_"></span><span id="DO_E_OVERLAPPING_RANGES__0X80D05012_"></span>DO_E_OVERLAPPING_RANGES (0x80d05012)
</dt> <dd>

La liste de plages d’octets contient des plages qui se chevauchent, ce qui n’est pas pris en charge.

</dd> <dt>

<span id="DO_E_FATAL_CORE_ERROR__0x80d06802_"></span><span id="do_e_fatal_core_error__0x80d06802_"></span><span id="DO_E_FATAL_CORE_ERROR__0X80D06802_"></span>DO_E_FATAL_CORE_ERROR (0x80d06802)
</dt> <dd>

Erreur irrécupérable rencontrée dans le noyau.

</dd> </dl>

 

 