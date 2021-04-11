---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: a15fe075-6696-4c70-b658-ae62d542bb4e
title: PageCopies
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6feef0745e3f9a86b3697b7e0ab65111fc3dfcb
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "104211313"
---
# <a name="pagecopies"></a><span data-ttu-id="92097-104">PageCopies</span><span class="sxs-lookup"><span data-stu-id="92097-104">PageCopies</span></span>

<span data-ttu-id="92097-105">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="92097-105">This topic is not current.</span></span> <span data-ttu-id="92097-106">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="92097-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="92097-107">Spécifie le nombre de copies d’une page.</span><span class="sxs-lookup"><span data-stu-id="92097-107">Specifies the number of copies of a page.</span></span>

-   [<span data-ttu-id="92097-108">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="92097-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="92097-109">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="92097-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="92097-110">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="92097-110">Element Information</span></span>



| <span data-ttu-id="92097-111">Nom</span><span class="sxs-lookup"><span data-stu-id="92097-111">Name</span></span>                       |                         |
|----------------------------|-------------------------|
| <span data-ttu-id="92097-112">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="92097-112">Element Type</span></span> <br/>   | <span data-ttu-id="92097-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="92097-113">ParameterDef</span></span><br/> |
| <span data-ttu-id="92097-114">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="92097-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="92097-115">Page</span><span class="sxs-lookup"><span data-stu-id="92097-115">Page</span></span><br/>         |
| <span data-ttu-id="92097-116">Notes</span><span class="sxs-lookup"><span data-stu-id="92097-116">Notes</span></span> <br/>          | <span data-ttu-id="92097-117">Aucun</span><span class="sxs-lookup"><span data-stu-id="92097-117">None</span></span><br/>         |



 

## <a name="structure-content"></a><span data-ttu-id="92097-118">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="92097-118">Structure Content</span></span>

<span data-ttu-id="92097-119">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="92097-119">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageCopies">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:integer</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxValue">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinValue">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Multiple">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Unconditional</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">copies</psf:Value>
  </psf:Property>
</psf:ParameterDef>
      
```

## <a name="structure-properties"></a><span data-ttu-id="92097-120">Propriétés de structure</span><span class="sxs-lookup"><span data-stu-id="92097-120">Structure Properties</span></span>

<span data-ttu-id="92097-121">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="92097-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="92097-122">Propriété</span><span class="sxs-lookup"><span data-stu-id="92097-122">Property</span></span>                | <span data-ttu-id="92097-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="92097-123">xsi:type</span></span>           | <span data-ttu-id="92097-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="92097-124">Value</span></span>                        |
|-------------------------|--------------------|------------------------------|
| <span data-ttu-id="92097-125">DataType</span><span class="sxs-lookup"><span data-stu-id="92097-125">DataType</span></span><br/>     | <span data-ttu-id="92097-126">string</span><span class="sxs-lookup"><span data-stu-id="92097-126">string</span></span><br/>  | <span data-ttu-id="92097-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="92097-127">xs:integer</span></span><br/>        |
| <span data-ttu-id="92097-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="92097-128">DefaultValue</span></span><br/> | <span data-ttu-id="92097-129">integer</span><span class="sxs-lookup"><span data-stu-id="92097-129">integer</span></span><br/> | <span data-ttu-id="92097-130">1</span><span class="sxs-lookup"><span data-stu-id="92097-130">1</span></span><br/>                 |
| <span data-ttu-id="92097-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="92097-131">MaxValue</span></span><br/>     | <span data-ttu-id="92097-132">entier</span><span class="sxs-lookup"><span data-stu-id="92097-132">integer</span></span><br/> | <span data-ttu-id="92097-133">non défini</span><span class="sxs-lookup"><span data-stu-id="92097-133">undefined</span></span><br/>         |
| <span data-ttu-id="92097-134">MinValue</span><span class="sxs-lookup"><span data-stu-id="92097-134">MinValue</span></span><br/>     | <span data-ttu-id="92097-135">integer</span><span class="sxs-lookup"><span data-stu-id="92097-135">integer</span></span><br/> | <span data-ttu-id="92097-136">1</span><span class="sxs-lookup"><span data-stu-id="92097-136">1</span></span><br/>                 |
| <span data-ttu-id="92097-137">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="92097-137">Mandatory</span></span><br/>    | <span data-ttu-id="92097-138">string</span><span class="sxs-lookup"><span data-stu-id="92097-138">string</span></span><br/>  | <span data-ttu-id="92097-139">PSK : sans condition</span><span class="sxs-lookup"><span data-stu-id="92097-139">psk:Unconditional</span></span><br/> |
| <span data-ttu-id="92097-140">Multiple</span><span class="sxs-lookup"><span data-stu-id="92097-140">Multiple</span></span><br/>     | <span data-ttu-id="92097-141">integer</span><span class="sxs-lookup"><span data-stu-id="92097-141">integer</span></span><br/> | <span data-ttu-id="92097-142">1</span><span class="sxs-lookup"><span data-stu-id="92097-142">1</span></span><br/>                 |
| <span data-ttu-id="92097-143">Unité</span><span class="sxs-lookup"><span data-stu-id="92097-143">UnitType</span></span><br/>     | <span data-ttu-id="92097-144">string</span><span class="sxs-lookup"><span data-stu-id="92097-144">string</span></span><br/>  | <span data-ttu-id="92097-145">copie</span><span class="sxs-lookup"><span data-stu-id="92097-145">copies</span></span><br/>            |



 

## <a name="related-topics"></a><span data-ttu-id="92097-146">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="92097-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="92097-147">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="92097-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




