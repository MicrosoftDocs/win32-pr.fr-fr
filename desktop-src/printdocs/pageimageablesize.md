---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: 6b81814f-2d9e-4862-8633-6ba016c11dac
title: PageImageableSize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1eef9012a7fda3eed6afd16add1d483c35c1111
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996106"
---
# <a name="pageimageablesize"></a><span data-ttu-id="d2af0-104">PageImageableSize</span><span class="sxs-lookup"><span data-stu-id="d2af0-104">PageImageableSize</span></span>

<span data-ttu-id="d2af0-105">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="d2af0-105">This topic is not current.</span></span> <span data-ttu-id="d2af0-106">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="d2af0-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="d2af0-107">Décrit le canevas Imaged pour la disposition et le rendu.</span><span class="sxs-lookup"><span data-stu-id="d2af0-107">Describes the imaged canvas for layout and rendering.</span></span> <span data-ttu-id="d2af0-108">Ce rapport est basé sur PageMediaSize et PageOrientation.</span><span class="sxs-lookup"><span data-stu-id="d2af0-108">This will be reported based on PageMediaSize and PageOrientation.</span></span>

<span data-ttu-id="d2af0-109">Les diagrammes suivants illustrent l’utilisation des variables PageImageableSize basée sur PageOrientation.</span><span class="sxs-lookup"><span data-stu-id="d2af0-109">The following diagrams illustrate the PageImageableSize variables usage based on PageOrientation.</span></span>

![diagramme qui affiche les mesures des pages](images/local-1641910626-image.png)

-   [<span data-ttu-id="d2af0-111">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="d2af0-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="d2af0-112">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="d2af0-112">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="d2af0-113">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="d2af0-113">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="d2af0-114">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="d2af0-114">Element Information</span></span>



|                            |                     |
|----------------------------|---------------------|
| <span data-ttu-id="d2af0-115">Nom</span><span class="sxs-lookup"><span data-stu-id="d2af0-115">Name</span></span> | <span data-ttu-id="d2af0-116">Value</span><span class="sxs-lookup"><span data-stu-id="d2af0-116">Value</span></span> |
| <span data-ttu-id="d2af0-117">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="d2af0-117">Element Type</span></span><br/>    | <span data-ttu-id="d2af0-118">Propriété</span><span class="sxs-lookup"><span data-stu-id="d2af0-118">Property</span></span><br/> |
| <span data-ttu-id="d2af0-119">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="d2af0-119">Scoping Prefix</span></span> <br/> | <span data-ttu-id="d2af0-120">Page</span><span class="sxs-lookup"><span data-stu-id="d2af0-120">Page</span></span><br/>     |
| <span data-ttu-id="d2af0-121">Notes</span><span class="sxs-lookup"><span data-stu-id="d2af0-121">Notes</span></span> <br/>          | <span data-ttu-id="d2af0-122">Aucun</span><span class="sxs-lookup"><span data-stu-id="d2af0-122">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="d2af0-123">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="d2af0-123">Structural Content</span></span>

<span data-ttu-id="d2af0-124">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="d2af0-124">The XML structure of this element is:</span></span>

``` syntax
<psf:Property name="psk:PageImageableSize">
  <psf:Property name="psk:ImageableSizeWidth">
    <psf:Value xsi:type="xs:integer">_ImageableSizeWidthValue_</psf:Value>
  </psf:Property>
  <psf:Property name="psk:ImageableSizeHeight">
    <psf:Value xsi:type="xs:integer">_ImageableSizeHeightValue_</psf:Value>
  </psf:Property>
  <!--Specifies the imageable area within the logical page.  -->
  <psf:Property name="psk:ImageableArea">
    <psf:Property name="psk:OriginWidth">
      <psf:Value xsi:type="xs:integer">_OriginWidthValue_</psf:Value>
    </psf:Property>
    <psf:Property name="psk:OriginHeight">
      <psf:Value xsi:type="xs:integer">_OriginHeightValue_</psf:Value>
    </psf:Property>
    <psf:Property name="psk:ExtentWidth">
      <psf:Value xsi:type="xs:integer">_ExtentWidthValue_</psf:Value>
    </psf:Property>
    <psf:Property name="psk:ExtentHeight">
      <psf:Value xsi:type="xs:integer">_ExtentHeightValue_</psf:Value>
    </psf:Property>
  </psf:Property>
</psf:Property>
```

## <a name="structure-variables"></a><span data-ttu-id="d2af0-125">Variables de structure</span><span class="sxs-lookup"><span data-stu-id="d2af0-125">Structure Variables</span></span>

<span data-ttu-id="d2af0-126">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="d2af0-126">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="d2af0-127">Nom</span><span class="sxs-lookup"><span data-stu-id="d2af0-127">Name</span></span>                                    | <span data-ttu-id="d2af0-128">Type de données</span><span class="sxs-lookup"><span data-stu-id="d2af0-128">Data type</span></span>          | <span data-ttu-id="d2af0-129">Unité</span><span class="sxs-lookup"><span data-stu-id="d2af0-129">Unit</span></span>               | <span data-ttu-id="d2af0-130">Valeurs prises en charge</span><span class="sxs-lookup"><span data-stu-id="d2af0-130">Supported values</span></span>                       | <span data-ttu-id="d2af0-131">Résumé</span><span class="sxs-lookup"><span data-stu-id="d2af0-131">Summary</span></span>                                                                                                                    |
|-----------------------------------------|--------------------|--------------------|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d2af0-132">\_ImageableSizeWidthValue\_</span><span class="sxs-lookup"><span data-stu-id="d2af0-132">\_ImageableSizeWidthValue\_</span></span><br/>  | <span data-ttu-id="d2af0-133">entier</span><span class="sxs-lookup"><span data-stu-id="d2af0-133">integer</span></span><br/> | <span data-ttu-id="d2af0-134">microns</span><span class="sxs-lookup"><span data-stu-id="d2af0-134">microns</span></span><br/> | <span data-ttu-id="d2af0-135">Supérieur à 0.</span><span class="sxs-lookup"><span data-stu-id="d2af0-135">Greater than 0.</span></span><br/>             | <span data-ttu-id="d2af0-136">Spécifie la dimension horizontale de la taille du média d’application par rapport au PageOrientation.</span><span class="sxs-lookup"><span data-stu-id="d2af0-136">Specifies the horizontal dimension of the application media size relative to the PageOrientation.</span></span><br/>               |
| <span data-ttu-id="d2af0-137">\_ImageableSizeHeightValue\_</span><span class="sxs-lookup"><span data-stu-id="d2af0-137">\_ImageableSizeHeightValue\_</span></span><br/> | <span data-ttu-id="d2af0-138">entier</span><span class="sxs-lookup"><span data-stu-id="d2af0-138">integer</span></span><br/> | <span data-ttu-id="d2af0-139">microns</span><span class="sxs-lookup"><span data-stu-id="d2af0-139">microns</span></span><br/> | <span data-ttu-id="d2af0-140">Supérieur à 0.</span><span class="sxs-lookup"><span data-stu-id="d2af0-140">Greater than 0.</span></span><br/>             | <span data-ttu-id="d2af0-141">Spécifie la dimension verticale de la taille du média d’application par rapport au PageOrientation.</span><span class="sxs-lookup"><span data-stu-id="d2af0-141">Specifies the vertical dimension of the application media size relative to the PageOrientation.</span></span><br/>                 |
| <span data-ttu-id="d2af0-142">\_OriginWidthValue\_</span><span class="sxs-lookup"><span data-stu-id="d2af0-142">\_OriginWidthValue\_</span></span><br/>         | <span data-ttu-id="d2af0-143">entier</span><span class="sxs-lookup"><span data-stu-id="d2af0-143">integer</span></span><br/> | <span data-ttu-id="d2af0-144">microns</span><span class="sxs-lookup"><span data-stu-id="d2af0-144">microns</span></span><br/> | <span data-ttu-id="d2af0-145">Supérieur ou égal à 0.</span><span class="sxs-lookup"><span data-stu-id="d2af0-145">Greater than or equal to 0.</span></span><br/> | <span data-ttu-id="d2af0-146">Spécifie l’origine horizontale de la zone imageable par rapport à la taille du média d’application.</span><span class="sxs-lookup"><span data-stu-id="d2af0-146">Specifies the horizontal origin of the imageable area relative to the application media size.</span></span><br/>                   |
| <span data-ttu-id="d2af0-147">\_OriginHeightValue\_</span><span class="sxs-lookup"><span data-stu-id="d2af0-147">\_OriginHeightValue\_</span></span><br/>        | <span data-ttu-id="d2af0-148">entier</span><span class="sxs-lookup"><span data-stu-id="d2af0-148">integer</span></span><br/> | <span data-ttu-id="d2af0-149">microns</span><span class="sxs-lookup"><span data-stu-id="d2af0-149">microns</span></span><br/> | <span data-ttu-id="d2af0-150">Supérieur ou égal à 0.</span><span class="sxs-lookup"><span data-stu-id="d2af0-150">Greater than or equal to 0.</span></span><br/> | <span data-ttu-id="d2af0-151">Spécifie l’origine verticale de la zone imageable par rapport à la taille du média d’application.</span><span class="sxs-lookup"><span data-stu-id="d2af0-151">Specifies the vertical origin of the imageable area relative to the application media size.</span></span><br/>                     |
| <span data-ttu-id="d2af0-152">\_ExtentWidthValue\_</span><span class="sxs-lookup"><span data-stu-id="d2af0-152">\_ExtentWidthValue\_</span></span><br/>         | <span data-ttu-id="d2af0-153">entier</span><span class="sxs-lookup"><span data-stu-id="d2af0-153">integer</span></span><br/> | <span data-ttu-id="d2af0-154">microns</span><span class="sxs-lookup"><span data-stu-id="d2af0-154">microns</span></span><br/> | <span data-ttu-id="d2af0-155">Supérieur à 0.</span><span class="sxs-lookup"><span data-stu-id="d2af0-155">Greater than 0.</span></span><br/>             | <span data-ttu-id="d2af0-156">Spécifie la distance horizontale entre l’origine et la limite limite de la taille du média d’application.</span><span class="sxs-lookup"><span data-stu-id="d2af0-156">Specifies the horizontal distance between the origin and the bounding limit of the application media size.</span></span><br/>      |
| <span data-ttu-id="d2af0-157">\_ExtentHeightValue\_</span><span class="sxs-lookup"><span data-stu-id="d2af0-157">\_ExtentHeightValue\_</span></span><br/>        | <span data-ttu-id="d2af0-158">entier</span><span class="sxs-lookup"><span data-stu-id="d2af0-158">integer</span></span><br/> | <span data-ttu-id="d2af0-159">microns</span><span class="sxs-lookup"><span data-stu-id="d2af0-159">microns</span></span><br/> | <span data-ttu-id="d2af0-160">Supérieur à 0.</span><span class="sxs-lookup"><span data-stu-id="d2af0-160">Greater than 0.</span></span><br/>             | <span data-ttu-id="d2af0-161">Spécifie la distance verticale entre l’origine et la limite limite de la taille du média de l’application de canevas.</span><span class="sxs-lookup"><span data-stu-id="d2af0-161">Specifies the vertical distance between the origin and the bounding limit of the canvas application media size.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="d2af0-162">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="d2af0-162">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="d2af0-163">Les mots clés de schéma d’impression publics sont définis dans l' https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords espace de noms.</span><span class="sxs-lookup"><span data-stu-id="d2af0-163">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="d2af0-164">Le contenu de la Extensible Markup Language publique (XML) pour ce mot clé est défini ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="d2af0-164">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Property name="psk:PageImageableSize">
  <psf:Property name="psk:ImageableSizeWidth">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psk:ImageableSizeHeight">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
    <psf:Property name="psk:ImageableArea">
      <psf:Property name="psk:OriginWidth">
        <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
      </psf:Property>
    <psf:Property name="psk:OriginHeight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:Property>
    <psf:Property name="psk:ExtentWidth">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:Property>
    <psf:Property name="psk:ExtentHeight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:Property>
  </psf:Property>
</psf:Property>
  
```

## <a name="related-topics"></a><span data-ttu-id="d2af0-165">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d2af0-165">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d2af0-166">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="d2af0-166">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




