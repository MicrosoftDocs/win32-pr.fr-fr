---
description: En savoir plus sur l’élément configurable par l’utilisateur DocumentCoverFront. Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: 25dbd083-5815-4b25-bfdc-4d14f96d2b45
title: DocumentCoverFront
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 301b67c9a741caa48024646854b208ac5dffbb20
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119824"
---
# <a name="documentcoverfront"></a><span data-ttu-id="19447-105">DocumentCoverFront</span><span class="sxs-lookup"><span data-stu-id="19447-105">DocumentCoverFront</span></span>

<span data-ttu-id="19447-106">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="19447-106">This topic is not current.</span></span> <span data-ttu-id="19447-107">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="19447-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="19447-108">Décrit la feuille de couverture avant (début).</span><span class="sxs-lookup"><span data-stu-id="19447-108">Describes the front (beginning) cover sheet.</span></span> <span data-ttu-id="19447-109">Chaque document aura une feuille distincte.</span><span class="sxs-lookup"><span data-stu-id="19447-109">Each document will have a separate sheet.</span></span> <span data-ttu-id="19447-110">La feuille de couverture doit être imprimée sur le PageMediaSize et le PageMediaType utilisés pour la première page du document.</span><span class="sxs-lookup"><span data-stu-id="19447-110">The cover sheet should be printed on the PageMediaSize and PageMediaType used for the first page of the document.</span></span> <span data-ttu-id="19447-111">La feuille de couverture doit être intégrée dans les options de traitement (telles que DocumentDuplex, DocumentNUp), comme indiqué par l’option spécifiée.</span><span class="sxs-lookup"><span data-stu-id="19447-111">The cover sheet should be integrated into processing options (such as DocumentDuplex, DocumentNUp) as indicated by the Option specified.</span></span>

-   [<span data-ttu-id="19447-112">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="19447-112">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="19447-113">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="19447-113">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="19447-114">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="19447-114">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="19447-115">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="19447-115">Element Information</span></span>



| <span data-ttu-id="19447-116">Nom</span><span class="sxs-lookup"><span data-stu-id="19447-116">Name</span></span> | <span data-ttu-id="19447-117">Value</span><span class="sxs-lookup"><span data-stu-id="19447-117">Value</span></span> |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="19447-118">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="19447-118">Element Type</span></span> <br/>   | <span data-ttu-id="19447-119">Fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="19447-119">Feature</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="19447-120">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="19447-120">Scoping Prefix</span></span> <br/> | <span data-ttu-id="19447-121">Document</span><span class="sxs-lookup"><span data-stu-id="19447-121">Document</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="19447-122">Remarques</span><span class="sxs-lookup"><span data-stu-id="19447-122">Notes</span></span> <br/>          | <span data-ttu-id="19447-123">Les consommateurs compatibles XPS doivent s’assurer qu’une référence URI à une ressource telle qu’une image ou un profil de couleurs dans un document de fonctionnalités d’impression ou un PrintTicket doit faire référence à un nom de partie (un URI relatif à la racine du package) dans le même package de document XPS qui contient le PrintTicket résultant.</span><span class="sxs-lookup"><span data-stu-id="19447-123">XPS-compliant consumers MUST enforce that a URI reference to a resource such as an image or color profile in either a Print Capabilities document or PrintTicket MUST refer to a part name (a relative URI to the package root) within the same XPS Document package that contains the resultant PrintTicket.</span></span> <span data-ttu-id="19447-124">Un consommateur XPS conforme ne doit pas utiliser un URI qui n’est pas conforme à la syntaxe du nom de la partie.</span><span class="sxs-lookup"><span data-stu-id="19447-124">A compliant XPS consumer MUST NOT use a URI that is not compliant with the part name syntax.</span></span> <span data-ttu-id="19447-125">Ces paramètres sont spécifiques à XPS.</span><span class="sxs-lookup"><span data-stu-id="19447-125">These settings are XPS specific.</span></span> <br/> <span data-ttu-id="19447-126">Les URI référencés dans un document de fonctionnalités d’impression ou un PrintTicket ne doivent pas être résolus en tant qu’URL.</span><span class="sxs-lookup"><span data-stu-id="19447-126">URIs which are referenced in either a Print Capabilities document or PrintTicket MUST NOT be resolved as URLs.</span></span> <span data-ttu-id="19447-127">Cela ne peut pas être résolu comme prévu et peut créer des risques de sécurité néfastes pour le pilote et le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="19447-127">This is unsafe as they may not resolve as intended and may create harmful security risks for the driver and operating system.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="19447-128">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="19447-128">Structural Content</span></span>

<span data-ttu-id="19447-129">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="19447-129">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:DocumentCoverFront">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <!-- Specifies the XPS specific part name for the front cover sheet. -->
    <psf:ScoredProperty name="psk:CoverFrontSource">
      <psf:ParameterRef name="psk:DocumentCoverFrontSource" />
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
      
```

## <a name="structure-variables"></a><span data-ttu-id="19447-130">Variables de structure</span><span class="sxs-lookup"><span data-stu-id="19447-130">Structure Variables</span></span>

<span data-ttu-id="19447-131">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="19447-131">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="19447-132">Nom</span><span class="sxs-lookup"><span data-stu-id="19447-132">Name</span></span>                               | <span data-ttu-id="19447-133">Type de données</span><span class="sxs-lookup"><span data-stu-id="19447-133">Data type</span></span>         | <span data-ttu-id="19447-134">Unité</span><span class="sxs-lookup"><span data-stu-id="19447-134">Unit</span></span>                  | <span data-ttu-id="19447-135">Valeurs prises en charge</span><span class="sxs-lookup"><span data-stu-id="19447-135">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="19447-136">Résumé</span><span class="sxs-lookup"><span data-stu-id="19447-136">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="19447-137">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="19447-137">\_OptionName\_</span></span><br/>          | <span data-ttu-id="19447-138">string</span><span class="sxs-lookup"><span data-stu-id="19447-138">string</span></span><br/> | <span data-ttu-id="19447-139">caractères</span><span class="sxs-lookup"><span data-stu-id="19447-139">characters</span></span><br/> | <span data-ttu-id="19447-140">Nom complet valide tel que défini par les [espaces de noms dans XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="19447-140">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="19447-141">Si aucun espace de noms n’est spécifié, l’espace de noms par défaut est utilisé.</span><span class="sxs-lookup"><span data-stu-id="19447-141">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="19447-142">Nom de l'option.</span><span class="sxs-lookup"><span data-stu-id="19447-142">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="19447-143">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="19447-143">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="19447-144">string</span><span class="sxs-lookup"><span data-stu-id="19447-144">string</span></span><br/> | <span data-ttu-id="19447-145">n/a</span><span class="sxs-lookup"><span data-stu-id="19447-145">n/a</span></span><br/>        | <span data-ttu-id="19447-146">True, False.</span><span class="sxs-lookup"><span data-stu-id="19447-146">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="19447-147">Définit une option qui, lorsqu’elle est sélectionnée, désactive cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="19447-147">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="19447-148">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="19447-148">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="19447-149">Les mots clés de schéma d’impression publics sont définis dans l' https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords espace de noms.</span><span class="sxs-lookup"><span data-stu-id="19447-149">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="19447-150">Le contenu de la Extensible Markup Language publique (XML) pour ce mot clé est défini ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="19447-150">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:DocumentCoverFront">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies no cover will be output -->
  <psf:Option name="psk:NoCover" />
  <!-- Specifies the cover indicated by "CoverFrontSource" should be printed on the back side 
       of the cover sheet.  If a DocumentCoverFrontSource ParameterInit element is not specified, 
       this Option should be ignored. -->
  <psf:Option name="psk:PrintBack">
    <psf:ScoredProperty name="psk:CoverFrontSource">
      <psf:ParameterRef name="psk:DocumentCoverFrontSource" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies the cover indicated by "CoverFrontSource" may be printed on either side 
       of the cover sheet.  If a DocumentCoverFrontSource ParameterInit element is not specified, 
       this Option should be ignored. -->
  <psf:Option name="psk:PrintBoth">
    <psf:ScoredProperty name="psk:CoverFrontSource">
      <psf:ParameterRef name="psk:DocumentCoverFrontSource" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies the cover indicated by "CoverFrontSource" should be printed on the front side 
       of the cover sheet.  If a DocumentCoverFrontSource ParameterInit element is not specified, 
       this Option should be ignored. -->
  <psf:Option name="psk:PrintFront">
    <psf:ScoredProperty name="psk:CoverFrontSource">
      <psf:ParameterRef name="psk:DocumentCoverFrontSource" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies a blank cover sheet should be printed. -->
  <psf:Option name="psk:BlankCover" />
</psf:Feature>    
```

## <a name="related-topics"></a><span data-ttu-id="19447-151">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="19447-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="19447-152">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="19447-152">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




