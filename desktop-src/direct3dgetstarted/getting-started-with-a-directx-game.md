---
title: Prise en main de DirectX pour Windows
description: La création d’un jeu Microsoft DirectX pour Windows est un défi pour un nouveau développeur. Ici, nous examinons rapidement les concepts impliqués et les étapes que vous devez suivre pour commencer à développer un jeu à l’aide de DirectX et C++.
ms.assetid: fd460c52-9854-4ffe-b89e-5219be2e11f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae09cd127a30401ae0493f5dd770fe1e67607b45
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106511696"
---
# <a name="get-started-with-directx-for-windows"></a><span data-ttu-id="b77de-104">Prise en main de DirectX pour Windows</span><span class="sxs-lookup"><span data-stu-id="b77de-104">Get started with DirectX for Windows</span></span>

<span data-ttu-id="b77de-105">La création d’un jeu Microsoft DirectX pour Windows est un défi pour un nouveau développeur.</span><span class="sxs-lookup"><span data-stu-id="b77de-105">Creating a Microsoft DirectX game for Windows is a challenge for a new developer.</span></span> <span data-ttu-id="b77de-106">Ici, nous examinons rapidement les concepts impliqués et les étapes que vous devez suivre pour commencer à développer un jeu à l’aide de DirectX et C++.</span><span class="sxs-lookup"><span data-stu-id="b77de-106">Here we quickly review the concepts involved and the steps you must take to begin developing a game using DirectX and C++.</span></span>

<span data-ttu-id="b77de-107">Commençons.</span><span class="sxs-lookup"><span data-stu-id="b77de-107">Let's get started.</span></span>

## <a name="what-skills-do-you-need"></a><span data-ttu-id="b77de-108">Quelles sont les compétences dont vous avez besoin ?</span><span class="sxs-lookup"><span data-stu-id="b77de-108">What skills do you need?</span></span>

<span data-ttu-id="b77de-109">Pour développer un jeu dans DirectX pour Windows, vous devez avoir quelques compétences de base.</span><span class="sxs-lookup"><span data-stu-id="b77de-109">To develop a game in DirectX for Windows, you must have a few basic skills.</span></span> <span data-ttu-id="b77de-110">Plus précisément, vous devez être en mesure d’effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="b77de-110">Specifically, you must be able to:</span></span>

-   <span data-ttu-id="b77de-111">Lisez et écrivez du code C++ moderne (C++ 11 vous aide le plus) et familiarisez-vous avec les principes et modèles de conception C++ de base tels que les modèles et le modèle de fabrique.</span><span class="sxs-lookup"><span data-stu-id="b77de-111">Read and write modern C++ code (C++11 helps the most), and be familiar with basic C++ design principles and patterns like templates and the factory model.</span></span> <span data-ttu-id="b77de-112">Vous devez également être familiarisé avec les bibliothèques C++ courantes, telles que la bibliothèque STL (Standard Template Library), et plus particulièrement avec les opérateurs de conversion, les types pointeur et les structures de données de bibliothèque de modèles standard (telles que STD :: Vector).</span><span class="sxs-lookup"><span data-stu-id="b77de-112">You must also be familiar with common C++ libraries like the Standard Template Library, and specifically with the casting operators, pointer types, and the standard template library data structures (such as std::vector).</span></span>
-   <span data-ttu-id="b77de-113">Comprenez la géométrie de base, la trigonométrie et l’algèbre linéaire.</span><span class="sxs-lookup"><span data-stu-id="b77de-113">Understand basic geometry, trigonometry, and linear algebra.</span></span> <span data-ttu-id="b77de-114">La majeure partie du code que vous trouverez dans les exemples suppose que vous comprenez ces formes de mathématiques et leurs règles communes.</span><span class="sxs-lookup"><span data-stu-id="b77de-114">Much of the code you will find in the examples assumes you understand these forms of mathematics and their common rules.</span></span>
-   <span data-ttu-id="b77de-115">Familiarisez-vous avec COM, en particulier [**Microsoft :: WRL :: ComPtr**](/previous-versions/visualstudio/visual-studio-2012/br244983(v=vs.110)) (pointeur intelligent).</span><span class="sxs-lookup"><span data-stu-id="b77de-115">Have familiarity with COM—especially [**Microsoft::WRL::ComPtr**](/previous-versions/visualstudio/visual-studio-2012/br244983(v=vs.110)) (smart pointer).</span></span>
-   <span data-ttu-id="b77de-116">Découvrez les bases de la technologie Graphics and Graphics, en particulier les graphiques 3D.</span><span class="sxs-lookup"><span data-stu-id="b77de-116">Understand the foundations of graphics and graphics technology, particularly 3D graphics.</span></span> <span data-ttu-id="b77de-117">Bien que DirectX ait sa propre terminologie, il s’appuie toujours sur une compréhension bien établie des principes graphiques 3D généraux.</span><span class="sxs-lookup"><span data-stu-id="b77de-117">While DirectX itself has its own terminology, it still builds upon a well-established understanding of general 3D graphics principles.</span></span>
-   <span data-ttu-id="b77de-118">Comprendre le concept d’une boucle de message, car vous allez implémenter une boucle qui écoute le système d’exploitation Windows.</span><span class="sxs-lookup"><span data-stu-id="b77de-118">Understand the concept of a message loop, because you'll be implementing a loop that listens to the Windows operating system.</span></span>

## <a name="and-were-off"></a><span data-ttu-id="b77de-119">Et nous sommes inactifs !</span><span class="sxs-lookup"><span data-stu-id="b77de-119">And we're off!</span></span>

<span data-ttu-id="b77de-120">Prêt à commencer ?</span><span class="sxs-lookup"><span data-stu-id="b77de-120">Ready to start?</span></span> <span data-ttu-id="b77de-121">Nous allons nous pencher sur.</span><span class="sxs-lookup"><span data-stu-id="b77de-121">Let's review before we head on.</span></span> <span data-ttu-id="b77de-122">Vous avez :</span><span class="sxs-lookup"><span data-stu-id="b77de-122">You have:</span></span>

-   <span data-ttu-id="b77de-123">Une installation mise à jour et opérationnelle de Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="b77de-123">An updated and working installation of Windows 8.1.</span></span>
-   <span data-ttu-id="b77de-124">Installation de [Microsoft Visual Studio](https://visualstudio.microsoft.com/downloads/download-visual-studio-vs).</span><span class="sxs-lookup"><span data-stu-id="b77de-124">An installation of [Microsoft Visual Studio](https://visualstudio.microsoft.com/downloads/download-visual-studio-vs).</span></span>
-   <span data-ttu-id="b77de-125">Un esprit intrépide et un désir d’en savoir plus sur le développement de jeux DirectX !</span><span class="sxs-lookup"><span data-stu-id="b77de-125">An intrepid spirit and a desire to learn more about DirectX game development!</span></span>

## <a name="next-steps"></a><span data-ttu-id="b77de-126">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="b77de-126">Next steps</span></span>



|                                                                                                    |                                                                                                           |
|----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b77de-127">Utiliser les ressources de l’appareil DirectX</span><span class="sxs-lookup"><span data-stu-id="b77de-127">Work with DirectX device resources</span></span>](work-with-dxgi.md)                                           | <span data-ttu-id="b77de-128">Découvrez comment utiliser DXGI pour créer un appareil graphique virtualisé et créer et configurer une chaîne de permutation.</span><span class="sxs-lookup"><span data-stu-id="b77de-128">Learn how to use DXGI to create a virtualized graphics device, and create and configure a swap chain.</span></span>     |
| [<span data-ttu-id="b77de-129">Comprendre le pipeline de rendu Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="b77de-129">Understand the Direct3D 11 rendering pipeline</span></span>](understand-the-directx-11-2-graphics-pipeline.md) | <span data-ttu-id="b77de-130">Découvrez comment raccorder la classe de ressources de l’appareil DirectX et dessiner à l’aide du pipeline de graphiques Direct3D.</span><span class="sxs-lookup"><span data-stu-id="b77de-130">Learn how to hook into the DirectX device resources class, and draw using the Direct3D graphics pipeline.</span></span> |
| [<span data-ttu-id="b77de-131">Utiliser des nuanceurs et des ressources de nuanceur</span><span class="sxs-lookup"><span data-stu-id="b77de-131">Work with shaders and shader resources</span></span>](work-with-shaders-and-shader-resources.md)               | <span data-ttu-id="b77de-132">Découvrez comment écrire des programmes nuanceurs HLSL pour les étapes de pipeline de graphiques Direct3D.</span><span class="sxs-lookup"><span data-stu-id="b77de-132">Learn how to write HLSL shader programs for Direct3D graphics pipeline stages.</span></span>                            |



 

 

 