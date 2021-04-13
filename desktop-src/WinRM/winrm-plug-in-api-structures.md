---
title: Structures d’API de plug-in WinRM
description: Structures d’API de plug-in WinRM
ms.assetid: 745619bc-c7b3-48fa-8212-cb1b5b9ed4db
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 685bcf87ef8c634db367db62b3ec1472b50e3b6b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310681"
---
# <a name="winrm-plug-in-api-structures"></a>Structures d’API de plug-in WinRM

Le tableau suivant fournit une vue d’ensemble des structures de l’interface de programmation d’applications (API) du plug-in Windows Remote Management (WinRM).



| Structure                                                        | Description                                                                              |
|------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [**QUOTA d’autorisation WSMAN \_ \_**](/windows/desktop/api/Wsman/ns-wsman-wsman_authz_quota)                 | Définit les informations de quota pour chaque utilisateur.                                           |
| [**\_Détails du certificat WSMan \_**](/windows/desktop/api/Wsman/ns-wsman-wsman_certificate_details) | Représente les champs dans le certificat client.                                     |
| [**jeu d’arguments de la \_ commande WSMan \_ \_**](/windows/desktop/api/Wsman/ns-wsman-wsman_command_arg_set)        | Représente l’ensemble des arguments passés à la ligne de commande.                  |
| [**\_filtre WSMan**](/windows/desktop/api/Wsman/ns-wsman-wsman_filter)                            | Définit le filtrage utilisé pour une opération.                                             |
| [**\_fragment WSMan**](/windows/desktop/api/Wsman/ns-wsman-wsman_fragment)                        | Définit les informations de fragment pour une opération.                                       |
| [**\_informations sur l’opération WSMan \_**](/windows/desktop/api/Wsman/ns-wsman-wsman_operation_info)           | Représente un point de terminaison de ressource spécifique pour lequel le plug-in doit exécuter la demande. |
| [**\_demande de plug-in WSMan \_**](/windows/desktop/api/Wsman/ns-wsman-wsman_plugin_request)           | Contient des informations sur la demande et est passé à chaque opération de plug-in.       |
| [**Détails de l' \_ expéditeur WSMan \_**](/windows/desktop/api/Wsman/ns-wsman-wsman_sender_details)           | Spécifie les détails du client pour chaque demande entrante.                                      |



 

 

 




