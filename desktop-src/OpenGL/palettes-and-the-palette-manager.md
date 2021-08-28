---
title: Palettes et gestionnaire de palette
description: le gestionnaire de Windows de la palette, qui fait partie du GDI, cible spécifiquement les adaptateurs d’affichage 8 bits avec une Palette matérielle de 256 entrées de couleur.
ms.assetid: 3bfa5077-37ac-4597-98da-f26ad1c107a1
keywords:
- OpenGL sur Windows, gestionnaire de palette
- OpenGL sur Windows, palettes de matériel
- Gestionnaire de palette OpenGL
- palettes de matériel OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58407a5ddafe862caa73edd498c4da529b0ac987880828177d0d0b284601efed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118936275"
---
# <a name="palettes-and-the-palette-manager"></a>Palettes et gestionnaire de palette

le gestionnaire de Windows de la palette, qui fait partie du GDI, cible spécifiquement les adaptateurs d’affichage 8 bits avec une *Palette matérielle* de 256 entrées de couleur. Les pixels de l’écran sont stockés sous la forme d’un index 8 bits dans la palette matérielle. Chaque entrée de la palette matérielle définit généralement une couleur de 24 bits (8 en rouge, vert et bleu).

Le gestionnaire de palettes gère une *palette système* qui est une copie de la palette matérielle. La palette système est divisée en deux sections : 20 couleurs réservées et les couleurs 236 restantes, que vous pouvez définir à l’aide du gestionnaire de palette.

Une *palette logique* par défaut de 20 couleurs est sélectionnée et réalisée dans un contexte de périphérique. Vous pouvez créer et utiliser une nouvelle palette logique. Pour modifier la palette du système, sélectionnez et réalisez la palette logique que vous avez créée.

Vous allez probablement créer une palette logique pour spécifier les couleurs que vous souhaitez afficher dans votre application OpenGL. À l’aide de certains appels GDI, vous pouvez remplacer temporairement la plus grande partie de la palette système par une palette logique. À l’aide d’une palette logique, vous pouvez définir des couleurs de pixels pour le GDI à l’aide du mode RVBA ou de l’index des couleurs. La taille maximale d’une palette logique est de 256 couleurs pour les appareils 8 bits et de 4 096 couleurs sur un appareil de couleur vraies (16, 24 et 32 bits).

pour plus d’informations sur les modes rvba et index des couleurs, consultez [Mode rvba et Windows gestion](rgba-mode-and-windows-palette-management.md) de la palette et [modes de couleurs OpenGL et Windows gestion](opengl-color-modes-and-windows-palette-management.md)de la palette.

 

 




