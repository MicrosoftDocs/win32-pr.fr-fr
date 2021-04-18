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
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106511839"
---
# <a name="porting-edited-display-lists"></a><span data-ttu-id="5979d-108">Portage des listes d’affichage modifiées</span><span class="sxs-lookup"><span data-stu-id="5979d-108">Porting Edited Display Lists</span></span>

<span data-ttu-id="5979d-109">Bien que vous ne puissiez pas modifier les listes d’affichage OpenGL, vous pouvez obtenir des résultats similaires en imbriquant des listes d’affichage, puis en détruisant et en créant de nouvelles versions des sous-listes.</span><span class="sxs-lookup"><span data-stu-id="5979d-109">Although you can't edit OpenGL display lists, you can get similar results by nesting display lists and then destroying and creating new versions of the sublists.</span></span> <span data-ttu-id="5979d-110">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="5979d-110">For example:</span></span>

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

 

 




