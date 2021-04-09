---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: 25c3c70f-20e3-4e44-9c59-bb66b4bd14d9
title: PageSourceColorProfileURI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6b3f2396fe3a886ed797392a3e1fd9f3c6d0170
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "104042987"
---
# <a name="pagesourcecolorprofileuri"></a><span data-ttu-id="8e2c9-104">PageSourceColorProfileURI</span><span class="sxs-lookup"><span data-stu-id="8e2c9-104">PageSourceColorProfileURI</span></span>

<span data-ttu-id="8e2c9-105">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="8e2c9-105">This topic is not current.</span></span> <span data-ttu-id="8e2c9-106">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="8e2c9-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="8e2c9-107">Spécifie la source du profil de couleurs.</span><span class="sxs-lookup"><span data-stu-id="8e2c9-107">Specifies the source for color profile.</span></span>

-   [<span data-ttu-id="8e2c9-108">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="8e2c9-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="8e2c9-109">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="8e2c9-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="8e2c9-110">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="8e2c9-110">Element Information</span></span>



| <span data-ttu-id="8e2c9-111">Nom</span><span class="sxs-lookup"><span data-stu-id="8e2c9-111">Name</span></span>                       |                                                     |
|----------------------------|-----------------------------------------------------|
| <span data-ttu-id="8e2c9-112">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="8e2c9-112">Element Type</span></span> <br/>   | <span data-ttu-id="8e2c9-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="8e2c9-113">ParameterDef</span></span><br/>                             |
| <span data-ttu-id="8e2c9-114">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="8e2c9-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="8e2c9-115">Page</span><span class="sxs-lookup"><span data-stu-id="8e2c9-115">Page</span></span><br/>                                     |
| <span data-ttu-id="8e2c9-116">Notes</span><span class="sxs-lookup"><span data-stu-id="8e2c9-116">Notes</span></span> <br/>          | <span data-ttu-id="8e2c9-117">Lié à l’élément PageSourceColorProfile</span><span class="sxs-lookup"><span data-stu-id="8e2c9-117">Linked to PageSourceColorProfile element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="8e2c9-118">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="8e2c9-118">Structure Content</span></span>

<span data-ttu-id="8e2c9-119">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="8e2c9-119">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="8e2c9-120">Propriétés de structure</span><span class="sxs-lookup"><span data-stu-id="8e2c9-120">Structure Properties</span></span>

<span data-ttu-id="8e2c9-121">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="8e2c9-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="8e2c9-122">Propriété</span><span class="sxs-lookup"><span data-stu-id="8e2c9-122">Property</span></span>                | <span data-ttu-id="8e2c9-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="8e2c9-123">xsi:type</span></span>           | <span data-ttu-id="8e2c9-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="8e2c9-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="8e2c9-125">DataType</span><span class="sxs-lookup"><span data-stu-id="8e2c9-125">DataType</span></span><br/>     | <span data-ttu-id="8e2c9-126">string</span><span class="sxs-lookup"><span data-stu-id="8e2c9-126">string</span></span><br/>  | <span data-ttu-id="8e2c9-127">xs:string</span><span class="sxs-lookup"><span data-stu-id="8e2c9-127">xs:string</span></span><br/>       |
| <span data-ttu-id="8e2c9-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="8e2c9-128">DefaultValue</span></span><br/> | <span data-ttu-id="8e2c9-129">string</span><span class="sxs-lookup"><span data-stu-id="8e2c9-129">string</span></span><br/>  | <span data-ttu-id="8e2c9-130">non défini</span><span class="sxs-lookup"><span data-stu-id="8e2c9-130">undefined</span></span><br/>       |
| <span data-ttu-id="8e2c9-131">MaxLength</span><span class="sxs-lookup"><span data-stu-id="8e2c9-131">MaxLength</span></span><br/>    | <span data-ttu-id="8e2c9-132">entier</span><span class="sxs-lookup"><span data-stu-id="8e2c9-132">integer</span></span><br/> | <span data-ttu-id="8e2c9-133">non défini</span><span class="sxs-lookup"><span data-stu-id="8e2c9-133">undefined</span></span><br/>       |
| <span data-ttu-id="8e2c9-134">MinLength</span><span class="sxs-lookup"><span data-stu-id="8e2c9-134">MinLength</span></span><br/>    | <span data-ttu-id="8e2c9-135">integer</span><span class="sxs-lookup"><span data-stu-id="8e2c9-135">integer</span></span><br/> | <span data-ttu-id="8e2c9-136">1</span><span class="sxs-lookup"><span data-stu-id="8e2c9-136">1</span></span><br/>               |
| <span data-ttu-id="8e2c9-137">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="8e2c9-137">Mandatory</span></span><br/>    | <span data-ttu-id="8e2c9-138">string</span><span class="sxs-lookup"><span data-stu-id="8e2c9-138">string</span></span><br/>  | <span data-ttu-id="8e2c9-139">PSK : conditionnel</span><span class="sxs-lookup"><span data-stu-id="8e2c9-139">psk:Conditional</span></span><br/> |
| <span data-ttu-id="8e2c9-140">Unité</span><span class="sxs-lookup"><span data-stu-id="8e2c9-140">UnitType</span></span><br/>     | <span data-ttu-id="8e2c9-141">string</span><span class="sxs-lookup"><span data-stu-id="8e2c9-141">string</span></span><br/>  | <span data-ttu-id="8e2c9-142">caractères</span><span class="sxs-lookup"><span data-stu-id="8e2c9-142">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="8e2c9-143">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8e2c9-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8e2c9-144">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="8e2c9-144">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




