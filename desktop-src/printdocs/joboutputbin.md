---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: 324ec426-b7c8-43af-96b9-74929358e262
title: JobOutputBin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 973433ac7f6e051d4656777696cc3a37cedd953b
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107999216"
---
# <a name="joboutputbin"></a><span data-ttu-id="e362c-104">JobOutputBin</span><span class="sxs-lookup"><span data-stu-id="e362c-104">JobOutputBin</span></span>

<span data-ttu-id="e362c-105">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="e362c-105">This topic is not current.</span></span> <span data-ttu-id="e362c-106">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="e362c-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="e362c-107">Décrit le bac de sortie installé sur un appareil ou la liste complète des emplacements pris en charge pour un appareil.</span><span class="sxs-lookup"><span data-stu-id="e362c-107">Describes the installed output bin in a device or the full list of supported bins for a device.</span></span> <span data-ttu-id="e362c-108">Les mots clés JobOutputBin, DocumentOutputBin et PageOutputBin s’excluent mutuellement, un seul doit être spécifié dans un document PrintTicket ou des fonctionnalités d’impression.</span><span class="sxs-lookup"><span data-stu-id="e362c-108">The JobOutputBin, DocumentOutputBin and PageOutputBin keywords are mutually exclusive only one should be specified in a PrintTicket or Print Capabilities document.</span></span>

-   [<span data-ttu-id="e362c-109">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="e362c-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="e362c-110">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="e362c-110">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="e362c-111">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="e362c-111">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="e362c-112">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="e362c-112">Element Information</span></span>



| <span data-ttu-id="e362c-113">Nom</span><span class="sxs-lookup"><span data-stu-id="e362c-113">Name</span></span> | <span data-ttu-id="e362c-114">Value</span><span class="sxs-lookup"><span data-stu-id="e362c-114">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="e362c-115">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="e362c-115">Element Type</span></span> <br/>   | <span data-ttu-id="e362c-116">Fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="e362c-116">Feature</span></span><br/> |
| <span data-ttu-id="e362c-117">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="e362c-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="e362c-118">Travail</span><span class="sxs-lookup"><span data-stu-id="e362c-118">Job</span></span><br/>     |
| <span data-ttu-id="e362c-119">Notes</span><span class="sxs-lookup"><span data-stu-id="e362c-119">Notes</span></span> <br/>          | <span data-ttu-id="e362c-120">Aucun</span><span class="sxs-lookup"><span data-stu-id="e362c-120">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="e362c-121">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="e362c-121">Structural Content</span></span>

<span data-ttu-id="e362c-122">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="e362c-122">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="e362c-123">Variables de structure</span><span class="sxs-lookup"><span data-stu-id="e362c-123">Structure Variables</span></span>

<span data-ttu-id="e362c-124">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="e362c-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="e362c-125">Nom</span><span class="sxs-lookup"><span data-stu-id="e362c-125">Name</span></span>                                   | <span data-ttu-id="e362c-126">Type de données</span><span class="sxs-lookup"><span data-stu-id="e362c-126">Data type</span></span>          | <span data-ttu-id="e362c-127">Unité</span><span class="sxs-lookup"><span data-stu-id="e362c-127">Unit</span></span>                  | <span data-ttu-id="e362c-128">Valeurs prises en charge</span><span class="sxs-lookup"><span data-stu-id="e362c-128">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="e362c-129">Résumé</span><span class="sxs-lookup"><span data-stu-id="e362c-129">Summary</span></span>                                                                             |
|----------------------------------------|--------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="e362c-130">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="e362c-130">\_OptionName\_</span></span><br/>              | <span data-ttu-id="e362c-131">string</span><span class="sxs-lookup"><span data-stu-id="e362c-131">string</span></span><br/>  | <span data-ttu-id="e362c-132">caractères</span><span class="sxs-lookup"><span data-stu-id="e362c-132">characters</span></span><br/> | <span data-ttu-id="e362c-133">Nom complet valide tel que défini par les [espaces de noms dans XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="e362c-133">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="e362c-134">Si aucun espace de noms n’est spécifié, l’espace de noms par défaut est utilisé.</span><span class="sxs-lookup"><span data-stu-id="e362c-134">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="e362c-135">Nom de l'option.</span><span class="sxs-lookup"><span data-stu-id="e362c-135">The name of the option.</span></span><br/>                                                  |
| <span data-ttu-id="e362c-136">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="e362c-136">\_IdentityOptionValue\_</span></span><br/>     | <span data-ttu-id="e362c-137">string</span><span class="sxs-lookup"><span data-stu-id="e362c-137">string</span></span><br/>  | <span data-ttu-id="e362c-138">n/a</span><span class="sxs-lookup"><span data-stu-id="e362c-138">n/a</span></span><br/>        | <span data-ttu-id="e362c-139">True, False.</span><span class="sxs-lookup"><span data-stu-id="e362c-139">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="e362c-140">Définit une option qui, lorsqu’elle est sélectionnée, désactive cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="e362c-140">Defines an Option which when selected would disable this feature.</span></span><br/>        |
| <span data-ttu-id="e362c-141">\_BinTypeValue\_</span><span class="sxs-lookup"><span data-stu-id="e362c-141">\_BinTypeValue\_</span></span><br/>            | <span data-ttu-id="e362c-142">string</span><span class="sxs-lookup"><span data-stu-id="e362c-142">string</span></span><br/>  | <span data-ttu-id="e362c-143">n/a</span><span class="sxs-lookup"><span data-stu-id="e362c-143">n/a</span></span><br/>        | <span data-ttu-id="e362c-144">Boîte aux lettres, trieuse, stacker, finisseur, aucun.</span><span class="sxs-lookup"><span data-stu-id="e362c-144">MailBox, Sorter, Stacker, Finisher, None.</span></span><br/>                                                                                                                                  | <span data-ttu-id="e362c-145">Spécifie le type général de l’emplacement.</span><span class="sxs-lookup"><span data-stu-id="e362c-145">Specifies the general type of the bin.</span></span><br/>                                   |
| <span data-ttu-id="e362c-146">\_MediaSheetCapacityValue\_</span><span class="sxs-lookup"><span data-stu-id="e362c-146">\_MediaSheetCapacityValue\_</span></span><br/> | <span data-ttu-id="e362c-147">entier</span><span class="sxs-lookup"><span data-stu-id="e362c-147">integer</span></span><br/> | <span data-ttu-id="e362c-148">feuilles</span><span class="sxs-lookup"><span data-stu-id="e362c-148">sheets</span></span><br/>     | <span data-ttu-id="e362c-149">Contrainte d’entier maximale autorisée par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="e362c-149">Maximum integer constraint allowed by device.</span></span><br/>                                                                                                                              | <span data-ttu-id="e362c-150">Spécifie la capacité du média en nombre de pages (au niveau complet) de l’emplacement.</span><span class="sxs-lookup"><span data-stu-id="e362c-150">Specifies the Media capacity in number of pages (full level) of the bin.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="e362c-151">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="e362c-151">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="e362c-152">Les mots clés de schéma d’impression publics sont définis dans l' https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords espace de noms.</span><span class="sxs-lookup"><span data-stu-id="e362c-152">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="e362c-153">Le contenu de la Extensible Markup Language publique (XML) pour ce mot clé est défini ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="e362c-153">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="e362c-154">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e362c-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e362c-155">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="e362c-155">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




