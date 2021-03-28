---
title: Format d’effet (Direct3D 11)
ms.assetid: c425f57b-fc14-46a5-bb65-a0a2305bd406
description: En savoir plus sur le format d’effet (Direct3D 11)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c08589fcb041591591d033b88e4fafe597e98520
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104200972"
---
# <a name="effect-format-direct3d-11"></a><span data-ttu-id="e6af6-103">Format d’effet (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="e6af6-103">Effect Format (Direct3D 11)</span></span>

<span data-ttu-id="e6af6-104">Un effet (qui est souvent stocké dans un fichier avec une extension de fichier. FX) déclare l’état du pipeline défini par un effet.</span><span class="sxs-lookup"><span data-stu-id="e6af6-104">An effect (which is often stored in a file with a .fx file extension) declares the pipeline state set by an effect.</span></span> <span data-ttu-id="e6af6-105">L’état de l’effet peut être divisé en trois catégories :</span><span class="sxs-lookup"><span data-stu-id="e6af6-105">Effect state can be roughly broken down into three categories:</span></span>

-   <span data-ttu-id="e6af6-106">[Variables](d3d11-effect-variable-syntax.md), qui sont généralement déclarées en haut d’un effet.</span><span class="sxs-lookup"><span data-stu-id="e6af6-106">[Variables](d3d11-effect-variable-syntax.md), which are usually declared at the top of an effect.</span></span>
-   <span data-ttu-id="e6af6-107">Les [fonctions](d3d11-effect-function-syntax.md), qui implémentent le code du nuanceur, ou sont utilisées comme fonctions d’assistance par d’autres fonctions.</span><span class="sxs-lookup"><span data-stu-id="e6af6-107">[Functions](d3d11-effect-function-syntax.md), which implement shader code, or are used as helper functions by other functions.</span></span>
-   <span data-ttu-id="e6af6-108">[Techniques](d3d11-effect-technique-syntax.md), qui peuvent être organisées en groupes d’effets, et implémenter des séquences de rendu à l’aide d’une ou de plusieurs passes d’effet.</span><span class="sxs-lookup"><span data-stu-id="e6af6-108">[Techniques](d3d11-effect-technique-syntax.md), which can be arranged in effect groups, and implement rendering sequences using one or more effect passes.</span></span> <span data-ttu-id="e6af6-109">Chaque passe définit un ou plusieurs [groupes d’États](d3d11-effect-states.md) et appelle des fonctions de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="e6af6-109">Each pass sets one or more [state groups](d3d11-effect-states.md) and calls shader functions.</span></span>

![diagramme des catégories de déclarations pour les effets, y compris les variables en haut, les fonctions en milieu et les techniques en bas](images/d3d10-effect-intro.png)

<span data-ttu-id="e6af6-111">Le diagramme précédent montre les catégories d’état d’effet.</span><span class="sxs-lookup"><span data-stu-id="e6af6-111">The preceding diagram shows the categories of effect state.</span></span>

<span data-ttu-id="e6af6-112">La définition du format binaire de l’effet se trouve dans le fichier binaire \\ EffectBinaryFormat. h dans le code source Effects.</span><span class="sxs-lookup"><span data-stu-id="e6af6-112">The definition of the effect binary format can be found in Binary\\EffectBinaryFormat.h in the effects source code.</span></span>


## <a name="in-this-section"></a><span data-ttu-id="e6af6-113">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="e6af6-113">In this section</span></span>



| <span data-ttu-id="e6af6-114">Rubrique</span><span class="sxs-lookup"><span data-stu-id="e6af6-114">Topic</span></span>                                                                   | <span data-ttu-id="e6af6-115">Description</span><span class="sxs-lookup"><span data-stu-id="e6af6-115">Description</span></span>                                                                                                          |
|-------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e6af6-116">Syntaxe de la variable Effect</span><span class="sxs-lookup"><span data-stu-id="e6af6-116">Effect Variable Syntax</span></span>](d3d11-effect-variable-syntax.md)<br/>   | <span data-ttu-id="e6af6-117">Une variable Effect est déclarée avec la syntaxe décrite dans cette section.</span><span class="sxs-lookup"><span data-stu-id="e6af6-117">An effect variable is declared with the syntax described in this section.</span></span><br/>                                 |
| [<span data-ttu-id="e6af6-118">Syntaxe d’annotation</span><span class="sxs-lookup"><span data-stu-id="e6af6-118">Annotation Syntax</span></span>](d3d11-effect-annotation-syntax.md)<br/>      | <span data-ttu-id="e6af6-119">Une annotation est une information définie par l’utilisateur, déclarée avec la syntaxe décrite dans cette section.</span><span class="sxs-lookup"><span data-stu-id="e6af6-119">An annotation is a user-defined piece of information, declared with the syntax described in this section.</span></span><br/> |
| [<span data-ttu-id="e6af6-120">Syntaxe des fonctions Effect</span><span class="sxs-lookup"><span data-stu-id="e6af6-120">Effect Function Syntax</span></span>](d3d11-effect-function-syntax.md)<br/>   | <span data-ttu-id="e6af6-121">Une fonction Effect est écrite en langage HLSL et est déclarée avec la syntaxe décrite dans cette section.</span><span class="sxs-lookup"><span data-stu-id="e6af6-121">An effect function is written in HLSL and is declared with the syntax described in this section.</span></span><br/>          |
| [<span data-ttu-id="e6af6-122">Syntaxe de la technique Effect</span><span class="sxs-lookup"><span data-stu-id="e6af6-122">Effect Technique Syntax</span></span>](d3d11-effect-technique-syntax.md)<br/> | <span data-ttu-id="e6af6-123">Une technique d’effet est déclarée avec la syntaxe décrite dans cette section.</span><span class="sxs-lookup"><span data-stu-id="e6af6-123">An effect technique is declared with the syntax described in this section.</span></span><br/>                                |
| [<span data-ttu-id="e6af6-124">Groupes d’États d’effet</span><span class="sxs-lookup"><span data-stu-id="e6af6-124">Effect State Groups</span></span>](d3d11-effect-states.md)<br/>               | <span data-ttu-id="e6af6-125">Les États d’effet sont des paires nom-valeur sous la forme d’une expression.</span><span class="sxs-lookup"><span data-stu-id="e6af6-125">Effect states are name value pairs in the form of an expression.</span></span><br/>                                          |
| [<span data-ttu-id="e6af6-126">Syntaxe de groupe d’effets</span><span class="sxs-lookup"><span data-stu-id="e6af6-126">Effect Group Syntax</span></span>](d3d11-effect-group-syntax.md)<br/>         | <span data-ttu-id="e6af6-127">Un groupe d’effets est déclaré avec la syntaxe décrite dans cette section.</span><span class="sxs-lookup"><span data-stu-id="e6af6-127">An effect group is declared with the syntax described in this section.</span></span><br/>                                    |



 

## <a name="related-topics"></a><span data-ttu-id="e6af6-128">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e6af6-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e6af6-129">Informations de référence sur Effects 11</span><span class="sxs-lookup"><span data-stu-id="e6af6-129">Effects 11 Reference</span></span>](d3d11-graphics-reference-effects11.md)
</dt> </dl>

 

 





