---
title: Portage du code en mode MSINGLE
description: OpenGL n’a pas d’équivalent pour le mode MSINGLE, à matrice unique.
ms.assetid: 7de933b8-150c-432d-89ee-5f5799ad8443
keywords:
- Portage de l’IRIS du GL, mode MSINGLE
- Portage à partir de IRIS GL, mode MSINGLE
- portage vers OpenGL à partir de IRIS GL, mode MSINGLE
- Portage OpenGL à partir de IRIS GL, mode MSINGLE
- Mode MSINGLE
- Portage de l’IRIS dans le GL, mode à matrice unique
- Portage à partir de IRIS GL, mode à matrice simple
- portage vers OpenGL à partir de IRIS GL, mode à matrice unique
- Portage OpenGL à partir du mode IRIS GL, une seule matrice
- mode à matrice unique
- mode double matrice
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83716cead9134ba7823f4206fb6479d323bd35bddee480e9353a7ceb9aad38ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118132388"
---
# <a name="porting-msingle-mode-code"></a>Portage du code en mode MSINGLE

OpenGL n’a pas d’équivalent pour le mode **MSINGLE**, à matrice unique. Bien que l’utilisation de ce mode soit déconseillée, il s’agit de la valeur par défaut pour IRIS GL. Si votre programme IRIS GL utilise le mode à matrice unique, vous devez le réécrire pour utiliser uniquement le mode double matrice. OpenGL est toujours en mode double matrice et est initialement en \_ mode MODELVIEW GL.

La plupart du code de l’IRIS dans le mode MSINGLE se présente comme suit :

``` syntax
projectionmatrix();
```

où *ProjectionMatrix* est l’un des suivants : **ortho**, **ortho2**, **perspective** ou **Window**. Pour effectuer un portage vers OpenGL, remplacez la fonction *ProjectionMatrix* en mode **MSINGLE** par :


```C++
glMatrixMode( GL_PROJECTION ); 
glLoadMatrix( identity matrix ); 
 
/* call one of these functions here: */ 
/* glFrustrum(), glOrtho(), glOrtho2(), gluPerspective()}; */ 
 
glMatrixMode( GL_MODELVIEW ); 
glLoadMatrix( identity matrix );
```



 

 




