---
description: En savoir plus sur le paramètre PageDestinationColorProfileURI. Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: b2a4a4d2-a8bc-48dc-ad56-20380f5f91c9
title: PageDestinationColorProfileURI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c3cf719a97f8f8086e88425c1667199815efbbb
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396674"
---
# <a name="pagedestinationcolorprofileuri"></a><span data-ttu-id="59e28-105">PageDestinationColorProfileURI</span><span class="sxs-lookup"><span data-stu-id="59e28-105">PageDestinationColorProfileURI</span></span>

<span data-ttu-id="59e28-106">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="59e28-106">This topic is not current.</span></span> <span data-ttu-id="59e28-107">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="59e28-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="59e28-108">Spécifie une référence URI relative à un profil ICC contenu dans un document XPS.</span><span class="sxs-lookup"><span data-stu-id="59e28-108">Specifies a relative URI reference to an ICC profile contained in an XPS Document.</span></span> <span data-ttu-id="59e28-109">Le traitement de cette option dépend de la configuration de la fonctionnalité PageDeviceColorSpaceUsage.</span><span class="sxs-lookup"><span data-stu-id="59e28-109">The processing of this option depends of the setting of the PageDeviceColorSpaceUsage feature.</span></span> <span data-ttu-id="59e28-110">Tous les éléments qui utilisent ce profil sont supposés être déjà dans l’espace de couleurs approprié du périphérique et ne sont pas gérés par la couleur dans le pilote ou le périphérique.</span><span class="sxs-lookup"><span data-stu-id="59e28-110">All elements using that profile are assumed to be already in the appropriate device color space, and will not be color managed in the driver or device.</span></span>

-   [<span data-ttu-id="59e28-111">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="59e28-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="59e28-112">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="59e28-112">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="59e28-113">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="59e28-113">Element Information</span></span>



| <span data-ttu-id="59e28-114">Nom</span><span class="sxs-lookup"><span data-stu-id="59e28-114">Name</span></span> | <span data-ttu-id="59e28-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="59e28-115">Value</span></span> |
|----------------------------|----------------------------------------------------------|
| <span data-ttu-id="59e28-116">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="59e28-116">Element Type</span></span> <br/>   | <span data-ttu-id="59e28-117">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="59e28-117">ParameterDef</span></span><br/>                                  |
| <span data-ttu-id="59e28-118">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="59e28-118">Scoping Prefix</span></span> <br/> | <span data-ttu-id="59e28-119">Page</span><span class="sxs-lookup"><span data-stu-id="59e28-119">Page</span></span><br/>                                          |
| <span data-ttu-id="59e28-120">Notes</span><span class="sxs-lookup"><span data-stu-id="59e28-120">Notes</span></span> <br/>          | <span data-ttu-id="59e28-121">Lié à l’élément PageDestinationColorProfile</span><span class="sxs-lookup"><span data-stu-id="59e28-121">Linked to PageDestinationColorProfile element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="59e28-122">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="59e28-122">Structure Content</span></span>

<span data-ttu-id="59e28-123">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="59e28-123">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageDestinationColorProfileURI">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:string</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxLength">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinLength">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Conditional</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">characters</psf:Value>
  </psf:Property>
</psf:ParameterDef>
      
```

## <a name="structure-properties"></a><span data-ttu-id="59e28-124">Propriétés de structure</span><span class="sxs-lookup"><span data-stu-id="59e28-124">Structure Properties</span></span>

<span data-ttu-id="59e28-125">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="59e28-125">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="59e28-126">Propriété</span><span class="sxs-lookup"><span data-stu-id="59e28-126">Property</span></span>                | <span data-ttu-id="59e28-127">xsi:type</span><span class="sxs-lookup"><span data-stu-id="59e28-127">xsi:type</span></span>           | <span data-ttu-id="59e28-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="59e28-128">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="59e28-129">DataType</span><span class="sxs-lookup"><span data-stu-id="59e28-129">DataType</span></span><br/>     | <span data-ttu-id="59e28-130">string</span><span class="sxs-lookup"><span data-stu-id="59e28-130">string</span></span><br/>  | <span data-ttu-id="59e28-131">xs:string</span><span class="sxs-lookup"><span data-stu-id="59e28-131">xs:string</span></span><br/>       |
| <span data-ttu-id="59e28-132">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="59e28-132">DefaultValue</span></span><br/> | <span data-ttu-id="59e28-133">string</span><span class="sxs-lookup"><span data-stu-id="59e28-133">string</span></span><br/>  | <span data-ttu-id="59e28-134">non défini</span><span class="sxs-lookup"><span data-stu-id="59e28-134">undefined</span></span><br/>       |
| <span data-ttu-id="59e28-135">MaxLength</span><span class="sxs-lookup"><span data-stu-id="59e28-135">MaxLength</span></span><br/>    | <span data-ttu-id="59e28-136">entier</span><span class="sxs-lookup"><span data-stu-id="59e28-136">integer</span></span><br/> | <span data-ttu-id="59e28-137">non défini</span><span class="sxs-lookup"><span data-stu-id="59e28-137">undefined</span></span><br/>       |
| <span data-ttu-id="59e28-138">MinLength</span><span class="sxs-lookup"><span data-stu-id="59e28-138">MinLength</span></span><br/>    | <span data-ttu-id="59e28-139">integer</span><span class="sxs-lookup"><span data-stu-id="59e28-139">integer</span></span><br/> | <span data-ttu-id="59e28-140">1</span><span class="sxs-lookup"><span data-stu-id="59e28-140">1</span></span><br/>               |
| <span data-ttu-id="59e28-141">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="59e28-141">Mandatory</span></span><br/>    | <span data-ttu-id="59e28-142">string</span><span class="sxs-lookup"><span data-stu-id="59e28-142">string</span></span><br/>  | <span data-ttu-id="59e28-143">PSK : conditionnel</span><span class="sxs-lookup"><span data-stu-id="59e28-143">psk:Conditional</span></span><br/> |
| <span data-ttu-id="59e28-144">Unité</span><span class="sxs-lookup"><span data-stu-id="59e28-144">UnitType</span></span><br/>     | <span data-ttu-id="59e28-145">string</span><span class="sxs-lookup"><span data-stu-id="59e28-145">string</span></span><br/>  | <span data-ttu-id="59e28-146">caractères</span><span class="sxs-lookup"><span data-stu-id="59e28-146">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="59e28-147">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="59e28-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="59e28-148">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="59e28-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




