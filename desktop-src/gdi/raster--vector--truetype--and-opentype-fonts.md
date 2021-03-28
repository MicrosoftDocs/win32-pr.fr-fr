---
description: Polices Raster, Vector, TrueType et OpenType
ms.assetid: 4fe98f04-3fb0-4a03-86c3-d0ea6f07f8f0
title: Polices Raster, Vector, TrueType et OpenType
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e9b4be20ac7d02075fcd5c6cdbefe9eb516ea21
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991180"
---
# <a name="raster-vector-truetype-and-opentype-fonts"></a>Polices Raster, Vector, TrueType et OpenType

Les applications peuvent utiliser quatre types différents de technologies de polices pour afficher et imprimer du texte :

-   Raster
-   Vecteur
-   TrueType
-   Microsoft OpenType

Les différences entre ces polices reflètent la façon dont le *glyphe* pour chaque caractère ou symbole est stocké dans le fichier de ressources de police respectif :

-   Dans les polices Raster, un glyphe est un bitmap que le système utilise pour dessiner un caractère unique ou un symbole dans la police.
-   Dans les polices vectorielles, un glyphe est une collection de points de terminaison de ligne qui définissent les segments de ligne que le système utilise pour dessiner un caractère ou un symbole dans la police.
-   Dans les polices TrueType et OpenType, un glyphe est une collection de commandes de lignes et de courbes, ainsi qu’une collection d’indicateurs.

Le système utilise les commandes de ligne et de courbe pour définir le contour de l’image bitmap d’un caractère ou d’un symbole dans la police TrueType ou Microsoft OpenType. Le système utilise les indications pour ajuster la longueur des lignes et des formes des courbes utilisées pour dessiner le caractère ou le symbole. Ces indicateurs et les réglages respectifs sont basés sur la quantité de mise à l’échelle utilisée pour réduire ou augmenter la taille de l’image bitmap. Une police OpenType est équivalente à une police TrueType, à ceci près qu’une police OpenType autorise les définitions de glyphes PostScript en plus des définitions de glyphe TrueType.

Étant donné que les bitmaps de chaque glyphe dans une police raster sont conçues pour une résolution spécifique du périphérique, les polices Raster sont généralement considérées comme dépendantes du périphérique. Les polices vectorielles, en revanche, ne dépendent pas de l’appareil, car chaque glyphe est stocké sous la forme d’une collection de lignes dimensionnables. Toutefois, les polices vectorielles sont généralement dessinées plus lentement que les polices Raster ou TrueType et OpenType. Les polices TrueType et OpenType offrent une vitesse de dessin relativement rapide et une véritable indépendance du périphérique. En utilisant les indicateurs associés à un glyphe, un développeur peut mettre à l’échelle les caractères d’une police TrueType ou OpenType vers le haut ou vers le haut tout en conservant leur forme d’origine.

Comme mentionné précédemment, les glyphes pour une police sont stockés dans un fichier de ressources de polices. Un fichier de ressources de police est en fait une DLL qui contient uniquement des données, il n’existe pas de code. Pour les polices Raster et vectorielles, ces données sont divisées en deux parties : un en-tête décrivant les métriques et les données de glyphes de la police. Un fichier de ressources de police pour une police raster ou vectorielle est identifié par l’extension de nom de fichier. fon. Pour les polices TrueType et OpenType, il existe deux fichiers pour chaque police : le premier fichier contient un en-tête relativement bref et le second contient les données de police réelles. Le premier fichier est identifié par une extension. pour et le second est identifié par une extension. ttf.

 

 



