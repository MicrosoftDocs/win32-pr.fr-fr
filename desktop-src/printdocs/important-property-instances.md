---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: 8169b74f-13e0-4f6b-81e2-1824d932ee50
title: Instances de propriété importantes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ad3f58c099913b129ee7be0337ecab3343a5e5e
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "106537184"
---
# <a name="important-property-instances"></a><span data-ttu-id="ba15e-104">Instances de propriété importantes</span><span class="sxs-lookup"><span data-stu-id="ba15e-104">Important Property Instances</span></span>

<span data-ttu-id="ba15e-105">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="ba15e-105">This topic is not current.</span></span> <span data-ttu-id="ba15e-106">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="ba15e-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="ba15e-107">Pour qu’un client PrintCapabilities puisse construire un PrintTicket raisonnable, le document PrintCapabilities doit fournir certaines propriétés des instances de fonctionnalité ainsi que des instances d’option dans la fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="ba15e-107">In order for a PrintCapabilities client to be able to construct a reasonable PrintTicket, the PrintCapabilities document must provide certain properties of Feature instances as well as Option instances within the Feature.</span></span> <span data-ttu-id="ba15e-108">Un module d’interface utilisateur générique requiert ces informations pour construire une interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ba15e-108">A generic user interface (UI) module requires such information to construct a UI.</span></span> <span data-ttu-id="ba15e-109">Cela nécessite à son tour que les mots clés du schéma d’impression définissent quelques instances de propriété qui s’affichent en tant qu’enfants des éléments Feature et option.</span><span class="sxs-lookup"><span data-stu-id="ba15e-109">This in turn requires that the Print Schema Keywords define a few Property instances that appear as children of Feature and Option elements.</span></span>

<span data-ttu-id="ba15e-110">Les éléments de fonctionnalité peuvent contenir la propriété suivante.</span><span class="sxs-lookup"><span data-stu-id="ba15e-110">Feature elements can contain the following Property.</span></span>



| <span data-ttu-id="ba15e-111">Propriété</span><span class="sxs-lookup"><span data-stu-id="ba15e-111">Property</span></span>                  | <span data-ttu-id="ba15e-112">Valeurs</span><span class="sxs-lookup"><span data-stu-id="ba15e-112">Values</span></span>                                 | <span data-ttu-id="ba15e-113">Objectif</span><span class="sxs-lookup"><span data-stu-id="ba15e-113">Purpose</span></span>                                                                                                                                                                                                                                                                                                       |
|---------------------------|----------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba15e-114">SelectionType</span><span class="sxs-lookup"><span data-stu-id="ba15e-114">SelectionType</span></span> <br/> | <span data-ttu-id="ba15e-115">PickOne</span><span class="sxs-lookup"><span data-stu-id="ba15e-115">PickOne</span></span><br/> <span data-ttu-id="ba15e-116">PickMany</span><span class="sxs-lookup"><span data-stu-id="ba15e-116">PickMany</span></span><br/> | <span data-ttu-id="ba15e-117">Spécifie le nombre d’options qui peuvent être sélectionnées pour cette fonctionnalité à un moment donné, soit un (PickOne), soit plusieurs (PickMany).</span><span class="sxs-lookup"><span data-stu-id="ba15e-117">Specifies the number of Options that can be selected for this Feature at a given time, either one (PickOne), or more than one (PickMany).</span></span> <span data-ttu-id="ba15e-118">Le client peut utiliser ces informations pour construire un PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="ba15e-118">The client can use this information to construct a PrintTicket.</span></span> <span data-ttu-id="ba15e-119">Ces informations affectent le comportement de l’interface utilisateur, ainsi que la validation PrintTicket par le fournisseur.</span><span class="sxs-lookup"><span data-stu-id="ba15e-119">This information affects UI behavior, as well as PrintTicket validation by the provider.</span></span><br/> |



 

<span data-ttu-id="ba15e-120">Les éléments option peuvent contenir la propriété suivante.</span><span class="sxs-lookup"><span data-stu-id="ba15e-120">Option elements can contain the following Property.</span></span>



| <span data-ttu-id="ba15e-121">Propriété</span><span class="sxs-lookup"><span data-stu-id="ba15e-121">Property</span></span>                   | <span data-ttu-id="ba15e-122">Valeurs</span><span class="sxs-lookup"><span data-stu-id="ba15e-122">Values</span></span>                           | <span data-ttu-id="ba15e-123">Objectif</span><span class="sxs-lookup"><span data-stu-id="ba15e-123">Purpose</span></span>                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba15e-124">IdentityOption</span><span class="sxs-lookup"><span data-stu-id="ba15e-124">IdentityOption</span></span> <br/> | <span data-ttu-id="ba15e-125">Vrai</span><span class="sxs-lookup"><span data-stu-id="ba15e-125">True</span></span><br/> <span data-ttu-id="ba15e-126">Faux</span><span class="sxs-lookup"><span data-stu-id="ba15e-126">False</span></span><br/> | <span data-ttu-id="ba15e-127">La sélection de la propriété IdentityOption est interprétée comme signifiant « désactiver cette fonctionnalité ».</span><span class="sxs-lookup"><span data-stu-id="ba15e-127">Selecting the IdentityOption Property is interpreted to mean "disable this feature".</span></span> <span data-ttu-id="ba15e-128">Une fonctionnalité qui contient une propriété SelectionType dont la valeur est PickMany doit également contenir une option qui a une propriété IdentityOption.</span><span class="sxs-lookup"><span data-stu-id="ba15e-128">A Feature that contains a SelectionType Property whose value is PickMany must also contain an Option that has an IdentityOption Property.</span></span> <span data-ttu-id="ba15e-129">Le code d’interface utilisateur (ou la construction du client d’un PrintTicket) doit désélectionner une autre option si la propriété IdentityOption est sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="ba15e-129">The UI code (or client constructing a PrintTicket) must deselect any other Option if the IdentityOption Property is selected.</span></span><br/> |



 

<span data-ttu-id="ba15e-130">Les éléments Feature, option et ParameterDef peuvent contenir la propriété suivante.</span><span class="sxs-lookup"><span data-stu-id="ba15e-130">Feature, Option, and ParameterDef elements can contain the following Property.</span></span>



| <span data-ttu-id="ba15e-131">Propriété</span><span class="sxs-lookup"><span data-stu-id="ba15e-131">Property</span></span>              | <span data-ttu-id="ba15e-132">Valeurs</span><span class="sxs-lookup"><span data-stu-id="ba15e-132">Values</span></span>                          | <span data-ttu-id="ba15e-133">Objectif</span><span class="sxs-lookup"><span data-stu-id="ba15e-133">Purpose</span></span>                                                                                                                                                                                                                                                                                                                                     |
|-----------------------|---------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba15e-134">DisplayUI</span><span class="sxs-lookup"><span data-stu-id="ba15e-134">DisplayUI</span></span> <br/> | <span data-ttu-id="ba15e-135">Afficher</span><span class="sxs-lookup"><span data-stu-id="ba15e-135">Show</span></span><br/> <span data-ttu-id="ba15e-136">Masquer</span><span class="sxs-lookup"><span data-stu-id="ba15e-136">Hide</span></span><br/> | <span data-ttu-id="ba15e-137">Spécifie si l’élément parent doit être affiché dans l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ba15e-137">Specifies whether the parent element should be displayed in the UI.</span></span> <span data-ttu-id="ba15e-138">Afficher indique que l’élément doit être affiché dans l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ba15e-138">Show indicates that the element should be displayed in the UI.</span></span> <span data-ttu-id="ba15e-139">Masquer indique que l’élément ne doit pas être affiché dans l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ba15e-139">Hide indicates that the element should not be displayed in the UI.</span></span> <span data-ttu-id="ba15e-140">Si cette propriété n’est pas définie pour un élément, l’interprétation par défaut est Show, ce qui signifie que l’élément est affiché.</span><span class="sxs-lookup"><span data-stu-id="ba15e-140">If this Property is not defined for an element, the default interpretation is Show, meaning that the element is displayed.</span></span><br/> |



 

<span data-ttu-id="ba15e-141">Les éléments Feature, option et ParameterDef peuvent contenir la propriété suivante.</span><span class="sxs-lookup"><span data-stu-id="ba15e-141">Feature, Option, and ParameterDef elements can contain the following Property.</span></span>



| <span data-ttu-id="ba15e-142">Propriété</span><span class="sxs-lookup"><span data-stu-id="ba15e-142">Property</span></span>                | <span data-ttu-id="ba15e-143">Valeur</span><span class="sxs-lookup"><span data-stu-id="ba15e-143">Value</span></span>             | <span data-ttu-id="ba15e-144">Objectif</span><span class="sxs-lookup"><span data-stu-id="ba15e-144">Purpose</span></span>                                                                                                                                                                                                                                                                                                                                                                                                               |
|-------------------------|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba15e-145">DisplayName</span><span class="sxs-lookup"><span data-stu-id="ba15e-145">DisplayName</span></span> <br/> | <span data-ttu-id="ba15e-146">String</span><span class="sxs-lookup"><span data-stu-id="ba15e-146">String</span></span><br/> | <span data-ttu-id="ba15e-147">Spécifie la chaîne d’affichage de l’élément parent, en remplaçant le nom d’affichage par défaut.</span><span class="sxs-lookup"><span data-stu-id="ba15e-147">Specifies the display string for the parent element, overriding the default display name.</span></span> <span data-ttu-id="ba15e-148">Peut être utilisé par les fournisseurs PrintCapabilities pour présenter un nom complet localisé et convivial.</span><span class="sxs-lookup"><span data-stu-id="ba15e-148">Can be used by PrintCapabilities providers to present a localized and user friendly display name.</span></span> <span data-ttu-id="ba15e-149">La valeur de nom complet par défaut est l’attribut de nom de l’élément parent.</span><span class="sxs-lookup"><span data-stu-id="ba15e-149">The default display name value is the name attribute for the parent element.</span></span> <br/> <span data-ttu-id="ba15e-150">Dans le cas d’éléments option, si l’attribut name n’est pas fourni, la propriété DisplayName doit être présente.</span><span class="sxs-lookup"><span data-stu-id="ba15e-150">In the case of Option elements, if the name attribute is not provided, then the DisplayName Property must be present.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="ba15e-151">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ba15e-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ba15e-152">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="ba15e-152">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




