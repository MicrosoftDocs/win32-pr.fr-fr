---
title: Portage des appels au plan du gabarit
description: Dans OpenGL, vous allouez des plans de stencil en demandant le format de pixel approprié avec le auxInitDisplayMode ou ChoosePixelFormat OpenGL.
ms.assetid: faea8a10-860a-4495-80fb-e83303e397df
keywords:
- Portage de l’IRIS dans le GL, plans de gabarit
- Portage à partir de IRIS GL, plans de stencil
- portage vers OpenGL à partir de IRIS GL, plans stencil
- Portage OpenGL à partir de IRIS GL, plans stencil
- plans de gabarit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 829ea033a75cb1153a475496c3f33398640dbc76
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310541"
---
# <a name="porting-stencil-plane-calls"></a><span data-ttu-id="09d6f-108">Portage des appels au plan du gabarit</span><span class="sxs-lookup"><span data-stu-id="09d6f-108">Porting Stencil Plane Calls</span></span>

<span data-ttu-id="09d6f-109">Dans OpenGL, vous allouez des plans de stencil en demandant le format de pixel approprié avec le **auxInitDisplayMode** ou [**ChoosePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat)OpenGL.</span><span class="sxs-lookup"><span data-stu-id="09d6f-109">In OpenGL, you allocate stencil planes by requesting the appropriate pixel format with the OpenGL **auxInitDisplayMode** or [**ChoosePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat).</span></span> <span data-ttu-id="09d6f-110">Mission.</span><span class="sxs-lookup"><span data-stu-id="09d6f-110">functions.</span></span> <span data-ttu-id="09d6f-111">Le tableau suivant répertorie les fonctions d’IRIS dans le GL qui affectent les plans de stencil et leurs fonctions OpenGL équivalentes.</span><span class="sxs-lookup"><span data-stu-id="09d6f-111">The following table lists IRIS GL functions that affect the stencil planes and their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="09d6f-112">Fonction IRIS GL</span><span class="sxs-lookup"><span data-stu-id="09d6f-112">IRIS GL function</span></span>             | <span data-ttu-id="09d6f-113">Fonction OpenGL</span><span class="sxs-lookup"><span data-stu-id="09d6f-113">OpenGL function</span></span>                                         | <span data-ttu-id="09d6f-114">Signification</span><span class="sxs-lookup"><span data-stu-id="09d6f-114">Meaning</span></span>                                                |
|------------------------------|---------------------------------------------------------|--------------------------------------------------------|
| <span data-ttu-id="09d6f-115">**stensize**</span><span class="sxs-lookup"><span data-stu-id="09d6f-115">**stensize**</span></span>                 | <span data-ttu-id="09d6f-116">**ChoosePixelFormat**</span><span class="sxs-lookup"><span data-stu-id="09d6f-116">**ChoosePixelFormat**</span></span>                                   |                                                        |
| <span data-ttu-id="09d6f-117">**stencil**( **true**,...)</span><span class="sxs-lookup"><span data-stu-id="09d6f-117">**stencil**( **TRUE**, ... )</span></span> | <span data-ttu-id="09d6f-118">[**glEnable**](glenable.md) (test de stencil du GL \_ \_ )</span><span class="sxs-lookup"><span data-stu-id="09d6f-118">[**glEnable**](glenable.md) ( GL\_STENCIL\_TEST )</span></span>      | <span data-ttu-id="09d6f-119">Active les tests de stencil.</span><span class="sxs-lookup"><span data-stu-id="09d6f-119">Enables stencil tests.</span></span>                                 |
| <span data-ttu-id="09d6f-120">**écrans**</span><span class="sxs-lookup"><span data-stu-id="09d6f-120">**stencil**</span></span>                  | [<span data-ttu-id="09d6f-121">**glStencilOp**</span><span class="sxs-lookup"><span data-stu-id="09d6f-121">**glStencilOp**</span></span>](glstencilop.md)                      | <span data-ttu-id="09d6f-122">Définit des actions de test de stencil.</span><span class="sxs-lookup"><span data-stu-id="09d6f-122">Sets stencil test actions.</span></span>                             |
| <span data-ttu-id="09d6f-123">**gabarit**(... Func,...)</span><span class="sxs-lookup"><span data-stu-id="09d6f-123">**stencil**(... func, ... )</span></span>  | [<span data-ttu-id="09d6f-124">**glStencilFunc**</span><span class="sxs-lookup"><span data-stu-id="09d6f-124">**glStencilFunc**</span></span>](glstencilfunc.md)                  | <span data-ttu-id="09d6f-125">Définit la fonction et la valeur de référence pour le test des stencils.</span><span class="sxs-lookup"><span data-stu-id="09d6f-125">Sets function and reference value for stencil testing.</span></span> |
| <span data-ttu-id="09d6f-126">**swritemask**</span><span class="sxs-lookup"><span data-stu-id="09d6f-126">**swritemask**</span></span>               | [<span data-ttu-id="09d6f-127">**glStencilMask**</span><span class="sxs-lookup"><span data-stu-id="09d6f-127">**glStencilMask**</span></span>](glstencilmask.md)                  | <span data-ttu-id="09d6f-128">Spécifie les bits de stencil qui peuvent être écrits.</span><span class="sxs-lookup"><span data-stu-id="09d6f-128">Specifies which stencil bits can be written.</span></span>           |
|                              | [<span data-ttu-id="09d6f-129">**glClearStencil**</span><span class="sxs-lookup"><span data-stu-id="09d6f-129">**glClearStencil**</span></span>](glclearstencil.md)                | <span data-ttu-id="09d6f-130">Spécifie la valeur Clear pour la mémoire tampon du stencil.</span><span class="sxs-lookup"><span data-stu-id="09d6f-130">Specifies the clear value for the stencil buffer.</span></span>      |
| <span data-ttu-id="09d6f-131">**sclear**</span><span class="sxs-lookup"><span data-stu-id="09d6f-131">**sclear**</span></span>                   | <span data-ttu-id="09d6f-132">[**glClear**](glclear.md) (bits de tampon de stencil du GL \_ \_ \_ )</span><span class="sxs-lookup"><span data-stu-id="09d6f-132">[**glClear**](glclear.md) ( GL\_STENCIL\_BUFFER\_BIT )</span></span> |                                                        |



 

<span data-ttu-id="09d6f-133">Les fonctions de comparaison de stencils et les opérations de réussite/échec de stencil sont presque équivalentes dans OpenGL et IRIS GL.</span><span class="sxs-lookup"><span data-stu-id="09d6f-133">Stencil-comparison functions and stencil pass/fail operations are nearly equivalent in OpenGL and IRIS GL.</span></span> <span data-ttu-id="09d6f-134">Les indicateurs de fonction du gabarit IRIS GL-sont précédés de DF ; les indicateurs OpenGL avec GL.</span><span class="sxs-lookup"><span data-stu-id="09d6f-134">The IRIS GL stencil-function flags are prefaced with SF; the OpenGL flags with GL.</span></span> <span data-ttu-id="09d6f-135">Les indicateurs d’opération de réussite/échec de l’IRIS GL sont précédés de ST ; les indicateurs OpenGL avec GL.</span><span class="sxs-lookup"><span data-stu-id="09d6f-135">IRIS GL pass/fail operation flags are prefaced with ST; the OpenGL flags with GL.</span></span>

 

 




