---
description: En savoir plus sur les définitions de paramètres dans un document PrintCapabilities. Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: 82ba4658-f0e1-47a7-bb0c-1b527fabde4a
title: Définitions de paramètres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4dc8ad2bed3a972202bc0a5bb07cbdd4ef9d8f44
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396574"
---
# <a name="parameter-definitions"></a><span data-ttu-id="9275d-105">Définitions de paramètres</span><span class="sxs-lookup"><span data-stu-id="9275d-105">Parameter Definitions</span></span>

<span data-ttu-id="9275d-106">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="9275d-106">This topic is not current.</span></span> <span data-ttu-id="9275d-107">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="9275d-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="9275d-108">Cette section décrit les définitions de paramètres publics qui peuvent apparaître dans un document PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="9275d-108">This section outlines the public parameter definitions which may appear in either a PrintCapabilities document.</span></span>

<span data-ttu-id="9275d-109">Les paramètres sont utilisés pour décrire une plage acceptable de valeurs, plutôt qu’une énumération discrète de valeurs.</span><span class="sxs-lookup"><span data-stu-id="9275d-109">Parameters are used to describe an acceptable range of values, rather than a discrete enumeration of values.</span></span>

## <a name="parameterdef"></a><span data-ttu-id="9275d-110">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="9275d-110">ParameterDef</span></span>

<span data-ttu-id="9275d-111">Pour obtenir un résumé du type d’élément ParameterDef, reportez-vous à la section [ParameterDef](parameterdef.md) .</span><span class="sxs-lookup"><span data-stu-id="9275d-111">For a summary of the ParameterDef element type, please refer to [ParameterDef](parameterdef.md) section.</span></span>

<span data-ttu-id="9275d-112">Pour plus d’informations sur l’interaction entre les éléments ParameterDef et les éléments ParameterInit, reportez-vous à la section [éléments ParameterDef et ParameterInit](./parameterdef-and-parameterinit-elements.md) .</span><span class="sxs-lookup"><span data-stu-id="9275d-112">For more information on the interaction between ParameterDef elements and ParameterInit elements, refer to [ParameterDef and ParameterInit Elements](./parameterdef-and-parameterinit-elements.md) section.</span></span>

<span data-ttu-id="9275d-113">Les éléments ParameterDef définis dans les mots clés du schéma d’impression doivent être entièrement définis dans un document PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="9275d-113">ParameterDef elements that are defined in the Print Schema Keywords must be fully defined in a PrintCapabilities document.</span></span>

## <a name="parameterref"></a><span data-ttu-id="9275d-114">ParameterRef</span><span class="sxs-lookup"><span data-stu-id="9275d-114">ParameterRef</span></span>

<span data-ttu-id="9275d-115">Pour obtenir un résumé du type d’élément ParameterRef, reportez-vous à la section [ParameterRef](parameterref.md) .</span><span class="sxs-lookup"><span data-stu-id="9275d-115">For a summary of the ParameterRef element type, please refer to [ParameterRef](parameterref.md) section.</span></span>

<span data-ttu-id="9275d-116">Un mot clé d’élément configurable par l’utilisateur peut contenir une référence à un paramètre.</span><span class="sxs-lookup"><span data-stu-id="9275d-116">A user configurable element keyword may contain a reference to a Parameter.</span></span> <span data-ttu-id="9275d-117">Les éléments ParameterRef sont spécifiés en tant qu’enfants d’un élément ScoredProperty. pour plus d’informations, consultez la section [éléments de référence de paramètre](parameter-reference-elements.md) .</span><span class="sxs-lookup"><span data-stu-id="9275d-117">ParameterRef elements are specified as a child of a ScoredProperty element For more information, please refer to [Parameter Reference Elements](parameter-reference-elements.md) section.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9275d-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9275d-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9275d-119">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="9275d-119">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 
