---
description: En savoir plus sur l’élément PageBlackGenerationProcessing, qui spécifie le comportement de la génération noire pour les séparations CMJN.
ms.assetid: 4edd1fdf-9601-440d-b967-82ffa6dceeb1
title: PageBlackGenerationProcessing
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d21861595917b67390857b380a416e441d454081
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408512"
---
# <a name="pageblackgenerationprocessing"></a><span data-ttu-id="aa411-103">PageBlackGenerationProcessing</span><span class="sxs-lookup"><span data-stu-id="aa411-103">PageBlackGenerationProcessing</span></span>

<span data-ttu-id="aa411-104">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="aa411-104">This topic is not current.</span></span> <span data-ttu-id="aa411-105">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="aa411-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="aa411-106">Spécifie le comportement de la génération noire pour les séparations CMJN.</span><span class="sxs-lookup"><span data-stu-id="aa411-106">Specifies black generation behavior for CMYK separations.</span></span>

-   [<span data-ttu-id="aa411-107">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="aa411-107">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="aa411-108">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="aa411-108">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="aa411-109">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="aa411-109">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="aa411-110">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="aa411-110">Element Information</span></span>



| <span data-ttu-id="aa411-111">Nom</span><span class="sxs-lookup"><span data-stu-id="aa411-111">Name</span></span> | <span data-ttu-id="aa411-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="aa411-112">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="aa411-113">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="aa411-113">Element Type</span></span> <br/>   | <span data-ttu-id="aa411-114">Fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="aa411-114">Feature</span></span><br/> |
| <span data-ttu-id="aa411-115">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="aa411-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="aa411-116">Page</span><span class="sxs-lookup"><span data-stu-id="aa411-116">Page</span></span><br/>    |
| <span data-ttu-id="aa411-117">Notes</span><span class="sxs-lookup"><span data-stu-id="aa411-117">Notes</span></span> <br/>          | <span data-ttu-id="aa411-118">Aucun</span><span class="sxs-lookup"><span data-stu-id="aa411-118">None</span></span> <br/>   |



 

## <a name="structural-content"></a><span data-ttu-id="aa411-119">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="aa411-119">Structural Content</span></span>

<span data-ttu-id="aa411-120">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="aa411-120">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageBlackGenerationProcessing">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
  </psf:Option>
</psf:Feature>
```

## <a name="structure-variables"></a><span data-ttu-id="aa411-121">Variables de structure</span><span class="sxs-lookup"><span data-stu-id="aa411-121">Structure Variables</span></span>

<span data-ttu-id="aa411-122">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="aa411-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="aa411-123">Nom</span><span class="sxs-lookup"><span data-stu-id="aa411-123">Name</span></span>                               | <span data-ttu-id="aa411-124">Type de données</span><span class="sxs-lookup"><span data-stu-id="aa411-124">Data type</span></span>         | <span data-ttu-id="aa411-125">Unité</span><span class="sxs-lookup"><span data-stu-id="aa411-125">Unit</span></span>                  | <span data-ttu-id="aa411-126">Valeurs prises en charge</span><span class="sxs-lookup"><span data-stu-id="aa411-126">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="aa411-127">Résumé</span><span class="sxs-lookup"><span data-stu-id="aa411-127">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="aa411-128">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="aa411-128">\_OptionName\_</span></span><br/>          | <span data-ttu-id="aa411-129">string</span><span class="sxs-lookup"><span data-stu-id="aa411-129">string</span></span><br/> | <span data-ttu-id="aa411-130">caractères</span><span class="sxs-lookup"><span data-stu-id="aa411-130">characters</span></span><br/> | <span data-ttu-id="aa411-131">Nom complet valide tel que défini par les [espaces de noms dans XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="aa411-131">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="aa411-132">Si aucun espace de noms n’est spécifié, l’espace de noms par défaut est utilisé.</span><span class="sxs-lookup"><span data-stu-id="aa411-132">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="aa411-133">Nom de l'option.</span><span class="sxs-lookup"><span data-stu-id="aa411-133">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="aa411-134">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="aa411-134">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="aa411-135">string</span><span class="sxs-lookup"><span data-stu-id="aa411-135">string</span></span><br/> | <span data-ttu-id="aa411-136">n/a</span><span class="sxs-lookup"><span data-stu-id="aa411-136">n/a</span></span><br/>        | <span data-ttu-id="aa411-137">True, False.</span><span class="sxs-lookup"><span data-stu-id="aa411-137">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="aa411-138">Définit une option qui, lorsqu’elle est sélectionnée, désactive cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="aa411-138">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="aa411-139">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="aa411-139">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="aa411-140">Les mots clés de schéma d’impression publics sont définis dans l' https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords espace de noms.</span><span class="sxs-lookup"><span data-stu-id="aa411-140">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="aa411-141">Le contenu de la Extensible Markup Language publique (XML) pour ce mot clé est défini ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="aa411-141">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageBlackGenerationProcessing">
  <psf:Option name="psk:Automatic" />
  <psf:Option name="psk:Custom">
    <!-- The max allowable sum of the four ink coverages anywhere in an image. -->
    <psf:ScoredProperty name="psk:TotalInkCoverageLimit">
      <psf:ParameterRef name="psk:PageBlackGenerationProcessingTotalInkCoverageLimit" />
    </psf:ScoredProperty>
    <!-- The maximum allowed K channel value. -->
    <psf:ScoredProperty name="psk:BlackInkLimit">
      <psf:ParameterRef name="psk:PageBlackGenerationProcessingBlackInkLimit" />
    </psf:ScoredProperty>
    <!-- The percentage of gray component replacement to perform. -->
    <psf:ScoredProperty name="psk:GrayComponentReplacementLevel">
      <psf:ParameterRef name="psk:PageBlackGenerationProcessingGrayComponentReplacementLevel" />
    </psf:ScoredProperty>
    <!-- The point in the highlight to shadow range where GCR should start (100% = darkest shadow). -->
    <psf:ScoredProperty name="psk:GrayComponentReplacementStart">
      <psf:ParameterRef name="psk:PageBlackGenerationProcessingGrayComponentReplacementStart" />
    </psf:ScoredProperty>
    <!-- The extented beyond neutrals (into chromatic colors) that GCR applies.  0% = Undercolor component replacement, 100% = Gray component replacement.  -->
    <psf:ScoredProperty name="psk:GrayComponentReplacementExtent">
      <psf:ParameterRef name="psk:PageBlackGenerationProcessingGrayComponentReplacementExtent" />
    </psf:ScoredProperty>
    <!-- The shadow level below which UCA will be applied.  -->
    <psf:ScoredProperty name="psk:UnderColorAdditionStart">
      <psf:ParameterRef name="psk:PageBlackGenerationProcessingUnderColorAdditionStart" />
    </psf:ScoredProperty>
    <!-- The amount chromatic ink (in gray component ratios) to add to areas where GCR/UCR has generated "BlackInkLimit" (or UCAStart, if specified) in the dark neutrals and near-neutral areas.  -->
    <psf:ScoredProperty name="psk:UnderColorAdditionLevel">
      <psf:ParameterRef name="psk:PageBlackGenerationProcessingUnderColorAdditionLevel" />
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature> 
```

## <a name="related-topics"></a><span data-ttu-id="aa411-142">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="aa411-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aa411-143">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="aa411-143">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




