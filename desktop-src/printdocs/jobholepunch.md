---
description: Obtenir des informations sur l’élément configurable par l’utilisateur JobHolePunch. Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: 26e9e7d6-7c01-4687-aa64-7aea867b4e58
title: JobHolePunch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c82a36784ab6a1fb5eb0c8d682c45cce574ee9e
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/09/2021
ms.locfileid: "113549357"
---
# <a name="jobholepunch"></a><span data-ttu-id="34482-105">JobHolePunch</span><span class="sxs-lookup"><span data-stu-id="34482-105">JobHolePunch</span></span>

<span data-ttu-id="34482-106">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="34482-106">This topic is not current.</span></span> <span data-ttu-id="34482-107">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="34482-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="34482-108">Décrit les caractéristiques de perforation de la sortie.</span><span class="sxs-lookup"><span data-stu-id="34482-108">Describes the hole punching characteristics of the output.</span></span> <span data-ttu-id="34482-109">Tous les documents sont perforés ensemble.</span><span class="sxs-lookup"><span data-stu-id="34482-109">All documents are punched together.</span></span> <span data-ttu-id="34482-110">Les mots clés JobHolePunch et DocumentHolePunch s’excluent mutuellement.</span><span class="sxs-lookup"><span data-stu-id="34482-110">The JobHolePunch and DocumentHolePunch keywords are mutually exclusive.</span></span> <span data-ttu-id="34482-111">Ils ne doivent pas être spécifiés simultanément dans un document de fonctionnalités PrintTicket ou Print.</span><span class="sxs-lookup"><span data-stu-id="34482-111">Both should not be specified simultaneously in a PrintTicket or Print Capabilities document.</span></span>

-   [<span data-ttu-id="34482-112">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="34482-112">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="34482-113">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="34482-113">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="34482-114">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="34482-114">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="34482-115">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="34482-115">Element Information</span></span>



| <span data-ttu-id="34482-116">Nom</span><span class="sxs-lookup"><span data-stu-id="34482-116">Name</span></span> | <span data-ttu-id="34482-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="34482-117">Value</span></span> |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34482-118">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="34482-118">Element Type</span></span> <br/>   | <span data-ttu-id="34482-119">Composant</span><span class="sxs-lookup"><span data-stu-id="34482-119">Feature</span></span><br/>                                                                                                                              |
| <span data-ttu-id="34482-120">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="34482-120">Scoping Prefix</span></span> <br/> | <span data-ttu-id="34482-121">Travail</span><span class="sxs-lookup"><span data-stu-id="34482-121">Job</span></span><br/>                                                                                                                                  |
| <span data-ttu-id="34482-122">Remarques</span><span class="sxs-lookup"><span data-stu-id="34482-122">Notes</span></span> <br/>          | <span data-ttu-id="34482-123">Haut, bas, gauche et droite sont relatifs à PageImageableSize, où Left est indiqué par l’origine de l’axe x et de l’axe y.</span><span class="sxs-lookup"><span data-stu-id="34482-123">Top, Bottom, Left, and Right are relative to the PageImageableSize, where TopLeft is denoted by the origin of the x-axis and y-axis.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="34482-124">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="34482-124">Structural Content</span></span>

<span data-ttu-id="34482-125">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="34482-125">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="34482-126">Variables de structure</span><span class="sxs-lookup"><span data-stu-id="34482-126">Structure Variables</span></span>

<span data-ttu-id="34482-127">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="34482-127">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="34482-128">Nom</span><span class="sxs-lookup"><span data-stu-id="34482-128">Name</span></span>                               | <span data-ttu-id="34482-129">Type de données</span><span class="sxs-lookup"><span data-stu-id="34482-129">Data type</span></span>         | <span data-ttu-id="34482-130">Unité</span><span class="sxs-lookup"><span data-stu-id="34482-130">Unit</span></span>                  | <span data-ttu-id="34482-131">Valeurs prises en charge</span><span class="sxs-lookup"><span data-stu-id="34482-131">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="34482-132">Résumé</span><span class="sxs-lookup"><span data-stu-id="34482-132">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="34482-133">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="34482-133">\_OptionName\_</span></span><br/>          | <span data-ttu-id="34482-134">string</span><span class="sxs-lookup"><span data-stu-id="34482-134">string</span></span><br/> | <span data-ttu-id="34482-135">caractères</span><span class="sxs-lookup"><span data-stu-id="34482-135">characters</span></span><br/> | <span data-ttu-id="34482-136">Nom complet valide tel que défini par les [espaces de noms dans XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="34482-136">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="34482-137">Si aucun espace de noms n’est spécifié, l’espace de noms par défaut est utilisé.</span><span class="sxs-lookup"><span data-stu-id="34482-137">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="34482-138">Nom de l'option.</span><span class="sxs-lookup"><span data-stu-id="34482-138">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="34482-139">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="34482-139">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="34482-140">string</span><span class="sxs-lookup"><span data-stu-id="34482-140">string</span></span><br/> | <span data-ttu-id="34482-141">n/a</span><span class="sxs-lookup"><span data-stu-id="34482-141">n/a</span></span><br/>        | <span data-ttu-id="34482-142">True, False.</span><span class="sxs-lookup"><span data-stu-id="34482-142">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="34482-143">Définit une option qui, lorsqu’elle est sélectionnée, désactive cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="34482-143">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="34482-144">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="34482-144">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="34482-145">Les mots clés de schéma d’impression publics sont définis dans l' https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords espace de noms.</span><span class="sxs-lookup"><span data-stu-id="34482-145">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="34482-146">Le contenu de la Extensible Markup Language publique (XML) pour ce mot clé est défini ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="34482-146">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="34482-147">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="34482-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="34482-148">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="34482-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




