---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: d1c36c47-107c-4012-a839-1018c2652209
title: PageWatermark
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8d0e0e47aa89a3cb6380a78dd49312d17f88ab8
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "106539812"
---
# <a name="pagewatermark"></a><span data-ttu-id="d5f99-104">PageWatermark</span><span class="sxs-lookup"><span data-stu-id="d5f99-104">PageWatermark</span></span>

<span data-ttu-id="d5f99-105">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="d5f99-105">This topic is not current.</span></span> <span data-ttu-id="d5f99-106">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="d5f99-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="d5f99-107">Décrit le paramètre de filigrane des caractéristiques de sortie et de filigrane.</span><span class="sxs-lookup"><span data-stu-id="d5f99-107">Describes the watermark setting of the output and the watermark characteristics.</span></span> <span data-ttu-id="d5f99-108">Les filigranes s’appliquent à la page logique, et non à la page physique.</span><span class="sxs-lookup"><span data-stu-id="d5f99-108">Watermarks apply to the logical page, not the physical page.</span></span> <span data-ttu-id="d5f99-109">Par exemple, si DocumentDuplex est activé, un filigrane apparaît sur chaque page nettoyage sur chaque feuille.</span><span class="sxs-lookup"><span data-stu-id="d5f99-109">For example, if DocumentDuplex is enabled, a watermark will appear on each NUp page on each sheet.</span></span> <span data-ttu-id="d5f99-110">Si DocumentDuplex, PagesPerSheet = 2, chaque feuille aura 2 filigranes.</span><span class="sxs-lookup"><span data-stu-id="d5f99-110">If DocumentDuplex, PagesPerSheet=2, then each sheet will have 2 watermarks.</span></span>

-   [<span data-ttu-id="d5f99-111">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="d5f99-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="d5f99-112">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="d5f99-112">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="d5f99-113">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="d5f99-113">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="d5f99-114">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="d5f99-114">Element Information</span></span>



| <span data-ttu-id="d5f99-115">Nom</span><span class="sxs-lookup"><span data-stu-id="d5f99-115">Name</span></span>                       |                                                                                                                                                 |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5f99-116">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="d5f99-116">Element Type</span></span> <br/>   | <span data-ttu-id="d5f99-117">Fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="d5f99-117">Feature</span></span><br/>                                                                                                                              |
| <span data-ttu-id="d5f99-118">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="d5f99-118">Scoping Prefix</span></span> <br/> | <span data-ttu-id="d5f99-119">Page</span><span class="sxs-lookup"><span data-stu-id="d5f99-119">Page</span></span><br/>                                                                                                                                 |
| <span data-ttu-id="d5f99-120">Notes</span><span class="sxs-lookup"><span data-stu-id="d5f99-120">Notes</span></span> <br/>          | <span data-ttu-id="d5f99-121">Les coordonnées sont relatives à PageImageableSize, où l’origine du filigrane est relative à l’origine du PageImageableSize.</span><span class="sxs-lookup"><span data-stu-id="d5f99-121">Coordinates are relative to PageImageableSize, where the origin of the watermark is relative to the origin of the PageImageableSize.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="d5f99-122">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="d5f99-122">Structural Content</span></span>

<span data-ttu-id="d5f99-123">La structure XML de cet élément est la suivante :</span><span class="sxs-lookup"><span data-stu-id="d5f99-123">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:Feature name="psk:PageWatermark">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <!-- Defines the width origin of the watermark. See the PageWatermarkOriginWidth ParameterDefinition for more information. -->
    <psf:ScoredProperty name="psk:OriginWidth">
      <psf:ParameterRef name="psk:PageWatermarkOriginWidth" />
    </psf:ScoredProperty>
    <!-- Defines the height origin of the watermark. See the PageWatermarkOriginHeight ParameterDefinition for more information. -->
    <psf:ScoredProperty name="psk:OriginHeight">
      <psf:ParameterRef name="psk:PageWatermarkOriginHeight" />
    </psf:ScoredProperty>
    <!-- Defines the transparency value of the watermark.  Transparency should be applied to all content, including transparent content. See the PageWatermarkTransparency ParameterDefinition for more information. -->
    <psf:ScoredProperty name="psk:Transparency">
      <psf:ParameterRef name="psk:PageWatermarkTransparency" />
    </psf:ScoredProperty>
    <!-- Defines the angle value of the watermark.  See the PageWatermarkAngle ParameterDefinition for more information. -->
    <psf:ScoredProperty name="psk:Angle">
      <psf:ParameterRef name="psk:PageWatermarkAngle" />
    </psf:ScoredProperty>
    <!-- Applicable to options that include bitmaps.  -->
    <!-- Specifies the text font color -->
    <!-- Applicable to options that include text. Defines the sRGB color for the watermark text.  Format is ARGB: #AARRGGBB.   -->
    <psf:ScoredProperty name="psk:FontColor">
      <psf:ParameterRef name="psk:PageWatermarkTextColor" />
    </psf:ScoredProperty>
    <!-- Applicable to options that include text.  Defines the available font sizes for the watermark text. Measured in points.-->
    <psf:ScoredProperty name="psk:FontSize">
      <psf:ParameterRef name="psk:PageWatermarkTextFontSize" />
    </psf:ScoredProperty>
    <!-- Applicable to options that include text. Defines the text to be displayed in the watermark. -->
    <psf:ScoredProperty name="psk:Text">
      <psf:ParameterRef name="psk:PageWatermarkTextText" />
    </psf:ScoredProperty>
  </psf:Option>
  <!--Defines the layering behavior of the watermark. -->
  <psf:Feature name="psk:Layering">
    <!-- Watermark appears over page content. -->
    <psf:Option name="psk:Overlay" />
    <!-- Watermark appear under page content. -->
    <psf:Option name="psk:Underlay" />
  </psf:Feature>
</psf:Feature>
```

## <a name="structure-variables"></a><span data-ttu-id="d5f99-124">Variables de structure</span><span class="sxs-lookup"><span data-stu-id="d5f99-124">Structure Variables</span></span>

<span data-ttu-id="d5f99-125">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="d5f99-125">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="d5f99-126">Nom</span><span class="sxs-lookup"><span data-stu-id="d5f99-126">Name</span></span>                               | <span data-ttu-id="d5f99-127">Type de données</span><span class="sxs-lookup"><span data-stu-id="d5f99-127">Data type</span></span>         | <span data-ttu-id="d5f99-128">Unité</span><span class="sxs-lookup"><span data-stu-id="d5f99-128">Unit</span></span>                  | <span data-ttu-id="d5f99-129">Valeurs prises en charge</span><span class="sxs-lookup"><span data-stu-id="d5f99-129">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="d5f99-130">Résumé</span><span class="sxs-lookup"><span data-stu-id="d5f99-130">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="d5f99-131">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="d5f99-131">\_OptionName\_</span></span><br/>          | <span data-ttu-id="d5f99-132">string</span><span class="sxs-lookup"><span data-stu-id="d5f99-132">string</span></span><br/> | <span data-ttu-id="d5f99-133">caractères</span><span class="sxs-lookup"><span data-stu-id="d5f99-133">characters</span></span><br/> | <span data-ttu-id="d5f99-134">Nom complet valide tel que défini par les [espaces de noms dans XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="d5f99-134">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="d5f99-135">Si aucun espace de noms n’est spécifié, l’espace de noms par défaut est utilisé.</span><span class="sxs-lookup"><span data-stu-id="d5f99-135">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="d5f99-136">Nom de l'option.</span><span class="sxs-lookup"><span data-stu-id="d5f99-136">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="d5f99-137">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="d5f99-137">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="d5f99-138">string</span><span class="sxs-lookup"><span data-stu-id="d5f99-138">string</span></span><br/> | <span data-ttu-id="d5f99-139">n/a</span><span class="sxs-lookup"><span data-stu-id="d5f99-139">n/a</span></span><br/>        | <span data-ttu-id="d5f99-140">True, False.</span><span class="sxs-lookup"><span data-stu-id="d5f99-140">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="d5f99-141">Définit une option qui, lorsqu’elle est sélectionnée, désactive cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="d5f99-141">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="d5f99-142">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="d5f99-142">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="d5f99-143">Les mots clés de schéma d’impression publics sont définis dans l' https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords espace de noms.</span><span class="sxs-lookup"><span data-stu-id="d5f99-143">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="d5f99-144">Le contenu de la Extensible Markup Language publique (XML) pour ce mot clé est défini ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="d5f99-144">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageWatermark">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies a text only watermark -->
  <psf:Option name="psk:Text">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">True</psf:Value>
    </psf:Property>
    <psf:ScoredProperty name="psk:OriginWidth">
      <psf:ParameterRef name="psk:PageWatermarkOriginWidth" />
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:OriginHeight">
      <psf:ParameterRef name="psk:PageWatermarkOriginHeight" />
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FontColor">
      <psf:ParameterRef name="psk:PageWatermarkTextColor" />
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FontSize">
      <psf:ParameterRef name="psk:PageWatermarkTextFontSize" />
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Text">
      <psf:ParameterRef name="psk:PageWatermarkTextText" />
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Transparency">
      <psf:ParameterRef name="psk:PageWatermarkTransparency" />
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Angle">
      <psf:ParameterRef name="psk:PageWatermarkTextAngle" />
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Feature name="psk:Layering">
    <!--Specifies Overlay Layering-->
    <psf:Option name="psk:Overlay" />
    <!--Specifies Underlay Layering-->
    <psf:Option name="psk:Underlay" />
  </psf:Feature>
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="d5f99-145">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d5f99-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d5f99-146">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="d5f99-146">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




