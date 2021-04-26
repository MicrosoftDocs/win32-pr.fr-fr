---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: 857caf51-ccf6-415c-aab3-1fed50fa7b34
title: PageMediaSizePSHeight
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96c6ddd593d95ae740a5e03d37e3d79c73e1638b
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107993696"
---
# <a name="pagemediasizepsheight"></a><span data-ttu-id="7b5b1-104">PageMediaSizePSHeight</span><span class="sxs-lookup"><span data-stu-id="7b5b1-104">PageMediaSizePSHeight</span></span>

<span data-ttu-id="7b5b1-105">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="7b5b1-105">This topic is not current.</span></span> <span data-ttu-id="7b5b1-106">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="7b5b1-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="7b5b1-107">Spécifie la hauteur de la page, parallèle à la direction de l’orientation du flux (référence [PostScript Printer Description file format Specification](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)).</span><span class="sxs-lookup"><span data-stu-id="7b5b1-107">Specifies the height of the page, parallel to the feed-orientation direction (Reference [PostScript Printer Description File Format Specification](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)).</span></span>

-   [<span data-ttu-id="7b5b1-108">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="7b5b1-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="7b5b1-109">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="7b5b1-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="7b5b1-110">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="7b5b1-110">Element Information</span></span>



| <span data-ttu-id="7b5b1-111">Nom</span><span class="sxs-lookup"><span data-stu-id="7b5b1-111">Name</span></span> | <span data-ttu-id="7b5b1-112">Value</span><span class="sxs-lookup"><span data-stu-id="7b5b1-112">Value</span></span> |
|----------------------------|-------------------------------------------------------------|
| <span data-ttu-id="7b5b1-113">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="7b5b1-113">Element Type</span></span> <br/>   | <span data-ttu-id="7b5b1-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="7b5b1-114">ParameterDef</span></span><br/>                                     |
| <span data-ttu-id="7b5b1-115">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="7b5b1-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="7b5b1-116">Page</span><span class="sxs-lookup"><span data-stu-id="7b5b1-116">Page</span></span><br/>                                             |
| <span data-ttu-id="7b5b1-117">Notes</span><span class="sxs-lookup"><span data-stu-id="7b5b1-117">Notes</span></span> <br/>          | <span data-ttu-id="7b5b1-118">Lié à l’élément PageMediaSize, option CustomPS</span><span class="sxs-lookup"><span data-stu-id="7b5b1-118">Linked to PageMediaSize element, CustomPS option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="7b5b1-119">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="7b5b1-119">Structure Content</span></span>

<span data-ttu-id="7b5b1-120">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="7b5b1-120">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageMediaSizePSHeight">
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

## <a name="structure-properties"></a><span data-ttu-id="7b5b1-121">Propriétés de structure</span><span class="sxs-lookup"><span data-stu-id="7b5b1-121">Structure Properties</span></span>

<span data-ttu-id="7b5b1-122">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="7b5b1-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="7b5b1-123">Propriété</span><span class="sxs-lookup"><span data-stu-id="7b5b1-123">Property</span></span>                | <span data-ttu-id="7b5b1-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="7b5b1-124">xsi:type</span></span>           | <span data-ttu-id="7b5b1-125">Value</span><span class="sxs-lookup"><span data-stu-id="7b5b1-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="7b5b1-126">DataType</span><span class="sxs-lookup"><span data-stu-id="7b5b1-126">DataType</span></span><br/>     | <span data-ttu-id="7b5b1-127">string</span><span class="sxs-lookup"><span data-stu-id="7b5b1-127">string</span></span><br/>  | <span data-ttu-id="7b5b1-128">xs:integer</span><span class="sxs-lookup"><span data-stu-id="7b5b1-128">xs:integer</span></span><br/>      |
| <span data-ttu-id="7b5b1-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="7b5b1-129">DefaultValue</span></span><br/> | <span data-ttu-id="7b5b1-130">entier</span><span class="sxs-lookup"><span data-stu-id="7b5b1-130">integer</span></span><br/> | <span data-ttu-id="7b5b1-131">non défini</span><span class="sxs-lookup"><span data-stu-id="7b5b1-131">undefined</span></span><br/>       |
| <span data-ttu-id="7b5b1-132">MaxValue</span><span class="sxs-lookup"><span data-stu-id="7b5b1-132">MaxValue</span></span><br/>     | <span data-ttu-id="7b5b1-133">entier</span><span class="sxs-lookup"><span data-stu-id="7b5b1-133">integer</span></span><br/> | <span data-ttu-id="7b5b1-134">non défini</span><span class="sxs-lookup"><span data-stu-id="7b5b1-134">undefined</span></span><br/>       |
| <span data-ttu-id="7b5b1-135">MinValue</span><span class="sxs-lookup"><span data-stu-id="7b5b1-135">MinValue</span></span><br/>     | <span data-ttu-id="7b5b1-136">entier</span><span class="sxs-lookup"><span data-stu-id="7b5b1-136">integer</span></span><br/> | <span data-ttu-id="7b5b1-137">non défini</span><span class="sxs-lookup"><span data-stu-id="7b5b1-137">undefined</span></span><br/>       |
| <span data-ttu-id="7b5b1-138">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="7b5b1-138">Mandatory</span></span><br/>    | <span data-ttu-id="7b5b1-139">string</span><span class="sxs-lookup"><span data-stu-id="7b5b1-139">string</span></span><br/>  | <span data-ttu-id="7b5b1-140">PSK : conditionnel</span><span class="sxs-lookup"><span data-stu-id="7b5b1-140">psk:Conditional</span></span><br/> |
| <span data-ttu-id="7b5b1-141">Plusieurs</span><span class="sxs-lookup"><span data-stu-id="7b5b1-141">Multiple</span></span><br/>     | <span data-ttu-id="7b5b1-142">integer</span><span class="sxs-lookup"><span data-stu-id="7b5b1-142">integer</span></span><br/> | <span data-ttu-id="7b5b1-143">1</span><span class="sxs-lookup"><span data-stu-id="7b5b1-143">1</span></span><br/>               |
| <span data-ttu-id="7b5b1-144">Unité</span><span class="sxs-lookup"><span data-stu-id="7b5b1-144">UnitType</span></span><br/>     | <span data-ttu-id="7b5b1-145">string</span><span class="sxs-lookup"><span data-stu-id="7b5b1-145">string</span></span><br/>  | <span data-ttu-id="7b5b1-146">microns</span><span class="sxs-lookup"><span data-stu-id="7b5b1-146">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="7b5b1-147">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7b5b1-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7b5b1-148">Spécification de format de fichier de description d’imprimante PostScript</span><span class="sxs-lookup"><span data-stu-id="7b5b1-148">PostScript Printer Description File Format Specification</span></span>](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)
</dt> <dt>

[<span data-ttu-id="7b5b1-149">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="7b5b1-149">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




