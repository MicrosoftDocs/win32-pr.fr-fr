---
title: Exemple de page Web inclus avec le contrôle ActiveX Bureau à distance
description: Un exemple de page Web (Default.htm) se trouve dans le répertoire d’installation de Connexion Bureau à distance par le Web.
ms.assetid: 3137f58b-1aec-4bd6-a3b2-d1db6c8b96e4
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dec07ee86dcb5d10dc289e8095c83771ebe9a8b0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310242"
---
# <a name="sample-webpage-included-with-the-remote-desktop-activex-control"></a>Exemple de page Web inclus avec le contrôle ActiveX Bureau à distance

Lorsque vous installez le contrôle Bureau à distance ActiveX de Connexion Bureau à distance par le Web, un exemple de page Web (Default.htm) est copié dans le répertoire d’installation de Connexion Bureau à distance par le Web. Cette page peut être exécutée telle quelle ou personnalisée pour répondre aux besoins d’un utilisateur ou d’une organisation.

L’exemple de page Web doit être installé sur un serveur Web exécutant Windows Server et Internet Information Server 4,0 ou version ultérieure. En outre, le navigateur sur l’ordinateur client doit être Internet Explorer version 4,0 ou ultérieure. Pour plus d’informations, consultez [Configuration requise pour connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).

Default.htm est une page Web de connexion par défaut qui recueille les informations de connexion de l’utilisateur. La page d’ouverture de session contient un champ obligatoire dans lequel l’utilisateur entre le nom de l’hôte de session Bureau à distance (hôte de session Bureau à distance) ou un ordinateur distant auquel se connecter. La page de connexion inclut également des champs facultatifs pour la taille de l’écran et les informations d’ouverture de session utilisateur, y compris le nom d’utilisateur et le domaine.

Après avoir collecté les données utilisateur, Default.htm les transmet au contrôle ActiveX Bureau à distance (msrdp. ocx) pour initier une session Bureau à distance. Les étapes à suivre pour initier la session sont les suivantes :

1.  Si nécessaire, Internet Explorer télécharge le fichier. cab et l’installe sur l’ordinateur de l’utilisateur.
2.  L’utilisateur entre le nom de domaine complet ou l’adresse IP de l’ordinateur distant dans le champ approprié.

    -   L’utilisateur peut éventuellement spécifier une taille d’écran pour la connexion. Si l’utilisateur ne spécifie pas de taille d’écran, la session s’ouvre en mode plein écran si l’utilisateur se trouve dans une zone de sécurité d’URL approuvée. Dans le cas contraire, la session s’ouvre en mode fenêtre.
    -   L’utilisateur peut éventuellement fournir des informations d’ouverture de session automatique (nom d’utilisateur, domaine) pour la session à distance.

3.  Quand l’utilisateur clique sur le bouton **se connecter** , Default.htm transmet les données fournies par l’utilisateur en tant que paramètres au contrôle ActiveX Bureau à distance.
4.  Le Bureau à distance s’ouvre dans la fenêtre du navigateur ou en mode plein écran, comme spécifié par l’utilisateur.

Quand Default.htm s’ouvre pour la première fois à l’aide d’Internet Explorer, une boîte de dialogue s’affiche, donnant à l’utilisateur la possibilité de télécharger le contrôle Bureau à distance ActiveX (msrdp. ocx). La boîte de dialogue s’affiche dans les conditions suivantes :

-   L’ordinateur qui a accédé à la page Web ne dispose pas d’une installation complète du client Connexion Bureau à distance par le Web (ou du Services Bureau à distance client avancé) avec prise en charge du Web.
-   La version installée du fichier. cab sur l’ordinateur client est antérieure à la version de la page Web Default.htm.

La taille de la session Bureau à distance qui s’affiche dans la fenêtre du navigateur correspond à la taille spécifiée dans la page Web Default.htm. Pour modifier la taille de l’écran, l’utilisateur doit se déconnecter de la session, revenir à la page Web Default.htm et modifier les informations de connexion. Si aucune taille d’écran n’a été spécifiée, la session s’ouvre dans la fenêtre du navigateur en mode plein écran par défaut. À cette résolution, le Bureau à distance se développe pour correspondre aux dimensions complètes de l’écran de l’utilisateur et les barres d’outils et les cadres de fenêtres du navigateur Internet Explorer ne s’affichent pas. Comme avec le client complet Connexion Bureau à distance, l’utilisateur peut basculer entre le mode plein écran et le mode fenêtre en appuyant sur la combinaison de [touches de raccourci](terminal-services-shortcut-keys.md) en mode plein écran (Ctrl + Alt + Attn).

Pour des raisons de sécurité, certaines options disponibles dans le gestionnaire de connexions Services Bureau à distance sont limitées dans le contrôle ActiveX Bureau à distance à certaines zones de sécurité d’URL Internet Explorer. Pour plus d’informations sur ces options et sur la spécification d’un programme à exécuter lors de la connexion, reportez-vous à la rubrique [fourniture de la sécurité du client RDP](providing-for-rdp-client-security.md) .

 

 




