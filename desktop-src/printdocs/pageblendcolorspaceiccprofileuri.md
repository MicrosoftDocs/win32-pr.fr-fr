---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: 05924c7d-e074-4835-b42c-53c77dc1bbb5
title: PageBlendColorSpaceICCProfileURI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1f3a6143bd934ebcb75c3e5455a30c7365f1a89
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "104042989"
---
# <a name="pageblendcolorspaceiccprofileuri"></a><span data-ttu-id="1929f-104">PageBlendColorSpaceICCProfileURI</span><span class="sxs-lookup"><span data-stu-id="1929f-104">PageBlendColorSpaceICCProfileURI</span></span>

<span data-ttu-id="1929f-105">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="1929f-105">This topic is not current.</span></span> <span data-ttu-id="1929f-106">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="1929f-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="1929f-107">Spécifie une référence URI relative à un profil ICC définissant l’espace colorimétrique à utiliser pour la fusion.</span><span class="sxs-lookup"><span data-stu-id="1929f-107">Specifies a relative URI reference to an ICC profile defining the color space that SHOULD be used for blending.</span></span> <span data-ttu-id="1929f-108"><Uri>Est un \_ nom de partie absolu relatif à la racine du package.</span><span class="sxs-lookup"><span data-stu-id="1929f-108">The <Uri> is an absolute part\_name relative to the package root.</span></span>

-   [<span data-ttu-id="1929f-109">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="1929f-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="1929f-110">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="1929f-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="1929f-111">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="1929f-111">Element Information</span></span>



| <span data-ttu-id="1929f-112">Nom</span><span class="sxs-lookup"><span data-stu-id="1929f-112">Name</span></span>                       |                                                                                                                                        |
|----------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1929f-113">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="1929f-113">Element Type</span></span> <br/>   | <span data-ttu-id="1929f-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="1929f-114">ParameterDef</span></span><br/>                                                                                                                |
| <span data-ttu-id="1929f-115">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="1929f-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="1929f-116">Page</span><span class="sxs-lookup"><span data-stu-id="1929f-116">Page</span></span><br/>                                                                                                                        |
| <span data-ttu-id="1929f-117">Notes</span><span class="sxs-lookup"><span data-stu-id="1929f-117">Notes</span></span> <br/>          | <span data-ttu-id="1929f-118">Cela s’applique uniquement aux documents XPS et ne doit pas être utilisé dans des des PrintTicket arbitraires.</span><span class="sxs-lookup"><span data-stu-id="1929f-118">This applies to XPS Documents only and should not be used in arbitrary PrintTickets.</span></span> <span data-ttu-id="1929f-119">Lié à l’élément PageBlendColorSpace.</span><span class="sxs-lookup"><span data-stu-id="1929f-119">Linked to PageBlendColorSpace element.</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="1929f-120">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="1929f-120">Structure Content</span></span>

<span data-ttu-id="1929f-121">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="1929f-121">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="1929f-122">Propriétés de structure</span><span class="sxs-lookup"><span data-stu-id="1929f-122">Structure Properties</span></span>

<span data-ttu-id="1929f-123">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="1929f-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="1929f-124">Propriété</span><span class="sxs-lookup"><span data-stu-id="1929f-124">Property</span></span>                | <span data-ttu-id="1929f-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="1929f-125">xsi:type</span></span>           | <span data-ttu-id="1929f-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="1929f-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="1929f-127">DataType</span><span class="sxs-lookup"><span data-stu-id="1929f-127">DataType</span></span><br/>     | <span data-ttu-id="1929f-128">string</span><span class="sxs-lookup"><span data-stu-id="1929f-128">string</span></span><br/>  | <span data-ttu-id="1929f-129">xs:string</span><span class="sxs-lookup"><span data-stu-id="1929f-129">xs:string</span></span><br/>       |
| <span data-ttu-id="1929f-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="1929f-130">DefaultValue</span></span><br/> | <span data-ttu-id="1929f-131">string</span><span class="sxs-lookup"><span data-stu-id="1929f-131">string</span></span><br/>  | <span data-ttu-id="1929f-132">non défini</span><span class="sxs-lookup"><span data-stu-id="1929f-132">undefined</span></span><br/>       |
| <span data-ttu-id="1929f-133">MaxLength</span><span class="sxs-lookup"><span data-stu-id="1929f-133">MaxLength</span></span><br/>    | <span data-ttu-id="1929f-134">entier</span><span class="sxs-lookup"><span data-stu-id="1929f-134">integer</span></span><br/> | <span data-ttu-id="1929f-135">non défini</span><span class="sxs-lookup"><span data-stu-id="1929f-135">undefined</span></span><br/>       |
| <span data-ttu-id="1929f-136">MinLength</span><span class="sxs-lookup"><span data-stu-id="1929f-136">MinLength</span></span><br/>    | <span data-ttu-id="1929f-137">integer</span><span class="sxs-lookup"><span data-stu-id="1929f-137">integer</span></span><br/> | <span data-ttu-id="1929f-138">1</span><span class="sxs-lookup"><span data-stu-id="1929f-138">1</span></span><br/>               |
| <span data-ttu-id="1929f-139">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="1929f-139">Mandatory</span></span><br/>    | <span data-ttu-id="1929f-140">string</span><span class="sxs-lookup"><span data-stu-id="1929f-140">string</span></span><br/>  | <span data-ttu-id="1929f-141">PSK : conditionnel</span><span class="sxs-lookup"><span data-stu-id="1929f-141">psk:Conditional</span></span><br/> |
| <span data-ttu-id="1929f-142">Unité</span><span class="sxs-lookup"><span data-stu-id="1929f-142">UnitType</span></span><br/>     | <span data-ttu-id="1929f-143">string</span><span class="sxs-lookup"><span data-stu-id="1929f-143">string</span></span><br/>  | <span data-ttu-id="1929f-144">caractères</span><span class="sxs-lookup"><span data-stu-id="1929f-144">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="1929f-145">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1929f-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1929f-146">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="1929f-146">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




