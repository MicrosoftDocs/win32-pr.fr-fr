---
title: exemple de page web inclus avec le contrôle de ActiveX Bureau à distance
description: Un exemple de page Web (Default.htm) se trouve dans le répertoire d’installation de Connexion Bureau à distance par le Web.
ms.assetid: 3137f58b-1aec-4bd6-a3b2-d1db6c8b96e4
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dec07ee86dcb5d10dc289e8095c83771ebe9a8b0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127324513"
---
# <a name="sample-webpage-included-with-the-remote-desktop-activex-control"></a>exemple de page web inclus avec le contrôle de ActiveX Bureau à distance

lorsque vous installez le contrôle Bureau à distance ActiveX de Connexion Bureau à distance par le Web, un exemple de page web (Default.htm) est copié dans le répertoire d’installation de Connexion Bureau à distance par le Web. Cette page peut être exécutée telle quelle ou personnalisée pour répondre aux besoins d’un utilisateur ou d’une organisation.

l’exemple de page web doit être installé sur un serveur web exécutant Windows server et Internet Information server 4,0 ou version ultérieure. En outre, le navigateur sur l’ordinateur client doit être Internet Explorer version 4,0 ou ultérieure. Pour plus d’informations, consultez [Configuration requise pour connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).

Default.htm est une page Web de connexion par défaut qui recueille les informations de connexion de l’utilisateur. La page d’ouverture de session contient un champ obligatoire dans lequel l’utilisateur entre le nom de l’hôte de session Bureau à distance (hôte de session Bureau à distance) ou un ordinateur distant auquel se connecter. La page de connexion inclut également des champs facultatifs pour la taille de l’écran et les informations d’ouverture de session utilisateur, y compris le nom d’utilisateur et le domaine.

après avoir collecté les données utilisateur, Default.htm les transmet au contrôle Bureau à distance ActiveX (Msrdp. ocx) pour initier une session bureau à distance. Les étapes à suivre pour initier la session sont les suivantes :

1.  Si nécessaire, Internet Explorer télécharge le fichier .cab et l’installe sur l’ordinateur de l’utilisateur.
2.  L’utilisateur entre le nom de domaine complet ou l’adresse IP de l’ordinateur distant dans le champ approprié.

    -   L’utilisateur peut éventuellement spécifier une taille d’écran pour la connexion. Si l’utilisateur ne spécifie pas de taille d’écran, la session s’ouvre en mode plein écran si l’utilisateur se trouve dans une zone de sécurité d’URL approuvée. Dans le cas contraire, la session s’ouvre en mode fenêtre.
    -   L’utilisateur peut éventuellement fournir des informations d’ouverture de session automatique (nom d’utilisateur, domaine) pour la session à distance.

3.  quand l’utilisateur clique sur le bouton **Connecter** , Default.htm passe les données fournies par l’utilisateur en tant que paramètres au contrôle de ActiveX Bureau à distance.
4.  Le Bureau à distance s’ouvre dans la fenêtre du navigateur ou en mode plein écran, comme spécifié par l’utilisateur.

quand Default.htm s’ouvre pour la première fois à l’aide d’Internet Explorer, une boîte de dialogue s’affiche et permet à l’utilisateur de télécharger le contrôle Bureau à distance ActiveX (Msrdp. ocx). La boîte de dialogue s’affiche dans les conditions suivantes :

-   L’ordinateur qui a accédé à la page Web ne dispose pas d’une installation complète du client Connexion Bureau à distance par le Web (ou du Services Bureau à distance client avancé) avec prise en charge du Web.
-   La version installée du fichier .cab sur l’ordinateur client est antérieure à la version de la page Web Default.htm.

La taille de la session Bureau à distance qui s’affiche dans la fenêtre du navigateur correspond à la taille spécifiée dans la page Web Default.htm. Pour modifier la taille de l’écran, l’utilisateur doit se déconnecter de la session, revenir à la page Web Default.htm et modifier les informations de connexion. Si aucune taille d’écran n’a été spécifiée, la session s’ouvre dans la fenêtre du navigateur en mode plein écran par défaut. À cette résolution, le Bureau à distance se développe pour correspondre aux dimensions complètes de l’écran de l’utilisateur et les barres d’outils et les cadres de fenêtres du navigateur Internet Explorer ne s’affichent pas. Comme avec le client complet Connexion Bureau à distance, l’utilisateur peut basculer entre le mode plein écran et le mode fenêtre en appuyant sur la combinaison de [touches de raccourci](terminal-services-shortcut-keys.md) en mode plein écran (Ctrl + Alt + Attn).

pour des raisons de sécurité, certaines options disponibles dans le gestionnaire de connexions Services Bureau à distance sont limitées dans la Bureau à distance ActiveX contrôle à certaines zones de sécurité URL d’Internet Explorer. Pour plus d’informations sur ces options et sur la spécification d’un programme à exécuter lors de la connexion, reportez-vous à la rubrique [fourniture de la sécurité du client RDP](providing-for-rdp-client-security.md) .

 

 




