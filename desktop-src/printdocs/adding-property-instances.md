---
description: En savoir plus sur l’ajout d’instances de propriété. Le schéma d’impression permet de présenter des instances de propriété dans une instance d’option.
ms.assetid: dac287a9-77ca-44d8-8019-b05e4c61dc52
title: Ajout d’instances de propriété
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8085fa10f824f32dc76aef0f1e5f78ca05b22b93
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409692"
---
# <a name="adding-property-instances"></a><span data-ttu-id="eef47-104">Ajout d’instances de propriété</span><span class="sxs-lookup"><span data-stu-id="eef47-104">Adding Property Instances</span></span>

<span data-ttu-id="eef47-105">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="eef47-105">This topic is not current.</span></span> <span data-ttu-id="eef47-106">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="eef47-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="eef47-107">Le schéma d’impression permet de présenter des instances de propriété dans une instance d’option.</span><span class="sxs-lookup"><span data-stu-id="eef47-107">The Print Schema allows Property instances to be present in an Option instance.</span></span> <span data-ttu-id="eef47-108">Les instances de propriété définies dans le document PrintCapabilities ne sont pas propagées vers les instances d’option enregistrées dans PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="eef47-108">The Property instances defined in the PrintCapabilities document are not propagated to the Option instances saved in the PrintTicket.</span></span> <span data-ttu-id="eef47-109">Les éléments de propriété n’affectent pas le résultat du processus de notation lorsque deux instances d’option sont comparées, mais les instances ScoredProperty affectent ce processus.</span><span class="sxs-lookup"><span data-stu-id="eef47-109">Property elements do not affect the result of the scoring process when two Option instances are compared, but ScoredProperty instances do affect this process.</span></span> <span data-ttu-id="eef47-110">Tous les pilotes de périphérique qui implémentent un algorithme de notation doivent respecter cette Convention.</span><span class="sxs-lookup"><span data-stu-id="eef47-110">All device drivers that implement a scoring algorithm should observe this convention.</span></span> <span data-ttu-id="eef47-111">Les fournisseurs PrintCapabilities sont autorisés à ajouter des instances de propriété à une option si ces instances sont spécifiques à cette option particulière, et pas d’autres, ou si le fournisseur prévoit que la valeur de cette propriété s’affiche pour chaque option de la fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="eef47-111">PrintCapabilities providers are permitted to add Property instances to an Option if these instances are specific to that particular Option and no others, or if the provider intends for the value of this Property to appear for every Option in the Feature.</span></span> <span data-ttu-id="eef47-112">Par exemple, supposons que la propriété PrintRate dépend de l’option sélectionnée pour la fonctionnalité PageResolution.</span><span class="sxs-lookup"><span data-stu-id="eef47-112">For example, suppose that the PrintRate Property is dependent on the Option selected for the PageResolution Feature.</span></span> <span data-ttu-id="eef47-113">Si la propriété PrintRate a été placée au niveau racine du document PrintCapabilities, elle est à valeur unique et reflète uniquement le taux d’impression pour la résolution actuellement sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="eef47-113">If the PrintRate Property were placed at the root level of the PrintCapabilities document, it would be single-valued and would reflect only the print rate for the currently selected resolution.</span></span> <span data-ttu-id="eef47-114">Toutefois, si la propriété PrintRate a été placée dans chaque option PageResolution, chaque instance de la propriété PrintRate peut refléter la vitesse d’impression de l’option PageResolution qui l’a contenue.</span><span class="sxs-lookup"><span data-stu-id="eef47-114">However, if the PrintRate Property were placed within each PageResolution Option, each instance of the PrintRate Property could reflect the print rate for the PageResolution Option that contained it.</span></span> <span data-ttu-id="eef47-115">Le document PrintCapabilities contient plusieurs définitions pour PrintRate, l’une correspondant à chaque option PageResolution.</span><span class="sxs-lookup"><span data-stu-id="eef47-115">The PrintCapabilities document would contain multiple definitions for PrintRate, one corresponding to each PageResolution Option.</span></span> <span data-ttu-id="eef47-116">À l’aide d’une représentation sténographique, le PrintCapabilities contiendra :</span><span class="sxs-lookup"><span data-stu-id="eef47-116">Using a shorthand representation, the PrintCapabilities would contain:</span></span>

``` syntax
<psf:Feature name="psk:PageResolution">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option>
    <psf:ScoredProperty name="psk:ResolutionX">
      <psf:Value xsi:type="xs:string">800dpi</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:ResolutionY">
      <psf:Value xsi:type="xs:string">600dpi</psf:Value>
    </psf:ScoredProperty>
    <!-- Note: The following Property is not part of the Print Schema Framework -->
    <!-- It is included for illustration purposes. -->
    <!-- It is shown as a privately defined implementation-->
    <Property name="FabrikamES500:PrintRate">
      <Value xsi:type="string">20ppm</Value>
    </psf:Property>
  </psf:Option>
</psf:Feature>
```

<span data-ttu-id="eef47-117">Dans certains cas, le fait de placer une propriété de taux d’impression dans chaque option de résolution est plus pratique pour le client, car le client peut déterminer en un clin d’œil l’effet de chaque option de résolution sur le taux d’impression, sans avoir à obtenir un nouveau document PrintCapabilities pour chaque paramètre de résolution.</span><span class="sxs-lookup"><span data-stu-id="eef47-117">In some situations, placing a print rate Property within each resolution Option is more convenient for the client, because the client can determine at a glance the effect that each resolution Option has on the print rate, without the need for obtaining a new PrintCapabilities document for each resolution setting.</span></span>

<span data-ttu-id="eef47-118">Notez également que les instances de propriété peuvent également être ajoutées en tant qu’éléments enfants d’éléments de fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="eef47-118">Note also that Property instances can also be added as child elements of Feature elements.</span></span> <span data-ttu-id="eef47-119">Cela est utile si des instances de propriété ou des valeurs d’instances de propriété sont spécifiques à chaque fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="eef47-119">This is useful if there are Property instances or values of Property instances that are specific to each Feature.</span></span> <span data-ttu-id="eef47-120">Par exemple, il peut y avoir une propriété qui spécifie s’il est possible de sélectionner une seule option à la fois pour une fonctionnalité, ou si plusieurs options peuvent être sélectionnées.</span><span class="sxs-lookup"><span data-stu-id="eef47-120">For example, there might be a Property that specifies whether only one Option is permitted to be selected at one time for a Feature, or whether multiple Options may be selected.</span></span> <span data-ttu-id="eef47-121">Il s’agit de l’une des propriétés choisies \_ \_ dans les fichiers PPD et GPD.</span><span class="sxs-lookup"><span data-stu-id="eef47-121">This is the PICK\_ONE, PICK\_MANY property used in PPD and GPD files.</span></span> <span data-ttu-id="eef47-122">Étant donné que certaines instances de fonctionnalités peuvent être identifiées comme en PICK \_ un, tandis que d’autres peuvent être identifiées en tant que sélection \_ de plusieurs, cette propriété doit être définie pour chaque fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="eef47-122">Because some Feature instances might be identified as PICK\_ONE, while others might be identified as PICK\_MANY, this Property must be defined for each Feature.</span></span> <span data-ttu-id="eef47-123">La recherche de la propriété en tant qu’élément enfant de la fonctionnalité produit l’association entre la propriété et la fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="eef47-123">Locating the Property as a child element of the Feature produces the association between the Property and the Feature.</span></span>

## <a name="related-topics"></a><span data-ttu-id="eef47-124">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="eef47-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eef47-125">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="eef47-125">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



