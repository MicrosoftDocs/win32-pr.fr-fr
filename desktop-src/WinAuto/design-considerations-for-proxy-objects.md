---
title: Considérations relatives à la conception des objets proxy
description: La conception d’objets proxy et accessibles dépend de la conception des éléments de l’interface utilisateur du serveur. Quelle que soit la conception, un élément d’interface utilisateur doit notifier son objet proxy avant qu’il ne soit détruit afin que l’objet proxy gère les appels des clients de manière appropriée.
ms.assetid: 83a9ff66-2fe6-4589-a187-cdaf207b02b8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9578c79f93f91834dec14808a1a1867f40b215a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028798"
---
# <a name="design-considerations-for-proxy-objects"></a>Considérations relatives à la conception des objets proxy

La conception d’objets proxy et accessibles dépend de la conception des éléments de l’interface utilisateur du serveur. Quelle que soit la conception, un élément d’interface utilisateur doit notifier son objet proxy avant qu’il ne soit détruit afin que l’objet proxy gère les appels des clients de manière appropriée.

La liste suivante décrit deux possibilités de conception :

-   Placez le code qui implémente l’interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) dans le même module que le code qui implémente l’élément d’interface utilisateur si le code de l’interface utilisateur est facilement extensible. Dans ce cas, le proxy est « léger » dans le sens où il n’est qu’à surveiller la durée de vie de l’objet accessible, transférer les appels à l’objet accessible et retourner les résultats.
-   Placez le code qui implémente [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) dans le même module que le code qui implémente l’objet proxy. Dans ce cas, l’objet accessible utilise des fonctions internes pour obtenir des informations sur l’élément d’interface utilisateur.

## <a name="trackbar-controls"></a>Contrôles TrackBar

Lors de l’implémentation de contrôles TrackBar, utilisez le type de ligne de commande TrackBar **\_ inversé** pour fournir des informations plus explicites. Ce style inverse l’échelle utilisée par [**IAccessible :: \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue).

Pour les trackbarss verticaux sans ce style, [**IAccessible :: obtenir \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue) retourne la valeur zéro (0) lorsque le curseur de la barre de défilement se trouve en haut du contrôle ; les valeurs augmentent à mesure que vous faites glisser le curseur vers le bas. Avec le **style \_ inversé tbs** , **IAccessible :: obten \_ accValue** retourne 100 (100) quand le curseur de la barre de défilement se trouve en haut ; les nombres diminuent lorsque vous déplacez le curseur de la barre de défilement vers le bas.

Pour les trackbars horizontaux sans ce style, la valeur zéro (0) est retournée lorsque le curseur de la barre de défilement se trouve à l’extrémité gauche du contrôle ; les valeurs augmentent à mesure que vous déplacez le curseur de la barre de défilement vers la droite. Avec le **style \_ inversé tbs** , [**IAccessible :: obten \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue) retourne 100 (100) quand le curseur de la barre de défilement se trouve à gauche ; les valeurs diminuent lorsque vous déplacez le curseur de la barre de défilement vers la droite.

 

 




