---
title: Conditions préalables pour le développement avec DirectX
description: Lorsque vous commencez à développer une application Windows à l’aide de DirectX, gardez à l’esprit les conditions préalables de cette page. Cela comprend les technologies que vous devez connaître avant de vous plonger dans.
ms.assetid: 93f566cf-0c16-4487-9d53-dc59746e4d00
keywords:
- Application DirectX, conditions préalables
- Application DirectX, application du Windows Store
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d5e09484bef67546047214702fab7d2d0a5c48d
ms.sourcegitcommit: 6394972f1e8b01229db602469df6bb137e31d776
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/16/2020
ms.locfileid: "104463975"
---
# <a name="prerequisites-for-developing-with-directx"></a><span data-ttu-id="9ed25-106">Conditions préalables pour le développement avec DirectX</span><span class="sxs-lookup"><span data-stu-id="9ed25-106">Prerequisites for developing with DirectX</span></span>

<span data-ttu-id="9ed25-107">Lorsque vous commencez à développer une application Windows à l’aide de DirectX, gardez à l’esprit les conditions préalables de cette page.</span><span class="sxs-lookup"><span data-stu-id="9ed25-107">When you start to develop a Windows app using DirectX, keep the prerequisites on this page in mind.</span></span> <span data-ttu-id="9ed25-108">Cela comprend les technologies que vous devez connaître avant de vous plonger dans.</span><span class="sxs-lookup"><span data-stu-id="9ed25-108">This includes the technologies you need to know before you dive in.</span></span>

## <a name="what-should-i-know-to-develop-a-windows-game-using-directx"></a><span data-ttu-id="9ed25-109">Que dois-je savoir pour développer un jeu Windows à l’aide de DirectX ?</span><span class="sxs-lookup"><span data-stu-id="9ed25-109">What should I know to develop a Windows game using DirectX?</span></span>

<span data-ttu-id="9ed25-110">Avant de commencer à développer une application du Windows Store à l’aide de DirectX, vous devez savoir comment programmer dans Windows avec C++.</span><span class="sxs-lookup"><span data-stu-id="9ed25-110">Before you start to develop a Windows Store app using DirectX, you need to know how to program in Windows with C++.</span></span> <span data-ttu-id="9ed25-111">Les applications Windows utilisant DirectX sont développées à un faible niveau de programmation, ce qui signifie que vous êtes exposé à de nombreuses fonctionnalités du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="9ed25-111">Windows apps using DirectX are developed at a low level of programming, which means that you will be exposed to many features of the operating system.</span></span> <span data-ttu-id="9ed25-112">Il s’agit notamment de la gestion de la mémoire et des ressources, ainsi que de l’interface du périphérique graphique lui-même.</span><span class="sxs-lookup"><span data-stu-id="9ed25-112">These include memory and resource management, and the interface for the graphics device itself.</span></span> <span data-ttu-id="9ed25-113">Si vous débutez avec le développement d’applications de jeux ou graphiques, cette opération peut s’avérer difficile.</span><span class="sxs-lookup"><span data-stu-id="9ed25-113">If you are new to game or graphics app development, you may find this challenging.</span></span> <span data-ttu-id="9ed25-114">Mais vous y trouverez également une récompense, car le développement de jeux à ce niveau crée des possibilités bien supérieures pour la conception et le développement d’applications graphiques et de jeux.</span><span class="sxs-lookup"><span data-stu-id="9ed25-114">But you will also find it rewarding, because learning game development at this level creates far, far greater possibilities for game and graphics app design and development.</span></span>

<span data-ttu-id="9ed25-115">Vous devez également comprendre les principes fondamentaux de la programmation et des mathématiques graphiques 2D et 3D, car la plupart des API que vous utiliserez ont été développées avec ces principes à l’esprit.</span><span class="sxs-lookup"><span data-stu-id="9ed25-115">You'll also need to understand the basics of 2D and 3D graphics programming and mathematics, because many of the APIs you'll use were developed with these principles in mind.</span></span> <span data-ttu-id="9ed25-116">Il est plus facile de comprendre les paramètres et les résultats si vous êtes familiarisé avec les opérations qui en dépendent.</span><span class="sxs-lookup"><span data-stu-id="9ed25-116">It'll be easier for you to understand their parameters and results if you are familiar with the operations behind them.</span></span>

<span data-ttu-id="9ed25-117">Au minimum, vous devez comprendre les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="9ed25-117">At a minimum, you should have a grasp of the following:</span></span>

-   <span data-ttu-id="9ed25-118">Programmation Windows C/C++.</span><span class="sxs-lookup"><span data-stu-id="9ed25-118">Windows C/C++ programming.</span></span> <span data-ttu-id="9ed25-119">Cela signifie que vous comprenez les pointeurs et les références, les événements et les rappels, et peut-être quelques bibliothèques communes comme ATL.</span><span class="sxs-lookup"><span data-stu-id="9ed25-119">This means that you understand pointers and references, events and callbacks, and perhaps a few of the common libraries like ATL.</span></span>
-   <span data-ttu-id="9ed25-120">Programmation Win32.</span><span class="sxs-lookup"><span data-stu-id="9ed25-120">Win32 programming.</span></span> <span data-ttu-id="9ed25-121">Vous comprenez comment les fenêtres sont créées et comment les événements d’interface utilisateur sont traités.</span><span class="sxs-lookup"><span data-stu-id="9ed25-121">You understand how windows are created, and how user interface events are processed.</span></span> <span data-ttu-id="9ed25-122">Vous comprenez également un peu les API COM et Win32 essentielles.</span><span class="sxs-lookup"><span data-stu-id="9ed25-122">You also understand a little bit about COM and essential Win32 APIs.</span></span>
-   <span data-ttu-id="9ed25-123">Algébrique et trigonométrie linéaires.</span><span class="sxs-lookup"><span data-stu-id="9ed25-123">Linear algebra and trigonometry.</span></span> <span data-ttu-id="9ed25-124">Bien que ce ne soit pas essentiel, vous aurez plus de temps si vous êtes familiarisé avec les concepts de ces deux disciplines mathématiques, car ils constituent la base d’une grande partie de la programmation de graphiques 3D.</span><span class="sxs-lookup"><span data-stu-id="9ed25-124">While not essential, you'll have an easier time if you are familiar with concepts from these two math disciplines, because they are the foundation of much of 3D graphics programming.</span></span>
-   <span data-ttu-id="9ed25-125">La terminologie et les concepts graphiques de base, tels que les bitmaps, les textures, les vertex, les mailles et les fenêtres d’affichage.</span><span class="sxs-lookup"><span data-stu-id="9ed25-125">Basic graphics terminology and concepts, such as bitmaps, textures, vertices, meshes, and viewports.</span></span>

## <a name="what-does-directx-provide-me"></a><span data-ttu-id="9ed25-126">Qu’est-ce que DirectX me permet ?</span><span class="sxs-lookup"><span data-stu-id="9ed25-126">What does DirectX provide me?</span></span>

<span data-ttu-id="9ed25-127">DirectX est l’ensemble principal d’API graphiques que vous allez utiliser pour développer des jeux Windows.</span><span class="sxs-lookup"><span data-stu-id="9ed25-127">DirectX is the primary set of graphics APIs you'll use to develop Windows games.</span></span> <span data-ttu-id="9ed25-128">Voici les catégories de fonctionnalités que vous devez connaître lorsque vous décidez du développement de votre jeu.</span><span class="sxs-lookup"><span data-stu-id="9ed25-128">Here are the categories of features that you must become familiar with when you decide how to develop your game.</span></span>



| <span data-ttu-id="9ed25-129">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="9ed25-129">Library</span></span>     | <span data-ttu-id="9ed25-130">Description</span><span class="sxs-lookup"><span data-stu-id="9ed25-130">Description</span></span>                                                                                                                                     |
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ed25-131">Direct3D</span><span class="sxs-lookup"><span data-stu-id="9ed25-131">Direct3D</span></span>    | <span data-ttu-id="9ed25-132">Ensemble de bibliothèques puissantes, orientées performances et accélérées par le matériel pour le rendu de graphiques 3D.</span><span class="sxs-lookup"><span data-stu-id="9ed25-132">A powerful, performance-oriented, hardware-accelerated set of libraries for rendering 3D graphics.</span></span>                                              |
| <span data-ttu-id="9ed25-133">Direct2D</span><span class="sxs-lookup"><span data-stu-id="9ed25-133">Direct2D</span></span>    | <span data-ttu-id="9ed25-134">Ensemble de bibliothèques de graphiques 2D pour l’image bitmap accélérée par le matériel et le dessin 2D vectoriel.</span><span class="sxs-lookup"><span data-stu-id="9ed25-134">A set of 2D graphics libraries for hardware-accelerated bitmap and vector 2D drawing.</span></span>                                                           |
| <span data-ttu-id="9ed25-135">DirectXMath</span><span class="sxs-lookup"><span data-stu-id="9ed25-135">DirectXMath</span></span> | <span data-ttu-id="9ed25-136">Bibliothèque d’opérations mathématiques courantes et optimisées utilisées dans les graphiques 2D et 3D, comme les opérations de vecteur et de matrice.</span><span class="sxs-lookup"><span data-stu-id="9ed25-136">A library of common, optimized math operations used in 2D and 3D graphics, such as vector and matrix operations.</span></span>                                |
| <span data-ttu-id="9ed25-137">DirectWrite</span><span class="sxs-lookup"><span data-stu-id="9ed25-137">DirectWrite</span></span> | <span data-ttu-id="9ed25-138">Bibliothèque d’API de rendu et de disposition de texte 2D.</span><span class="sxs-lookup"><span data-stu-id="9ed25-138">A library of 2D text rendering and layout APIs.</span></span> <span data-ttu-id="9ed25-139">Il prend en charge l’accélération matérielle et la pixellisation des logiciels.</span><span class="sxs-lookup"><span data-stu-id="9ed25-139">It supports both hardware acceleration and software rasterization.</span></span>                              |
| <span data-ttu-id="9ed25-140">XAudio2</span><span class="sxs-lookup"><span data-stu-id="9ed25-140">XAudio2</span></span>     | <span data-ttu-id="9ed25-141">Une API audio multiplateforme de bas niveau pour Microsoft Windows qui fournit un traitement de signal et une base de mixage audio pour le développement de jeux.</span><span class="sxs-lookup"><span data-stu-id="9ed25-141">A low-level, cross-platform audio API for Microsoft Windows that provides a signal processing and audio mixing foundation for game development.</span></span> |
| <span data-ttu-id="9ed25-142">XInput</span><span class="sxs-lookup"><span data-stu-id="9ed25-142">XInput</span></span>      | <span data-ttu-id="9ed25-143">Bibliothèque qui prend en charge différents contrôles de jeu traditionnels, en mettant l’accent sur le modèle de contrôleur Xbox 360.</span><span class="sxs-lookup"><span data-stu-id="9ed25-143">A library that supports various traditional gaming controls, with an emphasis on the Xbox 360 controller model.</span></span>                                 |



 

## <a name="what-tools-do-i-need-to-develop-a-windows-game-with-directx"></a><span data-ttu-id="9ed25-144">De quels outils ai-je besoin pour développer un jeu Windows avec DirectX ?</span><span class="sxs-lookup"><span data-stu-id="9ed25-144">What tools do I need to develop a Windows game with DirectX?</span></span>

<span data-ttu-id="9ed25-145">Pour vous familiariser avec ce didacticiel, vous avez besoin des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="9ed25-145">To get started with this tutorial, you need:</span></span>

-   <span data-ttu-id="9ed25-146">Windows 8.1 ou supérieur</span><span class="sxs-lookup"><span data-stu-id="9ed25-146">Windows 8.1 or greater</span></span>
-   <span data-ttu-id="9ed25-147">Microsoft Visual Studio 2013 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="9ed25-147">Microsoft Visual Studio 2013 or greater</span></span>

 

 




