---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: e1cb7e46-3078-46bf-a8c8-e10f6b9dd222
title: DocumentImpositionColor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea74db8ac616bc9ca6b7f6cde22f62bea742e7fb
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "106542104"
---
# <a name="documentimpositioncolor"></a><span data-ttu-id="df836-104">DocumentImpositionColor</span><span class="sxs-lookup"><span data-stu-id="df836-104">DocumentImpositionColor</span></span>

<span data-ttu-id="df836-105">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="df836-105">This topic is not current.</span></span> <span data-ttu-id="df836-106">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="df836-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="df836-107">Le contenu de l’application étiqueté avec la couleur nommée spécifiée doit apparaître dans toutes les séparations de couleurs.</span><span class="sxs-lookup"><span data-stu-id="df836-107">Application content labeled with the specified named color MUST appear on all color separations.</span></span>

-   [<span data-ttu-id="df836-108">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="df836-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="df836-109">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="df836-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="df836-110">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="df836-110">Element Information</span></span>



| <span data-ttu-id="df836-111">Nom</span><span class="sxs-lookup"><span data-stu-id="df836-111">Name</span></span>                       |                         |
|----------------------------|-------------------------|
| <span data-ttu-id="df836-112">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="df836-112">Element Type</span></span> <br/>   | <span data-ttu-id="df836-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="df836-113">ParameterDef</span></span><br/> |
| <span data-ttu-id="df836-114">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="df836-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="df836-115">Document</span><span class="sxs-lookup"><span data-stu-id="df836-115">Document</span></span><br/>     |
| <span data-ttu-id="df836-116">Notes</span><span class="sxs-lookup"><span data-stu-id="df836-116">Notes</span></span> <br/>          | <span data-ttu-id="df836-117">Aucun</span><span class="sxs-lookup"><span data-stu-id="df836-117">None</span></span><br/>         |



 

## <a name="structure-content"></a><span data-ttu-id="df836-118">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="df836-118">Structure Content</span></span>

<span data-ttu-id="df836-119">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="df836-119">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:DocumentImpositionColor">
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

## <a name="structure-properties"></a><span data-ttu-id="df836-120">Propriétés de structure</span><span class="sxs-lookup"><span data-stu-id="df836-120">Structure Properties</span></span>

<span data-ttu-id="df836-121">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="df836-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="df836-122">Propriété</span><span class="sxs-lookup"><span data-stu-id="df836-122">Property</span></span>                | <span data-ttu-id="df836-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="df836-123">xsi:type</span></span>           | <span data-ttu-id="df836-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="df836-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="df836-125">DataType</span><span class="sxs-lookup"><span data-stu-id="df836-125">DataType</span></span><br/>     | <span data-ttu-id="df836-126">string</span><span class="sxs-lookup"><span data-stu-id="df836-126">string</span></span><br/>  | <span data-ttu-id="df836-127">xs:string</span><span class="sxs-lookup"><span data-stu-id="df836-127">xs:string</span></span><br/>       |
| <span data-ttu-id="df836-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="df836-128">DefaultValue</span></span><br/> | <span data-ttu-id="df836-129">string</span><span class="sxs-lookup"><span data-stu-id="df836-129">string</span></span><br/>  | <span data-ttu-id="df836-130">non défini</span><span class="sxs-lookup"><span data-stu-id="df836-130">undefined</span></span><br/>       |
| <span data-ttu-id="df836-131">MaxLength</span><span class="sxs-lookup"><span data-stu-id="df836-131">MaxLength</span></span><br/>    | <span data-ttu-id="df836-132">entier</span><span class="sxs-lookup"><span data-stu-id="df836-132">integer</span></span><br/> | <span data-ttu-id="df836-133">non défini</span><span class="sxs-lookup"><span data-stu-id="df836-133">undefined</span></span><br/>       |
| <span data-ttu-id="df836-134">MinLength</span><span class="sxs-lookup"><span data-stu-id="df836-134">MinLength</span></span><br/>    | <span data-ttu-id="df836-135">integer</span><span class="sxs-lookup"><span data-stu-id="df836-135">integer</span></span><br/> | <span data-ttu-id="df836-136">1</span><span class="sxs-lookup"><span data-stu-id="df836-136">1</span></span><br/>               |
| <span data-ttu-id="df836-137">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="df836-137">Mandatory</span></span><br/>    | <span data-ttu-id="df836-138">string</span><span class="sxs-lookup"><span data-stu-id="df836-138">string</span></span><br/>  | <span data-ttu-id="df836-139">PSK : conditionnel</span><span class="sxs-lookup"><span data-stu-id="df836-139">psk:Conditional</span></span><br/> |
| <span data-ttu-id="df836-140">Unité</span><span class="sxs-lookup"><span data-stu-id="df836-140">UnitType</span></span><br/>     | <span data-ttu-id="df836-141">string</span><span class="sxs-lookup"><span data-stu-id="df836-141">string</span></span><br/>  | <span data-ttu-id="df836-142">caractères</span><span class="sxs-lookup"><span data-stu-id="df836-142">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="df836-143">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="df836-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="df836-144">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="df836-144">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




