---
description: Obtenir des informations sur le paramètre PageMediaSizePSWidth. Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: a1a684ce-5615-4ff7-a7aa-5c9f786f84ed
title: PageMediaSizePSWidth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfe678107d2a183ee0f0bf6ce290dfe230fa8cc2
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395644"
---
# <a name="pagemediasizepswidth"></a><span data-ttu-id="c495b-105">PageMediaSizePSWidth</span><span class="sxs-lookup"><span data-stu-id="c495b-105">PageMediaSizePSWidth</span></span>

<span data-ttu-id="c495b-106">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="c495b-106">This topic is not current.</span></span> <span data-ttu-id="c495b-107">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="c495b-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="c495b-108">Spécifie la largeur de la page perpendiculairement au sens de l’orientation du flux (référence [PostScript Printer Description file format Specification](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)).</span><span class="sxs-lookup"><span data-stu-id="c495b-108">Specifies the width of the page perpendicular to the feed-orientation direction (Reference [PostScript Printer Description File Format Specification](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)).</span></span>

-   [<span data-ttu-id="c495b-109">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="c495b-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="c495b-110">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="c495b-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="c495b-111">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="c495b-111">Element Information</span></span>



| <span data-ttu-id="c495b-112">Nom</span><span class="sxs-lookup"><span data-stu-id="c495b-112">Name</span></span> | <span data-ttu-id="c495b-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="c495b-113">Value</span></span> |
|----------------------------|-------------------------------------------------------------|
| <span data-ttu-id="c495b-114">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="c495b-114">Element Type</span></span> <br/>   | <span data-ttu-id="c495b-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="c495b-115">ParameterDef</span></span><br/>                                     |
| <span data-ttu-id="c495b-116">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="c495b-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="c495b-117">Page</span><span class="sxs-lookup"><span data-stu-id="c495b-117">Page</span></span><br/>                                             |
| <span data-ttu-id="c495b-118">Notes</span><span class="sxs-lookup"><span data-stu-id="c495b-118">Notes</span></span> <br/>          | <span data-ttu-id="c495b-119">Lié à l’élément PageMediaSize, option CustomPS</span><span class="sxs-lookup"><span data-stu-id="c495b-119">Linked to PageMediaSize element, CustomPS option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="c495b-120">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="c495b-120">Structure Content</span></span>

<span data-ttu-id="c495b-121">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="c495b-121">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="c495b-122">Propriétés de structure</span><span class="sxs-lookup"><span data-stu-id="c495b-122">Structure Properties</span></span>

<span data-ttu-id="c495b-123">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="c495b-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="c495b-124">Propriété</span><span class="sxs-lookup"><span data-stu-id="c495b-124">Property</span></span>                | <span data-ttu-id="c495b-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="c495b-125">xsi:type</span></span>           | <span data-ttu-id="c495b-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="c495b-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="c495b-127">DataType</span><span class="sxs-lookup"><span data-stu-id="c495b-127">DataType</span></span><br/>     | <span data-ttu-id="c495b-128">string</span><span class="sxs-lookup"><span data-stu-id="c495b-128">string</span></span><br/>  | <span data-ttu-id="c495b-129">xs:integer</span><span class="sxs-lookup"><span data-stu-id="c495b-129">xs:integer</span></span><br/>      |
| <span data-ttu-id="c495b-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="c495b-130">DefaultValue</span></span><br/> | <span data-ttu-id="c495b-131">entier</span><span class="sxs-lookup"><span data-stu-id="c495b-131">integer</span></span><br/> | <span data-ttu-id="c495b-132">non défini</span><span class="sxs-lookup"><span data-stu-id="c495b-132">undefined</span></span><br/>       |
| <span data-ttu-id="c495b-133">MaxValue</span><span class="sxs-lookup"><span data-stu-id="c495b-133">MaxValue</span></span><br/>     | <span data-ttu-id="c495b-134">entier</span><span class="sxs-lookup"><span data-stu-id="c495b-134">integer</span></span><br/> | <span data-ttu-id="c495b-135">non défini</span><span class="sxs-lookup"><span data-stu-id="c495b-135">undefined</span></span><br/>       |
| <span data-ttu-id="c495b-136">MinValue</span><span class="sxs-lookup"><span data-stu-id="c495b-136">MinValue</span></span><br/>     | <span data-ttu-id="c495b-137">entier</span><span class="sxs-lookup"><span data-stu-id="c495b-137">integer</span></span><br/> | <span data-ttu-id="c495b-138">non défini</span><span class="sxs-lookup"><span data-stu-id="c495b-138">undefined</span></span><br/>       |
| <span data-ttu-id="c495b-139">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="c495b-139">Mandatory</span></span><br/>    | <span data-ttu-id="c495b-140">string</span><span class="sxs-lookup"><span data-stu-id="c495b-140">string</span></span><br/>  | <span data-ttu-id="c495b-141">PSK : conditionnel</span><span class="sxs-lookup"><span data-stu-id="c495b-141">psk:Conditional</span></span><br/> |
| <span data-ttu-id="c495b-142">Multiple</span><span class="sxs-lookup"><span data-stu-id="c495b-142">Multiple</span></span><br/>     | <span data-ttu-id="c495b-143">integer</span><span class="sxs-lookup"><span data-stu-id="c495b-143">integer</span></span><br/> | <span data-ttu-id="c495b-144">1</span><span class="sxs-lookup"><span data-stu-id="c495b-144">1</span></span><br/>               |
| <span data-ttu-id="c495b-145">Unité</span><span class="sxs-lookup"><span data-stu-id="c495b-145">UnitType</span></span><br/>     | <span data-ttu-id="c495b-146">string</span><span class="sxs-lookup"><span data-stu-id="c495b-146">string</span></span><br/>  | <span data-ttu-id="c495b-147">microns</span><span class="sxs-lookup"><span data-stu-id="c495b-147">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="c495b-148">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c495b-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c495b-149">Spécification de format de fichier de description d’imprimante PostScript</span><span class="sxs-lookup"><span data-stu-id="c495b-149">PostScript Printer Description File Format Specification</span></span>](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)
</dt> <dt>

[<span data-ttu-id="c495b-150">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="c495b-150">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




