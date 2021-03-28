---
description: Vous trouverez ci-dessous des informations sur les choix à prendre en compte lors de la personnalisation des vignettes d’application de bureau pour Windows 8, notamment comment concevoir des vignettes d’application de bureau pour le nouvel écran d’accueil et comment choisir les points d’entrée à afficher dans l’écran d’accueil.
ms.assetid: EF5182A2-09B2-46F2-B55E-4BD212CC1F7F
title: Vignettes de l’application de bureau sur l’écran d’accueil
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0fcc5475732926300e2125ae9e97ea2d188bc468
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/06/2021
ms.locfileid: "104321369"
---
# <a name="desktop-app-tiles-on-the-start-screen"></a>Vignettes de l’application de bureau sur l’écran d’accueil

Vous trouverez ci-dessous des informations sur les choix à prendre en compte lors de la personnalisation des vignettes d’application de bureau pour Windows 8, notamment comment concevoir des vignettes d’application de bureau pour le nouvel écran d’accueil et comment choisir les points d’entrée à afficher dans l’écran d’accueil.

## <a name="design-your-tile-for-the-start-screen"></a>Concevoir votre vignette pour l’écran de démarrage

Vous pouvez personnaliser deux aspects des vignettes de vos applications de bureau : le nom de l’application et l’icône. La couleur d’arrière-plan est dérivée de la couleur d’arrière-plan choisie par l’utilisateur et n’est pas personnalisable par programmation.

![aide sur la conception des vignettes d’application.](images/tiles-desktop-1.png)

DO : Évitez la troncation du nom de votre application. Les vignettes de bureau épinglées à l’écran de démarrage peuvent contenir jusqu’à deux lignes de texte sur chaque ligne, ou environ dix caractères (bien que cela dépend de la langue de l’interface utilisateur). essayez donc de conserver un nom d’application suffisamment court pour éviter la troncation.

DO : fournissez des icônes pour les quatre valeurs d’échelle d’écran de démarrage prises en charge pour vous assurer que vos icônes paraissent nettes sur tous les facteurs de forme.



| Scale | Taille de la vignette (en pixels) | Taille d’icône utilisée (en pixels) |
|-------|-----------------------|----------------------------|
| 80 %   | 120 x 120             | 48 x 48                    |
| 100 %  | 150 x 150             | 64 x 64                    |
| 140%  | 210 x 210             | 96 x 96                    |
| 180%  | 270 x 270             | 128 x 128                  |



 

DO : Adoptez les principes de conception Microsoft. La nouvelle apparence pour les icônes est plate. par conséquent, si vous souhaitez imiter les icônes d’application du Windows Store pour votre application de bureau, pensez à prendre des ombres portées, et ainsi de suite.

NE pas : Évitez d’utiliser la couleur. Alors que les icônes d’application du Windows Store sont parfois monochromatiques, nous vous recommandons d’utiliser des icônes de couleur pour les applications de bureau. Cela permet de différencier les applications de bureau de la barre des tâches et d’autres vignettes de l’application de bureau dans l’écran d’accueil, car la couleur d’arrière-plan des vignettes du Bureau ne peut pas être personnalisée. Envisagez d’utiliser des couleurs plus saturées.

## <a name="decide-the-right-entry-points-to-include-in-the-start-screen"></a>Choisir les points d’entrée appropriés à inclure dans l’écran d’accueil

DO : ajouter un raccourci par application dans l’écran d’accueil lors de l’installation de l’application. Cela permet de s’assurer que les utilisateurs peuvent lancer votre application directement à partir de l’écran d’accueil ou par le biais d’une recherche. Si vous n’incluez pas de raccourci dans l’écran d’accueil, votre application devient difficile à lancer. En particulier, n’ajoutez pas de raccourci sur le bureau uniquement. Les utilisateurs voient l’écran d’accueil lorsqu’ils se connectent pour la première fois. par conséquent, le fait de placer un raccourci sur le bureau n’est pas aussi efficace que l’inclure dans l’écran d’accueil.

![Diagramme illustrant une grille avec une vignette d’application, des dimensions et un « Segoe U I Semilight » pour indiquer la police utilisée.](images/tiles-desktop-2.png)

NE pas : ne pas fournir plusieurs raccourcis vers la même application. Par exemple, n’avez pas deux raccourcis qui lancent une application dans deux modes différents, tels qu’un pour Windows Internet Explorer et un autre pour Internet Explorer sans modules complémentaires.

DO : réduire le nombre de vignettes ajoutées dans le cadre de l’installation. Envisagez d’exposer d’autres points d’entrée aux applications superflues. Par exemple, au lieu d’inclure une application de paramètres distincte avec une application console, accédez aux paramètres via une fonctionnalité de l’application console.

NE pas : ne placez pas de raccourcis vers les éléments suivants sur l’écran d’accueil :

-   Désinstallation. Les utilisateurs peuvent accéder aux programmes de désinstallation par le biais de l’élément programmes dans le panneau de configuration.
-   Fichiers d’aide. Incluez les rubriques d’aide directement dans votre application.
-   Paramètres et options de l’application. Inclure l’interface utilisateur pour configurer les paramètres d’une application dans l’application ou créer un élément du panneau de configuration.
-   Sites Web. Fournissez les liens appropriés vers des informations telles que des sites d’aide et de support technique directement dans votre application.
-   Assistants. Les assistants et d’autres tâches de configuration à usage unique doivent être lancés à partir de l’application.

NE créez pas de raccourcis vers des fonctionnalités ou des fonctionnalités qui peuvent être lancées à partir de l’application elle-même. Par exemple, les paramètres de langue peuvent être configurés à partir de n’importe quelle application Microsoft Office. il est donc inutile d’avoir un point d’entrée de paramètres de langue distinct sur l’écran d’accueil.

NE pas créer de raccourcis vers des éléments qui ne sont pas des fichiers exécutables. Les raccourcis qui ne correspondent pas à des fichiers exécutables, tels que des raccourcis qui lancent des sites Web ou des fichiers d’aide, sont filtrés à partir de l’écran d’accueil.

DO : Si vous installez une suite d’applications plutôt qu’une seule application, ajoutez un raccourci pour chaque application de la suite. Comme indiqué ci-dessus, évitez de créer des raccourcis vers des fonctionnalités secondaires telles que des informations d’aide, des utilitaires et des paramètres. Cette fonctionnalité doit être incluse dans la ou les applications pertinentes de la suite.

DO : créez un dossier produit de niveau unique pour les suites qui contiennent au moins trois vignettes. Dans la vue applications de l’écran d’accueil, accessible à partir de l’icône de recherche, les applications sont regroupées en fonction de leur dossier de niveau supérieur. Choisissez un nom de dossier descriptif mais concis ; Il est recommandé de disposer de trois mots ou moins. Sachez que bien que la vue applications regroupe des vignettes et affiche le nom du dossier, ce nom n’est pas visible lorsqu’une vignette est épinglée à l’écran d’accueil, de sorte que les noms des vignettes sont suffisamment descriptifs.

NE pas créer de dossier produit si votre suite ne contient qu’un seul raccourci. Placez votre raccourci dans le dossier de démarrage de niveau supérieur.

DO : lors de l’installation d’une suite de plus de trois applications, déterminez si l’une de ces applications est pour une utilisation secondaire, plus irrégulière, et ne doit pas être épinglée à l’écran d’accueil. Dans ce cas, peut-être ces vignettes peuvent être entièrement supprimées, conformément aux instructions ci-dessus, et lancées à partir d’une application principale. Si vous ne pouvez pas supprimer les vignettes, envisagez de les désépingler à partir de l’écran d’accueil. De cette façon, les raccourcis apparaissent toujours dans la vue **toutes les applications** , mais n’encombrent pas l’écran d’accueil de l’utilisateur.

Pour créer un raccourci d’application sans l’épingler à l’écran d’accueil, définissez la propriété suivante sur le raccourci : System. AppUserModel. StartPinOption = 1. Le nom symbolique de 1 est APPUSERMODEL \_ STARTPINOPTION \_ NOPINONINSTALL.

Cela empêche l’affichage du raccourci sur l’écran d’accueil, mais il peut toujours être affiché dans la vue **toutes les applications** et dans les résultats de la recherche. Seul l’utilisateur peut désépingler les raccourcis existants. vous devez donc définir cette propriété au cours de l’installation ou immédiatement après avoir placé l’application sur le disque.

NE créez pas de vignette pour un hôte ou un Runtime pour des applications, telles que Silverlight ou Java. Fournissez un point d’entrée pour désinstaller le Framework dans Ajout/suppression de programmes et fournissez tout point d’entrée de paramètres dans le panneau de configuration.

 

 



