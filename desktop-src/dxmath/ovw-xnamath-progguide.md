---
description: DirectXMath fournit une solution mathématique optimisée pour Windows.
ms.assetid: c2a64435-b2fb-3638-2eea-3ed52f4c7cd5
title: Guide de programmation DirectXMath
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df406787776f9fa5d1786e6ed6c5998e27a1c059
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517591"
---
# <a name="directxmath-programming-guide"></a><span data-ttu-id="c2836-103">Guide de programmation DirectXMath</span><span class="sxs-lookup"><span data-stu-id="c2836-103">DirectXMath programming guide</span></span>

<span data-ttu-id="c2836-104">DirectXMath fournit une solution mathématique optimisée pour Windows.</span><span class="sxs-lookup"><span data-stu-id="c2836-104">DirectXMath provides a math solution optimized for Windows.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="c2836-105">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="c2836-105">In this section</span></span>



| <span data-ttu-id="c2836-106">Rubrique</span><span class="sxs-lookup"><span data-stu-id="c2836-106">Topic</span></span>                                                             | <span data-ttu-id="c2836-107">Description</span><span class="sxs-lookup"><span data-stu-id="c2836-107">Description</span></span>                                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c2836-108">Prise en main</span><span class="sxs-lookup"><span data-stu-id="c2836-108">Getting Started</span></span>](pg-xnamath-getting-started.md)<br/>      | <span data-ttu-id="c2836-109">La bibliothèque DirectXMath implémente une interface optimale et portable pour les opérations algébriques arithmétiques et linéaires sur des vecteurs à virgule flottante simple précision (2D, 3D et 4D) ou des matrices (3 × 3 et 4 × 4).</span><span class="sxs-lookup"><span data-stu-id="c2836-109">The DirectXMath Library implements an optimal and portable interface for arithmetic and linear algebra operations on single-precision floating-point vectors (2D, 3D, and 4D) or matrices (3×3 and 4×4).</span></span> <br/>                                                    |
| [<span data-ttu-id="c2836-110">Nouveautés</span><span class="sxs-lookup"><span data-stu-id="c2836-110">What's New</span></span>](pg-xnamath-whatsnew.md)<br/>                  | <span data-ttu-id="c2836-111">La bibliothèque DirectXMath est basée sur la [bibliothèque XNA Math C++ SIMD version 2,04](https://walbourn.github.io/).</span><span class="sxs-lookup"><span data-stu-id="c2836-111">The DirectXMath library is based on the [XNA Math C++ SIMD library version 2.04](https://walbourn.github.io/).</span></span> <span data-ttu-id="c2836-112">Ici, nous décrivons comment DirectXMath diffère de XNA Math et comment les versions de DirectXMath diffèrent.</span><span class="sxs-lookup"><span data-stu-id="c2836-112">Here we describe how DirectXMath differs from XNA Math and how DirectXMath versions differ.</span></span> <br/> |
| [<span data-ttu-id="c2836-113">Migration de code</span><span class="sxs-lookup"><span data-stu-id="c2836-113">Code Migration</span></span>](pg-xnamath-migration.md)<br/>             | <span data-ttu-id="c2836-114">Cette vue d’ensemble décrit les modifications requises pour migrer le code existant à l’aide de la bibliothèque Math XNA vers la bibliothèque DirectXMath.</span><span class="sxs-lookup"><span data-stu-id="c2836-114">This overview describes the changes required to migrate existing code using the XNA Math library to the DirectXMath library.</span></span><br/>                                                                                                                                 |
| [<span data-ttu-id="c2836-115">Utilisation de D3DXMath</span><span class="sxs-lookup"><span data-stu-id="c2836-115">Working with D3DXMath</span></span>](pg-xnamath-migration-d3dx.md)<br/> | <span data-ttu-id="c2836-116">D3DXMath est une bibliothèque d’assistance mathématique pour les applications Direct3D.</span><span class="sxs-lookup"><span data-stu-id="c2836-116">D3DXMath is a math helper library for Direct3D applications.</span></span> <br/>                                                                                                                                                                                                |
| [<span data-ttu-id="c2836-117">Optimisation du code</span><span class="sxs-lookup"><span data-stu-id="c2836-117">Code Optimization</span></span>](pg-xnamath-optimizing.md)<br/>         | <span data-ttu-id="c2836-118">Cette rubrique décrit les considérations et les stratégies d’optimisation avec la bibliothèque DirectXMath.</span><span class="sxs-lookup"><span data-stu-id="c2836-118">This topic describes optimization considerations and strategies with the DirectXMath Library.</span></span><br/>                                                                                                                                                                |
| [<span data-ttu-id="c2836-119">Éléments internes de bibliothèque</span><span class="sxs-lookup"><span data-stu-id="c2836-119">Library Internals</span></span>](pg-xnamath-internals.md)<br/>          | <span data-ttu-id="c2836-120">Cette rubrique décrit la conception interne de la bibliothèque DirectXMath.</span><span class="sxs-lookup"><span data-stu-id="c2836-120">This topic describes the internal design of the DirectXMath library.</span></span><br/>                                                                                                                                                                                         |



 

## <a name="related-topics"></a><span data-ttu-id="c2836-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c2836-121">Related Topics</span></span>

<dl> <dt>

<span data-ttu-id="c2836-122"><span id="DirectXMath_Programming_Reference"></span><span id="directxmath_programming_reference"></span><span id="DIRECTXMATH_PROGRAMMING_REFERENCE"></span>[Informations de référence sur la programmation DirectXMath](ovw-xnamath-reference.md)</span><span class="sxs-lookup"><span data-stu-id="c2836-122"><span id="DirectXMath_Programming_Reference"></span><span id="directxmath_programming_reference"></span><span id="DIRECTXMATH_PROGRAMMING_REFERENCE"></span>[DirectXMath Programming Reference](ovw-xnamath-reference.md)</span></span>
<span data-ttu-id="c2836-123"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="c2836-123"></dt> <dd></dd> </dl></span></span>

## <a name="related-topics"></a><span data-ttu-id="c2836-124">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c2836-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c2836-125">DirectXMath</span><span class="sxs-lookup"><span data-stu-id="c2836-125">DirectXMath</span></span>](directxmath-portal.md)
</dt> </dl>

 

 




