---
description: Codes d’erreur du NSP PNRP
ms.assetid: adf40b1a-c5d6-418d-a012-cf6ba7d4fa24
title: Codes d’erreur du NSP PNRP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acee7465a86d56af9b2e07a1ae6948dd1b1a1e9145cee2165b7dd4e90f2a5f1c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119061347"
---
# <a name="pnrp-nsp-error-codes"></a>Codes d’erreur du NSP PNRP

Si la fonction du fournisseur d’espace de noms (NSP) renvoie une **\_ erreur de socket**, [WSAGetLastError](winsock-nsp-reference-links.md) doit être utilisé pour obtenir plus d’informations sur l’erreur. Le NSP PNRP retourne les codes d’erreur suivants :



| Terme                                                                                                                                                                     | Description                                                                                                        |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span id="WSA_E_CANCELLED"></span><span id="wsa_e_cancelled"></span>WSA \_ E \_ annulée<br/>                                                                         | Une opération est annulée.<br/>                                                                               |
| <span id="__WSA_E_NO_MORE"></span><span id="__wsa_e_no_more"></span>WSA \_ E \_ plus \_<br/>                                                                         | Les résultats d’une demande résolue ne sont pas prêts. Il se peut qu’il ne s’agit pas d’une erreur.<br/>                              |
| <span id="_WSA_IO_PENDING_"></span><span id="_wsa_io_pending_"></span>\_e/s WSA \_ en attente <br/>                                                                      | Une opération n’est pas terminée.<br/>                                                                           |
| <span id="WSA_NOT_ENOUGH_MEMORY"></span><span id="wsa_not_enough_memory"></span>\_mémoire WSA \_ insuffisante \_<br/>                                                      | La mémoire est insuffisante pour effectuer une action spécifiée.<br/>                                              |
| <span id="WSA_OPERATION_ABORTED"></span><span id="wsa_operation_aborted"></span>\_opération WSA \_ abandonnée<br/>                                                       | Une opération est annulée.<br/>                                                                               |
| <span id="WSA_PNRP_CLOUD_DISABLED"></span><span id="wsa_pnrp_cloud_disabled"></span>\_Cloud PNRP \_ PNRP \_ désactivé<br/>                                                | Un nom de Cloud spécifié est désactivé.<br/>                                                                     |
| <span id="WSA_PNRP_CLOUD_NOT_FOUND"></span><span id="wsa_pnrp_cloud_not_found"></span>\_Cloud PNRP \_ PNRP \_ \_ introuvable<br/>                                            | Un nom de Cloud spécifié n’est pas disponible.<br/>                                                                |
| <span id="WSA_PNRP_CLOUD_IS_SEARCH_ONLY"></span><span id="wsa_pnrp_cloud_is_search_only"></span>le \_ Cloud PNRP PNRP \_ \_ est une \_ recherche \_ uniquement<br/>                            | Une tentative a été effectuée pour enregistrer un nom dans un Cloud qui a été configuré pour être résolu uniquement.<br/>     |
| <span id="WSA_PNRP_CLIENT_INVALID_COMPARTMENT_ID"></span><span id="wsa_pnrp_client_invalid_compartment_id"></span>\_ID de \_ \_ compartiment non valide du client \_ WSA PNRP \_<br/> | Utilisation de PNRP dans un compartiment en dehors de la valeur par défaut. PNRP ne fonctionne que dans le compartiment par défaut.<br/>     |
| <span id="WSA_PNRP_INVALID_IDENTITY"></span><span id="wsa_pnrp_invalid_identity"></span>identité de WSA \_ PNRP \_ non valide \_<br/>                                          | Impossible d’accéder à une identité spécifiée.<br/>                                                                |
| <span id="WSA_PNRP_TOO_MUCH_LOAD"></span><span id="wsa_pnrp_too_much_load"></span>\_charge PNRP \_ trop \_ importante \_<br/>                                                  | Impossible de créer un nom d’homologue, car l’ordinateur ne dispose pas des ressources nécessaires pour traiter la demande. <br/> |
| <span id="WSAEFAULT"></span><span id="wsaefault"></span>WSAEFAULT<br/>                                                                                             | Une opération n’est pas autorisée dans l’état actuel.<br/>                                                        |
| <span id="WSAEINVAL"></span><span id="wsaeinval"></span>WSAEINVAL<br/>                                                                                             | Un paramètre ou une combinaison de paramètres non valide est spécifié.<br/>                                         |
| <span id="WSAENETUNREACH"></span><span id="wsaenetunreach"></span>WSAENETUNREACH<br/>                                                                              | Une connexion au réseau est perdue.<br/>                                                                    |
| <span id="WSAENOTIMPLEMENTED"></span><span id="wsaenotimplemented"></span>WSAENOTIMPLEMENTED<br/>                                                                  | Une fonctionnalité spécifiée n’est pas implémentée par PNRP.<br/>                                                   |
| <span id="WSAEOPNOTSUPP"></span><span id="wsaeopnotsupp"></span>WSAEOPNOTSUPP<br/>                                                                                 | PNRP n’est pas pris en charge par les fonctionnalités spécifiées.<br/>                                                     |
| <span id="WSAEWOULDBLOCK"></span><span id="wsaewouldblock"></span>WSAEWOULDBLOCK<br/>                                                                              | Une opération n’est pas terminée.<br/>                                                                           |
| <span id="__WSASERVICE_NOT_FOUND"></span><span id="__wsaservice_not_found"></span> WSASERVICE \_ \_ introuvable<br/>                                                     | Un fournisseur, un espace de noms ou un ID de service spécifié ne sont pas pris en charge.<br/>                                       |
| <span id="WSASYSNOTREADY"></span><span id="wsasysnotready"></span>WSASYSNOTREADY<br/>                                                                              | Le service n’a pas démarré.<br/>                                                                             |



 

 

 




