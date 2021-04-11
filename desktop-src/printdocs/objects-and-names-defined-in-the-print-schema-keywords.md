---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: 5a07ec21-dc7c-46d5-b1c2-de06f53fe6bf
title: Objets et noms définis dans les mots clés du schéma d’impression
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2347c73dd647f90a88821658cdcf9e2ed846e83
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "104211301"
---
# <a name="objects-and-names-defined-in-the-print-schema-keywords"></a><span data-ttu-id="946eb-104">Objets et noms définis dans les mots clés du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="946eb-104">Objects and Names Defined in the Print Schema Keywords</span></span>

<span data-ttu-id="946eb-105">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="946eb-105">This topic is not current.</span></span> <span data-ttu-id="946eb-106">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="946eb-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="946eb-107">L’infrastructure du schéma d’impression définit un espace de noms qui comprend les éléments et les attributs XML définis dans les mots clés du schéma d’impression.</span><span class="sxs-lookup"><span data-stu-id="946eb-107">The Print Schema Framework defines a namespace that includes the elements and XML attributes defined in the Print Schema Keywords.</span></span> <span data-ttu-id="946eb-108">Cela comprend des éléments tels que Feature, option et ScoredProperty ; les noms d’attributs tels que Name et Propagate ; valeurs et pour les attributs XML tels que contractions.</span><span class="sxs-lookup"><span data-stu-id="946eb-108">This includes elements such as Feature, Option, and ScoredProperty; attribute names such as name and propagate; and values for XML attributes such as constrained.</span></span> <span data-ttu-id="946eb-109">En d’autres termes, chaque utilisation d’un nom défini dans les mots clés du schéma d’impression doit être explicitement qualifiée avec cet espace de noms, ou doit être implicitement associée à cet espace de noms par l’utilisation d’un attribut xmlns par défaut.</span><span class="sxs-lookup"><span data-stu-id="946eb-109">In other words, every use of a name that is defined in the Print Schema Keywords should be explicitly qualified with this namespace, or should be implicitly associated with this namespace by the use of a default xmlns attribute.</span></span> <span data-ttu-id="946eb-110">Le document Mots clés du schéma d’impression définit les instances d’éléments publics qui peuvent apparaître dans n’importe quel contexte ou emplacement donné.</span><span class="sxs-lookup"><span data-stu-id="946eb-110">The Print Schema Keywords document defines the public element instances that may appear in any given context or location.</span></span> <span data-ttu-id="946eb-111">Les instances d’élément doivent apparaître uniquement dans le contexte ou l’emplacement désigné dans l’infrastructure du schéma d’impression.</span><span class="sxs-lookup"><span data-stu-id="946eb-111">Element instances must appear only within the context or location designated in the Print Schema Framework.</span></span> <span data-ttu-id="946eb-112">Par exemple, le <fibres discontinues : option Name = "PSK : letter" > instance définie dans les mots clés du schéma d’impression doit apparaître dans l’instance <de fibres discontinues : Feature Name = "PSK : PageMediaSize" > (également définie dans les mots clés du schéma d’impression).</span><span class="sxs-lookup"><span data-stu-id="946eb-112">For example, the <psf:Option name= "psk:Letter"> instance that is defined in the Print Schema Keywords must appear within the <psf:Feature name = "psk:PageMediaSize"> instance (also defined in the Print Schema Keywords).</span></span> <span data-ttu-id="946eb-113">Vous n’avez pas la liberté d’utiliser une instance d’option donnée en dehors de son contexte spécifié.</span><span class="sxs-lookup"><span data-stu-id="946eb-113">You do not have the freedom to use a given Option instance outside of its specified context.</span></span>

<span data-ttu-id="946eb-114">Les instances d’élément définies de manière privée peuvent apparaître n’importe où, à condition que le type d’élément apparaisse dans un contexte autorisé par l’infrastructure du schéma d’impression.</span><span class="sxs-lookup"><span data-stu-id="946eb-114">Privately-defined element instances may appear anywhere as long as the element type appears in a context allowed by the Print Schema Framework.</span></span>

## <a name="related-topics"></a><span data-ttu-id="946eb-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="946eb-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="946eb-116">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="946eb-116">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



