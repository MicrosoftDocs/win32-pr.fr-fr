---
description: Les fournisseurs PrintCapabilities doivent prendre en charge un ensemble minimal de fonctionnalités, qui sont implicites par l’interface du fournisseur PrintTicket/PrintCapabilities.
ms.assetid: 92e9bce1-d58e-40a4-9721-832d7c3bc2b2
title: Responsabilités des fournisseurs PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70cc04137eacdd2395205b96233db3c53964bc02
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404912"
---
# <a name="responsibilities-of-printcapabilities-providers"></a><span data-ttu-id="c5e69-103">Responsabilités des fournisseurs PrintCapabilities</span><span class="sxs-lookup"><span data-stu-id="c5e69-103">Responsibilities of PrintCapabilities Providers</span></span>

<span data-ttu-id="c5e69-104">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="c5e69-104">This topic is not current.</span></span> <span data-ttu-id="c5e69-105">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="c5e69-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="c5e69-106">Les fournisseurs PrintCapabilities doivent prendre en charge un ensemble minimal de fonctionnalités, qui sont implicites par l’interface du fournisseur PrintTicket/PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="c5e69-106">PrintCapabilities providers must support a minimum set of capabilities, which are implied by the PrintTicket/PrintCapabilities Provider Interface.</span></span> <span data-ttu-id="c5e69-107">Ces fonctionnalités sont répertoriées ici.</span><span class="sxs-lookup"><span data-stu-id="c5e69-107">These capabilities are listed here.</span></span>

-   <span data-ttu-id="c5e69-108">Ils doivent suivre la direction de la propagation ? Attribut XML, lorsqu’il apparaît dans le contexte approprié et contient une valeur valide pour ce contexte.</span><span class="sxs-lookup"><span data-stu-id="c5e69-108">They must follow the direction of the propagate??XML attribute, when it appears in the appropriate context and contains a valid value for that context.</span></span>

-   <span data-ttu-id="c5e69-109">Ils doivent générer un document PrintCapabilities conforme au schéma PrintCapabilities et répondant aux exigences spécifiées dans le schéma d’impression.</span><span class="sxs-lookup"><span data-stu-id="c5e69-109">They must generate a PrintCapabilities document that conforms to the PrintCapabilities Schema and satisfies the requirements specified in the Print Schema.</span></span>

-   <span data-ttu-id="c5e69-110">Ils doivent être en mesure de reconnaître un PrintTicket valide.</span><span class="sxs-lookup"><span data-stu-id="c5e69-110">They must be able to recognize a valid PrintTicket.</span></span>

-   <span data-ttu-id="c5e69-111">Ils doivent être en mesure d’interpréter un PrintTicket et de comprendre la configuration spécifique qu’il représente.</span><span class="sxs-lookup"><span data-stu-id="c5e69-111">They must be able to interpret a PrintTicket and understand the specific configuration it represents.</span></span>

-   <span data-ttu-id="c5e69-112">Ils doivent être en mesure de déterminer si cette configuration contient des conflits de contrainte.</span><span class="sxs-lookup"><span data-stu-id="c5e69-112">They must be able to determine whether that configuration contains constraint conflicts.</span></span>

-   <span data-ttu-id="c5e69-113">Ils doivent être en mesure de modifier un PrintTicket non valide ou en conflit en rendant la modification la moins importante nécessaire pour qu’il soit valide et sans conflit.</span><span class="sxs-lookup"><span data-stu-id="c5e69-113">They must be able to modify an invalid or conflicting PrintTicket by making the least significant change necessary to make it both valid and without conflicts.</span></span>

-   <span data-ttu-id="c5e69-114">Ils doivent être en mesure de générer un document PrintCapabilities pour une configuration d’appareil particulière.</span><span class="sxs-lookup"><span data-stu-id="c5e69-114">They must be able to generate a PrintCapabilities document for a particular device configuration.</span></span>

-   <span data-ttu-id="c5e69-115">Ils doivent être en mesure de générer une configuration par défaut ou un PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="c5e69-115">They must be able to generate a default configuration or PrintTicket.</span></span>

-   <span data-ttu-id="c5e69-116">Ils doivent être en mesure de générer un document PrintCapabilities qui correspond à la configuration par défaut.</span><span class="sxs-lookup"><span data-stu-id="c5e69-116">They must be able to generate a PrintCapabilities document that corresponds to the default configuration.</span></span>

-   <span data-ttu-id="c5e69-117">Ils doivent implémenter un processus de notation des options défini par le pilote de périphérique capable de déterminer la proximité de la correspondance entre deux instances d’option qui appartiennent à la même fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="c5e69-117">They must implement an Option-scoring process defined by the device driver capable of determining the closeness of match between two Option instances that belong to the same Feature.</span></span> <span data-ttu-id="c5e69-118">Cet algorithme est utilisé dans le processus de validation PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="c5e69-118">This algorithm is used in the PrintTicket validation process.</span></span>

<span data-ttu-id="c5e69-119">En plus des exigences ci-dessus, le document PrintCapabilities doit contenir des valeurs valides et correctes pour chaque attribut XML (par exemple, contractions) de chaque option.</span><span class="sxs-lookup"><span data-stu-id="c5e69-119">In addition to the foregoing requirements, the PrintCapabilities document must contain valid and correct values for each XML attribute (for example, constrained) of each Option.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c5e69-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c5e69-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c5e69-121">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="c5e69-121">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



