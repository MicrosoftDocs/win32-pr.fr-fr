---
title: Haute résolution
description: .
ms.assetid: 476fe65c-2acd-4a7a-8a76-72d9f010b772
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adad7c986c7083ab2327f0c8de0bd2cace5ef20a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031644"
---
# <a name="high-dpi"></a>Haute résolution

À mesure que les technologies d’affichage progressent, les fabricants ont augmenté le nombre de pixels pris en charge par leurs affichages. Bien que le texte, les images et les éléments d’interface utilisateur semblent nettement plus nets et plus lisibles dans les affichages haute résolution, le système d’exploitation doit être mis à l’échelle pour prendre en charge l’expérience visuelle. dans le cas contraire, tout semble plus petit.

Windows 7 prend en charge les affichages haute *résolution* . Les données de marché suggèrent que les déploiements d’écrans haute *résolution* (120-144 points par pouce (dpi)) augmenteront dans le délai de Windows 7. Lors de l’exécution de résolutions natives sur ces écrans, de nombreuses applications s’affichent très peu, sauf si elles utilisent la *haute résolution*. Certaines applications (telles que Windows Internet Explorer) disposent de fonctionnalités de mise à l’échelle des polices qui permettent aux utilisateurs d’effectuer un zoom avant et arrière, mais ce n’est pas le cas de nombreuses applications. La fonctionnalité *haute résolution* dans Windows 7 :

-   Garantit que les expériences Windows et d’application sont optimales sur le matériel standard (les paramètres *PPP* sont optimisés pour correspondre aux fonctionnalités du matériel).
-   Permet à l’interpréteur de commandes Windows et à d’autres applications Windows de s’afficher correctement avec différents paramètres *PPP* .
-   Respecte les paramètres *PPP* par défaut en fonction des spécifications et des fonctionnalités matérielles.
-   Permet aux utilisateurs de personnaliser les paramètres *PPP* sans redémarrage.
-   Garantit que l’écran est toujours défini sur résolution native.

La fonctionnalité de mise à l’échelle *PPP* de Windows met à l’échelle les polices et les éléments d’interface utilisateur (tels que les boutons, les icônes et les champs d’entrée) selon un pourcentage calculé, comme spécifié par le paramètre *PPP* . Cela diffère de la mise à l’échelle qui se produit lorsque la résolution d’affichage est abaissée. Dans le cas de la mise à l’échelle *dpi* , Windows fournit des polices et des éléments d’interface utilisateur qui sont dessinés avec davantage de pixels, ce qui entraîne une plus grande, une meilleure fidélité et une expérience Windows plus nette. Les applications Windows tierces peuvent tirer parti des paramètres *haute résolution* et ajuster l’interface utilisateur en conséquence, en déclarant eux-mêmes la prise en charge de la *résolution haute PPP* . Les développeurs d’applications ne doivent plus supposer que 96 ppp est la solution idéale pour toutes les applications.

Pour plus d’informations sur les *résolutions élevées* et sur l’écriture d’applications qui prennent en charge la *résolution* haute résolution, consultez [haute résolution](../hidpi/high-dpi-desktop-application-development-on-windows.md).

 

 