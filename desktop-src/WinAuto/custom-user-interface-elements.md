---
title: Éléments d’interface utilisateur personnalisés
description: Les développeurs de serveurs conçoivent des objets accessibles en fonction de l’interface utilisateur d’une application.
ms.assetid: d9453fb0-9b4a-4103-81e3-1255091255a0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b32a086b977a1737a17206261aaaa94faa754d93
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839533"
---
# <a name="custom-user-interface-elements"></a>Éléments d’interface utilisateur personnalisés

Les développeurs de serveurs conçoivent des objets accessibles en fonction de l’interface utilisateur d’une application. Étant donné que [Active Accessibility implémente l’interface IAccessible pour le compte des éléments d’interface utilisateur fournis par le système](appendix-a--supported-user-interface-elements-reference.md) , tels que les zones de liste, les menus et les contrôles TrackBar, vous devez implémenter l’interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) uniquement pour les types d’éléments d’interface utilisateur personnalisés suivants :

-   Contrôles personnalisés créés en inscrivant une classe de fenêtre définie par l’application
-   Contrôles personnalisés dessinés directement à l’écran qui n’ont pas de **HWND** associé
-   Contrôles personnalisés tels que les contrôles Microsoft ActiveX et Java
-   Les contrôles ou les objets de la fenêtre client de l’application qui ne sont pas déjà exposés

Les contrôles et menus owner-drawn sont accessibles tant que vous suivez les instructions présentées dans [raccourcis pour exposer des éléments d’interface utilisateur personnalisés](shortcuts-for-exposing-custom-user-interface-elements.md). Si vous suivez ces instructions, vous n’avez pas besoin d’implémenter l’interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) pour les contrôles et les menus owner-drawn.

Dans la plupart des cas, les contrôles superclassé et sous-classé sont accessibles car le système gère les fonctionnalités de base du contrôle. Toutefois, si un contrôle sous-classé ou sous-classé modifie considérablement le comportement du contrôle fourni par le système sur lequel il est basé, vous devez implémenter l’interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) . Pour plus d’informations, consultez [exposition de contrôles basés sur des contrôles système](exposing-controls-based-on-system-controls.md).

Si une application utilise uniquement des éléments d’interface utilisateur fournis par le système, elle n’a pas besoin d’implémenter [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible), à l’exception de sa fenêtre cliente. Par exemple, une application qui comprend un éditeur de texte, qui n’est pas implémentée à l’aide d’un contrôle d’édition, expose des lignes de texte sous forme d’objets accessibles. Notez que Microsoft Active Accessibility expose automatiquement le texte des contrôles Edit et Rich Edit sous la forme d’une chaîne de texte unique dans la propriété [**value**](value-property.md) du contrôle.

 

 




