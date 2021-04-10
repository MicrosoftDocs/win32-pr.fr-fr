---
title: L’interface utilisateur Edge est supprimée dans les scénarios « in-out-in » et « inertie »
description: L’interface utilisateur Edge est supprimée dans les scénarios « in-out-in » et « inertie »
ms.assetid: 005B6D03-52A6-4780-8D3E-4A5CDA5EED8C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef08eab653349beab0710d59d45bedc2874ced44
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104197330"
---
# <a name="edge-ui-is-suppressed-in-in-out-in-and-inertia-scenarios"></a>L’interface utilisateur Edge est supprimée dans les scénarios « in-out-in » et « inertie »

## <a name="platform"></a>Plateforme

<dl> Clients-Windows 8.1  
</dl>

## <a name="description"></a>Description

Dans certains cas, les utilisateurs peuvent involontairement appeler l’interface utilisateur Edge (icônes, barre d’application, changement d’application). Nous avons introduit une fonctionnalité qui permet aux développeurs de concevoir leur interface utilisateur pour la totalité de l’écran sans faire de intuitivité (par exemple, des bordures) pour empêcher l’utilisateur d’atteindre accidentellement les bords.

Il existe deux cas qui peuvent mener le plus souvent à des balayages d’arête involontaires :

-   Dans la panoramisation rapide, la vitesse et la imprécision de l’interaction peuvent parfois provoquer l’apparition de ces dernières à partir du bord de l’écran
-   Si les utilisateurs quittent et resaisient rapidement la zone d’écran lors de l’écriture manuscrite avec leur doigt, par exemple dans une application de peinture, ce comportement de sortie peut déclencher par erreur l’interface utilisateur du bord et interrompre l’expérience utilisateur.

Pour améliorer l’expérience des utilisateurs et des développeurs, l’interface utilisateur Edge sera désormais supprimée dans deux instances spécifiques :

-   Lorsqu’un utilisateur effectue une panoramisation dans une application qui prend en charge l’inertie de DManip et effectue un balayage en dehors de l’écran pendant l’inertie, l’interface utilisateur du bord n’est pas appelée dans une fenêtre de délai d’attente
-   Sur les appareils certifiés, lorsqu’un utilisateur passe rapidement de l’écran à l’extérieur de l’écran, et vice versa, à l’intérieur de certains paramètres, l’interface utilisateur du bord n’est pas appelée

## <a name="manifestations"></a>Manifestations

Les utilisateurs qui défilent rapidement par rapport à la périphérie lors de l’utilisation d’une application voient une baisse de l’inadvertance de bord involontaire.

## <a name="solution"></a>Solution

Les développeurs doivent garder à l’esprit ces atténuations et doivent être en mesure d’utiliser le plein écran sans craindre que les utilisateurs déclenchent accidentellement l’interface utilisateur Edge tout en interagissant avec l’application le long du bord.

 

 




