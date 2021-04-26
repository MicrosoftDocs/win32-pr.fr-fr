---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: b2a4a4d2-a8bc-48dc-ad56-20380f5f91c9
title: PageDestinationColorProfileURI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b321cba1608b1098dcc91f3800ef11f4968fb3f2
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996096"
---
# <a name="pagedestinationcolorprofileuri"></a><span data-ttu-id="e1ee1-104">PageDestinationColorProfileURI</span><span class="sxs-lookup"><span data-stu-id="e1ee1-104">PageDestinationColorProfileURI</span></span>

<span data-ttu-id="e1ee1-105">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="e1ee1-105">This topic is not current.</span></span> <span data-ttu-id="e1ee1-106">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="e1ee1-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="e1ee1-107">Spécifie une référence URI relative à un profil ICC contenu dans un document XPS.</span><span class="sxs-lookup"><span data-stu-id="e1ee1-107">Specifies a relative URI reference to an ICC profile contained in an XPS Document.</span></span> <span data-ttu-id="e1ee1-108">Le traitement de cette option dépend de la configuration de la fonctionnalité PageDeviceColorSpaceUsage.</span><span class="sxs-lookup"><span data-stu-id="e1ee1-108">The processing of this option depends of the setting of the PageDeviceColorSpaceUsage feature.</span></span> <span data-ttu-id="e1ee1-109">Tous les éléments qui utilisent ce profil sont supposés être déjà dans l’espace de couleurs approprié du périphérique et ne sont pas gérés par la couleur dans le pilote ou le périphérique.</span><span class="sxs-lookup"><span data-stu-id="e1ee1-109">All elements using that profile are assumed to be already in the appropriate device color space, and will not be color managed in the driver or device.</span></span>

-   [<span data-ttu-id="e1ee1-110">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="e1ee1-110">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="e1ee1-111">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="e1ee1-111">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="e1ee1-112">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="e1ee1-112">Element Information</span></span>



| <span data-ttu-id="e1ee1-113">Nom</span><span class="sxs-lookup"><span data-stu-id="e1ee1-113">Name</span></span> | <span data-ttu-id="e1ee1-114">Value</span><span class="sxs-lookup"><span data-stu-id="e1ee1-114">Value</span></span> |
|----------------------------|----------------------------------------------------------|
| <span data-ttu-id="e1ee1-115">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="e1ee1-115">Element Type</span></span> <br/>   | <span data-ttu-id="e1ee1-116">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="e1ee1-116">ParameterDef</span></span><br/>                                  |
| <span data-ttu-id="e1ee1-117">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="e1ee1-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="e1ee1-118">Page</span><span class="sxs-lookup"><span data-stu-id="e1ee1-118">Page</span></span><br/>                                          |
| <span data-ttu-id="e1ee1-119">Notes</span><span class="sxs-lookup"><span data-stu-id="e1ee1-119">Notes</span></span> <br/>          | <span data-ttu-id="e1ee1-120">Lié à l’élément PageDestinationColorProfile</span><span class="sxs-lookup"><span data-stu-id="e1ee1-120">Linked to PageDestinationColorProfile element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="e1ee1-121">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="e1ee1-121">Structure Content</span></span>

<span data-ttu-id="e1ee1-122">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="e1ee1-122">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="e1ee1-123">Propriétés de structure</span><span class="sxs-lookup"><span data-stu-id="e1ee1-123">Structure Properties</span></span>

<span data-ttu-id="e1ee1-124">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="e1ee1-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="e1ee1-125">Propriété</span><span class="sxs-lookup"><span data-stu-id="e1ee1-125">Property</span></span>                | <span data-ttu-id="e1ee1-126">xsi:type</span><span class="sxs-lookup"><span data-stu-id="e1ee1-126">xsi:type</span></span>           | <span data-ttu-id="e1ee1-127">Value</span><span class="sxs-lookup"><span data-stu-id="e1ee1-127">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="e1ee1-128">DataType</span><span class="sxs-lookup"><span data-stu-id="e1ee1-128">DataType</span></span><br/>     | <span data-ttu-id="e1ee1-129">string</span><span class="sxs-lookup"><span data-stu-id="e1ee1-129">string</span></span><br/>  | <span data-ttu-id="e1ee1-130">xs:string</span><span class="sxs-lookup"><span data-stu-id="e1ee1-130">xs:string</span></span><br/>       |
| <span data-ttu-id="e1ee1-131">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="e1ee1-131">DefaultValue</span></span><br/> | <span data-ttu-id="e1ee1-132">string</span><span class="sxs-lookup"><span data-stu-id="e1ee1-132">string</span></span><br/>  | <span data-ttu-id="e1ee1-133">non défini</span><span class="sxs-lookup"><span data-stu-id="e1ee1-133">undefined</span></span><br/>       |
| <span data-ttu-id="e1ee1-134">MaxLength</span><span class="sxs-lookup"><span data-stu-id="e1ee1-134">MaxLength</span></span><br/>    | <span data-ttu-id="e1ee1-135">entier</span><span class="sxs-lookup"><span data-stu-id="e1ee1-135">integer</span></span><br/> | <span data-ttu-id="e1ee1-136">non défini</span><span class="sxs-lookup"><span data-stu-id="e1ee1-136">undefined</span></span><br/>       |
| <span data-ttu-id="e1ee1-137">MinLength</span><span class="sxs-lookup"><span data-stu-id="e1ee1-137">MinLength</span></span><br/>    | <span data-ttu-id="e1ee1-138">integer</span><span class="sxs-lookup"><span data-stu-id="e1ee1-138">integer</span></span><br/> | <span data-ttu-id="e1ee1-139">1</span><span class="sxs-lookup"><span data-stu-id="e1ee1-139">1</span></span><br/>               |
| <span data-ttu-id="e1ee1-140">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="e1ee1-140">Mandatory</span></span><br/>    | <span data-ttu-id="e1ee1-141">string</span><span class="sxs-lookup"><span data-stu-id="e1ee1-141">string</span></span><br/>  | <span data-ttu-id="e1ee1-142">PSK : conditionnel</span><span class="sxs-lookup"><span data-stu-id="e1ee1-142">psk:Conditional</span></span><br/> |
| <span data-ttu-id="e1ee1-143">Unité</span><span class="sxs-lookup"><span data-stu-id="e1ee1-143">UnitType</span></span><br/>     | <span data-ttu-id="e1ee1-144">string</span><span class="sxs-lookup"><span data-stu-id="e1ee1-144">string</span></span><br/>  | <span data-ttu-id="e1ee1-145">caractères</span><span class="sxs-lookup"><span data-stu-id="e1ee1-145">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="e1ee1-146">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e1ee1-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e1ee1-147">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="e1ee1-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




