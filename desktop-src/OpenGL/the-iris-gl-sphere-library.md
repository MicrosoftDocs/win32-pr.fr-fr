---
title: Bibliothèque de sphères du GL IRIS
description: OpenGL ne prend pas en charge la bibliothèque de sphères du GL IRIS. Vous pouvez remplacer vos appels de la bibliothèque de sphères par des routines Quadrics à partir de la bibliothèque GLU. Pour plus d’informations sur la bibliothèque GLU, consultez le Guide de programmation Open GL et la bibliothèque de l’utilitaire OpenGL.
ms.assetid: 2b7e6a3d-d2d0-4b54-8dff-8c4d6b113007
keywords:
- Portage du GL IRIS, bibliothèque Sphere
- Portage à partir de IRIS GL, bibliothèque de sphères
- portage vers OpenGL à partir de IRIS GL, bibliothèque de sphères
- Portage OpenGL depuis IRIS GL, bibliothèque de sphères
- fonctions de dessin, bibliothèque de sphères
- bibliothèque de sphères
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 586974c5874aee73121e536cbadca4564a18c250
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310361"
---
# <a name="the-iris-gl-sphere-library"></a><span data-ttu-id="cc831-111">Bibliothèque de sphères du GL IRIS</span><span class="sxs-lookup"><span data-stu-id="cc831-111">The IRIS GL Sphere Library</span></span>

<span data-ttu-id="cc831-112">OpenGL ne prend pas en charge la bibliothèque de sphères du GL IRIS.</span><span class="sxs-lookup"><span data-stu-id="cc831-112">OpenGL does not support the IRIS GL sphere library.</span></span> <span data-ttu-id="cc831-113">Vous pouvez remplacer vos appels de la bibliothèque de sphères par des routines Quadrics à partir de la bibliothèque GLU.</span><span class="sxs-lookup"><span data-stu-id="cc831-113">You can replace your sphere library calls with quadrics routines from the GLU library.</span></span> <span data-ttu-id="cc831-114">Pour plus d’informations sur la bibliothèque GLU, consultez le *Guide de programmation Open GL* et la bibliothèque de l' [utilitaire OpenGL](opengl-utility-library.md).</span><span class="sxs-lookup"><span data-stu-id="cc831-114">For more information about the GLU library, see the *Open GL Programming Guide* and [OpenGL Utility Library](opengl-utility-library.md).</span></span>

<span data-ttu-id="cc831-115">Le tableau suivant répertorie les fonctions Quadrics OpenGL.</span><span class="sxs-lookup"><span data-stu-id="cc831-115">The following table lists the OpenGL quadrics functions.</span></span>



| <span data-ttu-id="cc831-116">Fonction OpenGL</span><span class="sxs-lookup"><span data-stu-id="cc831-116">OpenGL function</span></span>                                        | <span data-ttu-id="cc831-117">Signification</span><span class="sxs-lookup"><span data-stu-id="cc831-117">Meaning</span></span>                                                          |
|--------------------------------------------------------|------------------------------------------------------------------|
| [<span data-ttu-id="cc831-118">**gluNewQuadric**</span><span class="sxs-lookup"><span data-stu-id="cc831-118">**gluNewQuadric**</span></span>](glunewquadric.md)                 | <span data-ttu-id="cc831-119">Crée un nouvel objet quadric.</span><span class="sxs-lookup"><span data-stu-id="cc831-119">Creates a new quadric object.</span></span>                                    |
| [<span data-ttu-id="cc831-120">**gluDeleteQuadric**</span><span class="sxs-lookup"><span data-stu-id="cc831-120">**gluDeleteQuadric**</span></span>](gludeletequadric.md)           | <span data-ttu-id="cc831-121">Supprime un objet quadric.</span><span class="sxs-lookup"><span data-stu-id="cc831-121">Deletes a quadric object.</span></span>                                        |
| [<span data-ttu-id="cc831-122">*gluQuadricCallback*</span><span class="sxs-lookup"><span data-stu-id="cc831-122">*gluQuadricCallback*</span></span>](gluquadric.md)                 | <span data-ttu-id="cc831-123">Associe un rappel à un objet quadric, pour la gestion des erreurs.</span><span class="sxs-lookup"><span data-stu-id="cc831-123">Associates a callback with a quadric object, for error handling.</span></span> |
| [<span data-ttu-id="cc831-124">**gluQuadricNormals**</span><span class="sxs-lookup"><span data-stu-id="cc831-124">**gluQuadricNormals**</span></span>](gluquadricnormals.md)         | <span data-ttu-id="cc831-125">Spécifie les normales : aucune normale, une par face ou une par vertex.</span><span class="sxs-lookup"><span data-stu-id="cc831-125">Specifies normals: no normals, one per face, or one per vertex.</span></span>  |
| [<span data-ttu-id="cc831-126">**gluQuadricOrientation**</span><span class="sxs-lookup"><span data-stu-id="cc831-126">**gluQuadricOrientation**</span></span>](gluquadricorientation.md) | <span data-ttu-id="cc831-127">Spécifie la direction des normales : vers l’extérieur ou vers l’intérieur.</span><span class="sxs-lookup"><span data-stu-id="cc831-127">Specifies direction of normals: outward or inward.</span></span>               |
| [<span data-ttu-id="cc831-128">**gluQuadricTexture**</span><span class="sxs-lookup"><span data-stu-id="cc831-128">**gluQuadricTexture**</span></span>](gluquadrictexture.md)         | <span data-ttu-id="cc831-129">Active ou désactive la génération des coordonnées de texture.</span><span class="sxs-lookup"><span data-stu-id="cc831-129">Turns texture-coordinate generation on or off.</span></span>                   |
| [<span data-ttu-id="cc831-130">**gluQuadricDrawstyle**</span><span class="sxs-lookup"><span data-stu-id="cc831-130">**gluQuadricDrawstyle**</span></span>](gluquadricdrawstyle.md)     | <span data-ttu-id="cc831-131">Spécifie le style de dessin : polygones, lignes, points, etc.</span><span class="sxs-lookup"><span data-stu-id="cc831-131">Specifies drawing style: polygons, lines, points, and so on.</span></span>     |
| [<span data-ttu-id="cc831-132">**gluSphere**</span><span class="sxs-lookup"><span data-stu-id="cc831-132">**gluSphere**</span></span>](glusphere.md)                         | <span data-ttu-id="cc831-133">Dessine une sphère.</span><span class="sxs-lookup"><span data-stu-id="cc831-133">Draws a sphere.</span></span>                                                  |
| [<span data-ttu-id="cc831-134">**gluCylinder**</span><span class="sxs-lookup"><span data-stu-id="cc831-134">**gluCylinder**</span></span>](glucylinder.md)                     | <span data-ttu-id="cc831-135">Dessine un cylindre ou un cône.</span><span class="sxs-lookup"><span data-stu-id="cc831-135">Draws a cylinder or cone.</span></span>                                        |
| [<span data-ttu-id="cc831-136">**gluPartialDisk**</span><span class="sxs-lookup"><span data-stu-id="cc831-136">**gluPartialDisk**</span></span>](glupartialdisk.md)               | <span data-ttu-id="cc831-137">Dessine un arc.</span><span class="sxs-lookup"><span data-stu-id="cc831-137">Draws an arc.</span></span>                                                    |
| [<span data-ttu-id="cc831-138">**gluDisk**</span><span class="sxs-lookup"><span data-stu-id="cc831-138">**gluDisk**</span></span>](gludisk.md)                             | <span data-ttu-id="cc831-139">Dessine un cercle ou un disque.</span><span class="sxs-lookup"><span data-stu-id="cc831-139">Draws a circle or disk.</span></span>                                          |



 

<span data-ttu-id="cc831-140">Vous pouvez utiliser un objet quadric pour tous les Quadrics que vous souhaitez afficher de la même manière.</span><span class="sxs-lookup"><span data-stu-id="cc831-140">You can use one quadric object for all quadrics you want to render in similar ways.</span></span> <span data-ttu-id="cc831-141">L’exemple de code suivant utilise deux objets quadric pour dessiner quatre Quadrics, deux d’entre eux texturés.</span><span class="sxs-lookup"><span data-stu-id="cc831-141">The following code sample uses two quadric objects to draw four quadrics, two of them textured.</span></span>


```C++
GLUquadricObj    *texturedQuad, *plainQuad; 
 
texturedQuad = gluNewQuadric(void); 
gluQuadricTexture(texturedQuad, GL_TRUE); 
gluQuadricOrientation(texturedQuad, GLU_OUTSIDE); 
gluQuadricDrawStyle(texturedQuad, GLU_FILL); 
 
plainQuad = gluNewQuadric(void); 
gluQuadricDrawStyle(plainQuad, GLU_LINE); 
 
glColor3f (1.0, 1.0, 1.0); 
 
gluSphere(texturedQuad, 5.0, 20, 20); 
glTranslatef(10.0, 10.0, 0.0); 
gluCylinder(texturedQuad, 2.5, 5, 5, 10, 10); 
glTranslatef(10.0, 10.0, 0.0); 
gluDisk(plainQuad, 2.0, 5.0, 10, 10); 
glTranslatef(10.0, 10.0, 0.0); 
gluSphere(plainQuad, 5.0, 20, 20);
```



 

 




