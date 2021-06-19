---
description: En savoir plus sur les éléments ParameterRef dans l’infrastructure du schéma d’impression. Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: 78df6acf-eb4e-46c1-bf1d-c0a99cf49bff
title: Éléments ParameterRef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2935317bc4107e2071911ab1df826426b2bcec17
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396524"
---
# <a name="parameterref-elements"></a><span data-ttu-id="5404f-105">Éléments ParameterRef</span><span class="sxs-lookup"><span data-stu-id="5404f-105">ParameterRef Elements</span></span>

<span data-ttu-id="5404f-106">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="5404f-106">This topic is not current.</span></span> <span data-ttu-id="5404f-107">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="5404f-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="5404f-108">Les éléments ParameterRef s’appliquent spécifiquement aux éléments option, ce qui permet à cet élément d’option de faire référence à un élément ParameterDef particulier.</span><span class="sxs-lookup"><span data-stu-id="5404f-108">ParameterRef elements specifically apply to Option elements, allowing the ability for that Option element to refer to a particular ParameterDef element.</span></span> <span data-ttu-id="5404f-109">Pour ces éléments d’option, un élément ScoredProperty qui caractérise l’option n’est pas codé en dur dans le document PrintCapabilities en tant que valeur, mais est plutôt variable.</span><span class="sxs-lookup"><span data-stu-id="5404f-109">For these Option elements, a ScoredProperty element that characterizes the Option is not hard-coded in the PrintCapabilities document as a Value, but instead is variable.</span></span> <span data-ttu-id="5404f-110">Pour activer cette variabilité, ces éléments ScoredProperty contiennent un élément ParameterRef.</span><span class="sxs-lookup"><span data-stu-id="5404f-110">To enable this variability, these ScoredProperty elements contain a ParameterRef element.</span></span> <span data-ttu-id="5404f-111">Un élément ScoredProperty ne peut pas contenir à la fois un élément Value et un élément ParameterRef.</span><span class="sxs-lookup"><span data-stu-id="5404f-111">A ScoredProperty element may not contain both a Value element and a ParameterRef element.</span></span> <span data-ttu-id="5404f-112">Les éléments option contenant un ou plusieurs éléments ParameterRef sont appelés éléments d’option paramétrables.</span><span class="sxs-lookup"><span data-stu-id="5404f-112">Option elements containing one or more ParameterRef elements are called parameterized Option elements.</span></span>

<span data-ttu-id="5404f-113">L’infrastructure du schéma d’impression permet à un élément d’option de contenir un nombre quelconque d’éléments ScoredProperty qui font référence à des éléments de paramètres, ainsi que n’importe quel nombre d’éléments ScoredProperty qui contiennent des éléments de valeur.</span><span class="sxs-lookup"><span data-stu-id="5404f-113">The Print Schema Framework allows an Option element to contain any number of ScoredProperty elements that refer to Parameter elements, together with any number of ScoredProperty elements that contain Value elements.</span></span> <span data-ttu-id="5404f-114">L’infrastructure permet également à un nombre quelconque d’éléments de fonctionnalité de contenir des éléments d’option paramétrés, et un nombre quelconque d’éléments d’option paramétrables sont autorisés pour chaque élément de fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="5404f-114">The Framework also allows any number of Feature elements to contain parameterized Option elements, and any number of parameterized Option elements are permitted for each Feature element.</span></span> <span data-ttu-id="5404f-115">En outre, la même construction de paramètre peut être référencée par plusieurs éléments d’option différents, des éléments d’option qui peuvent appartenir à des éléments de fonctionnalité identiques ou différents.</span><span class="sxs-lookup"><span data-stu-id="5404f-115">Also, the same parameter construct can be referred to by several different Option elements, Option elements that can belong to the same or different Feature elements.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5404f-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5404f-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5404f-117">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="5404f-117">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



