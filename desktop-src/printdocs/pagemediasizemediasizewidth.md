---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: 22e4a6e9-4d18-4fff-873c-27ba59a79222
title: PageMediaSizeMediaSizeWidth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50df088fd25a69ee566e1406d3f1b833aa6131f5
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997566"
---
# <a name="pagemediasizemediasizewidth"></a><span data-ttu-id="779f0-104">PageMediaSizeMediaSizeWidth</span><span class="sxs-lookup"><span data-stu-id="779f0-104">PageMediaSizeMediaSizeWidth</span></span>

<span data-ttu-id="779f0-105">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="779f0-105">This topic is not current.</span></span> <span data-ttu-id="779f0-106">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="779f0-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="779f0-107">Spécifie la direction MediaSizeWidth de la dimension pour l’option MediaSize personnalisée.</span><span class="sxs-lookup"><span data-stu-id="779f0-107">Specifies the dimension MediaSizeWidth direction for the Custom MediaSize option.</span></span>

-   [<span data-ttu-id="779f0-108">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="779f0-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="779f0-109">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="779f0-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="779f0-110">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="779f0-110">Element Information</span></span>



| <span data-ttu-id="779f0-111">Nom</span><span class="sxs-lookup"><span data-stu-id="779f0-111">Name</span></span> | <span data-ttu-id="779f0-112">Value</span><span class="sxs-lookup"><span data-stu-id="779f0-112">Value</span></span> |
|----------------------------|-----------------------------------------------------------|
| <span data-ttu-id="779f0-113">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="779f0-113">Element Type</span></span> <br/>   | <span data-ttu-id="779f0-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="779f0-114">ParameterDef</span></span><br/>                                   |
| <span data-ttu-id="779f0-115">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="779f0-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="779f0-116">Page</span><span class="sxs-lookup"><span data-stu-id="779f0-116">Page</span></span><br/>                                           |
| <span data-ttu-id="779f0-117">Notes</span><span class="sxs-lookup"><span data-stu-id="779f0-117">Notes</span></span> <br/>          | <span data-ttu-id="779f0-118">Lié à l’élément PageMediaSize, option personnalisée</span><span class="sxs-lookup"><span data-stu-id="779f0-118">Linked to PageMediaSize element, Custom option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="779f0-119">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="779f0-119">Structure Content</span></span>

<span data-ttu-id="779f0-120">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="779f0-120">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageMediaSizeMediaSizeWidth">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:integer</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxValue">
    <psf:Value xsi:type="xs:integer">_Undefined</psf:Value>
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

## <a name="structure-properties"></a><span data-ttu-id="779f0-121">Propriétés de structure</span><span class="sxs-lookup"><span data-stu-id="779f0-121">Structure Properties</span></span>

<span data-ttu-id="779f0-122">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="779f0-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="779f0-123">Propriété</span><span class="sxs-lookup"><span data-stu-id="779f0-123">Property</span></span>                | <span data-ttu-id="779f0-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="779f0-124">xsi:type</span></span>           | <span data-ttu-id="779f0-125">Value</span><span class="sxs-lookup"><span data-stu-id="779f0-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="779f0-126">DataType</span><span class="sxs-lookup"><span data-stu-id="779f0-126">DataType</span></span><br/>     | <span data-ttu-id="779f0-127">string</span><span class="sxs-lookup"><span data-stu-id="779f0-127">string</span></span><br/>  | <span data-ttu-id="779f0-128">xs:integer</span><span class="sxs-lookup"><span data-stu-id="779f0-128">xs:integer</span></span><br/>      |
| <span data-ttu-id="779f0-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="779f0-129">DefaultValue</span></span><br/> | <span data-ttu-id="779f0-130">entier</span><span class="sxs-lookup"><span data-stu-id="779f0-130">integer</span></span><br/> | <span data-ttu-id="779f0-131">non défini</span><span class="sxs-lookup"><span data-stu-id="779f0-131">undefined</span></span><br/>       |
| <span data-ttu-id="779f0-132">MaxValue</span><span class="sxs-lookup"><span data-stu-id="779f0-132">MaxValue</span></span><br/>     | <span data-ttu-id="779f0-133">entier</span><span class="sxs-lookup"><span data-stu-id="779f0-133">integer</span></span><br/> | <span data-ttu-id="779f0-134">non défini</span><span class="sxs-lookup"><span data-stu-id="779f0-134">undefined</span></span><br/>       |
| <span data-ttu-id="779f0-135">MinValue</span><span class="sxs-lookup"><span data-stu-id="779f0-135">MinValue</span></span><br/>     | <span data-ttu-id="779f0-136">entier</span><span class="sxs-lookup"><span data-stu-id="779f0-136">integer</span></span><br/> | <span data-ttu-id="779f0-137">non défini</span><span class="sxs-lookup"><span data-stu-id="779f0-137">undefined</span></span><br/>       |
| <span data-ttu-id="779f0-138">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="779f0-138">Mandatory</span></span><br/>    | <span data-ttu-id="779f0-139">string</span><span class="sxs-lookup"><span data-stu-id="779f0-139">string</span></span><br/>  | <span data-ttu-id="779f0-140">PSK : conditionnel</span><span class="sxs-lookup"><span data-stu-id="779f0-140">psk:Conditional</span></span><br/> |
| <span data-ttu-id="779f0-141">Plusieurs</span><span class="sxs-lookup"><span data-stu-id="779f0-141">Multiple</span></span><br/>     | <span data-ttu-id="779f0-142">integer</span><span class="sxs-lookup"><span data-stu-id="779f0-142">integer</span></span><br/> | <span data-ttu-id="779f0-143">1</span><span class="sxs-lookup"><span data-stu-id="779f0-143">1</span></span><br/>               |
| <span data-ttu-id="779f0-144">Unité</span><span class="sxs-lookup"><span data-stu-id="779f0-144">UnitType</span></span><br/>     | <span data-ttu-id="779f0-145">string</span><span class="sxs-lookup"><span data-stu-id="779f0-145">string</span></span><br/>  | <span data-ttu-id="779f0-146">microns</span><span class="sxs-lookup"><span data-stu-id="779f0-146">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="779f0-147">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="779f0-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="779f0-148">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="779f0-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




