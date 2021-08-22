---
title: Superposition, Underlay et plans principaux
description: Vous pouvez utiliser des plans de couche matérielle (plans superposés et Underlay) dans vos applications.
ms.assetid: fd9401b3-f2a8-4384-92e8-61b346216542
keywords:
- OpenGL sur Windows, plans de couche matérielle
- plans de couche matérielle OpenGL
- plans de recouvrement OpenGL
- Underlay plans OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b968a0ab028fd0a699e31ad3a3601d7140435e2b36d0188bef46c5dca7cbad9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118936488"
---
# <a name="overlay-underlay-and-main-planes"></a>Superposition, Underlay et plans principaux

Vous pouvez utiliser des plans de couche matérielle (plans superposés et Underlay) dans vos applications. avec Windows, les formats de pixel décrivent les configurations en pixels d’un périphérique graphique. Chaque format de pixel décrit la profondeur et d’autres caractéristiques des mémoires tampons de couleur principales et décrit des mémoires tampons supplémentaires (par exemple, profondeur, accumulation, stencil et auxiliaire) utilisées par le plan principal. Les formats de pixel sont maintenant étendus pour inclure les mémoires tampons de superposition et Underlay.

Les plans de couche ont toujours une mémoire tampon de couleur frontale et peuvent également inclure des tampons de couleur d’arrière-plan et de couleur d’arrière-plan. Chaque plan de couche a un contexte de rendu spécifique à afficher dans les mémoires tampons de couche. Vous ne pouvez pas utiliser de fonctions de dessin GDI dans des plans de couche.

Une fenêtre gère les tampons de couleur des plans de couche de la même manière qu’elle gère les tampons de couleur plan principal. Vous pouvez afficher plusieurs fenêtres avec des plans de superposition et/ou de Underlay en même temps. Vous ne pouvez pas avoir des fenêtres de recouvrement flottantes qui peuvent se déplacer sur n’importe quelle fenêtre du plan de dessin principal. En outre, étant donné que les plans sous-jacents sont obscurcis dans une fenêtre à tout moment, vous ne pouvez pas utiliser de plans contextuels matériels qui n’ont pas de couleur transparente.

Chaque plan de couche dans une fenêtre est associé à une palette. Vous pouvez définir la palette d’un plan de couche d’index de couleurs, mais la palette d’un plan de couleurs RVBA est fixe. Vous devez vous rendre compte de la palette appropriée lorsqu’une fenêtre se trouve au premier plan. Les plans de couche ont une couleur ou un index de pixel transparent qui permet d’afficher tous les plans de la couche sous-jacente.

Vous pouvez copier l’état d’un contexte de rendu dans un autre contexte de rendu dans un plan de couche distinct. Vous pouvez également partager des listes d’affichage entre des contextes de rendu dans différents plans de couche.

Les fonctions suivantes sont utilisées avec les plans de couche :

-   [**wglCopyContext**](/windows/desktop/api/wingdi/nf-wingdi-wglcopycontext)
-   [**wglCreateLayerContext**](/windows/desktop/api/wingdi/nf-wingdi-wglcreatelayercontext)
-   [**wglDescribeLayerPlane**](/windows/desktop/api/wingdi/nf-wingdi-wgldescribelayerplane)
-   [**wglGetLayerPaletteEntries**](/windows/desktop/api/wingdi/nf-wingdi-wglgetlayerpaletteentries)
-   [**wglRealizeLayerPalette**](/windows/desktop/api/wingdi/nf-wingdi-wglrealizelayerpalette)
-   [**wglSetLayerPaletteEntries**](/windows/desktop/api/wingdi/nf-wingdi-wglsetlayerpaletteentries)
-   [**wglSwapLayerBuffers**](/windows/desktop/api/wingdi/nf-wingdi-wglswaplayerbuffers)

 

 




