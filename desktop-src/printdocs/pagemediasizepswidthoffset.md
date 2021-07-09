---
description: Obtenir des informations sur le paramètre PageMediaSizePSWidthOffset. Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: b93ad6e6-ab27-4fab-b488-6f402b6ee857
title: PageMediaSizePSWidthOffset
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 265acad803dbc334be115440e195967465b3ef50
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/09/2021
ms.locfileid: "113549099"
---
# <a name="pagemediasizepswidthoffset"></a><span data-ttu-id="4a9b0-105">PageMediaSizePSWidthOffset</span><span class="sxs-lookup"><span data-stu-id="4a9b0-105">PageMediaSizePSWidthOffset</span></span>

<span data-ttu-id="4a9b0-106">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="4a9b0-106">This topic is not current.</span></span> <span data-ttu-id="4a9b0-107">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="4a9b0-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="4a9b0-108">spécifie le décalage perpendiculaire à la direction de l’orientation du flux (référence [PostScript spécification du Format du fichier de Description](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)de l’imprimante).</span><span class="sxs-lookup"><span data-stu-id="4a9b0-108">Specifies the offset perpendicular to the feed-orientation direction (Reference [PostScript Printer Description File Format Specification](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)).</span></span>

-   [<span data-ttu-id="4a9b0-109">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="4a9b0-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="4a9b0-110">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="4a9b0-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="4a9b0-111">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="4a9b0-111">Element Information</span></span>



| <span data-ttu-id="4a9b0-112">Nom</span><span class="sxs-lookup"><span data-stu-id="4a9b0-112">Name</span></span> | <span data-ttu-id="4a9b0-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="4a9b0-113">Value</span></span> |
|----------------------------|-------------------------------------------------------------|
| <span data-ttu-id="4a9b0-114">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="4a9b0-114">Element Type</span></span> <br/>   | <span data-ttu-id="4a9b0-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="4a9b0-115">ParameterDef</span></span><br/>                                     |
| <span data-ttu-id="4a9b0-116">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="4a9b0-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="4a9b0-117">Page</span><span class="sxs-lookup"><span data-stu-id="4a9b0-117">Page</span></span><br/>                                             |
| <span data-ttu-id="4a9b0-118">Remarques</span><span class="sxs-lookup"><span data-stu-id="4a9b0-118">Notes</span></span> <br/>          | <span data-ttu-id="4a9b0-119">Lié à l’élément PageMediaSize, option CustomPS</span><span class="sxs-lookup"><span data-stu-id="4a9b0-119">Linked to PageMediaSize element, CustomPS option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="4a9b0-120">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="4a9b0-120">Structure Content</span></span>

<span data-ttu-id="4a9b0-121">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="4a9b0-121">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageMediaSizePSWidthOffset">
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

## <a name="structure-properties"></a><span data-ttu-id="4a9b0-122">Propriétés de structure</span><span class="sxs-lookup"><span data-stu-id="4a9b0-122">Structure Properties</span></span>

<span data-ttu-id="4a9b0-123">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="4a9b0-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="4a9b0-124">Propriété</span><span class="sxs-lookup"><span data-stu-id="4a9b0-124">Property</span></span>                | <span data-ttu-id="4a9b0-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="4a9b0-125">xsi:type</span></span>           | <span data-ttu-id="4a9b0-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="4a9b0-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="4a9b0-127">DataType</span><span class="sxs-lookup"><span data-stu-id="4a9b0-127">DataType</span></span><br/>     | <span data-ttu-id="4a9b0-128">string</span><span class="sxs-lookup"><span data-stu-id="4a9b0-128">string</span></span><br/>  | <span data-ttu-id="4a9b0-129">xs:integer</span><span class="sxs-lookup"><span data-stu-id="4a9b0-129">xs:integer</span></span><br/>      |
| <span data-ttu-id="4a9b0-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="4a9b0-130">DefaultValue</span></span><br/> | <span data-ttu-id="4a9b0-131">entier</span><span class="sxs-lookup"><span data-stu-id="4a9b0-131">integer</span></span><br/> | <span data-ttu-id="4a9b0-132">non défini</span><span class="sxs-lookup"><span data-stu-id="4a9b0-132">undefined</span></span><br/>       |
| <span data-ttu-id="4a9b0-133">MaxValue</span><span class="sxs-lookup"><span data-stu-id="4a9b0-133">MaxValue</span></span><br/>     | <span data-ttu-id="4a9b0-134">entier</span><span class="sxs-lookup"><span data-stu-id="4a9b0-134">integer</span></span><br/> | <span data-ttu-id="4a9b0-135">non défini</span><span class="sxs-lookup"><span data-stu-id="4a9b0-135">undefined</span></span><br/>       |
| <span data-ttu-id="4a9b0-136">MinValue</span><span class="sxs-lookup"><span data-stu-id="4a9b0-136">MinValue</span></span><br/>     | <span data-ttu-id="4a9b0-137">entier</span><span class="sxs-lookup"><span data-stu-id="4a9b0-137">integer</span></span><br/> | <span data-ttu-id="4a9b0-138">non défini</span><span class="sxs-lookup"><span data-stu-id="4a9b0-138">undefined</span></span><br/>       |
| <span data-ttu-id="4a9b0-139">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="4a9b0-139">Mandatory</span></span><br/>    | <span data-ttu-id="4a9b0-140">string</span><span class="sxs-lookup"><span data-stu-id="4a9b0-140">string</span></span><br/>  | <span data-ttu-id="4a9b0-141">PSK : conditionnel</span><span class="sxs-lookup"><span data-stu-id="4a9b0-141">psk:Conditional</span></span><br/> |
| <span data-ttu-id="4a9b0-142">Multiple</span><span class="sxs-lookup"><span data-stu-id="4a9b0-142">Multiple</span></span><br/>     | <span data-ttu-id="4a9b0-143">integer</span><span class="sxs-lookup"><span data-stu-id="4a9b0-143">integer</span></span><br/> | <span data-ttu-id="4a9b0-144">1</span><span class="sxs-lookup"><span data-stu-id="4a9b0-144">1</span></span><br/>               |
| <span data-ttu-id="4a9b0-145">Unité</span><span class="sxs-lookup"><span data-stu-id="4a9b0-145">UnitType</span></span><br/>     | <span data-ttu-id="4a9b0-146">string</span><span class="sxs-lookup"><span data-stu-id="4a9b0-146">string</span></span><br/>  | <span data-ttu-id="4a9b0-147">microns</span><span class="sxs-lookup"><span data-stu-id="4a9b0-147">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="4a9b0-148">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4a9b0-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4a9b0-149">PostScript Spécification de format de fichier de description d’imprimante</span><span class="sxs-lookup"><span data-stu-id="4a9b0-149">PostScript Printer Description File Format Specification</span></span>](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)
</dt> <dt>

[<span data-ttu-id="4a9b0-150">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="4a9b0-150">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




