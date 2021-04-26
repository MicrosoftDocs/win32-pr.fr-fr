---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: 05924c7d-e074-4835-b42c-53c77dc1bbb5
title: PageBlendColorSpaceICCProfileURI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cbf1233e172a81053baee0abe1e21d79064045a
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997696"
---
# <a name="pageblendcolorspaceiccprofileuri"></a><span data-ttu-id="b7c02-104">PageBlendColorSpaceICCProfileURI</span><span class="sxs-lookup"><span data-stu-id="b7c02-104">PageBlendColorSpaceICCProfileURI</span></span>

<span data-ttu-id="b7c02-105">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="b7c02-105">This topic is not current.</span></span> <span data-ttu-id="b7c02-106">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="b7c02-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="b7c02-107">Spécifie une référence URI relative à un profil ICC définissant l’espace colorimétrique à utiliser pour la fusion.</span><span class="sxs-lookup"><span data-stu-id="b7c02-107">Specifies a relative URI reference to an ICC profile defining the color space that SHOULD be used for blending.</span></span> <span data-ttu-id="b7c02-108"><Uri>Est un \_ nom de partie absolu relatif à la racine du package.</span><span class="sxs-lookup"><span data-stu-id="b7c02-108">The <Uri> is an absolute part\_name relative to the package root.</span></span>

-   [<span data-ttu-id="b7c02-109">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="b7c02-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="b7c02-110">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="b7c02-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="b7c02-111">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="b7c02-111">Element Information</span></span>



| <span data-ttu-id="b7c02-112">Nom</span><span class="sxs-lookup"><span data-stu-id="b7c02-112">Name</span></span> | <span data-ttu-id="b7c02-113">Value</span><span class="sxs-lookup"><span data-stu-id="b7c02-113">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7c02-114">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="b7c02-114">Element Type</span></span> <br/>   | <span data-ttu-id="b7c02-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="b7c02-115">ParameterDef</span></span><br/>                                                                                                                |
| <span data-ttu-id="b7c02-116">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="b7c02-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="b7c02-117">Page</span><span class="sxs-lookup"><span data-stu-id="b7c02-117">Page</span></span><br/>                                                                                                                        |
| <span data-ttu-id="b7c02-118">Notes</span><span class="sxs-lookup"><span data-stu-id="b7c02-118">Notes</span></span> <br/>          | <span data-ttu-id="b7c02-119">Cela s’applique uniquement aux documents XPS et ne doit pas être utilisé dans des des PrintTicket arbitraires.</span><span class="sxs-lookup"><span data-stu-id="b7c02-119">This applies to XPS Documents only and should not be used in arbitrary PrintTickets.</span></span> <span data-ttu-id="b7c02-120">Lié à l’élément PageBlendColorSpace.</span><span class="sxs-lookup"><span data-stu-id="b7c02-120">Linked to PageBlendColorSpace element.</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="b7c02-121">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="b7c02-121">Structure Content</span></span>

<span data-ttu-id="b7c02-122">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="b7c02-122">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageBlendColorSpaceICCProfileURI">
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

## <a name="structure-properties"></a><span data-ttu-id="b7c02-123">Propriétés de structure</span><span class="sxs-lookup"><span data-stu-id="b7c02-123">Structure Properties</span></span>

<span data-ttu-id="b7c02-124">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="b7c02-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="b7c02-125">Propriété</span><span class="sxs-lookup"><span data-stu-id="b7c02-125">Property</span></span>                | <span data-ttu-id="b7c02-126">xsi:type</span><span class="sxs-lookup"><span data-stu-id="b7c02-126">xsi:type</span></span>           | <span data-ttu-id="b7c02-127">Value</span><span class="sxs-lookup"><span data-stu-id="b7c02-127">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="b7c02-128">DataType</span><span class="sxs-lookup"><span data-stu-id="b7c02-128">DataType</span></span><br/>     | <span data-ttu-id="b7c02-129">string</span><span class="sxs-lookup"><span data-stu-id="b7c02-129">string</span></span><br/>  | <span data-ttu-id="b7c02-130">xs:string</span><span class="sxs-lookup"><span data-stu-id="b7c02-130">xs:string</span></span><br/>       |
| <span data-ttu-id="b7c02-131">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="b7c02-131">DefaultValue</span></span><br/> | <span data-ttu-id="b7c02-132">string</span><span class="sxs-lookup"><span data-stu-id="b7c02-132">string</span></span><br/>  | <span data-ttu-id="b7c02-133">non défini</span><span class="sxs-lookup"><span data-stu-id="b7c02-133">undefined</span></span><br/>       |
| <span data-ttu-id="b7c02-134">MaxLength</span><span class="sxs-lookup"><span data-stu-id="b7c02-134">MaxLength</span></span><br/>    | <span data-ttu-id="b7c02-135">entier</span><span class="sxs-lookup"><span data-stu-id="b7c02-135">integer</span></span><br/> | <span data-ttu-id="b7c02-136">non défini</span><span class="sxs-lookup"><span data-stu-id="b7c02-136">undefined</span></span><br/>       |
| <span data-ttu-id="b7c02-137">MinLength</span><span class="sxs-lookup"><span data-stu-id="b7c02-137">MinLength</span></span><br/>    | <span data-ttu-id="b7c02-138">integer</span><span class="sxs-lookup"><span data-stu-id="b7c02-138">integer</span></span><br/> | <span data-ttu-id="b7c02-139">1</span><span class="sxs-lookup"><span data-stu-id="b7c02-139">1</span></span><br/>               |
| <span data-ttu-id="b7c02-140">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="b7c02-140">Mandatory</span></span><br/>    | <span data-ttu-id="b7c02-141">string</span><span class="sxs-lookup"><span data-stu-id="b7c02-141">string</span></span><br/>  | <span data-ttu-id="b7c02-142">PSK : conditionnel</span><span class="sxs-lookup"><span data-stu-id="b7c02-142">psk:Conditional</span></span><br/> |
| <span data-ttu-id="b7c02-143">Unité</span><span class="sxs-lookup"><span data-stu-id="b7c02-143">UnitType</span></span><br/>     | <span data-ttu-id="b7c02-144">string</span><span class="sxs-lookup"><span data-stu-id="b7c02-144">string</span></span><br/>  | <span data-ttu-id="b7c02-145">caractères</span><span class="sxs-lookup"><span data-stu-id="b7c02-145">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="b7c02-146">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b7c02-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b7c02-147">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="b7c02-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




