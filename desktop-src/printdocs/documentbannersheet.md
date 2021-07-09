---
description: En savoir plus sur l’élément configurable par l’utilisateur DocumentBannerSheet. Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: c10da176-946a-4439-8ad7-037013b39e41
title: DocumentBannerSheet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80ce05ffae190835e4a8b4082c634b34e26103ab
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/09/2021
ms.locfileid: "113548767"
---
# <a name="documentbannersheet"></a><span data-ttu-id="fb429-105">DocumentBannerSheet</span><span class="sxs-lookup"><span data-stu-id="fb429-105">DocumentBannerSheet</span></span>

<span data-ttu-id="fb429-106">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="fb429-106">This topic is not current.</span></span> <span data-ttu-id="fb429-107">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="fb429-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="fb429-108">Décrit la feuille de bannière à générer pour un document particulier.</span><span class="sxs-lookup"><span data-stu-id="fb429-108">Describes the banner sheet to be output for a particular document.</span></span> <span data-ttu-id="fb429-109">La feuille de bannière doit être sortie sur le PageMediaSize par défaut, en utilisant le PageMediaType par défaut.</span><span class="sxs-lookup"><span data-stu-id="fb429-109">The banner sheet should be output on the default PageMediaSize ,using the default PageMediaType.</span></span> <span data-ttu-id="fb429-110">La feuille de bannière doit également être isolée du reste du document.</span><span class="sxs-lookup"><span data-stu-id="fb429-110">The banner sheet should also be isolated from the remainder of the document.</span></span> <span data-ttu-id="fb429-111">Cela signifie que toutes les options de finition de document ou de traitement (comme DocumentDuplex, DocumentStaple ou DocumentBinding) ne doivent pas inclure la feuille de bannière.</span><span class="sxs-lookup"><span data-stu-id="fb429-111">This means that any document finishing or processing options (such as DocumentDuplex, DocumentStaple, or DocumentBinding) should not include the banner sheet.</span></span> <span data-ttu-id="fb429-112">La feuille de bannière peut être isolée ou non du reste du travail.</span><span class="sxs-lookup"><span data-stu-id="fb429-112">The banner sheet may or may not be isolated from the remainder of the job.</span></span> <span data-ttu-id="fb429-113">Cela signifie que toutes les options de fin de tâche ou de traitement peuvent inclure la feuille de bannière de document.</span><span class="sxs-lookup"><span data-stu-id="fb429-113">This means that any job finishing or processing options, may include the document banner sheet.</span></span> <span data-ttu-id="fb429-114">La bannière doit avoir la première feuille du document.</span><span class="sxs-lookup"><span data-stu-id="fb429-114">The banner sheet should occur as the first sheet of the document.</span></span>

-   [<span data-ttu-id="fb429-115">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="fb429-115">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="fb429-116">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="fb429-116">Structural Content</span></span>](#structural-content)

## <a name="element-information"></a><span data-ttu-id="fb429-117">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="fb429-117">Element Information</span></span>



| <span data-ttu-id="fb429-118">Nom</span><span class="sxs-lookup"><span data-stu-id="fb429-118">Name</span></span> | <span data-ttu-id="fb429-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="fb429-119">Value</span></span> |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb429-120">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="fb429-120">Element Type</span></span> <br/>   | <span data-ttu-id="fb429-121">Composant</span><span class="sxs-lookup"><span data-stu-id="fb429-121">Feature</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="fb429-122">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="fb429-122">Scoping Prefix</span></span> <br/> | <span data-ttu-id="fb429-123">Document</span><span class="sxs-lookup"><span data-stu-id="fb429-123">Document</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="fb429-124">Remarques</span><span class="sxs-lookup"><span data-stu-id="fb429-124">Notes</span></span> <br/>          | <span data-ttu-id="fb429-125">Les consommateurs compatibles XPS doivent s’assurer qu’une référence URI à une ressource telle qu’une image ou un profil de couleurs dans un document de fonctionnalités d’impression ou un PrintTicket doit faire référence à un nom de partie (un URI relatif à la racine du package) dans le même package de document XPS qui contient le PrintTicket résultant.</span><span class="sxs-lookup"><span data-stu-id="fb429-125">XPS-compliant consumers MUST enforce that a URI reference to a resource such as an image or color profile in either a Print Capabilities document or PrintTicket MUST refer to a part name (a relative URI to the package root) within the same XPS Document package that contains the resultant PrintTicket.</span></span> <span data-ttu-id="fb429-126">Un consommateur XPS conforme ne doit pas utiliser un URI qui n’est pas conforme à la syntaxe du nom de la partie.</span><span class="sxs-lookup"><span data-stu-id="fb429-126">A compliant XPS consumer MUST NOT use a URI that is not compliant with the part name syntax.</span></span> <span data-ttu-id="fb429-127">Ces paramètres sont spécifiques à XPS.</span><span class="sxs-lookup"><span data-stu-id="fb429-127">These settings are XPS specific.</span></span> <br/> <span data-ttu-id="fb429-128">Les URI référencés dans un document de fonctionnalités d’impression ou un PrintTicket ne doivent pas être résolus en tant qu’URL.</span><span class="sxs-lookup"><span data-stu-id="fb429-128">URIs which are referenced in either a Print Capabilities document or PrintTicket MUST NOT be resolved as URLs.</span></span> <span data-ttu-id="fb429-129">Cela ne peut pas être résolu comme prévu et peut créer des risques de sécurité néfastes pour le pilote et le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="fb429-129">This is unsafe as they may not resolve as intended and may create harmful security risks for the driver and operating system.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="fb429-130">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="fb429-130">Structural Content</span></span>

<span data-ttu-id="fb429-131">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="fb429-131">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:DocumentBannerSheet">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <!-- Specifies the XPS specific part name -->
    <psf:ScoredProperty name="psk:BannerSheetSource">
      <psf:ParameterRef name="psk:DocumentBannerSheetSource" />
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
```

## <a name="structure-variables"></a><span data-ttu-id="fb429-132">Variables de structure</span><span class="sxs-lookup"><span data-stu-id="fb429-132">Structure Variables</span></span>

<span data-ttu-id="fb429-133">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="fb429-133">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="fb429-134">Nom</span><span class="sxs-lookup"><span data-stu-id="fb429-134">Name</span></span>                               | <span data-ttu-id="fb429-135">Type de données</span><span class="sxs-lookup"><span data-stu-id="fb429-135">Data type</span></span>         | <span data-ttu-id="fb429-136">Unité</span><span class="sxs-lookup"><span data-stu-id="fb429-136">Unit</span></span>                   | <span data-ttu-id="fb429-137">Valeurs prises en charge</span><span class="sxs-lookup"><span data-stu-id="fb429-137">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="fb429-138">Résumé</span><span class="sxs-lookup"><span data-stu-id="fb429-138">Summary</span></span>                                                                      |
|------------------------------------|-------------------|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="fb429-139">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="fb429-139">\_OptionName\_</span></span><br/>          | <span data-ttu-id="fb429-140">string</span><span class="sxs-lookup"><span data-stu-id="fb429-140">string</span></span><br/> | <span data-ttu-id="fb429-141">caractères</span><span class="sxs-lookup"><span data-stu-id="fb429-141">characters</span></span> <br/> | <span data-ttu-id="fb429-142">Nom complet valide tel que défini par les [espaces de noms dans XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="fb429-142">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="fb429-143">Si aucun espace de noms n’est spécifié, l’espace de noms par défaut est utilisé.</span><span class="sxs-lookup"><span data-stu-id="fb429-143">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="fb429-144">Nom de l’option</span><span class="sxs-lookup"><span data-stu-id="fb429-144">The name of the option</span></span><br/>                                            |
| <span data-ttu-id="fb429-145">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="fb429-145">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="fb429-146">string</span><span class="sxs-lookup"><span data-stu-id="fb429-146">string</span></span><br/> | <span data-ttu-id="fb429-147">n/a</span><span class="sxs-lookup"><span data-stu-id="fb429-147">n/a</span></span><br/>         | <span data-ttu-id="fb429-148">True, False</span><span class="sxs-lookup"><span data-stu-id="fb429-148">True, False</span></span><br/>                                                                                                                                                                | <span data-ttu-id="fb429-149">Définit une option qui, lorsqu’elle est sélectionnée, désactive cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="fb429-149">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="fb429-150">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="fb429-150">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="fb429-151">Les mots clés de schéma d’impression publics sont définis dans l' https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords espace de noms.</span><span class="sxs-lookup"><span data-stu-id="fb429-151">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="fb429-152">Le contenu de la Extensible Markup Language publique (XML) pour ce mot clé est défini ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="fb429-152">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:DocumentBannerSheet">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies a custom banner sheet should be output. If a DocumentBannerSheetSource 
     ParameterInit element is not specified, this Option should be ignored. -->
  <psf:Option name="psk:Custom">
    <psf:ScoredProperty name="psk:BannerSheetSource">
      <psf:ParameterRef name="psk:DocumentBannerSheetSource" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies no banner sheet should be output. -->
  <psf:Option name="psk:None" />
  <!-- Specifies the standard (device defined) banner sheet should be output. -->
  <psf:Option name="psk:Standard" />
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="fb429-153">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="fb429-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fb429-154">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="fb429-154">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




