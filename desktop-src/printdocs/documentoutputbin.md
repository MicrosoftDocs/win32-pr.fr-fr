---
description: En savoir plus sur DocumentOutputBin, qui décrit la liste complète des emplacements pris en charge pour l’appareil et permet la spécification du bac de sortie par document.
ms.assetid: 73840548-f68b-4af8-acb4-6f7faa2e8879
title: DocumentOutputBin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2afc20f15aed8d3076afb79d755c54791573b393
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409242"
---
# <a name="documentoutputbin"></a><span data-ttu-id="0a02a-103">DocumentOutputBin</span><span class="sxs-lookup"><span data-stu-id="0a02a-103">DocumentOutputBin</span></span>

<span data-ttu-id="0a02a-104">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="0a02a-104">This topic is not current.</span></span> <span data-ttu-id="0a02a-105">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="0a02a-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="0a02a-106">Décrit la liste complète des emplacements pris en charge pour l’appareil.</span><span class="sxs-lookup"><span data-stu-id="0a02a-106">Describes the full list of supported bins for the device.</span></span> <span data-ttu-id="0a02a-107">Autorise la spécification du bac de sortie par document.</span><span class="sxs-lookup"><span data-stu-id="0a02a-107">Allows specification of output bin on a per document basis.</span></span> <span data-ttu-id="0a02a-108">Les mots clés JobOutputBin, DocumentOutputBin et PageOutputBin s’excluent mutuellement, un seul doit être spécifié dans un document PrintTicket ou des fonctionnalités d’impression.</span><span class="sxs-lookup"><span data-stu-id="0a02a-108">The JobOutputBin, DocumentOutputBin and PageOutputBin keywords are mutually exclusive only one should be specified in a PrintTicket or Print Capabilities document.</span></span>

-   [<span data-ttu-id="0a02a-109">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="0a02a-109">Element Information</span></span>](#element-information)

-   [<span data-ttu-id="0a02a-110">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="0a02a-110">Structural Content</span></span>](#structural-content)

-   [<span data-ttu-id="0a02a-111">Contenu XML</span><span class="sxs-lookup"><span data-stu-id="0a02a-111">XML Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="0a02a-112">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="0a02a-112">Element Information</span></span>



| <span data-ttu-id="0a02a-113">Nom</span><span class="sxs-lookup"><span data-stu-id="0a02a-113">Name</span></span> | <span data-ttu-id="0a02a-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="0a02a-114">Value</span></span> |
|----------------------------|---------------------|
| <span data-ttu-id="0a02a-115">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="0a02a-115">Element Type</span></span> <br/>   | <span data-ttu-id="0a02a-116">Fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="0a02a-116">Feature</span></span><br/>  |
| <span data-ttu-id="0a02a-117">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="0a02a-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="0a02a-118">Document</span><span class="sxs-lookup"><span data-stu-id="0a02a-118">Document</span></span><br/> |
| <span data-ttu-id="0a02a-119">Notes</span><span class="sxs-lookup"><span data-stu-id="0a02a-119">Notes</span></span> <br/>          | <span data-ttu-id="0a02a-120">Aucun</span><span class="sxs-lookup"><span data-stu-id="0a02a-120">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="0a02a-121">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="0a02a-121">Structural Content</span></span>

<span data-ttu-id="0a02a-122">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="0a02a-122">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:DocumentOutputBin">
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

## <a name="structure-variables"></a><span data-ttu-id="0a02a-123">Variables de structure</span><span class="sxs-lookup"><span data-stu-id="0a02a-123">Structure Variables</span></span>

<span data-ttu-id="0a02a-124">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="0a02a-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="0a02a-125">Nom</span><span class="sxs-lookup"><span data-stu-id="0a02a-125">Name</span></span>                                   | <span data-ttu-id="0a02a-126">Type de données</span><span class="sxs-lookup"><span data-stu-id="0a02a-126">Data type</span></span>          | <span data-ttu-id="0a02a-127">Unité</span><span class="sxs-lookup"><span data-stu-id="0a02a-127">Unit</span></span>                  | <span data-ttu-id="0a02a-128">Valeurs prises en charge</span><span class="sxs-lookup"><span data-stu-id="0a02a-128">Supported values</span></span>                                                                                                                                                             | <span data-ttu-id="0a02a-129">Résumé</span><span class="sxs-lookup"><span data-stu-id="0a02a-129">Summary</span></span>                                                                             |
|----------------------------------------|--------------------|-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="0a02a-130">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="0a02a-130">\_OptionName\_</span></span><br/>              | <span data-ttu-id="0a02a-131">string</span><span class="sxs-lookup"><span data-stu-id="0a02a-131">string</span></span><br/>  | <span data-ttu-id="0a02a-132">caractères</span><span class="sxs-lookup"><span data-stu-id="0a02a-132">characters</span></span><br/> | <span data-ttu-id="0a02a-133">Nom complet valide tel que défini par https://www.w3.org/TR/1999/REC-xml-names-19990114/\#dt-qname .</span><span class="sxs-lookup"><span data-stu-id="0a02a-133">Valid fully qualified name as defined by https://www.w3.org/TR/1999/REC-xml-names-19990114/\#dt-qname.</span></span> <span data-ttu-id="0a02a-134">Si aucun espace de noms n’est spécifié, l’espace de noms par défaut est utilisé.</span><span class="sxs-lookup"><span data-stu-id="0a02a-134">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="0a02a-135">Nom de l'option.</span><span class="sxs-lookup"><span data-stu-id="0a02a-135">The name of the option.</span></span><br/>                                                  |
| <span data-ttu-id="0a02a-136">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="0a02a-136">\_IdentityOptionValue\_</span></span><br/>     | <span data-ttu-id="0a02a-137">string</span><span class="sxs-lookup"><span data-stu-id="0a02a-137">string</span></span><br/>  | <span data-ttu-id="0a02a-138">n/a</span><span class="sxs-lookup"><span data-stu-id="0a02a-138">n/a</span></span><br/>        | <span data-ttu-id="0a02a-139">True, False.</span><span class="sxs-lookup"><span data-stu-id="0a02a-139">True, False.</span></span><br/>                                                                                                                                                      | <span data-ttu-id="0a02a-140">Définit une option qui, lorsqu’elle est sélectionnée, désactive cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="0a02a-140">Defines an Option which when selected would disable this feature.</span></span><br/>        |
| <span data-ttu-id="0a02a-141">\_BinTypeValue\_</span><span class="sxs-lookup"><span data-stu-id="0a02a-141">\_BinTypeValue\_</span></span><br/>            | <span data-ttu-id="0a02a-142">string</span><span class="sxs-lookup"><span data-stu-id="0a02a-142">string</span></span><br/>  | <span data-ttu-id="0a02a-143">n/a</span><span class="sxs-lookup"><span data-stu-id="0a02a-143">n/a</span></span><br/>        | <span data-ttu-id="0a02a-144">Boîte aux lettres, trieuse, stacker, finisseur, aucun.</span><span class="sxs-lookup"><span data-stu-id="0a02a-144">MailBox, Sorter, Stacker, Finisher, None.</span></span><br/>                                                                                                                         | <span data-ttu-id="0a02a-145">Spécifie le type général de l’emplacement.</span><span class="sxs-lookup"><span data-stu-id="0a02a-145">Specifies the general type of the bin.</span></span><br/>                                   |
| <span data-ttu-id="0a02a-146">\_MediaSheetCapacityValue\_</span><span class="sxs-lookup"><span data-stu-id="0a02a-146">\_MediaSheetCapacityValue\_</span></span><br/> | <span data-ttu-id="0a02a-147">entier</span><span class="sxs-lookup"><span data-stu-id="0a02a-147">integer</span></span><br/> | <span data-ttu-id="0a02a-148">feuilles</span><span class="sxs-lookup"><span data-stu-id="0a02a-148">sheets</span></span><br/>     | <span data-ttu-id="0a02a-149">Supérieur à 0.</span><span class="sxs-lookup"><span data-stu-id="0a02a-149">Greater than 0.</span></span><br/>                                                                                                                                                   | <span data-ttu-id="0a02a-150">Spécifie la capacité du média en nombre de pages (au niveau complet) de l’emplacement.</span><span class="sxs-lookup"><span data-stu-id="0a02a-150">Specifies the Media capacity in number of pages (full level) of the bin.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="0a02a-151">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="0a02a-151">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="0a02a-152">Les mots clés de schéma d’impression publics sont définis dans l' https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords espace de noms.</span><span class="sxs-lookup"><span data-stu-id="0a02a-152">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="0a02a-153">Le contenu de la Extensible Markup Language publique (XML) pour ce mot clé est défini ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="0a02a-153">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:DocumentOutputBin">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option>
    <!--Specifies type of output bin-->
    <psf:ScoredProperty name="psk:BinType">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <!--Specifies media capacity for output bin-->
    <psf:ScoredProperty name="psk:MediaSheetCapacity">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>    
```

## <a name="related-topics"></a><span data-ttu-id="0a02a-154">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0a02a-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0a02a-155">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="0a02a-155">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




