---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: e73e1736-9be5-4831-8277-23a62658b7b5
title: JobNUpAllDocumentsContiguously
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90e307883a25fc977b9086259789c04f4b3a7cbf
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "104321774"
---
# <a name="jobnupalldocumentscontiguously"></a><span data-ttu-id="b7206-104">JobNUpAllDocumentsContiguously</span><span class="sxs-lookup"><span data-stu-id="b7206-104">JobNUpAllDocumentsContiguously</span></span>

<span data-ttu-id="b7206-105">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="b7206-105">This topic is not current.</span></span> <span data-ttu-id="b7206-106">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="b7206-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="b7206-107">Décrit la sortie de plusieurs pages logiques dans une feuille physique unique.</span><span class="sxs-lookup"><span data-stu-id="b7206-107">Describes the output of multiple logical pages to a single physical sheet.</span></span> <span data-ttu-id="b7206-108">Tous les documents du travail sont compilés ensemble de façon contiguë.</span><span class="sxs-lookup"><span data-stu-id="b7206-108">All documents in the job are compiled together contiguously.</span></span> <span data-ttu-id="b7206-109">JobNUpAllDocumentsContiguously et DocumentNUp s’excluent mutuellement.</span><span class="sxs-lookup"><span data-stu-id="b7206-109">JobNUpAllDocumentsContiguously and DocumentNUp are mutually exclusive.</span></span> <span data-ttu-id="b7206-110">Il revient au pilote de déterminer la gestion des contraintes entre ces mots clés.</span><span class="sxs-lookup"><span data-stu-id="b7206-110">It is up to the driver to determine constraint handling between these keywords.</span></span>

<span data-ttu-id="b7206-111">Le diagramme suivant illustre un exemple avec le document 1 contenant 3 pages et le document 2 contenant 2 pages.</span><span class="sxs-lookup"><span data-stu-id="b7206-111">The following diagram illustrates an example with Document 1 containing 3 pages, and Document 2 containing 2 pages.</span></span> <span data-ttu-id="b7206-112">Chaque document du travail est duplexé de façon contiguë.</span><span class="sxs-lookup"><span data-stu-id="b7206-112">Each document in the job is duplexed contiguously.</span></span> <span data-ttu-id="b7206-113">Les instructions de présentation présentées dans l’exemple sont l’option RightBottom.</span><span class="sxs-lookup"><span data-stu-id="b7206-113">The presentation directions shown in the example is the RightBottom option.</span></span>

![diagramme qui montre comment les pages de document sont disposées sur une feuille unique en fonction du paramètre DocumentNUp](images/local-1242234459-jobduplexpics.gif)

-   [<span data-ttu-id="b7206-115">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="b7206-115">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="b7206-116">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="b7206-116">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="b7206-117">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="b7206-117">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="b7206-118">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="b7206-118">Element Information</span></span>



| <span data-ttu-id="b7206-119">Nom</span><span class="sxs-lookup"><span data-stu-id="b7206-119">Name</span></span>                       |                                                                                                                                                |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7206-120">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="b7206-120">Element Type</span></span> <br/>   | <span data-ttu-id="b7206-121">Fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="b7206-121">Feature</span></span><br/>                                                                                                                             |
| <span data-ttu-id="b7206-122">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="b7206-122">Scoping Prefix</span></span> <br/> | <span data-ttu-id="b7206-123">Travail</span><span class="sxs-lookup"><span data-stu-id="b7206-123">Job</span></span><br/>                                                                                                                                 |
| <span data-ttu-id="b7206-124">Notes</span><span class="sxs-lookup"><span data-stu-id="b7206-124">Notes</span></span> <br/>          | <span data-ttu-id="b7206-125">Haut, bas, gauche et droite sont relatifs à PageImageableSize, où le sommet est indiqué par l’origine de la hauteur et de la largeur.</span><span class="sxs-lookup"><span data-stu-id="b7206-125">Top, Bottom, Left, and Right are relative to the PageImageableSize, where TopLeft is denoted by the origin of the height and width.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="b7206-126">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="b7206-126">Structural Content</span></span>

<span data-ttu-id="b7206-127">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="b7206-127">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:JobNUpAllDocumentsContiguously">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
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

## <a name="structure-variables"></a><span data-ttu-id="b7206-128">Variables de structure</span><span class="sxs-lookup"><span data-stu-id="b7206-128">Structure Variables</span></span>

<span data-ttu-id="b7206-129">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="b7206-129">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="b7206-130">Nom</span><span class="sxs-lookup"><span data-stu-id="b7206-130">Name</span></span>                                           | <span data-ttu-id="b7206-131">Type de données</span><span class="sxs-lookup"><span data-stu-id="b7206-131">Data type</span></span>          | <span data-ttu-id="b7206-132">Unité</span><span class="sxs-lookup"><span data-stu-id="b7206-132">Unit</span></span>                     | <span data-ttu-id="b7206-133">Valeurs prises en charge</span><span class="sxs-lookup"><span data-stu-id="b7206-133">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="b7206-134">Résumé</span><span class="sxs-lookup"><span data-stu-id="b7206-134">Summary</span></span>                                                                                                                              |
|------------------------------------------------|--------------------|--------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7206-135">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="b7206-135">\_OptionName\_</span></span><br/>                      | <span data-ttu-id="b7206-136">string</span><span class="sxs-lookup"><span data-stu-id="b7206-136">string</span></span><br/>  | <span data-ttu-id="b7206-137">caractères</span><span class="sxs-lookup"><span data-stu-id="b7206-137">characters</span></span><br/>    | <span data-ttu-id="b7206-138">Nom complet valide tel que défini par les [espaces de noms dans XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="b7206-138">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="b7206-139">Si aucun espace de noms n’est spécifié, l’espace de noms par défaut est utilisé.</span><span class="sxs-lookup"><span data-stu-id="b7206-139">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="b7206-140">Nom de l'option.</span><span class="sxs-lookup"><span data-stu-id="b7206-140">The name of the option.</span></span><br/>                                                                                                   |
| <span data-ttu-id="b7206-141">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="b7206-141">\_IdentityOptionValue\_</span></span><br/>             | <span data-ttu-id="b7206-142">string</span><span class="sxs-lookup"><span data-stu-id="b7206-142">string</span></span><br/>  | <span data-ttu-id="b7206-143">n/a</span><span class="sxs-lookup"><span data-stu-id="b7206-143">n/a</span></span><br/>           | <span data-ttu-id="b7206-144">True, False.</span><span class="sxs-lookup"><span data-stu-id="b7206-144">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="b7206-145">Définit une option qui, lorsqu’elle est sélectionnée, désactive cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="b7206-145">Defines an Option which when selected would disable this feature.</span></span><br/>                                                         |
| <span data-ttu-id="b7206-146">\_PagesPerSheetValue\_</span><span class="sxs-lookup"><span data-stu-id="b7206-146">\_PagesPerSheetValue\_</span></span><br/>              | <span data-ttu-id="b7206-147">entier</span><span class="sxs-lookup"><span data-stu-id="b7206-147">integer</span></span><br/> | <span data-ttu-id="b7206-148">Pages logiques</span><span class="sxs-lookup"><span data-stu-id="b7206-148">Logical pages</span></span><br/> | <span data-ttu-id="b7206-149">Tous les entiers (supérieurs à zéro).</span><span class="sxs-lookup"><span data-stu-id="b7206-149">All integers (Greater than zero).</span></span><br/>                                                                                                                                          | <span data-ttu-id="b7206-150">Spécifie le nombre de pages logiques par feuille physique.</span><span class="sxs-lookup"><span data-stu-id="b7206-150">Specifies the number of logical pages per physical sheet.</span></span> <span data-ttu-id="b7206-151">L’ensemble pris en charge peut être n’importe quel ensemble d’entiers, par exemple</span><span class="sxs-lookup"><span data-stu-id="b7206-151">Supported set can be any set of integers E.g.</span></span> <span data-ttu-id="b7206-152">{1,2,4,6,8,9,16}.</span><span class="sxs-lookup"><span data-stu-id="b7206-152">{1,2,4,6,8,9,16}.</span></span><br/> |
| <span data-ttu-id="b7206-153">\_PresentationDirectionOptionName\_</span><span class="sxs-lookup"><span data-stu-id="b7206-153">\_PresentationDirectionOptionName\_</span></span><br/> | <span data-ttu-id="b7206-154">string</span><span class="sxs-lookup"><span data-stu-id="b7206-154">string</span></span><br/>  | <span data-ttu-id="b7206-155">caractères</span><span class="sxs-lookup"><span data-stu-id="b7206-155">characters</span></span><br/>    | <span data-ttu-id="b7206-156">Nom complet valide tel que défini par les [espaces de noms dans XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="b7206-156">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="b7206-157">Si aucun espace de noms n’est spécifié, l’espace de noms par défaut est utilisé.</span><span class="sxs-lookup"><span data-stu-id="b7206-157">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="b7206-158">Nom de l'option.</span><span class="sxs-lookup"><span data-stu-id="b7206-158">The name of the option.</span></span><br/>                                                                                                   |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="b7206-159">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="b7206-159">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="b7206-160">Les mots clés de schéma d’impression publics sont définis dans l' https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords espace de noms.</span><span class="sxs-lookup"><span data-stu-id="b7206-160">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="b7206-161">Le contenu de la Extensible Markup Language publique (XML) pour ce mot clé est défini ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="b7206-161">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:JobNUpAllDocumentsContiguously">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option>
    <psf:ScoredProperty name="psk:PagesPerSheet">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Feature name="psk:PresentationDirection">
    <!-- Specifies left to right, top to bottom. -->
    <psf:Option name="psk:RightBottom" />
    <!-- Specifies top to bottom, left to right. -->
    <psf:Option name="psk:BottomRight" />
    <!-- Specifies right to left, top to bottom. -->
    <psf:Option name="psk:LeftBottom" />
    <!-- Specifies top to bottom, right to left. -->
    <psf:Option name="psk:BottomLeft" />
    <!-- Specifies left to right, bottom to top. -->
    <psf:Option name="psk:RightTop" />
    <!-- Specifies bottom to top, left to right. -->
    <psf:Option name="psk:TopRight" />
    <!-- Specifies right to left, bottom to top. -->
    <psf:Option name="psk:LeftTop" />
    <!-- Specifies bottom to top, right to left. -->
    <psf:Option name="psk:TopLeft" />
  </psf:Feature>
</psf:Feature>
    
```

## <a name="related-topics"></a><span data-ttu-id="b7206-162">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b7206-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b7206-163">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="b7206-163">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




