---
title: Portage de la couleur, de l’ombrage et du code Writemask
description: Portage de la couleur, de l’ombrage et du code Writemask
ms.assetid: ffcf33b2-c3b8-4e89-9c2f-085b98cbb496
keywords:
- Portage du GL IRIS, couleur
- Portage à partir de IRIS GL, couleur
- portage vers OpenGL à partir de IRIS GL, couleur
- Portage OpenGL à partir de IRIS GL, couleur
- Portage de l’IRIS dans le GL, ombrage
- Portage à partir de IRIS GL, ombrage
- portage vers OpenGL à partir de IRIS GL, ombrage
- Portage OpenGL à partir de IRIS GL, ombrage
- Portage du grand livre de l’IRIS, writemask
- Portage à partir de IRIS GL, writemask
- portage vers OpenGL à partir de IRIS GL, writemask
- Portage OpenGL à partir de IRIS GL, writemask
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f8bc35986bc0f9d7076411fecbd9c1fa5d7bfbc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671845"
---
# <a name="porting-color-shading-and-writemask-code"></a><span data-ttu-id="50f6a-115">Portage de la couleur, de l’ombrage et du code Writemask</span><span class="sxs-lookup"><span data-stu-id="50f6a-115">Porting Color, Shading, and Writemask Code</span></span>

<span data-ttu-id="50f6a-116">Lorsque vous portez des couleurs, des ombrages et du code writemask à OpenGL, gardez les points suivants à l’esprit :</span><span class="sxs-lookup"><span data-stu-id="50f6a-116">When porting color, shading, and writemask code to OpenGL, keep the following points in mind:</span></span>

-   <span data-ttu-id="50f6a-117">Bien que vous puissiez définir des index de carte de couleurs avec la fonction OpenGL [glIndex](glindex-functions.md) , OpenGL ne dispose pas d’une fonction pour le chargement d’index de carte de couleurs.</span><span class="sxs-lookup"><span data-stu-id="50f6a-117">Though you can set color-map indexes with the OpenGL [glIndex](glindex-functions.md) function, OpenGL does not have a function for loading color-map indexes.</span></span>
-   <span data-ttu-id="50f6a-118">Les valeurs de couleur sont normalisées en fonction de leur type de données.</span><span class="sxs-lookup"><span data-stu-id="50f6a-118">Color values are normalized to their data type.</span></span> <span data-ttu-id="50f6a-119">(Pour plus d’informations sur les valeurs de couleur, consultez [glColor](glcolor-functions.md)).</span><span class="sxs-lookup"><span data-stu-id="50f6a-119">(For information about color values, see [glColor](glcolor-functions.md)).</span></span>
-   <span data-ttu-id="50f6a-120">Il n’existe aucun équivalent simple pour **cpack**.</span><span class="sxs-lookup"><span data-stu-id="50f6a-120">There is no simple equivalent for **cpack**.</span></span>
-   <span data-ttu-id="50f6a-121">Vous devrez peut-être traduire le code qui comprend les fonctions **c** ou **Color** en [**glClearColor**](glclearcolor.md) ou [**glClearIndex**](glclearindex.md) au lieu de **glColor** ou **glIndex**.</span><span class="sxs-lookup"><span data-stu-id="50f6a-121">You may have to translate code that includes the **c** or **color** functions to [**glClearColor**](glclearcolor.md) or [**glClearIndex**](glclearindex.md) instead of **glColor** or **glIndex**.</span></span>
-   <span data-ttu-id="50f6a-122">Le writemask RVBA s’applique à chaque composant, mais pas à chaque bit.</span><span class="sxs-lookup"><span data-stu-id="50f6a-122">The RGBA writemask applies to each component but not for each bit.</span></span>
-   <span data-ttu-id="50f6a-123">IRIS GL fournit des constantes de couleur définies : noir, bleu, rouge, vert, MAGENTA, CYAN, jaune et blanc.</span><span class="sxs-lookup"><span data-stu-id="50f6a-123">IRIS GL provides defined color constants: BLACK, BLUE, RED, GREEN, MAGENTA, CYAN, YELLOW, and WHITE.</span></span> <span data-ttu-id="50f6a-124">OpenGL ne fournit pas ces constantes.</span><span class="sxs-lookup"><span data-stu-id="50f6a-124">OpenGL does not provide these constants.</span></span>

<span data-ttu-id="50f6a-125">Cette rubrique contient des informations sur les éléments suivants.</span><span class="sxs-lookup"><span data-stu-id="50f6a-125">This topic includes information on the following.</span></span>

-   [<span data-ttu-id="50f6a-126">Portage des appels de couleur</span><span class="sxs-lookup"><span data-stu-id="50f6a-126">Porting Color Calls</span></span>](porting-color-calls.md)
-   [<span data-ttu-id="50f6a-127">Portage de modèles d’ombrage</span><span class="sxs-lookup"><span data-stu-id="50f6a-127">Porting Shading Models</span></span>](porting-shading-models.md)

 

 




