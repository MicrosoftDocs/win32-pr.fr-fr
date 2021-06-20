---
description: En savoir plus sur l’élément DocumentHolePunch, qui décrit les caractéristiques de perforation de la sortie.
ms.assetid: 46fd5e22-a2f3-424d-8c2f-2d5ac089a230
title: DocumentHolePunch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 760559d3bb155030ff72a616096e5a860ba0d6b0
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409291"
---
# <a name="documentholepunch"></a><span data-ttu-id="0538a-103">DocumentHolePunch</span><span class="sxs-lookup"><span data-stu-id="0538a-103">DocumentHolePunch</span></span>

<span data-ttu-id="0538a-104">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="0538a-104">This topic is not current.</span></span> <span data-ttu-id="0538a-105">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="0538a-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="0538a-106">Décrit les caractéristiques de perforation de la sortie.</span><span class="sxs-lookup"><span data-stu-id="0538a-106">Describes the hole punching characteristics of the output.</span></span> <span data-ttu-id="0538a-107">Chaque document est perforé séparément.</span><span class="sxs-lookup"><span data-stu-id="0538a-107">Each document is punched separately.</span></span> <span data-ttu-id="0538a-108">Les mots clés JobHolePunch et DocumentHolePunch s’excluent mutuellement.</span><span class="sxs-lookup"><span data-stu-id="0538a-108">The JobHolePunch and DocumentHolePunch keywords are mutually exclusive.</span></span> <span data-ttu-id="0538a-109">Ils ne doivent pas être spécifiés simultanément dans un document de fonctionnalités PrintTicket ou Print.</span><span class="sxs-lookup"><span data-stu-id="0538a-109">Both should not be specified simultaneously in a PrintTicket or Print Capabilities document.</span></span>

-   [<span data-ttu-id="0538a-110">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="0538a-110">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="0538a-111">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="0538a-111">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="0538a-112">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="0538a-112">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="0538a-113">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="0538a-113">Element Information</span></span>



| <span data-ttu-id="0538a-114">Nom</span><span class="sxs-lookup"><span data-stu-id="0538a-114">Name</span></span> | <span data-ttu-id="0538a-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="0538a-115">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="0538a-116">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="0538a-116">Element Type</span></span> <br/>   | <span data-ttu-id="0538a-117">Fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="0538a-117">Feature</span></span><br/>                                                             |
| <span data-ttu-id="0538a-118">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="0538a-118">Scoping Prefix</span></span> <br/> | <span data-ttu-id="0538a-119">Document</span><span class="sxs-lookup"><span data-stu-id="0538a-119">Document</span></span><br/>                                                            |
| <span data-ttu-id="0538a-120">Notes</span><span class="sxs-lookup"><span data-stu-id="0538a-120">Notes</span></span> <br/>          | <span data-ttu-id="0538a-121">Haut, bas, gauche et droite sont relatifs à PageImageableSize.</span><span class="sxs-lookup"><span data-stu-id="0538a-121">Top, Bottom, Left, and Right are relative to the PageImageableSize.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="0538a-122">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="0538a-122">Structural Content</span></span>

<span data-ttu-id="0538a-123">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="0538a-123">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:DocumentHolePunch">
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

## <a name="structure-variables"></a><span data-ttu-id="0538a-124">Variables de structure</span><span class="sxs-lookup"><span data-stu-id="0538a-124">Structure Variables</span></span>

<span data-ttu-id="0538a-125">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="0538a-125">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="0538a-126">Nom</span><span class="sxs-lookup"><span data-stu-id="0538a-126">Name</span></span>                               | <span data-ttu-id="0538a-127">Type de données</span><span class="sxs-lookup"><span data-stu-id="0538a-127">Data type</span></span>         | <span data-ttu-id="0538a-128">Unité</span><span class="sxs-lookup"><span data-stu-id="0538a-128">Unit</span></span>                  | <span data-ttu-id="0538a-129">Valeurs prises en charge</span><span class="sxs-lookup"><span data-stu-id="0538a-129">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="0538a-130">Résumé</span><span class="sxs-lookup"><span data-stu-id="0538a-130">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="0538a-131">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="0538a-131">\_OptionName\_</span></span><br/>          | <span data-ttu-id="0538a-132">string</span><span class="sxs-lookup"><span data-stu-id="0538a-132">string</span></span><br/> | <span data-ttu-id="0538a-133">caractères</span><span class="sxs-lookup"><span data-stu-id="0538a-133">characters</span></span><br/> | <span data-ttu-id="0538a-134">Nom complet valide tel que défini par les [espaces de noms dans XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="0538a-134">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="0538a-135">Si aucun espace de noms n’est spécifié, l’espace de noms par défaut est utilisé.</span><span class="sxs-lookup"><span data-stu-id="0538a-135">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="0538a-136">Nom de l'option.</span><span class="sxs-lookup"><span data-stu-id="0538a-136">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="0538a-137">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="0538a-137">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="0538a-138">string</span><span class="sxs-lookup"><span data-stu-id="0538a-138">string</span></span><br/> | <span data-ttu-id="0538a-139">n/a</span><span class="sxs-lookup"><span data-stu-id="0538a-139">n/a</span></span><br/>        | <span data-ttu-id="0538a-140">True, False.</span><span class="sxs-lookup"><span data-stu-id="0538a-140">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="0538a-141">Définit une option qui, lorsqu’elle est sélectionnée, désactive cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="0538a-141">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="0538a-142">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="0538a-142">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="0538a-143">Les mots clés de schéma d’impression publics sont définis dans l' https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords espace de noms.</span><span class="sxs-lookup"><span data-stu-id="0538a-143">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="0538a-144">Le contenu de la Extensible Markup Language publique (XML) pour ce mot clé est défini ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="0538a-144">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:DocumentHolePunch">
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

## <a name="related-topics"></a><span data-ttu-id="0538a-145">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0538a-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0538a-146">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="0538a-146">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




