---
title: Énumération MPSTATUS_FLAG (MpClient. h)
description: Indicateurs de bits d’état de produit globaux possibles.
ms.assetid: BF2E6506-E76A-4785-8E91-99937B413548
keywords:
- MPSTATUS_FLAG énumération des fonctionnalités d’environnement Windows héritées
- PMPSTATUS_FLAG de l’héritage des Windows fonctionnalités d’environnement du pointeur d’énumération
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127231900"
---
# <a name="mpstatus_flag-enumeration"></a>\_Énumération de l’indicateur MPSTATUS

Indicateurs de bits d’état de produit globaux possibles.

## <a name="syntax"></a>Syntaxe


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



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="MP_STATUS_FLAG_NONE"></span><span id="mp_status_flag_none"></span>**indicateur d’état de Pack d' \_ état \_ \_ aucun**
</dt> <dd>

Aucun indicateur d’état défini (État non initialisé).

</dd> <dt>

<span id="MP_STATUS_FLAG_SERVICE_UNAVAILABLE"></span><span id="mp_status_flag_service_unavailable"></span>**SERVICE d’indicateur d’État du pack d’accès \_ \_ \_ \_ non disponible**
</dt> <dd>

Le service n’est pas en cours d’exécution.

</dd> <dt>

<span id="MP_STATUS_FLAG_MPENGINE_UNAVAILABLE"></span><span id="mp_status_flag_mpengine_unavailable"></span>**indicateur d’État du pack d' \_ \_ \_ MPENGINE \_ non disponible**
</dt> <dd>

Service démarré sans moteur de protection contre les programmes malveillants.

</dd> <dt>

<span id="MP_STATUS_FLAG_THREAT_FULLSCAN_REQUIRED"></span><span id="mp_status_flag_threat_fullscan_required"></span>**indicateur d’État du point de gestion- \_ \_ FULLSCAN des \_ menaces \_ \_ requis**
</dt> <dd>

Analyse complète en attente en raison d’une menace.

</dd> <dt>

<span id="MP_STATUS_FLAG_THREAT_REBOOT_REQUIRED"></span><span id="mp_status_flag_threat_reboot_required"></span>**indicateur d’État du pack d' \_ état- \_ \_ \_ redémarrage des menaces \_ requis**
</dt> <dd>

Redémarrage en attente en raison d’une menace.

</dd> <dt>

<span id="MP_STATUS_FLAG_THREAT_MANUAL_STEPS_REQUIRED"></span><span id="mp_status_flag_threat_manual_steps_required"></span>**indicateur d’État du pack d' \_ état \_ \_ \_ étapes manuelles des menaces \_ \_ requises**
</dt> <dd>

Étapes manuelles en attente en raison de l’action de la menace.

</dd> <dt>

<span id="MP_STATUS_FLAG_DUE_AV_SIGNATURE"></span><span id="mp_status_flag_due_av_signature"></span>**indicateur d’État du point de gestion, \_ \_ \_ \_ signature AV due \_**
</dt> <dd>

Signatures antivirus obsolètes.

</dd> <dt>

<span id="MP_STATUS_FLAG_DUE_AS_SIGNATURE"></span><span id="mp_status_flag_due_as_signature"></span>**indicateur d’État du pack d' \_ \_ \_ attente en raison \_ de la \_ signature**
</dt> <dd>

Signatures anti-espion obsolètes.

</dd> <dt>

<span id="MP_STATUS_FLAG_DUE_QUICK_SCAN"></span><span id="mp_status_flag_due_quick_scan"></span>**indicateur d’État du pack d' \_ \_ \_ analyse en raison d’une \_ \_ analyse rapide**
</dt> <dd>

Aucune analyse rapide ne s’est produite pendant une période spécifiée.

</dd> <dt>

<span id="MP_STATUS_FLAG_DUE_FULL_SCAN"></span><span id="mp_status_flag_due_full_scan"></span>**indicateur d’État du pack d' \_ \_ \_ analyse en raison d' \_ une \_ analyse complète**
</dt> <dd>

aucune analyse complète n’a eu lieu pendant une période spécifiée

</dd> <dt>

<span id="MP_STATUS_FLAG_INPROGRESS_SYSTEM_SCAN"></span><span id="mp_status_flag_inprogress_system_scan"></span>**analyse du système en cours d’indicateur d’État du pack d' \_ \_ \_ \_ \_ analyse**
</dt> <dd>

Analyse initiée par le système en cours.

</dd> <dt>

<span id="MP_STATUS_FLAG_INPROGRESS_ROUTINE_CLEANING"></span><span id="mp_status_flag_inprogress_routine_cleaning"></span>**nettoyage de la routine de l’indicateur d’État du pack d' \_ état \_ \_ \_ \_**
</dt> <dd>

Nettoyage initié par le système en cours.

</dd> <dt>

<span id="MP_STATUS_FLAG_DUE_SAMPLES"></span><span id="mp_status_flag_due_samples"></span>**exemples d’état de Pack d' \_ \_ \_ attente \_**
</dt> <dd>

Des exemples sont en attente d’envoi.

</dd> <dt>

<span id="MP_STATUS_FLAG_EVALUATION_MODE"></span><span id="mp_status_flag_evaluation_mode"></span>**MODE d’évaluation de l' \_ indicateur d’État MP \_ \_ \_**
</dt> <dd>

Le produit est en cours d’exécution en mode évaluation.

</dd> <dt>

<span id="MP_STATUS_FLAG_NONGENUINE"></span><span id="mp_status_flag_nongenuine"></span>**indicateur d’état de point de gestion pas \_ \_ \_ authentique**
</dt> <dd>

le produit s’exécute en mode de Windows non-authentique.

</dd> <dt>

<span id="MP_STATUS_FLAG_PRODUCT_EXPIRED"></span><span id="mp_status_flag_product_expired"></span>**indicateur d’État du pack d' \_ État du \_ \_ produit \_ expiré**
</dt> <dd>

Le produit a expiré.

</dd> <dt>

<span id="MP_STATUS_FLAG_THREAT_CALLISTO_REQUIRED"></span><span id="mp_status_flag_threat_callisto_required"></span>**\_indicateur d’État MP \_ \_ Threat \_ Callisto \_ requis**
</dt> <dd>

Analyse hors ligne Callisto requise.

</dd> <dt>

<span id="MP_STATUS_FLAG_SERVICE_ON_SYSTEM_SHUTDOWN"></span><span id="mp_status_flag_service_on_system_shutdown"></span>**\_ \_ \_ service \_ d’indicateur d’État du point de gestion à l' \_ arrêt du système \_**
</dt> <dd>

Le service s’arrête dans le cadre de l’arrêt du système.

</dd> <dt>

<span id="MP_STATUS_FLAG_SERVICE_CRITICAL_FAILURE"></span><span id="mp_status_flag_service_critical_failure"></span>**\_ \_ \_ défaillance critique du service d’indicateur \_ d’État du pack d’accès \_**
</dt> <dd>

Échec critique de la correction des menaces.

</dd> <dt>

<span id="MP_STATUS_FLAG_SERVICE_NON_CRITICAL_FAILURE"></span><span id="mp_status_flag_service_non_critical_failure"></span>**\_ \_ \_ \_ \_ défaillance non critique du service d’indicateur d’état \_ du point de gestion**
</dt> <dd>

Échec de la correction de la menace non critique.

</dd> <dt>

<span id="MP_STATUS_FLAG_HEALTH_INITIALIZED"></span><span id="mp_status_flag_health_initialized"></span>**\_intégrité de \_ l’indicateur d’État du point de gestion \_ \_ initialisée**
</dt> <dd>

Aucun indicateur d’état défini (état bien initialisé).

</dd> <dt>

<span id="MP_STATUS_FLAG_DUE_PLATFORM_UPDATE"></span><span id="mp_status_flag_due_platform_update"></span>**\_indicateur d’État MP en raison de la \_ \_ \_ \_ mise à jour de la plateforme**
</dt> <dd>

La plateforme est obsolète.

</dd> <dt>

<span id="MP_STATUS_FLAG_INPROGRESS_PLATFORM_UPDATE"></span><span id="mp_status_flag_inprogress_platform_update"></span>**\_ \_ \_ \_ \_ mise à jour de la plateforme en cours d’indicateur d’État MP**
</dt> <dd>

Mise à jour de la plateforme en cours.

</dd> <dt>

<span id="MP_STATUS_FLAG_PLATFORM_ABOUT_TO_BE_OUTDATED"></span><span id="mp_status_flag_platform_about_to_be_outdated"></span>**\_ \_ plateforme d’indicateur d’État MP sur le point \_ \_ \_ d' \_ être \_ obsolète**
</dt> <dd>

La plateforme est sur le paragraphe obsolète

</dd> <dt>

<span id="MP_STATUS_FLAG_END_OF_LIFE"></span><span id="mp_status_flag_end_of_life"></span>**\_ \_ \_ fin \_ de vie de l’indicateur d’État MP \_**
</dt> <dd>

La fin de la signature ou de la plateforme est passée ou en attente.

</dd> <dt>

<span id="MP_STATUS_FLAG_MAX"></span><span id="mp_status_flag_max"></span>**\_indicateur d’État MP \_ \_ Max.**
</dt> <dd>

Indicateur de nombre maximal valide.

</dd> <dt>

<span id="MP_STATUS_FLAG_ALL"></span><span id="mp_status_flag_all"></span>**\_indicateur d’État du point de gestion \_ \_**
</dt> <dd>

Valeur maximale possible.

</dd> </dl>

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau uniquement\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



 

 





