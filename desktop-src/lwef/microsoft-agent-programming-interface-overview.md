---
title: Vue d’ensemble de l’interface de programmation Microsoft Agent
description: Vue d’ensemble de l’interface de programmation Microsoft Agent
ms.assetid: 8709441b-9739-4f11-a2de-40a5f5eefb72
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad89249e064eb89d37f497fb79cb8982c79cb83c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840098"
---
# <a name="microsoft-agent-programming-interface-overview"></a>Vue d’ensemble de l’interface de programmation Microsoft Agent

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

L’API Microsoft Agent fournit des services qui prennent en charge l’affichage et l’animation de caractères animés. Implémenté comme un serveur com OLE Automation (Component Object Model \[ \] ), Microsoft Agent permet à plusieurs applications, appelées clients ou applications clientes, d’héberger et d’accéder en même temps à ses services d’animation, d’entrée et de sortie. Un client peut être n’importe quelle application qui se connecte aux interfaces COM de Microsoft Agent.

En tant que serveur COM, Microsoft Agent démarre automatiquement uniquement lorsqu’une application cliente utilise les interfaces COM et les demandes pour s’y connecter. Il reste en cours d’exécution jusqu’à ce que tous les clients ferment leurs connexions. Quand aucun client connecté n’est conservé, Microsoft Agent se ferme automatiquement.

Bien que vous puissiez appeler les interfaces COM de Microsoft agent directement, Microsoft Agent comprend également un contrôle Microsoft ActiveX. Ce contrôle facilite l’accès aux services de Microsoft Agent à partir de langages de programmation qui prennent en charge l’interface de contrôle ActiveX.

Outre la prise en charge des programmes autonomes écrits pour Windows, l’agent peut être écrit pour prendre en charge les pages Web, à condition que le navigateur prenne en charge l’interface ActiveX. Microsoft Internet Explorer prend en charge ActiveX ainsi que les langages de script que vous pouvez utiliser pour programmer l’agent. Si vous n’utilisez pas Internet Explorer, contactez votre fournisseur ou fournisseur à propos de la prise en charge d’ActiveX par le navigateur.

Les informations suivantes fournissent une brève vue d’ensemble des interfaces de programmation pour le logiciel Microsoft Agent.

-   [Services d’animation](animation-services.md)
-   [Services d’entrée](input-services.md)
-   [Fenêtre commandes vocales](the-voice-commands-window.md)
-   [Services de sortie](output-services.md)

 

 




