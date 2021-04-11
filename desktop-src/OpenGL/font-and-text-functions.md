---
title: Fonctions de police et de texte (OpenGL)
description: Les fonctions suivantes peuvent être utilisées pour gérer des polices et du texte.
ms.assetid: 42e16967-1eeb-4d37-bbd6-33c473eb2757
keywords:
- WGL, fonctions, texte
- WGL, police
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e205549346cccc2c44b7670db91530cfbc24017d
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104383667"
---
# <a name="font-and-text-functions-opengl"></a>Fonctions de police et de texte (OpenGL)

Les fonctions suivantes peuvent être utilisées pour gérer des polices et du texte.



| Fonction Windows                                 | Description                                                                                                                                                                                                                      |
|--------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**wglUseFontBitmaps**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontbitmapsa)   | Crée un jeu de listes d’affichage de bitmaps de caractères. Les caractères proviennent de la police actuelle d’un contexte de périphérique spécifié. Les caractères sont spécifiés en tant qu’exécution consécutive dans le jeu de glyphes de la police.                                      |
| [**wglUseFontOutlines**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontoutlinesa) | Crée un ensemble de listes d’affichage, en fonction des glyphes de la police de contour actuellement sélectionnée d’un contexte de périphérique, à utiliser avec le contexte de rendu actuel. Les listes d’affichage permettent de dessiner des caractères 3D de polices TrueType. |



 

Les fonctions **wglUseFontBitmaps** et **wglUseFontOutlines** prennent un handle vers un contexte de périphérique et utilisent la police actuelle de ce contexte de périphérique comme source pour les bitmaps. Par conséquent, il est nécessaire de définir la police du contexte de périphérique et les propriétés de la police avant d’appeler **wglUseFontBitmaps** ou **wglUseFontOutlines**.

Les fonctions [**wglUseFontBitmaps**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontbitmapsa) et [**wglUseFontOutlines**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontoutlinesa) prennent également un paramètre qui transforme le premier glyphe de la police en une liste d’affichage bitmap, et un paramètre qui spécifie le nombre de glyphes à convertir en listes d’affichage. La fonction crée ensuite des listes d’affichage pour l’exécution consécutive de glyphes spécifiée. Par exemple :

-   Pour créer un ensemble de listes d’affichage bitmap 224 pour tous les glyphes de jeu de caractères Windows, définissez ces deux paramètres sur 32 et 224, respectivement.
-   Pour créer un ensemble de listes d’affichage bitmap 256 pour tous les glyphes de jeu de caractères OEM, définissez ces deux paramètres sur 0 et 256, respectivement.
-   Pour créer une liste d’affichage à bitmap unique pour tout glyphe de jeu de caractères unique, définissez la seconde de ces paramètres sur 1.

Les fonctions **wglUseFontBitmaps** et **wglUseFontOutlines** représentent un glyphe null dans une police avec une liste d’affichage vide.

Les listes d’affichage créées par un appel à **wglUseFontBitmaps** ou **wglUseFontOutlines** sont numérotées automatiquement de façon consécutive.

Après avoir appelé la fonction [**wglUseFontBitmaps**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontbitmapsa) ou [**WglUseFontOutlines**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontoutlinesa) , appelez [**glCallLists**](glcalllists.md) pour dessiner une chaîne de caractères. Pour obtenir un exemple de code [, consultez dessin de texte dans une fenêtre Double-Buffered OpenGL](drawing-text-in-a-double-buffered-opengl-window.md) . Dans ce contexte, **glCallLists** utilise chaque caractère dans une chaîne en tant qu’index dans le tableau des listes d’affichage numérotées consécutivement créées par **wglUseFontBitmaps** ou **wglUseFontOutlines**.

Lorsque vous avez terminé de dessiner du texte, appelez la fonction [**glDeleteLists**](gldeletelists.md) pour libérer l’ensemble des listes d’affichage contiguës créées par **wglUseFontBitmaps** et **wglUseFontOutlines**.

 

 




