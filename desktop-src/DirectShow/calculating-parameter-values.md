---
description: Calcul des valeurs de paramètre
ms.assetid: cc3c26ed-a007-4350-99be-0ebd94953689
title: Calcul des valeurs de paramètre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89dac0767d7d19bc4331e1a9ee032ec5b3eaae2e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106513290"
---
# <a name="calculating-parameter-values"></a><span data-ttu-id="2aa04-103">Calcul des valeurs de paramètre</span><span class="sxs-lookup"><span data-stu-id="2aa04-103">Calculating Parameter Values</span></span>

<span data-ttu-id="2aa04-104">Éventuellement, une mémoire tampon d’entrée peut être très volumineuse.</span><span class="sxs-lookup"><span data-stu-id="2aa04-104">Potentially, an input buffer could be very large.</span></span> <span data-ttu-id="2aa04-105">Dans l’idéal, lorsque DMO traite la mémoire tampon, les paramètres suivent exactement leurs courbes dans tout le lot de données.</span><span class="sxs-lookup"><span data-stu-id="2aa04-105">Ideally, when the DMO processes the buffer, the parameters will exactly follow their curves throughout the entire batch of data.</span></span> <span data-ttu-id="2aa04-106">Toutefois, un DMO a une certaine liberté dans la manière dont il calcule ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="2aa04-106">However, a DMO has some leeway in how it calculates those values.</span></span>

-   <span data-ttu-id="2aa04-107">L’approche la plus précise consiste à calculer la valeur exacte pour chaque unité atomique de données ; par exemple, chaque exemple audio.</span><span class="sxs-lookup"><span data-stu-id="2aa04-107">The most accurate approach is to calculate the exact value for every atomic unit of data; for example, each audio sample.</span></span> <span data-ttu-id="2aa04-108">Cette approche est la plus coûteuse en termes de calcul.</span><span class="sxs-lookup"><span data-stu-id="2aa04-108">This approach is the most computationally expensive.</span></span>
-   <span data-ttu-id="2aa04-109">Une autre approche consiste à découper les données en unités plus petites de taille fixe, comme les exemples 100.</span><span class="sxs-lookup"><span data-stu-id="2aa04-109">Another approach is to slice the data into smaller units of some fixed size, such as 100 samples.</span></span> <span data-ttu-id="2aa04-110">Cette approche crée un effet « escalier-Stepping ».</span><span class="sxs-lookup"><span data-stu-id="2aa04-110">This approach creates a "stair-stepping" effect.</span></span> <span data-ttu-id="2aa04-111">Pour certains paramètres, cela peut être acceptable.</span><span class="sxs-lookup"><span data-stu-id="2aa04-111">For some parameters, that might be acceptable.</span></span> <span data-ttu-id="2aa04-112">Dans les effets audio, il peut créer des artefacts sonores.</span><span class="sxs-lookup"><span data-stu-id="2aa04-112">In audio effects, it might create audible artifacts.</span></span>
-   <span data-ttu-id="2aa04-113">Un compromis consiste à utiliser la technique précédente, mais au sein de chaque lot, effectuer une interpolation linéaire de la valeur de paramètre pour chaque exemple.</span><span class="sxs-lookup"><span data-stu-id="2aa04-113">A compromise is to use the previous technique, but within each batch, perform a linear interpolation of the parameter value for each sample.</span></span>

<span data-ttu-id="2aa04-114">Ces problèmes sont particulièrement importants pour le traitement audio.</span><span class="sxs-lookup"><span data-stu-id="2aa04-114">These issues are especially important for audio processing.</span></span> <span data-ttu-id="2aa04-115">Une seconde d’audio peut contenir des échantillons audio 48 000 par canal, ce qui représente un grand nombre de calculs à effectuer, mais l’oreille est sensible aux artefacts tels que les alias.</span><span class="sxs-lookup"><span data-stu-id="2aa04-115">One second of audio might contain 48,000 audio samples per channel, which is a lot of calculations to perform, yet the ear is sensitive to artifacts such as aliasing.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2aa04-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2aa04-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2aa04-117">Paramètres de média</span><span class="sxs-lookup"><span data-stu-id="2aa04-117">Media Parameters</span></span>](media-parameters.md)
</dt> </dl>

 

 



