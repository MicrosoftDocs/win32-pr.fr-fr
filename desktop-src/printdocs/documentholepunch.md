---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: 46fd5e22-a2f3-424d-8c2f-2d5ac089a230
title: DocumentHolePunch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 825120996d0d488af347ed871386a12d7f8014a7
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997886"
---
# <a name="documentholepunch"></a><span data-ttu-id="1f6e0-104">DocumentHolePunch</span><span class="sxs-lookup"><span data-stu-id="1f6e0-104">DocumentHolePunch</span></span>

<span data-ttu-id="1f6e0-105">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="1f6e0-105">This topic is not current.</span></span> <span data-ttu-id="1f6e0-106">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="1f6e0-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="1f6e0-107">Décrit les caractéristiques de perforation de la sortie.</span><span class="sxs-lookup"><span data-stu-id="1f6e0-107">Describes the hole punching characteristics of the output.</span></span> <span data-ttu-id="1f6e0-108">Chaque document est perforé séparément.</span><span class="sxs-lookup"><span data-stu-id="1f6e0-108">Each document is punched separately.</span></span> <span data-ttu-id="1f6e0-109">Les mots clés JobHolePunch et DocumentHolePunch s’excluent mutuellement.</span><span class="sxs-lookup"><span data-stu-id="1f6e0-109">The JobHolePunch and DocumentHolePunch keywords are mutually exclusive.</span></span> <span data-ttu-id="1f6e0-110">Ils ne doivent pas être spécifiés simultanément dans un document de fonctionnalités PrintTicket ou Print.</span><span class="sxs-lookup"><span data-stu-id="1f6e0-110">Both should not be specified simultaneously in a PrintTicket or Print Capabilities document.</span></span>

-   [<span data-ttu-id="1f6e0-111">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="1f6e0-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="1f6e0-112">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="1f6e0-112">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="1f6e0-113">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="1f6e0-113">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="1f6e0-114">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="1f6e0-114">Element Information</span></span>



| <span data-ttu-id="1f6e0-115">Nom</span><span class="sxs-lookup"><span data-stu-id="1f6e0-115">Name</span></span> | <span data-ttu-id="1f6e0-116">Value</span><span class="sxs-lookup"><span data-stu-id="1f6e0-116">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="1f6e0-117">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="1f6e0-117">Element Type</span></span> <br/>   | <span data-ttu-id="1f6e0-118">Fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="1f6e0-118">Feature</span></span><br/>                                                             |
| <span data-ttu-id="1f6e0-119">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="1f6e0-119">Scoping Prefix</span></span> <br/> | <span data-ttu-id="1f6e0-120">Document</span><span class="sxs-lookup"><span data-stu-id="1f6e0-120">Document</span></span><br/>                                                            |
| <span data-ttu-id="1f6e0-121">Notes</span><span class="sxs-lookup"><span data-stu-id="1f6e0-121">Notes</span></span> <br/>          | <span data-ttu-id="1f6e0-122">Haut, bas, gauche et droite sont relatifs à PageImageableSize.</span><span class="sxs-lookup"><span data-stu-id="1f6e0-122">Top, Bottom, Left, and Right are relative to the PageImageableSize.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="1f6e0-123">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="1f6e0-123">Structural Content</span></span>

<span data-ttu-id="1f6e0-124">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="1f6e0-124">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="1f6e0-125">Variables de structure</span><span class="sxs-lookup"><span data-stu-id="1f6e0-125">Structure Variables</span></span>

<span data-ttu-id="1f6e0-126">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="1f6e0-126">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="1f6e0-127">Nom</span><span class="sxs-lookup"><span data-stu-id="1f6e0-127">Name</span></span>                               | <span data-ttu-id="1f6e0-128">Type de données</span><span class="sxs-lookup"><span data-stu-id="1f6e0-128">Data type</span></span>         | <span data-ttu-id="1f6e0-129">Unité</span><span class="sxs-lookup"><span data-stu-id="1f6e0-129">Unit</span></span>                  | <span data-ttu-id="1f6e0-130">Valeurs prises en charge</span><span class="sxs-lookup"><span data-stu-id="1f6e0-130">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="1f6e0-131">Résumé</span><span class="sxs-lookup"><span data-stu-id="1f6e0-131">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="1f6e0-132">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="1f6e0-132">\_OptionName\_</span></span><br/>          | <span data-ttu-id="1f6e0-133">string</span><span class="sxs-lookup"><span data-stu-id="1f6e0-133">string</span></span><br/> | <span data-ttu-id="1f6e0-134">caractères</span><span class="sxs-lookup"><span data-stu-id="1f6e0-134">characters</span></span><br/> | <span data-ttu-id="1f6e0-135">Nom complet valide tel que défini par les [espaces de noms dans XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="1f6e0-135">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="1f6e0-136">Si aucun espace de noms n’est spécifié, l’espace de noms par défaut est utilisé.</span><span class="sxs-lookup"><span data-stu-id="1f6e0-136">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="1f6e0-137">Nom de l'option.</span><span class="sxs-lookup"><span data-stu-id="1f6e0-137">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="1f6e0-138">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="1f6e0-138">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="1f6e0-139">string</span><span class="sxs-lookup"><span data-stu-id="1f6e0-139">string</span></span><br/> | <span data-ttu-id="1f6e0-140">n/a</span><span class="sxs-lookup"><span data-stu-id="1f6e0-140">n/a</span></span><br/>        | <span data-ttu-id="1f6e0-141">True, False.</span><span class="sxs-lookup"><span data-stu-id="1f6e0-141">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="1f6e0-142">Définit une option qui, lorsqu’elle est sélectionnée, désactive cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="1f6e0-142">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="1f6e0-143">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="1f6e0-143">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="1f6e0-144">Les mots clés de schéma d’impression publics sont définis dans l' https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords espace de noms.</span><span class="sxs-lookup"><span data-stu-id="1f6e0-144">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="1f6e0-145">Le contenu de la Extensible Markup Language publique (XML) pour ce mot clé est défini ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="1f6e0-145">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="1f6e0-146">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1f6e0-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1f6e0-147">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="1f6e0-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




