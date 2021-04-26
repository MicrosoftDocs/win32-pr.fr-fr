---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: 73840548-f68b-4af8-acb4-6f7faa2e8879
title: DocumentOutputBin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96f6d16ca000e76b01cd2c3165054d7acc81351b
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997136"
---
# <a name="documentoutputbin"></a><span data-ttu-id="56b9a-104">DocumentOutputBin</span><span class="sxs-lookup"><span data-stu-id="56b9a-104">DocumentOutputBin</span></span>

<span data-ttu-id="56b9a-105">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="56b9a-105">This topic is not current.</span></span> <span data-ttu-id="56b9a-106">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="56b9a-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="56b9a-107">Décrit la liste complète des emplacements pris en charge pour l’appareil.</span><span class="sxs-lookup"><span data-stu-id="56b9a-107">Describes the full list of supported bins for the device.</span></span> <span data-ttu-id="56b9a-108">Autorise la spécification du bac de sortie par document.</span><span class="sxs-lookup"><span data-stu-id="56b9a-108">Allows specification of output bin on a per document basis.</span></span> <span data-ttu-id="56b9a-109">Les mots clés JobOutputBin, DocumentOutputBin et PageOutputBin s’excluent mutuellement, un seul doit être spécifié dans un document PrintTicket ou des fonctionnalités d’impression.</span><span class="sxs-lookup"><span data-stu-id="56b9a-109">The JobOutputBin, DocumentOutputBin and PageOutputBin keywords are mutually exclusive only one should be specified in a PrintTicket or Print Capabilities document.</span></span>

-   [<span data-ttu-id="56b9a-110">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="56b9a-110">Element Information</span></span>](#element-information)

-   [<span data-ttu-id="56b9a-111">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="56b9a-111">Structural Content</span></span>](#structural-content)

-   [<span data-ttu-id="56b9a-112">Contenu XML</span><span class="sxs-lookup"><span data-stu-id="56b9a-112">XML Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="56b9a-113">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="56b9a-113">Element Information</span></span>



| <span data-ttu-id="56b9a-114">Nom</span><span class="sxs-lookup"><span data-stu-id="56b9a-114">Name</span></span> | <span data-ttu-id="56b9a-115">Value</span><span class="sxs-lookup"><span data-stu-id="56b9a-115">Value</span></span> |
|----------------------------|---------------------|
| <span data-ttu-id="56b9a-116">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="56b9a-116">Element Type</span></span> <br/>   | <span data-ttu-id="56b9a-117">Fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="56b9a-117">Feature</span></span><br/>  |
| <span data-ttu-id="56b9a-118">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="56b9a-118">Scoping Prefix</span></span> <br/> | <span data-ttu-id="56b9a-119">Document</span><span class="sxs-lookup"><span data-stu-id="56b9a-119">Document</span></span><br/> |
| <span data-ttu-id="56b9a-120">Notes</span><span class="sxs-lookup"><span data-stu-id="56b9a-120">Notes</span></span> <br/>          | <span data-ttu-id="56b9a-121">Aucun</span><span class="sxs-lookup"><span data-stu-id="56b9a-121">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="56b9a-122">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="56b9a-122">Structural Content</span></span>

<span data-ttu-id="56b9a-123">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="56b9a-123">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="56b9a-124">Variables de structure</span><span class="sxs-lookup"><span data-stu-id="56b9a-124">Structure Variables</span></span>

<span data-ttu-id="56b9a-125">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="56b9a-125">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="56b9a-126">Nom</span><span class="sxs-lookup"><span data-stu-id="56b9a-126">Name</span></span>                                   | <span data-ttu-id="56b9a-127">Type de données</span><span class="sxs-lookup"><span data-stu-id="56b9a-127">Data type</span></span>          | <span data-ttu-id="56b9a-128">Unité</span><span class="sxs-lookup"><span data-stu-id="56b9a-128">Unit</span></span>                  | <span data-ttu-id="56b9a-129">Valeurs prises en charge</span><span class="sxs-lookup"><span data-stu-id="56b9a-129">Supported values</span></span>                                                                                                                                                             | <span data-ttu-id="56b9a-130">Résumé</span><span class="sxs-lookup"><span data-stu-id="56b9a-130">Summary</span></span>                                                                             |
|----------------------------------------|--------------------|-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="56b9a-131">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="56b9a-131">\_OptionName\_</span></span><br/>              | <span data-ttu-id="56b9a-132">string</span><span class="sxs-lookup"><span data-stu-id="56b9a-132">string</span></span><br/>  | <span data-ttu-id="56b9a-133">caractères</span><span class="sxs-lookup"><span data-stu-id="56b9a-133">characters</span></span><br/> | <span data-ttu-id="56b9a-134">Nom complet valide tel que défini par https://www.w3.org/TR/1999/REC-xml-names-19990114/\#dt-qname .</span><span class="sxs-lookup"><span data-stu-id="56b9a-134">Valid fully qualified name as defined by https://www.w3.org/TR/1999/REC-xml-names-19990114/\#dt-qname.</span></span> <span data-ttu-id="56b9a-135">Si aucun espace de noms n’est spécifié, l’espace de noms par défaut est utilisé.</span><span class="sxs-lookup"><span data-stu-id="56b9a-135">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="56b9a-136">Nom de l'option.</span><span class="sxs-lookup"><span data-stu-id="56b9a-136">The name of the option.</span></span><br/>                                                  |
| <span data-ttu-id="56b9a-137">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="56b9a-137">\_IdentityOptionValue\_</span></span><br/>     | <span data-ttu-id="56b9a-138">string</span><span class="sxs-lookup"><span data-stu-id="56b9a-138">string</span></span><br/>  | <span data-ttu-id="56b9a-139">n/a</span><span class="sxs-lookup"><span data-stu-id="56b9a-139">n/a</span></span><br/>        | <span data-ttu-id="56b9a-140">True, False.</span><span class="sxs-lookup"><span data-stu-id="56b9a-140">True, False.</span></span><br/>                                                                                                                                                      | <span data-ttu-id="56b9a-141">Définit une option qui, lorsqu’elle est sélectionnée, désactive cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="56b9a-141">Defines an Option which when selected would disable this feature.</span></span><br/>        |
| <span data-ttu-id="56b9a-142">\_BinTypeValue\_</span><span class="sxs-lookup"><span data-stu-id="56b9a-142">\_BinTypeValue\_</span></span><br/>            | <span data-ttu-id="56b9a-143">string</span><span class="sxs-lookup"><span data-stu-id="56b9a-143">string</span></span><br/>  | <span data-ttu-id="56b9a-144">n/a</span><span class="sxs-lookup"><span data-stu-id="56b9a-144">n/a</span></span><br/>        | <span data-ttu-id="56b9a-145">Boîte aux lettres, trieuse, stacker, finisseur, aucun.</span><span class="sxs-lookup"><span data-stu-id="56b9a-145">MailBox, Sorter, Stacker, Finisher, None.</span></span><br/>                                                                                                                         | <span data-ttu-id="56b9a-146">Spécifie le type général de l’emplacement.</span><span class="sxs-lookup"><span data-stu-id="56b9a-146">Specifies the general type of the bin.</span></span><br/>                                   |
| <span data-ttu-id="56b9a-147">\_MediaSheetCapacityValue\_</span><span class="sxs-lookup"><span data-stu-id="56b9a-147">\_MediaSheetCapacityValue\_</span></span><br/> | <span data-ttu-id="56b9a-148">entier</span><span class="sxs-lookup"><span data-stu-id="56b9a-148">integer</span></span><br/> | <span data-ttu-id="56b9a-149">feuilles</span><span class="sxs-lookup"><span data-stu-id="56b9a-149">sheets</span></span><br/>     | <span data-ttu-id="56b9a-150">Supérieur à 0.</span><span class="sxs-lookup"><span data-stu-id="56b9a-150">Greater than 0.</span></span><br/>                                                                                                                                                   | <span data-ttu-id="56b9a-151">Spécifie la capacité du média en nombre de pages (au niveau complet) de l’emplacement.</span><span class="sxs-lookup"><span data-stu-id="56b9a-151">Specifies the Media capacity in number of pages (full level) of the bin.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="56b9a-152">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="56b9a-152">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="56b9a-153">Les mots clés de schéma d’impression publics sont définis dans l' https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords espace de noms.</span><span class="sxs-lookup"><span data-stu-id="56b9a-153">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="56b9a-154">Le contenu de la Extensible Markup Language publique (XML) pour ce mot clé est défini ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="56b9a-154">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="56b9a-155">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="56b9a-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="56b9a-156">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="56b9a-156">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




