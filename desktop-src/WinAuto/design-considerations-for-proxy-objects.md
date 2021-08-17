---
title: Considérations relatives à la conception des objets proxy
description: La conception d’objets proxy et accessibles dépend de la conception des éléments de l’interface utilisateur du serveur. Quelle que soit la conception, un élément d’interface utilisateur doit notifier son objet proxy avant qu’il ne soit détruit afin que l’objet proxy gère les appels des clients de manière appropriée.
ms.assetid: 83a9ff66-2fe6-4589-a187-cdaf207b02b8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0cd96056f89e1efc18da3e299a76e92c85166efd7067e54f972a69eb8786d57
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118830069"
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

 

 




