---
title: Portage des sphères
description: En cas de portage vers OpenGL, gardez les points suivants à l’esprit
ms.assetid: ca6bb515-076d-45fc-bcdd-3d71877560fb
keywords:
- Portage de l’IRIS dans le GL, sphères
- Portage à partir de IRIS GL, sphères
- portage vers OpenGL depuis IRIS GL, sphères
- Portage OpenGL depuis IRIS GL, sphères
- fonctions de dessin, sphères
- sphères
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f48ac31c0204111173d9eb2d31a3119873ef45b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380113"
---
# <a name="porting-spheres"></a><span data-ttu-id="95daa-109">Portage des sphères</span><span class="sxs-lookup"><span data-stu-id="95daa-109">Porting Spheres</span></span>

<span data-ttu-id="95daa-110">En cas de portage vers OpenGL, gardez les points suivants à l’esprit :</span><span class="sxs-lookup"><span data-stu-id="95daa-110">When porting spheres to OpenGL, keep the following points in mind:</span></span>

-   <span data-ttu-id="95daa-111">Vous ne pouvez pas contrôler le type de primitives utilisées pour dessiner la sphère.</span><span class="sxs-lookup"><span data-stu-id="95daa-111">You cannot control the type of primitives used to draw the sphere.</span></span> <span data-ttu-id="95daa-112">Vous pouvez contrôler la précision de dessin d’une autre façon : utilisez les paramètres tranches et piles.</span><span class="sxs-lookup"><span data-stu-id="95daa-112">You can control drawing precision in another way: use the slices and stacks parameters.</span></span> <span data-ttu-id="95daa-113">Les tranches sont longitudinales ; les piles sont correspondantes.</span><span class="sxs-lookup"><span data-stu-id="95daa-113">Slices are longitudinal; stacks are latitudinal.</span></span>
-   <span data-ttu-id="95daa-114">Les sphères sont dessinées au centre de l’origine.</span><span class="sxs-lookup"><span data-stu-id="95daa-114">Spheres are drawn centered at the origin.</span></span> <span data-ttu-id="95daa-115">Au lieu de spécifier l’emplacement, comme vous le feriez avec la fonction IRIS GL **sphdraw** , faites précéder un appel à la fonction Glu [**gluSphere**](glusphere.md) d’une traduction.</span><span class="sxs-lookup"><span data-stu-id="95daa-115">Instead of specifying the location, as you do with the IRIS GL **sphdraw** function, precede a call to the GLU [**gluSphere**](glusphere.md) function with a translation.</span></span>
-   <span data-ttu-id="95daa-116">La bibliothèque de sphères n’est pas encore disponible pour OpenGL.</span><span class="sxs-lookup"><span data-stu-id="95daa-116">The sphere library is not yet available for OpenGL.</span></span>

<span data-ttu-id="95daa-117">Le tableau suivant répertorie les fonctions IRIS GL pour le dessin des sphères et leurs fonctions GLU équivalentes, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="95daa-117">The following table lists the IRIS GL functions for drawing spheres and their equivalent GLU functions where available.</span></span>



| <span data-ttu-id="95daa-118">Fonction IRIS GL</span><span class="sxs-lookup"><span data-stu-id="95daa-118">IRIS GL function</span></span> | <span data-ttu-id="95daa-119">GLU fonction)</span><span class="sxs-lookup"><span data-stu-id="95daa-119">GLU function</span></span>                                 | <span data-ttu-id="95daa-120">Signification</span><span class="sxs-lookup"><span data-stu-id="95daa-120">Meaning</span></span>                                       |
|------------------|----------------------------------------------|-----------------------------------------------|
| <span data-ttu-id="95daa-121">**sphobj**</span><span class="sxs-lookup"><span data-stu-id="95daa-121">**sphobj**</span></span>       | [<span data-ttu-id="95daa-122">**gluNewQuadric**</span><span class="sxs-lookup"><span data-stu-id="95daa-122">**gluNewQuadric**</span></span>](glunewquadric.md)       | <span data-ttu-id="95daa-123">Crée un objet Sphere.</span><span class="sxs-lookup"><span data-stu-id="95daa-123">Creates a new sphere object.</span></span>                  |
| <span data-ttu-id="95daa-124">**sphfree**</span><span class="sxs-lookup"><span data-stu-id="95daa-124">**sphfree**</span></span>      | [<span data-ttu-id="95daa-125">**gluDeleteQuadric**</span><span class="sxs-lookup"><span data-stu-id="95daa-125">**gluDeleteQuadric**</span></span>](gludeletequadric.md) | <span data-ttu-id="95daa-126">Supprime l’objet Sphere et la mémoire libre utilisés.</span><span class="sxs-lookup"><span data-stu-id="95daa-126">Deletes sphere object and free memory used.</span></span>   |
| <span data-ttu-id="95daa-127">**sphdraw**</span><span class="sxs-lookup"><span data-stu-id="95daa-127">**sphdraw**</span></span>      | [<span data-ttu-id="95daa-128">**gluSphere**</span><span class="sxs-lookup"><span data-stu-id="95daa-128">**gluSphere**</span></span>](glusphere.md)               | <span data-ttu-id="95daa-129">Dessine une sphère.</span><span class="sxs-lookup"><span data-stu-id="95daa-129">Draws a sphere.</span></span>                               |
| <span data-ttu-id="95daa-130">**sphmode**</span><span class="sxs-lookup"><span data-stu-id="95daa-130">**sphmode**</span></span>      |                                              | <span data-ttu-id="95daa-131">Définit les attributs de sphère.</span><span class="sxs-lookup"><span data-stu-id="95daa-131">Sets sphere attributes.</span></span>                       |
| <span data-ttu-id="95daa-132">**sphrotmatrix**</span><span class="sxs-lookup"><span data-stu-id="95daa-132">**sphrotmatrix**</span></span> |                                              | <span data-ttu-id="95daa-133">Contrôle l’orientation de la sphère.</span><span class="sxs-lookup"><span data-stu-id="95daa-133">Controls sphere orientation.</span></span>                  |
| <span data-ttu-id="95daa-134">**sphgnpolys**</span><span class="sxs-lookup"><span data-stu-id="95daa-134">**sphgnpolys**</span></span>   |                                              | <span data-ttu-id="95daa-135">Retourne le nombre de polygones dans la sphère actuelle.</span><span class="sxs-lookup"><span data-stu-id="95daa-135">Returns number of polygons in current sphere.</span></span> |



 

<span data-ttu-id="95daa-136">??</span><span class="sxs-lookup"><span data-stu-id="95daa-136">??</span></span>

 

 




