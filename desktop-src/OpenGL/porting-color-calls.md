---
title: Portage des appels de couleur
description: Le tableau suivant répertorie les fonctions IRIS GL Color et leurs fonctions OpenGL équivalentes.
ms.assetid: 4ca6c311-d6c8-4d10-9e9c-770a8e6de4bb
keywords:
- Portage du GL IRIS, couleur
- Portage à partir de IRIS GL, couleur
- portage vers OpenGL à partir de IRIS GL, couleur
- Portage OpenGL à partir de IRIS GL, couleur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 856b9f9d0a62b866ac1c9981d9fbb716cf243341
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671842"
---
# <a name="porting-color-calls"></a><span data-ttu-id="9ddf9-107">Portage des appels de couleur</span><span class="sxs-lookup"><span data-stu-id="9ddf9-107">Porting Color Calls</span></span>

<span data-ttu-id="9ddf9-108">Le tableau suivant répertorie les fonctions IRIS GL Color et leurs fonctions OpenGL équivalentes.</span><span class="sxs-lookup"><span data-stu-id="9ddf9-108">The following table lists IRIS GL color functions and their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="9ddf9-109">Fonction IRIS GL</span><span class="sxs-lookup"><span data-stu-id="9ddf9-109">IRIS GL function</span></span>                  | <span data-ttu-id="9ddf9-110">Fonction OpenGL</span><span class="sxs-lookup"><span data-stu-id="9ddf9-110">OpenGL function</span></span>                                                                                                                               | <span data-ttu-id="9ddf9-111">Signification</span><span class="sxs-lookup"><span data-stu-id="9ddf9-111">Meaning</span></span>                                              |
|-----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <span data-ttu-id="9ddf9-112">**c**</span><span class="sxs-lookup"><span data-stu-id="9ddf9-112">**c**</span></span>                             | [<span data-ttu-id="9ddf9-113">glColor</span><span class="sxs-lookup"><span data-stu-id="9ddf9-113">glColor</span></span>](glcolor-functions.md)                                                                                                              | <span data-ttu-id="9ddf9-114">Définit la couleur RVB.</span><span class="sxs-lookup"><span data-stu-id="9ddf9-114">Sets RGB color.</span></span>                                      |
| <span data-ttu-id="9ddf9-115">**color**</span><span class="sxs-lookup"><span data-stu-id="9ddf9-115">**color**</span></span>                         | [<span data-ttu-id="9ddf9-116">glIndex</span><span class="sxs-lookup"><span data-stu-id="9ddf9-116">glIndex</span></span>](glindex-functions.md)                                                                                                              | <span data-ttu-id="9ddf9-117">Définit l’index de couleur.</span><span class="sxs-lookup"><span data-stu-id="9ddf9-117">Sets the color index.</span></span>                                |
| <span data-ttu-id="9ddf9-118">**GetColor**</span><span class="sxs-lookup"><span data-stu-id="9ddf9-118">**getcolor**</span></span>                      | <span data-ttu-id="9ddf9-119">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) (index actuel de la comptabilité \_ \_ )</span><span class="sxs-lookup"><span data-stu-id="9ddf9-119">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( GL\_CURRENT\_INDEX )</span></span>                                               | <span data-ttu-id="9ddf9-120">Retourne l’index de couleur actuel.</span><span class="sxs-lookup"><span data-stu-id="9ddf9-120">Returns the current color index.</span></span>                     |
| <span data-ttu-id="9ddf9-121">**getmcolor**</span><span class="sxs-lookup"><span data-stu-id="9ddf9-121">**getmcolor**</span></span>                     |                                                                                                                                               | <span data-ttu-id="9ddf9-122">Obtient une copie des valeurs RVB pour une entrée de la carte des couleurs.</span><span class="sxs-lookup"><span data-stu-id="9ddf9-122">Gets a copy of the RGB values for a color map entry.</span></span> |
| <span data-ttu-id="9ddf9-123">**gRGBcolor**</span><span class="sxs-lookup"><span data-stu-id="9ddf9-123">**gRGBcolor**</span></span>                     | <span data-ttu-id="9ddf9-124">**glGet**( \_ couleur actuelle du GL \_ )</span><span class="sxs-lookup"><span data-stu-id="9ddf9-124">**glGet**( GL\_CURRENT\_COLOR )</span></span>                                                                                                               | <span data-ttu-id="9ddf9-125">Obtient les valeurs de couleur RVB actuelles.</span><span class="sxs-lookup"><span data-stu-id="9ddf9-125">Gets the current RGB color values.</span></span>                   |
| <span data-ttu-id="9ddf9-126">**mapcolor**</span><span class="sxs-lookup"><span data-stu-id="9ddf9-126">**mapcolor**</span></span>                      |                                                                                                                                               |                                                      |
| <span data-ttu-id="9ddf9-127">**RGBcolor**</span><span class="sxs-lookup"><span data-stu-id="9ddf9-127">**RGBcolor**</span></span>                      | <span data-ttu-id="9ddf9-128">**glColor**</span><span class="sxs-lookup"><span data-stu-id="9ddf9-128">**glColor**</span></span>                                                                                                                                   | <span data-ttu-id="9ddf9-129">Définit la couleur RVB.</span><span class="sxs-lookup"><span data-stu-id="9ddf9-129">Sets RGB color.</span></span>                                      |
| <span data-ttu-id="9ddf9-130">**writemask**</span><span class="sxs-lookup"><span data-stu-id="9ddf9-130">**writemask**</span></span>                     | [<span data-ttu-id="9ddf9-131">**glIndexMask**</span><span class="sxs-lookup"><span data-stu-id="9ddf9-131">**glIndexMask**</span></span>](glindexmask.md)                                                                                                            | <span data-ttu-id="9ddf9-132">Définit le masque de couleur du mode d’index des couleurs.</span><span class="sxs-lookup"><span data-stu-id="9ddf9-132">Sets the color-index mode color mask.</span></span>                |
| <span data-ttu-id="9ddf9-133">**wmpackRGBwritemask**</span><span class="sxs-lookup"><span data-stu-id="9ddf9-133">**wmpackRGBwritemask**</span></span><br/> | [<span data-ttu-id="9ddf9-134">**glColorMask**</span><span class="sxs-lookup"><span data-stu-id="9ddf9-134">**glColorMask**</span></span>](glcolormask.md)                                                                                                            | <span data-ttu-id="9ddf9-135">Définit le masque du mode de couleurs RVB.</span><span class="sxs-lookup"><span data-stu-id="9ddf9-135">Sets the RGB color mode mask.</span></span>                        |
| <span data-ttu-id="9ddf9-136">**getwritemask**</span><span class="sxs-lookup"><span data-stu-id="9ddf9-136">**getwritemask**</span></span>                  | <span data-ttu-id="9ddf9-137">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) (GL \_ Color \_ WRITEMASK)**glGet**(GL \_ index \_ WRITEMASK)</span><span class="sxs-lookup"><span data-stu-id="9ddf9-137">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( GL\_COLOR\_WRITEMASK )**glGet**( GL\_INDEX\_WRITEMASK )</span></span><br/> | <span data-ttu-id="9ddf9-138">Obtient le masque de couleur.</span><span class="sxs-lookup"><span data-stu-id="9ddf9-138">Gets the color mask.</span></span>                                 |
| <span data-ttu-id="9ddf9-139">**gRGBmask**</span><span class="sxs-lookup"><span data-stu-id="9ddf9-139">**gRGBmask**</span></span>                      | <span data-ttu-id="9ddf9-140">**glGet**( \_ couleur GL \_ WRITEMASK)</span><span class="sxs-lookup"><span data-stu-id="9ddf9-140">**glGet**( GL\_COLOR\_WRITEMASK )</span></span>                                                                                                             | <span data-ttu-id="9ddf9-141">Obtient le masque de couleur.</span><span class="sxs-lookup"><span data-stu-id="9ddf9-141">Gets the color mask.</span></span>                                 |
| <span data-ttu-id="9ddf9-142">**zwritemask**</span><span class="sxs-lookup"><span data-stu-id="9ddf9-142">**zwritemask**</span></span>                    | [<span data-ttu-id="9ddf9-143">**glDepthMask**</span><span class="sxs-lookup"><span data-stu-id="9ddf9-143">**glDepthMask**</span></span>](gldepthmask.md)                                                                                                            |                                                      |



 

> [!Note]
>
> <span data-ttu-id="9ddf9-144">Soyez prudent lors du remplacement de **zwritemask** par [**glDepthMask**](gldepthmask.md); **glDepthMask** accepte un argument booléen, tandis que **zwritemask** prend un champ de bits.</span><span class="sxs-lookup"><span data-stu-id="9ddf9-144">Be careful when replacing **zwritemask** with [**glDepthMask**](gldepthmask.md); **glDepthMask** takes a Boolean argument, whereas **zwritemask** takes a bit field.</span></span>

 

<span data-ttu-id="9ddf9-145">Si vous souhaitez utiliser plusieurs cartes de couleurs, vous devez utiliser les fonctions de mappage de couleurs Windows appropriées.</span><span class="sxs-lookup"><span data-stu-id="9ddf9-145">If you want to use multiple color maps, you need to use the appropriate Windows color map functions.</span></span> <span data-ttu-id="9ddf9-146">Par conséquent, **Multimap**, **onemap**, **getcmmode**, **setmap** et **GetMap** n’ont pas d’équivalents OpenGL.</span><span class="sxs-lookup"><span data-stu-id="9ddf9-146">Therefore, **multimap**, **onemap**, **getcmmode**, **setmap**, and **getmap** have no OpenGL equivalents.</span></span>

 

 





