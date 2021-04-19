---
title: Fonctions appelées par le système
description: Fonctions appelées par le système
ms.assetid: 006ac524-d456-44e9-957b-42a85dc92519
keywords:
- audio multimédia, fonctions ACM
- audio, fonctions ACM
- le gestionnaire de compression audio (ACM), fonctions
- ACM (gestionnaire de compression audio), fonctions
- Fonctions ACM
- fonctions de rappel
- Audio Compression Manager (ACM), fonctions de rappel
- ACM (gestionnaire de compression audio), fonctions de rappel
- procédures de Hook
- procédures relatives aux pilotes
- Audio Compression Manager (ACM), procédures de raccordement
- ACM (gestionnaire de compression audio), procédures de raccordement
- Audio Compression Manager (ACM), procédures relatives aux pilotes
- ACM (gestionnaire de compression audio), procédures relatives aux pilotes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1324ea168892d54f21754658607476c35075910
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "106510675"
---
# <a name="functions-called-by-the-system"></a><span data-ttu-id="8956e-117">Fonctions appelées par le système</span><span class="sxs-lookup"><span data-stu-id="8956e-117">Functions Called by the System</span></span>

<span data-ttu-id="8956e-118">Le système appelle trois types différents de fonctions définies par l’application.</span><span class="sxs-lookup"><span data-stu-id="8956e-118">The system calls three different kinds of application-defined functions.</span></span> <span data-ttu-id="8956e-119">Les fonctions de rappel sont des fonctions de votre application que le système appelle en réponse à une demande faite par une application.</span><span class="sxs-lookup"><span data-stu-id="8956e-119">Callback functions are functions in your application that the system calls in response to a request made by an application.</span></span> <span data-ttu-id="8956e-120">Les procédures de raccordement aident une application à gérer la personnalisation des boîtes de dialogue.</span><span class="sxs-lookup"><span data-stu-id="8956e-120">Hook procedures help an application handle the customization of dialog boxes.</span></span> <span data-ttu-id="8956e-121">Une procédure de pilote est l’implémentation d’une application de son propre codec, convertisseur ou filtre.</span><span class="sxs-lookup"><span data-stu-id="8956e-121">A driver procedure is an application's implementation of its own codec, converter, or filter.</span></span>

<span data-ttu-id="8956e-122">Les fonctions de rappel portent les noms suivants :</span><span class="sxs-lookup"><span data-stu-id="8956e-122">The callback functions have the following names:</span></span>

-   [<span data-ttu-id="8956e-123">**acmDriverEnumCallback**</span><span class="sxs-lookup"><span data-stu-id="8956e-123">**acmDriverEnumCallback**</span></span>](/windows/win32/api/msacm/nc-msacm-acmdriverenumcb)
-   [<span data-ttu-id="8956e-124">**acmFilterEnumCallback**</span><span class="sxs-lookup"><span data-stu-id="8956e-124">**acmFilterEnumCallback**</span></span>](/windows/desktop/api/Msacm/nc-msacm-acmfilterenumcb)
-   [<span data-ttu-id="8956e-125">**acmFilterTagEnumCallback**</span><span class="sxs-lookup"><span data-stu-id="8956e-125">**acmFilterTagEnumCallback**</span></span>](/windows/desktop/api/Msacm/nc-msacm-acmfiltertagenumcb)
-   [<span data-ttu-id="8956e-126">**acmFormatEnumCallback**</span><span class="sxs-lookup"><span data-stu-id="8956e-126">**acmFormatEnumCallback**</span></span>](/windows/desktop/api/Msacm/nc-msacm-acmformatenumcb)
-   [<span data-ttu-id="8956e-127">**acmFormatTagEnumCallback**</span><span class="sxs-lookup"><span data-stu-id="8956e-127">**acmFormatTagEnumCallback**</span></span>](/windows/desktop/api/Msacm/nc-msacm-acmformattagenumcb)
-   <span data-ttu-id="8956e-128">[**acmStreamConvertCallback**](/previous-versions//dd742925(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="8956e-128">[**acmStreamConvertCallback**](/previous-versions//dd742925(v=vs.85))</span></span>

<span data-ttu-id="8956e-129">La plupart des fonctions d’énumération dans l’ACM utilisent des fonctions de rappel.</span><span class="sxs-lookup"><span data-stu-id="8956e-129">Most of the enumeration functions in the ACM use callback functions.</span></span> <span data-ttu-id="8956e-130">Par exemple, lorsque vous appelez une fonction d’énumération, l’ACM énumère les éléments en appelant de façon répétée l’application via la fonction de rappel.</span><span class="sxs-lookup"><span data-stu-id="8956e-130">For example, when you call an enumeration function, the ACM enumerates the items by repeatedly calling the application through the callback function.</span></span>

<span data-ttu-id="8956e-131">Certaines fonctions ne peuvent pas être appelées à partir de ces fonctions de rappel.</span><span class="sxs-lookup"><span data-stu-id="8956e-131">Some functions cannot be called from within these callback functions.</span></span> <span data-ttu-id="8956e-132">Les fonctions qui ne peuvent pas être appelées manipulent des structures ACM internes qui sont utilisées par les fonctions d’énumération.</span><span class="sxs-lookup"><span data-stu-id="8956e-132">Functions that cannot be called manipulate internal ACM structures that are used by the enumeration functions.</span></span> <span data-ttu-id="8956e-133">Les fonctions suivantes ne doivent pas être appelées à partir d’une fonction de rappel :</span><span class="sxs-lookup"><span data-stu-id="8956e-133">The following functions should not be called from within a callback function:</span></span>

-   [<span data-ttu-id="8956e-134">**acmDriverAdd**</span><span class="sxs-lookup"><span data-stu-id="8956e-134">**acmDriverAdd**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmdriveradd)
-   [<span data-ttu-id="8956e-135">**acmDriverPriority**</span><span class="sxs-lookup"><span data-stu-id="8956e-135">**acmDriverPriority**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmdriverpriority)
-   [<span data-ttu-id="8956e-136">**acmDriverRemove**</span><span class="sxs-lookup"><span data-stu-id="8956e-136">**acmDriverRemove**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmdriverremove)

<span data-ttu-id="8956e-137">Le système appelle les fonctions suivantes pour aider une application à gérer la personnalisation des boîtes de dialogue :</span><span class="sxs-lookup"><span data-stu-id="8956e-137">The system calls the following functions to help an application handle the customization of dialog boxes:</span></span>

-   [<span data-ttu-id="8956e-138">**acmFilterChooseHookProc**</span><span class="sxs-lookup"><span data-stu-id="8956e-138">**acmFilterChooseHookProc**</span></span>](/windows/desktop/api/Msacm/nc-msacm-acmfilterchoosehookproc)
-   [<span data-ttu-id="8956e-139">**acmFormatChooseHookProc**</span><span class="sxs-lookup"><span data-stu-id="8956e-139">**acmFormatChooseHookProc**</span></span>](/windows/desktop/api/Msacm/nc-msacm-acmformatchoosehookproc)

<span data-ttu-id="8956e-140">La fonction suivante est spécifiée en tant que prototype qui permet à une application d’utiliser un codec, un convertisseur ou un filtre personnalisé.</span><span class="sxs-lookup"><span data-stu-id="8956e-140">The following function is specified as a prototype that allows an application to use a customized codec, converter, or filter.</span></span> <span data-ttu-id="8956e-141">Une fonction conforme à ce prototype peut être passée comme argument à la fonction [**acmDriverAdd**](/windows/desktop/api/Msacm/nf-msacm-acmdriveradd) .</span><span class="sxs-lookup"><span data-stu-id="8956e-141">A function conforming to this prototype may be passed as an argument to the [**acmDriverAdd**](/windows/desktop/api/Msacm/nf-msacm-acmdriveradd) function.</span></span>

-   [<span data-ttu-id="8956e-142">**acmDriverProc**</span><span class="sxs-lookup"><span data-stu-id="8956e-142">**acmDriverProc**</span></span>](/windows/desktop/api/Msacm/nc-msacm-acmdriverproc)

 

 