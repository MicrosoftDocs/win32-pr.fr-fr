---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: 6319e8fc-787f-4bc8-8436-1b498b3882d2
title: DocumentCopiesAllPages
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 723242ddd127113b573f167e6902b27fcca9665a
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107993986"
---
# <a name="documentcopiesallpages"></a><span data-ttu-id="dc133-104">DocumentCopiesAllPages</span><span class="sxs-lookup"><span data-stu-id="dc133-104">DocumentCopiesAllPages</span></span>

<span data-ttu-id="dc133-105">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="dc133-105">This topic is not current.</span></span> <span data-ttu-id="dc133-106">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="dc133-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="dc133-107">Spécifie le nombre de copies d’un document.</span><span class="sxs-lookup"><span data-stu-id="dc133-107">Specifies the number of copies of a document.</span></span>

-   [<span data-ttu-id="dc133-108">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="dc133-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="dc133-109">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="dc133-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="dc133-110">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="dc133-110">Element Information</span></span>



| <span data-ttu-id="dc133-111">Nom</span><span class="sxs-lookup"><span data-stu-id="dc133-111">Name</span></span> | <span data-ttu-id="dc133-112">Value</span><span class="sxs-lookup"><span data-stu-id="dc133-112">Value</span></span> |
|----------------------------|-------------------------|
| <span data-ttu-id="dc133-113">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="dc133-113">Element Type</span></span> <br/>   | <span data-ttu-id="dc133-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="dc133-114">ParameterDef</span></span><br/> |
| <span data-ttu-id="dc133-115">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="dc133-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="dc133-116">Document</span><span class="sxs-lookup"><span data-stu-id="dc133-116">Document</span></span><br/>     |
| <span data-ttu-id="dc133-117">Notes</span><span class="sxs-lookup"><span data-stu-id="dc133-117">Notes</span></span> <br/>          | <span data-ttu-id="dc133-118">Aucun</span><span class="sxs-lookup"><span data-stu-id="dc133-118">None</span></span><br/>         |



 

## <a name="structure-content"></a><span data-ttu-id="dc133-119">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="dc133-119">Structure Content</span></span>

<span data-ttu-id="dc133-120">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="dc133-120">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:DocumentCopiesAllPages">
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

## <a name="structure-properties"></a><span data-ttu-id="dc133-121">Propriétés de structure</span><span class="sxs-lookup"><span data-stu-id="dc133-121">Structure Properties</span></span>

<span data-ttu-id="dc133-122">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="dc133-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="dc133-123">Propriété</span><span class="sxs-lookup"><span data-stu-id="dc133-123">Property</span></span>                | <span data-ttu-id="dc133-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="dc133-124">xsi:type</span></span>           | <span data-ttu-id="dc133-125">Value</span><span class="sxs-lookup"><span data-stu-id="dc133-125">Value</span></span>                        |
|-------------------------|--------------------|------------------------------|
| <span data-ttu-id="dc133-126">DataType</span><span class="sxs-lookup"><span data-stu-id="dc133-126">DataType</span></span><br/>     | <span data-ttu-id="dc133-127">string</span><span class="sxs-lookup"><span data-stu-id="dc133-127">string</span></span><br/>  | <span data-ttu-id="dc133-128">xs:integer</span><span class="sxs-lookup"><span data-stu-id="dc133-128">xs:integer</span></span><br/>        |
| <span data-ttu-id="dc133-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="dc133-129">DefaultValue</span></span><br/> | <span data-ttu-id="dc133-130">integer</span><span class="sxs-lookup"><span data-stu-id="dc133-130">integer</span></span><br/> | <span data-ttu-id="dc133-131">1</span><span class="sxs-lookup"><span data-stu-id="dc133-131">1</span></span><br/>                 |
| <span data-ttu-id="dc133-132">MaxValue</span><span class="sxs-lookup"><span data-stu-id="dc133-132">MaxValue</span></span><br/>     | <span data-ttu-id="dc133-133">entier</span><span class="sxs-lookup"><span data-stu-id="dc133-133">integer</span></span><br/> | <span data-ttu-id="dc133-134">non défini</span><span class="sxs-lookup"><span data-stu-id="dc133-134">undefined</span></span><br/>         |
| <span data-ttu-id="dc133-135">MinValue</span><span class="sxs-lookup"><span data-stu-id="dc133-135">MinValue</span></span><br/>     | <span data-ttu-id="dc133-136">integer</span><span class="sxs-lookup"><span data-stu-id="dc133-136">integer</span></span><br/> | <span data-ttu-id="dc133-137">1</span><span class="sxs-lookup"><span data-stu-id="dc133-137">1</span></span><br/>                 |
| <span data-ttu-id="dc133-138">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="dc133-138">Mandatory</span></span><br/>    | <span data-ttu-id="dc133-139">string</span><span class="sxs-lookup"><span data-stu-id="dc133-139">string</span></span><br/>  | <span data-ttu-id="dc133-140">PSK : sans condition</span><span class="sxs-lookup"><span data-stu-id="dc133-140">psk:Unconditional</span></span><br/> |
| <span data-ttu-id="dc133-141">Plusieurs</span><span class="sxs-lookup"><span data-stu-id="dc133-141">Multiple</span></span><br/>     | <span data-ttu-id="dc133-142">integer</span><span class="sxs-lookup"><span data-stu-id="dc133-142">integer</span></span><br/> | <span data-ttu-id="dc133-143">1</span><span class="sxs-lookup"><span data-stu-id="dc133-143">1</span></span><br/>                 |
| <span data-ttu-id="dc133-144">Unité</span><span class="sxs-lookup"><span data-stu-id="dc133-144">UnitType</span></span><br/>     | <span data-ttu-id="dc133-145">string</span><span class="sxs-lookup"><span data-stu-id="dc133-145">string</span></span><br/>  | <span data-ttu-id="dc133-146">copie</span><span class="sxs-lookup"><span data-stu-id="dc133-146">copies</span></span><br/>            |



 

## <a name="related-topics"></a><span data-ttu-id="dc133-147">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="dc133-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dc133-148">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="dc133-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




