---
description: En savoir plus sur l’élément configurable par l’utilisateur PageResolution. Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: 88f9a9a3-520e-4044-9ab2-961de03878fa
title: PageResolution
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 760384ff900e7b35e37105fdb19e3635a434aa5a
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112394817"
---
# <a name="pageresolution"></a><span data-ttu-id="a0d87-105">PageResolution</span><span class="sxs-lookup"><span data-stu-id="a0d87-105">PageResolution</span></span>

<span data-ttu-id="a0d87-106">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="a0d87-106">This topic is not current.</span></span> <span data-ttu-id="a0d87-107">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="a0d87-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="a0d87-108">Définit la résolution de la page de sortie d'impression comme valeur qualitative ou comme points par pouce, ou les à la fois.</span><span class="sxs-lookup"><span data-stu-id="a0d87-108">Defines the page resolution of printed output as either a qualitative value or as dots per inch, or both.</span></span>

-   [<span data-ttu-id="a0d87-109">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="a0d87-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="a0d87-110">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="a0d87-110">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="a0d87-111">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="a0d87-111">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="a0d87-112">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="a0d87-112">Element Information</span></span>



| <span data-ttu-id="a0d87-113">Nom</span><span class="sxs-lookup"><span data-stu-id="a0d87-113">Name</span></span> | <span data-ttu-id="a0d87-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="a0d87-114">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="a0d87-115">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="a0d87-115">Element Type</span></span> <br/>   | <span data-ttu-id="a0d87-116">Fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="a0d87-116">Feature</span></span><br/> |
| <span data-ttu-id="a0d87-117">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="a0d87-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="a0d87-118">Page</span><span class="sxs-lookup"><span data-stu-id="a0d87-118">Page</span></span><br/>    |
| <span data-ttu-id="a0d87-119">Notes</span><span class="sxs-lookup"><span data-stu-id="a0d87-119">Notes</span></span> <br/>          | <span data-ttu-id="a0d87-120">Aucun</span><span class="sxs-lookup"><span data-stu-id="a0d87-120">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="a0d87-121">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="a0d87-121">Structural Content</span></span>

<span data-ttu-id="a0d87-122">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="a0d87-122">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="a0d87-123">Variables de structure</span><span class="sxs-lookup"><span data-stu-id="a0d87-123">Structure Variables</span></span>

<span data-ttu-id="a0d87-124">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="a0d87-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="a0d87-125">Nom</span><span class="sxs-lookup"><span data-stu-id="a0d87-125">Name</span></span>                                      | <span data-ttu-id="a0d87-126">Type de données</span><span class="sxs-lookup"><span data-stu-id="a0d87-126">Data type</span></span>          | <span data-ttu-id="a0d87-127">Unité</span><span class="sxs-lookup"><span data-stu-id="a0d87-127">Unit</span></span>                  | <span data-ttu-id="a0d87-128">Valeurs prises en charge</span><span class="sxs-lookup"><span data-stu-id="a0d87-128">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="a0d87-129">Résumé</span><span class="sxs-lookup"><span data-stu-id="a0d87-129">Summary</span></span>                                                                                                                                                          |
|-------------------------------------------|--------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0d87-130">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="a0d87-130">\_OptionName\_</span></span><br/>                 | <span data-ttu-id="a0d87-131">string</span><span class="sxs-lookup"><span data-stu-id="a0d87-131">string</span></span><br/>  | <span data-ttu-id="a0d87-132">caractères</span><span class="sxs-lookup"><span data-stu-id="a0d87-132">characters</span></span><br/> | <span data-ttu-id="a0d87-133">Nom complet valide tel que défini par les [espaces de noms dans XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="a0d87-133">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="a0d87-134">Si aucun espace de noms n’est spécifié, l’espace de noms par défaut est utilisé.</span><span class="sxs-lookup"><span data-stu-id="a0d87-134">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="a0d87-135">Nom de l'option.</span><span class="sxs-lookup"><span data-stu-id="a0d87-135">The name of the option.</span></span><br/>                                                                                                                               |
| <span data-ttu-id="a0d87-136">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="a0d87-136">\_IdentityOptionValue\_</span></span><br/>        | <span data-ttu-id="a0d87-137">string</span><span class="sxs-lookup"><span data-stu-id="a0d87-137">string</span></span><br/>  | <span data-ttu-id="a0d87-138">n/a</span><span class="sxs-lookup"><span data-stu-id="a0d87-138">n/a</span></span><br/>        | <span data-ttu-id="a0d87-139">True, False.</span><span class="sxs-lookup"><span data-stu-id="a0d87-139">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="a0d87-140">Définit une option qui, lorsqu’elle est sélectionnée, désactive cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="a0d87-140">Defines an Option which when selected would disable this feature.</span></span><br/>                                                                                     |
| <span data-ttu-id="a0d87-141">\_ResolutionXValue\_</span><span class="sxs-lookup"><span data-stu-id="a0d87-141">\_ResolutionXValue\_</span></span><br/>           | <span data-ttu-id="a0d87-142">entier</span><span class="sxs-lookup"><span data-stu-id="a0d87-142">integer</span></span><br/> | <span data-ttu-id="a0d87-143">PPP</span><span class="sxs-lookup"><span data-stu-id="a0d87-143">DPI</span></span><br/>        | <span data-ttu-id="a0d87-144">Supérieur à 0.</span><span class="sxs-lookup"><span data-stu-id="a0d87-144">Greater than 0.</span></span><br/>                                                                                                                                                            | <span data-ttu-id="a0d87-145">Spécifie le composant x de la résolution par rapport au PageImageableSize en DPI (par rapport à la direction du PageMediaSize et du flux du média).</span><span class="sxs-lookup"><span data-stu-id="a0d87-145">Specifies the x component of the resolution relative to the PageImageableSize in DPI (relative to the PageMediaSize and feed direction of the media).</span></span><br/> |
| <span data-ttu-id="a0d87-146">\_ResolutionYValue\_</span><span class="sxs-lookup"><span data-stu-id="a0d87-146">\_ResolutionYValue\_</span></span><br/>           | <span data-ttu-id="a0d87-147">entier</span><span class="sxs-lookup"><span data-stu-id="a0d87-147">integer</span></span><br/> | <span data-ttu-id="a0d87-148">PPP</span><span class="sxs-lookup"><span data-stu-id="a0d87-148">DPI</span></span><br/>        | <span data-ttu-id="a0d87-149">Supérieur à 0.</span><span class="sxs-lookup"><span data-stu-id="a0d87-149">Greater than 0.</span></span><br/>                                                                                                                                                            | <span data-ttu-id="a0d87-150">Spécifie le composant y de la résolution par rapport au PageImageableSize en DPI (par rapport à la direction du PageMediaSize et du flux du média).</span><span class="sxs-lookup"><span data-stu-id="a0d87-150">Specifies the y component of the resolution relative to the PageImageableSize in DPI (relative to the PageMediaSize and feed direction of the media).</span></span><br/> |
| <span data-ttu-id="a0d87-151">\_QualitativeResolutionValue\_</span><span class="sxs-lookup"><span data-stu-id="a0d87-151">\_QualitativeResolutionValue\_</span></span><br/> | <span data-ttu-id="a0d87-152">string</span><span class="sxs-lookup"><span data-stu-id="a0d87-152">string</span></span><br/>  | <span data-ttu-id="a0d87-153">n/a</span><span class="sxs-lookup"><span data-stu-id="a0d87-153">n/a</span></span><br/>        | <span data-ttu-id="a0d87-154">Par défaut, brouillon, élevé, normal, autre.</span><span class="sxs-lookup"><span data-stu-id="a0d87-154">Default, Draft, High, Normal, Other.</span></span><br/>                                                                                                                                       | <span data-ttu-id="a0d87-155">Spécifie une étiquette de qualité pour la résolution.</span><span class="sxs-lookup"><span data-stu-id="a0d87-155">Specifies a quality label for the resolution.</span></span><br/>                                                                                                         |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="a0d87-156">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="a0d87-156">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="a0d87-157">Les mots clés de schéma d’impression publics sont définis dans l' https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords espace de noms.</span><span class="sxs-lookup"><span data-stu-id="a0d87-157">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="a0d87-158">Le contenu de la Extensible Markup Language publique (XML) pour ce mot clé est défini ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="a0d87-158">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="a0d87-159">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a0d87-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a0d87-160">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="a0d87-160">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




