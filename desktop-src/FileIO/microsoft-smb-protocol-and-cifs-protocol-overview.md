---
description: Décrit l’implémentation Microsoft du protocole SMB (Server Message Block).
ms.assetid: 641017fa-3721-40aa-b13c-e26c8b61ce5c
title: Vue d’ensemble du protocole SMB Microsoft et du protocole CIFS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30326221694ce843733f6da7a6ad49c8dff336ec
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127009915"
---
# <a name="microsoft-smb-protocol-and-cifs-protocol-overview"></a>Vue d’ensemble du protocole SMB Microsoft et du protocole CIFS

le protocole smb (Server Message Block) est un protocole de partage de fichiers réseau, et tel qu’il est implémenté dans microsoft Windows est appelé protocole SMB microsoft. L’ensemble des paquets de messages qui définissent une version particulière du protocole est appelé un dialecte. Le protocole CIFS (Common Internet File System) est un dialecte de SMB. SMB et CIFS sont également disponibles sur les machines virtuelles, plusieurs versions d’UNIX et d’autres systèmes d’exploitation.

Les informations techniques de référence sur CIFS sont disponibles auprès de Microsoft Corporation au [protocole d’accès aux fichiers CIFS (Common Internet File System)](/openspecs/windows_protocols/ms-cifs/d416ff7c-c536-406e-a951-4f04b2fd1d2b).

Bien que son rôle principal soit le partage de fichiers, la fonctionnalité de protocole SMB Microsoft supplémentaire comprend les éléments suivants :

-   [Négociation de dialecte](microsoft-smb-protocol-dialects.md)
-   Détermination d’autres serveurs de protocole SMB Microsoft sur le réseau ou exploration réseau
-   Impression sur un réseau
-   [Authentification d’accès aux fichiers, aux répertoires et aux partages](microsoft-smb-protocol-authentication.md)
-   Verrouillage des fichiers et des enregistrements
-   Notification de modification de fichier et de répertoire
-   Gestion des attributs de fichiers étendus
-   Prise en charge d’Unicode
-   [Verrous opportunistes](opportunistic-locks.md)

Dans le modèle de mise en réseau OSI, le protocole SMB Microsoft est le plus souvent utilisé comme couche d’application ou protocole de couche de présentation, et il s’appuie sur des protocoles de niveau inférieur pour le transport. Le protocole de couche de transport le plus souvent utilisé par le protocole SMB Microsoft avec est NetBIOS sur TCP/IP ([NBT](/previous-versions//bb870909(v=vs.85))). Toutefois, le protocole SMB Microsoft peut également être utilisé sans un protocole de transport distinct, la combinaison protocole/NBT de Microsoft est généralement utilisée à des fins de compatibilité descendante.

Le protocole SMB Microsoft est une implémentation client-serveur et se compose d’un ensemble de paquets de données, chacun contenant une requête envoyée par le client ou une réponse envoyée par le serveur. Ces paquets peuvent être largement classés comme suit :

-   Les paquets de contrôle de session établissent et interrompent une connexion aux ressources du serveur partagé.
-   Les paquets d’accès aux fichiers accèdent à et manipulent des fichiers et des répertoires sur le serveur distant.
-   Les paquets de messages généraux envoient des données à des files d’attente d’impression, des mailslots et des canaux nommés, et fournissent des données sur l’état des files d’attente à l’impression.

Certains paquets de messages peuvent être regroupés et envoyés dans une transmission pour réduire la latence de la réponse et augmenter la bande passante réseau. C’est ce que l’on appelle le « traitement par lot ». la section [scénario de Exchange de paquets du protocole smb microsoft](microsoft-smb-protocol-packet-exchange-scenario.md) décrit un exemple de session de protocole smb microsoft qui utilise le traitement par lots de paquets.

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                                                             | Description                                                                                                                                                                                                                                                                 |
|-------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Dialectes du protocole SMB Microsoft](microsoft-smb-protocol-dialects.md)<br/>                                 | Pour établir une connexion entre un client et un serveur à l’aide du protocole SMB Microsoft, vous devez d’abord déterminer le dialecte avec le plus haut niveau de fonctionnalité pris en charge par le client et le serveur.<br/>                                                      |
| [Authentification du protocole SMB Microsoft](microsoft-smb-protocol-authentication.md)<br/>                     | Le modèle de sécurité utilisé dans le protocole SMB Microsoft est identique à celui utilisé par d’autres variantes de SMB et se compose de deux niveaux d’utilisateur et de partage de sécurité. Un partage est un fichier, un répertoire ou une imprimante accessible par les clients du protocole SMB Microsoft.<br/> |
| [scénario de Exchange de paquets de protocole SMB Microsoft](microsoft-smb-protocol-packet-exchange-scenario.md)<br/> | Exemple d’échange de paquets de protocole SMB Microsoft entre un client et un serveur.<br/>                                                                                                                                                                               |



 

 

