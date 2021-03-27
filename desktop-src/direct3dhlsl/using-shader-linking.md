---
title: Utilisation de la liaison de nuanceur
description: Nous montrons comment créer des fonctions HLSL précompilées, les empaqueter dans des bibliothèques et les lier à des nuanceurs complets au moment de l’exécution.
ms.assetid: 3A1597FF-F848-415E-BDF8-199C69C05C3B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7528415f1bedb0364a9c4b09126a983222fc42b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729916"
---
# <a name="using-shader-linking"></a><span data-ttu-id="2ae26-103">Utilisation de la liaison de nuanceur</span><span class="sxs-lookup"><span data-stu-id="2ae26-103">Using shader linking</span></span>

<span data-ttu-id="2ae26-104">Nous montrons comment créer des fonctions HLSL précompilées, les empaqueter dans des bibliothèques et les lier à des nuanceurs complets au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="2ae26-104">We show how to create precompiled HLSL functions, package them into libraries, and link them into full shaders at run-time.</span></span> <span data-ttu-id="2ae26-105">La liaison de nuanceur est prise en charge à partir de Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="2ae26-105">Shader linking is supported starting with Windows 8.1.</span></span>

<span data-ttu-id="2ae26-106">**Objectif :** Découvrez comment utiliser la liaison de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="2ae26-106">**Objective:** Learn how to use shader linking.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="2ae26-107">Prérequis</span><span class="sxs-lookup"><span data-stu-id="2ae26-107">Prerequisites</span></span>

<span data-ttu-id="2ae26-108">Nous partons du principe que vous êtes familiarisé avec C++.</span><span class="sxs-lookup"><span data-stu-id="2ae26-108">We assume that you are familiar with C++.</span></span> <span data-ttu-id="2ae26-109">Vous avez également besoin d’une expérience de base dans les concepts de programmation graphique.</span><span class="sxs-lookup"><span data-stu-id="2ae26-109">You also need basic experience with graphics programming concepts.</span></span>

<span data-ttu-id="2ae26-110">**Durée totale :** 60 minutes.</span><span class="sxs-lookup"><span data-stu-id="2ae26-110">**Total time to complete:** 60 minutes.</span></span>

## <a name="where-to-go-from-here"></a><span data-ttu-id="2ae26-111">Où aller à partir d’ici</span><span class="sxs-lookup"><span data-stu-id="2ae26-111">Where to go from here</span></span>

<span data-ttu-id="2ae26-112">Consultez également [API HLSL compiler](dx-graphics-d3dcompiler-reference.md).</span><span class="sxs-lookup"><span data-stu-id="2ae26-112">Also see [HLSL compiler APIs](dx-graphics-d3dcompiler-reference.md).</span></span>

<span data-ttu-id="2ae26-113">Les opérations suivantes sont abordées :</span><span class="sxs-lookup"><span data-stu-id="2ae26-113">We show you how to:</span></span>

-   <span data-ttu-id="2ae26-114">Compiler le code de votre nuanceur</span><span class="sxs-lookup"><span data-stu-id="2ae26-114">Compile your shader code</span></span>
-   <span data-ttu-id="2ae26-115">Charger le code compilé dans une bibliothèque de nuanceur</span><span class="sxs-lookup"><span data-stu-id="2ae26-115">Load the compiled code into a shader library</span></span>
-   <span data-ttu-id="2ae26-116">Lier les ressources des emplacements sources aux emplacements de destination</span><span class="sxs-lookup"><span data-stu-id="2ae26-116">Bind the resources from source slots to destination slots</span></span>
-   <span data-ttu-id="2ae26-117">Construire une fonction-liaison-graphiques (FLGs) pour les nuanceurs</span><span class="sxs-lookup"><span data-stu-id="2ae26-117">Construct function-linking-graphs (FLGs) for shaders</span></span>
-   <span data-ttu-id="2ae26-118">Lier des graphiques de nuanceur à une bibliothèque de nuanceur pour produire un objet blob de nuanceur que le runtime Direct3D peut utiliser</span><span class="sxs-lookup"><span data-stu-id="2ae26-118">Link shader graphs with a shader library to produce a shader blob that the Direct3D runtime can use</span></span>

<span data-ttu-id="2ae26-119">Nous allons ensuite créer une bibliothèque de nuanceur et lier les ressources des emplacements sources aux emplacements de destination.</span><span class="sxs-lookup"><span data-stu-id="2ae26-119">Next we make a shader library and bind resources from source slots to destination slots.</span></span>

[<span data-ttu-id="2ae26-120">Empaquetage d’une bibliothèque de nuanceur</span><span class="sxs-lookup"><span data-stu-id="2ae26-120">Packaging a shader library</span></span>](pachaging-a-shader-library.md)

## <a name="related-topics"></a><span data-ttu-id="2ae26-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2ae26-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2ae26-122">Guide de programmation pour HLSL</span><span class="sxs-lookup"><span data-stu-id="2ae26-122">Programming Guide for HLSL</span></span>](dx-graphics-hlsl-pguide.md)
</dt> <dt>

[<span data-ttu-id="2ae26-123">Graphismes Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="2ae26-123">Direct3D 11 Graphics</span></span>](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11)
</dt> <dt>

[<span data-ttu-id="2ae26-124">DXGI</span><span class="sxs-lookup"><span data-stu-id="2ae26-124">DXGI</span></span>](/windows/desktop/direct3ddxgi/dx-graphics-dxgi)
</dt> </dl>

 

 