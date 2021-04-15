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
ms.openlocfilehash: 1b8c62f93fa8e027dd1c91ca0bd40bc8e6ffaf9f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380119"
---
# <a name="porting-msingle-mode-code"></a><span data-ttu-id="7667b-114">Portage du code en mode MSINGLE</span><span class="sxs-lookup"><span data-stu-id="7667b-114">Porting MSINGLE Mode Code</span></span>

<span data-ttu-id="7667b-115">OpenGL n’a pas d’équivalent pour le mode **MSINGLE**, à matrice unique.</span><span class="sxs-lookup"><span data-stu-id="7667b-115">OpenGL has no equivalent for **MSINGLE**, single-matrix mode.</span></span> <span data-ttu-id="7667b-116">Bien que l’utilisation de ce mode soit déconseillée, il s’agit de la valeur par défaut pour IRIS GL.</span><span class="sxs-lookup"><span data-stu-id="7667b-116">Though use of this mode has been discouraged, it is the default for IRIS GL.</span></span> <span data-ttu-id="7667b-117">Si votre programme IRIS GL utilise le mode à matrice unique, vous devez le réécrire pour utiliser uniquement le mode double matrice.</span><span class="sxs-lookup"><span data-stu-id="7667b-117">If your IRIS GL program uses the single-matrix mode, you need to rewrite it to use double-matrix mode only.</span></span> <span data-ttu-id="7667b-118">OpenGL est toujours en mode double matrice et est initialement en \_ mode MODELVIEW GL.</span><span class="sxs-lookup"><span data-stu-id="7667b-118">OpenGL is always in double-matrix mode, and is initially in GL\_MODELVIEW mode.</span></span>

<span data-ttu-id="7667b-119">La plupart du code de l’IRIS dans le mode MSINGLE se présente comme suit :</span><span class="sxs-lookup"><span data-stu-id="7667b-119">Most IRIS GL code in MSINGLE mode looks like this:</span></span>

``` syntax
projectionmatrix();
```

<span data-ttu-id="7667b-120">où *ProjectionMatrix* est l’un des suivants : **ortho**, **ortho2**, **perspective** ou **Window**.</span><span class="sxs-lookup"><span data-stu-id="7667b-120">where *projectionmatrix* is one of: **ortho**, **ortho2**, **perspective**, or **window**.</span></span> <span data-ttu-id="7667b-121">Pour effectuer un portage vers OpenGL, remplacez la fonction *ProjectionMatrix* en mode **MSINGLE** par :</span><span class="sxs-lookup"><span data-stu-id="7667b-121">To port to OpenGL, replace the **MSINGLE** -mode *projectionmatrix* function with:</span></span>


```C++
glMatrixMode( GL_PROJECTION ); 
glLoadMatrix( identity matrix ); 
 
/* call one of these functions here: */ 
/* glFrustrum(), glOrtho(), glOrtho2(), gluPerspective()}; */ 
 
glMatrixMode( GL_MODELVIEW ); 
glLoadMatrix( identity matrix );
```



 

 




