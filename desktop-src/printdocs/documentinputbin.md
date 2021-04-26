---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: 334503d7-c044-41f7-b6aa-892b002b7a4e
title: DocumentInputBin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57890492ed5f0b575e6d462351282dd199f34f45
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997766"
---
# <a name="documentinputbin"></a><span data-ttu-id="2c91b-104">DocumentInputBin</span><span class="sxs-lookup"><span data-stu-id="2c91b-104">DocumentInputBin</span></span>

<span data-ttu-id="2c91b-105">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="2c91b-105">This topic is not current.</span></span> <span data-ttu-id="2c91b-106">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="2c91b-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="2c91b-107">Décrit le bac d’entrée installé dans un appareil ou la liste complète des emplacements pris en charge pour un appareil.</span><span class="sxs-lookup"><span data-stu-id="2c91b-107">Describes the installed input bin in a device or the full list of supported bins for a device.</span></span> <span data-ttu-id="2c91b-108">Les mots clés JobInputBin, DocumentInputBin et PageInputBin s’excluent mutuellement.</span><span class="sxs-lookup"><span data-stu-id="2c91b-108">The JobInputBin, DocumentInputBin, and PageInputBin keywords are mutually exclusive.</span></span> <span data-ttu-id="2c91b-109">Ils ne doivent pas être spécifiés simultanément dans un document de fonctionnalités PrintTicket ou Print.</span><span class="sxs-lookup"><span data-stu-id="2c91b-109">Both should not be specified simultaneously in a PrintTicket or Print Capabilities document.</span></span>

-   [<span data-ttu-id="2c91b-110">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="2c91b-110">Element Information</span></span>](#element-information)

-   [<span data-ttu-id="2c91b-111">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="2c91b-111">Structural Content</span></span>](#structural-content)

-   [<span data-ttu-id="2c91b-112">Contenu XML</span><span class="sxs-lookup"><span data-stu-id="2c91b-112">XML Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="2c91b-113">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="2c91b-113">Element Information</span></span>



| <span data-ttu-id="2c91b-114">Nom</span><span class="sxs-lookup"><span data-stu-id="2c91b-114">Name</span></span> | <span data-ttu-id="2c91b-115">Value</span><span class="sxs-lookup"><span data-stu-id="2c91b-115">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c91b-116">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="2c91b-116">Element Type</span></span> <br/>   | <span data-ttu-id="2c91b-117">Fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="2c91b-117">Feature</span></span><br/>                                                                                                             |
| <span data-ttu-id="2c91b-118">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="2c91b-118">Scoping Prefix</span></span> <br/> | <span data-ttu-id="2c91b-119">Document</span><span class="sxs-lookup"><span data-stu-id="2c91b-119">Document</span></span><br/>                                                                                                            |
| <span data-ttu-id="2c91b-120">Notes</span><span class="sxs-lookup"><span data-stu-id="2c91b-120">Notes</span></span> <br/>          | <span data-ttu-id="2c91b-121">Les emplacements pris en charge qui ne sont pas installés actuellement doivent être signalés comme étant limités dans le document PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="2c91b-121">Supported bins that are not currently installed should be flagged as constrained in the PrintCapabilities document.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="2c91b-122">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="2c91b-122">Structural Content</span></span>

<span data-ttu-id="2c91b-123">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="2c91b-123">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:DocumentInputBin">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <psf:Property name="psf:_EnvelopeOptionValue_">
      <psf:Value xsi:type="xs:string">_EnvelopeOptionValue_</psf:Value>
    </psf:Property>
    <psf:ScoredProperty name="psk:BinType">
      <psf:Value xsi:type="xs:string">_BinTypeValue_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FeedType">
      <psf:Value xsi:type="xs:string">_FeedTypeValue_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaCapacity">
      <psf:Value xsi:type="xs:string">_MediaCapacityValue_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeAutoSense">
      <psf:Value xsi:type="xs:string">_MediaSizeAutoSenseValue_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaTypeAutoSense">
      <psf:Value xsi:type="xs:string">_MediaTypeAutoSenseValue_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSheetCapacity">
      <psf:Value xsi:type="xs:integer">_MediaSheetCapacityValue_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaPath">
      <psf:Value xsi:type="xs:string">_MediaPathValue_</psf:Value>
    </psf:ScoredProperty>
    <psf:Property name="psk:FeedFace">
      <psf:Value xsi:type="xs:string">_FeedFaceValue_</psf:Value>
    </psf:Property>
    <psf:Property name="psk:FeedDirection">
      <psf:Value xsi:type="xs:string">_FeedDirectionValue_</psf:Value>
    </psf:Property>
  </psf:Option>
</psf:Feature>
```

## <a name="structure-variables"></a><span data-ttu-id="2c91b-124">Variables de structure</span><span class="sxs-lookup"><span data-stu-id="2c91b-124">Structure Variables</span></span>

<span data-ttu-id="2c91b-125">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="2c91b-125">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="2c91b-126">Nom</span><span class="sxs-lookup"><span data-stu-id="2c91b-126">Name</span></span>                                   | <span data-ttu-id="2c91b-127">Type de données</span><span class="sxs-lookup"><span data-stu-id="2c91b-127">Data type</span></span>          | <span data-ttu-id="2c91b-128">Unité</span><span class="sxs-lookup"><span data-stu-id="2c91b-128">Unit</span></span>                  | <span data-ttu-id="2c91b-129">Valeurs prises en charge</span><span class="sxs-lookup"><span data-stu-id="2c91b-129">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="2c91b-130">Résumé</span><span class="sxs-lookup"><span data-stu-id="2c91b-130">Summary</span></span>                                                                             |
|----------------------------------------|--------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="2c91b-131">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="2c91b-131">\_OptionName\_</span></span><br/>              | <span data-ttu-id="2c91b-132">string</span><span class="sxs-lookup"><span data-stu-id="2c91b-132">string</span></span><br/>  | <span data-ttu-id="2c91b-133">caractères</span><span class="sxs-lookup"><span data-stu-id="2c91b-133">characters</span></span><br/> | <span data-ttu-id="2c91b-134">Nom complet valide tel que défini par les [espaces de noms dans XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="2c91b-134">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="2c91b-135">Si aucun espace de noms n’est spécifié, l’espace de noms par défaut est utilisé.</span><span class="sxs-lookup"><span data-stu-id="2c91b-135">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="2c91b-136">Nom de l'option.</span><span class="sxs-lookup"><span data-stu-id="2c91b-136">The name of the option.</span></span><br/>                                                  |
| <span data-ttu-id="2c91b-137">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="2c91b-137">\_IdentityOptionValue\_</span></span><br/>     | <span data-ttu-id="2c91b-138">string</span><span class="sxs-lookup"><span data-stu-id="2c91b-138">string</span></span><br/>  | <span data-ttu-id="2c91b-139">n/a</span><span class="sxs-lookup"><span data-stu-id="2c91b-139">n/a</span></span><br/>        | <span data-ttu-id="2c91b-140">True, False.</span><span class="sxs-lookup"><span data-stu-id="2c91b-140">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="2c91b-141">Définit une option qui, lorsqu’elle est sélectionnée, désactive cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="2c91b-141">Defines an Option which when selected would disable this feature.</span></span><br/>        |
| <span data-ttu-id="2c91b-142">\_EnvelopeOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="2c91b-142">\_EnvelopeOptionValue\_</span></span><br/>     | <span data-ttu-id="2c91b-143">string</span><span class="sxs-lookup"><span data-stu-id="2c91b-143">string</span></span><br/>  | <span data-ttu-id="2c91b-144">n/a</span><span class="sxs-lookup"><span data-stu-id="2c91b-144">n/a</span></span><br/>        | <span data-ttu-id="2c91b-145">True, False.</span><span class="sxs-lookup"><span data-stu-id="2c91b-145">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="2c91b-146">Définit une option qui, lorsqu’elle est sélectionnée, désactive cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="2c91b-146">Defines an Option which when selected would disable this feature.</span></span><br/>        |
| <span data-ttu-id="2c91b-147">\_BinTypeValue\_</span><span class="sxs-lookup"><span data-stu-id="2c91b-147">\_BinTypeValue\_</span></span><br/>            | <span data-ttu-id="2c91b-148">string</span><span class="sxs-lookup"><span data-stu-id="2c91b-148">string</span></span><br/>  | <span data-ttu-id="2c91b-149">n/a</span><span class="sxs-lookup"><span data-stu-id="2c91b-149">n/a</span></span><br/>        | <span data-ttu-id="2c91b-150">ContinuousFeed, SheetFeed.</span><span class="sxs-lookup"><span data-stu-id="2c91b-150">ContinuousFeed, SheetFeed.</span></span><br/>                                                                                                                                                 | <span data-ttu-id="2c91b-151">Spécifie le type de l’emplacement.</span><span class="sxs-lookup"><span data-stu-id="2c91b-151">Specifies the type of the bin.</span></span><br/>                                           |
| <span data-ttu-id="2c91b-152">\_FeedTypeValue\_</span><span class="sxs-lookup"><span data-stu-id="2c91b-152">\_FeedTypeValue\_</span></span><br/>           | <span data-ttu-id="2c91b-153">string</span><span class="sxs-lookup"><span data-stu-id="2c91b-153">string</span></span><br/>  | <span data-ttu-id="2c91b-154">n/a</span><span class="sxs-lookup"><span data-stu-id="2c91b-154">n/a</span></span><br/>        | <span data-ttu-id="2c91b-155">Automatique, manuel.</span><span class="sxs-lookup"><span data-stu-id="2c91b-155">Automatic, Manual.</span></span><br/>                                                                                                                                                         | <span data-ttu-id="2c91b-156">Spécifie le mécanisme de flux de l’emplacement.</span><span class="sxs-lookup"><span data-stu-id="2c91b-156">Specifies the feed mechanism of the bin.</span></span><br/>                                 |
| <span data-ttu-id="2c91b-157">\_MediaCapacityValue\_</span><span class="sxs-lookup"><span data-stu-id="2c91b-157">\_MediaCapacityValue\_</span></span><br/>      | <span data-ttu-id="2c91b-158">entier</span><span class="sxs-lookup"><span data-stu-id="2c91b-158">integer</span></span><br/> | <span data-ttu-id="2c91b-159">feuilles</span><span class="sxs-lookup"><span data-stu-id="2c91b-159">sheets</span></span><br/>     | <span data-ttu-id="2c91b-160">Contrainte d’entier maximale autorisée par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="2c91b-160">Maximum integer constraint allowed by device.</span></span><br/>                                                                                                                              | <span data-ttu-id="2c91b-161">Spécifie si l’emplacement est un casier à capacité élevée (qualitatif).</span><span class="sxs-lookup"><span data-stu-id="2c91b-161">Specifies whether the bin is a high capacity bin (qualitative).</span></span><br/>          |
| <span data-ttu-id="2c91b-162">\_MediaSizeAutoSenseValue\_</span><span class="sxs-lookup"><span data-stu-id="2c91b-162">\_MediaSizeAutoSenseValue\_</span></span><br/> | <span data-ttu-id="2c91b-163">string</span><span class="sxs-lookup"><span data-stu-id="2c91b-163">string</span></span><br/>  | <span data-ttu-id="2c91b-164">n/a</span><span class="sxs-lookup"><span data-stu-id="2c91b-164">n/a</span></span><br/>        | <span data-ttu-id="2c91b-165">Pris en charge, aucun.</span><span class="sxs-lookup"><span data-stu-id="2c91b-165">Supported, None.</span></span><br/>                                                                                                                                                           | <span data-ttu-id="2c91b-166">Spécifie la fonctionnalité de détection automatique de la taille du média de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="2c91b-166">Specifies the media size auto sense capability of the device.</span></span><br/>            |
| <span data-ttu-id="2c91b-167">\_MediaTypeAutoSenseValue\_</span><span class="sxs-lookup"><span data-stu-id="2c91b-167">\_MediaTypeAutoSenseValue\_</span></span><br/> | <span data-ttu-id="2c91b-168">string</span><span class="sxs-lookup"><span data-stu-id="2c91b-168">string</span></span><br/>  | <span data-ttu-id="2c91b-169">n/a</span><span class="sxs-lookup"><span data-stu-id="2c91b-169">n/a</span></span><br/>        | <span data-ttu-id="2c91b-170">Pris en charge, aucun.</span><span class="sxs-lookup"><span data-stu-id="2c91b-170">Supported, None.</span></span><br/>                                                                                                                                                           | <span data-ttu-id="2c91b-171">Spécifie la capacité du média en nombre de pages (au niveau complet) de l’emplacement.</span><span class="sxs-lookup"><span data-stu-id="2c91b-171">Specifies the media capacity in number of pages (full level) of the bin.</span></span><br/> |
| <span data-ttu-id="2c91b-172">\_MediaPathValue\_</span><span class="sxs-lookup"><span data-stu-id="2c91b-172">\_MediaPathValue\_</span></span><br/>          | <span data-ttu-id="2c91b-173">string</span><span class="sxs-lookup"><span data-stu-id="2c91b-173">string</span></span><br/>  | <span data-ttu-id="2c91b-174">n/a</span><span class="sxs-lookup"><span data-stu-id="2c91b-174">n/a</span></span><br/>        | <span data-ttu-id="2c91b-175">Droit, en serpentin.</span><span class="sxs-lookup"><span data-stu-id="2c91b-175">Straight, Serpentine.</span></span><br/>                                                                                                                                                      | <span data-ttu-id="2c91b-176">Spécifie les caractéristiques du chemin d’accès du média.</span><span class="sxs-lookup"><span data-stu-id="2c91b-176">Specifies the characteristics of the media path.</span></span><br/>                         |
| <span data-ttu-id="2c91b-177">\_FeedFaceValue\_</span><span class="sxs-lookup"><span data-stu-id="2c91b-177">\_FeedFaceValue\_</span></span><br/>           | <span data-ttu-id="2c91b-178">string</span><span class="sxs-lookup"><span data-stu-id="2c91b-178">string</span></span><br/>  | <span data-ttu-id="2c91b-179">n/a</span><span class="sxs-lookup"><span data-stu-id="2c91b-179">n/a</span></span><br/>        | <span data-ttu-id="2c91b-180">FaceUp, FaceDown</span><span class="sxs-lookup"><span data-stu-id="2c91b-180">FaceUp, FaceDown</span></span><br/>                                                                                                                                                           | <span data-ttu-id="2c91b-181">Spécifie si le média doit être imprimé vers le haut ou vers le haut.</span><span class="sxs-lookup"><span data-stu-id="2c91b-181">Specifies whether media is to be printed face up or face down.</span></span><br/>           |
| <span data-ttu-id="2c91b-182">\_FeedDirectionValue\_</span><span class="sxs-lookup"><span data-stu-id="2c91b-182">\_FeedDirectionValue\_</span></span><br/>      | <span data-ttu-id="2c91b-183">string</span><span class="sxs-lookup"><span data-stu-id="2c91b-183">string</span></span><br/>  | <span data-ttu-id="2c91b-184">n/a</span><span class="sxs-lookup"><span data-stu-id="2c91b-184">n/a</span></span><br/>        | <span data-ttu-id="2c91b-185">LongEdgeFirst, ShortEdgeFirst</span><span class="sxs-lookup"><span data-stu-id="2c91b-185">LongEdgeFirst, ShortEdgeFirst</span></span><br/>                                                                                                                                              | <span data-ttu-id="2c91b-186">Spécifie si le média est alimenté en premier ou à l’extrémité du long bord.</span><span class="sxs-lookup"><span data-stu-id="2c91b-186">Specifies whether media is fed long edge first or short edge first.</span></span><br/>      |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="2c91b-187">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="2c91b-187">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="2c91b-188">Les mots clés de schéma d’impression publics sont définis dans l' https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords espace de noms.</span><span class="sxs-lookup"><span data-stu-id="2c91b-188">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="2c91b-189">Le contenu de la Extensible Markup Language publique (XML) pour ce mot clé est défini ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="2c91b-189">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:DocumentInputBin">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Device will automatically choose best option based on configuration -->
  <psf:Option name="psk:AutoSelect">
    <psf:ScoredProperty name="psk:BinType">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FeedType">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaCapacity">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeAutoSense">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaTypeAutoSense">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSheetCapacity">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaPath">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:Property name="psk:FeedFace">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:Property>
    <psf:Property name="psk:FeedDirection">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:Property>
  </psf:Option>
  <!--Specifies the default manual feed bin -->
  <psf:Option name="psk:Manual">
    <psf:ScoredProperty name="psk:BinType">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FeedType">
      <psf:Value xsi:type="xs:string">Manual</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaCapacity">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeAutoSense">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaTypeAutoSense">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSheetCapacity">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaPath">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:Property name="psk:FeedFace">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:Property>
    <psf:Property name="psk:FeedDirection">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:Property>
  </psf:Option>
  <!--Specifies the feed bin is a cassette-->
  <psf:Option name="psk:Cassette">
    <psf:ScoredProperty name="psk:BinType">
      <psf:Value xsi:type="xs:string">SheetFeed</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FeedType">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaCapacity">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeAutoSense">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaTypeAutoSense">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSheetCapacity">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaPath">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:Property name="psk:FeedFace">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:Property>
    <psf:Property name="psk:FeedDirection">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:Property>
  </psf:Option>
  <!--Specifies the feed bin is a tractor-->
  <psf:Option name="psk:Tractor">
    <psf:ScoredProperty name="psk:BinType">
      <psf:Value xsi:type="xs:string">ContinuousFeed</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FeedType">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaCapacity">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeAutoSense">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaTypeAutoSense">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSheetCapacity">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaPath">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:Property name="psk:FeedFace">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:Property>
    <psf:Property name="psk:FeedDirection">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:Property>
  </psf:Option>
  <!-- Device Input tray for Inkjet Printers -->
  <psf:Option name="psk:AutoSheetFeeder">
    <psf:ScoredProperty name="psk:BinType">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FeedType">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaCapacity">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeAutoSense">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaTypeAutoSense">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSheetCapacity">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaPath">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:Property name="psk:FeedFace">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:Property>
    <psf:Property name="psk:FeedDirection">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:Property>
  </psf:Option>
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="2c91b-190">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2c91b-190">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2c91b-191">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="2c91b-191">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




