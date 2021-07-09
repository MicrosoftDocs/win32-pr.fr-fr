---
description: En savoir plus sur l’élément configurable par l’utilisateur PageBlendColorSpace. Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: 86e3f44d-192e-412a-abb1-118e8592d90b
title: PageBlendColorSpace
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b36ce3a1def74058014fc396d9ef53aed6a32302
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/09/2021
ms.locfileid: "113549337"
---
# <a name="pageblendcolorspace"></a><span data-ttu-id="e71c1-105">PageBlendColorSpace</span><span class="sxs-lookup"><span data-stu-id="e71c1-105">PageBlendColorSpace</span></span>

<span data-ttu-id="e71c1-106">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="e71c1-106">This topic is not current.</span></span> <span data-ttu-id="e71c1-107">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="e71c1-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="e71c1-108">Décrit l’espace colorimétrique qui doit être utilisé pour les opérations de fusion.</span><span class="sxs-lookup"><span data-stu-id="e71c1-108">Describes the color space that should be used for blending operations.</span></span>

-   [<span data-ttu-id="e71c1-109">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="e71c1-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="e71c1-110">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="e71c1-110">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="e71c1-111">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="e71c1-111">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="e71c1-112">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="e71c1-112">Element Information</span></span>



| <span data-ttu-id="e71c1-113">Nom</span><span class="sxs-lookup"><span data-stu-id="e71c1-113">Name</span></span> | <span data-ttu-id="e71c1-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="e71c1-114">Value</span></span> |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e71c1-115">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="e71c1-115">Element Type</span></span> <br/>   | <span data-ttu-id="e71c1-116">Composant</span><span class="sxs-lookup"><span data-stu-id="e71c1-116">Feature</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="e71c1-117">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="e71c1-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="e71c1-118">Travail</span><span class="sxs-lookup"><span data-stu-id="e71c1-118">Job</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="e71c1-119">Remarques</span><span class="sxs-lookup"><span data-stu-id="e71c1-119">Notes</span></span> <br/>          | <span data-ttu-id="e71c1-120">Les consommateurs compatibles XPS doivent s’assurer qu’une référence URI à une ressource telle qu’une image ou un profil de couleurs dans un document de fonctionnalités d’impression ou un PrintTicket doit faire référence à un nom de partie (un URI relatif à la racine du package) dans le même package de document XPS qui contient le PrintTicket résultant.</span><span class="sxs-lookup"><span data-stu-id="e71c1-120">XPS-compliant consumers MUST enforce that a URI reference to a resource such as an image or color profile in either a Print Capabilities document or PrintTicket MUST refer to a part name (a relative URI to the package root) within the same XPS Document package that contains the resultant PrintTicket.</span></span> <span data-ttu-id="e71c1-121">Un consommateur XPS conforme ne doit pas utiliser un URI qui n’est pas conforme à la syntaxe du nom de la partie.</span><span class="sxs-lookup"><span data-stu-id="e71c1-121">A compliant XPS consumer MUST NOT use a URI that is not compliant with the part name syntax.</span></span> <span data-ttu-id="e71c1-122">Ces paramètres sont spécifiques à XPS.</span><span class="sxs-lookup"><span data-stu-id="e71c1-122">These settings are XPS specific.</span></span> <br/> <span data-ttu-id="e71c1-123">Les URI référencés dans un document de fonctionnalités d’impression ou un PrintTicket ne doivent pas être résolus en tant qu’URL.</span><span class="sxs-lookup"><span data-stu-id="e71c1-123">URIs which are referenced in either a Print Capabilities document or PrintTicket MUST NOT be resolved as URLs.</span></span> <span data-ttu-id="e71c1-124">Cela ne peut pas être résolu comme prévu et peut créer des risques de sécurité néfastes pour le pilote et le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="e71c1-124">This is unsafe as they may not resolve as intended and may create harmful security risks for the driver and operating system.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="e71c1-125">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="e71c1-125">Structural Content</span></span>

<span data-ttu-id="e71c1-126">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="e71c1-126">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="e71c1-127">Variables de structure</span><span class="sxs-lookup"><span data-stu-id="e71c1-127">Structure Variables</span></span>

<span data-ttu-id="e71c1-128">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="e71c1-128">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="e71c1-129">Nom</span><span class="sxs-lookup"><span data-stu-id="e71c1-129">Name</span></span>                               | <span data-ttu-id="e71c1-130">Type de données</span><span class="sxs-lookup"><span data-stu-id="e71c1-130">Data type</span></span>         | <span data-ttu-id="e71c1-131">Unité</span><span class="sxs-lookup"><span data-stu-id="e71c1-131">Unit</span></span>                  | <span data-ttu-id="e71c1-132">Valeurs prises en charge</span><span class="sxs-lookup"><span data-stu-id="e71c1-132">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="e71c1-133">Résumé</span><span class="sxs-lookup"><span data-stu-id="e71c1-133">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="e71c1-134">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="e71c1-134">\_OptionName\_</span></span><br/>          | <span data-ttu-id="e71c1-135">string</span><span class="sxs-lookup"><span data-stu-id="e71c1-135">string</span></span><br/> | <span data-ttu-id="e71c1-136">caractères</span><span class="sxs-lookup"><span data-stu-id="e71c1-136">characters</span></span><br/> | <span data-ttu-id="e71c1-137">Nom complet valide tel que défini par les [espaces de noms dans XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="e71c1-137">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="e71c1-138">Si aucun espace de noms n’est spécifié, l’espace de noms par défaut est utilisé.</span><span class="sxs-lookup"><span data-stu-id="e71c1-138">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="e71c1-139">Nom de l'option.</span><span class="sxs-lookup"><span data-stu-id="e71c1-139">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="e71c1-140">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="e71c1-140">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="e71c1-141">string</span><span class="sxs-lookup"><span data-stu-id="e71c1-141">string</span></span><br/> | <span data-ttu-id="e71c1-142">n/a</span><span class="sxs-lookup"><span data-stu-id="e71c1-142">n/a</span></span><br/>        | <span data-ttu-id="e71c1-143">True, False.</span><span class="sxs-lookup"><span data-stu-id="e71c1-143">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="e71c1-144">Définit une option qui, lorsqu’elle est sélectionnée, désactive cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="e71c1-144">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="e71c1-145">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="e71c1-145">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="e71c1-146">Les mots clés de schéma d’impression publics sont définis dans l' https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords espace de noms.</span><span class="sxs-lookup"><span data-stu-id="e71c1-146">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="e71c1-147">Le contenu de la Extensible Markup Language publique (XML) pour ce mot clé est défini ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="e71c1-147">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="e71c1-148">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e71c1-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e71c1-149">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="e71c1-149">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




