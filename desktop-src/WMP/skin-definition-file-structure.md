---
title: Structure du fichier de définition d’apparence
description: Structure du fichier de définition d’apparence
ms.assetid: 6b9ea288-ec64-473b-b796-ab637517099a
keywords:
- Apparences du lecteur Windows Media, fichiers de définition d’apparence
- apparences, fichiers de définition d’apparence
- fichiers pour les apparences, définition d’apparence
- fichiers de définition d’apparence, structure
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a64226fb918bcbf93c95ece52075e2c8e7ed13e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029477"
---
# <a name="skin-definition-file-structure"></a>Structure du fichier de définition d’apparence

Le fichier de définition d’apparence doit suivre une structure spécifique. Vous commencez avec un élément **Theme** , vous créez un ou plusieurs éléments **View** , puis vous définissez chaque élément **View** avec les éléments d’interface utilisateur appropriés pour le type de vue que vous souhaitez utiliser.

## <a name="theme-elements"></a>Éléments de thème

Au niveau supérieur, vous devez démarrer le fichier de définition d’apparence avec l’élément de **thème** et le fermer.


```C++
<THEME>
    ...
</THEME>

```



L’élément **Theme** est l’élément racine de votre apparence. Un fichier de définition d’apparence ne peut contenir qu’un seul élément **Theme** , et il doit se trouver au niveau supérieur. Les éléments de **thème** ont des attributs spécifiques et ambiants, mais la plupart du temps, vous n’aurez pas besoin de les utiliser. Pour plus d’informations sur ces attributs, consultez la référence sur la programmation de l' [apparence](skin-programming-reference.md).

## <a name="view-elements"></a>Éléments de vue

Chaque **thème** doit avoir au moins un élément d' **affichage** . L’élément **View** régit l’image particulière que vous voyez à l’écran. Vous souhaiterez peut-être disposer de plusieurs vues, ce qui vous permet de basculer vers l’avant et l’arrière. Par exemple, vous souhaiterez peut-être avoir un grand affichage pour travailler avec des sélections, une vue moyenne pour regarder les visualisations et une petite vue qui s’adapte à un coin de l’écran.

Si vous créez plusieurs vues, vous devez vous assurer que chaque vue a une valeur d’attribut d' **ID** unique qui sera utilisée pour identifier la vue. Vous devez définir l’attribut **BackgroundImage** ou votre vue n’aura pas d’image de départ. Si vous ne souhaitez pas afficher une image rectangulaire, vous souhaiterez probablement utiliser l’attribut **clippingColor** pour définir les zones de votre apparence qui ne seront pas affichées, et vous souhaiterez probablement définir l’attribut **TitleBar** de l’élément **View** .

Chaque élément de **vue** peut également avoir un ou plusieurs éléments de sous- **affichage** . Un élément de sous- **affichage** est semblable à une **vue** et peut être utilisé pour des parties de l’apparence que vous souhaitez déplacer, masquer ou afficher. Par exemple, un élément de sous- **affichage** peut être utilisé pour créer une barre coulissante qui s’affiche en dehors de votre apparence pour afficher un égaliseur graphique. Les éléments de sous- **affichage** peuvent être alignés avec la **vue** et avoir d’autres relations spéciales avec la **vue**.

## <a name="initializing-windows-media-player"></a>Initialisation du lecteur Windows Media

Vous pouvez définir certaines propriétés initiales du lecteur Windows Media à l’aide des éléments **Player**, **Settings** et **Controls** . Par exemple, vous pouvez définir le volume sur un niveau initial ou attribuer une valeur par défaut à un nom de fichier.

Le code suivant montre comment définir la valeur de l' **URL** dans une apparence :


```C++
<PLAYER
  URL = "https://proseware.com/mellow.wma">
</PLAYER>

```



Si vous souhaitez affecter la valeur false à l’attribut **AutoStart** des **paramètres** , vous devez utiliser le code suivant :


```C++
<PLAYER>
  <SETTINGS
    autoStart = "False">
  </SETTINGS>
</PLAYER>

```



Notez que l’élément **Settings** est imbriqué à l’intérieur de l’élément **Player** .

À l’aide de ces éléments, les attributs et les événements suivants peuvent être spécifiés au moment de la conception :

**Attributs de l’élément PLAYER**

-   **url**
-   **des réponses**
-   **Currentitemchange**
-   **Currentplaylistchange**
-   **Error**
-   **Markerhit**
-   **Mediachange**
-   **Mediacollectionchange**
-   **Modechange**
-   **Mpenstatechange**
-   **Mlaylistchange**
-   **Mlaystatechange**
-   **Mositionchange**
-   **Mcriptcommand**
-   **Mtatuschange**

**Attributs des éléments de paramètres**

-   **Démarrage automatique**
-   **équilibrée**
-   **baseURL**
-   **defaultFrame**
-   **enableErrorDialogs**
-   **invokeURLs**
-   **muette**
-   **playCount**
-   **évaluation**
-   **volume**

## <a name="controls-element-attributes"></a>Attributs d’élément de contrôle

-   **currentMarker**
-   **currentPosition**

## <a name="other-user-interface-elements"></a>Autres éléments de l’interface utilisateur

Une fois que vous avez défini votre **thème** et les éléments de **vue** , vous devez remplir votre **vue** avec des éléments d’interface utilisateur spécifiques. Vous n’avez pas à utiliser tous les éléments disponibles dans une apparence, juste ceux dont vous avez besoin.

Si un élément peut être vu par l’utilisateur, il est appelé contrôle. Les contrôles suivants sont disponibles pour les apparences :

-   Boutons
-   Curseurs, curseurs personnalisés et barres de progression
-   Zones de texte
-   Vidéos Windows
-   Fenêtres de visualisation
-   Fenêtres de sélection
-   Sous-affichage Windows

En outre, plusieurs éléments peuvent être utilisés pour définir plus précisément les actions du lecteur Windows Media, mais ils requièrent des éléments visuels tels que des boutons ou des curseurs :

-   Paramètres vidéo
-   Paramètres de l’égaliseur
-   Paramètres de visualisation

## <a name="buttons"></a>Boutons

Les boutons sont la partie la plus courante d’une apparence. Vous pouvez utiliser des boutons pour déclencher des actions telles que lire, arrêter, quitter, réduire et basculer vers un affichage différent. Le lecteur Windows Media fournit au créateur d’apparences deux types d’éléments Button : l’élément **Button** et l’élément **BUTTONGROUP** . En outre, il existe plusieurs types prédéfinis de boutons.

-   **Élément BUTTON.** L’élément **Button** est utilisé pour les boutons individuels. Si vous utilisez l’élément **Button** , vous devez fournir une image pour chaque bouton et définir l’emplacement exact où vous souhaitez que le bouton apparaisse par rapport à l’image d’arrière-plan. L’un des avantages de l’élément **Button** est que vous pouvez modifier l’image de bouton de manière dynamique.
-   **Élément BUTTONGROUP.** L’élément **BUTTONGROUP** est utilisé pour les groupes de boutons. En fait, vous devez placer chaque élément **BUTTONGROUP** avec une paire de balises **BUTTONGROUP** . L’utilisation de groupes de boutons est plus simple que l’utilisation de boutons individuels, car vous n’avez pas besoin de spécifier l’emplacement exact de chaque bouton. Au lieu de cela, vous fournissez une carte d’images distincte qui définit les actions qui se produisent lorsque la souris pointe sur une zone de votre arrière-plan ou clique dessus. L’utilisation de cartes d’images est simple, car vous pouvez prendre l’image que vous avez créée pour votre arrière-plan et la copier dans une couche de mappage dans votre programme d’édition de graphiques. L’utilisation de votre programme d’édition graphique est plus rapide et plus précise que la tentative de définition exacte de l’emplacement d’un bouton individuel sur l’arrière-plan.
-   **Boutons prédéfinis.** Il existe plusieurs boutons prédéfinis. Par exemple, vous pouvez utiliser un bouton PLAYELEMENT pour lire des fichiers multimédias numériques et un STOPELEMENT pour arrêter la lecture. Consultez élément [BUTTONGROUP](buttongroup-element.md) et [élément Button](button-element.md) dans la référence de programmation de l’apparence. Le [IMAGEBUTTON](imagebutton.md) peut être utilisé pour afficher des images qui peuvent changer en réponse à des événements spécifiques.

## <a name="sliders"></a>Curseurs

Les curseurs sont utiles pour utiliser des informations qui changent au fil du temps. Par exemple, vous pouvez utiliser un curseur pour indiquer la quantité de musique déjà lue pour un fichier multimédia particulier. Les curseurs peuvent être horizontaux ou verticaux, linéaires ou circulaires, ou toute forme que vous pouvez considérer. Les curseurs sont fournis en trois catégories : les curseurs, les barres de progression et les curseurs personnalisés.

-   **Curseurs.** Vous pouvez utiliser l’élément **Slider** pour les contrôles de volume ou pour permettre à l’utilisateur de passer à une autre partie du contenu multimédia.
-   **Barres de progression.** Les barres de progression sont similaires aux curseurs. Les barres de progression sont conçues pour afficher graphiquement le pourcentage d’un processus particulier qui est terminé, mais pas pour un processus avec lequel l’utilisateur souhaite interagir. Par exemple, vous souhaiterez peut-être utiliser une barre de progression pour indiquer la progression de la mise en mémoire tampon.
-   **Curseurs personnalisés.** Des fonctionnalités de curseur personnalisées sont fournies pour vous permettre de créer des contrôles tels que des boutons ou d’effectuer des mécanismes de contrôle inhabituels. Par exemple, si vous souhaitez créer un contrôle de volume qui habille votre apparence, vous pouvez le faire avec un curseur personnalisé. Pour configurer le curseur personnalisé, vous devez créer une image interactive qui contient des images en nuances de gris pour définir les emplacements des valeurs sur le curseur. Il est relativement facile d’effectuer cette opération avec un programme d’édition graphique qui prend en charge les couches.

## <a name="text"></a>Texte

Vous pouvez utiliser l’élément de **texte** pour afficher du texte sur votre apparence, par exemple des titres de chanson.

## <a name="video"></a>Vidéo

Vous pouvez afficher une vidéo dans votre apparence. L’élément **Video** vous permet de définir la taille et la position de la fenêtre vidéo.

Vous pouvez également autoriser l’utilisateur à modifier les paramètres vidéo avec l’élément **VIDEOSETTINGS** . Par exemple, vous pouvez créer des contrôles pour ajuster la luminosité de la vidéo.

Si vous ne fournissez pas d’élément vidéo et que le contenu contient une vidéo, le lecteur Windows Media revient en mode complet et votre apparence ne s’affiche pas.

## <a name="equalizer-settings"></a>Paramètres de l’égaliseur

Vous pouvez définir le filtrage pour des bandes de fréquence audio spécifiques à l’aide de l’élément **EQUALIZERSETTINGS** . Vous pouvez amplifier les basses, ajuster les aigus et configurer vos sons pour qu’ils correspondent à vos oreilles ou à votre salon.

## <a name="visualizations"></a>Visualisations

Vous pouvez afficher des visualisations dans votre apparence. Les visualisations sont des effets visuels qui changent au fil du temps à mesure que le son est lu par le biais du lecteur Windows Media. L’élément **Effects** détermine l’emplacement de lecture des visualisations, la taille de la fenêtre et les visualisations qui seront jouées.

## <a name="playlists"></a>Sélections

Vous pouvez utiliser l’élément **playlist** pour permettre à l’utilisateur de sélectionner un élément dans une sélection spécifique.

## <a name="subviews"></a>Sous-affichages

Vous pouvez utiliser l’élément de sous- **affichage** pour afficher des jeux secondaires de contrôles d’interface, tels qu’une sélection ou des contrôles vidéo.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Fichiers d’apparence**](skin-files.md)
</dt> </dl>

 

 




