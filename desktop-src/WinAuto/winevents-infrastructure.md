---
title: Infrastructure WinEvents
description: Le système d’exploitation Microsoft Windows comprend une fonctionnalité, appelée WinEvents, qui permet aux processus et aux applications qui s’exécutent sur le bureau Windows d’échanger certains types d’informations.
ms.assetid: ba97b00b-4a4c-4889-ae9c-8e92eb742849
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8846582a6d18f304cc08e3cb13ddb444cb278d7
ms.sourcegitcommit: 85688bbfbe5b121bc05ddf112d54c23a469dfbc0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/29/2020
ms.locfileid: "103679545"
---
# <a name="winevents"></a>WinEvents

Le système d’exploitation Microsoft Windows comprend une fonctionnalité, appelée *winEvents*, qui permet aux processus et aux applications qui s’exécutent sur le bureau Windows d’échanger certains types d’informations. Les outils d’accessibilité qui utilisent Microsoft UI Automation et Microsoft Active Accessibility font partie des principaux utilisateurs de WinEvents.

Dans le contexte de l’accessibilité, les fournisseurs UI Automation et les serveurs Microsoft Active Accessibility utilisent WinEvents pour informer les clients des modifications apportées à l’interface utilisateur d’une application, par exemple lorsqu’un élément d’interface utilisateur a été créé ou détruit, ou lorsqu’un nom d’élément, un État ou une valeur a changé.

Cette section fournit des suggestions, des instructions et des exemples pour aider les clients à gérer les WinEvents et à aider les serveurs à déterminer quand déclencher le WinEvent approprié.

## <a name="in-this-section"></a>Dans cette section

-   [Qu’est-ce que WinEvents ?](what-are-winevents.md)
-   [Inscription d’une fonction de raccordement](registering-a-hook-function.md)
-   [Événements de niveau système et de Object-Level](system-level-and-object-level-events.md)
-   [Fonctions de raccordement dans le contexte et hors contexte](in-context-and-out-of-context-hook-functions.md)
-   [Protection contre la réentrance dans les fonctions de raccordement](guarding-against-reentrancy-in-hook-functions.md)
-   [Allocation d’ID WinEvent](allocation-of-winevent-ids.md)

Pour obtenir une vue d’ensemble du processus de notification d’événements dans Microsoft Active Accessibility, voir [winEvents](winevents-overview.md) dans la [vue d’ensemble technique](technical-overview.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Infrastructure commune](common-infrastructure.md)
</dt> </dl>

 

 




