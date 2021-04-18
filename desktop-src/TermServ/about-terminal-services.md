---
title: À propos de Services Bureau à distance
description: Services Bureau à distance (anciennement services Terminal Server) offre des fonctionnalités similaires à celles d’un environnement de type terminal, d’un ordinateur hôte centralisé ou d’un macroordinateur dans lequel plusieurs terminaux se connectent à un ordinateur hôte.
ms.assetid: 5b5b0f97-f973-4f52-a965-c9c2390e6c8d
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance Services Bureau à distance, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4644170cfca3b4bacdd6db647e35549d56844e9b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106522627"
---
# <a name="about-remote-desktop-services"></a>À propos de Services Bureau à distance

Services Bureau à distance (anciennement services Terminal Server) offre des fonctionnalités similaires à celles d’un environnement de type terminal, d’un ordinateur hôte centralisé ou d’un macroordinateur dans lequel plusieurs terminaux se connectent à un ordinateur hôte. Chaque terminal fournit un canal d’entrée et de sortie entre un utilisateur et l’ordinateur hôte. Un utilisateur peut ouvrir une session sur un terminal, puis exécuter des applications sur l’ordinateur hôte, accéder à des fichiers, des bases de données, des ressources réseau, etc. Chaque session de terminal est indépendante, avec le système d’exploitation hôte qui gère les conflits entre plusieurs utilisateurs qui ont des ressources partagées.

La principale différence entre les Services Bureau à distance et l’environnement de macroordinateur traditionnel est que les terminaux passifs dans un environnement de macroordinateur fournissent uniquement une entrée et une sortie basées sur des caractères. Un client ou un émulateur Connexion Bureau à distance (RDC) fournit une interface utilisateur graphique complète comprenant un bureau du système d’exploitation Windows et la prise en charge d’un large éventail de périphériques d’entrée, tels qu’un clavier et une souris.

Dans l’environnement de Services Bureau à distance, une application s’exécute entièrement sur le serveur hôte de session Bureau à distance (hôte de session Bureau à distance) (anciennement appelé Terminal Server). Le client RDC n’effectue aucun traitement local des logiciels d’application. Le serveur transmet l’interface utilisateur graphique au client. Le client transmet à nouveau l’entrée de l’utilisateur au serveur.

Pour plus d'informations, consultez les rubriques ci-dessous.

## <a name="in-this-section"></a>Dans cette section

<dl> <dt>

[Modifier la valeur par défaut de la redirection de périphérique](modify-device-redirection-default-.md)
</dt> <dd>

Étant donné que les serveurs de passerelle Bureau à distance tentent d’appliquer des stratégies de redirection de périphérique sécurisées avant de transmettre la connexion cliente à un serveur hôte de session Bureau à distance, vous devrez peut-être désactiver ce paramètre par défaut dans certains cas.

</dd> <dt>

[Protocole RDP (Remote Desktop Protocol)](remote-desktop-protocol.md)
</dt> <dd>

Le protocole RDP (Bureau à distance Microsoft Protocol) fournit des fonctionnalités d’affichage et d’entrée à distance sur les connexions réseau pour les applications Windows exécutées sur un serveur.

</dd> <dt>

[API Services Bureau à distance](terminal-services-api.md)
</dt> <dd>

L’API Services Bureau à distance est surtout utile pour les applications client/serveur et les applications pour l’administration des Services Bureau à distance.

</dd> <dt>

[Applications de gestion de Services Bureau à distance](terminal-services-management-applications.md)
</dt> <dd>

Décrit les applications de gestion prises en charge par Services Bureau à distance.

</dd> <dt>

[Instructions de programmation Services Bureau à distance](terminal-services-programming-guidelines.md)
</dt> <dd>

Rubriques qui fournissent des instructions pour le développement d’applications dans un environnement de Services Bureau à distance.

</dd> <dt>

[Sessions Bureau à distance](terminal-services-sessions.md)
</dt> <dd>

Étant donné que chaque connexion à un client Connexion Bureau à distance (RDC) reçoit un ID de session distinct, l’expérience utilisateur est semblable à la connexion à plusieurs ordinateurs en même temps. par exemple, un ordinateur de bureau et un ordinateur privé.

</dd> <dt>

[Connexion Bureau à distance par le Web](remote-desktop-web-connection.md)
</dt> <dd>

Décrit comment installer un Connexion Bureau à distance par le Web.

</dd> <dt>

[Ressources sur un serveur hôte de session Bureau à distance](resources-on-a-terminal-server.md)
</dt> <dd>

Plusieurs utilisateurs peuvent se connecter simultanément à un seul serveur hôte de session Bureau à distance, en partageant les ressources matérielles et logicielles du serveur.

</dd> <dt>

[Nouveautés de Services Bureau à distance](what-s-new-in-terminal-services.md)
</dt> <dd>

Rubriques qui décrivent les modifications apportées à chaque version de l’API Services Bureau à distance.

</dd> </dl>

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Se connecter à un autre ordinateur à l’aide de Connexion Bureau à distance](https://windows.microsoft.com/windows/connect-using-remote-desktop-connection#connect-using-remote-desktop-connection=windows-7)
</dt> </dl>

 

 




