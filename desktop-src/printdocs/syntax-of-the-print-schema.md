---
description: En savoir plus sur la syntaxe du schéma d’impression, exprimée en syntaxe XML, et composée d’un petit nombre de types d’éléments.
ms.assetid: d67518e3-c379-4a50-aeda-31afaa7f05dd
title: Syntaxe du schéma d’impression
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ef52dbdbdfacc2d3cc947b46558319577a75b1b
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405292"
---
# <a name="syntax-of-the-print-schema"></a><span data-ttu-id="c0729-103">Syntaxe du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="c0729-103">Syntax of the Print Schema</span></span>

<span data-ttu-id="c0729-104">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="c0729-104">This topic is not current.</span></span> <span data-ttu-id="c0729-105">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="c0729-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="c0729-106">Le schéma d’impression est exprimé en syntaxe XML.</span><span class="sxs-lookup"><span data-stu-id="c0729-106">The Print Schema is expressed in XML syntax.</span></span> <span data-ttu-id="c0729-107">Les lecteurs sont donc censés être familiarisés avec la syntaxe XML et les termes tels que l’élément, la balise d’élément, le contenu de l’élément, l’attribut et l’espace de noms.</span><span class="sxs-lookup"><span data-stu-id="c0729-107">Readers are therefore expected to be familiar with XML syntax and terms such as element, element tag, element content, attribute, and namespace.</span></span> <span data-ttu-id="c0729-108">L’infrastructure du schéma d’impression est composée d’un petit nombre de types d’éléments ; chaque type d’élément remplit un rôle spécifique dans les technologies basées sur le schéma d’impression.</span><span class="sxs-lookup"><span data-stu-id="c0729-108">The Print Schema Framework is composed of a small number of element types; each element type serves a specific purpose in the technologies built on the Print Schema.</span></span>

<span data-ttu-id="c0729-109">Les types d’éléments se distinguent par leur balise d’élément XML.</span><span class="sxs-lookup"><span data-stu-id="c0729-109">Element types are distinguished by their XML element tag.</span></span> <span data-ttu-id="c0729-110">L’infrastructure du schéma d’impression définit la structure et l’organisation globales des technologies dépendantes, en indiquant pour chaque type d’élément quels types d’éléments sont autorisés en tant qu’éléments enfants.</span><span class="sxs-lookup"><span data-stu-id="c0729-110">The Print Schema Framework defines the overall structure and organization of the dependent technologies, by denoting for each element type which element types are allowed as child elements.</span></span>

<span data-ttu-id="c0729-111">De nombreux types d’éléments sont différenciés des autres du même type par l’attribut Name, qui joue un rôle significatif dans le schéma.</span><span class="sxs-lookup"><span data-stu-id="c0729-111">Many element types are differentiated from others of the same type by the name attribute, which plays a significant role in the schema.</span></span> <span data-ttu-id="c0729-112">L’attribut name sert à identifier les instances de chaque type d’élément.</span><span class="sxs-lookup"><span data-stu-id="c0729-112">The name attribute serves to identify instances of each element type.</span></span> <span data-ttu-id="c0729-113">Les mots clés du schéma d’impression définissent un ensemble de valeurs pour l’attribut Name pour la plupart des types d’éléments.</span><span class="sxs-lookup"><span data-stu-id="c0729-113">The Print Schema Keywords defines a set of values for the name attribute for many of the element types.</span></span> <span data-ttu-id="c0729-114">Dans la plupart des cas, les fournisseurs peuvent assigner leurs propres valeurs à l’attribut Name.</span><span class="sxs-lookup"><span data-stu-id="c0729-114">In most cases, providers can assign their own values to the name attribute.</span></span> <span data-ttu-id="c0729-115">Ils ont uniquement besoin de s’assurer que les valeurs sont XML QNames qualifié avec un espace de noms unique pour le fournisseur.</span><span class="sxs-lookup"><span data-stu-id="c0729-115">They need only ensure the values are XML QNames qualified with a namespace that is unique to the provider.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c0729-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c0729-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c0729-117">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="c0729-117">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



