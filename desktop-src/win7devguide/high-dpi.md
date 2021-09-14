---
title: Haute résolution
description: Haute résolution
ms.assetid: 476fe65c-2acd-4a7a-8a76-72d9f010b772
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc7c70e44c497f116348e7b42b260f056d593524
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127293962"
---
# <a name="high-dpi"></a>Haute résolution

À mesure que les technologies d’affichage progressent, les fabricants ont augmenté le nombre de pixels pris en charge par leurs affichages. Bien que le texte, les images et les éléments d’interface utilisateur semblent nettement plus nets et plus lisibles dans les affichages haute résolution, le système d’exploitation doit être mis à l’échelle pour prendre en charge l’expérience visuelle. dans le cas contraire, tout semble plus petit.

Windows 7 prend en charge les affichages haute *résolution* . les données de marché suggèrent que les déploiements d’écrans haute *résolution* (120-144 points par pouce (DPI)) augmentent au cours de la période de Windows 7. Lors de l’exécution de résolutions natives sur ces écrans, de nombreuses applications s’affichent très peu, sauf si elles utilisent la *haute résolution*. certaines applications (comme Windows Internet Explorer) disposent de fonctionnalités de mise à l’échelle des polices qui permettent aux utilisateurs d’effectuer des zooms avant et arrière, mais ce n’est pas le cas de nombreuses applications. la fonctionnalité *haute résolution* dans Windows 7 :

-   garantit que les Windows et les expériences d’application sont optimales sur le matériel standard (les paramètres *ppp* sont optimisés pour correspondre aux fonctionnalités du matériel).
-   permet à l’interpréteur de commandes Windows et à d’autres applications basées sur Windows de s’afficher correctement avec différents paramètres *ppp* .
-   Respecte les paramètres *PPP* par défaut en fonction des spécifications et des fonctionnalités matérielles.
-   Permet aux utilisateurs de personnaliser les paramètres *PPP* sans redémarrage.
-   Garantit que l’écran est toujours défini sur résolution native.

la fonctionnalité de mise à l’échelle *ppp* Windows met à l’échelle les polices et les éléments d’interface utilisateur (tels que les boutons, les icônes et les champs d’entrée) selon un pourcentage calculé, comme spécifié par le paramètre *ppp* . Cela diffère de la mise à l’échelle qui se produit lorsque la résolution d’affichage est abaissée. dans le cas de la mise à l’échelle *DPI* , Windows fournit des polices et des éléments d’interface utilisateur qui sont dessinés avec davantage de pixels, ce qui permet d’obtenir une expérience de Windows plus grande, plus haute et plus nette. les applications Windows tierces peuvent tirer parti des paramètres *haute résolution* et ajuster l’interface utilisateur en conséquence, en déclarant eux-mêmes la prise en charge de la *résolution élevée* . Les développeurs d’applications ne doivent plus supposer que 96 ppp est la solution idéale pour toutes les applications.

Pour plus d’informations sur les *résolutions élevées* et sur l’écriture d’applications qui prennent en charge la *résolution* haute résolution, consultez [haute résolution](../hidpi/high-dpi-desktop-application-development-on-windows.md).

 

 
