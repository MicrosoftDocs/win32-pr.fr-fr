---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: 941515a8-ba3f-47b9-9f3f-08a48122661a
title: DocumentNUp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab531a2095e83aa35f3dff450270c2a5b4520d62
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996286"
---
# <a name="documentnup"></a><span data-ttu-id="ab1d9-104">DocumentNUp</span><span class="sxs-lookup"><span data-stu-id="ab1d9-104">DocumentNUp</span></span>

<span data-ttu-id="ab1d9-105">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="ab1d9-105">This topic is not current.</span></span> <span data-ttu-id="ab1d9-106">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="ab1d9-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="ab1d9-107">Décrit la sortie et le format de plusieurs pages logiques dans une même feuille physique.</span><span class="sxs-lookup"><span data-stu-id="ab1d9-107">Describes the output and format of multiple logical pages to a single physical sheet.</span></span> <span data-ttu-id="ab1d9-108">Chaque document est compilé séparément.</span><span class="sxs-lookup"><span data-stu-id="ab1d9-108">Each document is compiled separately.</span></span> <span data-ttu-id="ab1d9-109">DocumentNUp et JobNUpAllDocumentsContiguously s’excluent mutuellement.</span><span class="sxs-lookup"><span data-stu-id="ab1d9-109">DocumentNUp and JobNUpAllDocumentsContiguously are mutually exclusive.</span></span> <span data-ttu-id="ab1d9-110">Il revient au pilote de déterminer la gestion des contraintes entre ces mots clés.</span><span class="sxs-lookup"><span data-stu-id="ab1d9-110">It is up to the driver to determine constraint handling between these keywords.</span></span>

<span data-ttu-id="ab1d9-111">Le diagramme suivant illustre un exemple avec le document 1 contenant 3 pages et le document 2 contenant 2 pages.</span><span class="sxs-lookup"><span data-stu-id="ab1d9-111">The following diagram illustrates an example with Document 1 containing 3 pages, and Document 2 containing 2 pages.</span></span> <span data-ttu-id="ab1d9-112">Chaque document est séparé par un duplex.</span><span class="sxs-lookup"><span data-stu-id="ab1d9-112">Each document is duplexed separately.</span></span> <span data-ttu-id="ab1d9-113">La direction de présentation présentée ci-dessous est l’option RightBottom.</span><span class="sxs-lookup"><span data-stu-id="ab1d9-113">The presentation direction shown below is the RightBottom option.</span></span>

![diagramme qui montre comment les pages de document sont disposées sur une feuille unique en fonction du paramètre DocumentNUp](images/local-1663869164-docduplex1.gif)

-   [<span data-ttu-id="ab1d9-115">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="ab1d9-115">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="ab1d9-116">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="ab1d9-116">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="ab1d9-117">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="ab1d9-117">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="ab1d9-118">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="ab1d9-118">Element Information</span></span>



| <span data-ttu-id="ab1d9-119">Nom</span><span class="sxs-lookup"><span data-stu-id="ab1d9-119">Name</span></span> | <span data-ttu-id="ab1d9-120">Value</span><span class="sxs-lookup"><span data-stu-id="ab1d9-120">Value</span></span> |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab1d9-121">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="ab1d9-121">Element Type</span></span> <br/>   | <span data-ttu-id="ab1d9-122">Fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="ab1d9-122">Feature</span></span><br/>                                                                                                                              |
| <span data-ttu-id="ab1d9-123">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="ab1d9-123">Scoping Prefix</span></span> <br/> | <span data-ttu-id="ab1d9-124">Document</span><span class="sxs-lookup"><span data-stu-id="ab1d9-124">Document</span></span><br/>                                                                                                                             |
| <span data-ttu-id="ab1d9-125">Notes</span><span class="sxs-lookup"><span data-stu-id="ab1d9-125">Notes</span></span> <br/>          | <span data-ttu-id="ab1d9-126">Haut, bas, gauche et droite sont relatifs à PageImageableSize, où Left est indiqué par l’origine de l’axe x et de l’axe y.</span><span class="sxs-lookup"><span data-stu-id="ab1d9-126">Top, Bottom, Left, and Right are relative to the PageImageableSize, where TopLeft is denoted by the origin of the x-axis and y-axis.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="ab1d9-127">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="ab1d9-127">Structural Content</span></span>

<span data-ttu-id="ab1d9-128">La structure XML de cet élément est la suivante :</span><span class="sxs-lookup"><span data-stu-id="ab1d9-128">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:Feature name="psk:DocumentNUp">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option>
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <psf:ScoredProperty name="psk:PagesPerSheet">
      <psf:Value xsi:type="xs:integer">_PagesPerSheetValue_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies the ordering direction of the pages.  First direction followed by second direction. -->
  <psf:Feature name="psk:PresentationDirection">
    <psf:Option name="psk:_PresentationDirectionOptionName_" />
  </psf:Feature>
</psf:Feature>
```

## <a name="structure-variables"></a><span data-ttu-id="ab1d9-129">Variables de structure</span><span class="sxs-lookup"><span data-stu-id="ab1d9-129">Structure Variables</span></span>

<span data-ttu-id="ab1d9-130">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="ab1d9-130">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="ab1d9-131">Nom</span><span class="sxs-lookup"><span data-stu-id="ab1d9-131">Name</span></span>                                           | <span data-ttu-id="ab1d9-132">Type de données</span><span class="sxs-lookup"><span data-stu-id="ab1d9-132">Data type</span></span>          | <span data-ttu-id="ab1d9-133">Unité</span><span class="sxs-lookup"><span data-stu-id="ab1d9-133">Unit</span></span>                     | <span data-ttu-id="ab1d9-134">Valeurs prises en charge</span><span class="sxs-lookup"><span data-stu-id="ab1d9-134">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="ab1d9-135">Résumé</span><span class="sxs-lookup"><span data-stu-id="ab1d9-135">Summary</span></span>                                                                                                                              |
|------------------------------------------------|--------------------|--------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab1d9-136">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="ab1d9-136">\_OptionName\_</span></span><br/>                      | <span data-ttu-id="ab1d9-137">string</span><span class="sxs-lookup"><span data-stu-id="ab1d9-137">string</span></span><br/>  | <span data-ttu-id="ab1d9-138">caractères</span><span class="sxs-lookup"><span data-stu-id="ab1d9-138">characters</span></span><br/>    | <span data-ttu-id="ab1d9-139">Nom complet valide tel que défini par les [espaces de noms dans XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="ab1d9-139">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="ab1d9-140">Si aucun espace de noms n’est spécifié, l’espace de noms par défaut est utilisé.</span><span class="sxs-lookup"><span data-stu-id="ab1d9-140">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="ab1d9-141">Nom de l'option.</span><span class="sxs-lookup"><span data-stu-id="ab1d9-141">The name of the option.</span></span><br/>                                                                                                   |
| <span data-ttu-id="ab1d9-142">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="ab1d9-142">\_IdentityOptionValue\_</span></span><br/>             | <span data-ttu-id="ab1d9-143">string</span><span class="sxs-lookup"><span data-stu-id="ab1d9-143">string</span></span><br/>  | <span data-ttu-id="ab1d9-144">n/a</span><span class="sxs-lookup"><span data-stu-id="ab1d9-144">n/a</span></span><br/>           | <span data-ttu-id="ab1d9-145">True, False.</span><span class="sxs-lookup"><span data-stu-id="ab1d9-145">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="ab1d9-146">Définit une option qui, lorsqu’elle est sélectionnée, désactive cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="ab1d9-146">Defines an Option which when selected would disable this feature.</span></span><br/>                                                         |
| <span data-ttu-id="ab1d9-147">\_PagesPerSheetValue\_</span><span class="sxs-lookup"><span data-stu-id="ab1d9-147">\_PagesPerSheetValue\_</span></span><br/>              | <span data-ttu-id="ab1d9-148">entier</span><span class="sxs-lookup"><span data-stu-id="ab1d9-148">integer</span></span><br/> | <span data-ttu-id="ab1d9-149">Pages logiques</span><span class="sxs-lookup"><span data-stu-id="ab1d9-149">Logical pages</span></span><br/> | <span data-ttu-id="ab1d9-150">Tous les entiers (supérieurs à zéro).</span><span class="sxs-lookup"><span data-stu-id="ab1d9-150">All integers (Greater than Zero).</span></span><br/>                                                                                                                                          | <span data-ttu-id="ab1d9-151">Spécifie le nombre de pages logiques par feuille physique.</span><span class="sxs-lookup"><span data-stu-id="ab1d9-151">Specifies the number of logical pages per physical sheet.</span></span> <span data-ttu-id="ab1d9-152">L’ensemble pris en charge peut être n’importe quel ensemble d’entiers, par exemple</span><span class="sxs-lookup"><span data-stu-id="ab1d9-152">Supported set can be any set of integers E.g.</span></span> <span data-ttu-id="ab1d9-153">{1,2,4,6,8,9,16}.</span><span class="sxs-lookup"><span data-stu-id="ab1d9-153">{1,2,4,6,8,9,16}.</span></span><br/> |
| <span data-ttu-id="ab1d9-154">\_PresentationDirectionOptionName\_</span><span class="sxs-lookup"><span data-stu-id="ab1d9-154">\_PresentationDirectionOptionName\_</span></span><br/> | <span data-ttu-id="ab1d9-155">string</span><span class="sxs-lookup"><span data-stu-id="ab1d9-155">string</span></span><br/>  | <span data-ttu-id="ab1d9-156">caractères</span><span class="sxs-lookup"><span data-stu-id="ab1d9-156">characters</span></span><br/>    | <span data-ttu-id="ab1d9-157">Nom complet valide tel que défini par les [espaces de noms dans XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="ab1d9-157">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="ab1d9-158">Si aucun espace de noms n’est spécifié, l’espace de noms par défaut est utilisé.</span><span class="sxs-lookup"><span data-stu-id="ab1d9-158">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="ab1d9-159">Nom de l'option.</span><span class="sxs-lookup"><span data-stu-id="ab1d9-159">The name of the option.</span></span><br/>                                                                                                   |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="ab1d9-160">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="ab1d9-160">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="ab1d9-161">Les mots clés de schéma d’impression publics sont définis dans l' https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords espace de noms.</span><span class="sxs-lookup"><span data-stu-id="ab1d9-161">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="ab1d9-162">Le contenu de la Extensible Markup Language publique (XML) pour ce mot clé est défini ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="ab1d9-162">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:DocumentNUp">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option>
    <psf:ScoredProperty name="psk:PagesPerSheet">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Feature name="psk:PresentationDirection">
    <!-- Specifies format left to right, top to bottom. -->
    <psf:Option name="psk:RightBottom" />
    <!-- Specifies format top to bottom, left to right. -->
    <psf:Option name="psk:BottomRight" />
    <!-- Specifies format right to left, top to bottom. -->
    <psf:Option name="psk:LeftBottom" />
    <!-- Specifies format top to bottom, right to left. -->
    <psf:Option name="psk:BottomLeft" />
    <!-- Specifies format left to right, bottom to top. -->
    <psf:Option name="psk:RightTop" />
    <!-- Specifies format bottom to top, left to right. -->
    <psf:Option name="psk:TopRight" />
    <!-- Specifies format right to left, bottom to top. -->
    <psf:Option name="psk:LeftTop" />
    <!-- Specifies format bottom to top, right to left. -->
    <psf:Option name="psk:TopLeft" />
  </psf:Feature>
</psf:Feature>
    
```

## <a name="related-topics"></a><span data-ttu-id="ab1d9-163">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ab1d9-163">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ab1d9-164">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="ab1d9-164">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




