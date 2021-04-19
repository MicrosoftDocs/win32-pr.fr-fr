---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: 88f9a9a3-520e-4044-9ab2-961de03878fa
title: PageResolution
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e0fdd16cf3dc0beb6a418b23d8ee6a93e4a6a61
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "106531771"
---
# <a name="pageresolution"></a><span data-ttu-id="45afa-104">PageResolution</span><span class="sxs-lookup"><span data-stu-id="45afa-104">PageResolution</span></span>

<span data-ttu-id="45afa-105">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="45afa-105">This topic is not current.</span></span> <span data-ttu-id="45afa-106">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="45afa-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="45afa-107">Définit la résolution de la page de sortie d'impression comme valeur qualitative ou comme points par pouce, ou les à la fois.</span><span class="sxs-lookup"><span data-stu-id="45afa-107">Defines the page resolution of printed output as either a qualitative value or as dots per inch, or both.</span></span>

-   [<span data-ttu-id="45afa-108">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="45afa-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="45afa-109">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="45afa-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="45afa-110">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="45afa-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="45afa-111">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="45afa-111">Element Information</span></span>



| <span data-ttu-id="45afa-112">Nom</span><span class="sxs-lookup"><span data-stu-id="45afa-112">Name</span></span>                       |                    |
|----------------------------|--------------------|
| <span data-ttu-id="45afa-113">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="45afa-113">Element Type</span></span> <br/>   | <span data-ttu-id="45afa-114">Fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="45afa-114">Feature</span></span><br/> |
| <span data-ttu-id="45afa-115">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="45afa-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="45afa-116">Page</span><span class="sxs-lookup"><span data-stu-id="45afa-116">Page</span></span><br/>    |
| <span data-ttu-id="45afa-117">Notes</span><span class="sxs-lookup"><span data-stu-id="45afa-117">Notes</span></span> <br/>          | <span data-ttu-id="45afa-118">Aucun</span><span class="sxs-lookup"><span data-stu-id="45afa-118">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="45afa-119">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="45afa-119">Structural Content</span></span>

<span data-ttu-id="45afa-120">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="45afa-120">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageResolution">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option>
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <psf:ScoredProperty name="psk:ResolutionX">
      <psf:Value xsi:type="xs:integer">_ResolutionXValue_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:ResolutionY">
      <psf:Value xsi:type="xs:integer">_ResolutionYValue_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:QualitativeResolution">
      <psf:Value xsi:type="xs:string">_QualitativeResolutionValue_</psf:Value>
    </psf:ScoredProperty> 
  </psf:Option>
</psf:Feature>      
```

## <a name="structure-variables"></a><span data-ttu-id="45afa-121">Variables de structure</span><span class="sxs-lookup"><span data-stu-id="45afa-121">Structure Variables</span></span>

<span data-ttu-id="45afa-122">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="45afa-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="45afa-123">Nom</span><span class="sxs-lookup"><span data-stu-id="45afa-123">Name</span></span>                                      | <span data-ttu-id="45afa-124">Type de données</span><span class="sxs-lookup"><span data-stu-id="45afa-124">Data type</span></span>          | <span data-ttu-id="45afa-125">Unité</span><span class="sxs-lookup"><span data-stu-id="45afa-125">Unit</span></span>                  | <span data-ttu-id="45afa-126">Valeurs prises en charge</span><span class="sxs-lookup"><span data-stu-id="45afa-126">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="45afa-127">Résumé</span><span class="sxs-lookup"><span data-stu-id="45afa-127">Summary</span></span>                                                                                                                                                          |
|-------------------------------------------|--------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="45afa-128">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="45afa-128">\_OptionName\_</span></span><br/>                 | <span data-ttu-id="45afa-129">string</span><span class="sxs-lookup"><span data-stu-id="45afa-129">string</span></span><br/>  | <span data-ttu-id="45afa-130">caractères</span><span class="sxs-lookup"><span data-stu-id="45afa-130">characters</span></span><br/> | <span data-ttu-id="45afa-131">Nom complet valide tel que défini par les [espaces de noms dans XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="45afa-131">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="45afa-132">Si aucun espace de noms n’est spécifié, l’espace de noms par défaut est utilisé.</span><span class="sxs-lookup"><span data-stu-id="45afa-132">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="45afa-133">Nom de l'option.</span><span class="sxs-lookup"><span data-stu-id="45afa-133">The name of the option.</span></span><br/>                                                                                                                               |
| <span data-ttu-id="45afa-134">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="45afa-134">\_IdentityOptionValue\_</span></span><br/>        | <span data-ttu-id="45afa-135">string</span><span class="sxs-lookup"><span data-stu-id="45afa-135">string</span></span><br/>  | <span data-ttu-id="45afa-136">n/a</span><span class="sxs-lookup"><span data-stu-id="45afa-136">n/a</span></span><br/>        | <span data-ttu-id="45afa-137">True, False.</span><span class="sxs-lookup"><span data-stu-id="45afa-137">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="45afa-138">Définit une option qui, lorsqu’elle est sélectionnée, désactive cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="45afa-138">Defines an Option which when selected would disable this feature.</span></span><br/>                                                                                     |
| <span data-ttu-id="45afa-139">\_ResolutionXValue\_</span><span class="sxs-lookup"><span data-stu-id="45afa-139">\_ResolutionXValue\_</span></span><br/>           | <span data-ttu-id="45afa-140">entier</span><span class="sxs-lookup"><span data-stu-id="45afa-140">integer</span></span><br/> | <span data-ttu-id="45afa-141">PPP</span><span class="sxs-lookup"><span data-stu-id="45afa-141">DPI</span></span><br/>        | <span data-ttu-id="45afa-142">Supérieur à 0.</span><span class="sxs-lookup"><span data-stu-id="45afa-142">Greater than 0.</span></span><br/>                                                                                                                                                            | <span data-ttu-id="45afa-143">Spécifie le composant x de la résolution par rapport au PageImageableSize en DPI (par rapport à la direction du PageMediaSize et du flux du média).</span><span class="sxs-lookup"><span data-stu-id="45afa-143">Specifies the x component of the resolution relative to the PageImageableSize in DPI (relative to the PageMediaSize and feed direction of the media).</span></span><br/> |
| <span data-ttu-id="45afa-144">\_ResolutionYValue\_</span><span class="sxs-lookup"><span data-stu-id="45afa-144">\_ResolutionYValue\_</span></span><br/>           | <span data-ttu-id="45afa-145">entier</span><span class="sxs-lookup"><span data-stu-id="45afa-145">integer</span></span><br/> | <span data-ttu-id="45afa-146">PPP</span><span class="sxs-lookup"><span data-stu-id="45afa-146">DPI</span></span><br/>        | <span data-ttu-id="45afa-147">Supérieur à 0.</span><span class="sxs-lookup"><span data-stu-id="45afa-147">Greater than 0.</span></span><br/>                                                                                                                                                            | <span data-ttu-id="45afa-148">Spécifie le composant y de la résolution par rapport au PageImageableSize en DPI (par rapport à la direction du PageMediaSize et du flux du média).</span><span class="sxs-lookup"><span data-stu-id="45afa-148">Specifies the y component of the resolution relative to the PageImageableSize in DPI (relative to the PageMediaSize and feed direction of the media).</span></span><br/> |
| <span data-ttu-id="45afa-149">\_QualitativeResolutionValue\_</span><span class="sxs-lookup"><span data-stu-id="45afa-149">\_QualitativeResolutionValue\_</span></span><br/> | <span data-ttu-id="45afa-150">string</span><span class="sxs-lookup"><span data-stu-id="45afa-150">string</span></span><br/>  | <span data-ttu-id="45afa-151">n/a</span><span class="sxs-lookup"><span data-stu-id="45afa-151">n/a</span></span><br/>        | <span data-ttu-id="45afa-152">Par défaut, brouillon, élevé, normal, autre.</span><span class="sxs-lookup"><span data-stu-id="45afa-152">Default, Draft, High, Normal, Other.</span></span><br/>                                                                                                                                       | <span data-ttu-id="45afa-153">Spécifie une étiquette de qualité pour la résolution.</span><span class="sxs-lookup"><span data-stu-id="45afa-153">Specifies a quality label for the resolution.</span></span><br/>                                                                                                         |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="45afa-154">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="45afa-154">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="45afa-155">Les mots clés de schéma d’impression publics sont définis dans l' https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords espace de noms.</span><span class="sxs-lookup"><span data-stu-id="45afa-155">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="45afa-156">Le contenu de la Extensible Markup Language publique (XML) pour ce mot clé est défini ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="45afa-156">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageResolution">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option>
    <!-- The horizontal resolution in dots per inch -->
    <psf:ScoredProperty name="psk:ResolutionX">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <!-- The vertical resolution in dots per inch -->
    <psf:ScoredProperty name="psk:ResolutionY">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <!-- Value representing the resolution -->
    <psf:ScoredProperty name="psk:QualitativeResolution">
      <psf:Value xsi:type="xs:string">Other</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>    
```

## <a name="related-topics"></a><span data-ttu-id="45afa-157">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="45afa-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="45afa-158">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="45afa-158">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




