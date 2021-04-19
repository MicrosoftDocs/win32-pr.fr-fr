---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: 857caf51-ccf6-415c-aab3-1fed50fa7b34
title: PageMediaSizePSHeight
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1cb576ce7d623f4d036db1332b0339e6cef518d3
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "106538266"
---
# <a name="pagemediasizepsheight"></a><span data-ttu-id="47a14-104">PageMediaSizePSHeight</span><span class="sxs-lookup"><span data-stu-id="47a14-104">PageMediaSizePSHeight</span></span>

<span data-ttu-id="47a14-105">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="47a14-105">This topic is not current.</span></span> <span data-ttu-id="47a14-106">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="47a14-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="47a14-107">Spécifie la hauteur de la page, parallèle à la direction de l’orientation du flux (référence [PostScript Printer Description file format Specification](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)).</span><span class="sxs-lookup"><span data-stu-id="47a14-107">Specifies the height of the page, parallel to the feed-orientation direction (Reference [PostScript Printer Description File Format Specification](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)).</span></span>

-   [<span data-ttu-id="47a14-108">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="47a14-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="47a14-109">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="47a14-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="47a14-110">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="47a14-110">Element Information</span></span>



| <span data-ttu-id="47a14-111">Nom</span><span class="sxs-lookup"><span data-stu-id="47a14-111">Name</span></span>                       |                                                             |
|----------------------------|-------------------------------------------------------------|
| <span data-ttu-id="47a14-112">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="47a14-112">Element Type</span></span> <br/>   | <span data-ttu-id="47a14-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="47a14-113">ParameterDef</span></span><br/>                                     |
| <span data-ttu-id="47a14-114">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="47a14-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="47a14-115">Page</span><span class="sxs-lookup"><span data-stu-id="47a14-115">Page</span></span><br/>                                             |
| <span data-ttu-id="47a14-116">Notes</span><span class="sxs-lookup"><span data-stu-id="47a14-116">Notes</span></span> <br/>          | <span data-ttu-id="47a14-117">Lié à l’élément PageMediaSize, option CustomPS</span><span class="sxs-lookup"><span data-stu-id="47a14-117">Linked to PageMediaSize element, CustomPS option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="47a14-118">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="47a14-118">Structure Content</span></span>

<span data-ttu-id="47a14-119">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="47a14-119">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="47a14-120">Propriétés de structure</span><span class="sxs-lookup"><span data-stu-id="47a14-120">Structure Properties</span></span>

<span data-ttu-id="47a14-121">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="47a14-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="47a14-122">Propriété</span><span class="sxs-lookup"><span data-stu-id="47a14-122">Property</span></span>                | <span data-ttu-id="47a14-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="47a14-123">xsi:type</span></span>           | <span data-ttu-id="47a14-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="47a14-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="47a14-125">DataType</span><span class="sxs-lookup"><span data-stu-id="47a14-125">DataType</span></span><br/>     | <span data-ttu-id="47a14-126">string</span><span class="sxs-lookup"><span data-stu-id="47a14-126">string</span></span><br/>  | <span data-ttu-id="47a14-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="47a14-127">xs:integer</span></span><br/>      |
| <span data-ttu-id="47a14-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="47a14-128">DefaultValue</span></span><br/> | <span data-ttu-id="47a14-129">entier</span><span class="sxs-lookup"><span data-stu-id="47a14-129">integer</span></span><br/> | <span data-ttu-id="47a14-130">non défini</span><span class="sxs-lookup"><span data-stu-id="47a14-130">undefined</span></span><br/>       |
| <span data-ttu-id="47a14-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="47a14-131">MaxValue</span></span><br/>     | <span data-ttu-id="47a14-132">entier</span><span class="sxs-lookup"><span data-stu-id="47a14-132">integer</span></span><br/> | <span data-ttu-id="47a14-133">non défini</span><span class="sxs-lookup"><span data-stu-id="47a14-133">undefined</span></span><br/>       |
| <span data-ttu-id="47a14-134">MinValue</span><span class="sxs-lookup"><span data-stu-id="47a14-134">MinValue</span></span><br/>     | <span data-ttu-id="47a14-135">entier</span><span class="sxs-lookup"><span data-stu-id="47a14-135">integer</span></span><br/> | <span data-ttu-id="47a14-136">non défini</span><span class="sxs-lookup"><span data-stu-id="47a14-136">undefined</span></span><br/>       |
| <span data-ttu-id="47a14-137">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="47a14-137">Mandatory</span></span><br/>    | <span data-ttu-id="47a14-138">string</span><span class="sxs-lookup"><span data-stu-id="47a14-138">string</span></span><br/>  | <span data-ttu-id="47a14-139">PSK : conditionnel</span><span class="sxs-lookup"><span data-stu-id="47a14-139">psk:Conditional</span></span><br/> |
| <span data-ttu-id="47a14-140">Multiple</span><span class="sxs-lookup"><span data-stu-id="47a14-140">Multiple</span></span><br/>     | <span data-ttu-id="47a14-141">integer</span><span class="sxs-lookup"><span data-stu-id="47a14-141">integer</span></span><br/> | <span data-ttu-id="47a14-142">1</span><span class="sxs-lookup"><span data-stu-id="47a14-142">1</span></span><br/>               |
| <span data-ttu-id="47a14-143">Unité</span><span class="sxs-lookup"><span data-stu-id="47a14-143">UnitType</span></span><br/>     | <span data-ttu-id="47a14-144">string</span><span class="sxs-lookup"><span data-stu-id="47a14-144">string</span></span><br/>  | <span data-ttu-id="47a14-145">microns</span><span class="sxs-lookup"><span data-stu-id="47a14-145">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="47a14-146">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="47a14-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="47a14-147">Spécification de format de fichier de description d’imprimante PostScript</span><span class="sxs-lookup"><span data-stu-id="47a14-147">PostScript Printer Description File Format Specification</span></span>](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)
</dt> <dt>

[<span data-ttu-id="47a14-148">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="47a14-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




