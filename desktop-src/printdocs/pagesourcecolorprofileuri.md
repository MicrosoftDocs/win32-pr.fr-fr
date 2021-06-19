---
description: Obtenir des informations sur le paramètre PageSourceColorProfileURI. Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: 25c3c70f-20e3-4e44-9c59-bb66b4bd14d9
title: PageSourceColorProfileURI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7b6acd064a6b0652720a6c0d783f10a7467fa16
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395624"
---
# <a name="pagesourcecolorprofileuri"></a><span data-ttu-id="8861c-105">PageSourceColorProfileURI</span><span class="sxs-lookup"><span data-stu-id="8861c-105">PageSourceColorProfileURI</span></span>

<span data-ttu-id="8861c-106">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="8861c-106">This topic is not current.</span></span> <span data-ttu-id="8861c-107">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="8861c-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="8861c-108">Spécifie la source du profil de couleurs.</span><span class="sxs-lookup"><span data-stu-id="8861c-108">Specifies the source for color profile.</span></span>

-   [<span data-ttu-id="8861c-109">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="8861c-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="8861c-110">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="8861c-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="8861c-111">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="8861c-111">Element Information</span></span>



| <span data-ttu-id="8861c-112">Nom</span><span class="sxs-lookup"><span data-stu-id="8861c-112">Name</span></span> | <span data-ttu-id="8861c-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="8861c-113">Value</span></span> |
|----------------------------|-----------------------------------------------------|
| <span data-ttu-id="8861c-114">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="8861c-114">Element Type</span></span> <br/>   | <span data-ttu-id="8861c-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="8861c-115">ParameterDef</span></span><br/>                             |
| <span data-ttu-id="8861c-116">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="8861c-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="8861c-117">Page</span><span class="sxs-lookup"><span data-stu-id="8861c-117">Page</span></span><br/>                                     |
| <span data-ttu-id="8861c-118">Notes</span><span class="sxs-lookup"><span data-stu-id="8861c-118">Notes</span></span> <br/>          | <span data-ttu-id="8861c-119">Lié à l’élément PageSourceColorProfile</span><span class="sxs-lookup"><span data-stu-id="8861c-119">Linked to PageSourceColorProfile element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="8861c-120">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="8861c-120">Structure Content</span></span>

<span data-ttu-id="8861c-121">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="8861c-121">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="8861c-122">Propriétés de structure</span><span class="sxs-lookup"><span data-stu-id="8861c-122">Structure Properties</span></span>

<span data-ttu-id="8861c-123">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="8861c-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="8861c-124">Propriété</span><span class="sxs-lookup"><span data-stu-id="8861c-124">Property</span></span>                | <span data-ttu-id="8861c-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="8861c-125">xsi:type</span></span>           | <span data-ttu-id="8861c-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="8861c-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="8861c-127">DataType</span><span class="sxs-lookup"><span data-stu-id="8861c-127">DataType</span></span><br/>     | <span data-ttu-id="8861c-128">string</span><span class="sxs-lookup"><span data-stu-id="8861c-128">string</span></span><br/>  | <span data-ttu-id="8861c-129">xs:string</span><span class="sxs-lookup"><span data-stu-id="8861c-129">xs:string</span></span><br/>       |
| <span data-ttu-id="8861c-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="8861c-130">DefaultValue</span></span><br/> | <span data-ttu-id="8861c-131">string</span><span class="sxs-lookup"><span data-stu-id="8861c-131">string</span></span><br/>  | <span data-ttu-id="8861c-132">non défini</span><span class="sxs-lookup"><span data-stu-id="8861c-132">undefined</span></span><br/>       |
| <span data-ttu-id="8861c-133">MaxLength</span><span class="sxs-lookup"><span data-stu-id="8861c-133">MaxLength</span></span><br/>    | <span data-ttu-id="8861c-134">entier</span><span class="sxs-lookup"><span data-stu-id="8861c-134">integer</span></span><br/> | <span data-ttu-id="8861c-135">non défini</span><span class="sxs-lookup"><span data-stu-id="8861c-135">undefined</span></span><br/>       |
| <span data-ttu-id="8861c-136">MinLength</span><span class="sxs-lookup"><span data-stu-id="8861c-136">MinLength</span></span><br/>    | <span data-ttu-id="8861c-137">integer</span><span class="sxs-lookup"><span data-stu-id="8861c-137">integer</span></span><br/> | <span data-ttu-id="8861c-138">1</span><span class="sxs-lookup"><span data-stu-id="8861c-138">1</span></span><br/>               |
| <span data-ttu-id="8861c-139">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="8861c-139">Mandatory</span></span><br/>    | <span data-ttu-id="8861c-140">string</span><span class="sxs-lookup"><span data-stu-id="8861c-140">string</span></span><br/>  | <span data-ttu-id="8861c-141">PSK : conditionnel</span><span class="sxs-lookup"><span data-stu-id="8861c-141">psk:Conditional</span></span><br/> |
| <span data-ttu-id="8861c-142">Unité</span><span class="sxs-lookup"><span data-stu-id="8861c-142">UnitType</span></span><br/>     | <span data-ttu-id="8861c-143">string</span><span class="sxs-lookup"><span data-stu-id="8861c-143">string</span></span><br/>  | <span data-ttu-id="8861c-144">caractères</span><span class="sxs-lookup"><span data-stu-id="8861c-144">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="8861c-145">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8861c-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8861c-146">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="8861c-146">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




