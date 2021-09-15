---
title: Dessiner du texte dans une fenêtre Double-Buffered OpenGL
description: Vous dessinez du texte dans une fenêtre OpenGL à deux tampons en créant des listes d’affichage pour les caractères sélectionnés dans une police, puis en exécutant la liste d’affichage appropriée pour chaque caractère que vous souhaitez dessiner.
ms.assetid: 59ac0414-a845-4f40-be9c-9962fd1585f6
keywords:
- OpenGL sur Windows, texte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b0bf4cc99a1806d734ccde5cfae98f4d367da13
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127413696"
---
# <a name="drawing-text-in-a-double-buffered-opengl-window"></a>Dessiner du texte dans une fenêtre Double-Buffered OpenGL

Vous dessinez du texte dans une fenêtre OpenGL à deux tampons en créant des listes d’affichage pour les caractères sélectionnés dans une police, puis en exécutant la liste d’affichage appropriée pour chaque caractère que vous souhaitez dessiner. L’exemple de code suivant crée un contexte de rendu, dessine un triangle rouge, puis l’étiquette avec du texte. Pour cet exemple de code, nous partons du principe qu’il existe un contexte de périphérique, avec une police et un format de pixel.


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



 

 




