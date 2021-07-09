---
description: Obtenir des informations sur l’élément configurable par l’utilisateur PageInputBin. Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: 78eb3119-a52f-4ff8-83bb-903e181c8a11
title: PageInputBin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc53d377106b95b26e694d531af2952cea98a8b1
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/09/2021
ms.locfileid: "113549167"
---
# <a name="pageinputbin"></a><span data-ttu-id="a7e79-105">PageInputBin</span><span class="sxs-lookup"><span data-stu-id="a7e79-105">PageInputBin</span></span>

<span data-ttu-id="a7e79-106">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="a7e79-106">This topic is not current.</span></span> <span data-ttu-id="a7e79-107">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="a7e79-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="a7e79-108">Décrit le bac d’entrée installé dans un appareil ou la liste complète des emplacements pris en charge pour un appareil.</span><span class="sxs-lookup"><span data-stu-id="a7e79-108">Describes the installed input bin in a device or the full list of supported bins for a device.</span></span> <span data-ttu-id="a7e79-109">Autorise la spécification d’un casier d’entrée par page.</span><span class="sxs-lookup"><span data-stu-id="a7e79-109">Allows specification of input bin on a per page basis.</span></span> <span data-ttu-id="a7e79-110">Les mots clés JobInputBin, DocumentInputBin et PageInputBin s’excluent mutuellement.</span><span class="sxs-lookup"><span data-stu-id="a7e79-110">The JobInputBin, DocumentInputBin, and PageInputBin keywords are mutually exclusive.</span></span> <span data-ttu-id="a7e79-111">Ils ne doivent pas être spécifiés simultanément dans un document de fonctionnalités PrintTicket ou Print.</span><span class="sxs-lookup"><span data-stu-id="a7e79-111">Both should not be specified simultaneously in a PrintTicket or Print Capabilities document.</span></span>

-   [<span data-ttu-id="a7e79-112">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="a7e79-112">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="a7e79-113">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="a7e79-113">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="a7e79-114">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="a7e79-114">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="a7e79-115">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="a7e79-115">Element Information</span></span>



| <span data-ttu-id="a7e79-116">Nom</span><span class="sxs-lookup"><span data-stu-id="a7e79-116">Name</span></span> | <span data-ttu-id="a7e79-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="a7e79-117">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="a7e79-118">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="a7e79-118">Element Type</span></span> <br/>   | <span data-ttu-id="a7e79-119">Composant</span><span class="sxs-lookup"><span data-stu-id="a7e79-119">Feature</span></span><br/> |
| <span data-ttu-id="a7e79-120">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="a7e79-120">Scoping Prefix</span></span> <br/> | <span data-ttu-id="a7e79-121">Page</span><span class="sxs-lookup"><span data-stu-id="a7e79-121">Page</span></span><br/>    |
| <span data-ttu-id="a7e79-122">Notes</span><span class="sxs-lookup"><span data-stu-id="a7e79-122">Notes</span></span> <br/>          | <span data-ttu-id="a7e79-123">Aucun</span><span class="sxs-lookup"><span data-stu-id="a7e79-123">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="a7e79-124">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="a7e79-124">Structural Content</span></span>

<span data-ttu-id="a7e79-125">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="a7e79-125">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageInputBin">
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

## <a name="structure-variables"></a><span data-ttu-id="a7e79-126">Variables de structure</span><span class="sxs-lookup"><span data-stu-id="a7e79-126">Structure Variables</span></span>

<span data-ttu-id="a7e79-127">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="a7e79-127">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="a7e79-128">Nom</span><span class="sxs-lookup"><span data-stu-id="a7e79-128">Name</span></span>                                   | <span data-ttu-id="a7e79-129">Type de données</span><span class="sxs-lookup"><span data-stu-id="a7e79-129">Data type</span></span>          | <span data-ttu-id="a7e79-130">Unité</span><span class="sxs-lookup"><span data-stu-id="a7e79-130">Unit</span></span>                  | <span data-ttu-id="a7e79-131">Valeurs prises en charge</span><span class="sxs-lookup"><span data-stu-id="a7e79-131">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="a7e79-132">Résumé</span><span class="sxs-lookup"><span data-stu-id="a7e79-132">Summary</span></span>                                                                             |
|----------------------------------------|--------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="a7e79-133">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="a7e79-133">\_OptionName\_</span></span><br/>              | <span data-ttu-id="a7e79-134">string</span><span class="sxs-lookup"><span data-stu-id="a7e79-134">string</span></span><br/>  | <span data-ttu-id="a7e79-135">caractères</span><span class="sxs-lookup"><span data-stu-id="a7e79-135">characters</span></span><br/> | <span data-ttu-id="a7e79-136">Nom complet valide tel que défini par les [espaces de noms dans XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="a7e79-136">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="a7e79-137">Si aucun espace de noms n’est spécifié, l’espace de noms par défaut est utilisé.</span><span class="sxs-lookup"><span data-stu-id="a7e79-137">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="a7e79-138">Nom de l'option.</span><span class="sxs-lookup"><span data-stu-id="a7e79-138">The name of the option.</span></span><br/>                                                  |
| <span data-ttu-id="a7e79-139">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="a7e79-139">\_IdentityOptionValue\_</span></span><br/>     | <span data-ttu-id="a7e79-140">string</span><span class="sxs-lookup"><span data-stu-id="a7e79-140">string</span></span><br/>  | <span data-ttu-id="a7e79-141">n/a</span><span class="sxs-lookup"><span data-stu-id="a7e79-141">n/a</span></span><br/>        | <span data-ttu-id="a7e79-142">True, False.</span><span class="sxs-lookup"><span data-stu-id="a7e79-142">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="a7e79-143">Définit une option qui, lorsqu’elle est sélectionnée, désactive cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="a7e79-143">Defines an Option which when selected would disable this feature.</span></span><br/>        |
| <span data-ttu-id="a7e79-144">\_EnvelopeOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="a7e79-144">\_EnvelopeOptionValue\_</span></span><br/>     | <span data-ttu-id="a7e79-145">string</span><span class="sxs-lookup"><span data-stu-id="a7e79-145">string</span></span><br/>  | <span data-ttu-id="a7e79-146">n/a</span><span class="sxs-lookup"><span data-stu-id="a7e79-146">n/a</span></span><br/>        | <span data-ttu-id="a7e79-147">True, False.</span><span class="sxs-lookup"><span data-stu-id="a7e79-147">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="a7e79-148">Définit une option qui, lorsqu’elle est sélectionnée, désactive cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="a7e79-148">Defines an Option which when selected would disable this feature.</span></span><br/>        |
| <span data-ttu-id="a7e79-149">\_BinTypeValue\_</span><span class="sxs-lookup"><span data-stu-id="a7e79-149">\_BinTypeValue\_</span></span><br/>            | <span data-ttu-id="a7e79-150">string</span><span class="sxs-lookup"><span data-stu-id="a7e79-150">string</span></span><br/>  | <span data-ttu-id="a7e79-151">n/a</span><span class="sxs-lookup"><span data-stu-id="a7e79-151">n/a</span></span><br/>        | <span data-ttu-id="a7e79-152">ContinuousFeed, SheetFeed.</span><span class="sxs-lookup"><span data-stu-id="a7e79-152">ContinuousFeed, SheetFeed.</span></span><br/>                                                                                                                                                 | <span data-ttu-id="a7e79-153">Spécifie le type de l’emplacement.</span><span class="sxs-lookup"><span data-stu-id="a7e79-153">Specifies the type of the bin.</span></span><br/>                                           |
| <span data-ttu-id="a7e79-154">\_FeedTypeValue\_</span><span class="sxs-lookup"><span data-stu-id="a7e79-154">\_FeedTypeValue\_</span></span><br/>           | <span data-ttu-id="a7e79-155">string</span><span class="sxs-lookup"><span data-stu-id="a7e79-155">string</span></span><br/>  | <span data-ttu-id="a7e79-156">n/a</span><span class="sxs-lookup"><span data-stu-id="a7e79-156">n/a</span></span><br/>        | <span data-ttu-id="a7e79-157">Automatique, manuel.</span><span class="sxs-lookup"><span data-stu-id="a7e79-157">Automatic, Manual.</span></span><br/>                                                                                                                                                         | <span data-ttu-id="a7e79-158">Spécifie le mécanisme de flux de l’emplacement.</span><span class="sxs-lookup"><span data-stu-id="a7e79-158">Specifies the feed mechanism of the bin.</span></span><br/>                                 |
| <span data-ttu-id="a7e79-159">\_MediaCapacityValue\_</span><span class="sxs-lookup"><span data-stu-id="a7e79-159">\_MediaCapacityValue\_</span></span><br/>      | <span data-ttu-id="a7e79-160">string</span><span class="sxs-lookup"><span data-stu-id="a7e79-160">string</span></span><br/>  | <span data-ttu-id="a7e79-161">n/a</span><span class="sxs-lookup"><span data-stu-id="a7e79-161">n/a</span></span><br/>        | <span data-ttu-id="a7e79-162">Haute, standard.</span><span class="sxs-lookup"><span data-stu-id="a7e79-162">High, Standard.</span></span><br/>                                                                                                                                                            | <span data-ttu-id="a7e79-163">Spécifie si l’emplacement est un casier à capacité élevée (qualitatif).</span><span class="sxs-lookup"><span data-stu-id="a7e79-163">Specifies whether the bin is a high capacity bin (qualitative).</span></span><br/>          |
| <span data-ttu-id="a7e79-164">\_MediaSizeAutoSenseValue\_</span><span class="sxs-lookup"><span data-stu-id="a7e79-164">\_MediaSizeAutoSenseValue\_</span></span><br/> | <span data-ttu-id="a7e79-165">string</span><span class="sxs-lookup"><span data-stu-id="a7e79-165">string</span></span><br/>  | <span data-ttu-id="a7e79-166">n/a</span><span class="sxs-lookup"><span data-stu-id="a7e79-166">n/a</span></span><br/>        | <span data-ttu-id="a7e79-167">Pris en charge, aucun.</span><span class="sxs-lookup"><span data-stu-id="a7e79-167">Supported, None.</span></span><br/>                                                                                                                                                           | <span data-ttu-id="a7e79-168">Spécifie la fonctionnalité de détection automatique de la taille du média de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="a7e79-168">Specifies the media size auto sense capability of device.</span></span><br/>                |
| <span data-ttu-id="a7e79-169">\_MediaTypeAutoSenseValue\_</span><span class="sxs-lookup"><span data-stu-id="a7e79-169">\_MediaTypeAutoSenseValue\_</span></span><br/> | <span data-ttu-id="a7e79-170">string</span><span class="sxs-lookup"><span data-stu-id="a7e79-170">string</span></span><br/>  | <span data-ttu-id="a7e79-171">n/a</span><span class="sxs-lookup"><span data-stu-id="a7e79-171">n/a</span></span><br/>        | <span data-ttu-id="a7e79-172">Pris en charge, aucun.</span><span class="sxs-lookup"><span data-stu-id="a7e79-172">Supported, None.</span></span><br/>                                                                                                                                                           | <span data-ttu-id="a7e79-173">Spécifie la fonctionnalité de détection automatique du type de média de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="a7e79-173">Specifies the media type auto sense capability of device.</span></span><br/>                |
| <span data-ttu-id="a7e79-174">\_MediaSheetCapacityValue\_</span><span class="sxs-lookup"><span data-stu-id="a7e79-174">\_MediaSheetCapacityValue\_</span></span><br/> | <span data-ttu-id="a7e79-175">entier</span><span class="sxs-lookup"><span data-stu-id="a7e79-175">integer</span></span><br/> | <span data-ttu-id="a7e79-176">feuilles</span><span class="sxs-lookup"><span data-stu-id="a7e79-176">sheets</span></span><br/>     | <span data-ttu-id="a7e79-177">Contrainte d’entier maximale autorisée par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="a7e79-177">Maximum integer constraint allowed by device.</span></span><br/>                                                                                                                              | <span data-ttu-id="a7e79-178">Spécifie la capacité du média en nombre de pages (au niveau complet) de l’emplacement.</span><span class="sxs-lookup"><span data-stu-id="a7e79-178">Specifies the Media capacity in number of pages (full level) of the bin.</span></span><br/> |
| <span data-ttu-id="a7e79-179">\_MediaPathValue\_</span><span class="sxs-lookup"><span data-stu-id="a7e79-179">\_MediaPathValue\_</span></span><br/>          | <span data-ttu-id="a7e79-180">string</span><span class="sxs-lookup"><span data-stu-id="a7e79-180">string</span></span><br/>  | <span data-ttu-id="a7e79-181">n/a</span><span class="sxs-lookup"><span data-stu-id="a7e79-181">n/a</span></span><br/>        | <span data-ttu-id="a7e79-182">Droit, en serpentin.</span><span class="sxs-lookup"><span data-stu-id="a7e79-182">Straight, Serpentine.</span></span><br/>                                                                                                                                                      | <span data-ttu-id="a7e79-183">Spécifie les caractéristiques du chemin d’accès du média.</span><span class="sxs-lookup"><span data-stu-id="a7e79-183">Specifies the characteristics of the media path.</span></span><br/>                         |
| <span data-ttu-id="a7e79-184">\_FeedFaceValue\_</span><span class="sxs-lookup"><span data-stu-id="a7e79-184">\_FeedFaceValue\_</span></span><br/>           | <span data-ttu-id="a7e79-185">string</span><span class="sxs-lookup"><span data-stu-id="a7e79-185">string</span></span><br/>  | <span data-ttu-id="a7e79-186">n/a</span><span class="sxs-lookup"><span data-stu-id="a7e79-186">n/a</span></span><br/>        | <span data-ttu-id="a7e79-187">FaceUp, FaceDown</span><span class="sxs-lookup"><span data-stu-id="a7e79-187">FaceUp, FaceDown</span></span><br/>                                                                                                                                                           | <span data-ttu-id="a7e79-188">Spécifie si le média doit être imprimé vers le haut ou vers le haut.</span><span class="sxs-lookup"><span data-stu-id="a7e79-188">Specifies whether media is to be printed face up or face down.</span></span><br/>           |
| <span data-ttu-id="a7e79-189">\_FeedDirectionValue\_</span><span class="sxs-lookup"><span data-stu-id="a7e79-189">\_FeedDirectionValue\_</span></span><br/>      | <span data-ttu-id="a7e79-190">string</span><span class="sxs-lookup"><span data-stu-id="a7e79-190">string</span></span><br/>  | <span data-ttu-id="a7e79-191">n/a</span><span class="sxs-lookup"><span data-stu-id="a7e79-191">n/a</span></span><br/>        | <span data-ttu-id="a7e79-192">LongEdgeFirst, ShortEdgeFirst</span><span class="sxs-lookup"><span data-stu-id="a7e79-192">LongEdgeFirst, ShortEdgeFirst</span></span><br/>                                                                                                                                              | <span data-ttu-id="a7e79-193">Spécifie si le média est alimenté en premier ou à l’extrémité du long bord.</span><span class="sxs-lookup"><span data-stu-id="a7e79-193">Specifies whether media is fed long edge first or short edge first.</span></span><br/>      |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="a7e79-194">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="a7e79-194">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="a7e79-195">Les mots clés de schéma d’impression publics sont définis dans l' https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords espace de noms.</span><span class="sxs-lookup"><span data-stu-id="a7e79-195">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="a7e79-196">Le contenu de la Extensible Markup Language publique (XML) pour ce mot clé est défini ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="a7e79-196">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageInputBin">
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

## <a name="related-topics"></a><span data-ttu-id="a7e79-197">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a7e79-197">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a7e79-198">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="a7e79-198">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




