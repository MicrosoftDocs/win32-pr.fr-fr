---
title: Portage des listes d’affichage
description: L’implémentation OpenGL des listes d’affichage est semblable à celle de l’application IRIS GL, avec deux exceptions dans OpenGL. vous ne pouvez pas modifier les listes d’affichage une fois que vous les avez créées et vous ne pouvez pas appeler de fonctions à partir des listes d’affichage.
ms.assetid: 617e19ff-6a55-4f7c-b229-075cdee8f1cf
keywords:
- Le portage du GL IRIS, afficher les listes
- Portage à partir de IRIS GL, afficher les listes
- portage vers OpenGL à partir de IRIS GL, afficher les listes
- Portage OpenGL depuis IRIS GL, afficher les listes
- afficher les listes, Portage à partir de IRIS GL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 461000e6d785f0d03bbbc8f738eba60768bc5d74
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309450"
---
# <a name="porting-display-lists"></a><span data-ttu-id="43bf3-108">Portage des listes d’affichage</span><span class="sxs-lookup"><span data-stu-id="43bf3-108">Porting Display Lists</span></span>

<span data-ttu-id="43bf3-109">L’implémentation OpenGL des listes d’affichage est semblable à l’implémentation IRIS GL, à deux exceptions près : dans OpenGL, vous ne pouvez pas modifier les listes d’affichage une fois que vous les avez créées et vous ne pouvez pas appeler de fonctions à partir des listes d’affichage.</span><span class="sxs-lookup"><span data-stu-id="43bf3-109">The OpenGL implementation of display lists is similar to the IRIS GL implementation, with two exceptions: in OpenGL you can't edit display lists once you've created them and you can't call functions from within display lists.</span></span>

<span data-ttu-id="43bf3-110">Étant donné que vous ne pouvez pas modifier ou appeler des fonctions dans des listes d’affichage, ces fonctions IRIS GL n’ont pas d’équivalent dans OpenGL :</span><span class="sxs-lookup"><span data-stu-id="43bf3-110">Because you can't edit or call functions from within display lists, these IRIS GL functions have no equivalent in OpenGL:</span></span>

-   <span data-ttu-id="43bf3-111">**editobj**</span><span class="sxs-lookup"><span data-stu-id="43bf3-111">**editobj**</span></span>
-   <span data-ttu-id="43bf3-112">**objdelete**, **objinsert** et **objreplace**</span><span class="sxs-lookup"><span data-stu-id="43bf3-112">**objdelete**, **objinsert**, and **objreplace**</span></span>
-   <span data-ttu-id="43bf3-113">**maketag**, **gentag**, **ISTAG** et **deltaG**</span><span class="sxs-lookup"><span data-stu-id="43bf3-113">**maketag**, **gentag**, **istag**, and **deltag**</span></span>
-   <span data-ttu-id="43bf3-114">**callfunc**</span><span class="sxs-lookup"><span data-stu-id="43bf3-114">**callfunc**</span></span>

<span data-ttu-id="43bf3-115">Dans IRIS GL, vous utilisez les fonctions **makeobj** et **closeobj** pour créer des listes d’affichage.</span><span class="sxs-lookup"><span data-stu-id="43bf3-115">In IRIS GL, you use the **makeobj** and **closeobj** functions to create display lists.</span></span> <span data-ttu-id="43bf3-116">Dans OpenGL, vous utilisez [**glNewList**](glnewlist.md) et [**glEndList**](glendlist.md).</span><span class="sxs-lookup"><span data-stu-id="43bf3-116">In OpenGL, you use [**glNewList**](glnewlist.md) and [**glEndList**](glendlist.md).</span></span>

<span data-ttu-id="43bf3-117">Le tableau suivant répertorie les fonctions IRIS GL Display List avec leurs fonctions OpenGL équivalentes.</span><span class="sxs-lookup"><span data-stu-id="43bf3-117">The following table lists the IRIS GL display list functions with their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="43bf3-118">Fonction IRIS GL</span><span class="sxs-lookup"><span data-stu-id="43bf3-118">IRIS GL function</span></span> | <span data-ttu-id="43bf3-119">Fonction OpenGL</span><span class="sxs-lookup"><span data-stu-id="43bf3-119">OpenGL function</span></span>                                                      | <span data-ttu-id="43bf3-120">Signification</span><span class="sxs-lookup"><span data-stu-id="43bf3-120">Meaning</span></span>                                                       |
|------------------|----------------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="43bf3-121">**makeobj**</span><span class="sxs-lookup"><span data-stu-id="43bf3-121">**makeobj**</span></span>      | <span data-ttu-id="43bf3-122">**glNewList**</span><span class="sxs-lookup"><span data-stu-id="43bf3-122">**glNewList**</span></span>                                                        | <span data-ttu-id="43bf3-123">Crée une nouvelle liste d’affichage.</span><span class="sxs-lookup"><span data-stu-id="43bf3-123">Creates a new display list.</span></span>                                   |
| <span data-ttu-id="43bf3-124">**closeobj**</span><span class="sxs-lookup"><span data-stu-id="43bf3-124">**closeobj**</span></span>     | <span data-ttu-id="43bf3-125">**glEndList**</span><span class="sxs-lookup"><span data-stu-id="43bf3-125">**glEndList**</span></span>                                                        | <span data-ttu-id="43bf3-126">Signale la fin de la liste d’affichage.</span><span class="sxs-lookup"><span data-stu-id="43bf3-126">Signals end of display list.</span></span>                                  |
| <span data-ttu-id="43bf3-127">**callobj**</span><span class="sxs-lookup"><span data-stu-id="43bf3-127">**callobj**</span></span>      | <span data-ttu-id="43bf3-128">[**glCallList**](glcalllist.md), [ **glCallLists**](glcalllists.md)</span><span class="sxs-lookup"><span data-stu-id="43bf3-128">[**glCallList**](glcalllist.md), [**glCallLists**](glcalllists.md)</span></span> | <span data-ttu-id="43bf3-129">Exécute une liste ou des listes d’affichage.</span><span class="sxs-lookup"><span data-stu-id="43bf3-129">Executes display list or lists.</span></span>                               |
| <span data-ttu-id="43bf3-130">**isobj**</span><span class="sxs-lookup"><span data-stu-id="43bf3-130">**isobj**</span></span>        | [<span data-ttu-id="43bf3-131">**glIsList**</span><span class="sxs-lookup"><span data-stu-id="43bf3-131">**glIsList**</span></span>](glislist.md)                                         | <span data-ttu-id="43bf3-132">Teste l’existence de la liste d’affichage.</span><span class="sxs-lookup"><span data-stu-id="43bf3-132">Tests for display list existence.</span></span>                             |
| <span data-ttu-id="43bf3-133">**delobj**</span><span class="sxs-lookup"><span data-stu-id="43bf3-133">**delobj**</span></span>       | [<span data-ttu-id="43bf3-134">**glDeleteLists**</span><span class="sxs-lookup"><span data-stu-id="43bf3-134">**glDeleteLists**</span></span>](gldeletelists.md)                               | <span data-ttu-id="43bf3-135">Supprime un groupe contigu de listes d’affichage.</span><span class="sxs-lookup"><span data-stu-id="43bf3-135">Deletes contiguous group of display lists.</span></span>                    |
| <span data-ttu-id="43bf3-136">**genobj**</span><span class="sxs-lookup"><span data-stu-id="43bf3-136">**genobj**</span></span>       | [<span data-ttu-id="43bf3-137">**glGenLists**</span><span class="sxs-lookup"><span data-stu-id="43bf3-137">**glGenLists**</span></span>](glgenlists.md)                                     | <span data-ttu-id="43bf3-138">Génère le nombre donné de listes d’affichage vides contiguës.</span><span class="sxs-lookup"><span data-stu-id="43bf3-138">Generates the given number of contiguous empty display lists.</span></span> |



 

<span data-ttu-id="43bf3-139">Cette rubrique contient des informations sur les éléments suivants.</span><span class="sxs-lookup"><span data-stu-id="43bf3-139">This topic includes information on the following.</span></span>

-   [<span data-ttu-id="43bf3-140">Portage de la fonction BBOX2</span><span class="sxs-lookup"><span data-stu-id="43bf3-140">Porting the bbox2 Function</span></span>](porting-the-bbox2-function.md)
-   [<span data-ttu-id="43bf3-141">Portage des listes d’affichage modifiées</span><span class="sxs-lookup"><span data-stu-id="43bf3-141">Porting Edited Display Lists</span></span>](porting-edited-display-lists.md)
-   [<span data-ttu-id="43bf3-142">Exemple de port d’une liste d’affichage</span><span class="sxs-lookup"><span data-stu-id="43bf3-142">A Sample Port of a Display List</span></span>](a-sample-port-of-a-display-list.md)

 

 




