---
description: En savoir plus sur l’élément JobErrorSheet, qui décrit la sortie de la feuille d’erreur. La totalité du travail aura une seule feuille d’erreur.
ms.assetid: ad30df59-0051-4471-8c0e-3207bcc7bfbe
title: JobErrorSheet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6dcee6c50d482793eeef96e29ad98385da11a4e6
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408902"
---
# <a name="joberrorsheet"></a><span data-ttu-id="36531-104">JobErrorSheet</span><span class="sxs-lookup"><span data-stu-id="36531-104">JobErrorSheet</span></span>

<span data-ttu-id="36531-105">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="36531-105">This topic is not current.</span></span> <span data-ttu-id="36531-106">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="36531-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="36531-107">Décrit la sortie de la feuille d’erreur.</span><span class="sxs-lookup"><span data-stu-id="36531-107">Describes the error sheet output.</span></span> <span data-ttu-id="36531-108">La totalité du travail aura une seule feuille d’erreur.</span><span class="sxs-lookup"><span data-stu-id="36531-108">The entire job will have a single error sheet.</span></span> <span data-ttu-id="36531-109">La feuille d’erreur doit être sortie sur le PageMediaSize par défaut et utiliser le PageMediaType par défaut.</span><span class="sxs-lookup"><span data-stu-id="36531-109">The error sheet should be output on the default PageMediaSize and using the default PageMediaType.</span></span> <span data-ttu-id="36531-110">La feuille d’erreur doit être isolée du reste du travail.</span><span class="sxs-lookup"><span data-stu-id="36531-110">The error sheet should to be isolated from the remainder of the job.</span></span> <span data-ttu-id="36531-111">Cela signifie que toutes les options de finition ou de traitement (telles que JobDuplex, JobStaple ou JobBinding) ne doivent pas inclure la feuille d’erreur.</span><span class="sxs-lookup"><span data-stu-id="36531-111">This means that any finishing or processing options (such as JobDuplex, JobStaple, or JobBinding) should not include the error sheet.</span></span> <span data-ttu-id="36531-112">La feuille d’erreur doit se produire comme la dernière feuille du travail.</span><span class="sxs-lookup"><span data-stu-id="36531-112">The error sheet should occur as the final sheet of the job.</span></span>

-   [<span data-ttu-id="36531-113">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="36531-113">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="36531-114">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="36531-114">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="36531-115">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="36531-115">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="36531-116">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="36531-116">Element Information</span></span>



| <span data-ttu-id="36531-117">Nom</span><span class="sxs-lookup"><span data-stu-id="36531-117">Name</span></span> | <span data-ttu-id="36531-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="36531-118">Value</span></span> |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="36531-119">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="36531-119">Element Type</span></span> <br/>   | <span data-ttu-id="36531-120">Fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="36531-120">Feature</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="36531-121">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="36531-121">Scoping Prefix</span></span> <br/> | <span data-ttu-id="36531-122">Travail</span><span class="sxs-lookup"><span data-stu-id="36531-122">Job</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="36531-123">Notes</span><span class="sxs-lookup"><span data-stu-id="36531-123">Notes</span></span> <br/>          | <span data-ttu-id="36531-124">Les consommateurs compatibles XPS doivent s’assurer qu’une référence URI à une ressource telle qu’une image ou un profil de couleurs dans un document de fonctionnalités d’impression ou un PrintTicket doit faire référence à un nom de partie (un URI relatif à la racine du package) dans le même package de document XPS qui contient le PrintTicket résultant.</span><span class="sxs-lookup"><span data-stu-id="36531-124">XPS-compliant consumers MUST enforce that a URI reference to a resource such as an image or color profile in either a Print Capabilities document or PrintTicket MUST refer to a part name (a relative URI to the package root) within the same XPS Document package that contains the resultant PrintTicket.</span></span> <span data-ttu-id="36531-125">Un consommateur XPS conforme ne doit pas utiliser un URI qui n’est pas conforme à la syntaxe du nom de la partie.</span><span class="sxs-lookup"><span data-stu-id="36531-125">A compliant XPS consumer MUST NOT use a URI that is not compliant with the part name syntax.</span></span> <span data-ttu-id="36531-126">Ces paramètres sont spécifiques à XPS.</span><span class="sxs-lookup"><span data-stu-id="36531-126">These settings are XPS specific.</span></span> <br/> <span data-ttu-id="36531-127">Les URI référencés dans un document de fonctionnalités d’impression ou un PrintTicket ne doivent pas être résolus en tant qu’URL.</span><span class="sxs-lookup"><span data-stu-id="36531-127">URIs which are referenced in either a Print Capabilities document or PrintTicket MUST NOT be resolved as URLs.</span></span> <span data-ttu-id="36531-128">Cela ne peut pas être résolu comme prévu et peut créer des risques de sécurité néfastes pour le pilote et le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="36531-128">This is unsafe as they may not resolve as intended and may create harmful security risks for the driver and operating system.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="36531-129">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="36531-129">Structural Content</span></span>

<span data-ttu-id="36531-130">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="36531-130">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:JobErrorSheet">
  <!--Describes when an error sheet should be output. -->
  <psf:Feature name="psk:ErrorSheetWhen">
    <psf:Property name="psf:SelectionType">
      <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
    </psf:Property>
    <psf:Option name="psk:_ErrorSheetWhenOptionName_">
      <psf:Property name="psf:IdentityOption">
        <psf:Value xsi:type="xs:string">_ErrorSheetWhenIdentityOptionValue_</psf:Value>
      </psf:Property>
    </psf:Option>
  </psf:Feature>
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <!-- Specifies the XPS part name for the error sheet. -->
    <psf:ScoredProperty name="psk:ErrorSheetSource">
      <psf:ParameterRef name="psk:JobErrorSheetSource" />
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>      
```

## <a name="structure-variables"></a><span data-ttu-id="36531-131">Variables de structure</span><span class="sxs-lookup"><span data-stu-id="36531-131">Structure Variables</span></span>

<span data-ttu-id="36531-132">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="36531-132">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="36531-133">Nom</span><span class="sxs-lookup"><span data-stu-id="36531-133">Name</span></span>                                             | <span data-ttu-id="36531-134">Type de données</span><span class="sxs-lookup"><span data-stu-id="36531-134">Data type</span></span>         | <span data-ttu-id="36531-135">Unité</span><span class="sxs-lookup"><span data-stu-id="36531-135">Unit</span></span>                  | <span data-ttu-id="36531-136">Valeurs prises en charge</span><span class="sxs-lookup"><span data-stu-id="36531-136">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="36531-137">Résumé</span><span class="sxs-lookup"><span data-stu-id="36531-137">Summary</span></span>                                                                      |
|--------------------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="36531-138">\_ErrorSheetWhenOptionName\_</span><span class="sxs-lookup"><span data-stu-id="36531-138">\_ErrorSheetWhenOptionName\_</span></span><br/>          | <span data-ttu-id="36531-139">string</span><span class="sxs-lookup"><span data-stu-id="36531-139">string</span></span><br/> | <span data-ttu-id="36531-140">caractères</span><span class="sxs-lookup"><span data-stu-id="36531-140">characters</span></span><br/> | <span data-ttu-id="36531-141">Nom complet valide tel que défini par les [espaces de noms dans XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="36531-141">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="36531-142">Si aucun espace de noms n’est spécifié, l’espace de noms par défaut est utilisé.</span><span class="sxs-lookup"><span data-stu-id="36531-142">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="36531-143">Nom de l'option.</span><span class="sxs-lookup"><span data-stu-id="36531-143">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="36531-144">\_ErrorSheetWhenIdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="36531-144">\_ErrorSheetWhenIdentityOptionValue\_</span></span><br/> | <span data-ttu-id="36531-145">string</span><span class="sxs-lookup"><span data-stu-id="36531-145">string</span></span><br/> | <span data-ttu-id="36531-146">n/a</span><span class="sxs-lookup"><span data-stu-id="36531-146">n/a</span></span><br/>        | <span data-ttu-id="36531-147">True, False.</span><span class="sxs-lookup"><span data-stu-id="36531-147">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="36531-148">Définit les critères de sélection de l’interface utilisateur (IU).</span><span class="sxs-lookup"><span data-stu-id="36531-148">Defines the user interface (UI) selection criteria.</span></span><br/>               |
| <span data-ttu-id="36531-149">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="36531-149">\_OptionName\_</span></span><br/>                        | <span data-ttu-id="36531-150">string</span><span class="sxs-lookup"><span data-stu-id="36531-150">string</span></span><br/> | <span data-ttu-id="36531-151">n/a</span><span class="sxs-lookup"><span data-stu-id="36531-151">n/a</span></span><br/>        | <span data-ttu-id="36531-152">Nom complet valide tel que défini par https://www.w3.org/TR/1999/REC-xml-names-19990114/\#dt-qname .</span><span class="sxs-lookup"><span data-stu-id="36531-152">Valid fully qualified name as defined by https://www.w3.org/TR/1999/REC-xml-names-19990114/\#dt-qname.</span></span> <span data-ttu-id="36531-153">Si aucun espace de noms n’est spécifié, l’espace de noms par défaut est utilisé.</span><span class="sxs-lookup"><span data-stu-id="36531-153">If no namespace is specified, default namespace is assumed.</span></span><br/>          | <span data-ttu-id="36531-154">Nom de l'option.</span><span class="sxs-lookup"><span data-stu-id="36531-154">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="36531-155">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="36531-155">\_IdentityOptionValue\_</span></span><br/>               | <span data-ttu-id="36531-156">string</span><span class="sxs-lookup"><span data-stu-id="36531-156">string</span></span><br/> | <span data-ttu-id="36531-157">n/a</span><span class="sxs-lookup"><span data-stu-id="36531-157">n/a</span></span><br/>        | <span data-ttu-id="36531-158">True, False.</span><span class="sxs-lookup"><span data-stu-id="36531-158">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="36531-159">Définit une option qui, lorsqu’elle est sélectionnée, désactive cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="36531-159">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="36531-160">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="36531-160">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="36531-161">Les mots clés de schéma d’impression publics sont définis dans l' https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords espace de noms.</span><span class="sxs-lookup"><span data-stu-id="36531-161">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="36531-162">Le contenu de la Extensible Markup Language publique (XML) pour ce mot clé est défini ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="36531-162">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:JobErrorSheet">
  <psf:Feature name="psk:ErrorSheetWhen">
    <psf:Property name="psf:SelectionType">
      <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
    </psf:Property>
    <!-- Specifies an error sheet will be output for every job. -->
    <psf:Option name="psk:Always" />
    <!-- Specifies an error sheet will be output only on error. -->
    <psf:Option name="psk:OnError" />
  </psf:Feature>
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies a custom error sheet should be output. If a JobErrorSheetSource 
     ParameterInit element is not specified, this Option should be ignored. -->
  <psf:Option name="psk:Custom">
    <psf:ScoredProperty name="psk:ErrorSheetSource">
      <psf:ParameterRef name="psk:JobErrorSheetSource" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies no error sheet should be output. -->
  <psf:Option name="psk:None" />
  <!-- Specifies the standard (device defined) error sheet should be output. -->
  <psf:Option name="psk:Standard" />
</psf:Feature>    
```

## <a name="related-topics"></a><span data-ttu-id="36531-163">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="36531-163">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="36531-164">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="36531-164">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




