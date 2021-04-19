---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: c10da176-946a-4439-8ad7-037013b39e41
title: DocumentBannerSheet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bac772fdbd9bf378716c42362dc1657a100f1231
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "106539809"
---
# <a name="documentbannersheet"></a><span data-ttu-id="eecd8-104">DocumentBannerSheet</span><span class="sxs-lookup"><span data-stu-id="eecd8-104">DocumentBannerSheet</span></span>

<span data-ttu-id="eecd8-105">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="eecd8-105">This topic is not current.</span></span> <span data-ttu-id="eecd8-106">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="eecd8-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="eecd8-107">Décrit la feuille de bannière à générer pour un document particulier.</span><span class="sxs-lookup"><span data-stu-id="eecd8-107">Describes the banner sheet to be output for a particular document.</span></span> <span data-ttu-id="eecd8-108">La feuille de bannière doit être sortie sur le PageMediaSize par défaut, en utilisant le PageMediaType par défaut.</span><span class="sxs-lookup"><span data-stu-id="eecd8-108">The banner sheet should be output on the default PageMediaSize ,using the default PageMediaType.</span></span> <span data-ttu-id="eecd8-109">La feuille de bannière doit également être isolée du reste du document.</span><span class="sxs-lookup"><span data-stu-id="eecd8-109">The banner sheet should also be isolated from the remainder of the document.</span></span> <span data-ttu-id="eecd8-110">Cela signifie que toutes les options de finition de document ou de traitement (comme DocumentDuplex, DocumentStaple ou DocumentBinding) ne doivent pas inclure la feuille de bannière.</span><span class="sxs-lookup"><span data-stu-id="eecd8-110">This means that any document finishing or processing options (such as DocumentDuplex, DocumentStaple, or DocumentBinding) should not include the banner sheet.</span></span> <span data-ttu-id="eecd8-111">La feuille de bannière peut être isolée ou non du reste du travail.</span><span class="sxs-lookup"><span data-stu-id="eecd8-111">The banner sheet may or may not be isolated from the remainder of the job.</span></span> <span data-ttu-id="eecd8-112">Cela signifie que toutes les options de fin de tâche ou de traitement peuvent inclure la feuille de bannière de document.</span><span class="sxs-lookup"><span data-stu-id="eecd8-112">This means that any job finishing or processing options, may include the document banner sheet.</span></span> <span data-ttu-id="eecd8-113">La bannière doit avoir la première feuille du document.</span><span class="sxs-lookup"><span data-stu-id="eecd8-113">The banner sheet should occur as the first sheet of the document.</span></span>

-   [<span data-ttu-id="eecd8-114">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="eecd8-114">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="eecd8-115">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="eecd8-115">Structural Content</span></span>](#structural-content)

## <a name="element-information"></a><span data-ttu-id="eecd8-116">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="eecd8-116">Element Information</span></span>



| <span data-ttu-id="eecd8-117">Nom</span><span class="sxs-lookup"><span data-stu-id="eecd8-117">Name</span></span>                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eecd8-118">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="eecd8-118">Element Type</span></span> <br/>   | <span data-ttu-id="eecd8-119">Fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="eecd8-119">Feature</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="eecd8-120">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="eecd8-120">Scoping Prefix</span></span> <br/> | <span data-ttu-id="eecd8-121">Document</span><span class="sxs-lookup"><span data-stu-id="eecd8-121">Document</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="eecd8-122">Notes</span><span class="sxs-lookup"><span data-stu-id="eecd8-122">Notes</span></span> <br/>          | <span data-ttu-id="eecd8-123">Les consommateurs compatibles XPS doivent s’assurer qu’une référence URI à une ressource telle qu’une image ou un profil de couleurs dans un document de fonctionnalités d’impression ou un PrintTicket doit faire référence à un nom de partie (un URI relatif à la racine du package) dans le même package de document XPS qui contient le PrintTicket résultant.</span><span class="sxs-lookup"><span data-stu-id="eecd8-123">XPS-compliant consumers MUST enforce that a URI reference to a resource such as an image or color profile in either a Print Capabilities document or PrintTicket MUST refer to a part name (a relative URI to the package root) within the same XPS Document package that contains the resultant PrintTicket.</span></span> <span data-ttu-id="eecd8-124">Un consommateur XPS conforme ne doit pas utiliser un URI qui n’est pas conforme à la syntaxe du nom de la partie.</span><span class="sxs-lookup"><span data-stu-id="eecd8-124">A compliant XPS consumer MUST NOT use a URI that is not compliant with the part name syntax.</span></span> <span data-ttu-id="eecd8-125">Ces paramètres sont spécifiques à XPS.</span><span class="sxs-lookup"><span data-stu-id="eecd8-125">These settings are XPS specific.</span></span> <br/> <span data-ttu-id="eecd8-126">Les URI référencés dans un document de fonctionnalités d’impression ou un PrintTicket ne doivent pas être résolus en tant qu’URL.</span><span class="sxs-lookup"><span data-stu-id="eecd8-126">URIs which are referenced in either a Print Capabilities document or PrintTicket MUST NOT be resolved as URLs.</span></span> <span data-ttu-id="eecd8-127">Cela ne peut pas être résolu comme prévu et peut créer des risques de sécurité néfastes pour le pilote et le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="eecd8-127">This is unsafe as they may not resolve as intended and may create harmful security risks for the driver and operating system.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="eecd8-128">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="eecd8-128">Structural Content</span></span>

<span data-ttu-id="eecd8-129">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="eecd8-129">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="eecd8-130">Variables de structure</span><span class="sxs-lookup"><span data-stu-id="eecd8-130">Structure Variables</span></span>

<span data-ttu-id="eecd8-131">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="eecd8-131">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="eecd8-132">Nom</span><span class="sxs-lookup"><span data-stu-id="eecd8-132">Name</span></span>                               | <span data-ttu-id="eecd8-133">Type de données</span><span class="sxs-lookup"><span data-stu-id="eecd8-133">Data type</span></span>         | <span data-ttu-id="eecd8-134">Unité</span><span class="sxs-lookup"><span data-stu-id="eecd8-134">Unit</span></span>                   | <span data-ttu-id="eecd8-135">Valeurs prises en charge</span><span class="sxs-lookup"><span data-stu-id="eecd8-135">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="eecd8-136">Résumé</span><span class="sxs-lookup"><span data-stu-id="eecd8-136">Summary</span></span>                                                                      |
|------------------------------------|-------------------|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="eecd8-137">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="eecd8-137">\_OptionName\_</span></span><br/>          | <span data-ttu-id="eecd8-138">string</span><span class="sxs-lookup"><span data-stu-id="eecd8-138">string</span></span><br/> | <span data-ttu-id="eecd8-139">caractères</span><span class="sxs-lookup"><span data-stu-id="eecd8-139">characters</span></span> <br/> | <span data-ttu-id="eecd8-140">Nom complet valide tel que défini par les [espaces de noms dans XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="eecd8-140">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="eecd8-141">Si aucun espace de noms n’est spécifié, l’espace de noms par défaut est utilisé.</span><span class="sxs-lookup"><span data-stu-id="eecd8-141">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="eecd8-142">Nom de l’option</span><span class="sxs-lookup"><span data-stu-id="eecd8-142">The name of the option</span></span><br/>                                            |
| <span data-ttu-id="eecd8-143">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="eecd8-143">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="eecd8-144">string</span><span class="sxs-lookup"><span data-stu-id="eecd8-144">string</span></span><br/> | <span data-ttu-id="eecd8-145">n/a</span><span class="sxs-lookup"><span data-stu-id="eecd8-145">n/a</span></span><br/>         | <span data-ttu-id="eecd8-146">True, False</span><span class="sxs-lookup"><span data-stu-id="eecd8-146">True, False</span></span><br/>                                                                                                                                                                | <span data-ttu-id="eecd8-147">Définit une option qui, lorsqu’elle est sélectionnée, désactive cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="eecd8-147">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="eecd8-148">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="eecd8-148">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="eecd8-149">Les mots clés de schéma d’impression publics sont définis dans l' https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords espace de noms.</span><span class="sxs-lookup"><span data-stu-id="eecd8-149">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="eecd8-150">Le contenu de la Extensible Markup Language publique (XML) pour ce mot clé est défini ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="eecd8-150">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="eecd8-151">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="eecd8-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eecd8-152">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="eecd8-152">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




