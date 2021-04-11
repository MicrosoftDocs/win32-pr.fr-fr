---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: c5050804-0e77-4d26-bf00-5d9690102b18
title: PageOutputBin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2bae72b69f83697cc2f482f21995acb587a2ace
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "104211360"
---
# <a name="pageoutputbin"></a><span data-ttu-id="1b50b-104">PageOutputBin</span><span class="sxs-lookup"><span data-stu-id="1b50b-104">PageOutputBin</span></span>

<span data-ttu-id="1b50b-105">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="1b50b-105">This topic is not current.</span></span> <span data-ttu-id="1b50b-106">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="1b50b-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="1b50b-107">Décrit la liste complète des emplacements pris en charge pour l’appareil.</span><span class="sxs-lookup"><span data-stu-id="1b50b-107">Describes the full list of supported bins for the device.</span></span> <span data-ttu-id="1b50b-108">Autorise la spécification du bac de sortie par page.</span><span class="sxs-lookup"><span data-stu-id="1b50b-108">Allows specification of output bin on a per page basis.</span></span> <span data-ttu-id="1b50b-109">Les mots clés JobOutputBin, DocumentOutputBin et PageOutputBin s’excluent mutuellement, un seul doit être spécifié dans un document PrintTicket ou des fonctionnalités d’impression.</span><span class="sxs-lookup"><span data-stu-id="1b50b-109">The JobOutputBin, DocumentOutputBin and PageOutputBin keywords are mutually exclusive only one should be specified in a PrintTicket or Print Capabilities document.</span></span>

-   [<span data-ttu-id="1b50b-110">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="1b50b-110">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="1b50b-111">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="1b50b-111">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="1b50b-112">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="1b50b-112">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="1b50b-113">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="1b50b-113">Element Information</span></span>



| <span data-ttu-id="1b50b-114">Nom</span><span class="sxs-lookup"><span data-stu-id="1b50b-114">Name</span></span>                       |                    |
|----------------------------|--------------------|
| <span data-ttu-id="1b50b-115">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="1b50b-115">Element Type</span></span> <br/>   | <span data-ttu-id="1b50b-116">Fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="1b50b-116">Feature</span></span><br/> |
| <span data-ttu-id="1b50b-117">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="1b50b-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="1b50b-118">Page</span><span class="sxs-lookup"><span data-stu-id="1b50b-118">Page</span></span><br/>    |
| <span data-ttu-id="1b50b-119">Notes</span><span class="sxs-lookup"><span data-stu-id="1b50b-119">Notes</span></span> <br/>          | <span data-ttu-id="1b50b-120">Aucun</span><span class="sxs-lookup"><span data-stu-id="1b50b-120">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="1b50b-121">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="1b50b-121">Structural Content</span></span>

<span data-ttu-id="1b50b-122">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="1b50b-122">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageOutputBin">
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

## <a name="structure-variables"></a><span data-ttu-id="1b50b-123">Variables de structure</span><span class="sxs-lookup"><span data-stu-id="1b50b-123">Structure Variables</span></span>

<span data-ttu-id="1b50b-124">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="1b50b-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="1b50b-125">Nom</span><span class="sxs-lookup"><span data-stu-id="1b50b-125">Name</span></span>                                   | <span data-ttu-id="1b50b-126">Type de données</span><span class="sxs-lookup"><span data-stu-id="1b50b-126">Data type</span></span>          | <span data-ttu-id="1b50b-127">Unité</span><span class="sxs-lookup"><span data-stu-id="1b50b-127">Unit</span></span>                  | <span data-ttu-id="1b50b-128">Valeurs prises en charge</span><span class="sxs-lookup"><span data-stu-id="1b50b-128">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="1b50b-129">Résumé</span><span class="sxs-lookup"><span data-stu-id="1b50b-129">Summary</span></span>                                                                             |
|----------------------------------------|--------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="1b50b-130">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="1b50b-130">\_OptionName\_</span></span><br/>              | <span data-ttu-id="1b50b-131">string</span><span class="sxs-lookup"><span data-stu-id="1b50b-131">string</span></span><br/>  | <span data-ttu-id="1b50b-132">caractères</span><span class="sxs-lookup"><span data-stu-id="1b50b-132">characters</span></span><br/> | <span data-ttu-id="1b50b-133">Nom complet valide tel que défini par les [espaces de noms dans XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="1b50b-133">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="1b50b-134">Si aucun espace de noms n’est spécifié, l’espace de noms par défaut est utilisé.</span><span class="sxs-lookup"><span data-stu-id="1b50b-134">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="1b50b-135">Nom de l'option.</span><span class="sxs-lookup"><span data-stu-id="1b50b-135">The name of the option.</span></span><br/>                                                  |
| <span data-ttu-id="1b50b-136">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="1b50b-136">\_IdentityOptionValue\_</span></span><br/>     | <span data-ttu-id="1b50b-137">string</span><span class="sxs-lookup"><span data-stu-id="1b50b-137">string</span></span><br/>  | <span data-ttu-id="1b50b-138">n/a</span><span class="sxs-lookup"><span data-stu-id="1b50b-138">n/a</span></span><br/>        | <span data-ttu-id="1b50b-139">True, False.</span><span class="sxs-lookup"><span data-stu-id="1b50b-139">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="1b50b-140">Définit une option qui, lorsqu’elle est sélectionnée, désactive cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="1b50b-140">Defines an Option which when selected would disable this feature.</span></span><br/>        |
| <span data-ttu-id="1b50b-141">\_BinTypeValue\_</span><span class="sxs-lookup"><span data-stu-id="1b50b-141">\_BinTypeValue\_</span></span><br/>            | <span data-ttu-id="1b50b-142">string</span><span class="sxs-lookup"><span data-stu-id="1b50b-142">string</span></span><br/>  | <span data-ttu-id="1b50b-143">n/a</span><span class="sxs-lookup"><span data-stu-id="1b50b-143">n/a</span></span><br/>        | <span data-ttu-id="1b50b-144">FaceDownTray, FaceUpTray, boîte aux lettres, trieuse, stacker, finisseur None.</span><span class="sxs-lookup"><span data-stu-id="1b50b-144">FaceDownTray, FaceUpTray, MailBox, Sorter, Stacker, Finisher None.</span></span><br/>                                                                                                         | <span data-ttu-id="1b50b-145">Spécifie le type général de l’emplacement.</span><span class="sxs-lookup"><span data-stu-id="1b50b-145">Specifies the general type of the bin.</span></span><br/>                                   |
| <span data-ttu-id="1b50b-146">\_MediaSheetCapacityValue\_</span><span class="sxs-lookup"><span data-stu-id="1b50b-146">\_MediaSheetCapacityValue\_</span></span><br/> | <span data-ttu-id="1b50b-147">entier</span><span class="sxs-lookup"><span data-stu-id="1b50b-147">integer</span></span><br/> | <span data-ttu-id="1b50b-148">feuilles</span><span class="sxs-lookup"><span data-stu-id="1b50b-148">sheets</span></span><br/>     | <span data-ttu-id="1b50b-149">Supérieur à 0.</span><span class="sxs-lookup"><span data-stu-id="1b50b-149">Greater than 0.</span></span><br/>                                                                                                                                                            | <span data-ttu-id="1b50b-150">Spécifie la capacité du média en nombre de pages (au niveau complet) de l’emplacement.</span><span class="sxs-lookup"><span data-stu-id="1b50b-150">Specifies the Media capacity in number of pages (full level) of the bin.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="1b50b-151">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="1b50b-151">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="1b50b-152">Les mots clés de schéma d’impression publics sont définis dans l' https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords espace de noms.</span><span class="sxs-lookup"><span data-stu-id="1b50b-152">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="1b50b-153">Le contenu de la Extensible Markup Language publique (XML) pour ce mot clé est défini ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="1b50b-153">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageOutputBin">
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

## <a name="related-topics"></a><span data-ttu-id="1b50b-154">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1b50b-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1b50b-155">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="1b50b-155">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




