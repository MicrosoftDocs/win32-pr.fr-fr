---
title: Expérience utilisateur
description: le nouveau bureau de Windows 7 apporte vie à vos applications.
ms.assetid: e706167a-435b-4c32-bb64-87113f368866
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a8d62c94cfaae137a921979e514c9500376be4abf858da5b64eee5ac3c8ec6c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119811411"
---
# <a name="the-desktop-experience"></a>Expérience utilisateur

le nouveau bureau de Windows 7 apporte vie à vos applications. Les applications sont désormais plus détectables, informatives et interactives. les interfaces utilisateur modernes et intuitives sont plus faciles à développer avec Windows 7. Les nouvelles expériences de bureau et d’application sont les suivantes :

-   La barre des tâches améliorée présente des miniatures interactives et active l’animation et l’interaction pour les applications réduites.
-   Le concept de destination permet aux utilisateurs de passer d’un clic aux fichiers, emplacements ou tâches qu’ils utilisent le plus fréquemment.
-   de nouveaux contrôles et api pour le *ruban*, basés sur l’interface utilisateur Office Fluent, sont disponibles pour ajouter facilement des contrôles de style *ruban*, des menus et des galeries à vos applications.
-   Une infrastructure d’animation vous aide à améliorer les animations personnalisées.

Les améliorations apportées à la plateforme de gadgets permettent aux applications d’installer des gadgets auxiliaires pendant l’installation ou la première exécution.

![capture d’écran montrant le bureau Windows 7.](images/windows7-6.jpg)

le nouveau bureau de Windows 7 apporte vie à vos applications

## <a name="jump-listsgetting-users-into-your-application-quickly"></a>Listes de raccourcis : récupération rapide des utilisateurs dans votre application

Les listes de raccourcis aident les utilisateurs à accéder à l’emplacement où ils veulent aller plus rapidement. Les listes de raccourcis sont des fichiers, des URL, des tâches ou des éléments personnalisés qui s’ouvrent dans l’application. Le nouveau menu listes de raccourcis dans le menu *Démarrer* et la barre des tâches rend les destinations communes et les tâches clés disponibles en un seul clic. Le menu listes de raccourcis est automatiquement renseigné en fonction de la fréquence et de l’utilisation des éléments récemment. Les développeurs peuvent fournir des listes de raccourcis personnalisées en fonction de leur propre sémantique. Les applications peuvent également définir des *tâches* qui s’affichent dans leurs menus : il s’agit des actions de l’application auxquelles les utilisateurs veulent accéder directement, par exemple la composition d’un courrier électronique. (Voir [extensions de la barre des tâches](../shell/taskbar-extensions.md) et [interface ICustomDestinationList](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icustomdestinationlist).)

![listes de raccourcis](images/windows7-7.jpg)

Les listes de raccourcis aident les utilisateurs à trouver l’emplacement où ils veulent aller plus rapidement

## <a name="enhanced-taskbar"></a>Barre des tâches améliorée

avec la nouvelle barre des tâches de Windows 7, les applications peuvent fournir plus d’informations à l’utilisateur de manière intuitive. Par exemple, les applications peuvent afficher des barres de progression dans les boutons de la barre des tâches afin que les utilisateurs puissent rester informés de la progression sans avoir à garder la fenêtre visible. Cela est utile pour le suivi des opérations de longue durée, telles que la copie de fichiers, les téléchargements, les installations ou la gravure de supports. Les superpositions d’icône peuvent être affichées dans la partie inférieure droite du bouton de la barre des tâches de l’application, et sont utilisées pour communiquer l’État ou les notifications (par exemple, un nouveau message). Les nouvelles API de miniatures permettent à une application de définir des fenêtres enfants et des images miniatures correspondantes pour ces fenêtres. La barre d’outils miniatures fournit un emplacement pour contrôler les actions courantes sans nécessiter la restauration de la fenêtre, par exemple *lire/arrêter* pour le média. (voir [Extensions de la barre des tâches](../shell/taskbar-extensions.md) et [Windows 7 : ressources](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples)pour les développeurs.)

## <a name="gadgets-platform"></a>Plateforme des gadgets

les gadgets sont une fonctionnalité populaire du Windows Vista desktop et, dans Windows 7, il est encore plus facile pour les applications d’installer des gadgets. dans Windows 7, une application peut ajouter par programme un gadget au bureau Windows lors de la configuration de l’application ou de la première exécution. Cela signifie que l’expérience prête à l’emploi d’une application peut inclure une simple case à cocher, par exemple, pour installer un gadget auxiliaire disponible sur le Bureau dès que l’application est prête à être utilisée. (Consultez [Présentation de la plateforme de gadgets](/previous-versions/windows/desktop/gadgetplatform/introduction-to-the-gadget-platform).)

![gadgets Windows](images/windows7-8.jpg)

dans Windows 7, il est encore plus facile pour les applications d’installer des gadgets

## <a name="windows-ribbon"></a>Windows Dernier



le contrôle de ruban Windows aide les développeurs à améliorer l’utilisation en exposant les fonctionnalités les plus fréquemment sollicitées de votre application directement aux utilisateurs finaux. Le ruban permet aux utilisateurs finaux de rechercher et d’utiliser plus facilement les fonctionnalités de l’application, car moins de fonctionnalités sont masquées, ce qui entraîne une augmentation de la productivité. le ruban est conçu comme une alternative intentionnelle au modèle de présentation de commande des menus, des barres d’outils, des volets de tâches et des boîtes de dialogue dans les applications standard Windows.

Les contrôles de ruban se composent d’un ensemble de Win32APIs qui remplacent les fonctionnalités de barre de menus de niveau supérieur et affichent une interface utilisateur de commande de style ruban à la place. elle est similaire dans les fonctionnalités et l’apparence au *ruban* dans le système 2007 Office. L’interface utilisateur est composée de plusieurs sous-contrôles qui incluent les éléments suivants :

-   Bouton de l’application (ou perle)
-   Barre d’outils accès rapide
-   Contrôle de *ruban* des onglets contextuels
-   Mini-barres d’outils
-   Galeries de styles

Les modèles et la création de balises sont à la disposition des développeurs pour accélérer le développement et l’intégration des fonctionnalités du ruban. (consultez [Windows infrastructure de ruban](../windowsribbon/-uiplat-windowsribbon-entry.md) et [Windows infrastructure de ruban : ressources de développeur](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsRibbon).)

![barre d’outils ruban](images/windows7-9.jpg)

Le contrôle de ruban aide les développeurs à améliorer l’utilisation en exposant les fonctionnalités les plus fréquemment sollicitées de votre application

## <a name="animation"></a>Animation

les animations lisses sont fondamentales pour de nombreuses applications d’interface utilisateur graphique, et Windows 7 introduit une infrastructure d’animation native pour la gestion de la planification et de l’exécution des animations. L’infrastructure d’animation fournit une bibliothèque de fonctions mathématiques utiles pour spécifier le comportement au fil du temps et permet aux développeurs de fournir leurs propres fonctions de comportement. Le Framework prend en charge la résolution sophistiquée des conflits lorsque plusieurs animations essaient de manipuler la même valeur en même temps. Une application peut spécifier qu’une animation doit être exécutée avant qu’une autre puisse démarrer et peut forcer l’achèvement dans un délai défini. La nouvelle infrastructure aide également les animations à déterminer les durées appropriées. (consultez [Windows gestionnaire d’animations](../uianimation/-main-portal.md).)

 

 