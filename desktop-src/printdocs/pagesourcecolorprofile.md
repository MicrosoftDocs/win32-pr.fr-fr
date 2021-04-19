---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: aa4f5425-6ca1-4820-b15d-bbead1f6d735
title: PageSourceColorProfile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32de15ec5110788ad85d8ceb2f251eb3b30000d8
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "106535759"
---
# <a name="pagesourcecolorprofile"></a><span data-ttu-id="01906-104">PageSourceColorProfile</span><span class="sxs-lookup"><span data-stu-id="01906-104">PageSourceColorProfile</span></span>

<span data-ttu-id="01906-105">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="01906-105">This topic is not current.</span></span> <span data-ttu-id="01906-106">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="01906-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="01906-107">Définit les caractéristiques du profil de couleurs source.</span><span class="sxs-lookup"><span data-stu-id="01906-107">Defines the characteristics of the source color profile.</span></span>

-   [<span data-ttu-id="01906-108">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="01906-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="01906-109">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="01906-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="01906-110">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="01906-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="01906-111">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="01906-111">Element Information</span></span>



| <span data-ttu-id="01906-112">Nom</span><span class="sxs-lookup"><span data-stu-id="01906-112">Name</span></span>                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="01906-113">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="01906-113">Element Type</span></span> <br/>   | <span data-ttu-id="01906-114">Fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="01906-114">Feature</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="01906-115">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="01906-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="01906-116">Page</span><span class="sxs-lookup"><span data-stu-id="01906-116">Page</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="01906-117">Notes</span><span class="sxs-lookup"><span data-stu-id="01906-117">Notes</span></span> <br/>          | <span data-ttu-id="01906-118">Les consommateurs compatibles XPS doivent s’assurer qu’une référence URI à une ressource telle qu’une image ou un profil de couleurs dans un document de fonctionnalités d’impression ou un PrintTicket doit faire référence à un nom de partie (un URI relatif à la racine du package) dans le même package de document XPS qui contient le PrintTicket résultant.</span><span class="sxs-lookup"><span data-stu-id="01906-118">XPS-compliant consumers MUST enforce that a URI reference to a resource such as an image or color profile in either a Print Capabilities document or PrintTicket MUST refer to a part name (a relative URI to the package root) within the same XPS Document package that contains the resultant PrintTicket.</span></span> <span data-ttu-id="01906-119">Un consommateur XPS conforme ne doit pas utiliser un URI qui n’est pas conforme à la syntaxe du nom de la partie.</span><span class="sxs-lookup"><span data-stu-id="01906-119">A compliant XPS consumer MUST NOT use a URI that is not compliant with the part name syntax.</span></span> <span data-ttu-id="01906-120">Ces paramètres sont spécifiques à XPS.</span><span class="sxs-lookup"><span data-stu-id="01906-120">These settings are XPS specific.</span></span> <br/> <span data-ttu-id="01906-121">Les URI référencés dans un document de fonctionnalités d’impression ou un PrintTicket ne doivent pas être résolus en tant qu’URL.</span><span class="sxs-lookup"><span data-stu-id="01906-121">URIs which are referenced in either a Print Capabilities document or PrintTicket MUST NOT be resolved as URLs.</span></span> <span data-ttu-id="01906-122">Cela ne peut pas être résolu comme prévu et peut créer des risques de sécurité néfastes pour le pilote et le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="01906-122">This is unsafe as they may not resolve as intended and may create harmful security risks for the driver and operating system.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="01906-123">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="01906-123">Structural Content</span></span>

<span data-ttu-id="01906-124">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="01906-124">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageSourceColorProfile">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
  </psf:Option>
</psf:Feature>
```

## <a name="structure-variables"></a><span data-ttu-id="01906-125">Variables de structure</span><span class="sxs-lookup"><span data-stu-id="01906-125">Structure Variables</span></span>

<span data-ttu-id="01906-126">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="01906-126">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="01906-127">Nom</span><span class="sxs-lookup"><span data-stu-id="01906-127">Name</span></span>                               | <span data-ttu-id="01906-128">Type de données</span><span class="sxs-lookup"><span data-stu-id="01906-128">Data type</span></span>         | <span data-ttu-id="01906-129">Unité</span><span class="sxs-lookup"><span data-stu-id="01906-129">Unit</span></span>                  | <span data-ttu-id="01906-130">Valeurs prises en charge</span><span class="sxs-lookup"><span data-stu-id="01906-130">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="01906-131">Résumé</span><span class="sxs-lookup"><span data-stu-id="01906-131">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="01906-132">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="01906-132">\_OptionName\_</span></span><br/>          | <span data-ttu-id="01906-133">string</span><span class="sxs-lookup"><span data-stu-id="01906-133">string</span></span><br/> | <span data-ttu-id="01906-134">caractères</span><span class="sxs-lookup"><span data-stu-id="01906-134">characters</span></span><br/> | <span data-ttu-id="01906-135">Nom complet valide tel que défini par les [espaces de noms dans XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="01906-135">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="01906-136">Si aucun espace de noms n’est spécifié, l’espace de noms par défaut est utilisé.</span><span class="sxs-lookup"><span data-stu-id="01906-136">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="01906-137">Nom de l'option.</span><span class="sxs-lookup"><span data-stu-id="01906-137">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="01906-138">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="01906-138">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="01906-139">string</span><span class="sxs-lookup"><span data-stu-id="01906-139">string</span></span><br/> | <span data-ttu-id="01906-140">n/a</span><span class="sxs-lookup"><span data-stu-id="01906-140">n/a</span></span><br/>        | <span data-ttu-id="01906-141">True, False.</span><span class="sxs-lookup"><span data-stu-id="01906-141">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="01906-142">Définit une option qui, lorsqu’elle est sélectionnée, désactive cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="01906-142">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="01906-143">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="01906-143">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="01906-144">Les mots clés de schéma d’impression publics sont définis dans l' https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords espace de noms.</span><span class="sxs-lookup"><span data-stu-id="01906-144">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="01906-145">Le contenu de la Extensible Markup Language publique (XML) pour ce mot clé est défini ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="01906-145">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageSourceColorProfile">
  <psf:Option name="psk:RGB">
    <!-- Source profile used to perform color management for untagged RGB data. -->
    <psf:ScoredProperty name="psk:SourceColorProfileURI">
      <psf:ParameterRef name="psk:PageSourceColorProfileURI" />
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:SourceColorProfileEmbedded">
      <psf:ParameterRef name="psk:PageSourceColorProfileEmbedded" />
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:CMYK">
    <!-- Source profile used to perform color management for untagged CMYK data. -->
    <psf:ScoredProperty name="psk:SourceColorProfileURI">
      <psf:ParameterRef name="psk:PageSourceColorProfileURI" />
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:SourceColorProfileEmbedded">
      <psf:ParameterRef name="psk:PageSourceColorProfileEmbedded" />
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:None" />
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="01906-146">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="01906-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="01906-147">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="01906-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




