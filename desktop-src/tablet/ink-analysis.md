---
description: Pour une application qui accepte l’écriture mixte et l’entrée de dessin, la possibilité de faire la distinction entre l’écriture manuscrite et le dessin et de regrouper l’écriture manuscrite en sous-catégories, telles que les segments de reconnaissance, les lignes et les paragraphes, est très utile.
ms.assetid: 17ce349c-10f3-4d9b-abb0-7af4f40bab32
title: Analyse des entrées manuscrites
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 021882d8f2de83b4bac9580ae66dd097bfd556db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104033868"
---
# <a name="ink-analysis"></a><span data-ttu-id="75376-103">Analyse des entrées manuscrites</span><span class="sxs-lookup"><span data-stu-id="75376-103">Ink Analysis</span></span>

<span data-ttu-id="75376-104">Pour une application qui accepte l’écriture mixte et l’entrée de dessin, la possibilité de faire la distinction entre l’écriture manuscrite et le dessin et de regrouper l’écriture manuscrite en sous-catégories, telles que les segments de reconnaissance, les lignes et les paragraphes, est très utile.</span><span class="sxs-lookup"><span data-stu-id="75376-104">For an application that accepts mixed handwriting and drawing input, the ability to distinguish between handwriting and drawing and to group handwriting into subcategories, such as recognition segments, lines, and paragraphs, is very useful.</span></span>

## <a name="ink-analysis-library"></a><span data-ttu-id="75376-105">Bibliothèque d’analyse d’encre</span><span class="sxs-lookup"><span data-stu-id="75376-105">Ink Analysis Library</span></span>

<span data-ttu-id="75376-106">Les API d’analyse d’encre combinent efficacement deux technologies distinctes mais complémentaires : la reconnaissance de l’écriture manuscrite et l’analyse de l’encre.</span><span class="sxs-lookup"><span data-stu-id="75376-106">The ink analysis APIs effectively combine two distinct but complimentary technologies: handwriting recognition and ink analyzing.</span></span> <span data-ttu-id="75376-107">La combinaison de ces deux technologies donne des résultats plus élevés que les parties.</span><span class="sxs-lookup"><span data-stu-id="75376-107">Combining these two technologies gives definitively greater results than the parts taken alone.</span></span>

<span data-ttu-id="75376-108">La reconnaissance de l’écriture manuscrite est l’analyse de calcul de l’encre numérique manuscrite pour retourner une interprétation basée sur des caractères dans une langue donnée.</span><span class="sxs-lookup"><span data-stu-id="75376-108">Handwriting recognition is the computational analysis of handwritten digital ink to return character-based interpretation in a given language.</span></span> <span data-ttu-id="75376-109">Autrement dit, la reconnaissance de l’écriture manuscrite indique comment l’ordinateur lit l’écriture manuscrite d’une personne.</span><span class="sxs-lookup"><span data-stu-id="75376-109">That is, handwriting recognition is how the computer "reads" a person's handwriting.</span></span>

<span data-ttu-id="75376-110">L’analyse de l’encre peut être divisée en une classification de l’encre et une analyse de la disposition.</span><span class="sxs-lookup"><span data-stu-id="75376-110">Ink analyzing can be further broken down into ink classification and layout analysis.</span></span> <span data-ttu-id="75376-111">La classification d’encre est la Division de calcul de l’encre en unités sémantiquement significatives, telles que les paragraphes, les lignes, les mots et les dessins.</span><span class="sxs-lookup"><span data-stu-id="75376-111">Ink classification is the computational division of ink into semantically meaningful units such as paragraphs, lines, words, and drawings.</span></span> <span data-ttu-id="75376-112">L’analyse de la disposition est l’examen de calcul de l’entrée d’encre pour déterminer la position de l’encre sur la surface d’encrage et la façon dont les traits sont liés l’un à l’autre de manière spatiale et même sémantique.</span><span class="sxs-lookup"><span data-stu-id="75376-112">Layout analysis is the computational examination of ink input to determine the position of the ink on the inking surface and how the strokes relate to each other spatially and even semantically.</span></span>

<span data-ttu-id="75376-113">Pour plus d’informations sur l’utilisation des API Ink analyse, consultez [vue d’ensemble](ink-analysis-overview.md)de l’analyse de l’encre.</span><span class="sxs-lookup"><span data-stu-id="75376-113">For details on how to use the Ink Analyis APIs, see [Ink Analysis Overview](ink-analysis-overview.md).</span></span>

 

 



