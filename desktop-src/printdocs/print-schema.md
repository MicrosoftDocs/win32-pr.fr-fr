---
description: Cette vue d’ensemble décrit le schéma d’impression et les liens vers les rubriques de référence du schéma d’impression. Le schéma d’impression comprend les mots clés du schéma d’impression et le Framework.
ms.assetid: d746bdd1-96c2-41f5-ad99-0b51c8ee8731
title: Référence du schéma d’impression hérité
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81a8f417d20913563cfd4a52ba51d21b516e73f0
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407132"
---
# <a name="legacy-print-schema-reference"></a><span data-ttu-id="9881a-104">Référence du schéma d’impression hérité</span><span class="sxs-lookup"><span data-stu-id="9881a-104">Legacy Print Schema Reference</span></span>

<span data-ttu-id="9881a-105">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="9881a-105">This topic is not current.</span></span> <span data-ttu-id="9881a-106">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="9881a-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="9881a-107">Le schéma d’impression et les technologies associées sont disponibles dans le Microsoft .NET Framework 3,0, Microsoft Windows Vista et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="9881a-107">The Print Schema and related technologies are available in the Microsoft .NET Framework 3.0, Microsoft Windows Vista, and later releases.</span></span>

<span data-ttu-id="9881a-108">Le schéma d’impression fournit un format XML pour l’expression et l’organisation d’un grand ensemble de propriétés qui décrivent un format de travail ou PrintCapabilities de manière hiérarchique.</span><span class="sxs-lookup"><span data-stu-id="9881a-108">The Print Schema provides an XML-based format for expressing and organizing a large set of properties that describe either a job format or PrintCapabilities in a hierarchically structured manner.</span></span>

<span data-ttu-id="9881a-109">Le schéma d’impression est un terme générique qui comprend deux composants : les mots clés du schéma d’impression et l’infrastructure du schéma d’impression.</span><span class="sxs-lookup"><span data-stu-id="9881a-109">The Print Schema is an umbrella term that includes two components, the Print Schema Keywords and the Print Schema Framework.</span></span> <span data-ttu-id="9881a-110">Le document des mots clés du schéma d’impression est un schéma public qui définit un ensemble d’instances d’éléments qui peuvent être utilisées pour décrire les attributs des appareils et la mise en forme du travail d’impression.</span><span class="sxs-lookup"><span data-stu-id="9881a-110">The Print Schema Keywords document is a public schema that defines a set of element instances that can be used to describe device attributes and print job formatting.</span></span> <span data-ttu-id="9881a-111">L’infrastructure du schéma d’impression est un schéma public qui définit une collection hiérarchique de types d’éléments XML et spécifie la manière dont les types d’éléments peuvent être utilisés ensemble.</span><span class="sxs-lookup"><span data-stu-id="9881a-111">The Print Schema Framework is a public schema that defines a hierarchically structured collection of XML element types, and specifies how the element types can be used together.</span></span>

<span data-ttu-id="9881a-112">Les mots clés du schéma d’impression et l’infrastructure du schéma d’impression constituent la base de deux technologies liées au schéma d’impression, du schéma PrintCapabilities et du schéma PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="9881a-112">The Print Schema Keywords and the Print Schema Framework form the foundation for two Print Schema-related technologies, the PrintCapabilities Schema, and the PrintTicket Schema.</span></span>

<span data-ttu-id="9881a-113">Il est important de garder à l’esprit que l’un des objectifs du schéma d’impression est de prendre en charge les extensions de schéma par les fournisseurs.</span><span class="sxs-lookup"><span data-stu-id="9881a-113">It is important to keep in mind that one of the goals of the Print Schema is to support schema extensions by providers.</span></span> <span data-ttu-id="9881a-114">Autrement dit, les fournisseurs ne sont pas limités à l’utilisation uniquement des instances de propriété, de fonctionnalité, d’option ou de ParameterInit définies dans les mots clés du schéma d’impression dans les technologies basées sur l’infrastructure du schéma d’impression.</span><span class="sxs-lookup"><span data-stu-id="9881a-114">That is, providers are not restricted to using only those Property, Feature, Option, or ParameterInit instances defined in the Print Schema Keywords in the technologies built on the Print Schema Framework.</span></span> <span data-ttu-id="9881a-115">Les instances d’éléments spécifiques au fournisseur peuvent être disséminées librement dans des instances d’élément définies dans les mots clés du schéma d’impression.</span><span class="sxs-lookup"><span data-stu-id="9881a-115">Provider-specific element instances may be freely interspersed within element instances defined in the Print Schema Keywords.</span></span> <span data-ttu-id="9881a-116">La seule exigence est que les instances de propriétés spécifiques au fournisseur (c’est-à-dire, privées) doivent appartenir à un espace de noms qui est clairement associé au fournisseur.</span><span class="sxs-lookup"><span data-stu-id="9881a-116">The only requirement is that provider-specific (that is, private) Property instances must belong to a namespace that is clearly associated with the provider.</span></span>

-   [<span data-ttu-id="9881a-117">Arrière-plan du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="9881a-117">Print Schema Background</span></span>](print-schema-background.md)

-   [<span data-ttu-id="9881a-118">Imprimer des technologies Schema-Related</span><span class="sxs-lookup"><span data-stu-id="9881a-118">Print Schema-Related Technologies</span></span>](print-schema-related-technologies.md)

-   [<span data-ttu-id="9881a-119">Termes utilisés dans le schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="9881a-119">Terms Used in the Print Schema</span></span>](terms-used-in-the-print-schema.md)

-   [<span data-ttu-id="9881a-120">Syntaxe du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="9881a-120">Syntax of the Print Schema</span></span>](syntax-of-the-print-schema.md)

-   [<span data-ttu-id="9881a-121">Résumé des types d’éléments</span><span class="sxs-lookup"><span data-stu-id="9881a-121">Summary of Element Types</span></span>](summary-of-element-types.md)

-   [<span data-ttu-id="9881a-122">Structure du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="9881a-122">Print Schema Framework</span></span>](print-schema-framework.md)

-   [<span data-ttu-id="9881a-123">Mots clés publics du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="9881a-123">Print Schema Public Keywords</span></span>](print-schema-public-keywords.md)

-   [<span data-ttu-id="9881a-124">Schéma PrintCapabilities et construction de document</span><span class="sxs-lookup"><span data-stu-id="9881a-124">PrintCapabilities Schema and Document Construction</span></span>](printcapabilities-schema-and-document-construction.md)

-   [<span data-ttu-id="9881a-125">Schéma PrintTicket et construction de document</span><span class="sxs-lookup"><span data-stu-id="9881a-125">PrintTicket Schema and Document Construction</span></span>](printticket-schema-and-document-construction.md)

## <a name="related-topics"></a><span data-ttu-id="9881a-126">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9881a-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9881a-127">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="9881a-127">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



