---
title: Portage d’objets NURBS
description: OpenGL traite la courbe NURBS comme des objets, de la même manière qu’elle traite Quadrics vous créez un objet NURBS, puis spécifiez la façon dont il doit être rendu. Le tableau suivant répertorie les fonctions GLU OpenGL pour la gestion des objets NURBS.
ms.assetid: baddf81b-219f-44bb-aa17-37404028b258
keywords:
- Portage de l’IRIS dans le GL, objets NURBS
- Portage à partir de IRIS GL, objets NURBS
- portage vers OpenGL à partir de IRIS GL, objets NURBS
- Portage OpenGL à partir de IRIS GL, objets NURBS
- Objets NURBS
- NURBS (non-uniform rational B-spline)
- B-spline rationnelle non uniforme (NURBS)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e0e56c06eea4e4a9a48f9062205277f8b999499
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380117"
---
# <a name="porting-nurbs-objects"></a><span data-ttu-id="226e4-111">Portage d’objets NURBS</span><span class="sxs-lookup"><span data-stu-id="226e4-111">Porting NURBS Objects</span></span>

<span data-ttu-id="226e4-112">OpenGL traite la courbe NURBS comme des objets, de la même manière qu’elle traite Quadrics : vous créez un objet NURBS, puis vous spécifiez comment il doit être rendu.</span><span class="sxs-lookup"><span data-stu-id="226e4-112">OpenGL treats NURBS as objects, similar to the way it treats quadrics: you create a NURBS object and then specify how it should be rendered.</span></span> <span data-ttu-id="226e4-113">Le tableau suivant répertorie les fonctions GLU OpenGL pour la gestion des objets NURBS.</span><span class="sxs-lookup"><span data-stu-id="226e4-113">The following table lists the OpenGL GLU functions for managing NURBS objects.</span></span>



| <span data-ttu-id="226e4-114">Fonction OpenGL GLU</span><span class="sxs-lookup"><span data-stu-id="226e4-114">OpenGL GLU function</span></span>                                      | <span data-ttu-id="226e4-115">Signification</span><span class="sxs-lookup"><span data-stu-id="226e4-115">Meaning</span></span>                                                        |
|----------------------------------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="226e4-116">**gluNewNurbsRenderer**</span><span class="sxs-lookup"><span data-stu-id="226e4-116">**gluNewNurbsRenderer**</span></span>](glunewnurbsrenderer.md)       | <span data-ttu-id="226e4-117">Crée un nouvel objet NURBS.</span><span class="sxs-lookup"><span data-stu-id="226e4-117">Creates a new NURBS object.</span></span>                                    |
| [<span data-ttu-id="226e4-118">**gluDeleteNurbsRenderer**</span><span class="sxs-lookup"><span data-stu-id="226e4-118">**gluDeleteNurbsRenderer**</span></span>](gludeletenurbsrenderer.md) | <span data-ttu-id="226e4-119">Supprime un objet NURBS.</span><span class="sxs-lookup"><span data-stu-id="226e4-119">Deletes a NURBS object.</span></span>                                        |
| [<span data-ttu-id="226e4-120">*gluNurbsCallback*</span><span class="sxs-lookup"><span data-stu-id="226e4-120">*gluNurbsCallback*</span></span>](glunurbs.md)                       | <span data-ttu-id="226e4-121">Associe un rappel à un objet NURBS pour la gestion des erreurs.</span><span class="sxs-lookup"><span data-stu-id="226e4-121">Associates a callback with a NURBS object, for error handling.</span></span> |



 

<span data-ttu-id="226e4-122">Lors du Portage du code NURBS du GL IRIS vers OpenGL, gardez les points suivants à l’esprit :</span><span class="sxs-lookup"><span data-stu-id="226e4-122">When porting IRIS GL NURBS code to OpenGL, keep the following points in mind:</span></span>

-   <span data-ttu-id="226e4-123">Les points de contrôle NURBS sont des valeurs float, et non des doubles.</span><span class="sxs-lookup"><span data-stu-id="226e4-123">NURBS control points are floats, not doubles.</span></span>
-   <span data-ttu-id="226e4-124">Le paramètre Stride est compté en valeurs float, et non en octets.</span><span class="sxs-lookup"><span data-stu-id="226e4-124">The stride parameter is counted in floats, not bytes.</span></span>
-   <span data-ttu-id="226e4-125">Si vous utilisez l’éclairage et que vous ne spécifiez pas de normales, appelez [**glEnable**](glenable.md) avec GL \_ auto \_ normal comme paramètre pour générer automatiquement des normales.</span><span class="sxs-lookup"><span data-stu-id="226e4-125">If you're using lighting and you're not specifying normals, call [**glEnable**](glenable.md) with GL\_AUTO\_NORMAL as the parameter to generate normals automatically.</span></span>

<span data-ttu-id="226e4-126">??</span><span class="sxs-lookup"><span data-stu-id="226e4-126">??</span></span>

 

 




