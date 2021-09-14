---
title: Exemple de port d’une liste d’affichage
description: Cette rubrique fournit un exemple de code d’IRIS dans le GL qui définit trois listes d’affichage. l’une des listes d’affichage fait référence aux autres dans sa définition. La suite de l’exemple IRIS GL est un exemple de ce à quoi ressemble le code lorsqu’il est porté à OpenGL.
ms.assetid: 03283b00-fb5b-4e89-9384-171b38f141ee
keywords:
- Le portage du GL IRIS, afficher les listes
- Portage à partir de IRIS GL, afficher les listes
- portage vers OpenGL à partir de IRIS GL, afficher les listes
- Portage OpenGL depuis IRIS GL, afficher les listes
- afficher les listes, Portage à partir de IRIS GL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77a856350a0a248bf7dcac51c36b9d35cf114956
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127194467"
---
# <a name="a-sample-port-of-a-display-list"></a>Exemple de port d’une liste d’affichage

Cette rubrique fournit un exemple de code d’IRIS dans le GL qui définit trois listes d’affichage. l’une des listes d’affichage fait référence aux autres dans sa définition. La suite de l’exemple IRIS GL est un exemple de ce à quoi ressemble le code lorsqu’il est porté à OpenGL.

## <a name="iris-gl-sample-display-list-code"></a>Exemple de code de liste d’affichage d’IRIS GL


```C++
makeobj(10);  // 10 object  
    cpack(0x0000FF); 
    recti(164, 33, 364, 600);   // Hollow rectangle  
closeobj(); 
 
makeobj(20);  // 20 object  
    cpack(0xFFFF00); 
    circle(0, 0, 25);           // Unfilled circle  
    recti(100, 100, 200, 200);  // Filled rectangle  
closeobj(); 
 
makeobj(30);  // 30 object  
    callobj(10); 
    cpack(0xFFFFFF); 
    recti(400, 100, 500, 300);  // Draw filled rectangle  
    callobj(20); 
closeobj(); 
 
// Now draw by calling the lists  
call(30);
```



## <a name="opengl-sample-display-list-code"></a>Exemple de code de liste d’affichage OpenGL

Voici le code de la comptabilité en IRIS précédent traduit en OpenGL :


```C++
glNewList(10, GL_COMPILE);            // List #10  
    glColor3f(1, 0, 0); 
    glRecti(164, 33, 364, 600); 
glEndList(); 
 
glNewList(20, GL_COMPILE);            //List #20  
    glColor3f(1, 1, 0);               // Set color to YELLOW  
    glPolygonMode(GL_BOTH, GL_LINE);  // Unfilled mode  
    glBegin(GL_POLYGON);  // Use polygon to approximate a circle  
        for(i=0; i<100; i++) { 
            cosine = 25 * cos(i * 2 * PI/100.0); 
            sine =   25 * sin(i * 2 * PI/100.0); 
            glVertex2f(cosine, sine); 
        } 
    glEnd(); 
    glBegin(GL_QUADS); 
        glColorf(0, 1, 1);            // Set color to CYAN  
        glVertex2i(100, 100); 
        glVertex2i(100, 200); 
        glVertex2i(200, 200); 
        glVertex2i(100, 200); 
    glEnd(); 
glEndList(); 
 
glNewList(30, GL_COMPILE);            // List #30  
    glCallList(10); 
        glColorf(1, 1, 1);            // Set color to WHITE  
        glRecti(400, 100, 500, 300); 
    glCallList(20); 
glEndList(); 
 
// Execute the display lists  
glCallList(30);
```



 

 




