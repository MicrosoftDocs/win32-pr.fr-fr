---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: cf35bb37-bf67-4e86-bfef-9838606982a5
title: PageScaling
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e32beceead1c0dc867a2bb7b24d476ef05bf8820
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997496"
---
# <a name="pagescaling"></a><span data-ttu-id="a226b-104">PageScaling</span><span class="sxs-lookup"><span data-stu-id="a226b-104">PageScaling</span></span>

<span data-ttu-id="a226b-105">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="a226b-105">This topic is not current.</span></span> <span data-ttu-id="a226b-106">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="a226b-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="a226b-107">Décrit les caractéristiques de mise à l’échelle de la sortie.</span><span class="sxs-lookup"><span data-stu-id="a226b-107">Describes the scaling characteristics of the output.</span></span> <span data-ttu-id="a226b-108">Certaines options de cette fonctionnalité requièrent que le consommateur soit en mesure de déterminer les caractéristiques des « dimensions de contenu de l’application ».</span><span class="sxs-lookup"><span data-stu-id="a226b-108">Certain Options of this Feature requires the consumer to be able to determine characteristics of the "application content dimensions."</span></span> <span data-ttu-id="a226b-109">En l’absence de la possibilité de déterminer ces caractéristiques, le consommateur doit avoir comme valeur par défaut l’option Identity.</span><span class="sxs-lookup"><span data-stu-id="a226b-109">In the absence of the ability to determine these characteristics, the consumer should default to the identity option.</span></span> <span data-ttu-id="a226b-110">Ces caractéristiques sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="a226b-110">These characteristics are:</span></span>



|                          |                                                                                                                                                                                                                                                       |
|--------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a226b-111">Taille du média d’application</span><span class="sxs-lookup"><span data-stu-id="a226b-111">Application Media Size</span></span>   | <span data-ttu-id="a226b-112">Dimensions des médias définies par la disposition de l’application.</span><span class="sxs-lookup"><span data-stu-id="a226b-112">The dimensions of the media defined by the application layout.</span></span> <span data-ttu-id="a226b-113">La taille du média d’application peut ou ne peut pas correspondre à un PageMediaSize pris en charge par le consommateur.</span><span class="sxs-lookup"><span data-stu-id="a226b-113">The application media size may or may not correspond to a PageMediaSize supported by the consumer.</span></span><br/>                                                                          |
| <span data-ttu-id="a226b-114">Taille du contenu de l’application</span><span class="sxs-lookup"><span data-stu-id="a226b-114">Application Content Size</span></span> | <span data-ttu-id="a226b-115">Dimensions des médias définies par la disposition de l’application.</span><span class="sxs-lookup"><span data-stu-id="a226b-115">The dimensions of the media defined by the application layout.</span></span> <span data-ttu-id="a226b-116">La taille du média d’application peut ou ne peut pas correspondre à un PageMediaSize pris en charge par le consommateur.</span><span class="sxs-lookup"><span data-stu-id="a226b-116">The application media size may or may not correspond to a PageMediaSize supported by the consumer.</span></span><br/>                                                                          |
| <span data-ttu-id="a226b-117">Taille du fond perdu de l’application</span><span class="sxs-lookup"><span data-stu-id="a226b-117">Application Bleed Size</span></span>   | <span data-ttu-id="a226b-118">Le décalage et l’étendue de la zone de fond perdu de l’application, une zone de dépassement de capacité utilisée par l’application pour l’inscription et la mise en page, par rapport à la taille du support d’application.</span><span class="sxs-lookup"><span data-stu-id="a226b-118">The offset and extent of the application bleed area, an overflow box used by application for registration and layout, in relation to the application media size.</span></span> <span data-ttu-id="a226b-119">La zone de fond perdu est supérieure ou égale à la taille du média de l’application.</span><span class="sxs-lookup"><span data-stu-id="a226b-119">The bleed area will be great than or equal to the application media size.</span></span><br/> |



 

-   [<span data-ttu-id="a226b-120">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="a226b-120">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="a226b-121">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="a226b-121">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="a226b-122">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="a226b-122">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="a226b-123">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="a226b-123">Element Information</span></span>



| <span data-ttu-id="a226b-124">Nom</span><span class="sxs-lookup"><span data-stu-id="a226b-124">Name</span></span> | <span data-ttu-id="a226b-125">Value</span><span class="sxs-lookup"><span data-stu-id="a226b-125">Value</span></span> |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a226b-126">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="a226b-126">Element Type</span></span> <br/>   | <span data-ttu-id="a226b-127">Fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="a226b-127">Feature</span></span><br/>                                                                                                                                                                                    |
| <span data-ttu-id="a226b-128">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="a226b-128">Scoping Prefix</span></span> <br/> | <span data-ttu-id="a226b-129">Page</span><span class="sxs-lookup"><span data-stu-id="a226b-129">Page</span></span><br/>                                                                                                                                                                                       |
| <span data-ttu-id="a226b-130">Notes</span><span class="sxs-lookup"><span data-stu-id="a226b-130">Notes</span></span> <br/>          | <span data-ttu-id="a226b-131">Haut, bas, gauche et droite sont relatifs à PageImageableSize.</span><span class="sxs-lookup"><span data-stu-id="a226b-131">Top, Bottom, Left, and Right are relative to the PageImageableSize.</span></span> <span data-ttu-id="a226b-132">Les coordonnées sont relatives à PageImageableSize, où l’origine de est relative à l’origine du PageImageableSize.</span><span class="sxs-lookup"><span data-stu-id="a226b-132">Coordinates are relative to PageImageableSize, where the origin of is relative to the origin of the PageImageableSize.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="a226b-133">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="a226b-133">Structural Content</span></span>

<span data-ttu-id="a226b-134">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="a226b-134">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageScaling">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <!-- Specifies offset of the width relative to the PageImageableSize.  
         Measured in microns. -->
    <psf:ScoredProperty name="psk:OffsetWidth">
      <psf:ParameterRef name="psk:PageScalingOffsetWidth" />
    </psf:ScoredProperty>
    <!-- Specifies offset of the height relative to the PageImageableSize.  
         Measured in microns. -->
    <psf:ScoredProperty name="psk:OffsetHeight">
      <psf:ParameterRef name="psk:PageScalingOffsetHeight" />
    </psf:ScoredProperty>
    <!-- Specifies the scaling percentage for the width dimension relative to the PageImageableSize. -->
    <psf:ScoredProperty name="psk:ScaleWidth">
      <psf:ParameterRef name="psk:PageScalingScaleWidth" />
    </psf:ScoredProperty>
    <!-- Specifies the scaling percentage for the height dimension relative to the PageImageableSize. -->
    <psf:ScoredProperty name="psk:ScaleHeight">
      <psf:ParameterRef name="psk:PageScalingScaleHeight" />
    </psf:ScoredProperty>
    <!-- Specifies the scaling percentage for square scaling (both dimensions are scaled equally). -->
    <psf:ScoredProperty name="psk:Scale">
      <psf:ParameterRef name="psk:PageScalingScale" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies the alignment of the scaled content. -->
  <psf:Feature name="psk:ScaleOffsetAlignment">
    <!-- Specifies the scaling should be aligned on the center of the bottom edge of the media. -->
    <psf:Option name="psk:BottomCenter"/>
    <!-- Specifies the scaling should be aligned on the bottom left corner of the media. -->
    <psf:Option name="psk:BottomLeft" />
    <!-- Specifies the scaling should be aligned on the bottom right corner of the media. -->
    <psf:Option name="psk:BottomRight "/>
    <!-- Specifies the scaling should be aligned on the bottom right corner of the media. -->
    <psf:Option name="psk:Center"/>
    <!-- Specifies the scaling should be aligned on the center of the left edge of the media. -->
    <psf:Option name="psk:LeftCenter"/>
    <!-- Specifies the scaling should be aligned on the center of the right edge of the media. -->
    <psf:Option name="psk:RightCenter"/>
    <!-- Specifies the scaling should be aligned on the center of the top edge of the media. -->
    <psf:Option name="psk:TopCenter"/>
    <!-- Specifies the scaling should be aligned on the top left corner of the media. -->
    <psf:Option name="psk:TopLeft"/>
    <!-- Specifies the scaling should be aligned on the top right corner of the media. -->
    <psf:Option name="psk:TopRight"/>
  </psf:Feature>
</psf:Feature>
```

## <a name="structure-variables"></a><span data-ttu-id="a226b-135">Variables de structure</span><span class="sxs-lookup"><span data-stu-id="a226b-135">Structure Variables</span></span>

<span data-ttu-id="a226b-136">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="a226b-136">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="a226b-137">Nom</span><span class="sxs-lookup"><span data-stu-id="a226b-137">Name</span></span>                               | <span data-ttu-id="a226b-138">Type de données</span><span class="sxs-lookup"><span data-stu-id="a226b-138">Data type</span></span>         | <span data-ttu-id="a226b-139">Unité</span><span class="sxs-lookup"><span data-stu-id="a226b-139">Unit</span></span>                  | <span data-ttu-id="a226b-140">Valeurs prises en charge</span><span class="sxs-lookup"><span data-stu-id="a226b-140">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="a226b-141">Résumé</span><span class="sxs-lookup"><span data-stu-id="a226b-141">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="a226b-142">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="a226b-142">\_OptionName\_</span></span><br/>          | <span data-ttu-id="a226b-143">string</span><span class="sxs-lookup"><span data-stu-id="a226b-143">string</span></span><br/> | <span data-ttu-id="a226b-144">caractères</span><span class="sxs-lookup"><span data-stu-id="a226b-144">characters</span></span><br/> | <span data-ttu-id="a226b-145">Nom complet valide tel que défini par les [espaces de noms dans XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="a226b-145">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="a226b-146">Si aucun espace de noms n’est spécifié, l’espace de noms par défaut est utilisé.</span><span class="sxs-lookup"><span data-stu-id="a226b-146">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="a226b-147">Nom de l'option.</span><span class="sxs-lookup"><span data-stu-id="a226b-147">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="a226b-148">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="a226b-148">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="a226b-149">string</span><span class="sxs-lookup"><span data-stu-id="a226b-149">string</span></span><br/> | <span data-ttu-id="a226b-150">n/a</span><span class="sxs-lookup"><span data-stu-id="a226b-150">n/a</span></span><br/>        | <span data-ttu-id="a226b-151">True, False.</span><span class="sxs-lookup"><span data-stu-id="a226b-151">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="a226b-152">Définit une option qui, lorsqu’elle est sélectionnée, désactive cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="a226b-152">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="a226b-153">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="a226b-153">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="a226b-154">Les mots clés de schéma d’impression publics sont définis dans l' https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords espace de noms.</span><span class="sxs-lookup"><span data-stu-id="a226b-154">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="a226b-155">Le contenu de la Extensible Markup Language publique (XML) pour ce mot clé est défini ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="a226b-155">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageScaling">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:Custom">
    <psf:ScoredProperty name="psk:OffsetWidth">
      <psf:ParameterRef name="psk:PageScalingOffsetWidth" />
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:OffsetHeight">
      <psf:ParameterRef name="psk:PageScalingOffsetHeight" />
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:ScaleWidth">
      <psf:ParameterRef name="psk:PageScalingScaleWidth" />
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:ScaleHeight">
      <psf:ParameterRef name="psk:PageScalingScaleHeight" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies a custom square scaling should be applied to the Application Media Size. -->
  <psf:Option name="psk:CustomSquare">
    <psf:ScoredProperty name="psk:OffsetWidth">
      <psf:ParameterRef name="psk:PageScalingOffsetWidth" />
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:OffsetHeight">
      <psf:ParameterRef name="psk:PageScalingOffsetHeight" />
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Scale">
      <psf:ParameterRef name="psk:PageScalingScale" />
    </psf:ScoredProperty>
  </psf:Option>

  <!-- Specifies the application bleed size should be scaled to the PageImageableSize preserving the aspect ratio. -->
  <psf:Option name="psk:FitApplicationBleedSizeToPageImageableSize" />
  <!-- Specifies the application content size should be scaled to the PageImageableSize preserving the aspect ratio. -->
  <psf:Option name="psk:FitApplicationContentSizeToPageImageableSize" />
  <!-- Specifies the application media size should be scaled to the PageImageableSize preserving the aspect ratio. -->
  <psf:Option name="psk:FitApplicationMediaSizeToPageImageableSize" />
  <!-- Specifies the application media size should be scaled to the PageMediaSize preserving the aspect ratio. -->
  <psf:Option name="psk:FitApplicationMediaSizeToPageMediaSize" />

  <!-- Specifies that no scaling should be applied. -->
  <psf:Option name="psk:None" />

  <!-- Specifies the alignment of the scaled content. -->
  <psf:Feature name="psk:ScaleOffsetAlignment">
    <!-- Specifies the scaling should be aligned on the center of the bottom edge of the media. -->
    <psf:Option name="psk:BottomCenter" />
    <!-- Specifies the scaling should be aligned on the bottom left corner of the media.-->
    <psf:Option name="psk:BottomLeft" />
    <!--Specifies the scaling should be aligned on the bottom right corner of the media.-->
    <psf:Option name="psk:BottomRight" />
    <!-- Specifies the scaling should be centered on the media.-->
    <psf:Option name="psk:Center" />
    <!-- Specifies the scaling should be aligned on the center of the left edge of the media.-->
    <psf:Option name="psk:LeftCenter" />
    <!--Specifies the scaling should be aligned on the center of the right edge of the media.-->
    <psf:Option name="psk:RightCenter" />
    <!-- Specifies the scaling should be aligned on the center of the top edge of the media.-->
    <psf:Option name="psk:TopCenter" />
    <!--  Specifies the scaling should be aligned on the top left corner of the media.-->
    <psf:Option name="psk:TopLeft" />
    <!-- Specifies the scaling should be aligned on the top right corner of the media.-->
    <psf:Option name="psk:TopRight" />
  </psf:Feature>
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="a226b-156">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a226b-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a226b-157">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="a226b-157">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




