---
description: En savoir plus sur l’élément JobPrimaryBannerSheet, qui décrit la feuille de bannière à générer pour le travail.
ms.assetid: c8f9001e-9f92-405a-8f3a-bc59b47c9e35
title: JobPrimaryBannerSheet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39922f65d71ea0cc6d6de6103bc159f79467038f
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408752"
---
# <a name="jobprimarybannersheet"></a><span data-ttu-id="40b4f-103">JobPrimaryBannerSheet</span><span class="sxs-lookup"><span data-stu-id="40b4f-103">JobPrimaryBannerSheet</span></span>

<span data-ttu-id="40b4f-104">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="40b4f-104">This topic is not current.</span></span> <span data-ttu-id="40b4f-105">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="40b4f-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="40b4f-106">Décrit la feuille de bannière à générer pour le travail.</span><span class="sxs-lookup"><span data-stu-id="40b4f-106">Describes the banner sheet to be output for the job.</span></span> <span data-ttu-id="40b4f-107">La feuille de bannière doit être sortie sur le PageMediaSize par défaut et utiliser le PageMediaType par défaut.</span><span class="sxs-lookup"><span data-stu-id="40b4f-107">The banner sheet should be output on the default PageMediaSize and using the default PageMediaType.</span></span> <span data-ttu-id="40b4f-108">La feuille de bannière doit être isolée du reste du travail.</span><span class="sxs-lookup"><span data-stu-id="40b4f-108">The banner sheet should be isolated from the remainder of the job.</span></span> <span data-ttu-id="40b4f-109">Cela signifie que les options de finition ou de traitement (telles que JobDuplexAllDocumentsContiguously, JobStapleAllDocuments ou JobBindAllDocuments) ne doivent pas inclure la feuille de bannière.</span><span class="sxs-lookup"><span data-stu-id="40b4f-109">This means that any finishing or processing options (such as JobDuplexAllDocumentsContiguously, JobStapleAllDocuments, or JobBindAllDocuments) should not include the banner sheet.</span></span> <span data-ttu-id="40b4f-110">La feuille de bannière doit se produire comme la première feuille du travail.</span><span class="sxs-lookup"><span data-stu-id="40b4f-110">The banner sheet should occur as the first sheet of the job.</span></span>

-   [<span data-ttu-id="40b4f-111">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="40b4f-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="40b4f-112">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="40b4f-112">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="40b4f-113">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="40b4f-113">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="40b4f-114">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="40b4f-114">Element Information</span></span>



| <span data-ttu-id="40b4f-115">Nom</span><span class="sxs-lookup"><span data-stu-id="40b4f-115">Name</span></span> | <span data-ttu-id="40b4f-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="40b4f-116">Value</span></span> |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="40b4f-117">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="40b4f-117">Element Type</span></span> <br/>   | <span data-ttu-id="40b4f-118">Fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="40b4f-118">Feature</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="40b4f-119">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="40b4f-119">Scoping Prefix</span></span> <br/> | <span data-ttu-id="40b4f-120">Travail</span><span class="sxs-lookup"><span data-stu-id="40b4f-120">Job</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="40b4f-121">Notes</span><span class="sxs-lookup"><span data-stu-id="40b4f-121">Notes</span></span> <br/>          | <span data-ttu-id="40b4f-122">Les consommateurs compatibles XPS doivent s’assurer qu’une référence URI à une ressource telle qu’une image ou un profil de couleurs dans un document de fonctionnalités d’impression ou un PrintTicket doit faire référence à un nom de partie (un URI relatif à la racine du package) dans le même package de document XPS qui contient le PrintTicket résultant.</span><span class="sxs-lookup"><span data-stu-id="40b4f-122">XPS-compliant consumers MUST enforce that a URI reference to a resource such as an image or color profile in either a Print Capabilities document or PrintTicket MUST refer to a part name (a relative URI to the package root) within the same XPS Document package that contains the resultant PrintTicket.</span></span> <span data-ttu-id="40b4f-123">Un consommateur XPS conforme ne doit pas utiliser un URI qui n’est pas conforme à la syntaxe du nom de la partie.</span><span class="sxs-lookup"><span data-stu-id="40b4f-123">A compliant XPS consumer MUST NOT use a URI that is not compliant with the part name syntax.</span></span> <span data-ttu-id="40b4f-124">Ces paramètres sont spécifiques à XPS.</span><span class="sxs-lookup"><span data-stu-id="40b4f-124">These settings are XPS specific.</span></span> <br/> <span data-ttu-id="40b4f-125">Les URI référencés dans un document de fonctionnalités d’impression ou un PrintTicket ne doivent pas être résolus en tant qu’URL.</span><span class="sxs-lookup"><span data-stu-id="40b4f-125">URIs which are referenced in either a Print Capabilities document or PrintTicket MUST NOT be resolved as URLs.</span></span> <span data-ttu-id="40b4f-126">Cela ne peut pas être résolu comme prévu et peut créer des risques de sécurité néfastes pour le pilote et le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="40b4f-126">This is unsafe as they may not resolve as intended and may create harmful security risks for the driver and operating system.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="40b4f-127">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="40b4f-127">Structural Content</span></span>

<span data-ttu-id="40b4f-128">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="40b4f-128">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:JobPrimaryBannerSheet">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <!-- Specifies the XPS part name for the banner sheet. -->
    <psf:ScoredProperty name="psk:BannerSheetSource">
      <psf:ParameterRef name="psk:JobPrimaryBannerSheetSource" />
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
```

## <a name="structure-variables"></a><span data-ttu-id="40b4f-129">Variables de structure</span><span class="sxs-lookup"><span data-stu-id="40b4f-129">Structure Variables</span></span>

<span data-ttu-id="40b4f-130">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="40b4f-130">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="40b4f-131">Nom</span><span class="sxs-lookup"><span data-stu-id="40b4f-131">Name</span></span>                               | <span data-ttu-id="40b4f-132">Type de données</span><span class="sxs-lookup"><span data-stu-id="40b4f-132">Data type</span></span>         | <span data-ttu-id="40b4f-133">Unité</span><span class="sxs-lookup"><span data-stu-id="40b4f-133">Unit</span></span>                  | <span data-ttu-id="40b4f-134">Valeurs prises en charge</span><span class="sxs-lookup"><span data-stu-id="40b4f-134">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="40b4f-135">Résumé</span><span class="sxs-lookup"><span data-stu-id="40b4f-135">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="40b4f-136">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="40b4f-136">\_OptionName\_</span></span><br/>          | <span data-ttu-id="40b4f-137">string</span><span class="sxs-lookup"><span data-stu-id="40b4f-137">string</span></span><br/> | <span data-ttu-id="40b4f-138">caractères</span><span class="sxs-lookup"><span data-stu-id="40b4f-138">characters</span></span><br/> | <span data-ttu-id="40b4f-139">Nom complet valide tel que défini par les [espaces de noms dans XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="40b4f-139">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="40b4f-140">Si aucun espace de noms n’est spécifié, l’espace de noms par défaut est utilisé.</span><span class="sxs-lookup"><span data-stu-id="40b4f-140">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="40b4f-141">Nom de l'option.</span><span class="sxs-lookup"><span data-stu-id="40b4f-141">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="40b4f-142">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="40b4f-142">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="40b4f-143">string</span><span class="sxs-lookup"><span data-stu-id="40b4f-143">string</span></span><br/> | <span data-ttu-id="40b4f-144">n/a</span><span class="sxs-lookup"><span data-stu-id="40b4f-144">n/a</span></span><br/>        | <span data-ttu-id="40b4f-145">True, False.</span><span class="sxs-lookup"><span data-stu-id="40b4f-145">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="40b4f-146">Définit une option qui, lorsqu’elle est sélectionnée, désactive cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="40b4f-146">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="40b4f-147">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="40b4f-147">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="40b4f-148">Les mots clés de schéma d’impression publics sont définis dans l' https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords espace de noms.</span><span class="sxs-lookup"><span data-stu-id="40b4f-148">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="40b4f-149">Le contenu de la Extensible Markup Language publique (XML) pour ce mot clé est défini ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="40b4f-149">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:JobPrimaryBannerSheet">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies a custom banner sheet should be output. If a JobPrimaryBannerSheetSource 
     ParameterInit element is not specified, this Option should be ignored.  -->
  <psf:Option name="psk:Custom">
    <psf:ScoredProperty name="psk:BannerSheetSource">
      <psf:ParameterRef name="psk:JobPrimaryBannerSheetSource" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies no banner sheet should be output. -->
  <psf:Option name="psk:None" />
  <!-- Specifies the standard (device defined) banner sheet should be output. -->
  <psf:Option name="psk:Standard" />
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="40b4f-150">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="40b4f-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="40b4f-151">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="40b4f-151">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




