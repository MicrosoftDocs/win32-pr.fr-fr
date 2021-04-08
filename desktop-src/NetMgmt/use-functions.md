---
title: Utiliser des fonctions
description: Les fonctions d’utilisation de la gestion du réseau examinent et gèrent les connexions (utilisations) entre les stations de travail et les serveurs. Les fonctions d’utilisation sont répertoriées ci-dessous.
ms.assetid: ddf1b8dc-f13b-402a-9e4e-e4944a29ac31
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbd2660b911fd87c39b9db10b0dbfea0e47c484c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842638"
---
# <a name="use-functions"></a>Utiliser des fonctions

Les fonctions d’utilisation de la gestion du réseau examinent et gèrent les connexions (utilisations) entre les stations de travail et les serveurs. Les fonctions d’utilisation sont répertoriées ci-dessous.



| Fonction                               | Description                                                                               |
|----------------------------------------|-------------------------------------------------------------------------------------------|
| [**NetUseAdd**](/windows/desktop/api/Lmuse/nf-lmuse-netuseadd)         | Crée une connexion entre un ordinateur local et un serveur.                               |
| [**NetUseDel**](/windows/desktop/api/Lmuse/nf-lmuse-netusedel)         | Met fin à une connexion à une ressource partagée.                                                   |
| [**NetUseEnum**](/windows/desktop/api/Lmuse/nf-lmuse-netuseenum)       | Répertorie toutes les connexions en cours entre l’ordinateur local et les ressources sur les serveurs distants. |
| [**NetUseGetInfo**](/windows/desktop/api/Lmuse/nf-lmuse-netusegetinfo) | Retourne des informations sur une connexion à une ressource partagée.                              |



 

Ces fonctions s’appliquent uniquement au client Server Message Block (station de travail LAN Manager). La fonction **NetUseGetInfo** ne prend pas en charge les partages système de fichiers DFS (DFS). Pour récupérer des informations de connexion pour une ressource partagée à l’aide d’un fournisseur de réseau différent (par exemple, WebDAV ou un partage DFS), utilisez la fonction [**WNetGetConnection**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetgetconnectiona) .

Les connexions se distinguent des sessions : une *session* est établie la première fois qu’une station de travail établit une connexion à une ressource partagée sur le serveur. Toutes les connexions supplémentaires entre la station de travail et le serveur font partie de cette même session jusqu’à la fin de la session. Deux types de connexions peuvent être établies : des connexions de nom d’appareil (qui peuvent uniquement être explicites) et des connexions UNC (Universal-Naming Convention) (qui peuvent être explicites ou implicites).

Les *connexions* sont établies par utilisateur. Une connexion établie par un utilisateur est supprimée lorsque l’utilisateur se déconnecte. Pour cette raison, les fonctions d’utilisation de la gestion du réseau sont locales uniquement, car une connexion configurée par un utilisateur distant n’est pas accessible à d’autres utilisateurs, même l’utilisateur qui a ouvert une session de manière interactive sur cet ordinateur.

La fonction [**NetUseAdd**](/windows/desktop/api/Lmuse/nf-lmuse-netuseadd) établit une connexion explicite entre l’ordinateur local et une ressource partagée sur un serveur en redirigeant un nom de périphérique local vers le nom de partage d’une ressource de serveur distant ( \\ \\ *ServerName* \\ *Nom_Partage*). Une fois qu’une connexion de nom d’appareil est établie, les utilisateurs ou les applications peuvent utiliser la ressource distante en spécifiant le nom de l’appareil local.

Les connexions UNC implicites sont effectuées par la fonction responsable de la connexion. Pour établir une connexion UNC implicite, une application transmet le nom de partage d’une ressource à toute fonction qui accepte les chemins d’accès UNC. La fonction accepte le nom UNC et établit une connexion avec le nom de partage spécifié. Toutes les demandes supplémentaires sur cette connexion requièrent le nom de partage complet.

Les fonctions d’utilisation sont disponibles aux niveaux d’informations suivants :

-   [**Utilisez \_ info \_ 0**](/windows/desktop/api/Lmuse/ns-lmuse-use_info_0)
-   [**UTILISER \_ info \_ 1**](/windows/desktop/api/Lmuse/ns-lmuse-use_info_1)
-   [**Utilisez \_ info \_ 2**](/windows/desktop/api/Lmuse/ns-lmuse-use_info_2)

 

 