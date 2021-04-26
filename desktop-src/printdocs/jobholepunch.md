---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: 26e9e7d6-7c01-4687-aa64-7aea867b4e58
title: JobHolePunch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56316c94dc56a2646446a8cd63885cceaa1407fa
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107999296"
---
# <a name="jobholepunch"></a><span data-ttu-id="da900-104">JobHolePunch</span><span class="sxs-lookup"><span data-stu-id="da900-104">JobHolePunch</span></span>

<span data-ttu-id="da900-105">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="da900-105">This topic is not current.</span></span> <span data-ttu-id="da900-106">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="da900-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="da900-107">Décrit les caractéristiques de perforation de la sortie.</span><span class="sxs-lookup"><span data-stu-id="da900-107">Describes the hole punching characteristics of the output.</span></span> <span data-ttu-id="da900-108">Tous les documents sont perforés ensemble.</span><span class="sxs-lookup"><span data-stu-id="da900-108">All documents are punched together.</span></span> <span data-ttu-id="da900-109">Les mots clés JobHolePunch et DocumentHolePunch s’excluent mutuellement.</span><span class="sxs-lookup"><span data-stu-id="da900-109">The JobHolePunch and DocumentHolePunch keywords are mutually exclusive.</span></span> <span data-ttu-id="da900-110">Ils ne doivent pas être spécifiés simultanément dans un document de fonctionnalités PrintTicket ou Print.</span><span class="sxs-lookup"><span data-stu-id="da900-110">Both should not be specified simultaneously in a PrintTicket or Print Capabilities document.</span></span>

-   [<span data-ttu-id="da900-111">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="da900-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="da900-112">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="da900-112">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="da900-113">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="da900-113">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="da900-114">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="da900-114">Element Information</span></span>



| <span data-ttu-id="da900-115">Nom</span><span class="sxs-lookup"><span data-stu-id="da900-115">Name</span></span> | <span data-ttu-id="da900-116">Value</span><span class="sxs-lookup"><span data-stu-id="da900-116">Value</span></span> |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="da900-117">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="da900-117">Element Type</span></span> <br/>   | <span data-ttu-id="da900-118">Fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="da900-118">Feature</span></span><br/>                                                                                                                              |
| <span data-ttu-id="da900-119">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="da900-119">Scoping Prefix</span></span> <br/> | <span data-ttu-id="da900-120">Travail</span><span class="sxs-lookup"><span data-stu-id="da900-120">Job</span></span><br/>                                                                                                                                  |
| <span data-ttu-id="da900-121">Notes</span><span class="sxs-lookup"><span data-stu-id="da900-121">Notes</span></span> <br/>          | <span data-ttu-id="da900-122">Haut, bas, gauche et droite sont relatifs à PageImageableSize, où Left est indiqué par l’origine de l’axe x et de l’axe y.</span><span class="sxs-lookup"><span data-stu-id="da900-122">Top, Bottom, Left, and Right are relative to the PageImageableSize, where TopLeft is denoted by the origin of the x-axis and y-axis.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="da900-123">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="da900-123">Structural Content</span></span>

<span data-ttu-id="da900-124">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="da900-124">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:JobHolePunch">
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

## <a name="structure-variables"></a><span data-ttu-id="da900-125">Variables de structure</span><span class="sxs-lookup"><span data-stu-id="da900-125">Structure Variables</span></span>

<span data-ttu-id="da900-126">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="da900-126">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="da900-127">Nom</span><span class="sxs-lookup"><span data-stu-id="da900-127">Name</span></span>                               | <span data-ttu-id="da900-128">Type de données</span><span class="sxs-lookup"><span data-stu-id="da900-128">Data type</span></span>         | <span data-ttu-id="da900-129">Unité</span><span class="sxs-lookup"><span data-stu-id="da900-129">Unit</span></span>                  | <span data-ttu-id="da900-130">Valeurs prises en charge</span><span class="sxs-lookup"><span data-stu-id="da900-130">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="da900-131">Résumé</span><span class="sxs-lookup"><span data-stu-id="da900-131">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="da900-132">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="da900-132">\_OptionName\_</span></span><br/>          | <span data-ttu-id="da900-133">string</span><span class="sxs-lookup"><span data-stu-id="da900-133">string</span></span><br/> | <span data-ttu-id="da900-134">caractères</span><span class="sxs-lookup"><span data-stu-id="da900-134">characters</span></span><br/> | <span data-ttu-id="da900-135">Nom complet valide tel que défini par les [espaces de noms dans XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="da900-135">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="da900-136">Si aucun espace de noms n’est spécifié, l’espace de noms par défaut est utilisé.</span><span class="sxs-lookup"><span data-stu-id="da900-136">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="da900-137">Nom de l'option.</span><span class="sxs-lookup"><span data-stu-id="da900-137">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="da900-138">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="da900-138">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="da900-139">string</span><span class="sxs-lookup"><span data-stu-id="da900-139">string</span></span><br/> | <span data-ttu-id="da900-140">n/a</span><span class="sxs-lookup"><span data-stu-id="da900-140">n/a</span></span><br/>        | <span data-ttu-id="da900-141">True, False.</span><span class="sxs-lookup"><span data-stu-id="da900-141">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="da900-142">Définit une option qui, lorsqu’elle est sélectionnée, désactive cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="da900-142">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="da900-143">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="da900-143">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="da900-144">Les mots clés de schéma d’impression publics sont définis dans l' https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords espace de noms.</span><span class="sxs-lookup"><span data-stu-id="da900-144">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="da900-145">Le contenu de la Extensible Markup Language publique (XML) pour ce mot clé est défini ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="da900-145">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:JobHolePunch">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies hole(s) along the bottom edge. -->
  <psf:Option name="psk:BottomEdge" />
  <!-- Specifies hole(s) along the left edge. -->
  <psf:Option name="psk:LeftEdge" />
  <!-- Specifies no hole punching. -->
  <psf:Option name="psk:None" />
  <!-- Specifies hole(s) along the right edge. -->
  <psf:Option name="psk:RightEdge" />
  <!-- Specifies hole(s) along the top edge. -->
  <psf:Option name="psk:TopEdge" />
</psf:Feature>    
```

## <a name="related-topics"></a><span data-ttu-id="da900-146">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="da900-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="da900-147">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="da900-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




