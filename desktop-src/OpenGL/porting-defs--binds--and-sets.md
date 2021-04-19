---
title: Portage des ensembles de paramètres, des liaisons et des ensembles
description: Portage des ensembles de paramètres, des liaisons et des ensembles
ms.assetid: 971feb14-ed39-4492-a62b-9930bdc506e9
keywords:
- Portage de l’IRIS dans le GL, définitions
- Portage à partir de IRIS GL, définitions
- portage vers OpenGL à partir de IRIS GL, définitions
- Portage OpenGL à partir de IRIS GL, définitions
- Portage des liaisons du GL IRIS, liaisons
- Portage à partir de IRIS GL, liaisons
- portage vers OpenGL à partir de IRIS GL, liaisons
- Portage OpenGL depuis IRIS GL, liaisons
- Portage du grand livre de l’IRIS, ensembles
- Portage à partir de IRIS GL, ensembles
- portage vers OpenGL à partir de IRIS GL, ensembles
- Portage OpenGL à partir de IRIS GL, ensembles
- definitions
- lie
- jeux
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0f9a88253390ee99f5b5870fd7a09e272f1c549
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106509784"
---
# <a name="porting-defs-binds-and-sets"></a><span data-ttu-id="609c7-118">Portage des ensembles de paramètres, des liaisons et des ensembles</span><span class="sxs-lookup"><span data-stu-id="609c7-118">Porting Defs, Binds, and Sets</span></span>

<span data-ttu-id="609c7-119">OpenGL n’a pas de tables de définitions stockées ; vous ne pouvez pas définir des modèles d’éclairage, du matériel, des textures, des styles de ligne ou des modèles en tant qu’objets distincts, comme vous pouvez le faire dans IRIS GL.</span><span class="sxs-lookup"><span data-stu-id="609c7-119">OpenGL doesn't have tables of stored definitions; you can't define lighting models, material, textures, line styles, or patterns as separate objects as you can in IRIS GL.</span></span> <span data-ttu-id="609c7-120">Ainsi, OpenGL n’a pas d’équivalent direct aux fonctions suivantes de la comptabilité IRIS :</span><span class="sxs-lookup"><span data-stu-id="609c7-120">Thus OpenGL has no direct equivalents to the following IRIS GL functions:</span></span>

-   <span data-ttu-id="609c7-121">**Imdef** et **lier**</span><span class="sxs-lookup"><span data-stu-id="609c7-121">**Imdef** and **Imbind**</span></span>
-   <span data-ttu-id="609c7-122">**tevdef** et **tevbind**</span><span class="sxs-lookup"><span data-stu-id="609c7-122">**tevdef** and **tevbind**</span></span>
-   <span data-ttu-id="609c7-123">**textdef** et **textbind**</span><span class="sxs-lookup"><span data-stu-id="609c7-123">**textdef** and **textbind**</span></span>
-   <span data-ttu-id="609c7-124">**definestyle** et **SetStyle**</span><span class="sxs-lookup"><span data-stu-id="609c7-124">**definestyle** and **setstyle**</span></span>
-   <span data-ttu-id="609c7-125">**defpattern** et **setPattern**</span><span class="sxs-lookup"><span data-stu-id="609c7-125">**defpattern** and **setpattern**</span></span>

<span data-ttu-id="609c7-126">Vous pouvez utiliser des listes d’affichage OpenGL pour imiter le mécanisme de définition/liaison de l’IRIS dans le GL.</span><span class="sxs-lookup"><span data-stu-id="609c7-126">You can use OpenGL display lists to mimic the IRIS GL def/bind mechanism.</span></span> <span data-ttu-id="609c7-127">Par exemple, voici une définition de matériau dans IRIS GL :</span><span class="sxs-lookup"><span data-stu-id="609c7-127">For example, here is a material definition in IRIS GL:</span></span>


```C++
float mat() = { 
    AMBIENT, .1, .1, .1, 
    DIFFUSE, 0, .369, .165, 
    SPECULAR, .5, .5, .5, 
    SHININESS, 10, 
    LMNULL 
}; 
lmdef(DEFMATERIAL, 1, 0, mat); 
lmbind(MATERIAL, 1);
```



<span data-ttu-id="609c7-128">L’exemple de code OpenGL suivant définit le même matériau dans une liste d’affichage référencée par le numéro de liste défini par **MYMATERIAL**.</span><span class="sxs-lookup"><span data-stu-id="609c7-128">The following OpenGL code sample defines the same material in a display list that is referred to by the list number defined by **MYMATERIAL**.</span></span>


```C++
#define MYMATERIAL 10 
 
GLfloat        mat_amb[] = {.1, .1, .1, 1.0}; 
GLfloat        mat_dif[] = {0, .369, .165, 1.0}; 
GLfloat        mat_spec[] = {.5, .5, .5, 1.0}; 
 
glNewList(MYMATERIAL, GL_COMPILE); 
    glMaterialfv(GL_FRONT, GL_AMBIENT, mat_amb); 
    glMaterialfv(GL_FRONT, GL_DIFFUSE, mat_dif); 
    glMaterialfv(GL_FRONT, GL_SHININESS, 10); 
glEndList(); 
 
glCallList( MYMATERIAL );
```



 

 




