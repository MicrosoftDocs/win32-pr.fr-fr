---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: 86e3f44d-192e-412a-abb1-118e8592d90b
title: PageBlendColorSpace
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e12002b25265a66a0aa3a5168f29e1e8e542ce31
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998076"
---
# <a name="pageblendcolorspace"></a><span data-ttu-id="47107-104">PageBlendColorSpace</span><span class="sxs-lookup"><span data-stu-id="47107-104">PageBlendColorSpace</span></span>

<span data-ttu-id="47107-105">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="47107-105">This topic is not current.</span></span> <span data-ttu-id="47107-106">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="47107-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="47107-107">Décrit l’espace colorimétrique qui doit être utilisé pour les opérations de fusion.</span><span class="sxs-lookup"><span data-stu-id="47107-107">Describes the color space that should be used for blending operations.</span></span>

-   [<span data-ttu-id="47107-108">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="47107-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="47107-109">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="47107-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="47107-110">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="47107-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="47107-111">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="47107-111">Element Information</span></span>



| <span data-ttu-id="47107-112">Nom</span><span class="sxs-lookup"><span data-stu-id="47107-112">Name</span></span> | <span data-ttu-id="47107-113">Value</span><span class="sxs-lookup"><span data-stu-id="47107-113">Value</span></span> |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="47107-114">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="47107-114">Element Type</span></span> <br/>   | <span data-ttu-id="47107-115">Fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="47107-115">Feature</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="47107-116">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="47107-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="47107-117">Travail</span><span class="sxs-lookup"><span data-stu-id="47107-117">Job</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="47107-118">Notes</span><span class="sxs-lookup"><span data-stu-id="47107-118">Notes</span></span> <br/>          | <span data-ttu-id="47107-119">Les consommateurs compatibles XPS doivent s’assurer qu’une référence URI à une ressource telle qu’une image ou un profil de couleurs dans un document de fonctionnalités d’impression ou un PrintTicket doit faire référence à un nom de partie (un URI relatif à la racine du package) dans le même package de document XPS qui contient le PrintTicket résultant.</span><span class="sxs-lookup"><span data-stu-id="47107-119">XPS-compliant consumers MUST enforce that a URI reference to a resource such as an image or color profile in either a Print Capabilities document or PrintTicket MUST refer to a part name (a relative URI to the package root) within the same XPS Document package that contains the resultant PrintTicket.</span></span> <span data-ttu-id="47107-120">Un consommateur XPS conforme ne doit pas utiliser un URI qui n’est pas conforme à la syntaxe du nom de la partie.</span><span class="sxs-lookup"><span data-stu-id="47107-120">A compliant XPS consumer MUST NOT use a URI that is not compliant with the part name syntax.</span></span> <span data-ttu-id="47107-121">Ces paramètres sont spécifiques à XPS.</span><span class="sxs-lookup"><span data-stu-id="47107-121">These settings are XPS specific.</span></span> <br/> <span data-ttu-id="47107-122">Les URI référencés dans un document de fonctionnalités d’impression ou un PrintTicket ne doivent pas être résolus en tant qu’URL.</span><span class="sxs-lookup"><span data-stu-id="47107-122">URIs which are referenced in either a Print Capabilities document or PrintTicket MUST NOT be resolved as URLs.</span></span> <span data-ttu-id="47107-123">Cela ne peut pas être résolu comme prévu et peut créer des risques de sécurité néfastes pour le pilote et le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="47107-123">This is unsafe as they may not resolve as intended and may create harmful security risks for the driver and operating system.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="47107-124">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="47107-124">Structural Content</span></span>

<span data-ttu-id="47107-125">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="47107-125">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageBlendColorSpace">
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

## <a name="structure-variables"></a><span data-ttu-id="47107-126">Variables de structure</span><span class="sxs-lookup"><span data-stu-id="47107-126">Structure Variables</span></span>

<span data-ttu-id="47107-127">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="47107-127">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="47107-128">Nom</span><span class="sxs-lookup"><span data-stu-id="47107-128">Name</span></span>                               | <span data-ttu-id="47107-129">Type de données</span><span class="sxs-lookup"><span data-stu-id="47107-129">Data type</span></span>         | <span data-ttu-id="47107-130">Unité</span><span class="sxs-lookup"><span data-stu-id="47107-130">Unit</span></span>                  | <span data-ttu-id="47107-131">Valeurs prises en charge</span><span class="sxs-lookup"><span data-stu-id="47107-131">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="47107-132">Résumé</span><span class="sxs-lookup"><span data-stu-id="47107-132">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="47107-133">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="47107-133">\_OptionName\_</span></span><br/>          | <span data-ttu-id="47107-134">string</span><span class="sxs-lookup"><span data-stu-id="47107-134">string</span></span><br/> | <span data-ttu-id="47107-135">caractères</span><span class="sxs-lookup"><span data-stu-id="47107-135">characters</span></span><br/> | <span data-ttu-id="47107-136">Nom complet valide tel que défini par les [espaces de noms dans XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="47107-136">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="47107-137">Si aucun espace de noms n’est spécifié, l’espace de noms par défaut est utilisé.</span><span class="sxs-lookup"><span data-stu-id="47107-137">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="47107-138">Nom de l'option.</span><span class="sxs-lookup"><span data-stu-id="47107-138">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="47107-139">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="47107-139">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="47107-140">string</span><span class="sxs-lookup"><span data-stu-id="47107-140">string</span></span><br/> | <span data-ttu-id="47107-141">n/a</span><span class="sxs-lookup"><span data-stu-id="47107-141">n/a</span></span><br/>        | <span data-ttu-id="47107-142">True, False.</span><span class="sxs-lookup"><span data-stu-id="47107-142">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="47107-143">Définit une option qui, lorsqu’elle est sélectionnée, désactive cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="47107-143">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="47107-144">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="47107-144">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="47107-145">Les mots clés de schéma d’impression publics sont définis dans l' https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords espace de noms.</span><span class="sxs-lookup"><span data-stu-id="47107-145">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="47107-146">Le contenu de la Extensible Markup Language publique (XML) pour ce mot clé est défini ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="47107-146">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageBlendColorSpace">
  <psf:Property name="SelectionType">
    <psf:Value xsi:type="xs:string">PickOne</psf:Value>
  </psf:Property>
  <!-- sRGB color space SHOULD be used for blending. -->
  <psf:Option name="psk:sRGB" />
  <!-- scRGB color space SHOULD be used for blending. -->
  <psf:Option name="psk:scRGB" />
  <!-- Specifies an ICC profile defining the color space that SHOULD be used for blending.  Note: This applies to XPS Documents only and should not be used in arbitrary PrintTickets. -->
  <psf:Option name="psk:ICCProfile">
    <!-- XPS specific part name for the blend mode ICC Profile -->
    <psf:ScoredProperty name="psk:URI">
      <psf:ParameterRef name="psk:PageBlendColorSpaceICCProfileURI" />
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="47107-147">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="47107-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="47107-148">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="47107-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




