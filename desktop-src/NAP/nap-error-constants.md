---
title: Constantes d’erreur NAP (WinError. h)
description: Les constantes d’erreur NAP suivantes sont définies dans WinError. h.
ms.assetid: b2fba990-75d9-4153-8058-c01e97700d00
topic_type:
- apiref
api_name:
- NAP_E_INVALID_PACKET
- NAP_E_MISSING_SOH
- NAP_E_CONFLICTING_ID
- NAP_E_NO_CACHED_SOH
- NAP_E_STILL_BOUND
- NAP_E_NOT_REGISTERED
- NAP_E_NOT_INITIALIZED
- NAP_E_MISMATCHED_ID
- NAP_E_NOT_PENDING
- NAP_E_ID_NOT_FOUND
- NAP_E_MAXSIZE_TOO_SMALL
- NAP_E_SERVICE_NOT_RUNNING
- NAP_S_CERT_ALREADY_PRESENT
- NAP_E_ENTITY_DISABLED
- NAP_E_NETSH_GROUPPOLICY_ERROR
- NAP_E_TOO_MANY_CALLS
- NAP_E_SHV_CONFIG_EXISTED
- NAP_E_SHV_CONFIG_NOT_FOUND
- NAP_E_SHV_TIMEOUT
api_location:
- WinError.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 411500ea5f0fc3ba0f1d4067a6befe902a81af3154c91e76c36425c289616eb8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118620838"
---
# <a name="nap-error-constants"></a>Constantes d’erreur NAP

> [!Note]  
> La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10

 

Les constantes d’erreur NAP suivantes sont définies dans WinError. h.

<dl> <dt>

<span id="NAP_E_INVALID_PACKET"></span><span id="nap_e_invalid_packet"></span>**\_paquet NAP E \_ non valide \_**
</dt> <dd> <dl> <dt>

\_HRESULT \_ typedef \_ (0x80270001L)
</dt> <dt>



Le paquet de [**déclaration d’intégrité**](/windows/win32/api/naptypes/ns-naptypes-soh) NAP n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="NAP_E_MISSING_SOH"></span><span id="nap_e_missing_soh"></span>**SOH de la protection d’accès réseau \_ \_ manquante \_**
</dt> <dd> <dl> <dt>

\_HRESULT \_ typedef \_ (0x80270002L)
</dt> <dt>



Une [**SOH**](/windows/win32/api/naptypes/ns-naptypes-soh) était manquante dans le paquet NAP.


</dt> </dl> </dd> <dt>

<span id="NAP_E_CONFLICTING_ID"></span><span id="nap_e_conflicting_id"></span>**\_ID en \_ conflit NAP \_ E**
</dt> <dd> <dl> <dt>

\_HRESULT \_ typedef \_ (0x80270003L)
</dt> <dt>



L’ID d’entité est en conflit avec un ID d’entité déjà inscrit.


</dt> </dl> </dd> <dt>

<span id="NAP_E_NO_CACHED_SOH"></span><span id="nap_e_no_cached_soh"></span>**E/r NAP \_ \_ non \_ mis en cache \_**
</dt> <dd> <dl> <dt>

\_HRESULT \_ typedef \_ (0x80270004L)
</dt> <dt>



Aucune déclaration d' [**intégrité**](/windows/win32/api/naptypes/ns-naptypes-soh) mise en cache n’est présente.


</dt> </dl> </dd> <dt>

<span id="NAP_E_STILL_BOUND"></span><span id="nap_e_still_bound"></span>**la protection NAP est \_ \_ toujours \_ liée**
</dt> <dd> <dl> <dt>

\_HRESULT \_ typedef \_ (0x80270005L)
</dt> <dt>



L’entité est toujours liée au système NAP.


</dt> </dl> </dd> <dt>

<span id="NAP_E_NOT_REGISTERED"></span><span id="nap_e_not_registered"></span>**NAP \_ E \_ non \_ inscrit**
</dt> <dd> <dl> <dt>

\_HRESULT \_ typedef \_ (0x80270006L)
</dt> <dt>



L’entité n’est pas inscrite auprès du système NAP.


</dt> </dl> </dd> <dt>

<span id="NAP_E_NOT_INITIALIZED"></span><span id="nap_e_not_initialized"></span>**NAP \_ E \_ non \_ initialisé**
</dt> <dd> <dl> <dt>

\_HRESULT \_ typedef \_ (0x80270007L)
</dt> <dt>



L’entité n’est pas initialisée avec le système NAP.


</dt> </dl> </dd> <dt>

<span id="NAP_E_MISMATCHED_ID"></span><span id="nap_e_mismatched_id"></span>**\_ID non \_ compatible NAP \_**
</dt> <dd> <dl> <dt>

\_HRESULT \_ typedef \_ (0x80270008L)
</dt> <dt>



Les ID de corrélation dans la requête [**SOH**](/windows/win32/api/naptypes/ns-naptypes-soh) et la réponse **SOH** ne correspondent pas.


</dt> </dl> </dd> <dt>

<span id="NAP_E_NOT_PENDING"></span><span id="nap_e_not_pending"></span>**NAP \_ E \_ non \_ en attente**
</dt> <dd> <dl> <dt>

\_HRESULT \_ typedef \_ (0x80270009L)
</dt> <dt>



La saisie semi-automatique a été indiquée sur une demande qui n’est pas actuellement en attente.


</dt> </dl> </dd> <dt>

<span id="NAP_E_ID_NOT_FOUND"></span><span id="nap_e_id_not_found"></span>**\_ID NAP \_ E \_ \_ introuvable**
</dt> <dd> <dl> <dt>

\_HRESULT \_ typedef \_ (0x8027000AL)
</dt> <dt>



L’ID du composant NAP est introuvable.


</dt> </dl> </dd> <dt>

<span id="NAP_E_MAXSIZE_TOO_SMALL"></span><span id="nap_e_maxsize_too_small"></span>**NAP \_ E \_ MaxSize \_ trop \_ petit**
</dt> <dd> <dl> <dt>

\_HRESULT \_ typedef \_ (0x8027000BL)
</dt> <dt>



La taille maximale de la connexion est trop petite pour un paquet SoH.


</dt> </dl> </dd> <dt>

<span id="NAP_E_SERVICE_NOT_RUNNING"></span><span id="nap_e_service_not_running"></span>**\_service E \_ NAP \_ non \_ exécuté**
</dt> <dd> <dl> <dt>

\_HRESULT \_ typedef \_ (0x8027000CL)
</dt> <dt>



Le service NapAgent n’est pas en cours d’exécution.


</dt> </dl> </dd> <dt>

<span id="NAP_S_CERT_ALREADY_PRESENT"></span><span id="nap_s_cert_already_present"></span>**\_certificat NAP \_ S \_ déjà \_ présent**
</dt> <dd> <dl> <dt>

\_HRESULT \_ typedef \_ (0x0027000DL) 
</dt> <dt>



Un certificat est déjà présent dans le magasin de certificats.


</dt> </dl> </dd> <dt>

<span id="NAP_E_ENTITY_DISABLED"></span><span id="nap_e_entity_disabled"></span>**\_entité NAP \_ E \_ désactivée**
</dt> <dd> <dl> <dt>

\_HRESULT \_ typedef \_ (0x8027000EL)
</dt> <dt>



L’entité est désactivée avec le service NapAgent.


</dt> </dl> </dd> <dt>

<span id="NAP_E_NETSH_GROUPPOLICY_ERROR"></span><span id="nap_e_netsh_grouppolicy_error"></span>**\_erreur NAP E \_ netsh \_ GROUPPOLICY \_**
</dt> <dd> <dl> <dt>

\_HRESULT \_ typedef \_ (0x8027000FL)
</dt> <dt>



Stratégie de groupe n’est pas configurée.


</dt> </dl> </dd> <dt>

<span id="NAP_E_TOO_MANY_CALLS"></span><span id="nap_e_too_many_calls"></span>**NAP \_ E \_ trop \_ d' \_ appels**
</dt> <dd> <dl> <dt>

\_HRESULT \_ typedef \_ (0x80270010L)
</dt> <dt>



Appels simultanés trop nombreux.


</dt> </dl> </dd> <dt>

<span id="NAP_E_SHV_CONFIG_EXISTED"></span><span id="nap_e_shv_config_existed"></span>**la \_ configuration NAP E \_ SHV \_ \_ existait**
</dt> <dd> <dl> <dt>

\_HRESULT \_ typedef \_ (0x80270011L)
</dt> <dt>



La configuration SHV existe déjà.

> [!Note]  
> pris en charge dans Windows 7 ou version ultérieure.

 


</dt> </dl> </dd> <dt>

<span id="NAP_E_SHV_CONFIG_NOT_FOUND"></span><span id="nap_e_shv_config_not_found"></span>**configuration de NAP \_ E \_ SHV \_ \_ \_ introuvable**
</dt> <dd> <dl> <dt>

\_HRESULT \_ typedef \_ (0x80270012L)
</dt> <dt>



La configuration SHV est introuvable.

> [!Note]  
> pris en charge dans Windows 7 ou version ultérieure.

 


</dt> </dl> </dd> <dt>

<span id="NAP_E_SHV_TIMEOUT"></span><span id="nap_e_shv_timeout"></span>**\_ \_ \_ délai d’attente du SHV NAP E**
</dt> <dd> <dl> <dt>

\_HRESULT \_ typedef \_ (0x80270013L)
</dt> <dt>



Le SHV a expiré sur la demande.

> [!Note]  
> pris en charge dans Windows 7 ou version ultérieure.

 


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>WinError. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Constantes NAP**](nap-constants.md)
</dt> </dl>

 

 





