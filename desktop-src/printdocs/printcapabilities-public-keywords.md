---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: 7f08747f-f7ff-4381-b2b9-1917e4708ee3
title: Mots clés publics PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81d5e7b001a8106f95c830f0af5e99ee9821af64
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "106523760"
---
# <a name="printcapabilities-public-keywords"></a><span data-ttu-id="fc6ea-104">Mots clés publics PrintCapabilities</span><span class="sxs-lookup"><span data-stu-id="fc6ea-104">PrintCapabilities Public Keywords</span></span>

<span data-ttu-id="fc6ea-105">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="fc6ea-105">This topic is not current.</span></span> <span data-ttu-id="fc6ea-106">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="fc6ea-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="fc6ea-107">La section suivante spécifie les éléments configurables par l’utilisateur et les définitions de paramètres qui peuvent s’appliquer à un document PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="fc6ea-107">The following section specifies both user configurable elements and parameter definitions which may be applicable to a PrintCapabilities document.</span></span>

## <a name="user-configurable-elements-usage"></a><span data-ttu-id="fc6ea-108">Utilisation des éléments configurables par l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="fc6ea-108">User Configurable Elements Usage</span></span>

<span data-ttu-id="fc6ea-109">Les éléments configurables par l’utilisateur représentent les mots clés publics du schéma d’impression, qui peuvent apparaître dans un document PrintCapabilities ou un PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="fc6ea-109">User Configurable Elements represent Print Schema Public Keywords which may appear in either a PrintCapabilities document or a PrintTicket.</span></span> <span data-ttu-id="fc6ea-110">Ils sont destinés à représenter des attributs d’appareil configurables pris en charge par un appareil spécifique ou à communiquer des intentions de paramètres d’impression par une application ou un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="fc6ea-110">They are intended to represent configurable device attributes supported by a specific device or communicate print setting intent by an application or user.</span></span>

<span data-ttu-id="fc6ea-111">Les éléments configurables par l’utilisateur peuvent référencer des éléments de référence de paramètre.</span><span class="sxs-lookup"><span data-stu-id="fc6ea-111">User Configurable Elements may reference Parameter Reference Elements.</span></span> <span data-ttu-id="fc6ea-112">Pour plus d’informations, reportez-vous à la section [éléments de référence de paramètre](parameter-reference-elements.md) .</span><span class="sxs-lookup"><span data-stu-id="fc6ea-112">For more information, please refer to [Parameter Reference Elements](parameter-reference-elements.md) section.</span></span>

## <a name="parameter-definitions-usage"></a><span data-ttu-id="fc6ea-113">Utilisation des définitions de paramètres</span><span class="sxs-lookup"><span data-stu-id="fc6ea-113">Parameter Definitions Usage</span></span>

<span data-ttu-id="fc6ea-114">Les définitions de paramètres prennent la forme de types d’éléments ParameterDef dans un document de fonctionnalités d’impression.</span><span class="sxs-lookup"><span data-stu-id="fc6ea-114">Parameters definitions take the form of ParameterDef element types in a Print Capabilities document.</span></span> <span data-ttu-id="fc6ea-115">Les types d’éléments ParameterDef sont initialisés dans un PrintTicket à l’aide du type d’élément ParameterInit.</span><span class="sxs-lookup"><span data-stu-id="fc6ea-115">ParameterDef element types are initialized in a PrintTicket using the ParameterInit element type.</span></span> <span data-ttu-id="fc6ea-116">La valeur du paramètre est spécifiée à l’aide de l’élément ParameterInit.</span><span class="sxs-lookup"><span data-stu-id="fc6ea-116">The value of the parameter will be specified using the ParameterInit element.</span></span> <span data-ttu-id="fc6ea-117">Un mot clé configurable par l’utilisateur peut faire référence à une définition de paramètre à l’aide du type d’élément ParameterRef.</span><span class="sxs-lookup"><span data-stu-id="fc6ea-117">A user configurable keyword may reference a parameter definition using the ParameterRef element type.</span></span> <span data-ttu-id="fc6ea-118">Pour plus d’informations, consultez la section [constructions de paramètres](parameter-constructs.md) .</span><span class="sxs-lookup"><span data-stu-id="fc6ea-118">For more information, please refer to [Parameter Constructs](parameter-constructs.md) section.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fc6ea-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="fc6ea-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fc6ea-120">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="fc6ea-120">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



