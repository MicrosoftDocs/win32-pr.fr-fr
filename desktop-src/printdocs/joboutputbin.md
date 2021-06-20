---
description: En savoir plus sur l’élément JobOutputBin, qui décrit le bac de sortie installé dans un appareil ou la liste complète des emplacements pris en charge pour un appareil.
ms.assetid: 324ec426-b7c8-43af-96b9-74929358e262
title: JobOutputBin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1243e9409f781b8babde6d6310ce7a2b083f8703
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408852"
---
# <a name="joboutputbin"></a><span data-ttu-id="a56fc-103">JobOutputBin</span><span class="sxs-lookup"><span data-stu-id="a56fc-103">JobOutputBin</span></span>

<span data-ttu-id="a56fc-104">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="a56fc-104">This topic is not current.</span></span> <span data-ttu-id="a56fc-105">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="a56fc-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="a56fc-106">Décrit le bac de sortie installé sur un appareil ou la liste complète des emplacements pris en charge pour un appareil.</span><span class="sxs-lookup"><span data-stu-id="a56fc-106">Describes the installed output bin in a device or the full list of supported bins for a device.</span></span> <span data-ttu-id="a56fc-107">Les mots clés JobOutputBin, DocumentOutputBin et PageOutputBin s’excluent mutuellement, un seul doit être spécifié dans un document PrintTicket ou des fonctionnalités d’impression.</span><span class="sxs-lookup"><span data-stu-id="a56fc-107">The JobOutputBin, DocumentOutputBin and PageOutputBin keywords are mutually exclusive only one should be specified in a PrintTicket or Print Capabilities document.</span></span>

-   [<span data-ttu-id="a56fc-108">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="a56fc-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="a56fc-109">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="a56fc-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="a56fc-110">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="a56fc-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="a56fc-111">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="a56fc-111">Element Information</span></span>



| <span data-ttu-id="a56fc-112">Nom</span><span class="sxs-lookup"><span data-stu-id="a56fc-112">Name</span></span> | <span data-ttu-id="a56fc-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="a56fc-113">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="a56fc-114">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="a56fc-114">Element Type</span></span> <br/>   | <span data-ttu-id="a56fc-115">Fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="a56fc-115">Feature</span></span><br/> |
| <span data-ttu-id="a56fc-116">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="a56fc-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="a56fc-117">Travail</span><span class="sxs-lookup"><span data-stu-id="a56fc-117">Job</span></span><br/>     |
| <span data-ttu-id="a56fc-118">Notes</span><span class="sxs-lookup"><span data-stu-id="a56fc-118">Notes</span></span> <br/>          | <span data-ttu-id="a56fc-119">Aucun</span><span class="sxs-lookup"><span data-stu-id="a56fc-119">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="a56fc-120">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="a56fc-120">Structural Content</span></span>

<span data-ttu-id="a56fc-121">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="a56fc-121">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:JobOutputBin">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <psf:ScoredProperty name="psk:BinType">
      <psf:Value xsi:type="xs:string">_BinTypeValue_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSheetCapacity">
      <psf:Value xsi:type="xs:integer">_MediaSheetCapacityValue_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
      
```

## <a name="structure-variables"></a><span data-ttu-id="a56fc-122">Variables de structure</span><span class="sxs-lookup"><span data-stu-id="a56fc-122">Structure Variables</span></span>

<span data-ttu-id="a56fc-123">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="a56fc-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="a56fc-124">Nom</span><span class="sxs-lookup"><span data-stu-id="a56fc-124">Name</span></span>                                   | <span data-ttu-id="a56fc-125">Type de données</span><span class="sxs-lookup"><span data-stu-id="a56fc-125">Data type</span></span>          | <span data-ttu-id="a56fc-126">Unité</span><span class="sxs-lookup"><span data-stu-id="a56fc-126">Unit</span></span>                  | <span data-ttu-id="a56fc-127">Valeurs prises en charge</span><span class="sxs-lookup"><span data-stu-id="a56fc-127">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="a56fc-128">Résumé</span><span class="sxs-lookup"><span data-stu-id="a56fc-128">Summary</span></span>                                                                             |
|----------------------------------------|--------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="a56fc-129">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="a56fc-129">\_OptionName\_</span></span><br/>              | <span data-ttu-id="a56fc-130">string</span><span class="sxs-lookup"><span data-stu-id="a56fc-130">string</span></span><br/>  | <span data-ttu-id="a56fc-131">caractères</span><span class="sxs-lookup"><span data-stu-id="a56fc-131">characters</span></span><br/> | <span data-ttu-id="a56fc-132">Nom complet valide tel que défini par les [espaces de noms dans XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="a56fc-132">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="a56fc-133">Si aucun espace de noms n’est spécifié, l’espace de noms par défaut est utilisé.</span><span class="sxs-lookup"><span data-stu-id="a56fc-133">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="a56fc-134">Nom de l'option.</span><span class="sxs-lookup"><span data-stu-id="a56fc-134">The name of the option.</span></span><br/>                                                  |
| <span data-ttu-id="a56fc-135">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="a56fc-135">\_IdentityOptionValue\_</span></span><br/>     | <span data-ttu-id="a56fc-136">string</span><span class="sxs-lookup"><span data-stu-id="a56fc-136">string</span></span><br/>  | <span data-ttu-id="a56fc-137">n/a</span><span class="sxs-lookup"><span data-stu-id="a56fc-137">n/a</span></span><br/>        | <span data-ttu-id="a56fc-138">True, False.</span><span class="sxs-lookup"><span data-stu-id="a56fc-138">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="a56fc-139">Définit une option qui, lorsqu’elle est sélectionnée, désactive cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="a56fc-139">Defines an Option which when selected would disable this feature.</span></span><br/>        |
| <span data-ttu-id="a56fc-140">\_BinTypeValue\_</span><span class="sxs-lookup"><span data-stu-id="a56fc-140">\_BinTypeValue\_</span></span><br/>            | <span data-ttu-id="a56fc-141">string</span><span class="sxs-lookup"><span data-stu-id="a56fc-141">string</span></span><br/>  | <span data-ttu-id="a56fc-142">n/a</span><span class="sxs-lookup"><span data-stu-id="a56fc-142">n/a</span></span><br/>        | <span data-ttu-id="a56fc-143">Boîte aux lettres, trieuse, stacker, finisseur, aucun.</span><span class="sxs-lookup"><span data-stu-id="a56fc-143">MailBox, Sorter, Stacker, Finisher, None.</span></span><br/>                                                                                                                                  | <span data-ttu-id="a56fc-144">Spécifie le type général de l’emplacement.</span><span class="sxs-lookup"><span data-stu-id="a56fc-144">Specifies the general type of the bin.</span></span><br/>                                   |
| <span data-ttu-id="a56fc-145">\_MediaSheetCapacityValue\_</span><span class="sxs-lookup"><span data-stu-id="a56fc-145">\_MediaSheetCapacityValue\_</span></span><br/> | <span data-ttu-id="a56fc-146">entier</span><span class="sxs-lookup"><span data-stu-id="a56fc-146">integer</span></span><br/> | <span data-ttu-id="a56fc-147">feuilles</span><span class="sxs-lookup"><span data-stu-id="a56fc-147">sheets</span></span><br/>     | <span data-ttu-id="a56fc-148">Contrainte d’entier maximale autorisée par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="a56fc-148">Maximum integer constraint allowed by device.</span></span><br/>                                                                                                                              | <span data-ttu-id="a56fc-149">Spécifie la capacité du média en nombre de pages (au niveau complet) de l’emplacement.</span><span class="sxs-lookup"><span data-stu-id="a56fc-149">Specifies the Media capacity in number of pages (full level) of the bin.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="a56fc-150">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="a56fc-150">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="a56fc-151">Les mots clés de schéma d’impression publics sont définis dans l' https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords espace de noms.</span><span class="sxs-lookup"><span data-stu-id="a56fc-151">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="a56fc-152">Le contenu de la Extensible Markup Language publique (XML) pour ce mot clé est défini ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="a56fc-152">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:JobOutputBin">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option>
    <psf:ScoredProperty name="psk:BinType">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>  
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSheetCapacity">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>  
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
    
```

## <a name="related-topics"></a><span data-ttu-id="a56fc-153">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a56fc-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a56fc-154">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="a56fc-154">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




