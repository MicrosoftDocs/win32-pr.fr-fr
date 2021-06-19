---
description: Obtenir des informations sur le paramètre PageMediaSizePSHeightOffset. Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: e86d6a5d-484d-4c80-8c86-7d12d287ee21
title: PageMediaSizePSHeightOffset
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5e2c0e3802a6c461fe2f9eec68b28677c254be9
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395734"
---
# <a name="pagemediasizepsheightoffset"></a><span data-ttu-id="08de9-105">PageMediaSizePSHeightOffset</span><span class="sxs-lookup"><span data-stu-id="08de9-105">PageMediaSizePSHeightOffset</span></span>

<span data-ttu-id="08de9-106">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="08de9-106">This topic is not current.</span></span> <span data-ttu-id="08de9-107">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="08de9-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="08de9-108">Spécifie le décalage, parallèle à la direction de l’orientation du flux ( [spécification du format du fichier de description d’imprimante PostScript](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)de référence).</span><span class="sxs-lookup"><span data-stu-id="08de9-108">Specifies the offset, parallel to the feed-orientation direction (Reference [PostScript Printer Description File Format Specification](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)).</span></span>

-   [<span data-ttu-id="08de9-109">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="08de9-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="08de9-110">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="08de9-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="08de9-111">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="08de9-111">Element Information</span></span>



| <span data-ttu-id="08de9-112">Nom</span><span class="sxs-lookup"><span data-stu-id="08de9-112">Name</span></span> | <span data-ttu-id="08de9-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="08de9-113">Value</span></span> |
|----------------------------|-------------------------------------------------------------|
| <span data-ttu-id="08de9-114">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="08de9-114">Element Type</span></span> <br/>   | <span data-ttu-id="08de9-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="08de9-115">ParameterDef</span></span><br/>                                     |
| <span data-ttu-id="08de9-116">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="08de9-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="08de9-117">Page</span><span class="sxs-lookup"><span data-stu-id="08de9-117">Page</span></span><br/>                                             |
| <span data-ttu-id="08de9-118">Notes</span><span class="sxs-lookup"><span data-stu-id="08de9-118">Notes</span></span> <br/>          | <span data-ttu-id="08de9-119">Lié à l’élément PageMediaSize, option CustomPS</span><span class="sxs-lookup"><span data-stu-id="08de9-119">Linked to PageMediaSize element, CustomPS option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="08de9-120">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="08de9-120">Structure Content</span></span>

<span data-ttu-id="08de9-121">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="08de9-121">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="08de9-122">Propriétés de structure</span><span class="sxs-lookup"><span data-stu-id="08de9-122">Structure Properties</span></span>

<span data-ttu-id="08de9-123">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="08de9-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="08de9-124">Propriété</span><span class="sxs-lookup"><span data-stu-id="08de9-124">Property</span></span>                | <span data-ttu-id="08de9-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="08de9-125">xsi:type</span></span>           | <span data-ttu-id="08de9-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="08de9-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="08de9-127">DataType</span><span class="sxs-lookup"><span data-stu-id="08de9-127">DataType</span></span><br/>     | <span data-ttu-id="08de9-128">string</span><span class="sxs-lookup"><span data-stu-id="08de9-128">string</span></span><br/>  | <span data-ttu-id="08de9-129">xs:integer</span><span class="sxs-lookup"><span data-stu-id="08de9-129">xs:integer</span></span><br/>      |
| <span data-ttu-id="08de9-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="08de9-130">DefaultValue</span></span><br/> | <span data-ttu-id="08de9-131">entier</span><span class="sxs-lookup"><span data-stu-id="08de9-131">integer</span></span><br/> | <span data-ttu-id="08de9-132">non défini</span><span class="sxs-lookup"><span data-stu-id="08de9-132">undefined</span></span><br/>       |
| <span data-ttu-id="08de9-133">MaxValue</span><span class="sxs-lookup"><span data-stu-id="08de9-133">MaxValue</span></span><br/>     | <span data-ttu-id="08de9-134">entier</span><span class="sxs-lookup"><span data-stu-id="08de9-134">integer</span></span><br/> | <span data-ttu-id="08de9-135">non défini</span><span class="sxs-lookup"><span data-stu-id="08de9-135">undefined</span></span><br/>       |
| <span data-ttu-id="08de9-136">MinValue</span><span class="sxs-lookup"><span data-stu-id="08de9-136">MinValue</span></span><br/>     | <span data-ttu-id="08de9-137">entier</span><span class="sxs-lookup"><span data-stu-id="08de9-137">integer</span></span><br/> | <span data-ttu-id="08de9-138">non défini</span><span class="sxs-lookup"><span data-stu-id="08de9-138">undefined</span></span><br/>       |
| <span data-ttu-id="08de9-139">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="08de9-139">Mandatory</span></span><br/>    | <span data-ttu-id="08de9-140">string</span><span class="sxs-lookup"><span data-stu-id="08de9-140">string</span></span><br/>  | <span data-ttu-id="08de9-141">PSK : conditionnel</span><span class="sxs-lookup"><span data-stu-id="08de9-141">psk:Conditional</span></span><br/> |
| <span data-ttu-id="08de9-142">Multiple</span><span class="sxs-lookup"><span data-stu-id="08de9-142">Multiple</span></span><br/>     | <span data-ttu-id="08de9-143">integer</span><span class="sxs-lookup"><span data-stu-id="08de9-143">integer</span></span><br/> | <span data-ttu-id="08de9-144">1</span><span class="sxs-lookup"><span data-stu-id="08de9-144">1</span></span><br/>               |
| <span data-ttu-id="08de9-145">Unité</span><span class="sxs-lookup"><span data-stu-id="08de9-145">UnitType</span></span><br/>     | <span data-ttu-id="08de9-146">string</span><span class="sxs-lookup"><span data-stu-id="08de9-146">string</span></span><br/>  | <span data-ttu-id="08de9-147">microns</span><span class="sxs-lookup"><span data-stu-id="08de9-147">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="08de9-148">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="08de9-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="08de9-149">Spécification de format de fichier de description d’imprimante PostScript</span><span class="sxs-lookup"><span data-stu-id="08de9-149">PostScript Printer Description File Format Specification</span></span>](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)
</dt> <dt>

[<span data-ttu-id="08de9-150">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="08de9-150">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




