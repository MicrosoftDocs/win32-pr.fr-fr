---
title: Variables d’État OpenGL
description: Les rubriques suivantes répertorient les noms des variables d’État qui peuvent être interrogées.
ms.assetid: f4bc4ec1-a529-4b9e-84af-94caa0ef7131
keywords:
- Variables d’État OpenGL
- variables d’État, OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36dee51ba7726277832d94eaf336d03d3c579189
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106536059"
---
# <a name="opengl-state-variables"></a><span data-ttu-id="6ba17-105">Variables d’État OpenGL</span><span class="sxs-lookup"><span data-stu-id="6ba17-105">OpenGL State Variables</span></span>

<span data-ttu-id="6ba17-106">Les rubriques suivantes répertorient les noms des variables d’État qui peuvent être interrogées :</span><span class="sxs-lookup"><span data-stu-id="6ba17-106">The following topics list the names of state variables that can be queried:</span></span>

-   [<span data-ttu-id="6ba17-107">**Variables d’État pour les valeurs actuelles et les données associées**</span><span class="sxs-lookup"><span data-stu-id="6ba17-107">**State Variables for Current Values and Associated Data**</span></span>](state-variables-for-current-values-and-associated-data.md)
-   [<span data-ttu-id="6ba17-108">**Variables d’état de transformation**</span><span class="sxs-lookup"><span data-stu-id="6ba17-108">**Transformation State Variables**</span></span>](transformation-state-variables.md)
-   [<span data-ttu-id="6ba17-109">**Variables d’état de coloration**</span><span class="sxs-lookup"><span data-stu-id="6ba17-109">**Coloring State Variables**</span></span>](coloring-state-variables.md)
-   [<span data-ttu-id="6ba17-110">**Variables d’état d’éclairage**</span><span class="sxs-lookup"><span data-stu-id="6ba17-110">**Lighting State Variables**</span></span>](lighting-state-variables.md)
-   [<span data-ttu-id="6ba17-111">**Variables d’état de pixellisation**</span><span class="sxs-lookup"><span data-stu-id="6ba17-111">**Rasterization State Variables**</span></span>](rasterization-state-variables.md)
-   [<span data-ttu-id="6ba17-112">**Variables d’état de texturation**</span><span class="sxs-lookup"><span data-stu-id="6ba17-112">**Texturing State Variables**</span></span>](texturing-state-variables.md)
-   [<span data-ttu-id="6ba17-113">**Opérations de pixel**</span><span class="sxs-lookup"><span data-stu-id="6ba17-113">**Pixel Operations**</span></span>](pixel-operations.md)
-   [<span data-ttu-id="6ba17-114">**Variables d’état de contrôle trame**</span><span class="sxs-lookup"><span data-stu-id="6ba17-114">**Framebuffer Control State Variables**</span></span>](framebuffer-control-state-variables.md)
-   [<span data-ttu-id="6ba17-115">**Variables d’état de pixel**</span><span class="sxs-lookup"><span data-stu-id="6ba17-115">**Pixel State Variables**</span></span>](pixel-state-variables.md)
-   [<span data-ttu-id="6ba17-116">**Variables d’état de l’évaluateur**</span><span class="sxs-lookup"><span data-stu-id="6ba17-116">**Evaluator State Variables**</span></span>](evaluator-state-variables.md)
-   [<span data-ttu-id="6ba17-117">**Variables d’état d’indicateur**</span><span class="sxs-lookup"><span data-stu-id="6ba17-117">**Hint State Variables**</span></span>](hint-state-variables.md)
-   [<span data-ttu-id="6ba17-118">**Variables d’État dépendantes de l’implémentation**</span><span class="sxs-lookup"><span data-stu-id="6ba17-118">**Implementation-Dependent State Variables**</span></span>](implementation-dependent-state-variables.md)
-   [<span data-ttu-id="6ba17-119">**Variables d’état de Pixel-Depth dépendant de l’implémentation**</span><span class="sxs-lookup"><span data-stu-id="6ba17-119">**Implementation-Dependent Pixel-Depth State Variables**</span></span>](implementation-dependent-pixel-depth-state-variables.md)
-   [<span data-ttu-id="6ba17-120">**Variables d’État diverses**</span><span class="sxs-lookup"><span data-stu-id="6ba17-120">**Miscellaneous State Variables**</span></span>](miscellaneous-state-variables.md)

<span data-ttu-id="6ba17-121">Pour chaque variable, la rubrique répertorie une description, un groupe d’attributs, une valeur initiale ou minimale et la fonction [**glGet \***](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) suggérée à utiliser pour l’obtenir.</span><span class="sxs-lookup"><span data-stu-id="6ba17-121">For each variable, the topic lists a description, attribute group, initial or minimum value, and the suggested [**glGet\***](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) function to use for obtaining it.</span></span>

<span data-ttu-id="6ba17-122">Les variables d’État que vous pouvez obtenir à l’aide de [**glGetBooleanv**](glgetbooleanv.md), [**glGetIntegerv**](glgetintegerv.md), [**glGetFloatv**](glgetfloatv.md)ou [**glGetDoublev**](glgetdoublev.md) sont répertoriées avec simplement l’une de ces functionsthe qui est la plus appropriée pour le type de données à retourner.</span><span class="sxs-lookup"><span data-stu-id="6ba17-122">State variables that you can obtain using [**glGetBooleanv**](glgetbooleanv.md), [**glGetIntegerv**](glgetintegerv.md), [**glGetFloatv**](glgetfloatv.md), or [**glGetDoublev**](glgetdoublev.md) are listed with just one of these functionsthe one that is most appropriate for the type of data to be returned.</span></span> <span data-ttu-id="6ba17-123">Vous ne pouvez pas obtenir ces variables d’État à l’aide de [**glIsEnabled**](glisenabled.md).</span><span class="sxs-lookup"><span data-stu-id="6ba17-123">You cannot obtain these state variables using [**glIsEnabled**](glisenabled.md).</span></span> <span data-ttu-id="6ba17-124">Toutefois, vous pouvez obtenir des variables d’État pour lesquelles **glIsEnabled** est listé comme fonction de requête avec **glGetBooleanv**, **glGetIntegerv**, **glGetFloatv** et **glGetDoublev**.</span><span class="sxs-lookup"><span data-stu-id="6ba17-124">However, you can obtain state variables for which **glIsEnabled** is listed as the query function with **glGetBooleanv**, **glGetIntegerv**, **glGetFloatv**, and **glGetDoublev**.</span></span> <span data-ttu-id="6ba17-125">Vous pouvez obtenir des variables d’État pour lesquelles toute autre fonction est listée en tant que fonction de requête uniquement à l’aide de cette fonction.</span><span class="sxs-lookup"><span data-stu-id="6ba17-125">You can obtain state variables for which any other function is listed as the query function only by using that function.</span></span> <span data-ttu-id="6ba17-126">Si aucun groupe d’attributs n’est listé, la variable n’appartient à aucun groupe.</span><span class="sxs-lookup"><span data-stu-id="6ba17-126">If no attribute group is listed, the variable doesn't belong to any group.</span></span> <span data-ttu-id="6ba17-127">Toutes les variables d’État que vous pouvez interroger, à l’exception de celles qui sont dépendantes de l’implémentation, ont des valeurs initiales.</span><span class="sxs-lookup"><span data-stu-id="6ba17-127">All state variables that you can query, except those that are implementation dependent, have initial values.</span></span> <span data-ttu-id="6ba17-128">Pour déterminer la valeur initiale d’une variable pour laquelle aucune valeur initiale n’est indiquée, consultez la référence de cette variable ou la</span><span class="sxs-lookup"><span data-stu-id="6ba17-128">To determine the initial value of a variable for which no initial value is listed, see that variable's reference or the</span></span>

<span data-ttu-id="6ba17-129">*Manuel de référence OpenGL*.</span><span class="sxs-lookup"><span data-stu-id="6ba17-129">*OpenGL Reference Manual*.</span></span>

 

 




