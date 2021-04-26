---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: 25c3c70f-20e3-4e44-9c59-bb66b4bd14d9
title: PageSourceColorProfileURI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f515fca037e58c0794f20bc1dd1afee8a779fb49
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996896"
---
# <a name="pagesourcecolorprofileuri"></a><span data-ttu-id="6563c-104">PageSourceColorProfileURI</span><span class="sxs-lookup"><span data-stu-id="6563c-104">PageSourceColorProfileURI</span></span>

<span data-ttu-id="6563c-105">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="6563c-105">This topic is not current.</span></span> <span data-ttu-id="6563c-106">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="6563c-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="6563c-107">Spécifie la source du profil de couleurs.</span><span class="sxs-lookup"><span data-stu-id="6563c-107">Specifies the source for color profile.</span></span>

-   [<span data-ttu-id="6563c-108">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="6563c-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="6563c-109">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="6563c-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="6563c-110">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="6563c-110">Element Information</span></span>



| <span data-ttu-id="6563c-111">Nom</span><span class="sxs-lookup"><span data-stu-id="6563c-111">Name</span></span> | <span data-ttu-id="6563c-112">Value</span><span class="sxs-lookup"><span data-stu-id="6563c-112">Value</span></span> |
|----------------------------|-----------------------------------------------------|
| <span data-ttu-id="6563c-113">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="6563c-113">Element Type</span></span> <br/>   | <span data-ttu-id="6563c-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="6563c-114">ParameterDef</span></span><br/>                             |
| <span data-ttu-id="6563c-115">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="6563c-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="6563c-116">Page</span><span class="sxs-lookup"><span data-stu-id="6563c-116">Page</span></span><br/>                                     |
| <span data-ttu-id="6563c-117">Notes</span><span class="sxs-lookup"><span data-stu-id="6563c-117">Notes</span></span> <br/>          | <span data-ttu-id="6563c-118">Lié à l’élément PageSourceColorProfile</span><span class="sxs-lookup"><span data-stu-id="6563c-118">Linked to PageSourceColorProfile element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="6563c-119">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="6563c-119">Structure Content</span></span>

<span data-ttu-id="6563c-120">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="6563c-120">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageSourceColorProfileURI">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:string</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxLength">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinLength">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Conditional</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">characters</psf:Value>
  </psf:Property>
</psf:ParameterDef>
      
```

## <a name="structure-properties"></a><span data-ttu-id="6563c-121">Propriétés de structure</span><span class="sxs-lookup"><span data-stu-id="6563c-121">Structure Properties</span></span>

<span data-ttu-id="6563c-122">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="6563c-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="6563c-123">Propriété</span><span class="sxs-lookup"><span data-stu-id="6563c-123">Property</span></span>                | <span data-ttu-id="6563c-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="6563c-124">xsi:type</span></span>           | <span data-ttu-id="6563c-125">Value</span><span class="sxs-lookup"><span data-stu-id="6563c-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="6563c-126">DataType</span><span class="sxs-lookup"><span data-stu-id="6563c-126">DataType</span></span><br/>     | <span data-ttu-id="6563c-127">string</span><span class="sxs-lookup"><span data-stu-id="6563c-127">string</span></span><br/>  | <span data-ttu-id="6563c-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="6563c-128">xs:string</span></span><br/>       |
| <span data-ttu-id="6563c-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="6563c-129">DefaultValue</span></span><br/> | <span data-ttu-id="6563c-130">string</span><span class="sxs-lookup"><span data-stu-id="6563c-130">string</span></span><br/>  | <span data-ttu-id="6563c-131">non défini</span><span class="sxs-lookup"><span data-stu-id="6563c-131">undefined</span></span><br/>       |
| <span data-ttu-id="6563c-132">MaxLength</span><span class="sxs-lookup"><span data-stu-id="6563c-132">MaxLength</span></span><br/>    | <span data-ttu-id="6563c-133">entier</span><span class="sxs-lookup"><span data-stu-id="6563c-133">integer</span></span><br/> | <span data-ttu-id="6563c-134">non défini</span><span class="sxs-lookup"><span data-stu-id="6563c-134">undefined</span></span><br/>       |
| <span data-ttu-id="6563c-135">MinLength</span><span class="sxs-lookup"><span data-stu-id="6563c-135">MinLength</span></span><br/>    | <span data-ttu-id="6563c-136">integer</span><span class="sxs-lookup"><span data-stu-id="6563c-136">integer</span></span><br/> | <span data-ttu-id="6563c-137">1</span><span class="sxs-lookup"><span data-stu-id="6563c-137">1</span></span><br/>               |
| <span data-ttu-id="6563c-138">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="6563c-138">Mandatory</span></span><br/>    | <span data-ttu-id="6563c-139">string</span><span class="sxs-lookup"><span data-stu-id="6563c-139">string</span></span><br/>  | <span data-ttu-id="6563c-140">PSK : conditionnel</span><span class="sxs-lookup"><span data-stu-id="6563c-140">psk:Conditional</span></span><br/> |
| <span data-ttu-id="6563c-141">Unité</span><span class="sxs-lookup"><span data-stu-id="6563c-141">UnitType</span></span><br/>     | <span data-ttu-id="6563c-142">string</span><span class="sxs-lookup"><span data-stu-id="6563c-142">string</span></span><br/>  | <span data-ttu-id="6563c-143">caractères</span><span class="sxs-lookup"><span data-stu-id="6563c-143">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="6563c-144">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6563c-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6563c-145">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="6563c-145">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




