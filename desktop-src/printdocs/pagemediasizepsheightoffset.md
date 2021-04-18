---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: e86d6a5d-484d-4c80-8c86-7d12d287ee21
title: PageMediaSizePSHeightOffset
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e02129d5c8c20fceef01a9cd5cf40e5827374a7
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "106522752"
---
# <a name="pagemediasizepsheightoffset"></a><span data-ttu-id="d5b5b-104">PageMediaSizePSHeightOffset</span><span class="sxs-lookup"><span data-stu-id="d5b5b-104">PageMediaSizePSHeightOffset</span></span>

<span data-ttu-id="d5b5b-105">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="d5b5b-105">This topic is not current.</span></span> <span data-ttu-id="d5b5b-106">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="d5b5b-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="d5b5b-107">Spécifie le décalage, parallèle à la direction de l’orientation du flux ( [spécification du format du fichier de description d’imprimante PostScript](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)de référence).</span><span class="sxs-lookup"><span data-stu-id="d5b5b-107">Specifies the offset, parallel to the feed-orientation direction (Reference [PostScript Printer Description File Format Specification](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)).</span></span>

-   [<span data-ttu-id="d5b5b-108">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="d5b5b-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="d5b5b-109">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="d5b5b-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="d5b5b-110">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="d5b5b-110">Element Information</span></span>



| <span data-ttu-id="d5b5b-111">Nom</span><span class="sxs-lookup"><span data-stu-id="d5b5b-111">Name</span></span>                       |                                                             |
|----------------------------|-------------------------------------------------------------|
| <span data-ttu-id="d5b5b-112">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="d5b5b-112">Element Type</span></span> <br/>   | <span data-ttu-id="d5b5b-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="d5b5b-113">ParameterDef</span></span><br/>                                     |
| <span data-ttu-id="d5b5b-114">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="d5b5b-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="d5b5b-115">Page</span><span class="sxs-lookup"><span data-stu-id="d5b5b-115">Page</span></span><br/>                                             |
| <span data-ttu-id="d5b5b-116">Notes</span><span class="sxs-lookup"><span data-stu-id="d5b5b-116">Notes</span></span> <br/>          | <span data-ttu-id="d5b5b-117">Lié à l’élément PageMediaSize, option CustomPS</span><span class="sxs-lookup"><span data-stu-id="d5b5b-117">Linked to PageMediaSize element, CustomPS option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="d5b5b-118">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="d5b5b-118">Structure Content</span></span>

<span data-ttu-id="d5b5b-119">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="d5b5b-119">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageMediaSizePSHeightOffset">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:integer</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxValue">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinValue">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Multiple">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Conditional</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">microns</psf:Value>
  </psf:Property>
</psf:ParameterDef>
      
```

## <a name="structure-properties"></a><span data-ttu-id="d5b5b-120">Propriétés de structure</span><span class="sxs-lookup"><span data-stu-id="d5b5b-120">Structure Properties</span></span>

<span data-ttu-id="d5b5b-121">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="d5b5b-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="d5b5b-122">Propriété</span><span class="sxs-lookup"><span data-stu-id="d5b5b-122">Property</span></span>                | <span data-ttu-id="d5b5b-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="d5b5b-123">xsi:type</span></span>           | <span data-ttu-id="d5b5b-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="d5b5b-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="d5b5b-125">DataType</span><span class="sxs-lookup"><span data-stu-id="d5b5b-125">DataType</span></span><br/>     | <span data-ttu-id="d5b5b-126">string</span><span class="sxs-lookup"><span data-stu-id="d5b5b-126">string</span></span><br/>  | <span data-ttu-id="d5b5b-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="d5b5b-127">xs:integer</span></span><br/>      |
| <span data-ttu-id="d5b5b-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="d5b5b-128">DefaultValue</span></span><br/> | <span data-ttu-id="d5b5b-129">entier</span><span class="sxs-lookup"><span data-stu-id="d5b5b-129">integer</span></span><br/> | <span data-ttu-id="d5b5b-130">non défini</span><span class="sxs-lookup"><span data-stu-id="d5b5b-130">undefined</span></span><br/>       |
| <span data-ttu-id="d5b5b-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="d5b5b-131">MaxValue</span></span><br/>     | <span data-ttu-id="d5b5b-132">entier</span><span class="sxs-lookup"><span data-stu-id="d5b5b-132">integer</span></span><br/> | <span data-ttu-id="d5b5b-133">non défini</span><span class="sxs-lookup"><span data-stu-id="d5b5b-133">undefined</span></span><br/>       |
| <span data-ttu-id="d5b5b-134">MinValue</span><span class="sxs-lookup"><span data-stu-id="d5b5b-134">MinValue</span></span><br/>     | <span data-ttu-id="d5b5b-135">entier</span><span class="sxs-lookup"><span data-stu-id="d5b5b-135">integer</span></span><br/> | <span data-ttu-id="d5b5b-136">non défini</span><span class="sxs-lookup"><span data-stu-id="d5b5b-136">undefined</span></span><br/>       |
| <span data-ttu-id="d5b5b-137">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="d5b5b-137">Mandatory</span></span><br/>    | <span data-ttu-id="d5b5b-138">string</span><span class="sxs-lookup"><span data-stu-id="d5b5b-138">string</span></span><br/>  | <span data-ttu-id="d5b5b-139">PSK : conditionnel</span><span class="sxs-lookup"><span data-stu-id="d5b5b-139">psk:Conditional</span></span><br/> |
| <span data-ttu-id="d5b5b-140">Multiple</span><span class="sxs-lookup"><span data-stu-id="d5b5b-140">Multiple</span></span><br/>     | <span data-ttu-id="d5b5b-141">integer</span><span class="sxs-lookup"><span data-stu-id="d5b5b-141">integer</span></span><br/> | <span data-ttu-id="d5b5b-142">1</span><span class="sxs-lookup"><span data-stu-id="d5b5b-142">1</span></span><br/>               |
| <span data-ttu-id="d5b5b-143">Unité</span><span class="sxs-lookup"><span data-stu-id="d5b5b-143">UnitType</span></span><br/>     | <span data-ttu-id="d5b5b-144">string</span><span class="sxs-lookup"><span data-stu-id="d5b5b-144">string</span></span><br/>  | <span data-ttu-id="d5b5b-145">microns</span><span class="sxs-lookup"><span data-stu-id="d5b5b-145">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="d5b5b-146">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d5b5b-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d5b5b-147">Spécification de format de fichier de description d’imprimante PostScript</span><span class="sxs-lookup"><span data-stu-id="d5b5b-147">PostScript Printer Description File Format Specification</span></span>](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)
</dt> <dt>

[<span data-ttu-id="d5b5b-148">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="d5b5b-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




