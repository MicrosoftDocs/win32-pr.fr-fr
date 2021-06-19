---
description: En savoir plus sur l’élément configurable par l’utilisateur PageImageableSize. Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: 6b81814f-2d9e-4862-8633-6ba016c11dac
title: PageImageableSize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee4e44bc9afe33b87d32b43c93eafc3b6d4ba4b0
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395304"
---
# <a name="pageimageablesize"></a><span data-ttu-id="c7582-105">PageImageableSize</span><span class="sxs-lookup"><span data-stu-id="c7582-105">PageImageableSize</span></span>

<span data-ttu-id="c7582-106">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="c7582-106">This topic is not current.</span></span> <span data-ttu-id="c7582-107">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="c7582-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="c7582-108">Décrit le canevas Imaged pour la disposition et le rendu.</span><span class="sxs-lookup"><span data-stu-id="c7582-108">Describes the imaged canvas for layout and rendering.</span></span> <span data-ttu-id="c7582-109">Ce rapport est basé sur PageMediaSize et PageOrientation.</span><span class="sxs-lookup"><span data-stu-id="c7582-109">This will be reported based on PageMediaSize and PageOrientation.</span></span>

<span data-ttu-id="c7582-110">Les diagrammes suivants illustrent l’utilisation des variables PageImageableSize basée sur PageOrientation.</span><span class="sxs-lookup"><span data-stu-id="c7582-110">The following diagrams illustrate the PageImageableSize variables usage based on PageOrientation.</span></span>

![diagramme qui affiche les mesures des pages](images/local-1641910626-image.png)

-   [<span data-ttu-id="c7582-112">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="c7582-112">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="c7582-113">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="c7582-113">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="c7582-114">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="c7582-114">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="c7582-115">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="c7582-115">Element Information</span></span>

| <span data-ttu-id="c7582-116">Nom</span><span class="sxs-lookup"><span data-stu-id="c7582-116">Name</span></span>                 | <span data-ttu-id="c7582-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="c7582-117">Value</span></span>         |
|----------------------|---------------|
| <span data-ttu-id="c7582-118">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="c7582-118">Element Type</span></span><br/>    | <span data-ttu-id="c7582-119">Propriété</span><span class="sxs-lookup"><span data-stu-id="c7582-119">Property</span></span><br/> |
| <span data-ttu-id="c7582-120">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="c7582-120">Scoping Prefix</span></span> <br/> | <span data-ttu-id="c7582-121">Page</span><span class="sxs-lookup"><span data-stu-id="c7582-121">Page</span></span><br/>     |
| <span data-ttu-id="c7582-122">Notes</span><span class="sxs-lookup"><span data-stu-id="c7582-122">Notes</span></span> <br/>          | <span data-ttu-id="c7582-123">Aucun</span><span class="sxs-lookup"><span data-stu-id="c7582-123">None</span></span><br/>     |

## <a name="structural-content"></a><span data-ttu-id="c7582-124">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="c7582-124">Structural Content</span></span>

<span data-ttu-id="c7582-125">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="c7582-125">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="c7582-126">Variables de structure</span><span class="sxs-lookup"><span data-stu-id="c7582-126">Structure Variables</span></span>

<span data-ttu-id="c7582-127">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="c7582-127">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="c7582-128">Nom</span><span class="sxs-lookup"><span data-stu-id="c7582-128">Name</span></span>                                    | <span data-ttu-id="c7582-129">Type de données</span><span class="sxs-lookup"><span data-stu-id="c7582-129">Data type</span></span>          | <span data-ttu-id="c7582-130">Unité</span><span class="sxs-lookup"><span data-stu-id="c7582-130">Unit</span></span>               | <span data-ttu-id="c7582-131">Valeurs prises en charge</span><span class="sxs-lookup"><span data-stu-id="c7582-131">Supported values</span></span>                       | <span data-ttu-id="c7582-132">Résumé</span><span class="sxs-lookup"><span data-stu-id="c7582-132">Summary</span></span>                                                                                                                    |
|-----------------------------------------|--------------------|--------------------|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7582-133">\_ImageableSizeWidthValue\_</span><span class="sxs-lookup"><span data-stu-id="c7582-133">\_ImageableSizeWidthValue\_</span></span><br/>  | <span data-ttu-id="c7582-134">entier</span><span class="sxs-lookup"><span data-stu-id="c7582-134">integer</span></span><br/> | <span data-ttu-id="c7582-135">microns</span><span class="sxs-lookup"><span data-stu-id="c7582-135">microns</span></span><br/> | <span data-ttu-id="c7582-136">Supérieur à 0.</span><span class="sxs-lookup"><span data-stu-id="c7582-136">Greater than 0.</span></span><br/>             | <span data-ttu-id="c7582-137">Spécifie la dimension horizontale de la taille du média d’application par rapport au PageOrientation.</span><span class="sxs-lookup"><span data-stu-id="c7582-137">Specifies the horizontal dimension of the application media size relative to the PageOrientation.</span></span><br/>               |
| <span data-ttu-id="c7582-138">\_ImageableSizeHeightValue\_</span><span class="sxs-lookup"><span data-stu-id="c7582-138">\_ImageableSizeHeightValue\_</span></span><br/> | <span data-ttu-id="c7582-139">entier</span><span class="sxs-lookup"><span data-stu-id="c7582-139">integer</span></span><br/> | <span data-ttu-id="c7582-140">microns</span><span class="sxs-lookup"><span data-stu-id="c7582-140">microns</span></span><br/> | <span data-ttu-id="c7582-141">Supérieur à 0.</span><span class="sxs-lookup"><span data-stu-id="c7582-141">Greater than 0.</span></span><br/>             | <span data-ttu-id="c7582-142">Spécifie la dimension verticale de la taille du média d’application par rapport au PageOrientation.</span><span class="sxs-lookup"><span data-stu-id="c7582-142">Specifies the vertical dimension of the application media size relative to the PageOrientation.</span></span><br/>                 |
| <span data-ttu-id="c7582-143">\_OriginWidthValue\_</span><span class="sxs-lookup"><span data-stu-id="c7582-143">\_OriginWidthValue\_</span></span><br/>         | <span data-ttu-id="c7582-144">entier</span><span class="sxs-lookup"><span data-stu-id="c7582-144">integer</span></span><br/> | <span data-ttu-id="c7582-145">microns</span><span class="sxs-lookup"><span data-stu-id="c7582-145">microns</span></span><br/> | <span data-ttu-id="c7582-146">Supérieur ou égal à 0.</span><span class="sxs-lookup"><span data-stu-id="c7582-146">Greater than or equal to 0.</span></span><br/> | <span data-ttu-id="c7582-147">Spécifie l’origine horizontale de la zone imageable par rapport à la taille du média d’application.</span><span class="sxs-lookup"><span data-stu-id="c7582-147">Specifies the horizontal origin of the imageable area relative to the application media size.</span></span><br/>                   |
| <span data-ttu-id="c7582-148">\_OriginHeightValue\_</span><span class="sxs-lookup"><span data-stu-id="c7582-148">\_OriginHeightValue\_</span></span><br/>        | <span data-ttu-id="c7582-149">entier</span><span class="sxs-lookup"><span data-stu-id="c7582-149">integer</span></span><br/> | <span data-ttu-id="c7582-150">microns</span><span class="sxs-lookup"><span data-stu-id="c7582-150">microns</span></span><br/> | <span data-ttu-id="c7582-151">Supérieur ou égal à 0.</span><span class="sxs-lookup"><span data-stu-id="c7582-151">Greater than or equal to 0.</span></span><br/> | <span data-ttu-id="c7582-152">Spécifie l’origine verticale de la zone imageable par rapport à la taille du média d’application.</span><span class="sxs-lookup"><span data-stu-id="c7582-152">Specifies the vertical origin of the imageable area relative to the application media size.</span></span><br/>                     |
| <span data-ttu-id="c7582-153">\_ExtentWidthValue\_</span><span class="sxs-lookup"><span data-stu-id="c7582-153">\_ExtentWidthValue\_</span></span><br/>         | <span data-ttu-id="c7582-154">entier</span><span class="sxs-lookup"><span data-stu-id="c7582-154">integer</span></span><br/> | <span data-ttu-id="c7582-155">microns</span><span class="sxs-lookup"><span data-stu-id="c7582-155">microns</span></span><br/> | <span data-ttu-id="c7582-156">Supérieur à 0.</span><span class="sxs-lookup"><span data-stu-id="c7582-156">Greater than 0.</span></span><br/>             | <span data-ttu-id="c7582-157">Spécifie la distance horizontale entre l’origine et la limite limite de la taille du média d’application.</span><span class="sxs-lookup"><span data-stu-id="c7582-157">Specifies the horizontal distance between the origin and the bounding limit of the application media size.</span></span><br/>      |
| <span data-ttu-id="c7582-158">\_ExtentHeightValue\_</span><span class="sxs-lookup"><span data-stu-id="c7582-158">\_ExtentHeightValue\_</span></span><br/>        | <span data-ttu-id="c7582-159">entier</span><span class="sxs-lookup"><span data-stu-id="c7582-159">integer</span></span><br/> | <span data-ttu-id="c7582-160">microns</span><span class="sxs-lookup"><span data-stu-id="c7582-160">microns</span></span><br/> | <span data-ttu-id="c7582-161">Supérieur à 0.</span><span class="sxs-lookup"><span data-stu-id="c7582-161">Greater than 0.</span></span><br/>             | <span data-ttu-id="c7582-162">Spécifie la distance verticale entre l’origine et la limite limite de la taille du média de l’application de canevas.</span><span class="sxs-lookup"><span data-stu-id="c7582-162">Specifies the vertical distance between the origin and the bounding limit of the canvas application media size.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="c7582-163">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="c7582-163">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="c7582-164">Les mots clés de schéma d’impression publics sont définis dans l' https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords espace de noms.</span><span class="sxs-lookup"><span data-stu-id="c7582-164">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="c7582-165">Le contenu de la Extensible Markup Language publique (XML) pour ce mot clé est défini ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="c7582-165">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="c7582-166">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c7582-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c7582-167">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="c7582-167">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




