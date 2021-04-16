---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: 6b81814f-2d9e-4862-8633-6ba016c11dac
title: PageImageableSize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26dca243defc08b43a79e897bfa91913a954bf37
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "104557086"
---
# <a name="pageimageablesize"></a><span data-ttu-id="547ef-104">PageImageableSize</span><span class="sxs-lookup"><span data-stu-id="547ef-104">PageImageableSize</span></span>

<span data-ttu-id="547ef-105">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="547ef-105">This topic is not current.</span></span> <span data-ttu-id="547ef-106">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="547ef-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="547ef-107">Décrit le canevas Imaged pour la disposition et le rendu.</span><span class="sxs-lookup"><span data-stu-id="547ef-107">Describes the imaged canvas for layout and rendering.</span></span> <span data-ttu-id="547ef-108">Ce rapport est basé sur PageMediaSize et PageOrientation.</span><span class="sxs-lookup"><span data-stu-id="547ef-108">This will be reported based on PageMediaSize and PageOrientation.</span></span>

<span data-ttu-id="547ef-109">Les diagrammes suivants illustrent l’utilisation des variables PageImageableSize basée sur PageOrientation.</span><span class="sxs-lookup"><span data-stu-id="547ef-109">The following diagrams illustrate the PageImageableSize variables usage based on PageOrientation.</span></span>

![diagramme qui affiche les mesures des pages](images/local-1641910626-image.png)

-   [<span data-ttu-id="547ef-111">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="547ef-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="547ef-112">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="547ef-112">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="547ef-113">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="547ef-113">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="547ef-114">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="547ef-114">Element Information</span></span>



|                            |                     |
|----------------------------|---------------------|
| <span data-ttu-id="547ef-115">Nom</span><span class="sxs-lookup"><span data-stu-id="547ef-115">Name</span></span>                       |                     |
| <span data-ttu-id="547ef-116">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="547ef-116">Element Type</span></span><br/>    | <span data-ttu-id="547ef-117">Propriété</span><span class="sxs-lookup"><span data-stu-id="547ef-117">Property</span></span><br/> |
| <span data-ttu-id="547ef-118">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="547ef-118">Scoping Prefix</span></span> <br/> | <span data-ttu-id="547ef-119">Page</span><span class="sxs-lookup"><span data-stu-id="547ef-119">Page</span></span><br/>     |
| <span data-ttu-id="547ef-120">Notes</span><span class="sxs-lookup"><span data-stu-id="547ef-120">Notes</span></span> <br/>          | <span data-ttu-id="547ef-121">Aucun</span><span class="sxs-lookup"><span data-stu-id="547ef-121">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="547ef-122">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="547ef-122">Structural Content</span></span>

<span data-ttu-id="547ef-123">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="547ef-123">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="547ef-124">Variables de structure</span><span class="sxs-lookup"><span data-stu-id="547ef-124">Structure Variables</span></span>

<span data-ttu-id="547ef-125">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="547ef-125">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="547ef-126">Nom</span><span class="sxs-lookup"><span data-stu-id="547ef-126">Name</span></span>                                    | <span data-ttu-id="547ef-127">Type de données</span><span class="sxs-lookup"><span data-stu-id="547ef-127">Data type</span></span>          | <span data-ttu-id="547ef-128">Unité</span><span class="sxs-lookup"><span data-stu-id="547ef-128">Unit</span></span>               | <span data-ttu-id="547ef-129">Valeurs prises en charge</span><span class="sxs-lookup"><span data-stu-id="547ef-129">Supported values</span></span>                       | <span data-ttu-id="547ef-130">Résumé</span><span class="sxs-lookup"><span data-stu-id="547ef-130">Summary</span></span>                                                                                                                    |
|-----------------------------------------|--------------------|--------------------|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="547ef-131">\_ImageableSizeWidthValue\_</span><span class="sxs-lookup"><span data-stu-id="547ef-131">\_ImageableSizeWidthValue\_</span></span><br/>  | <span data-ttu-id="547ef-132">entier</span><span class="sxs-lookup"><span data-stu-id="547ef-132">integer</span></span><br/> | <span data-ttu-id="547ef-133">microns</span><span class="sxs-lookup"><span data-stu-id="547ef-133">microns</span></span><br/> | <span data-ttu-id="547ef-134">Supérieur à 0.</span><span class="sxs-lookup"><span data-stu-id="547ef-134">Greater than 0.</span></span><br/>             | <span data-ttu-id="547ef-135">Spécifie la dimension horizontale de la taille du média d’application par rapport au PageOrientation.</span><span class="sxs-lookup"><span data-stu-id="547ef-135">Specifies the horizontal dimension of the application media size relative to the PageOrientation.</span></span><br/>               |
| <span data-ttu-id="547ef-136">\_ImageableSizeHeightValue\_</span><span class="sxs-lookup"><span data-stu-id="547ef-136">\_ImageableSizeHeightValue\_</span></span><br/> | <span data-ttu-id="547ef-137">entier</span><span class="sxs-lookup"><span data-stu-id="547ef-137">integer</span></span><br/> | <span data-ttu-id="547ef-138">microns</span><span class="sxs-lookup"><span data-stu-id="547ef-138">microns</span></span><br/> | <span data-ttu-id="547ef-139">Supérieur à 0.</span><span class="sxs-lookup"><span data-stu-id="547ef-139">Greater than 0.</span></span><br/>             | <span data-ttu-id="547ef-140">Spécifie la dimension verticale de la taille du média d’application par rapport au PageOrientation.</span><span class="sxs-lookup"><span data-stu-id="547ef-140">Specifies the vertical dimension of the application media size relative to the PageOrientation.</span></span><br/>                 |
| <span data-ttu-id="547ef-141">\_OriginWidthValue\_</span><span class="sxs-lookup"><span data-stu-id="547ef-141">\_OriginWidthValue\_</span></span><br/>         | <span data-ttu-id="547ef-142">entier</span><span class="sxs-lookup"><span data-stu-id="547ef-142">integer</span></span><br/> | <span data-ttu-id="547ef-143">microns</span><span class="sxs-lookup"><span data-stu-id="547ef-143">microns</span></span><br/> | <span data-ttu-id="547ef-144">Supérieur ou égal à 0.</span><span class="sxs-lookup"><span data-stu-id="547ef-144">Greater than or equal to 0.</span></span><br/> | <span data-ttu-id="547ef-145">Spécifie l’origine horizontale de la zone imageable par rapport à la taille du média d’application.</span><span class="sxs-lookup"><span data-stu-id="547ef-145">Specifies the horizontal origin of the imageable area relative to the application media size.</span></span><br/>                   |
| <span data-ttu-id="547ef-146">\_OriginHeightValue\_</span><span class="sxs-lookup"><span data-stu-id="547ef-146">\_OriginHeightValue\_</span></span><br/>        | <span data-ttu-id="547ef-147">entier</span><span class="sxs-lookup"><span data-stu-id="547ef-147">integer</span></span><br/> | <span data-ttu-id="547ef-148">microns</span><span class="sxs-lookup"><span data-stu-id="547ef-148">microns</span></span><br/> | <span data-ttu-id="547ef-149">Supérieur ou égal à 0.</span><span class="sxs-lookup"><span data-stu-id="547ef-149">Greater than or equal to 0.</span></span><br/> | <span data-ttu-id="547ef-150">Spécifie l’origine verticale de la zone imageable par rapport à la taille du média d’application.</span><span class="sxs-lookup"><span data-stu-id="547ef-150">Specifies the vertical origin of the imageable area relative to the application media size.</span></span><br/>                     |
| <span data-ttu-id="547ef-151">\_ExtentWidthValue\_</span><span class="sxs-lookup"><span data-stu-id="547ef-151">\_ExtentWidthValue\_</span></span><br/>         | <span data-ttu-id="547ef-152">entier</span><span class="sxs-lookup"><span data-stu-id="547ef-152">integer</span></span><br/> | <span data-ttu-id="547ef-153">microns</span><span class="sxs-lookup"><span data-stu-id="547ef-153">microns</span></span><br/> | <span data-ttu-id="547ef-154">Supérieur à 0.</span><span class="sxs-lookup"><span data-stu-id="547ef-154">Greater than 0.</span></span><br/>             | <span data-ttu-id="547ef-155">Spécifie la distance horizontale entre l’origine et la limite limite de la taille du média d’application.</span><span class="sxs-lookup"><span data-stu-id="547ef-155">Specifies the horizontal distance between the origin and the bounding limit of the application media size.</span></span><br/>      |
| <span data-ttu-id="547ef-156">\_ExtentHeightValue\_</span><span class="sxs-lookup"><span data-stu-id="547ef-156">\_ExtentHeightValue\_</span></span><br/>        | <span data-ttu-id="547ef-157">entier</span><span class="sxs-lookup"><span data-stu-id="547ef-157">integer</span></span><br/> | <span data-ttu-id="547ef-158">microns</span><span class="sxs-lookup"><span data-stu-id="547ef-158">microns</span></span><br/> | <span data-ttu-id="547ef-159">Supérieur à 0.</span><span class="sxs-lookup"><span data-stu-id="547ef-159">Greater than 0.</span></span><br/>             | <span data-ttu-id="547ef-160">Spécifie la distance verticale entre l’origine et la limite limite de la taille du média de l’application de canevas.</span><span class="sxs-lookup"><span data-stu-id="547ef-160">Specifies the vertical distance between the origin and the bounding limit of the canvas application media size.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="547ef-161">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="547ef-161">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="547ef-162">Les mots clés de schéma d’impression publics sont définis dans l' https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords espace de noms.</span><span class="sxs-lookup"><span data-stu-id="547ef-162">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="547ef-163">Le contenu de la Extensible Markup Language publique (XML) pour ce mot clé est défini ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="547ef-163">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="547ef-164">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="547ef-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="547ef-165">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="547ef-165">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




