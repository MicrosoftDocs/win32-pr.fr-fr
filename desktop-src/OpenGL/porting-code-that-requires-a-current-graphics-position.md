---
title: Code de port qui a besoin d’une position graphique actuelle
description: OpenGL ne conserve pas la position graphique actuelle. Les fonctions de l’IRIS du GL qui dépendent de la position graphique actuelle, telles que déplacer, dessiner et RMV, n’ont pas d’équivalents dans OpenGL.
ms.assetid: d6c42d9c-6fbb-4b72-8097-285d19b619c2
keywords:
- Portage de l’IRIS dans le GL, position graphique actuelle
- Portage à partir de IRIS GL, position graphique actuelle
- portage vers OpenGL à partir de IRIS GL, position graphique actuelle
- Portage OpenGL depuis IRIS GL, position graphique actuelle
- position graphique actuelle
- positions raster
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd7e7cbbaf0a22385c83569775758e24f70cd210
ms.sourcegitcommit: b95a94ffffda33f9ebbdd41787c01866444b4cf4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/27/2019
ms.locfileid: "103679265"
---
# <a name="port-code-that-needs-a-current-graphics-position"></a><span data-ttu-id="8d9ed-110">Code de port qui a besoin d’une position graphique actuelle</span><span class="sxs-lookup"><span data-stu-id="8d9ed-110">Port code that needs a current graphics position</span></span>

<span data-ttu-id="8d9ed-111">OpenGL ne conserve pas la position graphique actuelle.</span><span class="sxs-lookup"><span data-stu-id="8d9ed-111">OpenGL does not maintain a current graphics position.</span></span> <span data-ttu-id="8d9ed-112">Les fonctions de l’IRIS du GL qui dépendent de la position graphique actuelle, telles que **déplacer**, **dessiner** et **RMV**, n’ont pas d’équivalents dans OpenGL.</span><span class="sxs-lookup"><span data-stu-id="8d9ed-112">IRIS GL functions that depend on the current graphics position, such as **move**, **draw**, and **rmv**, have no equivalents in OpenGL.</span></span>

<span data-ttu-id="8d9ed-113">Les anciennes versions de IRIS GL comprenaient des commandes de dessin reposant sur la position graphique actuelle, bien que leur utilisation soit déconseillée.</span><span class="sxs-lookup"><span data-stu-id="8d9ed-113">Older versions of IRIS GL included drawing commands that relied upon the current graphics position, though their use has been discouraged.</span></span> <span data-ttu-id="8d9ed-114">Vous devrez réécrire votre code si vous vous reposez sur la position graphique actuelle de quelque manière que ce soit, ou si vous utilisez l’une des routines suivantes :</span><span class="sxs-lookup"><span data-stu-id="8d9ed-114">You will need to rewrite your code if you relied on the current graphics position in any way, or used any of the following routines:</span></span>

-   <span data-ttu-id="8d9ed-115">**dessiner** et **déplacer**</span><span class="sxs-lookup"><span data-stu-id="8d9ed-115">**draw** and **move**</span></span>
-   <span data-ttu-id="8d9ed-116">**PMV**, **PDR** et **PCLOS**</span><span class="sxs-lookup"><span data-stu-id="8d9ed-116">**pmv**, **pdr**, and **pclos**</span></span>
-   <span data-ttu-id="8d9ed-117">**RDR**, **RMV**, **rpdr** et **rpmv**</span><span class="sxs-lookup"><span data-stu-id="8d9ed-117">**rdr**, **rmv**, **rpdr**, and **rpmv**</span></span>
-   <span data-ttu-id="8d9ed-118">**getgpos**</span><span class="sxs-lookup"><span data-stu-id="8d9ed-118">**getgpos**</span></span>

<span data-ttu-id="8d9ed-119">OpenGL présente un concept de position raster qui correspond à la position actuelle du caractère de l’IRIS du GL.</span><span class="sxs-lookup"><span data-stu-id="8d9ed-119">OpenGL has a concept of raster position that corresponds to IRIS GL's current character position.</span></span> <span data-ttu-id="8d9ed-120">Pour plus d’informations sur le positionnement de la trame, consultez [Portage d’opérations de pixels](porting-pixel-operations.md).</span><span class="sxs-lookup"><span data-stu-id="8d9ed-120">For more information on raster positioning, see [Porting Pixel Operations](porting-pixel-operations.md).</span></span>

<span data-ttu-id="8d9ed-121">Cette rubrique contient des informations sur les éléments suivants.</span><span class="sxs-lookup"><span data-stu-id="8d9ed-121">This topic includes information on the following.</span></span>

-   [<span data-ttu-id="8d9ed-122">Portage de l’écran et des commandes de vidage de la mémoire tampon</span><span class="sxs-lookup"><span data-stu-id="8d9ed-122">Porting Screen and Buffer Clearing Commands</span></span>](porting-screen-and-buffer-clearing-commands.md)
-   [<span data-ttu-id="8d9ed-123">Fonctions de transformation et de matrice de Portage</span><span class="sxs-lookup"><span data-stu-id="8d9ed-123">Porting Matrix and Transformation Functions</span></span>](porting-matrix-and-transformation-functions.md)
-   [<span data-ttu-id="8d9ed-124">Portage du code en mode MSINGLE</span><span class="sxs-lookup"><span data-stu-id="8d9ed-124">Porting MSINGLE Mode Code</span></span>](porting-msingle-mode-code.md)
-   [<span data-ttu-id="8d9ed-125">Portage de fonctions qui obtiennent des matrices et des transformations</span><span class="sxs-lookup"><span data-stu-id="8d9ed-125">Porting Functions that Get Matrices and Transformations</span></span>](porting-functions-that-get-matrices-and-transformations.md)
-   [<span data-ttu-id="8d9ed-126">Portage des Viewports, Screenmasks et Scrboxes</span><span class="sxs-lookup"><span data-stu-id="8d9ed-126">Porting Viewports, Screenmasks, and Scrboxes</span></span>](porting-viewports--screenmasks--and-scrboxes.md)
-   [<span data-ttu-id="8d9ed-127">Portage des plans de découpage</span><span class="sxs-lookup"><span data-stu-id="8d9ed-127">Porting Clipping Planes</span></span>](porting-clipping-planes.md)

 

 




