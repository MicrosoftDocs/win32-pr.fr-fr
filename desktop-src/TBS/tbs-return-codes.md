---
title: Codes de retour TBS (TBS. h)
description: TBS utilise les codes suivants pour indiquer le résultat d’un appel de fonction.
ms.assetid: a3888263-aa00-4b31-b51d-c6d448c1edb7
topic_type:
- apiref
api_name:
- TBS_SUCCESS
- TBS_E_INTERNAL_ERROR
- TBS_E_BAD_PARAMETER
- TBS_E_INVALID_OUTPUT_POINTER
- TBS_E_INVALID_CONTEXT
- TBS_E_INSUFFICIENT_BUFFER
- TBS_E_IOERROR
- TBS_E_INVALID_CONTEXT_PARAM
- TBS_E_SERVICE_NOT_RUNNING
- TBS_E_TOO_MANY_TBS_CONTEXTS
- TBS_E_TOO_MANY_RESOURCES
- TBS_E_SERVICE_START_PENDING
- TBS_E_PPI_NOT_SUPPORTED
- TBS_E_COMMAND_CANCELED
- TBS_E_BUFFER_TOO_LARGE
- TBS_E_TPM_NOT_FOUND
- TBS_E_SERVICE_DISABLED
- TBS_E_NO_EVENT_LOG
- TBS_E_ACCESS_DENIED
- TBS_E_PROVISIONING_NOT_ALLOWED
- TBS_E_PPI_FUNCTION_UNSUPPORTED
- TBS_E_OWNERAUTH_NOT_FOUND
- TBS_E_PROVISIONING_INCOMPLETE
api_location:
- Tbs.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a0271c323e4ea300f45817aa59d4f5f9779f9981
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127193607"
---
# <a name="tbs-return-codes"></a>Codes de retour TBS

TBS utilise les codes suivants pour indiquer le résultat d’un appel de fonction.



| Constante/valeur                                                                                                                                                                                                                                                                                   | Description                                                                                                                                                                                                                                |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TBS_SUCCESS"></span><span id="tbs_success"></span><dl> <dt>**Tbs \_ SUCCÈS**</dt> <dt>0 (0x0)</dt> </dl>                                                                             | La fonction a réussi.<br/>                                                                                                                                                                                                         |
| <span id="TBS_E_INTERNAL_ERROR"></span><span id="tbs_e_internal_error"></span><dl> <dt>**Tbs \_ E \_ \_ erreur interne**</dt> <dt>2150121473 (0x80284001)</dt> </dl>                                | Une erreur interne du logiciel s'est produite.<br/>                                                                                                                                                                                            |
| <span id="TBS_E_BAD_PARAMETER"></span><span id="tbs_e_bad_parameter"></span><dl> <dt>**Tbs \_ E \_ \_ paramètre incorrect**</dt> <dt>2150121474 (0x80284002)</dt> </dl>                                   | Une ou plusieurs valeurs de paramètre ne sont pas valides.<br/>                                                                                                                                                                                     |
| <span id="TBS_E_INVALID_OUTPUT_POINTER"></span><span id="tbs_e_invalid_output_pointer"></span><dl> <dt>**Tbs \_ E \_ \_ \_ pointeur de sortie non valide**</dt> <dt>2150121475 (0x80284003)</dt> </dl>       | Un pointeur de sortie spécifié est incorrect.<br/>                                                                                                                                                                                              |
| <span id="TBS_E_INVALID_CONTEXT"></span><span id="tbs_e_invalid_context"></span><dl> <dt>**Tbs \_ E \_ \_ contexte non valide**</dt> <dt>2150121476 (0x80284004)</dt> </dl>                             | Le handle de contexte spécifié ne fait pas référence à un contexte valide.<br/>                                                                                                                                                                 |
| <span id="TBS_E_INSUFFICIENT_BUFFER"></span><span id="tbs_e_insufficient_buffer"></span><dl> <dt>**Tbs \_ \_ \_ Mémoire tampon insuffisante**</dt> <dt>2150121477 (0x80284005)</dt> </dl>                 | La mémoire tampon de sortie spécifiée est insuffisante.<br/>                                                                                                                                                                                       |
| <span id="TBS_E_IOERROR"></span><span id="tbs_e_ioerror"></span><dl> <dt>**Tbs \_ E \_ IOERROR**</dt> <dt>2150121478 (0x80284006)</dt> </dl>                                                      | Une erreur s’est produite lors de la communication avec le module de plateforme sécurisée.<br/>                                                                                                                                                                             |
| <span id="TBS_E_INVALID_CONTEXT_PARAM"></span><span id="tbs_e_invalid_context_param"></span><dl> <dt>**Tbs \_ E \_ paramètre de contexte non valide \_ \_ param**</dt> <dt>2150121479 (0x80284007)</dt> </dl>          | Un paramètre de contexte qui n’est pas valide a été passé lors de la tentative de création d’un contexte TBS.<br/>                                                                                                                                       |
| <span id="TBS_E_SERVICE_NOT_RUNNING"></span><span id="tbs_e_service_not_running"></span><dl> <dt>**Tbs \_ \_Service E \_ non \_ exécuté**</dt> <dt>2150121480 (0x80284008)</dt> </dl>                | Le service TBS n’est pas en cours d’exécution et n’a pas pu être démarré.<br/>                                                                                                                                                                        |
| <span id="TBS_E_TOO_MANY_TBS_CONTEXTS"></span><span id="tbs_e_too_many_tbs_contexts"></span><dl> <dt>**Tbs \_ E \_ trop \_ de \_ \_ contextes tbs**</dt> <dt>2150121481 (0x80284009)</dt> </dl>         | Impossible de créer un nouveau contexte, car il y a trop de contextes ouverts.<br/>                                                                                                                                                    |
| <span id="TBS_E_TOO_MANY_RESOURCES"></span><span id="tbs_e_too_many_resources"></span><dl> <dt>**Tbs \_ E \_ trop \_ de \_ ressources**</dt> <dt>2150121482 (0x8028400A)</dt> </dl>                   | Une nouvelle ressource virtuelle n’a pas pu être créée, car il y a trop de ressources virtuelles ouvertes.<br/>                                                                                                                                  |
| <span id="TBS_E_SERVICE_START_PENDING"></span><span id="tbs_e_service_start_pending"></span><dl> <dt>**Tbs \_ \_Démarrage du service E \_ \_ en attente**</dt> <dt>2150121483 (0x8028400B)</dt> </dl>          | Le service TBS a été démarré mais n’est pas encore en cours d’exécution.<br/>                                                                                                                                                                        |
| <span id="TBS_E_PPI_NOT_SUPPORTED"></span><span id="tbs_e_ppi_not_supported"></span><dl> <dt>**Tbs \_ E \_ PPP \_ non \_ pris en charge**</dt> <dt>2150121484 (0x8028400C)</dt> </dl>                      | L’interface de présence physique n’est pas prise en charge.<br/>                                                                                                                                                                               |
| <span id="TBS_E_COMMAND_CANCELED"></span><span id="tbs_e_command_canceled"></span><dl> <dt>**Tbs \_ \_Commande E \_ annulée**</dt> <dt>2150121485 (0x8028400D)</dt> </dl>                          | La commande a été annulée.<br/>                                                                                                                                                                                                       |
| <span id="TBS_E_BUFFER_TOO_LARGE"></span><span id="tbs_e_buffer_too_large"></span><dl> <dt>**Tbs \_ \_Tampon E \_ trop \_ grand**</dt> <dt>2150121486 (0x8028400E)</dt> </dl>                         | Le tampon d’entrée ou de sortie est trop grand.<br/>                                                                                                                                                                                        |
| <span id="TBS_E_TPM_NOT_FOUND"></span><span id="tbs_e_tpm_not_found"></span><dl> <dt>**Tbs \_ E \_ TPM \_ \_ introuvable**</dt> <dt>2150121487 (0x8028400F)</dt> </dl>                                  | Impossible de trouver un appareil de sécurité de Module de plateforme sécurisée (TPM) compatible (TPM) sur cet ordinateur.<br/>                                                                                                                                    |
| <span id="TBS_E_SERVICE_DISABLED"></span><span id="tbs_e_service_disabled"></span><dl> <dt>**Tbs \_ \_Service E \_ désactivé**</dt> <dt>2150121488 (0x80284010)</dt> </dl>                          | Le service TBS a été désactivé.<br/>                                                                                                                                                                                              |
| <span id="TBS_E_NO_EVENT_LOG"></span><span id="tbs_e_no_event_log"></span><dl> <dt>**Tbs \_ E \_ aucun \_ \_ journal des événements**</dt> <dt>2150121489 (0x80284011)</dt> </dl>                                     | Le journal des événements TBS n’est pas disponible.<br/>                                                                                                                                                                                             |
| <span id="TBS_E_ACCESS_DENIED"></span><span id="tbs_e_access_denied"></span><dl> <dt>**Tbs \_ \_Accès E \_ refusé**</dt> <dt>2150121490 (0x80284012)</dt> </dl>                                   | L’appelant ne dispose pas des droits appropriés pour effectuer l’opération demandée.<br/>                                                                                                                                             |
| <span id="TBS_E_PROVISIONING_NOT_ALLOWED"></span><span id="tbs_e_provisioning_not_allowed"></span><dl> <dt>**Tbs \_ \_Approvisionnement E \_ non \_ autorisé**</dt> <dt>2150121491 (0x80284013)</dt> </dl> | L’action de provisionnement du module de plateforme sécurisée n’est pas autorisée par les indicateurs spécifiés.<br/>                                                                                                                                                              |
| <span id="TBS_E_PPI_FUNCTION_UNSUPPORTED"></span><span id="tbs_e_ppi_function_unsupported"></span><dl> <dt>**Tbs \_ \_Fonction E \_ PPI \_ non prise en charge**</dt> <dt>2150121492 (0x80284014)</dt> </dl> | L’interface de présence physique de ce microprogramme ne prend pas en charge la méthode demandée.<br/>                                                                                                                                         |
| <span id="TBS_E_OWNERAUTH_NOT_FOUND"></span><span id="tbs_e_ownerauth_not_found"></span><dl> <dt>**Tbs \_ E \_ origine \_ \_ introuvable**</dt> <dt>2150121493 (0x80284015)</dt> </dl>                | La valeur de origine TPM demandée est introuvable.<br/>                                                                                                                                                                                |
| <span id="TBS_E_PROVISIONING_INCOMPLETE"></span><span id="tbs_e_provisioning_incomplete"></span><dl> <dt>**Tbs \_ \_PROvisionnement E \_ incomplet**</dt> <dt>2150121493 (0x80284015)</dt> </dl>     | L’approvisionnement du module de plateforme sécurisée ne s’est pas terminé. Pour plus d’informations sur l’exécution de l’approvisionnement, appelez la méthode WMI [**\_ TPM Win32**](/windows/desktop/SecProv/win32-tpm) pour la configuration du module de plateforme sécurisée (« provision ») et vérifiez les informations renvoyées.<br/> |



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                   |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                             |
| En-tête<br/>                   | <dl> <dt>Tbs. h</dt> </dl> |



 

