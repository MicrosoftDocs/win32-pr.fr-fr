---
title: Événements System-Level et Object-Level
description: Microsoft Active Accessibility utilise trois classes de niveau système WinEvents, de niveau objet et de console.
ms.assetid: 3333fe6c-38cd-4e7e-be4b-94c9f824e7e7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0d14a0469527a7654dd3e323adb47d650866ca9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309741"
---
# <a name="system-level-and-object-level-events"></a>Événements System-Level et Object-Level

Microsoft Active Accessibility utilise trois classes de WinEvents : *au niveau du système*, au niveau de l' *objet* et à la *console*. Chacun a l’une des valeurs de [constantes d’événement](event-constants.md) correspondantes suivantes :

-   Les constantes d’événement qui commencent par \_ le système d’événements identifient les événements au niveau du système. Ces événements décrivent les situations qui affectent toutes les applications dans le système.
-   Les constantes d’événement qui commencent par l’objet d’événement \_ identifient les événements de niveau objet. Ces événements se rapportent à des situations spécifiques aux objets au sein d’une même application.
-   Les constantes d’événement qui commencent par la console d’événements \_ identifient les événements au niveau de la console. Ces événements indiquent des modifications dans les fenêtres de la console.

Les classes d’événements système et de niveau objet sont toutes les deux générées par le système d’exploitation et les applications serveur. Le système d’exploitation génère des événements au niveau du système et de l’objet pour les scénarios suivants :

-   Notifications à l’ensemble du système concernant les changements de focus
-   Modifications de l’activation
-   Événements relatifs aux objets fournis par le système, tels que les contrôles communs

Les applications serveur génèrent des événements de niveau système pour les objets personnalisés qui répliquent des objets système, tels que des menus personnalisés et des barres de défilement.

Les applications serveur génèrent généralement des événements de niveau objet pour les modifications apportées aux objets accessibles qu’ils contiennent, tels que la création d’objets, la destruction et la sélection.

Bien que le système génère des événements de niveau objet pour les objets [**Window**](window.md) , les serveurs doivent également envoyer des événements de niveau objet pour chaque objet accessible contenu dans une fenêtre. Par exemple, si une application serveur inscrit une classe de fenêtre définie par l’application pour créer un contrôle personnalisé, le système génère des événements de niveau objet pour la fenêtre qui contient le contrôle personnalisé ; le serveur génère des événements de niveau objet pour l’objet accessible qui fournit des informations sur le contrôle.

Les serveurs génèrent uniquement des événements de niveau objet pour les contrôles personnalisés pour lesquels ils implémentent l’interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) . Pour plus d’informations, consultez [éléments d’interface utilisateur personnalisés](custom-user-interface-elements.md).

 

 




