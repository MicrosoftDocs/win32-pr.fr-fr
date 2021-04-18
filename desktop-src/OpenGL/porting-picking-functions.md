---
title: Fonctions de sélection du Portage
description: Toutes les fonctions d’IRIS GL de prélèvement ont des équivalents OpenGL, à l’exception de clearhitcode. Le tableau suivant répertorie les fonctions d’IRIS du GL de prélèvement et leurs fonctions OpenGL équivalentes.
ms.assetid: f8fbd0c2-14bf-47bc-be7f-eeef346dbac1
keywords:
- Portage du GL d’IRIS, prélèvement
- Portage à partir de IRIS GL, prélèvement
- portage vers OpenGL à partir de IRIS GL, prélèvement
- Portage OpenGL depuis IRIS GL, prélèvement
- mat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db4c0ea6011860f7d5010dd0bb7d5d23b671d99a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106536268"
---
# <a name="porting-picking-functions"></a><span data-ttu-id="02569-109">Fonctions de sélection du Portage</span><span class="sxs-lookup"><span data-stu-id="02569-109">Porting Picking Functions</span></span>

<span data-ttu-id="02569-110">Toutes les fonctions d’IRIS GL de prélèvement ont des équivalents OpenGL, à l’exception de **clearhitcode**.</span><span class="sxs-lookup"><span data-stu-id="02569-110">All IRIS GL picking functions have OpenGL equivalents, with the exception of **clearhitcode**.</span></span> <span data-ttu-id="02569-111">Le tableau suivant répertorie les fonctions d’IRIS du GL de prélèvement et leurs fonctions OpenGL équivalentes.</span><span class="sxs-lookup"><span data-stu-id="02569-111">The following table lists the IRIS GL picking functions and their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="02569-112">Fonction IRIS GL</span><span class="sxs-lookup"><span data-stu-id="02569-112">IRIS GL function</span></span>                | <span data-ttu-id="02569-113">Fonction OpenGL</span><span class="sxs-lookup"><span data-stu-id="02569-113">OpenGL function</span></span>                                                                           | <span data-ttu-id="02569-114">Signification</span><span class="sxs-lookup"><span data-stu-id="02569-114">Meaning</span></span>                                |
|---------------------------------|-------------------------------------------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="02569-115">**clearhitcode**</span><span class="sxs-lookup"><span data-stu-id="02569-115">**clearhitcode**</span></span>                | <span data-ttu-id="02569-116">Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="02569-116">Not supported.</span></span>                                                                            | <span data-ttu-id="02569-117">Efface les variables globales et Hitcode.</span><span class="sxs-lookup"><span data-stu-id="02569-117">Clears global variable and hitcode.</span></span>    |
| <span data-ttu-id="02569-118">**pickselect**</span><span class="sxs-lookup"><span data-stu-id="02569-118">**pickselect**</span></span><br/>       | <span data-ttu-id="02569-119">[**glRenderMode**](glrendermode.md) ( \_ sélection GL)</span><span class="sxs-lookup"><span data-stu-id="02569-119">[**glRenderMode**](glrendermode.md) ( GL\_SELECT )</span></span>                                       | <span data-ttu-id="02569-120">Bascule en mode sélection ou choix.</span><span class="sxs-lookup"><span data-stu-id="02569-120">Switches to selection or picking mode.</span></span> |
| <span data-ttu-id="02569-121">**endpickendselect**</span><span class="sxs-lookup"><span data-stu-id="02569-121">**endpickendselect**</span></span><br/> | <span data-ttu-id="02569-122">[**glRenderMode**](glrendermode.md) ( \_ rendu GL)</span><span class="sxs-lookup"><span data-stu-id="02569-122">[**glRenderMode**](glrendermode.md) ( GL\_RENDER )</span></span>                                       | <span data-ttu-id="02569-123">Bascule en mode de rendu.</span><span class="sxs-lookup"><span data-stu-id="02569-123">Switches to rendering mode.</span></span>            |
| <span data-ttu-id="02569-124">**picksize**</span><span class="sxs-lookup"><span data-stu-id="02569-124">**picksize**</span></span>                    | <span data-ttu-id="02569-125">[**gluPickMatrix**](glupickmatrix.md)[**glSelectBuffer**](glselectbuffer.md)</span><span class="sxs-lookup"><span data-stu-id="02569-125">[**gluPickMatrix**](glupickmatrix.md)[**glSelectBuffer**](glselectbuffer.md)</span></span><br/> | <span data-ttu-id="02569-126">Définit le tableau de retour.</span><span class="sxs-lookup"><span data-stu-id="02569-126">Sets the return array.</span></span>                 |
| <span data-ttu-id="02569-127">**initnames**</span><span class="sxs-lookup"><span data-stu-id="02569-127">**initnames**</span></span>                   | [<span data-ttu-id="02569-128">**glInitNames**</span><span class="sxs-lookup"><span data-stu-id="02569-128">**glInitNames**</span></span>](glinitnames.md)                                                        |                                        |
| <span data-ttu-id="02569-129">**pushnamepopname**</span><span class="sxs-lookup"><span data-stu-id="02569-129">**pushnamepopname**</span></span><br/>  | <span data-ttu-id="02569-130">[**glPushName**](glpushname.md)[**glPopName**](glpopname.md)</span><span class="sxs-lookup"><span data-stu-id="02569-130">[**glPushName**](glpushname.md)[**glPopName**](glpopname.md)</span></span><br/>                 |                                        |
| <span data-ttu-id="02569-131">**loadname**</span><span class="sxs-lookup"><span data-stu-id="02569-131">**loadname**</span></span>                    | [<span data-ttu-id="02569-132">**glLoadName**</span><span class="sxs-lookup"><span data-stu-id="02569-132">**glLoadName**</span></span>](glloadname.md)                                                          |                                        |



 

<span data-ttu-id="02569-133">Pour plus d’informations sur le prélèvement, consultez [**gluPickMatrix**](glupickmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="02569-133">For more information on picking, see [**gluPickMatrix**](glupickmatrix.md).</span></span>

 

 





