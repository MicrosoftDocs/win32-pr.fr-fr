---
description: Une fois qu’un PrintTicket est validé, il peut être utilisé pour créer un instantané du PrintCapabilities.
ms.assetid: b49e20b7-bd9e-4b8f-bb4a-bb1e99b0c417
title: Création d’un document PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b96ea51cef9dfd0f351704b3b71a7f6163737736
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409512"
---
# <a name="creating-a-printcapabilities-document"></a><span data-ttu-id="4b0d9-103">Création d’un document PrintCapabilities</span><span class="sxs-lookup"><span data-stu-id="4b0d9-103">Creating a PrintCapabilities Document</span></span>

<span data-ttu-id="4b0d9-104">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="4b0d9-104">This topic is not current.</span></span> <span data-ttu-id="4b0d9-105">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="4b0d9-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="4b0d9-106">Une fois qu’un PrintTicket est validé, il peut être utilisé pour créer un instantané du PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="4b0d9-106">After a PrintTicket is validated, it can be used to create a snapshot of the PrintCapabilities.</span></span> <span data-ttu-id="4b0d9-107">Le fournisseur doit avoir une représentation interne pour toute propriété dont la valeur dépend de la configuration de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="4b0d9-107">The provider must have an internal representation for any Property whose Value is dependent on the device configuration.</span></span> <span data-ttu-id="4b0d9-108">Par exemple, si SpotDiameter est une propriété qui dépend à la fois des fonctionnalités de résolution et de MediaType, une représentation interne de SpotDiameter telle qu’elle est liée aux différentes valeurs pour la résolution et le MediaType peut apparaître comme dans le tableau suivant :</span><span class="sxs-lookup"><span data-stu-id="4b0d9-108">For example, if SpotDiameter is a Property that is dependent on both the Resolution and MediaType Features, an internal representation of SpotDiameter as it relates to the various values for Resolution and MediaType might appear as in the following table:</span></span>



| <span data-ttu-id="4b0d9-109">Résolution</span><span class="sxs-lookup"><span data-stu-id="4b0d9-109">Resolution</span></span>      | <span data-ttu-id="4b0d9-110">MediaType</span><span class="sxs-lookup"><span data-stu-id="4b0d9-110">MediaType</span></span>         | <span data-ttu-id="4b0d9-111">SpotDiameter</span><span class="sxs-lookup"><span data-stu-id="4b0d9-111">SpotDiameter</span></span>   |
|-----------------|-------------------|----------------|
| <span data-ttu-id="4b0d9-112">300</span><span class="sxs-lookup"><span data-stu-id="4b0d9-112">300</span></span><br/>  | <span data-ttu-id="4b0d9-113">Liés</span><span class="sxs-lookup"><span data-stu-id="4b0d9-113">Bond</span></span><br/>   | <span data-ttu-id="4b0d9-114">520</span><span class="sxs-lookup"><span data-stu-id="4b0d9-114">520</span></span><br/> |
| <span data-ttu-id="4b0d9-115">300</span><span class="sxs-lookup"><span data-stu-id="4b0d9-115">300</span></span><br/>  | <span data-ttu-id="4b0d9-116">Brillance</span><span class="sxs-lookup"><span data-stu-id="4b0d9-116">Glossy</span></span><br/> | <span data-ttu-id="4b0d9-117">350</span><span class="sxs-lookup"><span data-stu-id="4b0d9-117">350</span></span><br/> |
| <span data-ttu-id="4b0d9-118">600</span><span class="sxs-lookup"><span data-stu-id="4b0d9-118">600</span></span><br/>  | <span data-ttu-id="4b0d9-119">Liés</span><span class="sxs-lookup"><span data-stu-id="4b0d9-119">Bond</span></span><br/>   | <span data-ttu-id="4b0d9-120">330</span><span class="sxs-lookup"><span data-stu-id="4b0d9-120">330</span></span><br/> |
| <span data-ttu-id="4b0d9-121">600</span><span class="sxs-lookup"><span data-stu-id="4b0d9-121">600</span></span><br/>  | <span data-ttu-id="4b0d9-122">Brillance</span><span class="sxs-lookup"><span data-stu-id="4b0d9-122">Glossy</span></span><br/> | <span data-ttu-id="4b0d9-123">180</span><span class="sxs-lookup"><span data-stu-id="4b0d9-123">180</span></span><br/> |
| <span data-ttu-id="4b0d9-124">1200</span><span class="sxs-lookup"><span data-stu-id="4b0d9-124">1200</span></span><br/> | <span data-ttu-id="4b0d9-125">Liés</span><span class="sxs-lookup"><span data-stu-id="4b0d9-125">Bond</span></span><br/>   | <span data-ttu-id="4b0d9-126">250</span><span class="sxs-lookup"><span data-stu-id="4b0d9-126">250</span></span><br/> |
| <span data-ttu-id="4b0d9-127">1200</span><span class="sxs-lookup"><span data-stu-id="4b0d9-127">1200</span></span><br/> | <span data-ttu-id="4b0d9-128">Brillance</span><span class="sxs-lookup"><span data-stu-id="4b0d9-128">Glossy</span></span><br/> | <span data-ttu-id="4b0d9-129">100</span><span class="sxs-lookup"><span data-stu-id="4b0d9-129">100</span></span><br/> |



 

<span data-ttu-id="4b0d9-130">Pour cet exemple, le fournisseur PrintCapabilities doit utiliser le PrintTicket fourni pour sélectionner l’entrée appropriée dans la table interne et signaler comme valeur pour la propriété SpotDiameter.</span><span class="sxs-lookup"><span data-stu-id="4b0d9-130">For this example, the PrintCapabilities provider must use the provided PrintTicket to select the proper entry from the internal table and report that as the Value for the SpotDiameter Property.</span></span> <span data-ttu-id="4b0d9-131">Ce processus est répété pour chaque propriété à valeurs multiples (pour chaque propriété dont la valeur dépend de la configuration).</span><span class="sxs-lookup"><span data-stu-id="4b0d9-131">This process is repeated for every multi-valued Property (for every Property whose Value is dependent on the configuration).</span></span> <span data-ttu-id="4b0d9-132">La section [schéma PrintCapabilities et construction de document](printcapabilities-schema-and-document-construction.md) décrit les autres étapes impliquées dans la création d’un instantané du PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="4b0d9-132">The [PrintCapabilities Schema and Document Construction](printcapabilities-schema-and-document-construction.md) section describes the other steps involved in creating a snapshot of the PrintCapabilities.</span></span>

<span data-ttu-id="4b0d9-133">Pour créer un instantané du document PrintCapabilities par défaut, fournissez un PrintTicket par défaut (plutôt qu’un PrintTicket arbitraire) à la méthode qui crée des documents PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="4b0d9-133">To create a snapshot of the default PrintCapabilities document, provide a default PrintTicket (rather than an arbitrary PrintTicket) to the method that creates PrintCapabilities documents.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4b0d9-134">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4b0d9-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4b0d9-135">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="4b0d9-135">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




