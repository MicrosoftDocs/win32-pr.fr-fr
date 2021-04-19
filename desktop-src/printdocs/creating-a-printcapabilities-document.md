---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: b49e20b7-bd9e-4b8f-bb4a-bb1e99b0c417
title: Création d’un document PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ccb1adf4626254ba9f71c706ad7d4556a23aeb6
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "106535751"
---
# <a name="creating-a-printcapabilities-document"></a><span data-ttu-id="a7845-104">Création d’un document PrintCapabilities</span><span class="sxs-lookup"><span data-stu-id="a7845-104">Creating a PrintCapabilities Document</span></span>

<span data-ttu-id="a7845-105">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="a7845-105">This topic is not current.</span></span> <span data-ttu-id="a7845-106">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="a7845-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="a7845-107">Une fois qu’un PrintTicket est validé, il peut être utilisé pour créer un instantané du PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="a7845-107">After a PrintTicket is validated, it can be used to create a snapshot of the PrintCapabilities.</span></span> <span data-ttu-id="a7845-108">Le fournisseur doit avoir une représentation interne pour toute propriété dont la valeur dépend de la configuration de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="a7845-108">The provider must have an internal representation for any Property whose Value is dependent on the device configuration.</span></span> <span data-ttu-id="a7845-109">Par exemple, si SpotDiameter est une propriété qui dépend à la fois des fonctionnalités de résolution et de MediaType, une représentation interne de SpotDiameter telle qu’elle est liée aux différentes valeurs pour la résolution et le MediaType peut apparaître comme dans le tableau suivant :</span><span class="sxs-lookup"><span data-stu-id="a7845-109">For example, if SpotDiameter is a Property that is dependent on both the Resolution and MediaType Features, an internal representation of SpotDiameter as it relates to the various values for Resolution and MediaType might appear as in the following table:</span></span>



| <span data-ttu-id="a7845-110">Résolution</span><span class="sxs-lookup"><span data-stu-id="a7845-110">Resolution</span></span>      | <span data-ttu-id="a7845-111">MediaType</span><span class="sxs-lookup"><span data-stu-id="a7845-111">MediaType</span></span>         | <span data-ttu-id="a7845-112">SpotDiameter</span><span class="sxs-lookup"><span data-stu-id="a7845-112">SpotDiameter</span></span>   |
|-----------------|-------------------|----------------|
| <span data-ttu-id="a7845-113">300</span><span class="sxs-lookup"><span data-stu-id="a7845-113">300</span></span><br/>  | <span data-ttu-id="a7845-114">Liés</span><span class="sxs-lookup"><span data-stu-id="a7845-114">Bond</span></span><br/>   | <span data-ttu-id="a7845-115">520</span><span class="sxs-lookup"><span data-stu-id="a7845-115">520</span></span><br/> |
| <span data-ttu-id="a7845-116">300</span><span class="sxs-lookup"><span data-stu-id="a7845-116">300</span></span><br/>  | <span data-ttu-id="a7845-117">Brillance</span><span class="sxs-lookup"><span data-stu-id="a7845-117">Glossy</span></span><br/> | <span data-ttu-id="a7845-118">350</span><span class="sxs-lookup"><span data-stu-id="a7845-118">350</span></span><br/> |
| <span data-ttu-id="a7845-119">600</span><span class="sxs-lookup"><span data-stu-id="a7845-119">600</span></span><br/>  | <span data-ttu-id="a7845-120">Liés</span><span class="sxs-lookup"><span data-stu-id="a7845-120">Bond</span></span><br/>   | <span data-ttu-id="a7845-121">330</span><span class="sxs-lookup"><span data-stu-id="a7845-121">330</span></span><br/> |
| <span data-ttu-id="a7845-122">600</span><span class="sxs-lookup"><span data-stu-id="a7845-122">600</span></span><br/>  | <span data-ttu-id="a7845-123">Brillance</span><span class="sxs-lookup"><span data-stu-id="a7845-123">Glossy</span></span><br/> | <span data-ttu-id="a7845-124">180</span><span class="sxs-lookup"><span data-stu-id="a7845-124">180</span></span><br/> |
| <span data-ttu-id="a7845-125">1200</span><span class="sxs-lookup"><span data-stu-id="a7845-125">1200</span></span><br/> | <span data-ttu-id="a7845-126">Liés</span><span class="sxs-lookup"><span data-stu-id="a7845-126">Bond</span></span><br/>   | <span data-ttu-id="a7845-127">250</span><span class="sxs-lookup"><span data-stu-id="a7845-127">250</span></span><br/> |
| <span data-ttu-id="a7845-128">1200</span><span class="sxs-lookup"><span data-stu-id="a7845-128">1200</span></span><br/> | <span data-ttu-id="a7845-129">Brillance</span><span class="sxs-lookup"><span data-stu-id="a7845-129">Glossy</span></span><br/> | <span data-ttu-id="a7845-130">100</span><span class="sxs-lookup"><span data-stu-id="a7845-130">100</span></span><br/> |



 

<span data-ttu-id="a7845-131">Pour cet exemple, le fournisseur PrintCapabilities doit utiliser le PrintTicket fourni pour sélectionner l’entrée appropriée dans la table interne et signaler comme valeur pour la propriété SpotDiameter.</span><span class="sxs-lookup"><span data-stu-id="a7845-131">For this example, the PrintCapabilities provider must use the provided PrintTicket to select the proper entry from the internal table and report that as the Value for the SpotDiameter Property.</span></span> <span data-ttu-id="a7845-132">Ce processus est répété pour chaque propriété à valeurs multiples (pour chaque propriété dont la valeur dépend de la configuration).</span><span class="sxs-lookup"><span data-stu-id="a7845-132">This process is repeated for every multi-valued Property (for every Property whose Value is dependent on the configuration).</span></span> <span data-ttu-id="a7845-133">La section [schéma PrintCapabilities et construction de document](printcapabilities-schema-and-document-construction.md) décrit les autres étapes impliquées dans la création d’un instantané du PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="a7845-133">The [PrintCapabilities Schema and Document Construction](printcapabilities-schema-and-document-construction.md) section describes the other steps involved in creating a snapshot of the PrintCapabilities.</span></span>

<span data-ttu-id="a7845-134">Pour créer un instantané du document PrintCapabilities par défaut, fournissez un PrintTicket par défaut (plutôt qu’un PrintTicket arbitraire) à la méthode qui crée des documents PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="a7845-134">To create a snapshot of the default PrintCapabilities document, provide a default PrintTicket (rather than an arbitrary PrintTicket) to the method that creates PrintCapabilities documents.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a7845-135">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a7845-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a7845-136">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="a7845-136">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




