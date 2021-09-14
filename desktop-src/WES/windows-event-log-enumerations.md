---
title: Windows Énumérations des journaux des événements
description: Windows Le journal des événements définit les énumérations suivantes.
ms.assetid: 2dd0e9ef-057b-4d0a-8b21-e7f14e5ae6e3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c019a090d1a12e30948e5ed1f5672853caed848c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127192107"
---
# <a name="windows-event-log-enumerations"></a>Windows Énumérations des journaux des événements

Windows Le journal des événements définit les énumérations suivantes.



| Énumération                                                                          | Description                                                                                                                        |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [**\_type d' \_ horloge du canal evt \_**](/windows/desktop/api/WinEvt/ne-winevt-evt_channel_clock_type)                          | Définit les valeurs qui spécifient le type d’horodatage à utiliser lors de l’enregistrement du canal des événements.                                         |
| [**ID de propriété de la \_ configuration du canal evt \_ \_ \_**](/windows/desktop/api/WinEvt/ne-winevt-evt_channel_config_property_id)         | Définit les identificateurs qui identifient les propriétés de configuration d’un canal.                                                   |
| [**\_ \_ type d’isolation du canal evt \_**](/windows/desktop/api/WinEvt/ne-winevt-evt_channel_isolation_type)                  | Définit les autorisations d’accès par défaut à appliquer au canal.                                                                    |
| [**\_indicateurs de \_ Référence du canal evt \_**](/windows/desktop/api/WinEvt/ne-winevt-evt_channel_reference_flags)                | Définit les valeurs qui spécifient comment un canal est référencé.                                                                       |
| [**\_type de \_ SID du canal evt \_**](/windows/desktop/api/WinEvt/ne-winevt-evt_channel_sid_type)                              | Définit les valeurs qui déterminent si l’événement comprend l’identificateur de sécurité (SID) du principal qui a consigné l’événement. |
| [**\_type de canal evt \_**](/windows/desktop/api/WinEvt/ne-winevt-evt_channel_type)                                       | Définit le type d’un canal.                                                                                                     |
| [**\_ID de \_ propriété des métadonnées d’événement evt \_ \_**](/windows/desktop/api/WinEvt/ne-winevt-evt_event_metadata_property_id)         | Définit les identificateurs qui identifient les propriétés de métadonnées d’une définition d’événement.                                              |
| [**ID de propriété de l' \_ événement evt \_ \_**](/windows/desktop/api/WinEvt/ne-winevt-evt_event_property_id)               | Définit les valeurs qui déterminent les informations de requête à récupérer.                                                               |
| [**\_indicateurs EXPORTLOG \_ evt**](/windows/desktop/api/WinEvt/ne-winevt-evt_exportlog_flags)                                 | Définit des valeurs qui indiquent si les événements proviennent d’un canal ou d’un fichier journal.                                                   |
| [**\_indicateurs de \_ message au format evt \_**](/windows/desktop/api/WinEvt/ne-winevt-evt_format_message_flags)                      | Définit les valeurs qui spécifient la chaîne de message de l’événement à mettre en forme.                                                       |
| [**\_ID de \_ propriété de journal evt \_**](/windows/desktop/api/WinEvt/ne-winevt-evt_log_property_id)                                | Définit les identificateurs qui identifient les propriétés de métadonnées de fichier journal d’un canal ou d’un fichier journal.                                   |
| [**\_classe de connexion evt \_**](/windows/desktop/api/WinEvt/ne-winevt-evt_login_class)                                         | Définit les types de méthodes de connexion que vous pouvez utiliser pour vous connecter à l’ordinateur distant.                                             |
| [**EVT \_ ouvrir \_ les \_ indicateurs de journal**](/windows/desktop/api/WinEvt/ne-winevt-evt_open_log_flags)                                  | Définit les valeurs qui spécifient si un canal ou un fichier journal exporté doit être ouvert.                                                    |
| [**\_ID de \_ propriété de métadonnées du serveur de publication evt \_ \_**](/windows/desktop/api/WinEvt/ne-winevt-evt_publisher_metadata_property_id) | Définit les identificateurs qui identifient les propriétés de métadonnées d’un fournisseur.                                                       |
| [**\_indicateurs de requête evt \_**](/windows/desktop/api/WinEvt/ne-winevt-evt_query_flags)                                         | Définit les valeurs qui spécifient comment retourner les résultats de la requête et si vous effectuez une requête sur un canal ou un fichier journal.           |
| [**\_ID de \_ propriété de requête evt \_**](/windows/desktop/api/WinEvt/ne-winevt-evt_query_property_id)                            | Définit les identificateurs qui identifient les informations de requête que vous pouvez récupérer.                                                 |
| [**\_indicateurs de \_ contexte de rendu evt \_**](/windows/desktop/api/WinEvt/ne-winevt-evt_render_context_flags)                      | Définit les valeurs qui spécifient le type d’informations auxquelles accéder à partir de l’événement.                                                  |
| [**\_indicateurs de rendu evt \_**](/windows/desktop/api/WinEvt/ne-winevt-evt_render_flags)                                       | Définit les valeurs qui spécifient les éléments à restituer.                                                                                    |
| [**\_indicateurs de \_ connexion \_ RPC evt**](/windows/desktop/api/WinEvt/ne-winevt-evt_rpc_login_flags)                                | Définit les types d’authentification que vous pouvez utiliser pour authentifier l’utilisateur lors de la connexion à un ordinateur distant.                |
| [**\_indicateurs de recherche evt \_**](/windows/desktop/api/WinEvt/ne-winevt-evt_seek_flags)                                           | Définit la position relative dans le jeu de résultats à partir duquel effectuer la recherche.                                                                |
| [**\_indicateurs d’abonnement evt \_**](/windows/desktop/api/WinEvt/ne-winevt-evt_subscribe_flags)                                 | Définit les valeurs possibles qui spécifient quand démarrer l’abonnement aux événements.                                                      |
| [**\_action de \_ notification d’abonnement evt \_**](/windows/desktop/api/WinEvt/ne-winevt-evt_subscribe_notify_action)                | Définit les types de données possibles que le service d’abonnement peut remettre à votre rappel.                                     |
| [**\_ID de \_ propriété \_ système EVT**](/windows/desktop/api/WinEvt/ne-winevt-evt_system_property_id)                          | Définit les identificateurs qui identifient les propriétés définies par le système d’un événement.                                                   |
| [**\_type Variant \_ evt**](/windows/desktop/api/WinEvt/ne-winevt-evt_variant_type)                                       | Définit les types de données possibles d’un élément de données Variant.                                                                            |



 

 

 




