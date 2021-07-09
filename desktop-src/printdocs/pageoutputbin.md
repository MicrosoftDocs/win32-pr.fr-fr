---
description: En savoir plus sur l’élément configurable par l’utilisateur PageOutputBin. Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: c5050804-0e77-4d26-bf00-5d9690102b18
title: PageOutputBin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a9963bf2ca7a2dd60be37c797a27c6ff09b1206
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/09/2021
ms.locfileid: "113548997"
---
# <a name="pageoutputbin"></a><span data-ttu-id="eeb3c-105">PageOutputBin</span><span class="sxs-lookup"><span data-stu-id="eeb3c-105">PageOutputBin</span></span>

<span data-ttu-id="eeb3c-106">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="eeb3c-106">This topic is not current.</span></span> <span data-ttu-id="eeb3c-107">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="eeb3c-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="eeb3c-108">Décrit la liste complète des emplacements pris en charge pour l’appareil.</span><span class="sxs-lookup"><span data-stu-id="eeb3c-108">Describes the full list of supported bins for the device.</span></span> <span data-ttu-id="eeb3c-109">Autorise la spécification du bac de sortie par page.</span><span class="sxs-lookup"><span data-stu-id="eeb3c-109">Allows specification of output bin on a per page basis.</span></span> <span data-ttu-id="eeb3c-110">Les mots clés JobOutputBin, DocumentOutputBin et PageOutputBin s’excluent mutuellement, un seul doit être spécifié dans un document PrintTicket ou des fonctionnalités d’impression.</span><span class="sxs-lookup"><span data-stu-id="eeb3c-110">The JobOutputBin, DocumentOutputBin and PageOutputBin keywords are mutually exclusive only one should be specified in a PrintTicket or Print Capabilities document.</span></span>

-   [<span data-ttu-id="eeb3c-111">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="eeb3c-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="eeb3c-112">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="eeb3c-112">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="eeb3c-113">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="eeb3c-113">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="eeb3c-114">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="eeb3c-114">Element Information</span></span>



| <span data-ttu-id="eeb3c-115">Nom</span><span class="sxs-lookup"><span data-stu-id="eeb3c-115">Name</span></span> | <span data-ttu-id="eeb3c-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="eeb3c-116">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="eeb3c-117">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="eeb3c-117">Element Type</span></span> <br/>   | <span data-ttu-id="eeb3c-118">Composant</span><span class="sxs-lookup"><span data-stu-id="eeb3c-118">Feature</span></span><br/> |
| <span data-ttu-id="eeb3c-119">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="eeb3c-119">Scoping Prefix</span></span> <br/> | <span data-ttu-id="eeb3c-120">Page</span><span class="sxs-lookup"><span data-stu-id="eeb3c-120">Page</span></span><br/>    |
| <span data-ttu-id="eeb3c-121">Notes</span><span class="sxs-lookup"><span data-stu-id="eeb3c-121">Notes</span></span> <br/>          | <span data-ttu-id="eeb3c-122">Aucun</span><span class="sxs-lookup"><span data-stu-id="eeb3c-122">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="eeb3c-123">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="eeb3c-123">Structural Content</span></span>

<span data-ttu-id="eeb3c-124">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="eeb3c-124">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="eeb3c-125">Variables de structure</span><span class="sxs-lookup"><span data-stu-id="eeb3c-125">Structure Variables</span></span>

<span data-ttu-id="eeb3c-126">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="eeb3c-126">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="eeb3c-127">Nom</span><span class="sxs-lookup"><span data-stu-id="eeb3c-127">Name</span></span>                                   | <span data-ttu-id="eeb3c-128">Type de données</span><span class="sxs-lookup"><span data-stu-id="eeb3c-128">Data type</span></span>          | <span data-ttu-id="eeb3c-129">Unité</span><span class="sxs-lookup"><span data-stu-id="eeb3c-129">Unit</span></span>                  | <span data-ttu-id="eeb3c-130">Valeurs prises en charge</span><span class="sxs-lookup"><span data-stu-id="eeb3c-130">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="eeb3c-131">Résumé</span><span class="sxs-lookup"><span data-stu-id="eeb3c-131">Summary</span></span>                                                                             |
|----------------------------------------|--------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="eeb3c-132">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="eeb3c-132">\_OptionName\_</span></span><br/>              | <span data-ttu-id="eeb3c-133">string</span><span class="sxs-lookup"><span data-stu-id="eeb3c-133">string</span></span><br/>  | <span data-ttu-id="eeb3c-134">caractères</span><span class="sxs-lookup"><span data-stu-id="eeb3c-134">characters</span></span><br/> | <span data-ttu-id="eeb3c-135">Nom complet valide tel que défini par les [espaces de noms dans XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="eeb3c-135">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="eeb3c-136">Si aucun espace de noms n’est spécifié, l’espace de noms par défaut est utilisé.</span><span class="sxs-lookup"><span data-stu-id="eeb3c-136">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="eeb3c-137">Nom de l'option.</span><span class="sxs-lookup"><span data-stu-id="eeb3c-137">The name of the option.</span></span><br/>                                                  |
| <span data-ttu-id="eeb3c-138">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="eeb3c-138">\_IdentityOptionValue\_</span></span><br/>     | <span data-ttu-id="eeb3c-139">string</span><span class="sxs-lookup"><span data-stu-id="eeb3c-139">string</span></span><br/>  | <span data-ttu-id="eeb3c-140">n/a</span><span class="sxs-lookup"><span data-stu-id="eeb3c-140">n/a</span></span><br/>        | <span data-ttu-id="eeb3c-141">True, False.</span><span class="sxs-lookup"><span data-stu-id="eeb3c-141">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="eeb3c-142">Définit une option qui, lorsqu’elle est sélectionnée, désactive cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="eeb3c-142">Defines an Option which when selected would disable this feature.</span></span><br/>        |
| <span data-ttu-id="eeb3c-143">\_BinTypeValue\_</span><span class="sxs-lookup"><span data-stu-id="eeb3c-143">\_BinTypeValue\_</span></span><br/>            | <span data-ttu-id="eeb3c-144">string</span><span class="sxs-lookup"><span data-stu-id="eeb3c-144">string</span></span><br/>  | <span data-ttu-id="eeb3c-145">n/a</span><span class="sxs-lookup"><span data-stu-id="eeb3c-145">n/a</span></span><br/>        | <span data-ttu-id="eeb3c-146">FaceDownTray, FaceUpTray, boîte aux lettres, trieuse, stacker, finisseur None.</span><span class="sxs-lookup"><span data-stu-id="eeb3c-146">FaceDownTray, FaceUpTray, MailBox, Sorter, Stacker, Finisher None.</span></span><br/>                                                                                                         | <span data-ttu-id="eeb3c-147">Spécifie le type général de l’emplacement.</span><span class="sxs-lookup"><span data-stu-id="eeb3c-147">Specifies the general type of the bin.</span></span><br/>                                   |
| <span data-ttu-id="eeb3c-148">\_MediaSheetCapacityValue\_</span><span class="sxs-lookup"><span data-stu-id="eeb3c-148">\_MediaSheetCapacityValue\_</span></span><br/> | <span data-ttu-id="eeb3c-149">entier</span><span class="sxs-lookup"><span data-stu-id="eeb3c-149">integer</span></span><br/> | <span data-ttu-id="eeb3c-150">feuilles</span><span class="sxs-lookup"><span data-stu-id="eeb3c-150">sheets</span></span><br/>     | <span data-ttu-id="eeb3c-151">Supérieur à 0.</span><span class="sxs-lookup"><span data-stu-id="eeb3c-151">Greater than 0.</span></span><br/>                                                                                                                                                            | <span data-ttu-id="eeb3c-152">Spécifie la capacité du média en nombre de pages (au niveau complet) de l’emplacement.</span><span class="sxs-lookup"><span data-stu-id="eeb3c-152">Specifies the Media capacity in number of pages (full level) of the bin.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="eeb3c-153">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="eeb3c-153">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="eeb3c-154">Les mots clés de schéma d’impression publics sont définis dans l' https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords espace de noms.</span><span class="sxs-lookup"><span data-stu-id="eeb3c-154">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="eeb3c-155">Le contenu de la Extensible Markup Language publique (XML) pour ce mot clé est défini ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="eeb3c-155">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="eeb3c-156">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="eeb3c-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eeb3c-157">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="eeb3c-157">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




