---
title: Portage des fonctions de courbe et de surface
description: Portage des fonctions de courbe et de surface
ms.assetid: 2e80f742-6665-4e7c-a8a1-c43c4764ccc8
keywords:
- Portage de l’IRIS dans le GL, courbes
- Portage à partir de IRIS GL, courbes
- portage vers OpenGL à partir de IRIS GL, courbes
- Portage OpenGL à partir de IRIS GL, courbes
- Portage de l’IRIS dans le GL, carreaux de surface
- Portage à partir de IRIS GL, carreaux de surface
- portage vers OpenGL à partir de IRIS GL, carreaux de surface
- Portage OpenGL à partir de IRIS GL, carreaux de surface
- courbes
- carreaux de surface
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3caedc89697d1c83325a00b3dc1cb55c34612e64
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309454"
---
# <a name="porting-curve-and-surface-functions"></a><span data-ttu-id="1606f-113">Portage des fonctions de courbe et de surface</span><span class="sxs-lookup"><span data-stu-id="1606f-113">Porting Curve and Surface Functions</span></span>

<span data-ttu-id="1606f-114">OpenGL ne prend pas en charge les équivalents des fonctions IRIS GL pour les courbes et les carreaux de surface.</span><span class="sxs-lookup"><span data-stu-id="1606f-114">OpenGL doesn't support equivalents to the IRIS GL functions for curves and surface patches.</span></span> <span data-ttu-id="1606f-115">Vous devez réécrire votre code s’il comprend l’un des appels suivants :</span><span class="sxs-lookup"><span data-stu-id="1606f-115">You'll need to rewrite your code if it includes any of the following calls:</span></span>

-   <span data-ttu-id="1606f-116">**defbasis**</span><span class="sxs-lookup"><span data-stu-id="1606f-116">**defbasis**</span></span>
-   <span data-ttu-id="1606f-117">**curvebasis**, **curveprecision**, **CRV**, **CrVn**, **RCRV**, **rcrvn** et **curveit**</span><span class="sxs-lookup"><span data-stu-id="1606f-117">**curvebasis**, **curveprecision**, **crv**, **crvn**, **rcrv**, **rcrvn**, and **curveit**</span></span>
-   <span data-ttu-id="1606f-118">**patchbasis**, **patchcurves**, **patchprecision**, **patch** et **rpatch**</span><span class="sxs-lookup"><span data-stu-id="1606f-118">**patchbasis**, **patchcurves**, **patchprecision**, **patch**, and **rpatch**</span></span>

<span data-ttu-id="1606f-119">Cette rubrique contient des informations sur les éléments suivants.</span><span class="sxs-lookup"><span data-stu-id="1606f-119">This topic includes information on the following.</span></span>

-   [<span data-ttu-id="1606f-120">Portage d’objets NURBS</span><span class="sxs-lookup"><span data-stu-id="1606f-120">Porting NURBS Objects</span></span>](porting-nurbs-objects.md)
-   [<span data-ttu-id="1606f-121">Portage de courbes NURBS</span><span class="sxs-lookup"><span data-stu-id="1606f-121">Porting NURBS Curves</span></span>](porting-nurbs-curves.md)
-   [<span data-ttu-id="1606f-122">Portage des courbes de suppression</span><span class="sxs-lookup"><span data-stu-id="1606f-122">Porting Trimming Curves</span></span>](porting-trimming-curves.md)
-   [<span data-ttu-id="1606f-123">Portage des surfaces NURBS</span><span class="sxs-lookup"><span data-stu-id="1606f-123">Porting NURBS Surfaces</span></span>](porting-nurbs-surfaces.md)

 

 




