---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: 82ba4658-f0e1-47a7-bb0c-1b527fabde4a
title: Définitions de paramètres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca5a71bfc5a5111a826b5d221ff1436ecf921dd2
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "104211315"
---
# <a name="parameter-definitions"></a><span data-ttu-id="662ee-104">Définitions de paramètres</span><span class="sxs-lookup"><span data-stu-id="662ee-104">Parameter Definitions</span></span>

<span data-ttu-id="662ee-105">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="662ee-105">This topic is not current.</span></span> <span data-ttu-id="662ee-106">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="662ee-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="662ee-107">Cette section décrit les définitions de paramètres publics qui peuvent apparaître dans un document PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="662ee-107">This section outlines the public parameter definitions which may appear in either a PrintCapabilities document.</span></span>

<span data-ttu-id="662ee-108">Les paramètres sont utilisés pour décrire une plage acceptable de valeurs, plutôt qu’une énumération discrète de valeurs.</span><span class="sxs-lookup"><span data-stu-id="662ee-108">Parameters are used to describe an acceptable range of values, rather than a discrete enumeration of values.</span></span>

## <a name="parameterdef"></a><span data-ttu-id="662ee-109">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="662ee-109">ParameterDef</span></span>

<span data-ttu-id="662ee-110">Pour obtenir un résumé du type d’élément ParameterDef, reportez-vous à la section [ParameterDef](parameterdef.md) .</span><span class="sxs-lookup"><span data-stu-id="662ee-110">For a summary of the ParameterDef element type, please refer to [ParameterDef](parameterdef.md) section.</span></span>

<span data-ttu-id="662ee-111">Pour plus d’informations sur l’interaction entre les éléments ParameterDef et les éléments ParameterInit, reportez-vous à la section [éléments ParameterDef et ParameterInit](./parameterdef-and-parameterinit-elements.md) .</span><span class="sxs-lookup"><span data-stu-id="662ee-111">For more information on the interaction between ParameterDef elements and ParameterInit elements, refer to [ParameterDef and ParameterInit Elements](./parameterdef-and-parameterinit-elements.md) section.</span></span>

<span data-ttu-id="662ee-112">Les éléments ParameterDef définis dans les mots clés du schéma d’impression doivent être entièrement définis dans un document PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="662ee-112">ParameterDef elements that are defined in the Print Schema Keywords must be fully defined in a PrintCapabilities document.</span></span>

## <a name="parameterref"></a><span data-ttu-id="662ee-113">ParameterRef</span><span class="sxs-lookup"><span data-stu-id="662ee-113">ParameterRef</span></span>

<span data-ttu-id="662ee-114">Pour obtenir un résumé du type d’élément ParameterRef, reportez-vous à la section [ParameterRef](parameterref.md) .</span><span class="sxs-lookup"><span data-stu-id="662ee-114">For a summary of the ParameterRef element type, please refer to [ParameterRef](parameterref.md) section.</span></span>

<span data-ttu-id="662ee-115">Un mot clé d’élément configurable par l’utilisateur peut contenir une référence à un paramètre.</span><span class="sxs-lookup"><span data-stu-id="662ee-115">A user configurable element keyword may contain a reference to a Parameter.</span></span> <span data-ttu-id="662ee-116">Les éléments ParameterRef sont spécifiés en tant qu’enfants d’un élément ScoredProperty. pour plus d’informations, consultez la section [éléments de référence de paramètre](parameter-reference-elements.md) .</span><span class="sxs-lookup"><span data-stu-id="662ee-116">ParameterRef elements are specified as a child of a ScoredProperty element For more information, please refer to [Parameter Reference Elements](parameter-reference-elements.md) section.</span></span>

## <a name="related-topics"></a><span data-ttu-id="662ee-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="662ee-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="662ee-118">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="662ee-118">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 
