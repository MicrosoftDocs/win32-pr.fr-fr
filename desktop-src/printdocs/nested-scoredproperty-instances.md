---
description: Les instances ScoredProperty peuvent également être imbriquées dans d’autres instances ScoredProperty ou en tant qu’éléments enfants d’une instance d’option.
ms.assetid: 071dc91f-3574-4e0e-b2ba-0e4a56ce4a28
title: Instances ScoredProperty imbriquées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15a80d291fa59b2f36191f42b2f99ea9d22789a2
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408602"
---
# <a name="nested-scoredproperty-instances"></a><span data-ttu-id="5d066-103">Instances ScoredProperty imbriquées</span><span class="sxs-lookup"><span data-stu-id="5d066-103">Nested ScoredProperty Instances</span></span>

<span data-ttu-id="5d066-104">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="5d066-104">This topic is not current.</span></span> <span data-ttu-id="5d066-105">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="5d066-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="5d066-106">Notez que vous n’êtes pas limité à l’ajout d’instances ScoredProperty en tant qu’éléments enfants d’une instance d’option.</span><span class="sxs-lookup"><span data-stu-id="5d066-106">Notice that you are not restricted to adding ScoredProperty instances as child elements of an Option instance.</span></span> <span data-ttu-id="5d066-107">Les instances ScoredProperty peuvent également être imbriquées dans d’autres instances ScoredProperty.</span><span class="sxs-lookup"><span data-stu-id="5d066-107">ScoredProperty instances may also be nested within other ScoredProperty instances.</span></span> <span data-ttu-id="5d066-108">Cela est utile quand une propriété de l’appareil est complexe et est mieux représentée par plusieurs sous-propriétés.</span><span class="sxs-lookup"><span data-stu-id="5d066-108">This is useful when a device property is complex and is best represented by multiple subproperties.</span></span> <span data-ttu-id="5d066-109">L’ajout de sous-propriétés à une propriété (ou publique) existante ou à un ScoredProperty est un bon moyen d’améliorer une option, tout en conservant la portabilité avec les instances d’option existantes.</span><span class="sxs-lookup"><span data-stu-id="5d066-109">Adding subproperties to an existing (or public) Property or ScoredProperty is a good way to enhance an Option, while retaining portability with existing Option instances.</span></span> <span data-ttu-id="5d066-110">Par exemple, les instances d’option standard pour la fonctionnalité MediaType contiennent un ScoredProperty décrivant le poids du média comme clair, moyen, lourd ou ExtraHeavy.</span><span class="sxs-lookup"><span data-stu-id="5d066-110">For example, the standard Option instances for the MediaType Feature contain a ScoredProperty describing the weight of the media as Light, Medium, Heavy, or ExtraHeavy.</span></span> <span data-ttu-id="5d066-111">Si vous souhaitez obtenir des descriptions plus précises du poids, vous pouvez ajouter une sous-propriété (GramsPer100Sheets dans l’exemple suivant) qui contient le poids réel (en grammes) de feuilles de 100 de médias.</span><span class="sxs-lookup"><span data-stu-id="5d066-111">If you want more precise descriptions of the weight, you can add a subproperty (GramsPer100Sheets in the following example) that contains the actual weight (in grams) of 100 sheets of media.</span></span> <span data-ttu-id="5d066-112">L’option Enhanced peut se présenter comme dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="5d066-112">The enhanced Option might look like the following example.</span></span>

``` syntax
<!-- Note: The following ScoredProperty is not a Public Print Schema ScoredProperty -->
<!-- This example shows a nested ScoredProperty defined by a Private namespace-->
<!-- It is included for illustration purposes. -->

<psf:ScoredProperty name="FabrikamES500:PaperWeight">
  <psf:Value xsi:type="xs:string">Medium</psf:Value>
  <psf:ScoredProperty name="FabrikamES500:GramsPerSheet">
    <Value xsi:type="decimal">109.5</Value>
  </psf:ScoredProperty>
</psf:ScoredProperty>
```

<span data-ttu-id="5d066-113">Une comparaison des instances d’options d’origine et améliorées produit une correspondance presque parfaite, car l’option améliorée est un sur-ensemble de l’original, et les emplacements et valeurs de chacune des instances ScoredProperty d’origine sont conservés.</span><span class="sxs-lookup"><span data-stu-id="5d066-113">A comparison of the original and enhanced Option instances produces a near-perfect match, because the enhanced Option is a superset of the original, and the locations and values of each of the original ScoredProperty instances is preserved.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5d066-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5d066-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5d066-115">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="5d066-115">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



