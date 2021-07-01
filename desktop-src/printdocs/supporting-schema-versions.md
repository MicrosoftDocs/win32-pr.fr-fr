---
description: Apprenez à prendre en charge différentes versions de l’infrastructure du schéma d’impression. Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: fc89dd2d-9a5d-400b-aee9-a1e4cf7d83da
title: Versions de schéma de prise en charge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7eac627d3dd711bc952d881efd393720af128e7f
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120594"
---
# <a name="supporting-schema-versions"></a><span data-ttu-id="0e5c9-105">Versions de schéma de prise en charge</span><span class="sxs-lookup"><span data-stu-id="0e5c9-105">Supporting Schema Versions</span></span>

<span data-ttu-id="0e5c9-106">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="0e5c9-106">This topic is not current.</span></span> <span data-ttu-id="0e5c9-107">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="0e5c9-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="0e5c9-108">L’infrastructure du schéma d’impression est susceptible de changer à l’avenir à mesure que de nouveaux besoins se présentent.</span><span class="sxs-lookup"><span data-stu-id="0e5c9-108">The Print Schema Framework is subject to change in the future as new needs arise.</span></span> <span data-ttu-id="0e5c9-109">Ces modifications sont censées être très rares, car la modification la plus courante est l’introduction de nouveaux noms d’instance.</span><span class="sxs-lookup"><span data-stu-id="0e5c9-109">Such changes are expected to be very infrequent, because the most common change is the introduction of new instance names.</span></span> <span data-ttu-id="0e5c9-110">Cette modification n’affecte pas la structure de l’infrastructure et doit être transparente pour les clients et les fournisseurs.</span><span class="sxs-lookup"><span data-stu-id="0e5c9-110">This change does not affect the structure of the Framework, and should be transparent to clients and providers.</span></span> <span data-ttu-id="0e5c9-111">Toute modification apportée à la structure et à l’organisation de l’infrastructure du schéma d’impression est identifiée par un incrément de son numéro de version.</span><span class="sxs-lookup"><span data-stu-id="0e5c9-111">Any changes to the structure and organization of the Print Schema Framework will be identified by increments to its version number.</span></span> <span data-ttu-id="0e5c9-112">Les ajouts aux mots clés du schéma d’impression ne sont pas identifiés.</span><span class="sxs-lookup"><span data-stu-id="0e5c9-112">Additions to the Print Schema Keywords will not be identified.</span></span> <span data-ttu-id="0e5c9-113">Les fournisseurs PrintTicket doivent être en mesure de prendre en charge la version actuelle de l’infrastructure du schéma d’impression, ainsi que toute version antérieure.</span><span class="sxs-lookup"><span data-stu-id="0e5c9-113">PrintTicket providers must be capable of supporting the current Print Schema Framework version, as well as any prior version.</span></span> <span data-ttu-id="0e5c9-114">La version de l’infrastructure du schéma d’impression est identifiée à l’aide de l’attribut XML : version qui apparaît à l’élément racine du PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="0e5c9-114">The Print Schema Framework version is identified using the XML Attribute: Version that appears at the root element of the PrintTicket.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0e5c9-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0e5c9-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0e5c9-116">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="0e5c9-116">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



