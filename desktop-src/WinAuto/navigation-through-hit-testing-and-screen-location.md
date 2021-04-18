---
title: Navigation via le test de positionnement et l’emplacement à l’écran
description: Pour localiser les enfants d’un objet ou pour déterminer la taille d’un objet, les clients peuvent atteindre des points de test sur l’écran.
ms.assetid: ba08814f-87bc-4b47-8b61-179a48d5092f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c26d055246e038611e881bd353bcc865c5e77136
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106509192"
---
# <a name="navigation-through-hit-testing-and-screen-location"></a>Navigation via le test de positionnement et l’emplacement à l’écran

Pour localiser les enfants d’un objet ou pour déterminer la taille d’un objet, les clients peuvent atteindre des points de test sur l’écran. Deux méthodes sont disponibles :

-   [**IAccessible :: accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**IAccessible :: accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)

## <a name="using-iaccessibleacchittest"></a>Utilisation de IAccessible :: accHitTest

Pour déterminer si un point se trouve dans un objet, au sein de son enfant, ou si aucun des clients n’appelle la méthode [**IAccessible :: accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest) de l’objet parent, en passant les coordonnées d’écran du point à tester. La liste suivante décrit certains scénarios types :

-   Si les enfants de l’objet se chevauchent à un point spécifié, [**IAccessible :: accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest) récupère l’enfant le plus élevé qui semble occuper l’espace.
-   Si une fenêtre couvre un enfant, ou si l’enfant est coupé par le parent, le test de positionnement sur le point couvert récupère l’enfant même s’il n’est pas visible.
-   Si l’enfant trouvé au point spécifié est un objet accessible, par opposition à un élément enfant, la méthode retourne l’interface [**IDispatch**](idispatch-interface.md) de l’enfant.

## <a name="using-iaccessibleacclocation"></a>Utilisation de IAccessible :: accLocation

Pour récupérer l’emplacement à l’écran d’un objet ou de l’un des enfants de l’objet, les clients appellent [**IAccessible :: accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation). Cette méthode retourne les coordonnées du rectangle englobant de l’objet spécifié. Si l’objet n’est pas mis en forme comme un rectangle, la méthode retourne les coordonnées du plus petit rectangle qui englobe la totalité de l’objet.

L’illustration suivante montre la relation entre la région d’un objet non rectangulaire et son rectangle englobant.

![Illustration montrant la région d’un objet non rectangulaire (un cercle) et son rectangle englobant.](images/region.gif)

> [!Note]  
> [**IAccessible :: accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest) est plus précis que [**IAccessible :: accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation) , car il permet aux clients de déterminer l’emplacement des objets sur une base pixel par pixel plutôt qu’avec des rectangles englobants. Cette précision est utile, par exemple, lorsqu’une application collecte des informations en effectuant le suivi de l’emplacement du pointeur de la souris.

 

 

 




