---
title: Créer votre première application Windows à l’aide de DirectX
description: Cette section décrit les raisons pour lesquelles vous pouvez utiliser le modèle C++ pour le développement d’applications du Windows Store et fournit des didacticiels et des procédures de base pour la prise en main du développement d’applications DirectX.
ms.assetid: b632ba9c-1c30-4d21-ac79-7f2a193956fe
keywords:
- Application DirectX, prise en main
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da5e3afed57244789c0e3e06ab71ec39e581305c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103670969"
---
# <a name="create-your-first-windows-app-using-directx"></a><span data-ttu-id="0a6b6-104">Créer votre première application Windows à l’aide de DirectX</span><span class="sxs-lookup"><span data-stu-id="0a6b6-104">Create your first Windows app using DirectX</span></span>

<span data-ttu-id="0a6b6-105">Si vous connaissez DirectX, vous pouvez développer une application DirectX en utilisant le langage C++ natif et le langage HLSL pour tirer pleinement parti du matériel graphique.</span><span class="sxs-lookup"><span data-stu-id="0a6b6-105">If you know DirectX, you can develop a DirectX app using native C++ and HLSL to take full advantage of graphics hardware.</span></span>

<span data-ttu-id="0a6b6-106">Utilisez ce didacticiel de base pour commencer à utiliser le développement d’applications DirectX, puis utilisez la feuille de route pour poursuivre l’exploration de DirectX.</span><span class="sxs-lookup"><span data-stu-id="0a6b6-106">Use this basic tutorial to get started with DirectX app development, then use the roadmap to continue exploring DirectX.</span></span>

## <a name="windows-desktop-app-with-c-and-directx"></a><span data-ttu-id="0a6b6-107">Application de bureau Windows avec C++ et DirectX</span><span class="sxs-lookup"><span data-stu-id="0a6b6-107">Windows desktop app with C++ and DirectX</span></span>

<span data-ttu-id="0a6b6-108">Une application de bureau Windows avec DirectX est une application développée à l’aide des API natives C++ et DirectX.</span><span class="sxs-lookup"><span data-stu-id="0a6b6-108">A Windows desktop app with DirectX is an app developed using native C++ and DirectX APIs.</span></span> <span data-ttu-id="0a6b6-109">Ce modèle est plus complexe qu’une application écrite dans un Framework géré, mais il offre une plus grande souplesse et un meilleur accès aux ressources système, en particulier les périphériques graphiques.</span><span class="sxs-lookup"><span data-stu-id="0a6b6-109">This model is more complex than an app written in a managed framework, but it provides greater flexibility and greater access to system resources especially graphics devices.</span></span> <span data-ttu-id="0a6b6-110">C’est donc un bon modèle pour le développeur expérimenté.</span><span class="sxs-lookup"><span data-stu-id="0a6b6-110">So, it is a good model for the experienced developer.</span></span>

## <a name="why-develop-a-windows-app-with-directx"></a><span data-ttu-id="0a6b6-111">Pourquoi développer une application Windows avec DirectX ?</span><span class="sxs-lookup"><span data-stu-id="0a6b6-111">Why develop a Windows app with DirectX?</span></span>

<span data-ttu-id="0a6b6-112">La réponse est simple : vous souhaitez créer un jeu qui utilise beaucoup de graphiques ou de multimédia, et peut utiliser les fonctionnalités prises en charge par de nombreux périphériques graphiques.</span><span class="sxs-lookup"><span data-stu-id="0a6b6-112">The answer is simple: you want to make a game that is graphics- or multimedia-intensive, and can use the features that many graphics devices support.</span></span> <span data-ttu-id="0a6b6-113">Ce n’est pas facile si vous ne connaissez pas le développement de jeux ou le développement Windows et C/C++, mais qu’il existe une bonne nouvelle : DirectX 11 est la version la plus simple et la plus cohésive de Microsoft DirectX.</span><span class="sxs-lookup"><span data-stu-id="0a6b6-113">This won't be easy if you are new to game development or to Windows development and C/C++, but there's some good news: DirectX 11 is the simplest and most cohesive version of Microsoft DirectX yet.</span></span> <span data-ttu-id="0a6b6-114">C’est également le plus puissant et le plus riche en fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="0a6b6-114">It's also the most powerful and feature-rich.</span></span> <span data-ttu-id="0a6b6-115">Si votre objectif est de maîtriser le développement de jeux et d’apprendre les techniques de rendu les plus avancées, DirectX peut vous offrir la possibilité de le faire.</span><span class="sxs-lookup"><span data-stu-id="0a6b6-115">If your goal is to master game development and learn the most advanced rendering techniques, then DirectX can provide the opportunity for you to do that.</span></span>

<span data-ttu-id="0a6b6-116">Cela dit, la planification de votre jeu (ou de l’application interactive, en temps réel) est essentielle.</span><span class="sxs-lookup"><span data-stu-id="0a6b6-116">That said, planning your game (or interactive, real-time app) is essential.</span></span> <span data-ttu-id="0a6b6-117">Si vous débutez dans le développement de jeux et que votre jeu n’a pas besoin d’exigences graphiques, envisagez de le développer avec le .NET Framework à la place.</span><span class="sxs-lookup"><span data-stu-id="0a6b6-117">If you are new to game development, and your game doesn't have demanding graphics requirements, consider developing it with the .NET framework instead.</span></span> <span data-ttu-id="0a6b6-118">En outre, un grand nombre de graphiques « middleware » et de packages de développement de jeux sont disponibles pour les plateformes Windows, et d’autres ne nécessitent pas de compétences de programmation significatives.</span><span class="sxs-lookup"><span data-stu-id="0a6b6-118">Also, many "middleware" graphics and game development packages are available for Windows platforms, and some do not require significant programming skills.</span></span>

<span data-ttu-id="0a6b6-119">Si vous êtes sûr ou si vous avez simplement un rêve de créer un jeu avec des graphiques haute fidélité (ou une application avec du contenu graphique complexe), lisez-le !</span><span class="sxs-lookup"><span data-stu-id="0a6b6-119">If you are confident, or simply have a dream of making a game with high-fidelity graphics (or an app with complex graphics content), then read on!</span></span>

## <a name="in-this-section"></a><span data-ttu-id="0a6b6-120">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="0a6b6-120">In this section</span></span>



| <span data-ttu-id="0a6b6-121">Rubrique</span><span class="sxs-lookup"><span data-stu-id="0a6b6-121">Topic</span></span>                                                                                                                     | <span data-ttu-id="0a6b6-122">Description</span><span class="sxs-lookup"><span data-stu-id="0a6b6-122">Description</span></span>                                                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0a6b6-123">Conditions préalables pour le développement avec DirectX</span><span class="sxs-lookup"><span data-stu-id="0a6b6-123">Prerequisites for developing with DirectX</span></span>](pre-requisites-for-developing-a-tailored-c---with-directx-app.md)<br/> | <span data-ttu-id="0a6b6-124">Lorsque vous commencez à développer une application Windows à l’aide de DirectX, gardez à l’esprit les conditions préalables de cette page.</span><span class="sxs-lookup"><span data-stu-id="0a6b6-124">When you start to develop a Windows app using DirectX, keep the prerequisites on this page in mind.</span></span> <span data-ttu-id="0a6b6-125">Cela comprend les technologies que vous devez connaître avant de vous plonger dans.</span><span class="sxs-lookup"><span data-stu-id="0a6b6-125">This includes the technologies you need to know before you dive in.</span></span><br/>                            |
| [<span data-ttu-id="0a6b6-126">Prise en main de DirectX pour Windows</span><span class="sxs-lookup"><span data-stu-id="0a6b6-126">Get started with DirectX for Windows</span></span>](getting-started-with-a-directx-game.md)<br/>                                | <span data-ttu-id="0a6b6-127">La création d’un jeu DirectX pour Windows est un défi pour un nouveau développeur.</span><span class="sxs-lookup"><span data-stu-id="0a6b6-127">Creating a DirectX game for Windows is a challenge for a new developer.</span></span> <span data-ttu-id="0a6b6-128">Ici, nous examinons rapidement les concepts impliqués et les étapes que vous devez suivre pour commencer à développer un jeu à l’aide de DirectX et C++.</span><span class="sxs-lookup"><span data-stu-id="0a6b6-128">Here we quickly review the concepts involved and the steps you must take to begin developing a game using DirectX and C++.</span></span><br/> |
| [<span data-ttu-id="0a6b6-129">Feuille de route pour les applications de bureau DirectX</span><span class="sxs-lookup"><span data-stu-id="0a6b6-129">Roadmap for Desktop DirectX apps</span></span>](roadmap-for-metro-style-apps-using-directx.md)<br/>                             | <span data-ttu-id="0a6b6-130">Voici des ressources clés pour vous aider à utiliser DirectX et C++ pour développer des applications de bureau riches en graphiques, comme les jeux.</span><span class="sxs-lookup"><span data-stu-id="0a6b6-130">Here are key resources to help you get started with using DirectX and C++ to develop graphics-intensive Desktop apps, like games.</span></span> <br/>                                                                 |



 

 

 





