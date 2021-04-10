---
title: Instructions générales sur le portage
description: Le portage d’applications 32 bits vers Microsoft Windows 64 bits sera plus facile qu’avec le portage d’applications 16 bits vers Windows 32 bits. Toutefois, le déplacement sera plus fluide avec une planification minutieuse. Voici quelques recommandations générales.
ms.assetid: 28c1656e-93a2-441b-8946-18017e0b2b29
keywords:
- Portage d’applications 32 bits 64 vers la programmation Windows 64 bits Windows bits
- Guide de programmation Windows 64 bits-programmation Windows 64 bits, indications sur le portage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d31734edd8b85bd61b8b84cb2c66d835f0085ac1
ms.sourcegitcommit: 35bb565804eaeed7ac5503595753f59d120076dd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/09/2021
ms.locfileid: "104211174"
---
# <a name="general-porting-guidelines"></a><span data-ttu-id="9e0bd-107">Instructions générales sur le portage</span><span class="sxs-lookup"><span data-stu-id="9e0bd-107">General Porting Guidelines</span></span>

<span data-ttu-id="9e0bd-108">Le portage d’applications 32 bits vers Microsoft Windows 64 bits sera plus facile qu’avec le portage d’applications 16 bits vers Windows 32 bits.</span><span class="sxs-lookup"><span data-stu-id="9e0bd-108">Porting 32-bit applications to 64-bit Microsoft Windows will be easier than it was porting 16-bit applications to 32-bit Windows.</span></span> <span data-ttu-id="9e0bd-109">Toutefois, le déplacement sera plus fluide avec une planification minutieuse.</span><span class="sxs-lookup"><span data-stu-id="9e0bd-109">However, the move will go more smoothly with some careful planning.</span></span> <span data-ttu-id="9e0bd-110">Voici quelques recommandations générales.</span><span class="sxs-lookup"><span data-stu-id="9e0bd-110">The following are some general guidelines.</span></span>

## <a name="planning"></a><span data-ttu-id="9e0bd-111">Planification</span><span class="sxs-lookup"><span data-stu-id="9e0bd-111">Planning</span></span>

-   <span data-ttu-id="9e0bd-112">Déterminez l’ampleur de l’effort requis pour le port.</span><span class="sxs-lookup"><span data-stu-id="9e0bd-112">Determine the magnitude of the effort required for the port.</span></span> <span data-ttu-id="9e0bd-113">Évaluer la quantité de travail impliquée par l’identification des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="9e0bd-113">Gauge how much work is involved by identifying the following items:</span></span>
    -   <span data-ttu-id="9e0bd-114">Problème 32-code bit.</span><span class="sxs-lookup"><span data-stu-id="9e0bd-114">Problem 32-bit code.</span></span> <span data-ttu-id="9e0bd-115">Compilez votre code 32 bits avec le compilateur 64 bits et examinez l’étendue des erreurs et des avertissements.</span><span class="sxs-lookup"><span data-stu-id="9e0bd-115">Compile your 32-bit code with the 64-bit compiler and examine the extent of the errors and warnings.</span></span>
    -   <span data-ttu-id="9e0bd-116">Composants partagés ou dépendances.</span><span class="sxs-lookup"><span data-stu-id="9e0bd-116">Shared components or dependencies.</span></span> <span data-ttu-id="9e0bd-117">Identifiez les composants de votre application qui proviennent d’autres équipes et si ces équipes envisagent de développer des versions 64 bits de leur code.</span><span class="sxs-lookup"><span data-stu-id="9e0bd-117">Determine which components in your application originate from other teams and whether those teams plan to develop 64-bit versions of their code.</span></span>
    -   <span data-ttu-id="9e0bd-118">Code d’héritage ou d’assembly.</span><span class="sxs-lookup"><span data-stu-id="9e0bd-118">Legacy or assembly code.</span></span> <span data-ttu-id="9e0bd-119">les applications Windows 16 bits ne s’exécutent pas sur Windows 64 bits et doivent être réécrites.</span><span class="sxs-lookup"><span data-stu-id="9e0bd-119">16-bit Windows-based applications do not run on 64-bit Windows and must be rewritten.</span></span> <span data-ttu-id="9e0bd-120">Bien que le code assembleur x86 s’exécute dans WOW64, vous pouvez réécrire ce code pour tirer parti de la vitesse de l’architecture Intel Itanium.</span><span class="sxs-lookup"><span data-stu-id="9e0bd-120">While x86 assembly code runs in WOW64, you may want to rewrite this code to take advantage of the speed of the Intel Itanium architecture.</span></span>
-   <span data-ttu-id="9e0bd-121">Portage de l’application entière, et pas seulement d’une partie de celle-ci.</span><span class="sxs-lookup"><span data-stu-id="9e0bd-121">Port the entire application, not just portions of it.</span></span>

    <span data-ttu-id="9e0bd-122">Bien qu’il soit possible de porter des parties d’une application ou de limiter le code à 2G avec/LARGEADDRESSAWARE : NO, cette stratégie offre des gains à long terme pour la douleur à long terme.</span><span class="sxs-lookup"><span data-stu-id="9e0bd-122">Although it is possible to port pieces of an application or to limit code to 2G with /LARGEADDRESSAWARE:NO, this strategy trades short-term gain for long-term pain.</span></span>

    > [!Note]  
    > <span data-ttu-id="9e0bd-123">/LARGEADDRESSAWARE : NO est ignoré pour un binaire ARM64.</span><span class="sxs-lookup"><span data-stu-id="9e0bd-123">/LARGEADDRESSAWARE:NO is ignored for an ARM64 binary.</span></span>

     

-   <span data-ttu-id="9e0bd-124">Recherchez des substituts pour les technologies qui ne seront pas portées.</span><span class="sxs-lookup"><span data-stu-id="9e0bd-124">Find substitutes for technologies that will not be ported.</span></span>

    <span data-ttu-id="9e0bd-125">Certaines technologies, y compris DAO (Data Access Object) et le moteur de base de données Red jet, ne seront pas portées vers Windows 64 bits.</span><span class="sxs-lookup"><span data-stu-id="9e0bd-125">Some technologies, including DAO (Data Access Object) and the Jet Red database engine, will not be ported to 64-bit Windows.</span></span>

-   <span data-ttu-id="9e0bd-126">Traitez votre version 64 bits comme une version distincte du produit.</span><span class="sxs-lookup"><span data-stu-id="9e0bd-126">Treat your 64-bit version as a separate product release.</span></span>

    <span data-ttu-id="9e0bd-127">Même si votre produit 64 bits peut partager la même base de code que votre 32 bits, il nécessite des tests supplémentaires et peut avoir d’autres considérations relatives à la version.</span><span class="sxs-lookup"><span data-stu-id="9e0bd-127">Even though your 64-bit product may share the same code base as your 32-bit, it needs additional testing and may have other release considerations.</span></span>

## <a name="development"></a><span data-ttu-id="9e0bd-128">Développement</span><span class="sxs-lookup"><span data-stu-id="9e0bd-128">Development</span></span>

-   <span data-ttu-id="9e0bd-129">Commencez à développer du code conforme maintenant.</span><span class="sxs-lookup"><span data-stu-id="9e0bd-129">Start developing compliant code now.</span></span>

    <span data-ttu-id="9e0bd-130">Les développeurs peuvent commencer à écrire du code conforme en utilisant les derniers fichiers d’en-tête Windows et les nouveaux types de données sans effets néfastes sur le développement de produits 32 bits.</span><span class="sxs-lookup"><span data-stu-id="9e0bd-130">Developers can start writing compliant code by using the latest Windows header files and the new data types with no adverse effects on 32-bit product development.</span></span> <span data-ttu-id="9e0bd-131">Pour plus d’informations, consultez [préparation pour Windows 64 bits](getting-ready-for-64-bit-windows.md).</span><span class="sxs-lookup"><span data-stu-id="9e0bd-131">For more information, see [Getting Ready for 64-bit Windows](getting-ready-for-64-bit-windows.md).</span></span>

-   <span data-ttu-id="9e0bd-132">Assurez-vous que votre code peut être compilé pour les fenêtres 32 et 64 bits.</span><span class="sxs-lookup"><span data-stu-id="9e0bd-132">Ensure that your code can be compiled for both 32- and 64-bit Windows.</span></span>

    <span data-ttu-id="9e0bd-133">Le nouveau modèle de données a été conçu pour permettre la génération d’applications 32 et 64 bits à partir d’une base de code unique avec quelques modifications.</span><span class="sxs-lookup"><span data-stu-id="9e0bd-133">The new data model was designed to allow 32- and 64-bit applications to be built from a single code base with few modifications.</span></span> <span data-ttu-id="9e0bd-134">Les équipes de développement SQL Server et Windows développent des versions 32 et 64 bits de leurs produits à partir de la même base de code.</span><span class="sxs-lookup"><span data-stu-id="9e0bd-134">The SQL Server and Windows development teams are developing 32- and 64-bit versions of their products from the same code base.</span></span>

-   <span data-ttu-id="9e0bd-135">Utilisez les nouvelles fonctionnalités d’optimisation du compilateur pour obtenir de meilleures performances.</span><span class="sxs-lookup"><span data-stu-id="9e0bd-135">Use the compiler's new optimization features for best performance.</span></span>

    <span data-ttu-id="9e0bd-136">L’optimisation du code pour les processeurs Intel Itanium est plus importante que celle de l’architecture x86.</span><span class="sxs-lookup"><span data-stu-id="9e0bd-136">Code optimization for Intel Itanium processors is more important than it was for the x86.</span></span> <span data-ttu-id="9e0bd-137">Le compilateur suppose un grand nombre des fonctions d’optimisation précédemment gérées par le microprocesseur.</span><span class="sxs-lookup"><span data-stu-id="9e0bd-137">The compiler assumes many of the optimization functions previously handled by the microprocessor.</span></span> <span data-ttu-id="9e0bd-138">Vous pouvez optimiser les performances d’une application 64 bits en utilisant deux nouvelles fonctionnalités d’optimisation du compilateur : l’optimisation *guidée par profil* et l’optimisation de l’ensemble du *programme*.</span><span class="sxs-lookup"><span data-stu-id="9e0bd-138">You can maximize the performance of a 64-bit application by using two new optimization features of the compiler: *Profile Guided Optimization* and *Whole Program Optimization*.</span></span> <span data-ttu-id="9e0bd-139">Les deux fonctionnalités entraînent des temps de génération plus longs et nécessitent le développement anticipé de bons scénarios de test.</span><span class="sxs-lookup"><span data-stu-id="9e0bd-139">Both features result in longer build times and require the early development of good test scenarios.</span></span>

    <span data-ttu-id="9e0bd-140">L' *optimisation guidée par profil* implique un processus de compilation en deux étapes.</span><span class="sxs-lookup"><span data-stu-id="9e0bd-140">*Profile Guided Optimization* involves a two-step compile process.</span></span> <span data-ttu-id="9e0bd-141">Au cours de la première compilation, le code est instrumenté pour capturer le comportement d’exécution.</span><span class="sxs-lookup"><span data-stu-id="9e0bd-141">During the first compile, the code is instrumented to capture the execution behavior.</span></span> <span data-ttu-id="9e0bd-142">Ces informations sont utilisées lors de la deuxième compilation pour guider toutes les fonctionnalités d’optimisation.</span><span class="sxs-lookup"><span data-stu-id="9e0bd-142">This information is used during the second compile to guide all optimization features.</span></span>

    <span data-ttu-id="9e0bd-143">L’optimisation de l' *ensemble du programme* analyse le code dans tous les fichiers d’application, et pas seulement dans un seul.</span><span class="sxs-lookup"><span data-stu-id="9e0bd-143">*Whole Program Optimization* analyzes the code in all application files, not just a single one.</span></span> <span data-ttu-id="9e0bd-144">Cette approche augmente les performances de plusieurs façons, y compris une meilleure incorporation, ainsi qu’une analyse des effets secondaires améliorée et des conventions d’appel personnalisées.</span><span class="sxs-lookup"><span data-stu-id="9e0bd-144">This approach increases performance in several ways, including better inlining, as well as improved side-effect analysis and custom calling conventions.</span></span>

## <a name="testing"></a><span data-ttu-id="9e0bd-145">Test</span><span class="sxs-lookup"><span data-stu-id="9e0bd-145">Testing</span></span>

-   <span data-ttu-id="9e0bd-146">Déterminez si vous allez tester le code 64-ou 32 bits s’exécutant dans WOW64.</span><span class="sxs-lookup"><span data-stu-id="9e0bd-146">Determine whether you'll test 64- or 32-bit code running in WOW64.</span></span>

    <span data-ttu-id="9e0bd-147">Certaines applications incluent du code 64 bits natif et du code 32 bits s’exécutant dans WOW64.</span><span class="sxs-lookup"><span data-stu-id="9e0bd-147">Some applications include both native 64-bit code and 32-bit code running in WOW64.</span></span> <span data-ttu-id="9e0bd-148">Examinez cela en détail pendant le développement d’un plan de test et décidez si vos outils de test doivent être de 64 bits, 32 bits ou une combinaison.</span><span class="sxs-lookup"><span data-stu-id="9e0bd-148">Investigate this closely while developing a test plan, and decide whether your test tools should be 64-bit, 32-bit, or a combination.</span></span> <span data-ttu-id="9e0bd-149">Vous aurez souvent besoin de tester les versions 64 et 32 bits de votre application sur Windows 64 bits.</span><span class="sxs-lookup"><span data-stu-id="9e0bd-149">You will often need to test both the 64- and 32-bit versions of your application on 64-bit Windows.</span></span>

-   <span data-ttu-id="9e0bd-150">Testez les composants 32 bits fréquemment utilisés.</span><span class="sxs-lookup"><span data-stu-id="9e0bd-150">Test frequently used 32-bit components.</span></span>

    <span data-ttu-id="9e0bd-151">Tout d’abord, recompilez votre code pour 64 bits et test.</span><span class="sxs-lookup"><span data-stu-id="9e0bd-151">First, recompile your code to 64-bit and test.</span></span> <span data-ttu-id="9e0bd-152">Ensuite, corrigez les problèmes, recompilez-les dans 32 bits, puis testez.</span><span class="sxs-lookup"><span data-stu-id="9e0bd-152">Second, fix problems, recompile in 32-bits, and then test.</span></span> <span data-ttu-id="9e0bd-153">Troisièmement, recompilez en 64 bits et testez.</span><span class="sxs-lookup"><span data-stu-id="9e0bd-153">Third, recompile to 64-bit and test.</span></span>

-   <span data-ttu-id="9e0bd-154">Testez les composants COM et RPC.</span><span class="sxs-lookup"><span data-stu-id="9e0bd-154">Test COM and RPC components.</span></span>

    <span data-ttu-id="9e0bd-155">Assurez-vous que les composants COM et RPC 32 et 64 bits communiquent correctement.</span><span class="sxs-lookup"><span data-stu-id="9e0bd-155">Make sure that both 32- and 64-bit COM and RPC components communicate correctly.</span></span> <span data-ttu-id="9e0bd-156">Vous devrez peut-être également tester les communications avec des composants 16 bits sur un réseau.</span><span class="sxs-lookup"><span data-stu-id="9e0bd-156">You may also have to test communications with 16-bit components over a network.</span></span>

-   <span data-ttu-id="9e0bd-157">Testez votre version 32 bits sur Windows 64 bits.</span><span class="sxs-lookup"><span data-stu-id="9e0bd-157">Test your 32-bit version on 64-bit Windows.</span></span>

    <span data-ttu-id="9e0bd-158">Les clients peuvent continuer à utiliser des applications 32 bits sur Windows 64 bits, où les problèmes de performances et de mémoire ne sont pas des considérations majeures.</span><span class="sxs-lookup"><span data-stu-id="9e0bd-158">Customers can continue to use 32-bit applications on 64-bit Windows where performance and memory issues are not major considerations.</span></span>

-   <span data-ttu-id="9e0bd-159">Testez différentes configurations de mémoire.</span><span class="sxs-lookup"><span data-stu-id="9e0bd-159">Test different memory configurations.</span></span>

    <span data-ttu-id="9e0bd-160">L’ajout de grandes quantités de mémoire sur le serveur expose parfois des problèmes précédemment inaperçus dans l’application ou le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="9e0bd-160">Adding large amounts of memory on the server sometimes exposes previously unnoticed problems in either the application or the operating system.</span></span>

 

 




