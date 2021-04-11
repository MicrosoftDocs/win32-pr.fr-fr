---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: 22e4a6e9-4d18-4fff-873c-27ba59a79222
title: PageMediaSizeMediaSizeWidth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb1f72e667f3de3bce86beb1c65c5fde4ebc8669
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "104321690"
---
# <a name="pagemediasizemediasizewidth"></a><span data-ttu-id="cd526-104">PageMediaSizeMediaSizeWidth</span><span class="sxs-lookup"><span data-stu-id="cd526-104">PageMediaSizeMediaSizeWidth</span></span>

<span data-ttu-id="cd526-105">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="cd526-105">This topic is not current.</span></span> <span data-ttu-id="cd526-106">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="cd526-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="cd526-107">Spécifie la direction MediaSizeWidth de la dimension pour l’option MediaSize personnalisée.</span><span class="sxs-lookup"><span data-stu-id="cd526-107">Specifies the dimension MediaSizeWidth direction for the Custom MediaSize option.</span></span>

-   [<span data-ttu-id="cd526-108">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="cd526-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="cd526-109">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="cd526-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="cd526-110">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="cd526-110">Element Information</span></span>



| <span data-ttu-id="cd526-111">Nom</span><span class="sxs-lookup"><span data-stu-id="cd526-111">Name</span></span>                       |                                                           |
|----------------------------|-----------------------------------------------------------|
| <span data-ttu-id="cd526-112">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="cd526-112">Element Type</span></span> <br/>   | <span data-ttu-id="cd526-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="cd526-113">ParameterDef</span></span><br/>                                   |
| <span data-ttu-id="cd526-114">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="cd526-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="cd526-115">Page</span><span class="sxs-lookup"><span data-stu-id="cd526-115">Page</span></span><br/>                                           |
| <span data-ttu-id="cd526-116">Notes</span><span class="sxs-lookup"><span data-stu-id="cd526-116">Notes</span></span> <br/>          | <span data-ttu-id="cd526-117">Lié à l’élément PageMediaSize, option personnalisée</span><span class="sxs-lookup"><span data-stu-id="cd526-117">Linked to PageMediaSize element, Custom option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="cd526-118">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="cd526-118">Structure Content</span></span>

<span data-ttu-id="cd526-119">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="cd526-119">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="cd526-120">Propriétés de structure</span><span class="sxs-lookup"><span data-stu-id="cd526-120">Structure Properties</span></span>

<span data-ttu-id="cd526-121">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="cd526-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="cd526-122">Propriété</span><span class="sxs-lookup"><span data-stu-id="cd526-122">Property</span></span>                | <span data-ttu-id="cd526-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="cd526-123">xsi:type</span></span>           | <span data-ttu-id="cd526-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="cd526-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="cd526-125">DataType</span><span class="sxs-lookup"><span data-stu-id="cd526-125">DataType</span></span><br/>     | <span data-ttu-id="cd526-126">string</span><span class="sxs-lookup"><span data-stu-id="cd526-126">string</span></span><br/>  | <span data-ttu-id="cd526-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="cd526-127">xs:integer</span></span><br/>      |
| <span data-ttu-id="cd526-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="cd526-128">DefaultValue</span></span><br/> | <span data-ttu-id="cd526-129">entier</span><span class="sxs-lookup"><span data-stu-id="cd526-129">integer</span></span><br/> | <span data-ttu-id="cd526-130">non défini</span><span class="sxs-lookup"><span data-stu-id="cd526-130">undefined</span></span><br/>       |
| <span data-ttu-id="cd526-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="cd526-131">MaxValue</span></span><br/>     | <span data-ttu-id="cd526-132">entier</span><span class="sxs-lookup"><span data-stu-id="cd526-132">integer</span></span><br/> | <span data-ttu-id="cd526-133">non défini</span><span class="sxs-lookup"><span data-stu-id="cd526-133">undefined</span></span><br/>       |
| <span data-ttu-id="cd526-134">MinValue</span><span class="sxs-lookup"><span data-stu-id="cd526-134">MinValue</span></span><br/>     | <span data-ttu-id="cd526-135">entier</span><span class="sxs-lookup"><span data-stu-id="cd526-135">integer</span></span><br/> | <span data-ttu-id="cd526-136">non défini</span><span class="sxs-lookup"><span data-stu-id="cd526-136">undefined</span></span><br/>       |
| <span data-ttu-id="cd526-137">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="cd526-137">Mandatory</span></span><br/>    | <span data-ttu-id="cd526-138">string</span><span class="sxs-lookup"><span data-stu-id="cd526-138">string</span></span><br/>  | <span data-ttu-id="cd526-139">PSK : conditionnel</span><span class="sxs-lookup"><span data-stu-id="cd526-139">psk:Conditional</span></span><br/> |
| <span data-ttu-id="cd526-140">Multiple</span><span class="sxs-lookup"><span data-stu-id="cd526-140">Multiple</span></span><br/>     | <span data-ttu-id="cd526-141">integer</span><span class="sxs-lookup"><span data-stu-id="cd526-141">integer</span></span><br/> | <span data-ttu-id="cd526-142">1</span><span class="sxs-lookup"><span data-stu-id="cd526-142">1</span></span><br/>               |
| <span data-ttu-id="cd526-143">Unité</span><span class="sxs-lookup"><span data-stu-id="cd526-143">UnitType</span></span><br/>     | <span data-ttu-id="cd526-144">string</span><span class="sxs-lookup"><span data-stu-id="cd526-144">string</span></span><br/>  | <span data-ttu-id="cd526-145">microns</span><span class="sxs-lookup"><span data-stu-id="cd526-145">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="cd526-146">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="cd526-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cd526-147">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="cd526-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




