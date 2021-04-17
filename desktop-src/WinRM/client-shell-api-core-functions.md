---
title: Fonctions principales de l’API du shell client
description: Le tableau suivant fournit une vue d’ensemble des fonctions de base pour l’API d’environnement client Windows Remote Management (WinRM).
ms.assetid: cd0e6b55-03e8-4ebe-aea8-35d268cdb18c
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebfe3390b3808cd0abbe9d6bf4ea83ccb0a92338
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380005"
---
# <a name="client-shell-api-core-functions"></a>Fonctions principales de l’API du shell client

Le tableau suivant fournit une vue d’ensemble des fonctions de base pour l’API d’environnement client Windows Remote Management (WinRM).



| Fonctions de base                                                   | Description                                                                                                                                                                     |
|------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WSManCloseCommand**](/windows/desktop/api/Wsman/nf-wsman-wsmanclosecommand)                   | Ferme une commande.                                                                                                                                                               |
| [**WSManCloseOperation**](/windows/desktop/api/Wsman/nf-wsman-wsmancloseoperation)               | Ferme une opération.                                                                                                                                                            |
| [**WSManCloseSession**](/windows/desktop/api/Wsman/nf-wsman-wsmanclosesession)                   | Ferme une session WinRM.                                                                                                                                                         |
| [**WSManCloseShell**](/windows/desktop/api/Wsman/nf-wsman-wsmancloseshell)                       | Ferme un objet Shell.                                                                                                                                                          |
| [**WSManConnectShell**](/windows/desktop/api/Wsman/nf-wsman-wsmanconnectshell)                   | Établit une connexion à une session de serveur existante.                                                                                                                                         |
| [**WSManConnectShellCommand**](/windows/desktop/api/Wsman/nf-wsman-wsmanconnectshellcommand)     | Établit une connexion à une commande existante qui s’exécute dans un interpréteur de commandes.                                                                                                                             |
| [**WSManCreateSession**](/windows/desktop/api/Wsman/nf-wsman-wsmancreatesession)                 | Crée une session WinRM.                                                                                                                                                        |
| [**WSManCreateShell**](/windows/desktop/api/Wsman/nf-wsman-wsmancreateshell)                     | Crée un objet Shell.                                                                                                                                                         |
| [**WSManCreateShellEx**](/windows/desktop/api/Wsman/nf-wsman-wsmancreateshellex)                 | Crée un objet Shell en utilisant les mêmes fonctionnalités que la fonction [**WSManCreateShell**](/windows/desktop/api/Wsman/nf-wsman-wsmancreateshell) , avec l’ajout d’un ID de Shell spécifié par le client.          |
| [**WSManDeinitialize**](/windows/desktop/api/Wsman/nf-wsman-wsmandeinitialize)                   | Déinitialise la pile du client WinRM.                                                                                                                                           |
| [**WSManDisconnectShell**](/windows/desktop/api/Wsman/nf-wsman-wsmandisconnectshell)             | Déconnecte la connexion réseau d’un shell actif et de ses commandes associées.                                                                                              |
| [**WSManInitialize**](/windows/desktop/api/Wsman/nf-wsman-wsmaninitialize)                       | Initialise WinRM.                                                                                                                                                              |
| [**WSManReceiveShellOutput**](/windows/desktop/api/Wsman/nf-wsman-wsmanreceiveshelloutput)       | Reçoit la sortie de l’interpréteur de commandes.                                                                                                                                                          |
| [**WSManReconnectShell**](/windows/desktop/api/Wsman/nf-wsman-wsmanreconnectshell)               | Reconnecte une session d’interpréteur de commandes précédemment déconnectée. Pour reconnecter les commandes associées à la session de l’interpréteur de commandes, utilisez [**WSManReconnectShellCommand**](/windows/desktop/api/Wsman/nf-wsman-wsmanreconnectshellcommand). |
| [**WSManReconnectShellCommand**](/windows/desktop/api/Wsman/nf-wsman-wsmanreconnectshellcommand) | Reconnecte une commande précédemment déconnectée.                                                                                                                                   |
| [**WSManRunShellCommand**](/windows/desktop/api/Wsman/nf-wsman-wsmanrunshellcommand)             | Exécute une commande d’interpréteur de commandes.                                                                                                                                                           |
| [**WSManRunShellCommandEx**](/windows/desktop/api/Wsman/nf-wsman-wsmanrunshellcommandex)         | Fournit les mêmes fonctionnalités que la fonction [**WSManRunShellCommand**](/windows/desktop/api/Wsman/nf-wsman-wsmanrunshellcommand) , avec l’ajout d’une option d’ID de commande.                                 |
| [**WSManSendShellInput**](/windows/desktop/api/Wsman/nf-wsman-wsmansendshellinput)               | Envoie l’entrée à un shell.                                                                                                                                                         |
| [**WSManSignalShell**](/windows/desktop/api/Wsman/nf-wsman-wsmansignalshell)                     | Signale un shell.                                                                                                                                                                |



 

 

 




