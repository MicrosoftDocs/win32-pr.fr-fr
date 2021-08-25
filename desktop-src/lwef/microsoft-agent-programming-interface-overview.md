---
title: Vue d’ensemble de l’interface de programmation Microsoft Agent
description: Vue d’ensemble de l’interface de programmation Microsoft Agent
ms.assetid: 8709441b-9739-4f11-a2de-40a5f5eefb72
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73e4dc087064afb0e3beaaf97d987e496239d3fd378461acaf5601927ac6d929
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119887919"
---
# <a name="microsoft-agent-programming-interface-overview"></a>Vue d’ensemble de l’interface de programmation Microsoft Agent

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

L’API Microsoft Agent fournit des services qui prennent en charge l’affichage et l’animation de caractères animés. Implémenté comme un serveur com OLE Automation (Component Object Model \[ \] ), Microsoft Agent permet à plusieurs applications, appelées clients ou applications clientes, d’héberger et d’accéder en même temps à ses services d’animation, d’entrée et de sortie. Un client peut être n’importe quelle application qui se connecte aux interfaces COM de Microsoft Agent.

En tant que serveur COM, Microsoft Agent démarre automatiquement uniquement lorsqu’une application cliente utilise les interfaces COM et les demandes pour s’y connecter. Il reste en cours d’exécution jusqu’à ce que tous les clients ferment leurs connexions. Quand aucun client connecté n’est conservé, Microsoft Agent se ferme automatiquement.

bien que vous puissiez appeler les interfaces COM de microsoft agent directement, microsoft agent comprend également un contrôle microsoft ActiveX. ce contrôle facilite l’accès aux services de Microsoft Agent à partir de langages de programmation qui prennent en charge l’interface de contrôle ActiveX.

outre la prise en charge des programmes autonomes écrits pour Windows, l’Agent peut être écrit pour prendre en charge les pages web, à condition que le navigateur prenne en charge l’interface ActiveX. Microsoft Internet Explorer prend en charge les ActiveX, ainsi que les langages de script que vous pouvez utiliser pour programmer l’Agent. Si vous n’utilisez pas Internet Explorer, contactez votre fournisseur ou fournisseur à propos de la prise en charge de ActiveX par le navigateur.

Les informations suivantes fournissent une brève vue d’ensemble des interfaces de programmation pour le logiciel Microsoft Agent.

-   [Services d’animation](animation-services.md)
-   [Services d’entrée](input-services.md)
-   [Fenêtre commandes vocales](the-voice-commands-window.md)
-   [Services de sortie](output-services.md)

 

 




