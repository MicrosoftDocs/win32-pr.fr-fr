---
title: Palettes et gestionnaire de palette
description: Le gestionnaire de palette Windows, qui fait partie du GDI, cible spécifiquement des adaptateurs d’affichage 8 bits avec une palette de 256 de couleurs.
ms.assetid: 3bfa5077-37ac-4597-98da-f26ad1c107a1
keywords:
- OpenGL sur Windows, gestionnaire de palette
- OpenGL sur Windows, palettes matérielles
- Gestionnaire de palette OpenGL
- palettes de matériel OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3dac7d122ec36201e0156a141efc3291a87c7150
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106510404"
---
# <a name="palettes-and-the-palette-manager"></a>Palettes et gestionnaire de palette

Le gestionnaire de palette Windows, qui fait partie du GDI, cible spécifiquement des adaptateurs d’affichage 8 bits avec une *palette* de 256 de couleurs. Les pixels de l’écran sont stockés sous la forme d’un index 8 bits dans la palette matérielle. Chaque entrée de la palette matérielle définit généralement une couleur de 24 bits (8 en rouge, vert et bleu).

Le gestionnaire de palettes gère une *palette système* qui est une copie de la palette matérielle. La palette système est divisée en deux sections : 20 couleurs réservées et les couleurs 236 restantes, que vous pouvez définir à l’aide du gestionnaire de palette.

Une *palette logique* par défaut de 20 couleurs est sélectionnée et réalisée dans un contexte de périphérique. Vous pouvez créer et utiliser une nouvelle palette logique. Pour modifier la palette du système, sélectionnez et réalisez la palette logique que vous avez créée.

Vous allez probablement créer une palette logique pour spécifier les couleurs que vous souhaitez afficher dans votre application OpenGL. À l’aide de certains appels GDI, vous pouvez remplacer temporairement la plus grande partie de la palette système par une palette logique. À l’aide d’une palette logique, vous pouvez définir des couleurs de pixels pour le GDI à l’aide du mode RVBA ou de l’index des couleurs. La taille maximale d’une palette logique est de 256 couleurs pour les appareils 8 bits et de 4 096 couleurs sur un appareil de couleur vraies (16, 24 et 32 bits).

Pour plus d’informations sur les modes RVBA et index des couleurs, consultez [mode RVBA et gestion de la palette Windows](rgba-mode-and-windows-palette-management.md) et [modes de couleurs OpenGL et gestion de la palette Windows](opengl-color-modes-and-windows-palette-management.md).

 

 




