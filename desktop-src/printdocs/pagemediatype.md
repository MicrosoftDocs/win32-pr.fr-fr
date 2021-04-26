---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: 29d7ae65-9dd3-4a29-8e5e-79708638a3bb
title: PageMediaType
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3d41ed2af931068e340e9a9d0828db109594de8
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994516"
---
# <a name="pagemediatype"></a><span data-ttu-id="419d5-104">PageMediaType</span><span class="sxs-lookup"><span data-stu-id="419d5-104">PageMediaType</span></span>

<span data-ttu-id="419d5-105">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="419d5-105">This topic is not current.</span></span> <span data-ttu-id="419d5-106">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="419d5-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="419d5-107">Décrit les options de MediaType et les caractéristiques de chaque option.</span><span class="sxs-lookup"><span data-stu-id="419d5-107">Describes the MediaType options and the characteristics of each option.</span></span>

-   [<span data-ttu-id="419d5-108">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="419d5-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="419d5-109">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="419d5-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="419d5-110">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="419d5-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="419d5-111">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="419d5-111">Element Information</span></span>



| <span data-ttu-id="419d5-112">Nom</span><span class="sxs-lookup"><span data-stu-id="419d5-112">Name</span></span> | <span data-ttu-id="419d5-113">Value</span><span class="sxs-lookup"><span data-stu-id="419d5-113">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="419d5-114">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="419d5-114">Element Type</span></span> <br/>   | <span data-ttu-id="419d5-115">Fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="419d5-115">Feature</span></span><br/> |
| <span data-ttu-id="419d5-116">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="419d5-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="419d5-117">Page</span><span class="sxs-lookup"><span data-stu-id="419d5-117">Page</span></span><br/>    |
| <span data-ttu-id="419d5-118">Notes</span><span class="sxs-lookup"><span data-stu-id="419d5-118">Notes</span></span> <br/>          | <span data-ttu-id="419d5-119">Aucun</span><span class="sxs-lookup"><span data-stu-id="419d5-119">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="419d5-120">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="419d5-120">Structural Content</span></span>

<span data-ttu-id="419d5-121">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="419d5-121">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageMediaType">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <psf:ScoredProperty name="psk:BackCoating">
      <psf:Value xsi:type="xs:string">_BackCoatingValue_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FrontCoating">
      <psf:Value xsi:type="xs:string">_FrontCoatingValue_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Material">
      <psf:Value xsi:type="xs:string">_MaterialValue_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePrinted">
      <psf:Value xsi:type="xs:string">_PrePrintedValue_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePunched">
      <psf:Value xsi:type="xs:string">_PrePunchedValue_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Recycled">
      <psf:Value xsi:type="xs:string">_RecycledValue_</psf:Value>
    </psf:ScoredProperty>     
    <psf:ScoredProperty name="psk:Weight">
      <psf:Value xsi:type="xs:integer">_WeightValue_</psf:Value>
    </psf:ScoredProperty> 
  </psf:Option>
</psf:Feature>
      
```

## <a name="structure-variables"></a><span data-ttu-id="419d5-122">Variables de structure</span><span class="sxs-lookup"><span data-stu-id="419d5-122">Structure Variables</span></span>

<span data-ttu-id="419d5-123">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="419d5-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="419d5-124">Nom</span><span class="sxs-lookup"><span data-stu-id="419d5-124">Name</span></span>                               | <span data-ttu-id="419d5-125">Type de données</span><span class="sxs-lookup"><span data-stu-id="419d5-125">Data type</span></span>          | <span data-ttu-id="419d5-126">Unité</span><span class="sxs-lookup"><span data-stu-id="419d5-126">Unit</span></span>                              | <span data-ttu-id="419d5-127">Valeurs prises en charge</span><span class="sxs-lookup"><span data-stu-id="419d5-127">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="419d5-128">Résumé</span><span class="sxs-lookup"><span data-stu-id="419d5-128">Summary</span></span>                                                                      |
|------------------------------------|--------------------|-----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="419d5-129">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="419d5-129">\_OptionName\_</span></span><br/>          | <span data-ttu-id="419d5-130">string</span><span class="sxs-lookup"><span data-stu-id="419d5-130">string</span></span><br/>  | <span data-ttu-id="419d5-131">caractères</span><span class="sxs-lookup"><span data-stu-id="419d5-131">characters</span></span><br/>             | <span data-ttu-id="419d5-132">Nom complet valide tel que défini par les [espaces de noms dans XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="419d5-132">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="419d5-133">Si aucun espace de noms n’est spécifié, l’espace de noms par défaut est utilisé.</span><span class="sxs-lookup"><span data-stu-id="419d5-133">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="419d5-134">Nom de l'option.</span><span class="sxs-lookup"><span data-stu-id="419d5-134">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="419d5-135">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="419d5-135">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="419d5-136">string</span><span class="sxs-lookup"><span data-stu-id="419d5-136">string</span></span><br/>  | <span data-ttu-id="419d5-137">n/a</span><span class="sxs-lookup"><span data-stu-id="419d5-137">n/a</span></span><br/>                    | <span data-ttu-id="419d5-138">True, False.</span><span class="sxs-lookup"><span data-stu-id="419d5-138">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="419d5-139">Définit une option qui, lorsqu’elle est sélectionnée, désactive cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="419d5-139">Defines an Option which when selected would disable this feature.</span></span><br/> |
| <span data-ttu-id="419d5-140">\_BackCoatingValue\_</span><span class="sxs-lookup"><span data-stu-id="419d5-140">\_BackCoatingValue\_</span></span><br/>    | <span data-ttu-id="419d5-141">string</span><span class="sxs-lookup"><span data-stu-id="419d5-141">string</span></span><br/>  | <span data-ttu-id="419d5-142">n/a</span><span class="sxs-lookup"><span data-stu-id="419d5-142">n/a</span></span><br/>                    | <span data-ttu-id="419d5-143">Brillant, HighGloss, mat, aucun, satin, SemiGloss.</span><span class="sxs-lookup"><span data-stu-id="419d5-143">Glossy, HighGloss, Matte, None, Satin, SemiGloss.</span></span><br/>                                                                                                                          | <span data-ttu-id="419d5-144">Spécifie le revêtement du côté arrière du média.</span><span class="sxs-lookup"><span data-stu-id="419d5-144">Specifies the coating of the back side of the media.</span></span><br/>              |
| <span data-ttu-id="419d5-145">\_FrontCoatingValue\_</span><span class="sxs-lookup"><span data-stu-id="419d5-145">\_FrontCoatingValue\_</span></span><br/>   | <span data-ttu-id="419d5-146">string</span><span class="sxs-lookup"><span data-stu-id="419d5-146">string</span></span><br/>  | <span data-ttu-id="419d5-147">n/a</span><span class="sxs-lookup"><span data-stu-id="419d5-147">n/a</span></span><br/>                    | <span data-ttu-id="419d5-148">Brillant, HighGloss, mat, aucun, satin, SemiGloss.</span><span class="sxs-lookup"><span data-stu-id="419d5-148">Glossy, HighGloss, Matte, None, Satin, SemiGloss.</span></span><br/>                                                                                                                          | <span data-ttu-id="419d5-149">Spécifie le revêtement du côté frontal du média.</span><span class="sxs-lookup"><span data-stu-id="419d5-149">Specifies the coating of the front side of the media.</span></span><br/>             |
| <span data-ttu-id="419d5-150">\_MaterialValue\_</span><span class="sxs-lookup"><span data-stu-id="419d5-150">\_MaterialValue\_</span></span><br/>       | <span data-ttu-id="419d5-151">string</span><span class="sxs-lookup"><span data-stu-id="419d5-151">string</span></span><br/>  | <span data-ttu-id="419d5-152">n/a</span><span class="sxs-lookup"><span data-stu-id="419d5-152">n/a</span></span><br/>                    | <span data-ttu-id="419d5-153">Aluminium, affichage, DryFilm, papier, polyester, transparence, WetFilm.</span><span class="sxs-lookup"><span data-stu-id="419d5-153">Aluminum, Display, DryFilm, Paper, Polyester, Transparency, WetFilm.</span></span><br/>                                                                                                       | <span data-ttu-id="419d5-154">Spécifie le matériau à partir duquel le média est établi.</span><span class="sxs-lookup"><span data-stu-id="419d5-154">Specifies the material the media is made out of.</span></span><br/>                  |
| <span data-ttu-id="419d5-155">\_PrePrintedValue\_</span><span class="sxs-lookup"><span data-stu-id="419d5-155">\_PrePrintedValue\_</span></span><br/>     | <span data-ttu-id="419d5-156">string</span><span class="sxs-lookup"><span data-stu-id="419d5-156">string</span></span><br/>  | <span data-ttu-id="419d5-157">n/a</span><span class="sxs-lookup"><span data-stu-id="419d5-157">n/a</span></span><br/>                    | <span data-ttu-id="419d5-158">Aucun, préimprimé, en-tête.</span><span class="sxs-lookup"><span data-stu-id="419d5-158">None, PrePrinted, Letterhead.</span></span><br/>                                                                                                                                              | <span data-ttu-id="419d5-159">Spécifie les caractéristiques préimprimées des médias.</span><span class="sxs-lookup"><span data-stu-id="419d5-159">Specifies media preprinted characteristics.</span></span><br/>                       |
| <span data-ttu-id="419d5-160">\_PrePunchedValue\_</span><span class="sxs-lookup"><span data-stu-id="419d5-160">\_PrePunchedValue\_</span></span><br/>     | <span data-ttu-id="419d5-161">string</span><span class="sxs-lookup"><span data-stu-id="419d5-161">string</span></span><br/>  | <span data-ttu-id="419d5-162">n/a</span><span class="sxs-lookup"><span data-stu-id="419d5-162">n/a</span></span><br/>                    | <span data-ttu-id="419d5-163">Aucun, préperforé.</span><span class="sxs-lookup"><span data-stu-id="419d5-163">None, PrePunched.</span></span><br/>                                                                                                                                                          | <span data-ttu-id="419d5-164">Spécifie les caractéristiques des médias préperforés.</span><span class="sxs-lookup"><span data-stu-id="419d5-164">Specifies media prepunched characteristics.</span></span><br/>                       |
| <span data-ttu-id="419d5-165">\_RecycledValue\_</span><span class="sxs-lookup"><span data-stu-id="419d5-165">\_RecycledValue\_</span></span><br/>       | <span data-ttu-id="419d5-166">string</span><span class="sxs-lookup"><span data-stu-id="419d5-166">string</span></span><br/>  | <span data-ttu-id="419d5-167">n/a</span><span class="sxs-lookup"><span data-stu-id="419d5-167">n/a</span></span><br/>                    | <span data-ttu-id="419d5-168">Aucun, standard.</span><span class="sxs-lookup"><span data-stu-id="419d5-168">None, Standard.</span></span><br/>                                                                                                                                                            | <span data-ttu-id="419d5-169">Spécifie les caractéristiques du support recyclé.</span><span class="sxs-lookup"><span data-stu-id="419d5-169">Specifies media recycled characteristics.</span></span><br/>                         |
| <span data-ttu-id="419d5-170">\_WeightValue\_</span><span class="sxs-lookup"><span data-stu-id="419d5-170">\_WeightValue\_</span></span><br/>         | <span data-ttu-id="419d5-171">entier</span><span class="sxs-lookup"><span data-stu-id="419d5-171">integer</span></span><br/> | <span data-ttu-id="419d5-172">grammes par mètre carré</span><span class="sxs-lookup"><span data-stu-id="419d5-172">grams per square meter</span></span><br/> | <span data-ttu-id="419d5-173">Supérieur à 0.</span><span class="sxs-lookup"><span data-stu-id="419d5-173">Greater than 0.</span></span><br/>                                                                                                                                                            | <span data-ttu-id="419d5-174">Spécifie les caractéristiques de poids du média.</span><span class="sxs-lookup"><span data-stu-id="419d5-174">Specifies media weight characteristics.</span></span><br/>                           |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="419d5-175">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="419d5-175">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="419d5-176">Les mots clés de schéma d’impression publics sont définis dans l' `https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords` espace de noms.</span><span class="sxs-lookup"><span data-stu-id="419d5-176">The public Print Schema keywords are defined in the `https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords` namespace.</span></span> <span data-ttu-id="419d5-177">Le contenu de la Extensible Markup Language publique (XML) pour ce mot clé est défini ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="419d5-177">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageMediaType">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies Media would be Automatically selected. -->
  <psf:Option name="psk:AutoSelect"/>
  <!-- Specifies archival quality media. -->
  <psf:Option name="psk:Archival">
    <psf:ScoredProperty name="psk:BackCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FrontCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Material">
      <psf:Value xsi:type="xs:string">Paper</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePrinted">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePunched">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Recycled">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Weight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies specialty back printing film media. -->
  <psf:Option name="psk:BackPrintFilm">
    <psf:ScoredProperty name="psk:BackCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FrontCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Material">
      <psf:Value xsi:type="xs:string">DryFilm</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePrinted">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePunched">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Recycled">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Weight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies standard bond media. -->
  <psf:Option name="psk:Bond">
    <psf:ScoredProperty name="psk:BackCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FrontCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Material">
      <psf:Value xsi:type="xs:string">Paper</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePrinted">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePunched">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Recycled">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Weight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies standard card stock media. -->
  <psf:Option name="psk:CardStock">
    <psf:ScoredProperty name="psk:BackCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FrontCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Material">
      <psf:Value xsi:type="xs:string">Paper</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePrinted">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePunched">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Recycled">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Weight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies continuous feed media. -->
  <psf:Option name="psk:Continous">
    <psf:ScoredProperty name="psk:BackCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FrontCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Material">
      <psf:Value xsi:type="xs:string">Paper</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePrinted">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePunched">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Recycled">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Weight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies standard envelope media. -->
  <psf:Option name="psk:EnvelopePlain">
    <psf:ScoredProperty name="psk:BackCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FrontCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Material">
      <psf:Value xsi:type="xs:string">Paper</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePrinted">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePunched">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Recycled">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Weight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies windowed envelope media. -->
  <psf:Option name="psk:EnvelopeWindow">
    <psf:ScoredProperty name="psk:BackCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FrontCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Material">
      <psf:Value xsi:type="xs:string">Paper</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePrinted">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePunched">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Recycled">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Weight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies fabric media. -->
  <psf:Option name="psk:Fabric">
    <psf:ScoredProperty name="psk:BackCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FrontCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Material">
      <psf:Value xsi:type="xs:string">Polyester</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePrinted">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePunched">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Recycled">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Weight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies specialty high resolution media. -->
  <psf:Option name="psk:HighResolution">
    <psf:ScoredProperty name="psk:BackCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FrontCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Material">
      <psf:Value xsi:type="xs:string">Paper</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePrinted">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePunched">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Recycled">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Weight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies label media. -->
  <psf:Option name="psk:Label">
    <psf:ScoredProperty name="psk:BackCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FrontCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Material">
      <psf:Value xsi:type="xs:string">Paper</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePrinted">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePunched">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Recycled">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Weight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies attached multi-part forms media. -->
  <psf:Option name="psk:MultiLayerForm">
    <psf:ScoredProperty name="psk:BackCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FrontCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Material">
      <psf:Value xsi:type="xs:string">Paper</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePrinted">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePunched">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Recycled">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Weight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies separate multi-part forms media. -->
  <psf:Option name="psk:MultiPartForm">
    <psf:ScoredProperty name="psk:BackCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FrontCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Material">
      <psf:Value xsi:type="xs:string">Paper</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePrinted">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePunched">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Recycled">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Weight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies standard photographic media. -->
  <psf:Option name="psk:Photographic">
    <psf:ScoredProperty name="psk:BackCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FrontCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Material">
      <psf:Value xsi:type="xs:string">Paper</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePrinted">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePunched">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Recycled">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Weight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies film photographic media. -->
  <psf:Option name="psk:PhotographicFilm">
    <psf:ScoredProperty name="psk:BackCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FrontCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Material">
      <psf:Value xsi:type="xs:string">DryFilm</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePrinted">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePunched">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Recycled">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Weight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies glossy photographic media. -->
  <psf:Option name="psk:PhotographicGlossy">
    <psf:ScoredProperty name="psk:BackCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FrontCoating">
      <psf:Value xsi:type="xs:string">Glossy</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Material">
      <psf:Value xsi:type="xs:string">Paper</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePrinted">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePunched">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Recycled">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Weight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies high gloss photographic media. -->
  <psf:Option name="psk:PhotographicHighGloss">
    <psf:ScoredProperty name="psk:BackCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FrontCoating">
      <psf:Value xsi:type="xs:string">HighGloss</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Material">
      <psf:Value xsi:type="xs:string">Paper</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePrinted">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePunched">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Recycled">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Weight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies matte photographic media. -->
  <psf:Option name="psk:PhotographicMatte">
    <psf:ScoredProperty name="psk:BackCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FrontCoating">
      <psf:Value xsi:type="xs:string">Matte</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Material">
      <psf:Value xsi:type="xs:string">Paper</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePrinted">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePunched">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Recycled">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Weight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies satin photographic media. -->
  <psf:Option name="psk:PhotographicSatin">
    <psf:ScoredProperty name="psk:BackCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FrontCoating">
      <psf:Value xsi:type="xs:string">Satin</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Material">
      <psf:Value xsi:type="xs:string">Paper</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePrinted">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePunched">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Recycled">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Weight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies semi-gloss photographic media. -->
  <psf:Option name="psk:PhotographicSemiGloss">
    <psf:ScoredProperty name="psk:BackCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FrontCoating">
      <psf:Value xsi:type="xs:string">SemiGloss</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Material">
      <psf:Value xsi:type="xs:string">Paper</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePrinted">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePunched">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Recycled">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Weight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies standard paper media. -->
  <psf:Option name="psk:Plain">
    <psf:ScoredProperty name="psk:BackCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FrontCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Material">
      <psf:Value xsi:type="xs:string">Paper</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePrinted">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePunched">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Recycled">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Weight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies output to an output display in continuous form. -->
  <psf:Option name="psk:Screen">
    <psf:ScoredProperty name="psk:BackCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FrontCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Material">
      <psf:Value xsi:type="xs:string">Display</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePrinted">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePunched">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Recycled">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Weight">
      <psf:Value xsi:type="xs:integer">0</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies output to an output display in paged form. -->
  <psf:Option name="psk:ScreenPaged">
    <psf:ScoredProperty name="psk:BackCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FrontCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Material">
      <psf:Value xsi:type="xs:string">Display</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePrinted">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePunched">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Recycled">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Weight">
      <psf:Value xsi:type="xs:integer">0</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies specialty stationery media. -->
  <psf:Option name="psk:Stationery">
    <psf:ScoredProperty name="psk:BackCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FrontCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Material">
      <psf:Value xsi:type="xs:string">Display</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePrinted">
      <psf:Value xsi:type="xs:string">Letterhead</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePunched">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Recycled">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Weight">
      <psf:Value xsi:type="xs:integer">0</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies tab stock media that is not pre-cut (single tabs). -->
  <psf:Option name="psk:TabStockFull">
    <psf:ScoredProperty name="psk:BackCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FrontCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Material">
      <psf:Value xsi:type="xs:string">Paper</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePrinted">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePunched">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Recycled">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Weight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies tab stock media that is pre-cut (multiple tabs). -->
  <psf:Option name="psk:TabStockPreCut">
    <psf:ScoredProperty name="psk:BackCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FrontCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Material">
      <psf:Value xsi:type="xs:string">Paper</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePrinted">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePunched">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Recycled">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Weight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies transparency media. -->
  <psf:Option name="psk:Transparency">
    <psf:ScoredProperty name="psk:BackCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FrontCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Material">
      <psf:Value xsi:type="xs:string">Transparency</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePrinted">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePunched">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Recycled">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Weight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies specialty T-shirt transfer media. -->
  <psf:Option name="psk:TShirtTransfer">
    <psf:ScoredProperty name="psk:BackCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FrontCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Material">
      <psf:Value xsi:type="xs:string">Paper</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePrinted">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePunched">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Recycled">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Weight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies unknown or unlisted media. -->
  <psf:Option name="psk:None">
    <psf:ScoredProperty name="psk:BackCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FrontCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Material">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePrinted">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePunched">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Recycled">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Weight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>    
```

## <a name="related-topics"></a><span data-ttu-id="419d5-178">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="419d5-178">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="419d5-179">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="419d5-179">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>
