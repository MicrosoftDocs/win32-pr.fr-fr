---
description: Une image bitmap est l’un des objets GDI qui peuvent être sélectionnés dans un contexte de périphérique (DC).
ms.assetid: 36afaabc-1334-42d1-8004-7952ce3c119e
title: À propos des bitmaps
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53dbba516734dc255ce33005a7a9073865765785
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527706"
---
# <a name="about-bitmaps"></a>À propos des bitmaps

Une image bitmap est l’un des objets GDI qui peuvent être sélectionnés dans un *contexte de périphérique* (DC). Les [contextes de périphérique](device-contexts.md) sont des structures qui définissent un ensemble d’objets graphiques et leurs attributs associés, ainsi que des modes graphiques qui affectent la sortie. Le tableau ci-dessous décrit les objets GDI qui peuvent être sélectionnés dans un contexte de périphérique.



| Objet graphique                         | Description                                                                                                                                                                                          |
|----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Images bitmap](bitmaps.md)                 | Crée, manipule (mettre à l’échelle, faire défiler, faire pivoter et peindre) et stocke les images en tant que fichiers sur un disque.                                                                                                       |
| [Pinceaux](brushes.md)                 | Peint l’intérieur des polygones, des ellipses et des tracés.                                                                                                                                                |
| [Polices](fonts-and-text.md)            | Dessine du texte sur les affichages vidéo et les autres périphériques de sortie.                                                                                                                                               |
| [Palette logique](logical-palette.md) | Palette de couleurs créée par une application et associée à un contexte de périphérique donné.                                                                                                                |
| [Chemins d’accès](paths.md)                     | Un ou plusieurs figures (ou formes) qui sont remplies et/ou délimitées.                                                                                                                                     |
| [Stylets](pens.md)                       | Outil graphique utilisé par une application pour dessiner des lignes et des courbes.                                                                                                                                   |
| [Régions](regions.md)                 | Rectangle, polygone ou ellipse (ou combinaison de deux ou plusieurs de ces formes) pouvant être rempli, peint, inversé, encadré et utilisé pour effectuer un test de positionnement (test de l’emplacement du curseur). |



 

Du point de vue d’un développeur, une image bitmap se compose d’une collection de structures qui spécifient ou contiennent les éléments suivants :

-   En-tête qui décrit la résolution de l’appareil sur lequel le rectangle de pixels a été créé, les dimensions du rectangle, la taille du tableau de bits, et ainsi de suite.
-   Palette logique.
-   Tableau de bits qui définit la relation entre les pixels de l’image bitmap et les entrées de la palette logique.

Une taille de bitmap est liée au type d’image qu’elle contient. Les images bitmap peuvent être de type monochrome ou couleur. Dans une image, chaque pixel correspond à un ou plusieurs bits dans une bitmap. Les images monochromes présentent un rapport de 1 bit par pixel (BPP). L’imagerie des couleurs est plus complexe. Le nombre de couleurs qui peuvent être affichées par une image bitmap est égal à deux au nombre de bits par pixel. Ainsi, une bitmap de couleur 256 nécessite 8 bpp (2 ^ 8 = 256).

Les applications du panneau de configuration sont des exemples d’applications qui utilisent des bitmaps. Lorsque vous sélectionnez un arrière-plan (ou un papier peint) pour votre bureau, vous sélectionnez en fait une image bitmap, que le système utilise pour peindre l’arrière-plan du bureau. Le système crée le motif d’arrière-plan sélectionné en dessinant à plusieurs reprises un modèle de pixel de 32 par 32 sur le bureau.

L’illustration suivante montre le point de vue du développeur de l’image bitmap trouvée dans le Redbrick.bmp de fichiers. Il montre un tableau palette, un rectangle de pixels de 32 par 32 et le tableau d’index qui mappe les couleurs de la palette aux pixels du rectangle.

![illustration du rectangle de pixels, du tableau de palette et du tableau d’index de redbrick.bmp](images/csbmp-01.png)

Dans l’exemple précédent, le rectangle de pixels a été créé sur un périphérique d’affichage VGA à l’aide d’une palette de 16 couleurs. Une palette de 16 couleurs requiert des index 4 bits. par conséquent, le tableau qui mappe les couleurs de la palette aux couleurs de pixel est également composé d’index 4 bits. (Pour plus d’informations sur les palettes de couleurs logiques, consultez [couleurs](colors.md).)

> [!Note]
>
> Dans l’image bitmap ci-dessus, le système mappe les index aux pixels en commençant par la ligne de numérisation inférieure de la région rectangulaire et en terminant par la ligne de numérisation supérieure. Une *ligne de numérisation* est une ligne unique de pixels adjacents sur un affichage vidéo. Par exemple, la première ligne du tableau (ligne 0) correspond à la ligne inférieure des pixels, analyser la ligne 31. Cela est dû au fait que la bitmap ci-dessus est une image bitmap indépendante du périphérique (DIB), un type courant de bitmap. Dans les DIB descendants et dans les bitmaps dépendantes de l’appareil (DDB), le système mappe les index aux pixels en commençant par la ligne de numérisation supérieure.

 

Les rubriques suivantes décrivent les différentes zones des bitmaps.

-   [Classifications bitmap](bitmap-classifications.md)
-   [Types d’en-tête de bitmap](bitmap-header-types.md)
-   [Extensions JPEG et PNG pour des structures et des fonctions bitmap spécifiques](jpeg-and-png-extensions-for-specific-bitmap-functions-and-structures.md)
-   [Images bitmap, contextes de périphérique et surfaces de dessin](bitmaps--device-contexts--and-drawing-surfaces.md)
-   [Création d’une image bitmap](bitmap-creation.md)
-   [Rotation de bitmap](bitmap-rotation.md)
-   [Mise à l’échelle des bitmaps](bitmap-scaling.md)
-   [Bitmaps en tant que pinceaux](bitmaps-as-brushes.md)
-   [Stockage bitmap](bitmap-storage.md)
-   [Compression de bitmap](bitmap-compression.md)
-   [Fusion alpha](alpha-blending.md)
-   [Ombrage lissé](smooth-shading.md)
-   [Fonctions bitmap compatibles ICM](icm-enabled-bitmap-functions.md)

 

 



