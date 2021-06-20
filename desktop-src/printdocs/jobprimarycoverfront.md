---
description: En savoir plus sur l’élément JobPrimaryCoverFront, qui décrit la feuille de couverture. La totalité du travail aura une seule feuille principale.
ms.assetid: 270b16f6-677c-430a-aa69-1b5c6dfd3ba4
title: JobPrimaryCoverFront
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c60aef4a70404ce6777b9bfe2848fddffa4e89d
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408672"
---
# <a name="jobprimarycoverfront"></a><span data-ttu-id="360bd-104">JobPrimaryCoverFront</span><span class="sxs-lookup"><span data-stu-id="360bd-104">JobPrimaryCoverFront</span></span>

<span data-ttu-id="360bd-105">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="360bd-105">This topic is not current.</span></span> <span data-ttu-id="360bd-106">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="360bd-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="360bd-107">Décrit la feuille de couverture avant (début).</span><span class="sxs-lookup"><span data-stu-id="360bd-107">Describes the front (beginning) cover sheet.</span></span> <span data-ttu-id="360bd-108">La totalité du travail aura une seule feuille principale.</span><span class="sxs-lookup"><span data-stu-id="360bd-108">The entire job will have a single primary sheet.</span></span> <span data-ttu-id="360bd-109">La feuille de couverture doit être imprimée sur le PageMediaSize et le PageMediaType utilisés pour la première page du travail.</span><span class="sxs-lookup"><span data-stu-id="360bd-109">The cover sheet should be printed on the PageMediaSize and PageMediaType used for the first page of the job.</span></span> <span data-ttu-id="360bd-110">La feuille de couverture doit être intégrée dans les options de traitement (telles que JobDuplexAllDocumentsContiguously, JobNUpAllDocumentsContiguously), comme indiqué par l’option spécifiée.</span><span class="sxs-lookup"><span data-stu-id="360bd-110">The cover sheet should be integrated into processing options (such as JobDuplexAllDocumentsContiguously, JobNUpAllDocumentsContiguously) as indicated by the Option specified.</span></span>

-   [<span data-ttu-id="360bd-111">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="360bd-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="360bd-112">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="360bd-112">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="360bd-113">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="360bd-113">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="360bd-114">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="360bd-114">Element Information</span></span>



| <span data-ttu-id="360bd-115">Nom</span><span class="sxs-lookup"><span data-stu-id="360bd-115">Name</span></span> | <span data-ttu-id="360bd-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="360bd-116">Value</span></span> |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="360bd-117">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="360bd-117">Element Type</span></span> <br/>   | <span data-ttu-id="360bd-118">Fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="360bd-118">Feature</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="360bd-119">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="360bd-119">Scoping Prefix</span></span> <br/> | <span data-ttu-id="360bd-120">Travail</span><span class="sxs-lookup"><span data-stu-id="360bd-120">Job</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="360bd-121">Notes</span><span class="sxs-lookup"><span data-stu-id="360bd-121">Notes</span></span> <br/>          | <span data-ttu-id="360bd-122">Les consommateurs compatibles XPS doivent s’assurer qu’une référence URI à une ressource telle qu’une image ou un profil de couleurs dans un document de fonctionnalités d’impression ou un PrintTicket doit faire référence à un nom de partie (un URI relatif à la racine du package) dans le même package de document XPS qui contient le PrintTicket résultant.</span><span class="sxs-lookup"><span data-stu-id="360bd-122">XPS-compliant consumers MUST enforce that a URI reference to a resource such as an image or color profile in either a Print Capabilities document or PrintTicket MUST refer to a part name (a relative URI to the package root) within the same XPS Document package that contains the resultant PrintTicket.</span></span> <span data-ttu-id="360bd-123">Un consommateur XPS conforme ne doit pas utiliser un URI qui n’est pas conforme à la syntaxe du nom de la partie.</span><span class="sxs-lookup"><span data-stu-id="360bd-123">A compliant XPS consumer MUST NOT use a URI that is not compliant with the part name syntax.</span></span> <span data-ttu-id="360bd-124">Ces paramètres sont spécifiques à XPS.</span><span class="sxs-lookup"><span data-stu-id="360bd-124">These settings are XPS specific.</span></span> <br/> <span data-ttu-id="360bd-125">Les URI référencés dans un document de fonctionnalités d’impression ou un PrintTicket ne doivent pas être résolus en tant qu’URL.</span><span class="sxs-lookup"><span data-stu-id="360bd-125">URIs which are referenced in either a Print Capabilities document or PrintTicket MUST NOT be resolved as URLs.</span></span> <span data-ttu-id="360bd-126">Cela ne peut pas être résolu comme prévu et peut créer des risques de sécurité néfastes pour le pilote et le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="360bd-126">This is unsafe as they may not resolve as intended and may create harmful security risks for the driver and operating system.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="360bd-127">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="360bd-127">Structural Content</span></span>

<span data-ttu-id="360bd-128">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="360bd-128">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:JobPrimaryCoverFront">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <!-- Specifies the XPS part name for the front cover sheet. -->
    <psf:ScoredProperty name="psk:CoverFrontSource">
      <psf:ParameterRef name="psk:JobPrimaryCoverFrontSource" />
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
      
```

## <a name="structure-variables"></a><span data-ttu-id="360bd-129">Variables de structure</span><span class="sxs-lookup"><span data-stu-id="360bd-129">Structure Variables</span></span>

<span data-ttu-id="360bd-130">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="360bd-130">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="360bd-131">Nom</span><span class="sxs-lookup"><span data-stu-id="360bd-131">Name</span></span>                               | <span data-ttu-id="360bd-132">Type de données</span><span class="sxs-lookup"><span data-stu-id="360bd-132">Data type</span></span>         | <span data-ttu-id="360bd-133">Unité</span><span class="sxs-lookup"><span data-stu-id="360bd-133">Unit</span></span>           | <span data-ttu-id="360bd-134">Valeurs prises en charge</span><span class="sxs-lookup"><span data-stu-id="360bd-134">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="360bd-135">Résumé</span><span class="sxs-lookup"><span data-stu-id="360bd-135">Summary</span></span>                                                                      |
|------------------------------------|-------------------|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="360bd-136">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="360bd-136">\_OptionName\_</span></span><br/>          | <span data-ttu-id="360bd-137">string</span><span class="sxs-lookup"><span data-stu-id="360bd-137">string</span></span><br/> | <span data-ttu-id="360bd-138">n/a</span><span class="sxs-lookup"><span data-stu-id="360bd-138">n/a</span></span><br/> | <span data-ttu-id="360bd-139">Nom complet valide tel que défini par les [espaces de noms dans XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="360bd-139">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="360bd-140">Si aucun espace de noms n’est spécifié, l’espace de noms par défaut est utilisé.</span><span class="sxs-lookup"><span data-stu-id="360bd-140">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="360bd-141">Nom de l'option.</span><span class="sxs-lookup"><span data-stu-id="360bd-141">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="360bd-142">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="360bd-142">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="360bd-143">string</span><span class="sxs-lookup"><span data-stu-id="360bd-143">string</span></span><br/> | <span data-ttu-id="360bd-144">n/a</span><span class="sxs-lookup"><span data-stu-id="360bd-144">n/a</span></span><br/> | <span data-ttu-id="360bd-145">True, False.</span><span class="sxs-lookup"><span data-stu-id="360bd-145">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="360bd-146">Définit une option qui, lorsqu’elle est sélectionnée, désactive cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="360bd-146">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="360bd-147">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="360bd-147">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="360bd-148">Les mots clés de schéma d’impression publics sont définis dans l' https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords espace de noms.</span><span class="sxs-lookup"><span data-stu-id="360bd-148">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="360bd-149">Le contenu de la Extensible Markup Language publique (XML) pour ce mot clé est défini ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="360bd-149">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:JobPrimaryCoverFront">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies no cover will be output -->
  <psf:Option name="psk:NoCover" />
  <!-- Specifies the cover indicated by "CoverFrontSource" should be printed on the back side 
       of the cover sheet.  If a JobPrimaryCoverFrontSource ParameterInit element is not specified, 
       this Option should be ignored. -->
  <psf:Option name="psk:PrintFront">
    <psf:ScoredProperty name="psk:CoverFrontSource">
      <psf:ParameterRef name="psk:JobPrimaryCoverFrontSource" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies the cover indicated by "CoverFrontSource" may be printed on either side 
       of the cover sheet.  If a JobCoverBackSource ParameterInit element is not specified, 
       this Option should be ignored. -->
  <psf:Option name="psk:PrintBoth">
    <psf:ScoredProperty name="psk:CoverFrontSource">
      <psf:ParameterRef name="psk:JobPrimaryCoverFrontSource" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies the cover indicated by "CoverFrontSource" should be printed on the front side 
       of the cover sheet.  If a JobCoverBackSource ParameterInit element is not specified, 
       this Option should be ignored. -->
  <psf:Option name="psk:PrintBack">
    <psf:ScoredProperty name="psk:CoverFrontSource">
      <psf:ParameterRef name="psk:JobPrimaryCoverFrontSource" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies a blank cover sheet should be printed. -->
  <psf:Option name="psk:BlankCover" />
</psf:Feature>
    
```

## <a name="related-topics"></a><span data-ttu-id="360bd-150">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="360bd-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="360bd-151">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="360bd-151">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




