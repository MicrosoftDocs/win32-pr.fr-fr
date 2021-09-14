---
title: Portage des listes d’affichage modifiées
description: Bien que vous ne puissiez pas modifier les listes d’affichage OpenGL, vous pouvez obtenir des résultats similaires en imbriquant des listes d’affichage, puis en détruisant et en créant de nouvelles versions des sous-listes.
ms.assetid: b7f7ffed-c3de-43d4-bff2-f244faa3a27a
keywords:
- Le portage du GL IRIS, afficher les listes
- Portage à partir de IRIS GL, afficher les listes
- portage vers OpenGL à partir de IRIS GL, afficher les listes
- Portage OpenGL depuis IRIS GL, afficher les listes
- afficher les listes, Portage à partir de IRIS GL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5555c850d4695ba3732b61c0a41b7aedd8af0a9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127119118"
---
# <a name="porting-edited-display-lists"></a>Portage des listes d’affichage modifiées

Bien que vous ne puissiez pas modifier les listes d’affichage OpenGL, vous pouvez obtenir des résultats similaires en imbriquant des listes d’affichage, puis en détruisant et en créant de nouvelles versions des sous-listes. Par exemple :

``` syntax
glNewList (1, GL_COMPILE); 
    glIndexi(MY_RED); 
glEndlist(); 
 
glNewList(2, GL_COMPILE); 
    glScalef(1.2, 1.2, 1.0); 
glEndList(); 
 
glNewList(3, GL_COMPILE); 
    glCallList(1); 
    glCallList(2); 
glEndList(); 
 
glDeleteLists(1, 2); 
glNewList(1, GL_COMPILE); 
    glIndexi(MY_CYAN); 
glEndList(); 
glNewList(2, GL_COPILE); 
    glScalef(0.5, 0.5, 1.0); 
glEndList;
```

 

 




