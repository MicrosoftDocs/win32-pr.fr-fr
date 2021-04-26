---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: a1a684ce-5615-4ff7-a7aa-5c9f786f84ed
title: PageMediaSizePSWidth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f4399b75f047c2705983c893075995800396120
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997546"
---
# <a name="pagemediasizepswidth"></a><span data-ttu-id="75404-104">PageMediaSizePSWidth</span><span class="sxs-lookup"><span data-stu-id="75404-104">PageMediaSizePSWidth</span></span>

<span data-ttu-id="75404-105">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="75404-105">This topic is not current.</span></span> <span data-ttu-id="75404-106">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="75404-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="75404-107">Spécifie la largeur de la page perpendiculairement au sens de l’orientation du flux (référence [PostScript Printer Description file format Specification](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)).</span><span class="sxs-lookup"><span data-stu-id="75404-107">Specifies the width of the page perpendicular to the feed-orientation direction (Reference [PostScript Printer Description File Format Specification](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)).</span></span>

-   [<span data-ttu-id="75404-108">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="75404-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="75404-109">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="75404-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="75404-110">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="75404-110">Element Information</span></span>



| <span data-ttu-id="75404-111">Nom</span><span class="sxs-lookup"><span data-stu-id="75404-111">Name</span></span> | <span data-ttu-id="75404-112">Value</span><span class="sxs-lookup"><span data-stu-id="75404-112">Value</span></span> |
|----------------------------|-------------------------------------------------------------|
| <span data-ttu-id="75404-113">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="75404-113">Element Type</span></span> <br/>   | <span data-ttu-id="75404-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="75404-114">ParameterDef</span></span><br/>                                     |
| <span data-ttu-id="75404-115">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="75404-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="75404-116">Page</span><span class="sxs-lookup"><span data-stu-id="75404-116">Page</span></span><br/>                                             |
| <span data-ttu-id="75404-117">Notes</span><span class="sxs-lookup"><span data-stu-id="75404-117">Notes</span></span> <br/>          | <span data-ttu-id="75404-118">Lié à l’élément PageMediaSize, option CustomPS</span><span class="sxs-lookup"><span data-stu-id="75404-118">Linked to PageMediaSize element, CustomPS option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="75404-119">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="75404-119">Structure Content</span></span>

<span data-ttu-id="75404-120">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="75404-120">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageMediaSizePSWidth">
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

## <a name="structure-properties"></a><span data-ttu-id="75404-121">Propriétés de structure</span><span class="sxs-lookup"><span data-stu-id="75404-121">Structure Properties</span></span>

<span data-ttu-id="75404-122">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="75404-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="75404-123">Propriété</span><span class="sxs-lookup"><span data-stu-id="75404-123">Property</span></span>                | <span data-ttu-id="75404-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="75404-124">xsi:type</span></span>           | <span data-ttu-id="75404-125">Value</span><span class="sxs-lookup"><span data-stu-id="75404-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="75404-126">DataType</span><span class="sxs-lookup"><span data-stu-id="75404-126">DataType</span></span><br/>     | <span data-ttu-id="75404-127">string</span><span class="sxs-lookup"><span data-stu-id="75404-127">string</span></span><br/>  | <span data-ttu-id="75404-128">xs:integer</span><span class="sxs-lookup"><span data-stu-id="75404-128">xs:integer</span></span><br/>      |
| <span data-ttu-id="75404-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="75404-129">DefaultValue</span></span><br/> | <span data-ttu-id="75404-130">entier</span><span class="sxs-lookup"><span data-stu-id="75404-130">integer</span></span><br/> | <span data-ttu-id="75404-131">non défini</span><span class="sxs-lookup"><span data-stu-id="75404-131">undefined</span></span><br/>       |
| <span data-ttu-id="75404-132">MaxValue</span><span class="sxs-lookup"><span data-stu-id="75404-132">MaxValue</span></span><br/>     | <span data-ttu-id="75404-133">entier</span><span class="sxs-lookup"><span data-stu-id="75404-133">integer</span></span><br/> | <span data-ttu-id="75404-134">non défini</span><span class="sxs-lookup"><span data-stu-id="75404-134">undefined</span></span><br/>       |
| <span data-ttu-id="75404-135">MinValue</span><span class="sxs-lookup"><span data-stu-id="75404-135">MinValue</span></span><br/>     | <span data-ttu-id="75404-136">entier</span><span class="sxs-lookup"><span data-stu-id="75404-136">integer</span></span><br/> | <span data-ttu-id="75404-137">non défini</span><span class="sxs-lookup"><span data-stu-id="75404-137">undefined</span></span><br/>       |
| <span data-ttu-id="75404-138">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="75404-138">Mandatory</span></span><br/>    | <span data-ttu-id="75404-139">string</span><span class="sxs-lookup"><span data-stu-id="75404-139">string</span></span><br/>  | <span data-ttu-id="75404-140">PSK : conditionnel</span><span class="sxs-lookup"><span data-stu-id="75404-140">psk:Conditional</span></span><br/> |
| <span data-ttu-id="75404-141">Plusieurs</span><span class="sxs-lookup"><span data-stu-id="75404-141">Multiple</span></span><br/>     | <span data-ttu-id="75404-142">integer</span><span class="sxs-lookup"><span data-stu-id="75404-142">integer</span></span><br/> | <span data-ttu-id="75404-143">1</span><span class="sxs-lookup"><span data-stu-id="75404-143">1</span></span><br/>               |
| <span data-ttu-id="75404-144">Unité</span><span class="sxs-lookup"><span data-stu-id="75404-144">UnitType</span></span><br/>     | <span data-ttu-id="75404-145">string</span><span class="sxs-lookup"><span data-stu-id="75404-145">string</span></span><br/>  | <span data-ttu-id="75404-146">microns</span><span class="sxs-lookup"><span data-stu-id="75404-146">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="75404-147">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="75404-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="75404-148">Spécification de format de fichier de description d’imprimante PostScript</span><span class="sxs-lookup"><span data-stu-id="75404-148">PostScript Printer Description File Format Specification</span></span>](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)
</dt> <dt>

[<span data-ttu-id="75404-149">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="75404-149">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




