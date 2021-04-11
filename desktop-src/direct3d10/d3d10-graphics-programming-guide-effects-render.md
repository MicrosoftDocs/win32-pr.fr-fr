---
description: Un effet peut être utilisé pour stocker des informations ou pour effectuer un rendu à l’aide d’un groupe d’États.
ms.assetid: c5654335-ad80-4a5b-bf1f-5f32b2cc8ea2
title: Rendu d’un effet (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfba9432412846e2dc634d6ab68be999b504e06f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104200921"
---
# <a name="rendering-an-effect-direct3d-10"></a><span data-ttu-id="1f7f7-103">Rendu d’un effet (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="1f7f7-103">Rendering an Effect (Direct3D 10)</span></span>

<span data-ttu-id="1f7f7-104">Un effet peut être utilisé pour stocker des informations ou pour effectuer un rendu à l’aide d’un groupe d’États.</span><span class="sxs-lookup"><span data-stu-id="1f7f7-104">An effect can be used to store information, or to render using a group of state.</span></span> <span data-ttu-id="1f7f7-105">Chaque technique spécifie les nuanceurs de vertex, les nuanceurs de géométrie, les nuanceurs de pixels, l’état du nuanceur, l’échantillonnage et l’état de la texture, ainsi que l’état du pipeline.</span><span class="sxs-lookup"><span data-stu-id="1f7f7-105">Each technique specifies vertex shaders, geometry shaders, pixel shaders, shader state, sampler and texture state and other pipeline state.</span></span> <span data-ttu-id="1f7f7-106">Ainsi, une fois que vous avez organisé l’État en conséquence, vous pouvez encapsuler l’effet de rendu résultant de cet État en créant et en rendant l’effet.</span><span class="sxs-lookup"><span data-stu-id="1f7f7-106">So once you have organized state into an effect, you can encapsulate the rendering effect that results from that state by creating and rendering the effect.</span></span>

<span data-ttu-id="1f7f7-107">Il existe quelques étapes pour préparer un effet pour le rendu.</span><span class="sxs-lookup"><span data-stu-id="1f7f7-107">There are a few steps for preparing an effect for rendering.</span></span> <span data-ttu-id="1f7f7-108">La première consiste à compiler, qui vérifie le code HLSL comme par rapport à la syntaxe du langage HLSL et aux règles de l’infrastructure d’effet.</span><span class="sxs-lookup"><span data-stu-id="1f7f7-108">The first is compiling, which checks the HLSL like code against the HLSL language syntax and the effect framework rules.</span></span> <span data-ttu-id="1f7f7-109">Vous pouvez compiler un effet à partir de votre application à l’aide d’appels d’API ou vous pouvez compiler un effet hors connexion à l’aide de l’utilitaire Effect compiler.</span><span class="sxs-lookup"><span data-stu-id="1f7f7-109">You can compile an effect from your application using API calls or you can compile an effect offline using the effect compiler utility.</span></span> <span data-ttu-id="1f7f7-110">Une fois que votre effet a été compilé avec succès, créez-le en appelant un ensemble d’API différent (mais très similaire).</span><span class="sxs-lookup"><span data-stu-id="1f7f7-110">Once your effect has successfully compiled, create it by calling a different (but very similar) set of APIs.</span></span>

<span data-ttu-id="1f7f7-111">Une fois l’effet créé, il y a deux étapes restantes pour l’utiliser.</span><span class="sxs-lookup"><span data-stu-id="1f7f7-111">After the effect is created, there are two remaining steps for using it.</span></span> <span data-ttu-id="1f7f7-112">Tout d’abord, vous devez initialiser les valeurs d’état des effets (les valeurs des variables d’effet) à l’aide d’un certain nombre de méthodes pour définir l’État.</span><span class="sxs-lookup"><span data-stu-id="1f7f7-112">First, you must initialize the effect state values (the values of the effect variables) using a number of methods for setting state.</span></span> <span data-ttu-id="1f7f7-113">Pour certaines variables, cette opération peut être effectuée une fois lors de la création d’un effet ; d’autres doivent être mis à jour chaque fois que votre application appelle la boucle de rendu.</span><span class="sxs-lookup"><span data-stu-id="1f7f7-113">For some variables this can be done once when an effect is created; others must be updated each time your application calls the render loop.</span></span> <span data-ttu-id="1f7f7-114">Une fois les variables d’effet définies, vous indiquez au runtime d’afficher les effets en appliquant une technique.</span><span class="sxs-lookup"><span data-stu-id="1f7f7-114">Once the effect variables are set, you tell the runtime to render the affect by applying a technique.</span></span> <span data-ttu-id="1f7f7-115">Ces rubriques sont abordées plus en détail ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="1f7f7-115">These topics are all discussed in further detail below.</span></span>

-   [<span data-ttu-id="1f7f7-116">Compiler un effet (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="1f7f7-116">Compile an Effect (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-effects-compile.md)
-   [<span data-ttu-id="1f7f7-117">Créer un effet (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="1f7f7-117">Create an Effect (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-effects-create.md)
-   [<span data-ttu-id="1f7f7-118">Définir l’état de l’effet (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="1f7f7-118">Set Effect State (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-effects-set-state.md)
-   [<span data-ttu-id="1f7f7-119">Appliquer une technique (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="1f7f7-119">Apply a Technique (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-effects-apply-technique.md)

<span data-ttu-id="1f7f7-120">Naturellement, il existe des [considérations relatives aux performances](d3d10-graphics-programming-guide-effects-performance.md) pour l’utilisation des effets.</span><span class="sxs-lookup"><span data-stu-id="1f7f7-120">Naturally there are [performance considerations](d3d10-graphics-programming-guide-effects-performance.md) for using effects.</span></span> <span data-ttu-id="1f7f7-121">Ces considérations sont en grande partie les mêmes si vous n’utilisez pas d’effet.</span><span class="sxs-lookup"><span data-stu-id="1f7f7-121">These considerations are largely the same if you are not using an effect.</span></span> <span data-ttu-id="1f7f7-122">Par exemple, la réduction du nombre de modifications d’État ou l’Organisation des variables qui doivent être mises à jour par fréquence.</span><span class="sxs-lookup"><span data-stu-id="1f7f7-122">Things like, minimizing the amount of state changes, or organizing the variables that need to be updated by frequency.</span></span> <span data-ttu-id="1f7f7-123">Ces tactiques permettent de réduire la quantité de données qui doivent être envoyées du processeur au GPU, et donc de réduire les problèmes potentiels de synchronisation.</span><span class="sxs-lookup"><span data-stu-id="1f7f7-123">These tactics are used to minimize the amount of data that needs to be sent from the CPU to the GPU, and therefore minimize potential synchronization problems.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1f7f7-124">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1f7f7-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1f7f7-125">Effets (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="1f7f7-125">Effects (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-effects.md)
</dt> </dl>

 

 



