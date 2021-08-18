---
description: Notions de base des interfaces utilisateur Light-Aware
ms.assetid: 7ea391cb-f72b-4ac1-99be-c957d4ccc8af
title: Notions de base des interfaces utilisateur Light-Aware
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8955180dfc57219d3b640c6463f2ee2025f22500d3d29b688bc4b0c154895f66
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118890191"
---
# <a name="fundamentals-of-light-aware-user-interfaces"></a>Notions de base des interfaces utilisateur Light-Aware

Le terme *interface utilisateur sensible* fait référence à un programme qui utilise des données de capteur de lumière pour optimiser son contenu, ses contrôles et d’autres graphiques pour une expérience utilisateur optimale dans de nombreuses conditions d’éclairage, allant de l’obscurité à la lumière directe. Les optimisations les plus importantes sont peut-être la lisibilité, la lisibilité et les interactions dans le soleil direct, car les écrans ne fonctionnent généralement pas correctement dans ces conditions. Dans cette section, nous nous concentrons sur trois propriétés de l’interface utilisateur : mise à l’échelle, contraste et couleur. Ces propriétés peuvent être modifiées pour optimiser l’expérience utilisateur visuelle.

## <a name="scale-and-brightness"></a>Échelle et luminosité

En général, les objets plus grands sont plus faciles à voir. Lorsque l’ordinateur se trouve dans des conditions d’éclairage indésirables (par exemple, dans le soleil direct), le contenu est plus grand, ce qui permet d’améliorer la lisibilité et l’interactivité de ce contenu.

Les photographies suivantes comparent un ordinateur portable dans une lumière solaire directe avec une luminosité et des niveaux de zoom classiques sur un ordinateur portable dans les mêmes conditions d’éclairage avec une interface utilisateur sensible. La première photographie montre l’affichage défini sur une luminosité de 40% avec des niveaux de zoom normaux. La deuxième photographie montre l’affichage défini sur une luminosité de 100% avec des niveaux de zoom accrus.

![affichage de l’ordinateur portable à 40% de luminosité avec des niveaux de zoom normaux](images/laptop-40.png)![affichage de l’ordinateur portable à 100% de luminosité avec des niveaux de zoom accrus](images/laptop-100.png)

### <a name="varying-font-size"></a>Taille de police variable

Si vous augmentez la taille de la police utilisée pour afficher du texte, le texte est plus lisible dans des conditions d’éclairage défavorables. Le style de police, le type de police et d’autres caractéristiques peuvent également être modifiés pour optimiser la lisibilité et la lisibilité. Par exemple, les polices sans serif sont généralement plus faciles à lire que les polices Serif.

![police sans serif par rapport à la police serif](images/fonts.png)

### <a name="zooming-content"></a>Zoom sur le contenu

Si votre programme implémente le zoom, il peut être utilisé pour mettre à l’échelle le contenu. Le zoom avant améliore la lisibilité lors du zoom arrière permet au programme d’afficher davantage de contenu.

### <a name="altering-vector-graphic-rendering-properties"></a>Modification des propriétés de rendu des graphiques vectoriels

Si votre programme affiche des primitives de graphiques vectoriels (telles que des lignes, des cercles, etc.), les caractéristiques du rendu peuvent être modifiées pour optimiser la lisibilité. Par exemple, si votre programme affiche des rectangles, la largeur des lignes utilisées pour le rendu des rectangles peut être mise à l’échelle (plus large pour l’extérieur et plus étroit pour les inportes) afin d’optimiser l’apparence et la lisibilité du contenu graphique vectoriel.

## <a name="contrast"></a>Comparez

Lorsque les écrans LCD sont utilisés dans des conditions d’éclairage brillant, le contraste global de l’écran est réduit. Lorsque l’écran est inondé de lumière (à partir du soleil, par exemple), la perception des zones sombres de l’utilisateur sur l’écran est réduite. En général, il est important d’augmenter le contraste du contenu et de l’interface utilisateur lorsque la lumière ambiante est brillante. Il peut être souhaitable d’utiliser un modèle de couleurs monochrome pour maximiser le contraste dans ces conditions d’éclairage. Une autre façon d’augmenter le contraste consiste à remplacer le contenu à contraste faible (par exemple, un mode photo aérien dans un programme de mappage) par des éléments à contraste élevé (tels que le mode graphique vectoriel de la rue noir sur blanc).

## <a name="color"></a>Couleur

Les couleurs utilisées par un programme pour afficher son contenu peuvent avoir un effet considérable sur l’expérience globale de l’utilisateur et la lisibilité du contenu rendu. En modifiant le contraste des couleurs en fonction de la lumière ambiante, vous pouvez rendre le contenu plus lisible dans des conditions d’éclairage indésirables, telles qu’une lumière lumineuse et une lumière sombre lumineuse.

Une façon d’augmenter le contraste des couleurs est de saturer les couleurs. Une autre méthode consiste à utiliser des couleurs complémentaires plutôt que des couleurs adjacentes pour une meilleure lisibilité. Les couleurs complémentaires sont des paires de couleurs de couleur opposée, telles que le bleu et le jaune. L’exemple côte à côte suivant montre comment l’utilisation de couleurs complémentaires peut aider à améliorer le contraste des couleurs.

![exemple des effets de la couleur de texte sur la lisibilité.](images/color.png)

 

 



