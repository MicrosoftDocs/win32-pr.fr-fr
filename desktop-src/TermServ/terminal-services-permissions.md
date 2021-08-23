---
title: Autorisations de Services Bureau à distance
description: Vous pouvez utiliser les autorisations fournies pour Services Bureau à distance pour contrôler la façon dont les utilisateurs et les groupes accèdent au serveur.
ms.assetid: 448a7f9b-bf12-48eb-a3e7-4512ec288d95
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 668bf4902ffb133c403e5ea2f74bbc165cf99bca500c95eed5d5dac3cb48a710
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999889"
---
# <a name="remote-desktop-services-permissions"></a>Autorisations de Services Bureau à distance

Vous pouvez utiliser les autorisations fournies pour Services Bureau à distance pour contrôler la façon dont les utilisateurs et les groupes accèdent au serveur. Pour obtenir une description des types d’autorisation par défaut et des informations plus détaillées sur les autorisations de Services Bureau à distance en général, consultez la documentation qui accompagne l’outil d’administration de la configuration Services Bureau à distance. pour plus d’informations sur la configuration de ces autorisations pour Windows Server 2008, consultez [configurer des autorisations pour les connexions Services Bureau à distance](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc753032(v=ws.11)).

Voici une liste des autorisations que vous pouvez définir et des tâches que les autorisations autorisent.



| Valeur                        | Signification                                                                                                                                                               |
|------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Informations sur la requête<br/> | Interroger les sessions et les serveurs pour plus d’informations.<br/>                                                                                                                |
| Définir des informations<br/>   | Configurez les propriétés de connexion.<br/>                                                                                                                           |
| Contrôle à distance<br/>    | Afficher ou contrôler activement la session d’un autre utilisateur.<br/>                                                                                                           |
| Ouverture de session<br/>             | Connectez-vous à une session sur le serveur.<br/>                                                                                                                         |
| Fermer la session<br/>            | Déconnecte un utilisateur d’une session. Sachez que la déconnexion d’un utilisateur sans avertissement peut entraîner la perte de données au niveau du client.<br/>                                  |
| Message<br/>           | Envoyer un message aux sessions d’un autre utilisateur.<br/>                                                                                                                 |
| Se connecter<br/>           | Connecter à une autre session.<br/>                                                                                                                                |
| Déconnecter<br/>        | Déconnecter une session.<br/>                                                                                                                                      |
| Canaux virtuels<br/>  | Utiliser des canaux virtuels. Sachez que la désactivation des canaux virtuels désactive certaines fonctionnalités Services Bureau à distance telles que le presse-papiers et la redirection d’imprimante.<br/> |
| Réinitialiser<br/>             | Mettre fin à une session. N’oubliez pas que la fin d’une session sans avertissement peut entraîner la perte de données au niveau du client.<br/>                                                    |



 

L’autorisation Logon est requise pour qu’un utilisateur se connecte à une nouvelle session de Services Bureau à distance. Toutes les autres Services Bureau à distance autorisations s’appliquent pour contrôler la session de Services Bureau à distance d’un autre utilisateur.

Services Bureau à distance autorisations peuvent être accordées ou définies pour des utilisateurs individuels ou des groupes. Les utilisateurs peuvent également hériter des autorisations à la suite d’un membre de groupe. Toutefois, le refus d’une autorisation remplace une autorisation héritée. Par exemple, les membres du groupe Bureau à distance utilisateurs (RDU) disposent de l’autorisation de requête par défaut. Si un administrateur définit l’autorisation de requête sur « refuser » pour cet utilisateur, l’utilisateur ne sera pas en mesure d’interroger la session d’un autre utilisateur. Une fois qu’un utilisateur se connecte à une session, l’utilisateur se voit accorder toutes les autres Services Bureau à distance autorisations pour sa session.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Applications de gestion de Services Bureau à distance](terminal-services-management-applications.md)
</dt> <dt>

[**\_TSAccount Win32**](win32-tsaccount.md)
</dt> </dl>

 

