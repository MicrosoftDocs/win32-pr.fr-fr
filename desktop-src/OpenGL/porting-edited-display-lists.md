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
ms.openlocfilehash: 13f1630b0560091482d47f85e038d908dcfab202ae772c4d35dc388324b46075
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119485579"
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

 

 




