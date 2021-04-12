---
title: Utilisation des évaluateurs
description: Utilisation des évaluateurs
ms.assetid: a5a99d0a-526e-4492-90c4-a6b9fdbdff16
keywords:
- OpenGL, évaluateurs
- évaluateurs OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1aef70a7a854e16cf4992d9dd44c4931ad4d044
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309642"
---
# <a name="using-evaluators"></a><span data-ttu-id="cd85d-105">Utilisation des évaluateurs</span><span class="sxs-lookup"><span data-stu-id="cd85d-105">Using Evaluators</span></span>

<span data-ttu-id="cd85d-106">Les fonctions de l’évaluateur OpenGL vous permettent d’utiliser un mappage polynomial pour produire des vertex, des normales, des coordonnées de texture et des couleurs.</span><span class="sxs-lookup"><span data-stu-id="cd85d-106">The OpenGL evaluator functions allow you to use a polynomial mapping to produce vertices, normals, texture coordinates, and colors.</span></span> <span data-ttu-id="cd85d-107">Ces valeurs calculées sont ensuite transmises au pipeline de traitement comme si elles avaient été spécifiées directement.</span><span class="sxs-lookup"><span data-stu-id="cd85d-107">These calculated values are then passed on to the processing pipeline as if they had been directly specified.</span></span> <span data-ttu-id="cd85d-108">Les fonctions de l’évaluateur sont également la base des fonctions NURBS (B-spline rationnelles non uniformes) qui vous permettent de définir des courbes et des surfaces, comme décrit dans Bibliothèque de l' [utilitaire OpenGL](opengl-utility-library.md).</span><span class="sxs-lookup"><span data-stu-id="cd85d-108">The evaluator functions are also the basis for the NURBS (Non-Uniform Rational B-Spline) functions, which allow you to define curves and surfaces, as described under [OpenGL Utility library](opengl-utility-library.md).</span></span>

<span data-ttu-id="cd85d-109">La première étape de l’utilisation des évaluateurs consiste à définir le mappage polynomial approprié à une ou deux dimensions à l’aide de [**glMap \***](glmap1.md).</span><span class="sxs-lookup"><span data-stu-id="cd85d-109">The first step in using evaluators is to define the appropriate one- or two-dimensional polynomial mapping using [**glMap\***](glmap1.md).</span></span> <span data-ttu-id="cd85d-110">Vous pouvez ensuite spécifier et évaluer les valeurs de domaine pour ce mappage de l’une des deux manières suivantes :</span><span class="sxs-lookup"><span data-stu-id="cd85d-110">You can then specify and evaluate the domain values for this map in one of two ways:</span></span>

-   <span data-ttu-id="cd85d-111">Définissez une série de valeurs de domaine uniformément espacées à mapper à l’aide de [**glMapGrid**](glmapgrid-functions.md) , puis évaluez un sous-ensemble rectangulaire de cette grille avec [**glEvalMesh**](glevalmesh-functions.md).</span><span class="sxs-lookup"><span data-stu-id="cd85d-111">Define a series of evenly spaced domain values to be mapped using [**glMapGrid**](glmapgrid-functions.md) and then evaluate a rectangular subset of that grid with [**glEvalMesh**](glevalmesh-functions.md).</span></span> <span data-ttu-id="cd85d-112">Un point unique de la grille peut être évalué à l’aide de [**glEvalPoint**](glevalpoint.md).</span><span class="sxs-lookup"><span data-stu-id="cd85d-112">A single point of the grid can be evaluated using [**glEvalPoint**](glevalpoint.md).</span></span>
-   <span data-ttu-id="cd85d-113">Spécifiez explicitement une valeur de domaine souhaitée comme argument, qui évalue les mappages à cette valeur.</span><span class="sxs-lookup"><span data-stu-id="cd85d-113">Explicitly specify a desired domain value as an argument, which evaluates the maps at that value.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cd85d-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="cd85d-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cd85d-115">Référence des évaluateurs</span><span class="sxs-lookup"><span data-stu-id="cd85d-115">Evaluators Reference</span></span>](evaluators-reference.md)
</dt> </dl>

 

 




