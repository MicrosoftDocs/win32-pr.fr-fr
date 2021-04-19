---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: 1a6ff76a-0818-464a-bf75-534dc7ea383f
title: PageDestinationColorProfile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fde6077bc2bae611c2a791ecf041cb52588c2ebb
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "106535122"
---
# <a name="pagedestinationcolorprofile"></a><span data-ttu-id="22248-104">PageDestinationColorProfile</span><span class="sxs-lookup"><span data-stu-id="22248-104">PageDestinationColorProfile</span></span>

<span data-ttu-id="22248-105">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="22248-105">This topic is not current.</span></span> <span data-ttu-id="22248-106">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="22248-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="22248-107">Définit les caractéristiques du profil de couleurs de destination.</span><span class="sxs-lookup"><span data-stu-id="22248-107">Defines the characteristics of the destination color profile.</span></span> <span data-ttu-id="22248-108">Indique si l’application ou le pilote sélectionne le profil de couleurs de destination à utiliser.</span><span class="sxs-lookup"><span data-stu-id="22248-108">Describes whether the application or driver selects the destination color profile to be used.</span></span>

-   [<span data-ttu-id="22248-109">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="22248-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="22248-110">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="22248-110">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="22248-111">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="22248-111">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="22248-112">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="22248-112">Element Information</span></span>



| <span data-ttu-id="22248-113">Nom</span><span class="sxs-lookup"><span data-stu-id="22248-113">Name</span></span>                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="22248-114">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="22248-114">Element Type</span></span> <br/>   | <span data-ttu-id="22248-115">Fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="22248-115">Feature</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="22248-116">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="22248-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="22248-117">Page</span><span class="sxs-lookup"><span data-stu-id="22248-117">Page</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="22248-118">Notes</span><span class="sxs-lookup"><span data-stu-id="22248-118">Notes</span></span> <br/>          | <span data-ttu-id="22248-119">Les consommateurs compatibles XPS doivent s’assurer qu’une référence URI à une ressource telle qu’une image ou un profil de couleurs dans un document de fonctionnalités d’impression ou un PrintTicket doit faire référence à un nom de partie (un URI relatif à la racine du package) dans le même package de document XPS qui contient le PrintTicket résultant.</span><span class="sxs-lookup"><span data-stu-id="22248-119">XPS-compliant consumers MUST enforce that a URI reference to a resource such as an image or color profile in either a Print Capabilities document or PrintTicket MUST refer to a part name (a relative URI to the package root) within the same XPS Document package that contains the resultant PrintTicket.</span></span> <span data-ttu-id="22248-120">Un consommateur XPS conforme ne doit pas utiliser un URI qui n’est pas conforme à la syntaxe du nom de la partie.</span><span class="sxs-lookup"><span data-stu-id="22248-120">A compliant XPS consumer MUST NOT use a URI that is not compliant with the part name syntax.</span></span> <span data-ttu-id="22248-121">Ces paramètres sont spécifiques à XPS.</span><span class="sxs-lookup"><span data-stu-id="22248-121">These settings are XPS specific.</span></span> <br/> <span data-ttu-id="22248-122">Les URI référencés dans un document de fonctionnalités d’impression ou un PrintTicket ne doivent pas être résolus en tant qu’URL.</span><span class="sxs-lookup"><span data-stu-id="22248-122">URIs which are referenced in either a Print Capabilities document or PrintTicket MUST NOT be resolved as URLs.</span></span> <span data-ttu-id="22248-123">Cela ne peut pas être résolu comme prévu et peut créer des risques de sécurité néfastes pour le pilote et le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="22248-123">This is unsafe as they may not resolve as intended and may create harmful security risks for the driver and operating system.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="22248-124">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="22248-124">Structural Content</span></span>

<span data-ttu-id="22248-125">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="22248-125">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageDestinationColorProfile">
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

## <a name="structure-variables"></a><span data-ttu-id="22248-126">Variables de structure</span><span class="sxs-lookup"><span data-stu-id="22248-126">Structure Variables</span></span>

<span data-ttu-id="22248-127">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="22248-127">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="22248-128">Nom</span><span class="sxs-lookup"><span data-stu-id="22248-128">Name</span></span>                               | <span data-ttu-id="22248-129">Type de données</span><span class="sxs-lookup"><span data-stu-id="22248-129">Data type</span></span>         | <span data-ttu-id="22248-130">Unité</span><span class="sxs-lookup"><span data-stu-id="22248-130">Unit</span></span>                  | <span data-ttu-id="22248-131">Valeurs prises en charge</span><span class="sxs-lookup"><span data-stu-id="22248-131">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="22248-132">Résumé</span><span class="sxs-lookup"><span data-stu-id="22248-132">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="22248-133">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="22248-133">\_OptionName\_</span></span><br/>          | <span data-ttu-id="22248-134">string</span><span class="sxs-lookup"><span data-stu-id="22248-134">string</span></span><br/> | <span data-ttu-id="22248-135">caractères</span><span class="sxs-lookup"><span data-stu-id="22248-135">characters</span></span><br/> | <span data-ttu-id="22248-136">Nom complet valide tel que défini par les [espaces de noms dans XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="22248-136">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="22248-137">Si aucun espace de noms n’est spécifié, l’espace de noms par défaut est utilisé.</span><span class="sxs-lookup"><span data-stu-id="22248-137">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="22248-138">Nom de l'option.</span><span class="sxs-lookup"><span data-stu-id="22248-138">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="22248-139">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="22248-139">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="22248-140">string</span><span class="sxs-lookup"><span data-stu-id="22248-140">string</span></span><br/> | <span data-ttu-id="22248-141">n/a</span><span class="sxs-lookup"><span data-stu-id="22248-141">n/a</span></span><br/>        | <span data-ttu-id="22248-142">True, False.</span><span class="sxs-lookup"><span data-stu-id="22248-142">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="22248-143">Définit une option qui, lorsqu’elle est sélectionnée, désactive cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="22248-143">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="22248-144">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="22248-144">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="22248-145">Les mots clés de schéma d’impression publics sont définis dans l' https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords espace de noms.</span><span class="sxs-lookup"><span data-stu-id="22248-145">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="22248-146">Le contenu de la Extensible Markup Language publique (XML) pour ce mot clé est défini ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="22248-146">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageDestinationColorProfile">
  <!-- Application specifies the destination profile to be used. -->
  <psf:Option name="psk:Application">
    <!-- Destination profile used to perform color management. -->
    <psf:ScoredProperty name="psk:DestinationColorProfileURI">
      <psf:ParameterRef name="psk:PageDestinationColorProfileURI" />
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:DestinationColorProfileEmbedded">
      <psf:ParameterRef name="psk:PageDestinationColorProfileEmbedded" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Driver selects the destination profile that best matches its current configuration. -->
  <psf:Option name="psk:DriverConfiguration" />
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="22248-147">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="22248-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="22248-148">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="22248-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




