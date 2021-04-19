---
title: Espaces de couleurs CMJ et CMJN
description: Les espaces de couleurs CMJ et CMJN sont souvent utilisés dans l’impression couleur. Un espace de couleurs CMJ utilise le cyan, le magenta et le jaune (CMJ) comme couleurs primaires. Les couleurs secondaires rouge, vert et bleu.
ms.assetid: e135b5ef-fa5c-49b7-8537-5dc31cde2418
keywords:
- Système de couleurs Windows (WCS), espaces de couleurs CMJ
- WCS (système de couleurs Windows), CMJ d’espaces de couleurs
- gestion des couleurs des images, espaces de couleurs CMJ
- gestion des couleurs, espaces de couleurs CMJ
- couleurs, espaces de couleurs CMJ
- espaces de couleurs, CMJ
- Espaces de couleurs CMJ
- Windows Color System (WCS), espaces de couleurs CMJN
- WCS (système de couleurs Windows), espaces de couleurs CMJN
- gestion des couleurs des images, espaces de couleurs CMJN
- gestion des couleurs, espaces CMYKcolor
- couleurs, espaces de couleurs CMJN
- espaces colorimétriques, CMJN
- Espaces de couleurs CMJN
- Cyan
- Magenta
- yellow
- cyan magenta jaune (CMJ)
- CMJ (cyan magenta jaune)
- cyan magenta jaune noir (CMJN)
- CMJN (cyan magenta jaune noir)
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52622c929222eb9027b6272137a8b897210697b6
ms.sourcegitcommit: 38954f8f0d70f44bff4a943784f468ebd7ef691a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/26/2021
ms.locfileid: "106544333"
---
# <a name="cmy-and-cmyk-color-spaces"></a>Espaces de couleurs CMJ et CMJN

Les [espaces de couleurs](c.md) CMJ et CMJN sont souvent utilisés dans l’impression couleur. Un espace de couleurs CMJ utilise le cyan, le magenta et le jaune (CMJ) comme [couleurs primaires](p.md). Les couleurs secondaires rouge, vert et bleu.

Les figures suivantes sont des représentations de couleur de l’espace de couleurs CMJ. L’espace de couleurs CMJ est normalisé.

![Cube d’espace de couleurs CMJ à des valeurs maximales](images/cmyclrs1.png)

![Cube d’espace colorimétrique CMJ aux valeurs minimales](images/cmyclrs2.png)

L’espace de couleurs CMJ est soustrait. Par conséquent, le blanc se trouve à l’adresse (0,0, 0,0, 0,0) et le noir à (1,0, 1,0, 1,0). Si vous commencez avec le blanc sans soustraire les couleurs, vous êtes blanc. Si vous commencez avec le blanc et que vous soustrayez toutes les couleurs de manière égale, vous êtes noir.

L’espace colorimétrique CMJN est une variation sur le modèle CMJ. Il ajoute du noir (cyan, magenta, jaune et noir). L’espace colorimétrique CMJN ferme l’intervalle entre la théorie et la pratique. En théorie, le composant noir supplémentaire n’est pas nécessaire. Toutefois, l’expérience avec différents types d’encres et de papiers a montré que lorsque des composants équivalents des encres cyan, magenta et jaune sont mélangés, le résultat est généralement un brun foncé, et non le noir. L’ajout d’encre noire à la combinaison résout ce problème.

Les espaces de couleurs CMJ et CMJN peuvent être indépendants des appareils, mais ils sont le plus souvent utilisés en référence à un appareil spécifique.

 

 




