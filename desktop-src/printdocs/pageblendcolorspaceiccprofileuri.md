---
description: En savoir plus sur le paramètre PageBlendColorSpaceICCProfileURI. Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: 05924c7d-e074-4835-b42c-53c77dc1bbb5
title: PageBlendColorSpaceICCProfileURI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50db89757737ff5aa6a1358af418ee33809b960e
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/09/2021
ms.locfileid: "113549317"
---
# <a name="pageblendcolorspaceiccprofileuri"></a><span data-ttu-id="239c8-105">PageBlendColorSpaceICCProfileURI</span><span class="sxs-lookup"><span data-stu-id="239c8-105">PageBlendColorSpaceICCProfileURI</span></span>

<span data-ttu-id="239c8-106">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="239c8-106">This topic is not current.</span></span> <span data-ttu-id="239c8-107">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="239c8-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="239c8-108">Spécifie une référence URI relative à un profil ICC définissant l’espace colorimétrique à utiliser pour la fusion.</span><span class="sxs-lookup"><span data-stu-id="239c8-108">Specifies a relative URI reference to an ICC profile defining the color space that SHOULD be used for blending.</span></span> <span data-ttu-id="239c8-109"><Uri>Est un \_ nom de partie absolu relatif à la racine du package.</span><span class="sxs-lookup"><span data-stu-id="239c8-109">The <Uri> is an absolute part\_name relative to the package root.</span></span>

-   [<span data-ttu-id="239c8-110">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="239c8-110">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="239c8-111">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="239c8-111">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="239c8-112">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="239c8-112">Element Information</span></span>



| <span data-ttu-id="239c8-113">Nom</span><span class="sxs-lookup"><span data-stu-id="239c8-113">Name</span></span> | <span data-ttu-id="239c8-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="239c8-114">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="239c8-115">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="239c8-115">Element Type</span></span> <br/>   | <span data-ttu-id="239c8-116">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="239c8-116">ParameterDef</span></span><br/>                                                                                                                |
| <span data-ttu-id="239c8-117">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="239c8-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="239c8-118">Page</span><span class="sxs-lookup"><span data-stu-id="239c8-118">Page</span></span><br/>                                                                                                                        |
| <span data-ttu-id="239c8-119">Remarques</span><span class="sxs-lookup"><span data-stu-id="239c8-119">Notes</span></span> <br/>          | <span data-ttu-id="239c8-120">Cela s’applique uniquement aux documents XPS et ne doit pas être utilisé dans des des PrintTicket arbitraires.</span><span class="sxs-lookup"><span data-stu-id="239c8-120">This applies to XPS Documents only and should not be used in arbitrary PrintTickets.</span></span> <span data-ttu-id="239c8-121">Lié à l’élément PageBlendColorSpace.</span><span class="sxs-lookup"><span data-stu-id="239c8-121">Linked to PageBlendColorSpace element.</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="239c8-122">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="239c8-122">Structure Content</span></span>

<span data-ttu-id="239c8-123">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="239c8-123">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="239c8-124">Propriétés de structure</span><span class="sxs-lookup"><span data-stu-id="239c8-124">Structure Properties</span></span>

<span data-ttu-id="239c8-125">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="239c8-125">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="239c8-126">Propriété</span><span class="sxs-lookup"><span data-stu-id="239c8-126">Property</span></span>                | <span data-ttu-id="239c8-127">xsi:type</span><span class="sxs-lookup"><span data-stu-id="239c8-127">xsi:type</span></span>           | <span data-ttu-id="239c8-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="239c8-128">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="239c8-129">DataType</span><span class="sxs-lookup"><span data-stu-id="239c8-129">DataType</span></span><br/>     | <span data-ttu-id="239c8-130">string</span><span class="sxs-lookup"><span data-stu-id="239c8-130">string</span></span><br/>  | <span data-ttu-id="239c8-131">xs:string</span><span class="sxs-lookup"><span data-stu-id="239c8-131">xs:string</span></span><br/>       |
| <span data-ttu-id="239c8-132">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="239c8-132">DefaultValue</span></span><br/> | <span data-ttu-id="239c8-133">string</span><span class="sxs-lookup"><span data-stu-id="239c8-133">string</span></span><br/>  | <span data-ttu-id="239c8-134">non défini</span><span class="sxs-lookup"><span data-stu-id="239c8-134">undefined</span></span><br/>       |
| <span data-ttu-id="239c8-135">MaxLength</span><span class="sxs-lookup"><span data-stu-id="239c8-135">MaxLength</span></span><br/>    | <span data-ttu-id="239c8-136">entier</span><span class="sxs-lookup"><span data-stu-id="239c8-136">integer</span></span><br/> | <span data-ttu-id="239c8-137">non défini</span><span class="sxs-lookup"><span data-stu-id="239c8-137">undefined</span></span><br/>       |
| <span data-ttu-id="239c8-138">MinLength</span><span class="sxs-lookup"><span data-stu-id="239c8-138">MinLength</span></span><br/>    | <span data-ttu-id="239c8-139">integer</span><span class="sxs-lookup"><span data-stu-id="239c8-139">integer</span></span><br/> | <span data-ttu-id="239c8-140">1</span><span class="sxs-lookup"><span data-stu-id="239c8-140">1</span></span><br/>               |
| <span data-ttu-id="239c8-141">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="239c8-141">Mandatory</span></span><br/>    | <span data-ttu-id="239c8-142">string</span><span class="sxs-lookup"><span data-stu-id="239c8-142">string</span></span><br/>  | <span data-ttu-id="239c8-143">PSK : conditionnel</span><span class="sxs-lookup"><span data-stu-id="239c8-143">psk:Conditional</span></span><br/> |
| <span data-ttu-id="239c8-144">Unité</span><span class="sxs-lookup"><span data-stu-id="239c8-144">UnitType</span></span><br/>     | <span data-ttu-id="239c8-145">string</span><span class="sxs-lookup"><span data-stu-id="239c8-145">string</span></span><br/>  | <span data-ttu-id="239c8-146">caractères</span><span class="sxs-lookup"><span data-stu-id="239c8-146">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="239c8-147">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="239c8-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="239c8-148">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="239c8-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




