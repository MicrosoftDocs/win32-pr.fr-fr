---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: b2a4a4d2-a8bc-48dc-ad56-20380f5f91c9
title: PageDestinationColorProfileURI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fff2ca269eaed9331f6c2077e6b396cca5a01c4
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "106545219"
---
# <a name="pagedestinationcolorprofileuri"></a><span data-ttu-id="b7bee-104">PageDestinationColorProfileURI</span><span class="sxs-lookup"><span data-stu-id="b7bee-104">PageDestinationColorProfileURI</span></span>

<span data-ttu-id="b7bee-105">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="b7bee-105">This topic is not current.</span></span> <span data-ttu-id="b7bee-106">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="b7bee-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="b7bee-107">Spécifie une référence URI relative à un profil ICC contenu dans un document XPS.</span><span class="sxs-lookup"><span data-stu-id="b7bee-107">Specifies a relative URI reference to an ICC profile contained in an XPS Document.</span></span> <span data-ttu-id="b7bee-108">Le traitement de cette option dépend de la configuration de la fonctionnalité PageDeviceColorSpaceUsage.</span><span class="sxs-lookup"><span data-stu-id="b7bee-108">The processing of this option depends of the setting of the PageDeviceColorSpaceUsage feature.</span></span> <span data-ttu-id="b7bee-109">Tous les éléments qui utilisent ce profil sont supposés être déjà dans l’espace de couleurs approprié du périphérique et ne sont pas gérés par la couleur dans le pilote ou le périphérique.</span><span class="sxs-lookup"><span data-stu-id="b7bee-109">All elements using that profile are assumed to be already in the appropriate device color space, and will not be color managed in the driver or device.</span></span>

-   [<span data-ttu-id="b7bee-110">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="b7bee-110">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="b7bee-111">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="b7bee-111">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="b7bee-112">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="b7bee-112">Element Information</span></span>



| <span data-ttu-id="b7bee-113">Nom</span><span class="sxs-lookup"><span data-stu-id="b7bee-113">Name</span></span>                       |                                                          |
|----------------------------|----------------------------------------------------------|
| <span data-ttu-id="b7bee-114">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="b7bee-114">Element Type</span></span> <br/>   | <span data-ttu-id="b7bee-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="b7bee-115">ParameterDef</span></span><br/>                                  |
| <span data-ttu-id="b7bee-116">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="b7bee-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="b7bee-117">Page</span><span class="sxs-lookup"><span data-stu-id="b7bee-117">Page</span></span><br/>                                          |
| <span data-ttu-id="b7bee-118">Notes</span><span class="sxs-lookup"><span data-stu-id="b7bee-118">Notes</span></span> <br/>          | <span data-ttu-id="b7bee-119">Lié à l’élément PageDestinationColorProfile</span><span class="sxs-lookup"><span data-stu-id="b7bee-119">Linked to PageDestinationColorProfile element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="b7bee-120">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="b7bee-120">Structure Content</span></span>

<span data-ttu-id="b7bee-121">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="b7bee-121">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="b7bee-122">Propriétés de structure</span><span class="sxs-lookup"><span data-stu-id="b7bee-122">Structure Properties</span></span>

<span data-ttu-id="b7bee-123">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="b7bee-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="b7bee-124">Propriété</span><span class="sxs-lookup"><span data-stu-id="b7bee-124">Property</span></span>                | <span data-ttu-id="b7bee-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="b7bee-125">xsi:type</span></span>           | <span data-ttu-id="b7bee-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="b7bee-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="b7bee-127">DataType</span><span class="sxs-lookup"><span data-stu-id="b7bee-127">DataType</span></span><br/>     | <span data-ttu-id="b7bee-128">string</span><span class="sxs-lookup"><span data-stu-id="b7bee-128">string</span></span><br/>  | <span data-ttu-id="b7bee-129">xs:string</span><span class="sxs-lookup"><span data-stu-id="b7bee-129">xs:string</span></span><br/>       |
| <span data-ttu-id="b7bee-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="b7bee-130">DefaultValue</span></span><br/> | <span data-ttu-id="b7bee-131">string</span><span class="sxs-lookup"><span data-stu-id="b7bee-131">string</span></span><br/>  | <span data-ttu-id="b7bee-132">non défini</span><span class="sxs-lookup"><span data-stu-id="b7bee-132">undefined</span></span><br/>       |
| <span data-ttu-id="b7bee-133">MaxLength</span><span class="sxs-lookup"><span data-stu-id="b7bee-133">MaxLength</span></span><br/>    | <span data-ttu-id="b7bee-134">entier</span><span class="sxs-lookup"><span data-stu-id="b7bee-134">integer</span></span><br/> | <span data-ttu-id="b7bee-135">non défini</span><span class="sxs-lookup"><span data-stu-id="b7bee-135">undefined</span></span><br/>       |
| <span data-ttu-id="b7bee-136">MinLength</span><span class="sxs-lookup"><span data-stu-id="b7bee-136">MinLength</span></span><br/>    | <span data-ttu-id="b7bee-137">integer</span><span class="sxs-lookup"><span data-stu-id="b7bee-137">integer</span></span><br/> | <span data-ttu-id="b7bee-138">1</span><span class="sxs-lookup"><span data-stu-id="b7bee-138">1</span></span><br/>               |
| <span data-ttu-id="b7bee-139">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="b7bee-139">Mandatory</span></span><br/>    | <span data-ttu-id="b7bee-140">string</span><span class="sxs-lookup"><span data-stu-id="b7bee-140">string</span></span><br/>  | <span data-ttu-id="b7bee-141">PSK : conditionnel</span><span class="sxs-lookup"><span data-stu-id="b7bee-141">psk:Conditional</span></span><br/> |
| <span data-ttu-id="b7bee-142">Unité</span><span class="sxs-lookup"><span data-stu-id="b7bee-142">UnitType</span></span><br/>     | <span data-ttu-id="b7bee-143">string</span><span class="sxs-lookup"><span data-stu-id="b7bee-143">string</span></span><br/>  | <span data-ttu-id="b7bee-144">caractères</span><span class="sxs-lookup"><span data-stu-id="b7bee-144">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="b7bee-145">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b7bee-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b7bee-146">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="b7bee-146">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




