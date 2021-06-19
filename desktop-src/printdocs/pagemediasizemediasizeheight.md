---
description: Obtenir des informations sur le paramètre PageMediaSizeMediaSizeHeight. Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: 209b3024-60cf-47e0-8738-cd7795e38c2a
title: PageMediaSizeMediaSizeHeight
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 547077e7a63d91d6db43e8ebf6225a771bf237d8
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395794"
---
# <a name="pagemediasizemediasizeheight"></a><span data-ttu-id="ee4e0-105">PageMediaSizeMediaSizeHeight</span><span class="sxs-lookup"><span data-stu-id="ee4e0-105">PageMediaSizeMediaSizeHeight</span></span>

<span data-ttu-id="ee4e0-106">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="ee4e0-106">This topic is not current.</span></span> <span data-ttu-id="ee4e0-107">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="ee4e0-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="ee4e0-108">Spécifie la direction MediaSizeHeight de la dimension pour l’option MediaSize personnalisée.</span><span class="sxs-lookup"><span data-stu-id="ee4e0-108">Specifies the dimension MediaSizeHeight direction for the Custom MediaSize option.</span></span>

-   [<span data-ttu-id="ee4e0-109">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="ee4e0-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="ee4e0-110">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="ee4e0-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="ee4e0-111">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="ee4e0-111">Element Information</span></span>



| <span data-ttu-id="ee4e0-112">Nom</span><span class="sxs-lookup"><span data-stu-id="ee4e0-112">Name</span></span> | <span data-ttu-id="ee4e0-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="ee4e0-113">Value</span></span> |
|----------------------------|-----------------------------------------------------------|
| <span data-ttu-id="ee4e0-114">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="ee4e0-114">Element Type</span></span> <br/>   | <span data-ttu-id="ee4e0-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="ee4e0-115">ParameterDef</span></span><br/>                                   |
| <span data-ttu-id="ee4e0-116">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="ee4e0-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="ee4e0-117">Page</span><span class="sxs-lookup"><span data-stu-id="ee4e0-117">Page</span></span><br/>                                           |
| <span data-ttu-id="ee4e0-118">Notes</span><span class="sxs-lookup"><span data-stu-id="ee4e0-118">Notes</span></span> <br/>          | <span data-ttu-id="ee4e0-119">Lié à l’élément PageMediaSize, option personnalisée</span><span class="sxs-lookup"><span data-stu-id="ee4e0-119">Linked to PageMediaSize element, Custom option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="ee4e0-120">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="ee4e0-120">Structure Content</span></span>

<span data-ttu-id="ee4e0-121">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="ee4e0-121">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageMediaSizeMediaSizeHeight">
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

## <a name="structure-properties"></a><span data-ttu-id="ee4e0-122">Propriétés de structure</span><span class="sxs-lookup"><span data-stu-id="ee4e0-122">Structure Properties</span></span>

<span data-ttu-id="ee4e0-123">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="ee4e0-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="ee4e0-124">Propriété</span><span class="sxs-lookup"><span data-stu-id="ee4e0-124">Property</span></span>                | <span data-ttu-id="ee4e0-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="ee4e0-125">xsi:type</span></span>           | <span data-ttu-id="ee4e0-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="ee4e0-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="ee4e0-127">DataType</span><span class="sxs-lookup"><span data-stu-id="ee4e0-127">DataType</span></span><br/>     | <span data-ttu-id="ee4e0-128">string</span><span class="sxs-lookup"><span data-stu-id="ee4e0-128">string</span></span><br/>  | <span data-ttu-id="ee4e0-129">xs:integer</span><span class="sxs-lookup"><span data-stu-id="ee4e0-129">xs:integer</span></span><br/>      |
| <span data-ttu-id="ee4e0-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="ee4e0-130">DefaultValue</span></span><br/> | <span data-ttu-id="ee4e0-131">entier</span><span class="sxs-lookup"><span data-stu-id="ee4e0-131">integer</span></span><br/> | <span data-ttu-id="ee4e0-132">non défini</span><span class="sxs-lookup"><span data-stu-id="ee4e0-132">undefined</span></span><br/>       |
| <span data-ttu-id="ee4e0-133">MaxValue</span><span class="sxs-lookup"><span data-stu-id="ee4e0-133">MaxValue</span></span><br/>     | <span data-ttu-id="ee4e0-134">entier</span><span class="sxs-lookup"><span data-stu-id="ee4e0-134">integer</span></span><br/> | <span data-ttu-id="ee4e0-135">non défini</span><span class="sxs-lookup"><span data-stu-id="ee4e0-135">undefined</span></span><br/>       |
| <span data-ttu-id="ee4e0-136">MinValue</span><span class="sxs-lookup"><span data-stu-id="ee4e0-136">MinValue</span></span><br/>     | <span data-ttu-id="ee4e0-137">entier</span><span class="sxs-lookup"><span data-stu-id="ee4e0-137">integer</span></span><br/> | <span data-ttu-id="ee4e0-138">non défini</span><span class="sxs-lookup"><span data-stu-id="ee4e0-138">undefined</span></span><br/>       |
| <span data-ttu-id="ee4e0-139">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="ee4e0-139">Mandatory</span></span><br/>    | <span data-ttu-id="ee4e0-140">string</span><span class="sxs-lookup"><span data-stu-id="ee4e0-140">string</span></span><br/>  | <span data-ttu-id="ee4e0-141">PSK : conditionnel</span><span class="sxs-lookup"><span data-stu-id="ee4e0-141">psk:Conditional</span></span><br/> |
| <span data-ttu-id="ee4e0-142">Multiple</span><span class="sxs-lookup"><span data-stu-id="ee4e0-142">Multiple</span></span><br/>     | <span data-ttu-id="ee4e0-143">integer</span><span class="sxs-lookup"><span data-stu-id="ee4e0-143">integer</span></span><br/> | <span data-ttu-id="ee4e0-144">1</span><span class="sxs-lookup"><span data-stu-id="ee4e0-144">1</span></span><br/>               |
| <span data-ttu-id="ee4e0-145">Unité</span><span class="sxs-lookup"><span data-stu-id="ee4e0-145">UnitType</span></span><br/>     | <span data-ttu-id="ee4e0-146">string</span><span class="sxs-lookup"><span data-stu-id="ee4e0-146">string</span></span><br/>  | <span data-ttu-id="ee4e0-147">microns</span><span class="sxs-lookup"><span data-stu-id="ee4e0-147">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="ee4e0-148">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ee4e0-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ee4e0-149">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="ee4e0-149">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




