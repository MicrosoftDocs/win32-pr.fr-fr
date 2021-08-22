---
title: Structures et définitions de l’API de l’interpréteur de commandes client
description: le tableau suivant fournit une vue d’ensemble des structures et des autres définitions pour l’API d’environnement Client du Windows Remote Management (WinRM).
ms.assetid: b7a3c92e-6796-482f-9d70-18a48cce4ad8
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c9c3d1f6f9f9d476e9b49ef309e5236e4421e0b5afa77fa1072b92f2060cfcd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119643259"
---
# <a name="client-shell-api-structures-and-definitions"></a>Structures et définitions de l’API de l’interpréteur de commandes client

le tableau suivant fournit une vue d’ensemble des structures et des autres définitions pour l’API d’environnement Client du Windows Remote Management (WinRM).



| Fonction                                                                      | Description                                                                                  |
|-------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [**fonction d’achèvement de l’interpréteur de commandes WSMAN \_ \_ \_**](/windows/win32/api/wsman/nc-wsman-wsman_shell_completion_function) | Fonction de rappel qui est appelée pour les opérations de Shell, qui entraînent une demande distante. |



 



| Structure                                                                      | Description                                                                                                                                 |
|--------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_ \_ informations d’identification de l’authentification WSMan**](/windows/desktop/api/Wsman/ns-wsman-wsman_authentication_credentials) | Définit la méthode d’authentification et les informations d’identification utilisées pour l’authentification du serveur ou du proxy.                                              |
| [**\_données WSMan**](/windows/desktop/api/Wsman/ns-wsman-wsman_data)                                              | Stocke les données entrantes et sortantes utilisées dans l’API WinRM.                                                                                     |
| [**\_fichier binaire de données WSMan \_**](/windows/desktop/api/Wsman/ns-wsman-wsman_data_binary)                               | Stocke des données binaires pour une utilisation avec diverses fonctions de l’API WinRM.                                                                                |
| [**\_texte de données WSMan \_**](/windows/desktop/api/Wsman/ns-wsman-wsman_data_text)                                   | Stocke des données textuelles pour une utilisation avec diverses fonctions de l’API WinRM.                                                                            |
| [**\_variable d’environnement WSMan \_**](/windows/desktop/api/Wsman/ns-wsman-wsman_environment_variable)             | Définit une variable d’environnement individuelle à l’aide d’une paire nom/valeur.                                                                  |
| [**\_variable d’environnement WSMan \_ \_ définie**](/windows/desktop/api/Wsman/ns-wsman-wsman_environment_variable_set)    | Définit un tableau de variables d’environnement.                                                                                                  |
| [**\_erreur WSMan**](/windows/desktop/api/Wsman/ns-wsman-wsman_error)                                     | Contient des informations sur l’erreur.                                                                                                                 |
| [**\_clé WSMan**](/windows/desktop/api/Wsman/ns-wsman-wsman_key)                                                | Représente une paire clé/valeur dans un jeu de sélecteurs et est utilisé pour identifier une ressource particulière.                                       |
| [**WSMAN \_ (option)**](/windows/desktop/api/Wsman/ns-wsman-wsman_option)                                          | Représente un nom d’option et une paire de valeurs spécifiques.                                                                                           |
| [**\_option WSMan \_ définie**](/windows/desktop/api/Wsman/ns-wsman-wsman_option_set)                                 | Représente un ensemble d’options.                                                                                                                |
| [**\_informations sur le proxy WSMan \_**](/windows/desktop/api/Wsman/ns-wsman-wsman_proxy_info)                                 | Définit les informations de proxy pour chaque session.                                                                                                |
| [**résultat de la \_ réception de \_ données WSMan \_**](/windows/desktop/api/Wsman/ns-wsman-wsman_receive_data_result)              | Représente les données de sortie reçues de l’API [**WSManReceiveShellOutput**](/windows/desktop/api/Wsman/nf-wsman-wsmanreceiveshelloutput) .                                |
| [**\_données de réponse WSMan \_**](/windows/desktop/api/Wsman/ns-wsman-wsman_response_data)                           | Représente les données de sortie reçues d’une opération [**WSMan**](wsman.md) .                                                                |
| [**\_jeu de sélecteurs WSMan \_**](/windows/desktop/api/Wsman/ns-wsman-wsman_selector_set)                             | Définit un jeu de clés qui représentent l’identité d’une ressource.                                                                            |
| [**WSMAN \_ Shell \_ Async**](/windows/desktop/api/Wsman/ns-wsman-wsman_shell_async)                               | Définit une structure asynchrone qui est passée à toutes les opérations de Shell.                                                                   |
| [**\_informations de \_ déconnexion de l’interpréteur de commandes WSMan \_**](/windows/desktop/api/Wsman/ns-wsman-wsman_shell_disconnect_info)          | TBD                                                                                                                                         |
| [**informations de démarrage de WSMAN \_ Shell \_ \_**](/windows/desktop/api/Wsman/ns-wsman-wsman_shell_startup_info_v10)                | Stocke toutes les données spécifiques au shell nécessaires à la création d’un shell à l’aide de l’appel de plug-in [**WSManCreateShell**](/windows/desktop/api/Wsman/nf-wsman-wsmancreateshell) . |
| [**\_ID de flux WSMan \_ \_ défini**](/windows/desktop/api/Wsman/ns-wsman-wsman_stream_id_set)                          | Répertorie tous les flux utilisés pour l’entrée ou la sortie pour le shell et les commandes.                                                  |
| [**\_ID \_ de mot de passe du nom d’utilisateur WSMan \_**](/windows/desktop/api/Wsman/ns-wsman-wsman_username_password_creds)      | Définit les informations d’identification utilisées pour l’authentification.                                                                                            |



 

 

 