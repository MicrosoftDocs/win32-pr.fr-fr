---
description: En savoir plus sur le paramètre PageDestinationColorProfileEmbedded. Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: b360f870-bfaa-4d4d-adce-17fcfc48b6a6
title: PageDestinationColorProfileEmbedded
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05865636b6554873844a99b523f8c21fe2bfc1c7
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/09/2021
ms.locfileid: "113549207"
---
# <a name="pagedestinationcolorprofileembedded"></a><span data-ttu-id="4618b-105">PageDestinationColorProfileEmbedded</span><span class="sxs-lookup"><span data-stu-id="4618b-105">PageDestinationColorProfileEmbedded</span></span>

<span data-ttu-id="4618b-106">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="4618b-106">This topic is not current.</span></span> <span data-ttu-id="4618b-107">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="4618b-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="4618b-108">Spécifie le profil de couleurs de destination incorporé.</span><span class="sxs-lookup"><span data-stu-id="4618b-108">Specifies the embedded destination color profile.</span></span>

-   [<span data-ttu-id="4618b-109">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="4618b-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="4618b-110">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="4618b-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="4618b-111">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="4618b-111">Element Information</span></span>



| <span data-ttu-id="4618b-112">Nom</span><span class="sxs-lookup"><span data-stu-id="4618b-112">Name</span></span> | <span data-ttu-id="4618b-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="4618b-113">Value</span></span> |
|----------------------------|----------------------------------------------------------|
| <span data-ttu-id="4618b-114">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="4618b-114">Element Type</span></span> <br/>   | <span data-ttu-id="4618b-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="4618b-115">ParameterDef</span></span><br/>                                  |
| <span data-ttu-id="4618b-116">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="4618b-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="4618b-117">Page</span><span class="sxs-lookup"><span data-stu-id="4618b-117">Page</span></span><br/>                                          |
| <span data-ttu-id="4618b-118">Remarques</span><span class="sxs-lookup"><span data-stu-id="4618b-118">Notes</span></span> <br/>          | <span data-ttu-id="4618b-119">Lié à l’élément PageDestinationColorProfile</span><span class="sxs-lookup"><span data-stu-id="4618b-119">Linked to PageDestinationColorProfile element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="4618b-120">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="4618b-120">Structure Content</span></span>

<span data-ttu-id="4618b-121">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="4618b-121">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageDestinationColorProfileEmbedded">
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

## <a name="structure-properties"></a><span data-ttu-id="4618b-122">Propriétés de structure</span><span class="sxs-lookup"><span data-stu-id="4618b-122">Structure Properties</span></span>

<span data-ttu-id="4618b-123">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="4618b-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="4618b-124">Propriété</span><span class="sxs-lookup"><span data-stu-id="4618b-124">Property</span></span>                | <span data-ttu-id="4618b-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="4618b-125">xsi:type</span></span>           | <span data-ttu-id="4618b-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="4618b-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="4618b-127">DataType</span><span class="sxs-lookup"><span data-stu-id="4618b-127">DataType</span></span><br/>     | <span data-ttu-id="4618b-128">string</span><span class="sxs-lookup"><span data-stu-id="4618b-128">string</span></span><br/>  | <span data-ttu-id="4618b-129">xs:string</span><span class="sxs-lookup"><span data-stu-id="4618b-129">xs:string</span></span><br/>       |
| <span data-ttu-id="4618b-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="4618b-130">DefaultValue</span></span><br/> | <span data-ttu-id="4618b-131">string</span><span class="sxs-lookup"><span data-stu-id="4618b-131">string</span></span><br/>  | <span data-ttu-id="4618b-132">non défini</span><span class="sxs-lookup"><span data-stu-id="4618b-132">undefined</span></span><br/>       |
| <span data-ttu-id="4618b-133">MaxLength</span><span class="sxs-lookup"><span data-stu-id="4618b-133">MaxLength</span></span><br/>    | <span data-ttu-id="4618b-134">entier</span><span class="sxs-lookup"><span data-stu-id="4618b-134">integer</span></span><br/> | <span data-ttu-id="4618b-135">non défini</span><span class="sxs-lookup"><span data-stu-id="4618b-135">undefined</span></span><br/>       |
| <span data-ttu-id="4618b-136">MinLength</span><span class="sxs-lookup"><span data-stu-id="4618b-136">MinLength</span></span><br/>    | <span data-ttu-id="4618b-137">integer</span><span class="sxs-lookup"><span data-stu-id="4618b-137">integer</span></span><br/> | <span data-ttu-id="4618b-138">1</span><span class="sxs-lookup"><span data-stu-id="4618b-138">1</span></span><br/>               |
| <span data-ttu-id="4618b-139">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="4618b-139">Mandatory</span></span><br/>    | <span data-ttu-id="4618b-140">string</span><span class="sxs-lookup"><span data-stu-id="4618b-140">string</span></span><br/>  | <span data-ttu-id="4618b-141">PSK : conditionnel</span><span class="sxs-lookup"><span data-stu-id="4618b-141">psk:Conditional</span></span><br/> |
| <span data-ttu-id="4618b-142">Unité</span><span class="sxs-lookup"><span data-stu-id="4618b-142">UnitType</span></span><br/>     | <span data-ttu-id="4618b-143">string</span><span class="sxs-lookup"><span data-stu-id="4618b-143">string</span></span><br/>  | <span data-ttu-id="4618b-144">caractères</span><span class="sxs-lookup"><span data-stu-id="4618b-144">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="4618b-145">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4618b-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4618b-146">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="4618b-146">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




