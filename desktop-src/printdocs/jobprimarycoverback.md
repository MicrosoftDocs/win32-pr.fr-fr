---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: 83626e3c-1ce8-4c91-b656-9f0c06c5b1ec
title: JobPrimaryCoverBack
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 073e65f80c3bee31423d0cf813d454a32e6f559b
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "106532173"
---
# <a name="jobprimarycoverback"></a><span data-ttu-id="eb099-104">JobPrimaryCoverBack</span><span class="sxs-lookup"><span data-stu-id="eb099-104">JobPrimaryCoverBack</span></span>

<span data-ttu-id="eb099-105">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="eb099-105">This topic is not current.</span></span> <span data-ttu-id="eb099-106">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="eb099-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="eb099-107">Décrit la feuille de couverture Back (final).</span><span class="sxs-lookup"><span data-stu-id="eb099-107">Describes the back (ending) cover sheet.</span></span> <span data-ttu-id="eb099-108">Chaque travail aura une feuille principale distincte.</span><span class="sxs-lookup"><span data-stu-id="eb099-108">Each job will have a separate primary sheet.</span></span> <span data-ttu-id="eb099-109">La feuille de couverture doit être imprimée sur le PageMediaSize et le PageMediaType utilisés pour la dernière page du travail.</span><span class="sxs-lookup"><span data-stu-id="eb099-109">The cover sheet should be printed on the PageMediaSize and PageMediaType used for the final page of the job.</span></span> <span data-ttu-id="eb099-110">La feuille de couverture doit être intégrée dans les options de traitement (telles que JobDuplexAllDocumentsContiguously, JobNUpAllDocumentsContiguously), comme indiqué par l’option spécifiée.</span><span class="sxs-lookup"><span data-stu-id="eb099-110">The cover sheet should be integrated into processing options (such as JobDuplexAllDocumentsContiguously, JobNUpAllDocumentsContiguously) as indicated by the Option specified.</span></span>

-   [<span data-ttu-id="eb099-111">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="eb099-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="eb099-112">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="eb099-112">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="eb099-113">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="eb099-113">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="eb099-114">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="eb099-114">Element Information</span></span>



| <span data-ttu-id="eb099-115">Nom</span><span class="sxs-lookup"><span data-stu-id="eb099-115">Name</span></span>                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb099-116">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="eb099-116">Element Type</span></span> <br/>   | <span data-ttu-id="eb099-117">Fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="eb099-117">Feature</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="eb099-118">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="eb099-118">Scoping Prefix</span></span> <br/> | <span data-ttu-id="eb099-119">Travail</span><span class="sxs-lookup"><span data-stu-id="eb099-119">Job</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="eb099-120">Notes</span><span class="sxs-lookup"><span data-stu-id="eb099-120">Notes</span></span> <br/>          | <span data-ttu-id="eb099-121">Les consommateurs compatibles XPS doivent s’assurer qu’une référence URI à une ressource telle qu’une image ou un profil de couleurs dans un document de fonctionnalités d’impression ou un PrintTicket doit faire référence à un nom de partie (un URI relatif à la racine du package) dans le même package de document XPS qui contient le PrintTicket résultant.</span><span class="sxs-lookup"><span data-stu-id="eb099-121">XPS-compliant consumers MUST enforce that a URI reference to a resource such as an image or color profile in either a Print Capabilities document or PrintTicket MUST refer to a part name (a relative URI to the package root) within the same XPS Document package that contains the resultant PrintTicket.</span></span> <span data-ttu-id="eb099-122">Un consommateur XPS conforme ne doit pas utiliser un URI qui n’est pas conforme à la syntaxe du nom de la partie.</span><span class="sxs-lookup"><span data-stu-id="eb099-122">A compliant XPS consumer MUST NOT use a URI that is not compliant with the part name syntax.</span></span> <span data-ttu-id="eb099-123">Ces paramètres sont spécifiques à XPS.</span><span class="sxs-lookup"><span data-stu-id="eb099-123">These settings are XPS specific.</span></span> <br/> <span data-ttu-id="eb099-124">Les URI référencés dans un document de fonctionnalités d’impression ou un PrintTicket ne doivent pas être résolus en tant qu’URL.</span><span class="sxs-lookup"><span data-stu-id="eb099-124">URIs which are referenced in either a Print Capabilities document or PrintTicket MUST NOT be resolved as URLs.</span></span> <span data-ttu-id="eb099-125">Cela ne peut pas être résolu comme prévu et peut créer des risques de sécurité néfastes pour le pilote et le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="eb099-125">This is unsafe as they may not resolve as intended and may create harmful security risks for the driver and operating system.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="eb099-126">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="eb099-126">Structural Content</span></span>

<span data-ttu-id="eb099-127">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="eb099-127">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:JobPrimaryCoverBack">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
  <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
  <!-- Specifies the XPS part name for the back cover sheet. -->
  <psf:ScoredProperty name="psk:CoverBackSource">
      <psf:ParameterRef name="psk:JobPrimaryCoverBackSource" />
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
```

## <a name="structure-variables"></a><span data-ttu-id="eb099-128">Variables de structure</span><span class="sxs-lookup"><span data-stu-id="eb099-128">Structure Variables</span></span>

<span data-ttu-id="eb099-129">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="eb099-129">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="eb099-130">Nom</span><span class="sxs-lookup"><span data-stu-id="eb099-130">Name</span></span>                               | <span data-ttu-id="eb099-131">Type de données</span><span class="sxs-lookup"><span data-stu-id="eb099-131">Data type</span></span>         | <span data-ttu-id="eb099-132">Unité</span><span class="sxs-lookup"><span data-stu-id="eb099-132">Unit</span></span>                  | <span data-ttu-id="eb099-133">Valeurs prises en charge</span><span class="sxs-lookup"><span data-stu-id="eb099-133">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="eb099-134">Résumé</span><span class="sxs-lookup"><span data-stu-id="eb099-134">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="eb099-135">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="eb099-135">\_OptionName\_</span></span><br/>          | <span data-ttu-id="eb099-136">string</span><span class="sxs-lookup"><span data-stu-id="eb099-136">string</span></span><br/> | <span data-ttu-id="eb099-137">caractères</span><span class="sxs-lookup"><span data-stu-id="eb099-137">characters</span></span><br/> | <span data-ttu-id="eb099-138">Nom complet valide tel que défini par les [espaces de noms dans XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="eb099-138">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="eb099-139">Si aucun espace de noms n’est spécifié, l’espace de noms par défaut est utilisé.</span><span class="sxs-lookup"><span data-stu-id="eb099-139">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="eb099-140">Nom de l'option.</span><span class="sxs-lookup"><span data-stu-id="eb099-140">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="eb099-141">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="eb099-141">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="eb099-142">string</span><span class="sxs-lookup"><span data-stu-id="eb099-142">string</span></span><br/> | <span data-ttu-id="eb099-143">n/a</span><span class="sxs-lookup"><span data-stu-id="eb099-143">n/a</span></span><br/>        | <span data-ttu-id="eb099-144">True, False.</span><span class="sxs-lookup"><span data-stu-id="eb099-144">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="eb099-145">Définit une option qui, lorsqu’elle est sélectionnée, désactive cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="eb099-145">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="eb099-146">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="eb099-146">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="eb099-147">Les mots clés de schéma d’impression publics sont définis dans l' https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords espace de noms.</span><span class="sxs-lookup"><span data-stu-id="eb099-147">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="eb099-148">Le contenu de la Extensible Markup Language publique (XML) pour ce mot clé est défini ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="eb099-148">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:JobPrimaryCoverBack">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies no cover will be output -->
  <psf:Option name="psk:NoCover" />
  <!-- Specifies the cover indicated by "CoverBackSource" should be printed on the back side 
       of the cover sheet.  If a JobPrimaryCoverBackSource ParameterInit element is not specified, 
       this Option should be ignored. -->
  <psf:Option name="psk:PrintBack">
    <psf:ScoredProperty name="psk:CoverBackSource">
      <psf:ParameterRef name="psk:JobPrimaryCoverBackSource" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies the cover indicated by "CoverBackSource" may be printed on either sides 
       of the cover sheet.  If a JobPrimaryCoverBackSource ParameterInit element is not specified, 
       this Option should be ignored. -->
  <psf:Option name="psk:PrintBoth">
    <psf:ScoredProperty name="psk:CoverBackSource">
      <psf:ParameterRef name="psk:JobPrimaryCoverBackSource" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies the cover indicated by "CoverBackSource" should be printed on the front side 
       of the cover sheet.  If a JobPrimaryCoverBackSource ParameterInit element is not specified, 
       this Option should be ignored. -->
  <psf:Option name="psk:PrintFront">
    <psf:ScoredProperty name="psk:CoverBackSource">
      <psf:ParameterRef name="psk:JobPrimaryCoverBackSource" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies a blank cover sheet should be printed. -->
  <psf:Option name="psk:BlankCover" />
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="eb099-149">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="eb099-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eb099-150">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="eb099-150">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




