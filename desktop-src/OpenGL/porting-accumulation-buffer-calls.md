---
title: Portage des appels de tampon d’accumulation
description: Vous devez allouer votre mémoire tampon d’accumulation en demandant le format de pixel approprié avec la fonction OpenGL auxInitDisplayMode ou ChoosePixelFormat.
ms.assetid: 523728ce-4aae-4247-a3dc-23864231cad1
keywords:
- Portage des tampons du GL d’IRIS, accumulation
- Portage à partir de IRIS GL, accumulation de mémoires tampons
- portage vers OpenGL depuis IRIS GL, accumulation de mémoires tampons
- Portage OpenGL depuis IRIS GL, accumulation de mémoires tampons
- mémoires tampons d’accumulation OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91ca91cb3ba35535ba2470297070dffc932a1c33
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104197426"
---
# <a name="porting-accumulation-buffer-calls"></a><span data-ttu-id="0b6e0-108">Portage des appels de tampon d’accumulation</span><span class="sxs-lookup"><span data-stu-id="0b6e0-108">Porting Accumulation Buffer Calls</span></span>

<span data-ttu-id="0b6e0-109">Vous devez allouer votre mémoire tampon d’accumulation en demandant le format de pixel approprié avec la fonction OpenGL **auxInitDisplayMode** ou [**ChoosePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat) .</span><span class="sxs-lookup"><span data-stu-id="0b6e0-109">You must allocate your accumulation buffer by requesting the appropriate pixel format with the OpenGL **auxInitDisplayMode** or [**ChoosePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat) function.</span></span> <span data-ttu-id="0b6e0-110">Le tableau suivant répertorie les fonctions d’IRIS dans le GL qui affectent la mémoire tampon d’accumulation et leurs fonctions OpenGL équivalentes.</span><span class="sxs-lookup"><span data-stu-id="0b6e0-110">The following table lists IRIS GL functions that affect the accumulation buffer and their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="0b6e0-111">Fonction IRIS GL</span><span class="sxs-lookup"><span data-stu-id="0b6e0-111">IRIS GL function</span></span>       | <span data-ttu-id="0b6e0-112">Fonction OpenGL</span><span class="sxs-lookup"><span data-stu-id="0b6e0-112">OpenGL function</span></span>                                       | <span data-ttu-id="0b6e0-113">Signification</span><span class="sxs-lookup"><span data-stu-id="0b6e0-113">Meaning</span></span>                                                                       |
|------------------------|-------------------------------------------------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="0b6e0-114">**acsize**</span><span class="sxs-lookup"><span data-stu-id="0b6e0-114">**acsize**</span></span>             | <span data-ttu-id="0b6e0-115">**auxInitDisplayMode** ou **ChoosePixelFormat**</span><span class="sxs-lookup"><span data-stu-id="0b6e0-115">**auxInitDisplayMode** or **ChoosePixelFormat**</span></span>       | <span data-ttu-id="0b6e0-116">Spécifie le nombre de bitplanes par composant de couleur dans la mémoire tampon d’accumulation.</span><span class="sxs-lookup"><span data-stu-id="0b6e0-116">Specifies number of bitplanes per color component in the accumulation buffer.</span></span> |
| <span data-ttu-id="0b6e0-117">**acbuf**</span><span class="sxs-lookup"><span data-stu-id="0b6e0-117">**acbuf**</span></span>              | [<span data-ttu-id="0b6e0-118">**glAccum**</span><span class="sxs-lookup"><span data-stu-id="0b6e0-118">**glAccum**</span></span>](glaccum.md)                            | <span data-ttu-id="0b6e0-119">Opère sur la mémoire tampon d’accumulation.</span><span class="sxs-lookup"><span data-stu-id="0b6e0-119">Operates on the accumulation buffer.</span></span>                                          |
|                        | [<span data-ttu-id="0b6e0-120">**glClearAccum**</span><span class="sxs-lookup"><span data-stu-id="0b6e0-120">**glClearAccum**</span></span>](glclearaccum.md)                  | <span data-ttu-id="0b6e0-121">Définit des valeurs claires pour la mémoire tampon d’accumulation.</span><span class="sxs-lookup"><span data-stu-id="0b6e0-121">Sets clear values for accumulation buffer.</span></span>                                    |
| <span data-ttu-id="0b6e0-122">**acbuf**(AC \_ Clear)</span><span class="sxs-lookup"><span data-stu-id="0b6e0-122">**acbuf**( AC\_CLEAR )</span></span> | <span data-ttu-id="0b6e0-123">[**glClear**](glclear.md) ( \_ bit de tampon amort GL \_ \_ )</span><span class="sxs-lookup"><span data-stu-id="0b6e0-123">[**glClear**](glclear.md) ( GL\_ACCUM\_BUFFER\_BIT )</span></span> | <span data-ttu-id="0b6e0-124">Efface la mémoire tampon d’accumulation.</span><span class="sxs-lookup"><span data-stu-id="0b6e0-124">Clears the accumulation buffer.</span></span>                                               |



 

<span data-ttu-id="0b6e0-125">Le tableau suivant répertorie les paramètres **acbuf** de l’iris du GL ainsi que les paramètres [**glAccum**](glaccum.md) OpenGL équivalents.</span><span class="sxs-lookup"><span data-stu-id="0b6e0-125">The following table lists the IRIS GL **acbuf** parameters along with the equivalent OpenGL [**glAccum**](glaccum.md) parameters.</span></span>



| <span data-ttu-id="0b6e0-126">Paramètre IRIS GL</span><span class="sxs-lookup"><span data-stu-id="0b6e0-126">IRIS GL parameter</span></span>     | <span data-ttu-id="0b6e0-127">Paramètre OpenGL</span><span class="sxs-lookup"><span data-stu-id="0b6e0-127">OpenGL parameter</span></span> |
|-----------------------|------------------|
| <span data-ttu-id="0b6e0-128">\_accumulation AC</span><span class="sxs-lookup"><span data-stu-id="0b6e0-128">AC\_ACCUMULATE</span></span>        | <span data-ttu-id="0b6e0-129">\_total amort</span><span class="sxs-lookup"><span data-stu-id="0b6e0-129">GL\_ACCUM</span></span>        |
| <span data-ttu-id="0b6e0-130">\_accumulation d’effacement AC \_</span><span class="sxs-lookup"><span data-stu-id="0b6e0-130">AC\_CLEAR\_ACCUMULATE</span></span> | <span data-ttu-id="0b6e0-131">charge du GL \_</span><span class="sxs-lookup"><span data-stu-id="0b6e0-131">GL\_LOAD</span></span>         |
| <span data-ttu-id="0b6e0-132">\_retour AC</span><span class="sxs-lookup"><span data-stu-id="0b6e0-132">AC\_RETURN</span></span>            | <span data-ttu-id="0b6e0-133">\_retour GL</span><span class="sxs-lookup"><span data-stu-id="0b6e0-133">GL\_RETURN</span></span>       |
| <span data-ttu-id="0b6e0-134">AC \_ mult</span><span class="sxs-lookup"><span data-stu-id="0b6e0-134">AC\_MULT</span></span>              | <span data-ttu-id="0b6e0-135">GL \_ mult</span><span class="sxs-lookup"><span data-stu-id="0b6e0-135">GL\_MULT</span></span>         |
| <span data-ttu-id="0b6e0-136">\_Ajout AC</span><span class="sxs-lookup"><span data-stu-id="0b6e0-136">AC\_ADD</span></span>               | <span data-ttu-id="0b6e0-137">ajout au GL \_</span><span class="sxs-lookup"><span data-stu-id="0b6e0-137">GL\_ADD</span></span>          |



 

 

 




