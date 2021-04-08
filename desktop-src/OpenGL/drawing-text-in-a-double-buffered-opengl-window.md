---
title: Dessiner du texte dans une fenêtre Double-Buffered OpenGL
description: Vous dessinez du texte dans une fenêtre OpenGL à deux tampons en créant des listes d’affichage pour les caractères sélectionnés dans une police, puis en exécutant la liste d’affichage appropriée pour chaque caractère que vous souhaitez dessiner.
ms.assetid: 59ac0414-a845-4f40-be9c-9962fd1585f6
keywords:
- OpenGL sur Windows, texte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b0bf4cc99a1806d734ccde5cfae98f4d367da13
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675497"
---
# <a name="drawing-text-in-a-double-buffered-opengl-window"></a><span data-ttu-id="56148-104">Dessiner du texte dans une fenêtre Double-Buffered OpenGL</span><span class="sxs-lookup"><span data-stu-id="56148-104">Drawing Text in a Double-Buffered OpenGL Window</span></span>

<span data-ttu-id="56148-105">Vous dessinez du texte dans une fenêtre OpenGL à deux tampons en créant des listes d’affichage pour les caractères sélectionnés dans une police, puis en exécutant la liste d’affichage appropriée pour chaque caractère que vous souhaitez dessiner.</span><span class="sxs-lookup"><span data-stu-id="56148-105">You draw text in a double-buffered OpenGL window by creating display lists for selected characters in a font, and then executing the appropriate display list for each character you want to draw.</span></span> <span data-ttu-id="56148-106">L’exemple de code suivant crée un contexte de rendu, dessine un triangle rouge, puis l’étiquette avec du texte.</span><span class="sxs-lookup"><span data-stu-id="56148-106">The following code sample creates a rendering context, draws a red triangle, and then labels it with text.</span></span> <span data-ttu-id="56148-107">Pour cet exemple de code, nous partons du principe qu’il existe un contexte de périphérique, avec une police et un format de pixel.</span><span class="sxs-lookup"><span data-stu-id="56148-107">For this sample code, we assume that there is a device context, with a font and pixel format.</span></span>


```C++
// create an OpenGL rendering context  
hglrc = wglCreateContext(hdc); 
 
// make it this thread's current rendering context  
wglMakeCurrent(hdc, hglrc); 
 
// make the color a deep blue hue  
glClearColor(0.0F, 0.0F, 0.4F, 1.0F); 
 
// make the shading smooth 
glShadeModel(GL_SMOOTH); 
 
// clear the color buffers  
glClear(GL_COLOR_BUFFER_BIT); 
 
// specify a red triangle  
glBegin(GL_TRIANGLES); 
    glColor3f(1.0F, 0.0F, 0.0F); 
    glVertex2f(10.0F, 10.0F); 
    glVertex2f(250.0F, 50.0F); 
    glVertex2f(105.0F, 280.0F); 
glEnd(); 
 
// create bitmaps for the device context font's first 256 glyphs  
wglUseFontBitmaps(hdc, 0, 256, 1000); 
 
// move bottom left, southwest of the red triangle  
glRasterPos2f(30.0F, 300.0F); 
 
// set up for a string-drawing display list call  
glListBase(1000); 
 
// draw a string using font display lists  
glCallLists(12, GL_UNSIGNED_BYTE, "Red Triangle"); 
 
// get all those commands to execute  
glFlush(); 
 
// delete our 256 glyph display lists  
glDeleteLists(1000, 256) ; 
 
// make the rendering context not current  
wglMakeCurrent (NULL, NULL) ; 
 
// release the device context  
ReleaseDC(hdc) ; 
 
// delete the rendering context  
wglDeleteContext(hglrc);
```



 

 




