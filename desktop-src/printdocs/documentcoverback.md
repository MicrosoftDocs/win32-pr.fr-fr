---
description: En savoir plus sur l’élément DocumentCoverBack, qui décrit la feuille de couverture back. Chaque document aura une feuille distincte.
ms.assetid: 29d0bf2d-4897-43ed-ba3d-0b38b2f30375
title: DocumentCoverBack
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad5c75fd4bbce89bbc707c17a82202846cf2490a
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409382"
---
# <a name="documentcoverback"></a><span data-ttu-id="b6c2c-104">DocumentCoverBack</span><span class="sxs-lookup"><span data-stu-id="b6c2c-104">DocumentCoverBack</span></span>

<span data-ttu-id="b6c2c-105">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="b6c2c-105">This topic is not current.</span></span> <span data-ttu-id="b6c2c-106">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="b6c2c-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="b6c2c-107">Décrit la feuille de couverture Back (final).</span><span class="sxs-lookup"><span data-stu-id="b6c2c-107">Describes the back (ending) cover sheet.</span></span> <span data-ttu-id="b6c2c-108">Chaque document aura une feuille distincte.</span><span class="sxs-lookup"><span data-stu-id="b6c2c-108">Each document will have a separate sheet.</span></span> <span data-ttu-id="b6c2c-109">La feuille de couverture doit être imprimée sur le PageMediaSize et le PageMediaType utilisés pour la dernière page du document.</span><span class="sxs-lookup"><span data-stu-id="b6c2c-109">The cover sheet should be printed on the PageMediaSize and PageMediaType used for the final page of the document.</span></span> <span data-ttu-id="b6c2c-110">La feuille de couverture doit être intégrée dans les options de traitement (telles que DocumentDuplex, DocumentNUp), comme indiqué par l’option spécifiée.</span><span class="sxs-lookup"><span data-stu-id="b6c2c-110">The cover sheet should be integrated into processing options (such as DocumentDuplex, DocumentNUp) as indicated by the Option specified.</span></span>

-   [<span data-ttu-id="b6c2c-111">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="b6c2c-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="b6c2c-112">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="b6c2c-112">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="b6c2c-113">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="b6c2c-113">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="b6c2c-114">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="b6c2c-114">Element Information</span></span>



| <span data-ttu-id="b6c2c-115">Nom</span><span class="sxs-lookup"><span data-stu-id="b6c2c-115">Name</span></span> | <span data-ttu-id="b6c2c-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="b6c2c-116">Value</span></span> |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6c2c-117">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="b6c2c-117">Element Type</span></span> <br/>   | <span data-ttu-id="b6c2c-118">Fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="b6c2c-118">Feature</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="b6c2c-119">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="b6c2c-119">Scoping Prefix</span></span> <br/> | <span data-ttu-id="b6c2c-120">Document</span><span class="sxs-lookup"><span data-stu-id="b6c2c-120">Document</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="b6c2c-121">Notes</span><span class="sxs-lookup"><span data-stu-id="b6c2c-121">Notes</span></span> <br/>          | <span data-ttu-id="b6c2c-122">Les consommateurs compatibles XPS doivent s’assurer qu’une référence URI à une ressource telle qu’une image ou un profil de couleurs dans un document de fonctionnalités d’impression ou un PrintTicket doit faire référence à un nom de partie (un URI relatif à la racine du package) dans le même package de document XPS qui contient le PrintTicket résultant.</span><span class="sxs-lookup"><span data-stu-id="b6c2c-122">XPS-compliant consumers MUST enforce that a URI reference to a resource such as an image or color profile in either a Print Capabilities document or PrintTicket MUST refer to a part name (a relative URI to the package root) within the same XPS Document package that contains the resultant PrintTicket.</span></span> <span data-ttu-id="b6c2c-123">Un consommateur XPS conforme ne doit pas utiliser un URI qui n’est pas conforme à la syntaxe du nom de la partie.</span><span class="sxs-lookup"><span data-stu-id="b6c2c-123">A compliant XPS consumer MUST NOT use a URI that is not compliant with the part name syntax.</span></span> <span data-ttu-id="b6c2c-124">Ces paramètres sont spécifiques à XPS.</span><span class="sxs-lookup"><span data-stu-id="b6c2c-124">These settings are XPS specific.</span></span> <br/> <span data-ttu-id="b6c2c-125">Les URI référencés dans un document de fonctionnalités d’impression ou un PrintTicket ne doivent pas être résolus en tant qu’URL.</span><span class="sxs-lookup"><span data-stu-id="b6c2c-125">URIs which are referenced in either a Print Capabilities document or PrintTicket MUST NOT be resolved as URLs.</span></span> <span data-ttu-id="b6c2c-126">Cela ne peut pas être résolu comme prévu et peut créer des risques de sécurité néfastes pour le pilote et le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="b6c2c-126">This is unsafe as they may not resolve as intended and may create harmful security risks for the driver and operating system.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="b6c2c-127">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="b6c2c-127">Structural Content</span></span>

<span data-ttu-id="b6c2c-128">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="b6c2c-128">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:DocumentCoverBack">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <!--Specifies the XPS specific part name for the back cover sheet-->
    <psf:ScoredProperty name="psk:CoverBackSource">
      <psf:ParameterRef name="psk:DocumentCoverBackSource" />
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
```

## <a name="structure-variables"></a><span data-ttu-id="b6c2c-129">Variables de structure</span><span class="sxs-lookup"><span data-stu-id="b6c2c-129">Structure Variables</span></span>

<span data-ttu-id="b6c2c-130">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="b6c2c-130">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="b6c2c-131">Nom</span><span class="sxs-lookup"><span data-stu-id="b6c2c-131">Name</span></span>                               | <span data-ttu-id="b6c2c-132">Type de données</span><span class="sxs-lookup"><span data-stu-id="b6c2c-132">Data type</span></span>         | <span data-ttu-id="b6c2c-133">Unité</span><span class="sxs-lookup"><span data-stu-id="b6c2c-133">Unit</span></span>                  | <span data-ttu-id="b6c2c-134">Valeurs prises en charge</span><span class="sxs-lookup"><span data-stu-id="b6c2c-134">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="b6c2c-135">Résumé</span><span class="sxs-lookup"><span data-stu-id="b6c2c-135">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="b6c2c-136">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="b6c2c-136">\_OptionName\_</span></span><br/>          | <span data-ttu-id="b6c2c-137">string</span><span class="sxs-lookup"><span data-stu-id="b6c2c-137">string</span></span><br/> | <span data-ttu-id="b6c2c-138">caractères</span><span class="sxs-lookup"><span data-stu-id="b6c2c-138">characters</span></span><br/> | <span data-ttu-id="b6c2c-139">Nom complet valide tel que défini par les [espaces de noms dans XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="b6c2c-139">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="b6c2c-140">Si aucun espace de noms n’est spécifié, l’espace de noms par défaut est utilisé.</span><span class="sxs-lookup"><span data-stu-id="b6c2c-140">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="b6c2c-141">Nom de l'option.</span><span class="sxs-lookup"><span data-stu-id="b6c2c-141">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="b6c2c-142">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="b6c2c-142">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="b6c2c-143">string</span><span class="sxs-lookup"><span data-stu-id="b6c2c-143">string</span></span><br/> | <span data-ttu-id="b6c2c-144">n/a</span><span class="sxs-lookup"><span data-stu-id="b6c2c-144">n/a</span></span><br/>        | <span data-ttu-id="b6c2c-145">True, False.</span><span class="sxs-lookup"><span data-stu-id="b6c2c-145">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="b6c2c-146">Définit une option qui, lorsqu’elle est sélectionnée, désactive cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="b6c2c-146">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="b6c2c-147">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="b6c2c-147">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="b6c2c-148">Les mots clés de schéma d’impression publics sont définis dans l' https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords espace de noms.</span><span class="sxs-lookup"><span data-stu-id="b6c2c-148">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="b6c2c-149">Le contenu de la Extensible Markup Language publique (XML) pour ce mot clé est défini ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="b6c2c-149">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:DocumentCoverBack">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies no cover will be output -->
  <psf:Option name="psk:NoCover" />
  <!-- Specifies the cover indicated by "CoverBackSource" should be printed on the back side 
       of the cover sheet.  If a DocumentCoverBackSource ParameterInit element is not specified, 
       this Option should be ignored. -->
  <psf:Option name="psk:PrintBack">
    <psf:ScoredProperty name="psk:CoverBackSource">
      <psf:ParameterRef name="psk:DocumentCoverBackSource" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies the cover indicated by "CoverBackSource" may be printed on either sides 
       of the cover sheet.  If a DocumentCoverBackSource ParameterInit element is not specified, 
       this Option should be ignored. -->
  <psf:Option name="psk:PrintBoth">
    <psf:ScoredProperty name="psk:CoverBackSource">
      <psf:ParameterRef name="psk:DocumentCoverBackSource" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies the cover indicated by "CoverBackSource" should be printed on the front side 
       of the cover sheet.  If a DocumentCoverBackSource ParameterInit element is not specified, 
       this Option should be ignored. -->
  <psf:Option name="psk:PrintFront">
    <psf:ScoredProperty name="psk:CoverBackSource">
      <psf:ParameterRef name="psk:DocumentCoverBackSource" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies a blank cover sheet should be printed. -->
  <psf:Option name="psk:BlankCover" />
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="b6c2c-150">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b6c2c-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b6c2c-151">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="b6c2c-151">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




