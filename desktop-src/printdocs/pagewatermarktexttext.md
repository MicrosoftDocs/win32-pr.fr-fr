---
description: Obtenir plus d’informations sur le paramètre PageWatermarkTextText. Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: 3b01f05c-fe2e-4467-b2a7-5431a41200cd
title: PageWatermarkTextText
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3db5ef33008f0ccb66b6af34e2cc245b90c1ebea
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395964"
---
# <a name="pagewatermarktexttext"></a><span data-ttu-id="801c7-105">PageWatermarkTextText</span><span class="sxs-lookup"><span data-stu-id="801c7-105">PageWatermarkTextText</span></span>

<span data-ttu-id="801c7-106">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="801c7-106">This topic is not current.</span></span> <span data-ttu-id="801c7-107">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="801c7-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="801c7-108">Spécifie le texte du filigrane.</span><span class="sxs-lookup"><span data-stu-id="801c7-108">Specifies the text of the watermark.</span></span>

-   [<span data-ttu-id="801c7-109">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="801c7-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="801c7-110">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="801c7-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="801c7-111">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="801c7-111">Element Information</span></span>



| <span data-ttu-id="801c7-112">Nom</span><span class="sxs-lookup"><span data-stu-id="801c7-112">Name</span></span> | <span data-ttu-id="801c7-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="801c7-113">Value</span></span> |
|----------------------------|--------------------------------------------|
| <span data-ttu-id="801c7-114">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="801c7-114">Element Type</span></span> <br/>   | <span data-ttu-id="801c7-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="801c7-115">ParameterDef</span></span><br/>                    |
| <span data-ttu-id="801c7-116">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="801c7-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="801c7-117">Page</span><span class="sxs-lookup"><span data-stu-id="801c7-117">Page</span></span><br/>                            |
| <span data-ttu-id="801c7-118">Notes</span><span class="sxs-lookup"><span data-stu-id="801c7-118">Notes</span></span> <br/>          | <span data-ttu-id="801c7-119">Lié à l’élément PageWatermark</span><span class="sxs-lookup"><span data-stu-id="801c7-119">Linked to PageWatermark element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="801c7-120">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="801c7-120">Structure Content</span></span>

<span data-ttu-id="801c7-121">La structure XML de cet élément est la suivante :</span><span class="sxs-lookup"><span data-stu-id="801c7-121">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageWatermarkTextText">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:string</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
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

## <a name="structure-properties"></a><span data-ttu-id="801c7-122">Propriétés de structure</span><span class="sxs-lookup"><span data-stu-id="801c7-122">Structure Properties</span></span>

<span data-ttu-id="801c7-123">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="801c7-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="801c7-124">Propriété</span><span class="sxs-lookup"><span data-stu-id="801c7-124">Property</span></span>                | <span data-ttu-id="801c7-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="801c7-125">xsi:type</span></span>           | <span data-ttu-id="801c7-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="801c7-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="801c7-127">DataType</span><span class="sxs-lookup"><span data-stu-id="801c7-127">DataType</span></span><br/>     | <span data-ttu-id="801c7-128">String</span><span class="sxs-lookup"><span data-stu-id="801c7-128">String</span></span><br/>  | <span data-ttu-id="801c7-129">xs:string</span><span class="sxs-lookup"><span data-stu-id="801c7-129">xs:string</span></span><br/>       |
| <span data-ttu-id="801c7-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="801c7-130">DefaultValue</span></span><br/> | <span data-ttu-id="801c7-131">Integer</span><span class="sxs-lookup"><span data-stu-id="801c7-131">Integer</span></span><br/> | <span data-ttu-id="801c7-132">non défini</span><span class="sxs-lookup"><span data-stu-id="801c7-132">undefined</span></span><br/>       |
| <span data-ttu-id="801c7-133">MaxLength</span><span class="sxs-lookup"><span data-stu-id="801c7-133">MaxLength</span></span><br/>    | <span data-ttu-id="801c7-134">Integer</span><span class="sxs-lookup"><span data-stu-id="801c7-134">Integer</span></span><br/> | <span data-ttu-id="801c7-135">non défini</span><span class="sxs-lookup"><span data-stu-id="801c7-135">undefined</span></span><br/>       |
| <span data-ttu-id="801c7-136">MinLength</span><span class="sxs-lookup"><span data-stu-id="801c7-136">MinLength</span></span><br/>    | <span data-ttu-id="801c7-137">Integer</span><span class="sxs-lookup"><span data-stu-id="801c7-137">Integer</span></span><br/> | <span data-ttu-id="801c7-138">1</span><span class="sxs-lookup"><span data-stu-id="801c7-138">1</span></span><br/>               |
| <span data-ttu-id="801c7-139">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="801c7-139">Mandatory</span></span><br/>    | <span data-ttu-id="801c7-140">String</span><span class="sxs-lookup"><span data-stu-id="801c7-140">String</span></span><br/>  | <span data-ttu-id="801c7-141">PSK : conditionnel</span><span class="sxs-lookup"><span data-stu-id="801c7-141">psk:Conditional</span></span><br/> |
| <span data-ttu-id="801c7-142">Unité</span><span class="sxs-lookup"><span data-stu-id="801c7-142">UnitType</span></span><br/>     | <span data-ttu-id="801c7-143">String</span><span class="sxs-lookup"><span data-stu-id="801c7-143">String</span></span><br/>  | <span data-ttu-id="801c7-144">caractères</span><span class="sxs-lookup"><span data-stu-id="801c7-144">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="801c7-145">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="801c7-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="801c7-146">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="801c7-146">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




