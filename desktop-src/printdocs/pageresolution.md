---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: 88f9a9a3-520e-4044-9ab2-961de03878fa
title: PageResolution
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e44a7ff73c03929d3dfc8bc9f7c31c878ad039c
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107993716"
---
# <a name="pageresolution"></a><span data-ttu-id="0376c-104">PageResolution</span><span class="sxs-lookup"><span data-stu-id="0376c-104">PageResolution</span></span>

<span data-ttu-id="0376c-105">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="0376c-105">This topic is not current.</span></span> <span data-ttu-id="0376c-106">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="0376c-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="0376c-107">Définit la résolution de la page de sortie d'impression comme valeur qualitative ou comme points par pouce, ou les à la fois.</span><span class="sxs-lookup"><span data-stu-id="0376c-107">Defines the page resolution of printed output as either a qualitative value or as dots per inch, or both.</span></span>

-   [<span data-ttu-id="0376c-108">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="0376c-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="0376c-109">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="0376c-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="0376c-110">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="0376c-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="0376c-111">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="0376c-111">Element Information</span></span>



| <span data-ttu-id="0376c-112">Nom</span><span class="sxs-lookup"><span data-stu-id="0376c-112">Name</span></span> | <span data-ttu-id="0376c-113">Value</span><span class="sxs-lookup"><span data-stu-id="0376c-113">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="0376c-114">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="0376c-114">Element Type</span></span> <br/>   | <span data-ttu-id="0376c-115">Fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="0376c-115">Feature</span></span><br/> |
| <span data-ttu-id="0376c-116">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="0376c-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="0376c-117">Page</span><span class="sxs-lookup"><span data-stu-id="0376c-117">Page</span></span><br/>    |
| <span data-ttu-id="0376c-118">Notes</span><span class="sxs-lookup"><span data-stu-id="0376c-118">Notes</span></span> <br/>          | <span data-ttu-id="0376c-119">Aucun</span><span class="sxs-lookup"><span data-stu-id="0376c-119">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="0376c-120">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="0376c-120">Structural Content</span></span>

<span data-ttu-id="0376c-121">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="0376c-121">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="0376c-122">Variables de structure</span><span class="sxs-lookup"><span data-stu-id="0376c-122">Structure Variables</span></span>

<span data-ttu-id="0376c-123">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="0376c-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="0376c-124">Nom</span><span class="sxs-lookup"><span data-stu-id="0376c-124">Name</span></span>                                      | <span data-ttu-id="0376c-125">Type de données</span><span class="sxs-lookup"><span data-stu-id="0376c-125">Data type</span></span>          | <span data-ttu-id="0376c-126">Unité</span><span class="sxs-lookup"><span data-stu-id="0376c-126">Unit</span></span>                  | <span data-ttu-id="0376c-127">Valeurs prises en charge</span><span class="sxs-lookup"><span data-stu-id="0376c-127">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="0376c-128">Résumé</span><span class="sxs-lookup"><span data-stu-id="0376c-128">Summary</span></span>                                                                                                                                                          |
|-------------------------------------------|--------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0376c-129">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="0376c-129">\_OptionName\_</span></span><br/>                 | <span data-ttu-id="0376c-130">string</span><span class="sxs-lookup"><span data-stu-id="0376c-130">string</span></span><br/>  | <span data-ttu-id="0376c-131">caractères</span><span class="sxs-lookup"><span data-stu-id="0376c-131">characters</span></span><br/> | <span data-ttu-id="0376c-132">Nom complet valide tel que défini par les [espaces de noms dans XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="0376c-132">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="0376c-133">Si aucun espace de noms n’est spécifié, l’espace de noms par défaut est utilisé.</span><span class="sxs-lookup"><span data-stu-id="0376c-133">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="0376c-134">Nom de l'option.</span><span class="sxs-lookup"><span data-stu-id="0376c-134">The name of the option.</span></span><br/>                                                                                                                               |
| <span data-ttu-id="0376c-135">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="0376c-135">\_IdentityOptionValue\_</span></span><br/>        | <span data-ttu-id="0376c-136">string</span><span class="sxs-lookup"><span data-stu-id="0376c-136">string</span></span><br/>  | <span data-ttu-id="0376c-137">n/a</span><span class="sxs-lookup"><span data-stu-id="0376c-137">n/a</span></span><br/>        | <span data-ttu-id="0376c-138">True, False.</span><span class="sxs-lookup"><span data-stu-id="0376c-138">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="0376c-139">Définit une option qui, lorsqu’elle est sélectionnée, désactive cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="0376c-139">Defines an Option which when selected would disable this feature.</span></span><br/>                                                                                     |
| <span data-ttu-id="0376c-140">\_ResolutionXValue\_</span><span class="sxs-lookup"><span data-stu-id="0376c-140">\_ResolutionXValue\_</span></span><br/>           | <span data-ttu-id="0376c-141">entier</span><span class="sxs-lookup"><span data-stu-id="0376c-141">integer</span></span><br/> | <span data-ttu-id="0376c-142">PPP</span><span class="sxs-lookup"><span data-stu-id="0376c-142">DPI</span></span><br/>        | <span data-ttu-id="0376c-143">Supérieur à 0.</span><span class="sxs-lookup"><span data-stu-id="0376c-143">Greater than 0.</span></span><br/>                                                                                                                                                            | <span data-ttu-id="0376c-144">Spécifie le composant x de la résolution par rapport au PageImageableSize en DPI (par rapport à la direction du PageMediaSize et du flux du média).</span><span class="sxs-lookup"><span data-stu-id="0376c-144">Specifies the x component of the resolution relative to the PageImageableSize in DPI (relative to the PageMediaSize and feed direction of the media).</span></span><br/> |
| <span data-ttu-id="0376c-145">\_ResolutionYValue\_</span><span class="sxs-lookup"><span data-stu-id="0376c-145">\_ResolutionYValue\_</span></span><br/>           | <span data-ttu-id="0376c-146">entier</span><span class="sxs-lookup"><span data-stu-id="0376c-146">integer</span></span><br/> | <span data-ttu-id="0376c-147">PPP</span><span class="sxs-lookup"><span data-stu-id="0376c-147">DPI</span></span><br/>        | <span data-ttu-id="0376c-148">Supérieur à 0.</span><span class="sxs-lookup"><span data-stu-id="0376c-148">Greater than 0.</span></span><br/>                                                                                                                                                            | <span data-ttu-id="0376c-149">Spécifie le composant y de la résolution par rapport au PageImageableSize en DPI (par rapport à la direction du PageMediaSize et du flux du média).</span><span class="sxs-lookup"><span data-stu-id="0376c-149">Specifies the y component of the resolution relative to the PageImageableSize in DPI (relative to the PageMediaSize and feed direction of the media).</span></span><br/> |
| <span data-ttu-id="0376c-150">\_QualitativeResolutionValue\_</span><span class="sxs-lookup"><span data-stu-id="0376c-150">\_QualitativeResolutionValue\_</span></span><br/> | <span data-ttu-id="0376c-151">string</span><span class="sxs-lookup"><span data-stu-id="0376c-151">string</span></span><br/>  | <span data-ttu-id="0376c-152">n/a</span><span class="sxs-lookup"><span data-stu-id="0376c-152">n/a</span></span><br/>        | <span data-ttu-id="0376c-153">Par défaut, brouillon, élevé, normal, autre.</span><span class="sxs-lookup"><span data-stu-id="0376c-153">Default, Draft, High, Normal, Other.</span></span><br/>                                                                                                                                       | <span data-ttu-id="0376c-154">Spécifie une étiquette de qualité pour la résolution.</span><span class="sxs-lookup"><span data-stu-id="0376c-154">Specifies a quality label for the resolution.</span></span><br/>                                                                                                         |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="0376c-155">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="0376c-155">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="0376c-156">Les mots clés de schéma d’impression publics sont définis dans l' https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords espace de noms.</span><span class="sxs-lookup"><span data-stu-id="0376c-156">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="0376c-157">Le contenu de la Extensible Markup Language publique (XML) pour ce mot clé est défini ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="0376c-157">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="0376c-158">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0376c-158">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0376c-159">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="0376c-159">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




