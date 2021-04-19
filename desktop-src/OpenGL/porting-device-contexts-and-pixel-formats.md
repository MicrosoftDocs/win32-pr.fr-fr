---
title: Portage des contextes de périphérique et des formats de pixel
description: Portage des contextes de périphérique et des formats de pixel
ms.assetid: b60cac27-1e2e-4da5-81c4-69446b92f820
keywords:
- portage vers OpenGL, pixels
- Portage OpenGL, pixels
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d793c139c6d7a0a0fc85b2e2c36f30176ce9ab6e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106531185"
---
# <a name="porting-device-contexts-and-pixel-formats"></a>Portage des contextes de périphérique et des formats de pixel

Chaque fenêtre de l’implémentation Microsoft d’OpenGL pour Windows a son propre format de pixel actuel. Un format de pixel est défini par une structure de données [**PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) . Étant donné que chaque fenêtre a son propre format de pixel, vous obtenez un contexte de périphérique, définissez le format de pixel du contexte de périphérique, puis créez un contexte de rendu OpenGL pour le contexte de périphérique. Le contexte de rendu utilise automatiquement le format de pixel de son contexte de périphérique.

Le système de fenêtre X utilise également une structure de données, **XVisualInfo**, pour spécifier les propriétés des pixels dans une fenêtre. Les structures **XVisualInfo** contiennent une structure de données **visuelles** qui décrit comment les ressources de couleur sont utilisées dans un écran spécifique.

Dans le système de fenêtre X, **XVisualInfo** est utilisé pour créer une fenêtre en définissant la fenêtre au format de pixel souhaité. La structure retournée est utilisée pour créer la fenêtre et un contexte de rendu. Dans Windows, vous créez d’abord une fenêtre et vous recevez un handle vers un contexte de périphérique (HDC) de la fenêtre. Le HDC est ensuite utilisé pour définir le format de pixel de la fenêtre. Le contexte de rendu utilise le format de pixel de la fenêtre.

Le tableau suivant compare les fonctions de système de fenêtres X et de GLX visuelles à leurs fonctions de format de pixel Windows équivalentes.



| X fenêtre/GLX fonction visuelle                                                                                     | Fonction de format de pixel Windows                                                                                                      |
|------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| XVisualInfo \* **glXChooseVisual**(Display *\* dpy*, int *Screen*, int *\* attribList*)                               | int [**ChoosePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat)(HDC *HDC*, PIXELFORMATDESCRIPTOR *\* PPFD*)                                      |
| int **glXGetConfig**(Display *\* dpy* *\* , XVisualInfo,* int *\* attribList*, int *\* value*)                      | int [**DescribePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-describepixelformat)(HDC *HDC*, int *iPixelFormat*, uint *nBytes*, LPPIXELFORMATDESCRIPTOR *PPFD*) |
| XVisualInfo \* **XGetVisualInfo**(Display *\* dpy*, long *vinfo \_ Mask*, XVisualInfo *\* vinfo \_ temp*, int *\* nItems*) | int [**GetPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-getpixelformat)(HDC *HDC*)                                                                           |
| Le *visuel* retourné par **glxChooseVisual** est utilisé lors de la création d’une fenêtre.                                   | BOOL [**SetPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-setpixelformat)(HDC *HDC*, int *iPixelFormat*, PIXELFORMATDESCRIPTOR *\* PPFD*)                        |



 

Les sections suivantes fournissent des exemples de fragments de code de format de pixel pour un programme système X Window et le même code une fois qu’il a été porté vers Windows.

-   [Exemple de code de format de pixel GLX](glx-pixel-format-code-sample.md)
-   [Exemple de code de format de pixel Windows](win32-pixel-format-code-sample.md)

Pour plus d’informations sur les formats de pixel, consultez [formats de pixel](pixel-formats.md).

 

 




