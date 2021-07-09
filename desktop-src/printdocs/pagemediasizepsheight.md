---
description: Obtenir des informations sur le paramètre PageMediaSizePSHeight. Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: 857caf51-ccf6-415c-aab3-1fed50fa7b34
title: PageMediaSizePSHeight
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b1e7a30935c27fadb5d6ebb8dfb8f377e05a5e3
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/09/2021
ms.locfileid: "113549094"
---
# <a name="pagemediasizepsheight"></a><span data-ttu-id="32429-105">PageMediaSizePSHeight</span><span class="sxs-lookup"><span data-stu-id="32429-105">PageMediaSizePSHeight</span></span>

<span data-ttu-id="32429-106">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="32429-106">This topic is not current.</span></span> <span data-ttu-id="32429-107">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="32429-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="32429-108">spécifie la hauteur de la page, parallèle à la direction de l’orientation du flux (référence [PostScript spécification du Format du fichier de Description](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)de l’imprimante).</span><span class="sxs-lookup"><span data-stu-id="32429-108">Specifies the height of the page, parallel to the feed-orientation direction (Reference [PostScript Printer Description File Format Specification](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)).</span></span>

-   [<span data-ttu-id="32429-109">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="32429-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="32429-110">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="32429-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="32429-111">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="32429-111">Element Information</span></span>



| <span data-ttu-id="32429-112">Nom</span><span class="sxs-lookup"><span data-stu-id="32429-112">Name</span></span> | <span data-ttu-id="32429-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="32429-113">Value</span></span> |
|----------------------------|-------------------------------------------------------------|
| <span data-ttu-id="32429-114">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="32429-114">Element Type</span></span> <br/>   | <span data-ttu-id="32429-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="32429-115">ParameterDef</span></span><br/>                                     |
| <span data-ttu-id="32429-116">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="32429-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="32429-117">Page</span><span class="sxs-lookup"><span data-stu-id="32429-117">Page</span></span><br/>                                             |
| <span data-ttu-id="32429-118">Remarques</span><span class="sxs-lookup"><span data-stu-id="32429-118">Notes</span></span> <br/>          | <span data-ttu-id="32429-119">Lié à l’élément PageMediaSize, option CustomPS</span><span class="sxs-lookup"><span data-stu-id="32429-119">Linked to PageMediaSize element, CustomPS option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="32429-120">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="32429-120">Structure Content</span></span>

<span data-ttu-id="32429-121">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="32429-121">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="32429-122">Propriétés de structure</span><span class="sxs-lookup"><span data-stu-id="32429-122">Structure Properties</span></span>

<span data-ttu-id="32429-123">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="32429-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="32429-124">Propriété</span><span class="sxs-lookup"><span data-stu-id="32429-124">Property</span></span>                | <span data-ttu-id="32429-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="32429-125">xsi:type</span></span>           | <span data-ttu-id="32429-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="32429-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="32429-127">DataType</span><span class="sxs-lookup"><span data-stu-id="32429-127">DataType</span></span><br/>     | <span data-ttu-id="32429-128">string</span><span class="sxs-lookup"><span data-stu-id="32429-128">string</span></span><br/>  | <span data-ttu-id="32429-129">xs:integer</span><span class="sxs-lookup"><span data-stu-id="32429-129">xs:integer</span></span><br/>      |
| <span data-ttu-id="32429-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="32429-130">DefaultValue</span></span><br/> | <span data-ttu-id="32429-131">entier</span><span class="sxs-lookup"><span data-stu-id="32429-131">integer</span></span><br/> | <span data-ttu-id="32429-132">non défini</span><span class="sxs-lookup"><span data-stu-id="32429-132">undefined</span></span><br/>       |
| <span data-ttu-id="32429-133">MaxValue</span><span class="sxs-lookup"><span data-stu-id="32429-133">MaxValue</span></span><br/>     | <span data-ttu-id="32429-134">entier</span><span class="sxs-lookup"><span data-stu-id="32429-134">integer</span></span><br/> | <span data-ttu-id="32429-135">non défini</span><span class="sxs-lookup"><span data-stu-id="32429-135">undefined</span></span><br/>       |
| <span data-ttu-id="32429-136">MinValue</span><span class="sxs-lookup"><span data-stu-id="32429-136">MinValue</span></span><br/>     | <span data-ttu-id="32429-137">entier</span><span class="sxs-lookup"><span data-stu-id="32429-137">integer</span></span><br/> | <span data-ttu-id="32429-138">non défini</span><span class="sxs-lookup"><span data-stu-id="32429-138">undefined</span></span><br/>       |
| <span data-ttu-id="32429-139">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="32429-139">Mandatory</span></span><br/>    | <span data-ttu-id="32429-140">string</span><span class="sxs-lookup"><span data-stu-id="32429-140">string</span></span><br/>  | <span data-ttu-id="32429-141">PSK : conditionnel</span><span class="sxs-lookup"><span data-stu-id="32429-141">psk:Conditional</span></span><br/> |
| <span data-ttu-id="32429-142">Multiple</span><span class="sxs-lookup"><span data-stu-id="32429-142">Multiple</span></span><br/>     | <span data-ttu-id="32429-143">integer</span><span class="sxs-lookup"><span data-stu-id="32429-143">integer</span></span><br/> | <span data-ttu-id="32429-144">1</span><span class="sxs-lookup"><span data-stu-id="32429-144">1</span></span><br/>               |
| <span data-ttu-id="32429-145">Unité</span><span class="sxs-lookup"><span data-stu-id="32429-145">UnitType</span></span><br/>     | <span data-ttu-id="32429-146">string</span><span class="sxs-lookup"><span data-stu-id="32429-146">string</span></span><br/>  | <span data-ttu-id="32429-147">microns</span><span class="sxs-lookup"><span data-stu-id="32429-147">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="32429-148">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="32429-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="32429-149">PostScript Spécification de format de fichier de description d’imprimante</span><span class="sxs-lookup"><span data-stu-id="32429-149">PostScript Printer Description File Format Specification</span></span>](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)
</dt> <dt>

[<span data-ttu-id="32429-150">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="32429-150">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




