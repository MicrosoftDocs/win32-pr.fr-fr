---
description: Pour qu’un client crée un PrintTicket, le document PrintCapabilities doit fournir les propriétés des instances de fonctionnalité et des instances d’option dans la fonctionnalité.
ms.assetid: 8169b74f-13e0-4f6b-81e2-1824d932ee50
title: Instances de propriété importantes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4691b73b1206ee092c171b213a3815925b7f53c6
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409122"
---
# <a name="important-property-instances"></a><span data-ttu-id="f4c2a-103">Instances de propriété importantes</span><span class="sxs-lookup"><span data-stu-id="f4c2a-103">Important Property Instances</span></span>

<span data-ttu-id="f4c2a-104">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="f4c2a-104">This topic is not current.</span></span> <span data-ttu-id="f4c2a-105">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="f4c2a-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="f4c2a-106">Pour qu’un client PrintCapabilities puisse construire un PrintTicket raisonnable, le document PrintCapabilities doit fournir certaines propriétés des instances de fonctionnalité ainsi que des instances d’option dans la fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="f4c2a-106">In order for a PrintCapabilities client to be able to construct a reasonable PrintTicket, the PrintCapabilities document must provide certain properties of Feature instances as well as Option instances within the Feature.</span></span> <span data-ttu-id="f4c2a-107">Un module d’interface utilisateur générique requiert ces informations pour construire une interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f4c2a-107">A generic user interface (UI) module requires such information to construct a UI.</span></span> <span data-ttu-id="f4c2a-108">Cela nécessite à son tour que les mots clés du schéma d’impression définissent quelques instances de propriété qui s’affichent en tant qu’enfants des éléments Feature et option.</span><span class="sxs-lookup"><span data-stu-id="f4c2a-108">This in turn requires that the Print Schema Keywords define a few Property instances that appear as children of Feature and Option elements.</span></span>

<span data-ttu-id="f4c2a-109">Les éléments de fonctionnalité peuvent contenir la propriété suivante.</span><span class="sxs-lookup"><span data-stu-id="f4c2a-109">Feature elements can contain the following Property.</span></span>



| <span data-ttu-id="f4c2a-110">Propriété</span><span class="sxs-lookup"><span data-stu-id="f4c2a-110">Property</span></span>                  | <span data-ttu-id="f4c2a-111">Valeurs</span><span class="sxs-lookup"><span data-stu-id="f4c2a-111">Values</span></span>                                 | <span data-ttu-id="f4c2a-112">Objectif</span><span class="sxs-lookup"><span data-stu-id="f4c2a-112">Purpose</span></span>                                                                                                                                                                                                                                                                                                       |
|---------------------------|----------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f4c2a-113">SelectionType</span><span class="sxs-lookup"><span data-stu-id="f4c2a-113">SelectionType</span></span> <br/> | <span data-ttu-id="f4c2a-114">PickOne</span><span class="sxs-lookup"><span data-stu-id="f4c2a-114">PickOne</span></span><br/> <span data-ttu-id="f4c2a-115">PickMany</span><span class="sxs-lookup"><span data-stu-id="f4c2a-115">PickMany</span></span><br/> | <span data-ttu-id="f4c2a-116">Spécifie le nombre d’options qui peuvent être sélectionnées pour cette fonctionnalité à un moment donné, soit un (PickOne), soit plusieurs (PickMany).</span><span class="sxs-lookup"><span data-stu-id="f4c2a-116">Specifies the number of Options that can be selected for this Feature at a given time, either one (PickOne), or more than one (PickMany).</span></span> <span data-ttu-id="f4c2a-117">Le client peut utiliser ces informations pour construire un PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="f4c2a-117">The client can use this information to construct a PrintTicket.</span></span> <span data-ttu-id="f4c2a-118">Ces informations affectent le comportement de l’interface utilisateur, ainsi que la validation PrintTicket par le fournisseur.</span><span class="sxs-lookup"><span data-stu-id="f4c2a-118">This information affects UI behavior, as well as PrintTicket validation by the provider.</span></span><br/> |



 

<span data-ttu-id="f4c2a-119">Les éléments option peuvent contenir la propriété suivante.</span><span class="sxs-lookup"><span data-stu-id="f4c2a-119">Option elements can contain the following Property.</span></span>



| <span data-ttu-id="f4c2a-120">Propriété</span><span class="sxs-lookup"><span data-stu-id="f4c2a-120">Property</span></span>                   | <span data-ttu-id="f4c2a-121">Valeurs</span><span class="sxs-lookup"><span data-stu-id="f4c2a-121">Values</span></span>                           | <span data-ttu-id="f4c2a-122">Objectif</span><span class="sxs-lookup"><span data-stu-id="f4c2a-122">Purpose</span></span>                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f4c2a-123">IdentityOption</span><span class="sxs-lookup"><span data-stu-id="f4c2a-123">IdentityOption</span></span> <br/> | <span data-ttu-id="f4c2a-124">True</span><span class="sxs-lookup"><span data-stu-id="f4c2a-124">True</span></span><br/> <span data-ttu-id="f4c2a-125">False</span><span class="sxs-lookup"><span data-stu-id="f4c2a-125">False</span></span><br/> | <span data-ttu-id="f4c2a-126">La sélection de la propriété IdentityOption est interprétée comme signifiant « désactiver cette fonctionnalité ».</span><span class="sxs-lookup"><span data-stu-id="f4c2a-126">Selecting the IdentityOption Property is interpreted to mean "disable this feature".</span></span> <span data-ttu-id="f4c2a-127">Une fonctionnalité qui contient une propriété SelectionType dont la valeur est PickMany doit également contenir une option qui a une propriété IdentityOption.</span><span class="sxs-lookup"><span data-stu-id="f4c2a-127">A Feature that contains a SelectionType Property whose value is PickMany must also contain an Option that has an IdentityOption Property.</span></span> <span data-ttu-id="f4c2a-128">Le code d’interface utilisateur (ou la construction du client d’un PrintTicket) doit désélectionner une autre option si la propriété IdentityOption est sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="f4c2a-128">The UI code (or client constructing a PrintTicket) must deselect any other Option if the IdentityOption Property is selected.</span></span><br/> |



 

<span data-ttu-id="f4c2a-129">Les éléments Feature, option et ParameterDef peuvent contenir la propriété suivante.</span><span class="sxs-lookup"><span data-stu-id="f4c2a-129">Feature, Option, and ParameterDef elements can contain the following Property.</span></span>



| <span data-ttu-id="f4c2a-130">Propriété</span><span class="sxs-lookup"><span data-stu-id="f4c2a-130">Property</span></span>              | <span data-ttu-id="f4c2a-131">Valeurs</span><span class="sxs-lookup"><span data-stu-id="f4c2a-131">Values</span></span>                          | <span data-ttu-id="f4c2a-132">Objectif</span><span class="sxs-lookup"><span data-stu-id="f4c2a-132">Purpose</span></span>                                                                                                                                                                                                                                                                                                                                     |
|-----------------------|---------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f4c2a-133">DisplayUI</span><span class="sxs-lookup"><span data-stu-id="f4c2a-133">DisplayUI</span></span> <br/> | <span data-ttu-id="f4c2a-134">Afficher</span><span class="sxs-lookup"><span data-stu-id="f4c2a-134">Show</span></span><br/> <span data-ttu-id="f4c2a-135">Masquer</span><span class="sxs-lookup"><span data-stu-id="f4c2a-135">Hide</span></span><br/> | <span data-ttu-id="f4c2a-136">Spécifie si l’élément parent doit être affiché dans l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f4c2a-136">Specifies whether the parent element should be displayed in the UI.</span></span> <span data-ttu-id="f4c2a-137">Afficher indique que l’élément doit être affiché dans l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f4c2a-137">Show indicates that the element should be displayed in the UI.</span></span> <span data-ttu-id="f4c2a-138">Masquer indique que l’élément ne doit pas être affiché dans l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f4c2a-138">Hide indicates that the element should not be displayed in the UI.</span></span> <span data-ttu-id="f4c2a-139">Si cette propriété n’est pas définie pour un élément, l’interprétation par défaut est Show, ce qui signifie que l’élément est affiché.</span><span class="sxs-lookup"><span data-stu-id="f4c2a-139">If this Property is not defined for an element, the default interpretation is Show, meaning that the element is displayed.</span></span><br/> |



 

<span data-ttu-id="f4c2a-140">Les éléments Feature, option et ParameterDef peuvent contenir la propriété suivante.</span><span class="sxs-lookup"><span data-stu-id="f4c2a-140">Feature, Option, and ParameterDef elements can contain the following Property.</span></span>



| <span data-ttu-id="f4c2a-141">Propriété</span><span class="sxs-lookup"><span data-stu-id="f4c2a-141">Property</span></span>                | <span data-ttu-id="f4c2a-142">Valeur</span><span class="sxs-lookup"><span data-stu-id="f4c2a-142">Value</span></span>             | <span data-ttu-id="f4c2a-143">Objectif</span><span class="sxs-lookup"><span data-stu-id="f4c2a-143">Purpose</span></span>                                                                                                                                                                                                                                                                                                                                                                                                               |
|-------------------------|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f4c2a-144">DisplayName</span><span class="sxs-lookup"><span data-stu-id="f4c2a-144">DisplayName</span></span> <br/> | <span data-ttu-id="f4c2a-145">String</span><span class="sxs-lookup"><span data-stu-id="f4c2a-145">String</span></span><br/> | <span data-ttu-id="f4c2a-146">Spécifie la chaîne d’affichage de l’élément parent, en remplaçant le nom d’affichage par défaut.</span><span class="sxs-lookup"><span data-stu-id="f4c2a-146">Specifies the display string for the parent element, overriding the default display name.</span></span> <span data-ttu-id="f4c2a-147">Peut être utilisé par les fournisseurs PrintCapabilities pour présenter un nom complet localisé et convivial.</span><span class="sxs-lookup"><span data-stu-id="f4c2a-147">Can be used by PrintCapabilities providers to present a localized and user friendly display name.</span></span> <span data-ttu-id="f4c2a-148">La valeur de nom complet par défaut est l’attribut de nom de l’élément parent.</span><span class="sxs-lookup"><span data-stu-id="f4c2a-148">The default display name value is the name attribute for the parent element.</span></span> <br/> <span data-ttu-id="f4c2a-149">Dans le cas d’éléments option, si l’attribut name n’est pas fourni, la propriété DisplayName doit être présente.</span><span class="sxs-lookup"><span data-stu-id="f4c2a-149">In the case of Option elements, if the name attribute is not provided, then the DisplayName Property must be present.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="f4c2a-150">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f4c2a-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f4c2a-151">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="f4c2a-151">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




