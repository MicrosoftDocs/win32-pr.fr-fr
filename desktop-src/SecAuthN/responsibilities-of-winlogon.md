---
description: Répertorie et explique les responsabilités de Winlogon.
ms.assetid: 5aef4164-11bd-4acc-b851-de982e35d2b5
title: Responsabilités de Winlogon
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6561bea11c48eb474c0ff56c5c0aa5ebfa0c22d9d6689aa55a6a208bbbc683e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118919027"
---
# <a name="responsibilities-of-winlogon"></a>Responsabilités de Winlogon

[*Winlogon*](../secgloss/w-gly.md) a les responsabilités suivantes :

-   Station Windows et protection des postes de travail

    Winlogon définit la protection de la station Windows et des postes de travail correspondants pour s’assurer que chacun d’eux est correctement accessible. En général, cela signifie que le système local aura un accès complet à ces objets et qu’un utilisateur connecté de manière interactive aura un accès en lecture à l’objet de station Windows et un accès complet à l’objet de bureau de l’application.

-   Reconnaissance SAS standard

    Winlogon dispose de hooks spéciaux dans le serveur User32 qui lui permettent de surveiller les événements de séquence de touches de [*sécurité*](../secgloss/s-gly.md) (SAS) Ctrl + Alt + Suppr. Winlogon rend ces informations d’événement SAP accessibles aux GINA pour les utiliser en tant que SAP, ou dans le cadre de leur SAS. En règle générale, les GINA doivent surveiller les propres SASss. Toutefois, toute [*Gina*](../secgloss/g-gly.md) avec la combinaison de touches Ctrl + Alt + Del standard comme l’une des sociétés reconnues par l’informatique Sass doit utiliser la prise en charge de Winlogon fournie à cet effet.

-   Distribution de routine SAS

    Lorsque Winlogon rencontre un événement SAS ou lorsqu’une signature d’accès partagé est remise à Winlogon par le GINA, Winlogon définit l’État en conséquence, les modifications apportées au bureau Winlogon et appelle l’une des fonctions de traitement SAP du GINA.

-   Chargement du profil utilisateur

    Lorsque les utilisateurs ouvrent une session, leurs profils utilisateur sont chargés dans le registre. De cette façon, les processus de l’utilisateur peuvent utiliser la clé de Registre spéciale HKEY \_ Current \_ User. Winlogon effectue cette opération automatiquement après une ouverture de session réussie, mais avant l’activation de l’interpréteur de commandes pour l’utilisateur qui vient d’être connecté.

-   Attribution de la sécurité à l’interpréteur de commandes utilisateur

    Lorsqu’un utilisateur ouvre une session, GINA est responsable de la création d’un ou plusieurs processus initiaux pour cet utilisateur. Winlogon fournit une fonction de prise en charge pour que le GINA applique la sécurité de l’utilisateur qui vient d’être connecté à ces processus. toutefois, la meilleure façon de procéder est de faire en sorte que GINA appelle la fonction Windows [**CreateProcessAsUser**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera)et laisse le système fournir le service.

-   Contrôle de l’écran de veille

    Winlogon surveille l’activité du clavier et de la souris pour déterminer quand activer les économiseurs d’écran. Une fois l’économiseur d’écran activé, Winlogon continue à surveiller l’activité du clavier et de la souris pour déterminer quand arrêter l’économiseur d’écran. Si l’économiseur d’écran est marqué comme sécurisé, Winlogon traite la station de travail comme étant verrouillée. En cas d’activité de la souris ou du clavier, Winlogon appelle la fonction [**WlxDisplayLockedNotice**](/windows/desktop/api/Winwlx/nf-winwlx-wlxdisplaylockednotice) de la dll Gina et le comportement verrouillé de la station de travail reprend. Si l’économiseur d’écran n’est pas sécurisé, toute activité du clavier ou de la souris met fin à l’économiseur d’écran sans notification à GINA.

-   Prise en charge de plusieurs fournisseurs de réseau

    plusieurs réseaux installés sur un système de Windows peuvent être inclus dans le processus d’authentification et dans les opérations de mise à jour des mots de passe. Cette inclusion permet aux réseaux supplémentaires de collecter des informations d’identification et d’authentification en même temps pendant la connexion normale, à l’aide du Bureau sécurisé de Winlogon. Certains des paramètres requis dans les services Winlogon disponibles pour GINA prennent en charge explicitement ces fournisseurs de réseau supplémentaires.

 

 
