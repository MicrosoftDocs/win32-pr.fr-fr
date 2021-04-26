---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: 78eb3119-a52f-4ff8-83bb-903e181c8a11
title: PageInputBin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f74e75653f7c6cbc6a586b80b3e8217286ce7c36
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107993766"
---
# <a name="pageinputbin"></a><span data-ttu-id="80545-104">PageInputBin</span><span class="sxs-lookup"><span data-stu-id="80545-104">PageInputBin</span></span>

<span data-ttu-id="80545-105">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="80545-105">This topic is not current.</span></span> <span data-ttu-id="80545-106">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="80545-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="80545-107">Décrit le bac d’entrée installé dans un appareil ou la liste complète des emplacements pris en charge pour un appareil.</span><span class="sxs-lookup"><span data-stu-id="80545-107">Describes the installed input bin in a device or the full list of supported bins for a device.</span></span> <span data-ttu-id="80545-108">Autorise la spécification d’un casier d’entrée par page.</span><span class="sxs-lookup"><span data-stu-id="80545-108">Allows specification of input bin on a per page basis.</span></span> <span data-ttu-id="80545-109">Les mots clés JobInputBin, DocumentInputBin et PageInputBin s’excluent mutuellement.</span><span class="sxs-lookup"><span data-stu-id="80545-109">The JobInputBin, DocumentInputBin, and PageInputBin keywords are mutually exclusive.</span></span> <span data-ttu-id="80545-110">Ils ne doivent pas être spécifiés simultanément dans un document de fonctionnalités PrintTicket ou Print.</span><span class="sxs-lookup"><span data-stu-id="80545-110">Both should not be specified simultaneously in a PrintTicket or Print Capabilities document.</span></span>

-   [<span data-ttu-id="80545-111">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="80545-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="80545-112">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="80545-112">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="80545-113">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="80545-113">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="80545-114">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="80545-114">Element Information</span></span>



| <span data-ttu-id="80545-115">Nom</span><span class="sxs-lookup"><span data-stu-id="80545-115">Name</span></span> | <span data-ttu-id="80545-116">Value</span><span class="sxs-lookup"><span data-stu-id="80545-116">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="80545-117">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="80545-117">Element Type</span></span> <br/>   | <span data-ttu-id="80545-118">Fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="80545-118">Feature</span></span><br/> |
| <span data-ttu-id="80545-119">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="80545-119">Scoping Prefix</span></span> <br/> | <span data-ttu-id="80545-120">Page</span><span class="sxs-lookup"><span data-stu-id="80545-120">Page</span></span><br/>    |
| <span data-ttu-id="80545-121">Notes</span><span class="sxs-lookup"><span data-stu-id="80545-121">Notes</span></span> <br/>          | <span data-ttu-id="80545-122">Aucun</span><span class="sxs-lookup"><span data-stu-id="80545-122">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="80545-123">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="80545-123">Structural Content</span></span>

<span data-ttu-id="80545-124">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="80545-124">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="80545-125">Variables de structure</span><span class="sxs-lookup"><span data-stu-id="80545-125">Structure Variables</span></span>

<span data-ttu-id="80545-126">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="80545-126">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="80545-127">Nom</span><span class="sxs-lookup"><span data-stu-id="80545-127">Name</span></span>                                   | <span data-ttu-id="80545-128">Type de données</span><span class="sxs-lookup"><span data-stu-id="80545-128">Data type</span></span>          | <span data-ttu-id="80545-129">Unité</span><span class="sxs-lookup"><span data-stu-id="80545-129">Unit</span></span>                  | <span data-ttu-id="80545-130">Valeurs prises en charge</span><span class="sxs-lookup"><span data-stu-id="80545-130">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="80545-131">Résumé</span><span class="sxs-lookup"><span data-stu-id="80545-131">Summary</span></span>                                                                             |
|----------------------------------------|--------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="80545-132">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="80545-132">\_OptionName\_</span></span><br/>              | <span data-ttu-id="80545-133">string</span><span class="sxs-lookup"><span data-stu-id="80545-133">string</span></span><br/>  | <span data-ttu-id="80545-134">caractères</span><span class="sxs-lookup"><span data-stu-id="80545-134">characters</span></span><br/> | <span data-ttu-id="80545-135">Nom complet valide tel que défini par les [espaces de noms dans XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="80545-135">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="80545-136">Si aucun espace de noms n’est spécifié, l’espace de noms par défaut est utilisé.</span><span class="sxs-lookup"><span data-stu-id="80545-136">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="80545-137">Nom de l'option.</span><span class="sxs-lookup"><span data-stu-id="80545-137">The name of the option.</span></span><br/>                                                  |
| <span data-ttu-id="80545-138">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="80545-138">\_IdentityOptionValue\_</span></span><br/>     | <span data-ttu-id="80545-139">string</span><span class="sxs-lookup"><span data-stu-id="80545-139">string</span></span><br/>  | <span data-ttu-id="80545-140">n/a</span><span class="sxs-lookup"><span data-stu-id="80545-140">n/a</span></span><br/>        | <span data-ttu-id="80545-141">True, False.</span><span class="sxs-lookup"><span data-stu-id="80545-141">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="80545-142">Définit une option qui, lorsqu’elle est sélectionnée, désactive cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="80545-142">Defines an Option which when selected would disable this feature.</span></span><br/>        |
| <span data-ttu-id="80545-143">\_EnvelopeOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="80545-143">\_EnvelopeOptionValue\_</span></span><br/>     | <span data-ttu-id="80545-144">string</span><span class="sxs-lookup"><span data-stu-id="80545-144">string</span></span><br/>  | <span data-ttu-id="80545-145">n/a</span><span class="sxs-lookup"><span data-stu-id="80545-145">n/a</span></span><br/>        | <span data-ttu-id="80545-146">True, False.</span><span class="sxs-lookup"><span data-stu-id="80545-146">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="80545-147">Définit une option qui, lorsqu’elle est sélectionnée, désactive cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="80545-147">Defines an Option which when selected would disable this feature.</span></span><br/>        |
| <span data-ttu-id="80545-148">\_BinTypeValue\_</span><span class="sxs-lookup"><span data-stu-id="80545-148">\_BinTypeValue\_</span></span><br/>            | <span data-ttu-id="80545-149">string</span><span class="sxs-lookup"><span data-stu-id="80545-149">string</span></span><br/>  | <span data-ttu-id="80545-150">n/a</span><span class="sxs-lookup"><span data-stu-id="80545-150">n/a</span></span><br/>        | <span data-ttu-id="80545-151">ContinuousFeed, SheetFeed.</span><span class="sxs-lookup"><span data-stu-id="80545-151">ContinuousFeed, SheetFeed.</span></span><br/>                                                                                                                                                 | <span data-ttu-id="80545-152">Spécifie le type de l’emplacement.</span><span class="sxs-lookup"><span data-stu-id="80545-152">Specifies the type of the bin.</span></span><br/>                                           |
| <span data-ttu-id="80545-153">\_FeedTypeValue\_</span><span class="sxs-lookup"><span data-stu-id="80545-153">\_FeedTypeValue\_</span></span><br/>           | <span data-ttu-id="80545-154">string</span><span class="sxs-lookup"><span data-stu-id="80545-154">string</span></span><br/>  | <span data-ttu-id="80545-155">n/a</span><span class="sxs-lookup"><span data-stu-id="80545-155">n/a</span></span><br/>        | <span data-ttu-id="80545-156">Automatique, manuel.</span><span class="sxs-lookup"><span data-stu-id="80545-156">Automatic, Manual.</span></span><br/>                                                                                                                                                         | <span data-ttu-id="80545-157">Spécifie le mécanisme de flux de l’emplacement.</span><span class="sxs-lookup"><span data-stu-id="80545-157">Specifies the feed mechanism of the bin.</span></span><br/>                                 |
| <span data-ttu-id="80545-158">\_MediaCapacityValue\_</span><span class="sxs-lookup"><span data-stu-id="80545-158">\_MediaCapacityValue\_</span></span><br/>      | <span data-ttu-id="80545-159">string</span><span class="sxs-lookup"><span data-stu-id="80545-159">string</span></span><br/>  | <span data-ttu-id="80545-160">n/a</span><span class="sxs-lookup"><span data-stu-id="80545-160">n/a</span></span><br/>        | <span data-ttu-id="80545-161">Haute, standard.</span><span class="sxs-lookup"><span data-stu-id="80545-161">High, Standard.</span></span><br/>                                                                                                                                                            | <span data-ttu-id="80545-162">Spécifie si l’emplacement est un casier à capacité élevée (qualitatif).</span><span class="sxs-lookup"><span data-stu-id="80545-162">Specifies whether the bin is a high capacity bin (qualitative).</span></span><br/>          |
| <span data-ttu-id="80545-163">\_MediaSizeAutoSenseValue\_</span><span class="sxs-lookup"><span data-stu-id="80545-163">\_MediaSizeAutoSenseValue\_</span></span><br/> | <span data-ttu-id="80545-164">string</span><span class="sxs-lookup"><span data-stu-id="80545-164">string</span></span><br/>  | <span data-ttu-id="80545-165">n/a</span><span class="sxs-lookup"><span data-stu-id="80545-165">n/a</span></span><br/>        | <span data-ttu-id="80545-166">Pris en charge, aucun.</span><span class="sxs-lookup"><span data-stu-id="80545-166">Supported, None.</span></span><br/>                                                                                                                                                           | <span data-ttu-id="80545-167">Spécifie la fonctionnalité de détection automatique de la taille du média de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="80545-167">Specifies the media size auto sense capability of device.</span></span><br/>                |
| <span data-ttu-id="80545-168">\_MediaTypeAutoSenseValue\_</span><span class="sxs-lookup"><span data-stu-id="80545-168">\_MediaTypeAutoSenseValue\_</span></span><br/> | <span data-ttu-id="80545-169">string</span><span class="sxs-lookup"><span data-stu-id="80545-169">string</span></span><br/>  | <span data-ttu-id="80545-170">n/a</span><span class="sxs-lookup"><span data-stu-id="80545-170">n/a</span></span><br/>        | <span data-ttu-id="80545-171">Pris en charge, aucun.</span><span class="sxs-lookup"><span data-stu-id="80545-171">Supported, None.</span></span><br/>                                                                                                                                                           | <span data-ttu-id="80545-172">Spécifie la fonctionnalité de détection automatique du type de média de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="80545-172">Specifies the media type auto sense capability of device.</span></span><br/>                |
| <span data-ttu-id="80545-173">\_MediaSheetCapacityValue\_</span><span class="sxs-lookup"><span data-stu-id="80545-173">\_MediaSheetCapacityValue\_</span></span><br/> | <span data-ttu-id="80545-174">entier</span><span class="sxs-lookup"><span data-stu-id="80545-174">integer</span></span><br/> | <span data-ttu-id="80545-175">feuilles</span><span class="sxs-lookup"><span data-stu-id="80545-175">sheets</span></span><br/>     | <span data-ttu-id="80545-176">Contrainte d’entier maximale autorisée par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="80545-176">Maximum integer constraint allowed by device.</span></span><br/>                                                                                                                              | <span data-ttu-id="80545-177">Spécifie la capacité du média en nombre de pages (au niveau complet) de l’emplacement.</span><span class="sxs-lookup"><span data-stu-id="80545-177">Specifies the Media capacity in number of pages (full level) of the bin.</span></span><br/> |
| <span data-ttu-id="80545-178">\_MediaPathValue\_</span><span class="sxs-lookup"><span data-stu-id="80545-178">\_MediaPathValue\_</span></span><br/>          | <span data-ttu-id="80545-179">string</span><span class="sxs-lookup"><span data-stu-id="80545-179">string</span></span><br/>  | <span data-ttu-id="80545-180">n/a</span><span class="sxs-lookup"><span data-stu-id="80545-180">n/a</span></span><br/>        | <span data-ttu-id="80545-181">Droit, en serpentin.</span><span class="sxs-lookup"><span data-stu-id="80545-181">Straight, Serpentine.</span></span><br/>                                                                                                                                                      | <span data-ttu-id="80545-182">Spécifie les caractéristiques du chemin d’accès du média.</span><span class="sxs-lookup"><span data-stu-id="80545-182">Specifies the characteristics of the media path.</span></span><br/>                         |
| <span data-ttu-id="80545-183">\_FeedFaceValue\_</span><span class="sxs-lookup"><span data-stu-id="80545-183">\_FeedFaceValue\_</span></span><br/>           | <span data-ttu-id="80545-184">string</span><span class="sxs-lookup"><span data-stu-id="80545-184">string</span></span><br/>  | <span data-ttu-id="80545-185">n/a</span><span class="sxs-lookup"><span data-stu-id="80545-185">n/a</span></span><br/>        | <span data-ttu-id="80545-186">FaceUp, FaceDown</span><span class="sxs-lookup"><span data-stu-id="80545-186">FaceUp, FaceDown</span></span><br/>                                                                                                                                                           | <span data-ttu-id="80545-187">Spécifie si le média doit être imprimé vers le haut ou vers le haut.</span><span class="sxs-lookup"><span data-stu-id="80545-187">Specifies whether media is to be printed face up or face down.</span></span><br/>           |
| <span data-ttu-id="80545-188">\_FeedDirectionValue\_</span><span class="sxs-lookup"><span data-stu-id="80545-188">\_FeedDirectionValue\_</span></span><br/>      | <span data-ttu-id="80545-189">string</span><span class="sxs-lookup"><span data-stu-id="80545-189">string</span></span><br/>  | <span data-ttu-id="80545-190">n/a</span><span class="sxs-lookup"><span data-stu-id="80545-190">n/a</span></span><br/>        | <span data-ttu-id="80545-191">LongEdgeFirst, ShortEdgeFirst</span><span class="sxs-lookup"><span data-stu-id="80545-191">LongEdgeFirst, ShortEdgeFirst</span></span><br/>                                                                                                                                              | <span data-ttu-id="80545-192">Spécifie si le média est alimenté en premier ou à l’extrémité du long bord.</span><span class="sxs-lookup"><span data-stu-id="80545-192">Specifies whether media is fed long edge first or short edge first.</span></span><br/>      |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="80545-193">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="80545-193">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="80545-194">Les mots clés de schéma d’impression publics sont définis dans l' https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords espace de noms.</span><span class="sxs-lookup"><span data-stu-id="80545-194">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="80545-195">Le contenu de la Extensible Markup Language publique (XML) pour ce mot clé est défini ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="80545-195">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="80545-196">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="80545-196">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="80545-197">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="80545-197">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




