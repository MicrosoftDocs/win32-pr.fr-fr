---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: 334503d7-c044-41f7-b6aa-892b002b7a4e
title: DocumentInputBin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95a4459f621ac4455a69e891c2eeda6f785b6d8b
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "106545223"
---
# <a name="documentinputbin"></a><span data-ttu-id="8880f-104">DocumentInputBin</span><span class="sxs-lookup"><span data-stu-id="8880f-104">DocumentInputBin</span></span>

<span data-ttu-id="8880f-105">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="8880f-105">This topic is not current.</span></span> <span data-ttu-id="8880f-106">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="8880f-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="8880f-107">Décrit le bac d’entrée installé dans un appareil ou la liste complète des emplacements pris en charge pour un appareil.</span><span class="sxs-lookup"><span data-stu-id="8880f-107">Describes the installed input bin in a device or the full list of supported bins for a device.</span></span> <span data-ttu-id="8880f-108">Les mots clés JobInputBin, DocumentInputBin et PageInputBin s’excluent mutuellement.</span><span class="sxs-lookup"><span data-stu-id="8880f-108">The JobInputBin, DocumentInputBin, and PageInputBin keywords are mutually exclusive.</span></span> <span data-ttu-id="8880f-109">Ils ne doivent pas être spécifiés simultanément dans un document de fonctionnalités PrintTicket ou Print.</span><span class="sxs-lookup"><span data-stu-id="8880f-109">Both should not be specified simultaneously in a PrintTicket or Print Capabilities document.</span></span>

-   [<span data-ttu-id="8880f-110">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="8880f-110">Element Information</span></span>](#element-information)

-   [<span data-ttu-id="8880f-111">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="8880f-111">Structural Content</span></span>](#structural-content)

-   [<span data-ttu-id="8880f-112">Contenu XML</span><span class="sxs-lookup"><span data-stu-id="8880f-112">XML Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="8880f-113">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="8880f-113">Element Information</span></span>



| <span data-ttu-id="8880f-114">Nom</span><span class="sxs-lookup"><span data-stu-id="8880f-114">Name</span></span>                       |                                                                                                                                |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8880f-115">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="8880f-115">Element Type</span></span> <br/>   | <span data-ttu-id="8880f-116">Fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="8880f-116">Feature</span></span><br/>                                                                                                             |
| <span data-ttu-id="8880f-117">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="8880f-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="8880f-118">Document</span><span class="sxs-lookup"><span data-stu-id="8880f-118">Document</span></span><br/>                                                                                                            |
| <span data-ttu-id="8880f-119">Notes</span><span class="sxs-lookup"><span data-stu-id="8880f-119">Notes</span></span> <br/>          | <span data-ttu-id="8880f-120">Les emplacements pris en charge qui ne sont pas installés actuellement doivent être signalés comme étant limités dans le document PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="8880f-120">Supported bins that are not currently installed should be flagged as constrained in the PrintCapabilities document.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="8880f-121">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="8880f-121">Structural Content</span></span>

<span data-ttu-id="8880f-122">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="8880f-122">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="8880f-123">Variables de structure</span><span class="sxs-lookup"><span data-stu-id="8880f-123">Structure Variables</span></span>

<span data-ttu-id="8880f-124">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="8880f-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="8880f-125">Nom</span><span class="sxs-lookup"><span data-stu-id="8880f-125">Name</span></span>                                   | <span data-ttu-id="8880f-126">Type de données</span><span class="sxs-lookup"><span data-stu-id="8880f-126">Data type</span></span>          | <span data-ttu-id="8880f-127">Unité</span><span class="sxs-lookup"><span data-stu-id="8880f-127">Unit</span></span>                  | <span data-ttu-id="8880f-128">Valeurs prises en charge</span><span class="sxs-lookup"><span data-stu-id="8880f-128">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="8880f-129">Résumé</span><span class="sxs-lookup"><span data-stu-id="8880f-129">Summary</span></span>                                                                             |
|----------------------------------------|--------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="8880f-130">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="8880f-130">\_OptionName\_</span></span><br/>              | <span data-ttu-id="8880f-131">string</span><span class="sxs-lookup"><span data-stu-id="8880f-131">string</span></span><br/>  | <span data-ttu-id="8880f-132">caractères</span><span class="sxs-lookup"><span data-stu-id="8880f-132">characters</span></span><br/> | <span data-ttu-id="8880f-133">Nom complet valide tel que défini par les [espaces de noms dans XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="8880f-133">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="8880f-134">Si aucun espace de noms n’est spécifié, l’espace de noms par défaut est utilisé.</span><span class="sxs-lookup"><span data-stu-id="8880f-134">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="8880f-135">Nom de l'option.</span><span class="sxs-lookup"><span data-stu-id="8880f-135">The name of the option.</span></span><br/>                                                  |
| <span data-ttu-id="8880f-136">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="8880f-136">\_IdentityOptionValue\_</span></span><br/>     | <span data-ttu-id="8880f-137">string</span><span class="sxs-lookup"><span data-stu-id="8880f-137">string</span></span><br/>  | <span data-ttu-id="8880f-138">n/a</span><span class="sxs-lookup"><span data-stu-id="8880f-138">n/a</span></span><br/>        | <span data-ttu-id="8880f-139">True, False.</span><span class="sxs-lookup"><span data-stu-id="8880f-139">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="8880f-140">Définit une option qui, lorsqu’elle est sélectionnée, désactive cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="8880f-140">Defines an Option which when selected would disable this feature.</span></span><br/>        |
| <span data-ttu-id="8880f-141">\_EnvelopeOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="8880f-141">\_EnvelopeOptionValue\_</span></span><br/>     | <span data-ttu-id="8880f-142">string</span><span class="sxs-lookup"><span data-stu-id="8880f-142">string</span></span><br/>  | <span data-ttu-id="8880f-143">n/a</span><span class="sxs-lookup"><span data-stu-id="8880f-143">n/a</span></span><br/>        | <span data-ttu-id="8880f-144">True, False.</span><span class="sxs-lookup"><span data-stu-id="8880f-144">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="8880f-145">Définit une option qui, lorsqu’elle est sélectionnée, désactive cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="8880f-145">Defines an Option which when selected would disable this feature.</span></span><br/>        |
| <span data-ttu-id="8880f-146">\_BinTypeValue\_</span><span class="sxs-lookup"><span data-stu-id="8880f-146">\_BinTypeValue\_</span></span><br/>            | <span data-ttu-id="8880f-147">string</span><span class="sxs-lookup"><span data-stu-id="8880f-147">string</span></span><br/>  | <span data-ttu-id="8880f-148">n/a</span><span class="sxs-lookup"><span data-stu-id="8880f-148">n/a</span></span><br/>        | <span data-ttu-id="8880f-149">ContinuousFeed, SheetFeed.</span><span class="sxs-lookup"><span data-stu-id="8880f-149">ContinuousFeed, SheetFeed.</span></span><br/>                                                                                                                                                 | <span data-ttu-id="8880f-150">Spécifie le type de l’emplacement.</span><span class="sxs-lookup"><span data-stu-id="8880f-150">Specifies the type of the bin.</span></span><br/>                                           |
| <span data-ttu-id="8880f-151">\_FeedTypeValue\_</span><span class="sxs-lookup"><span data-stu-id="8880f-151">\_FeedTypeValue\_</span></span><br/>           | <span data-ttu-id="8880f-152">string</span><span class="sxs-lookup"><span data-stu-id="8880f-152">string</span></span><br/>  | <span data-ttu-id="8880f-153">n/a</span><span class="sxs-lookup"><span data-stu-id="8880f-153">n/a</span></span><br/>        | <span data-ttu-id="8880f-154">Automatique, manuel.</span><span class="sxs-lookup"><span data-stu-id="8880f-154">Automatic, Manual.</span></span><br/>                                                                                                                                                         | <span data-ttu-id="8880f-155">Spécifie le mécanisme de flux de l’emplacement.</span><span class="sxs-lookup"><span data-stu-id="8880f-155">Specifies the feed mechanism of the bin.</span></span><br/>                                 |
| <span data-ttu-id="8880f-156">\_MediaCapacityValue\_</span><span class="sxs-lookup"><span data-stu-id="8880f-156">\_MediaCapacityValue\_</span></span><br/>      | <span data-ttu-id="8880f-157">entier</span><span class="sxs-lookup"><span data-stu-id="8880f-157">integer</span></span><br/> | <span data-ttu-id="8880f-158">feuilles</span><span class="sxs-lookup"><span data-stu-id="8880f-158">sheets</span></span><br/>     | <span data-ttu-id="8880f-159">Contrainte d’entier maximale autorisée par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="8880f-159">Maximum integer constraint allowed by device.</span></span><br/>                                                                                                                              | <span data-ttu-id="8880f-160">Spécifie si l’emplacement est un casier à capacité élevée (qualitatif).</span><span class="sxs-lookup"><span data-stu-id="8880f-160">Specifies whether the bin is a high capacity bin (qualitative).</span></span><br/>          |
| <span data-ttu-id="8880f-161">\_MediaSizeAutoSenseValue\_</span><span class="sxs-lookup"><span data-stu-id="8880f-161">\_MediaSizeAutoSenseValue\_</span></span><br/> | <span data-ttu-id="8880f-162">string</span><span class="sxs-lookup"><span data-stu-id="8880f-162">string</span></span><br/>  | <span data-ttu-id="8880f-163">n/a</span><span class="sxs-lookup"><span data-stu-id="8880f-163">n/a</span></span><br/>        | <span data-ttu-id="8880f-164">Pris en charge, aucun.</span><span class="sxs-lookup"><span data-stu-id="8880f-164">Supported, None.</span></span><br/>                                                                                                                                                           | <span data-ttu-id="8880f-165">Spécifie la fonctionnalité de détection automatique de la taille du média de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="8880f-165">Specifies the media size auto sense capability of the device.</span></span><br/>            |
| <span data-ttu-id="8880f-166">\_MediaTypeAutoSenseValue\_</span><span class="sxs-lookup"><span data-stu-id="8880f-166">\_MediaTypeAutoSenseValue\_</span></span><br/> | <span data-ttu-id="8880f-167">string</span><span class="sxs-lookup"><span data-stu-id="8880f-167">string</span></span><br/>  | <span data-ttu-id="8880f-168">n/a</span><span class="sxs-lookup"><span data-stu-id="8880f-168">n/a</span></span><br/>        | <span data-ttu-id="8880f-169">Pris en charge, aucun.</span><span class="sxs-lookup"><span data-stu-id="8880f-169">Supported, None.</span></span><br/>                                                                                                                                                           | <span data-ttu-id="8880f-170">Spécifie la capacité du média en nombre de pages (au niveau complet) de l’emplacement.</span><span class="sxs-lookup"><span data-stu-id="8880f-170">Specifies the media capacity in number of pages (full level) of the bin.</span></span><br/> |
| <span data-ttu-id="8880f-171">\_MediaPathValue\_</span><span class="sxs-lookup"><span data-stu-id="8880f-171">\_MediaPathValue\_</span></span><br/>          | <span data-ttu-id="8880f-172">string</span><span class="sxs-lookup"><span data-stu-id="8880f-172">string</span></span><br/>  | <span data-ttu-id="8880f-173">n/a</span><span class="sxs-lookup"><span data-stu-id="8880f-173">n/a</span></span><br/>        | <span data-ttu-id="8880f-174">Droit, en serpentin.</span><span class="sxs-lookup"><span data-stu-id="8880f-174">Straight, Serpentine.</span></span><br/>                                                                                                                                                      | <span data-ttu-id="8880f-175">Spécifie les caractéristiques du chemin d’accès du média.</span><span class="sxs-lookup"><span data-stu-id="8880f-175">Specifies the characteristics of the media path.</span></span><br/>                         |
| <span data-ttu-id="8880f-176">\_FeedFaceValue\_</span><span class="sxs-lookup"><span data-stu-id="8880f-176">\_FeedFaceValue\_</span></span><br/>           | <span data-ttu-id="8880f-177">string</span><span class="sxs-lookup"><span data-stu-id="8880f-177">string</span></span><br/>  | <span data-ttu-id="8880f-178">n/a</span><span class="sxs-lookup"><span data-stu-id="8880f-178">n/a</span></span><br/>        | <span data-ttu-id="8880f-179">FaceUp, FaceDown</span><span class="sxs-lookup"><span data-stu-id="8880f-179">FaceUp, FaceDown</span></span><br/>                                                                                                                                                           | <span data-ttu-id="8880f-180">Spécifie si le média doit être imprimé vers le haut ou vers le haut.</span><span class="sxs-lookup"><span data-stu-id="8880f-180">Specifies whether media is to be printed face up or face down.</span></span><br/>           |
| <span data-ttu-id="8880f-181">\_FeedDirectionValue\_</span><span class="sxs-lookup"><span data-stu-id="8880f-181">\_FeedDirectionValue\_</span></span><br/>      | <span data-ttu-id="8880f-182">string</span><span class="sxs-lookup"><span data-stu-id="8880f-182">string</span></span><br/>  | <span data-ttu-id="8880f-183">n/a</span><span class="sxs-lookup"><span data-stu-id="8880f-183">n/a</span></span><br/>        | <span data-ttu-id="8880f-184">LongEdgeFirst, ShortEdgeFirst</span><span class="sxs-lookup"><span data-stu-id="8880f-184">LongEdgeFirst, ShortEdgeFirst</span></span><br/>                                                                                                                                              | <span data-ttu-id="8880f-185">Spécifie si le média est alimenté en premier ou à l’extrémité du long bord.</span><span class="sxs-lookup"><span data-stu-id="8880f-185">Specifies whether media is fed long edge first or short edge first.</span></span><br/>      |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="8880f-186">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="8880f-186">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="8880f-187">Les mots clés de schéma d’impression publics sont définis dans l' https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords espace de noms.</span><span class="sxs-lookup"><span data-stu-id="8880f-187">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="8880f-188">Le contenu de la Extensible Markup Language publique (XML) pour ce mot clé est défini ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="8880f-188">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="8880f-189">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8880f-189">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8880f-190">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="8880f-190">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




