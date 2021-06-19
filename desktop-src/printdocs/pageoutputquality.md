---
description: En savoir plus sur l’élément configurable par l’utilisateur PageOutputQuality. Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: 4720f812-a71a-458f-85fa-7885cca0dbbb
title: PageOutputQuality
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8001d8ffd6bb3ead50a27b9ea36c9849c475576f
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395586"
---
# <a name="pageoutputquality"></a><span data-ttu-id="04d4d-105">PageOutputQuality</span><span class="sxs-lookup"><span data-stu-id="04d4d-105">PageOutputQuality</span></span>

<span data-ttu-id="04d4d-106">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="04d4d-106">This topic is not current.</span></span> <span data-ttu-id="04d4d-107">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="04d4d-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="04d4d-108">Décrit le niveau de qualité de la sortie.</span><span class="sxs-lookup"><span data-stu-id="04d4d-108">Describes the quality level of the output.</span></span>

-   [<span data-ttu-id="04d4d-109">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="04d4d-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="04d4d-110">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="04d4d-110">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="04d4d-111">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="04d4d-111">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="04d4d-112">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="04d4d-112">Element Information</span></span>



| <span data-ttu-id="04d4d-113">Nom</span><span class="sxs-lookup"><span data-stu-id="04d4d-113">Name</span></span> | <span data-ttu-id="04d4d-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="04d4d-114">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="04d4d-115">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="04d4d-115">Element Type</span></span> <br/>   | <span data-ttu-id="04d4d-116">Fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="04d4d-116">Feature</span></span><br/> |
| <span data-ttu-id="04d4d-117">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="04d4d-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="04d4d-118">Page</span><span class="sxs-lookup"><span data-stu-id="04d4d-118">Page</span></span><br/>    |
| <span data-ttu-id="04d4d-119">Notes</span><span class="sxs-lookup"><span data-stu-id="04d4d-119">Notes</span></span> <br/>          | <span data-ttu-id="04d4d-120">Aucun</span><span class="sxs-lookup"><span data-stu-id="04d4d-120">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="04d4d-121">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="04d4d-121">Structural Content</span></span>

<span data-ttu-id="04d4d-122">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="04d4d-122">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageOutputQuality">
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

## <a name="structure-variables"></a><span data-ttu-id="04d4d-123">Variables de structure</span><span class="sxs-lookup"><span data-stu-id="04d4d-123">Structure Variables</span></span>

<span data-ttu-id="04d4d-124">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="04d4d-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="04d4d-125">Nom</span><span class="sxs-lookup"><span data-stu-id="04d4d-125">Name</span></span>                               | <span data-ttu-id="04d4d-126">Type de données</span><span class="sxs-lookup"><span data-stu-id="04d4d-126">Data type</span></span>         | <span data-ttu-id="04d4d-127">Unité</span><span class="sxs-lookup"><span data-stu-id="04d4d-127">Unit</span></span>                  | <span data-ttu-id="04d4d-128">Valeurs prises en charge</span><span class="sxs-lookup"><span data-stu-id="04d4d-128">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="04d4d-129">Résumé</span><span class="sxs-lookup"><span data-stu-id="04d4d-129">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="04d4d-130">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="04d4d-130">\_OptionName\_</span></span><br/>          | <span data-ttu-id="04d4d-131">string</span><span class="sxs-lookup"><span data-stu-id="04d4d-131">string</span></span><br/> | <span data-ttu-id="04d4d-132">caractères</span><span class="sxs-lookup"><span data-stu-id="04d4d-132">characters</span></span><br/> | <span data-ttu-id="04d4d-133">Nom complet valide tel que défini par les [espaces de noms dans XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="04d4d-133">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="04d4d-134">Si aucun espace de noms n’est spécifié, l’espace de noms par défaut est utilisé.</span><span class="sxs-lookup"><span data-stu-id="04d4d-134">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="04d4d-135">Nom de l’option</span><span class="sxs-lookup"><span data-stu-id="04d4d-135">The name of the option</span></span><br/>                                            |
| <span data-ttu-id="04d4d-136">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="04d4d-136">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="04d4d-137">string</span><span class="sxs-lookup"><span data-stu-id="04d4d-137">string</span></span><br/> | <span data-ttu-id="04d4d-138">n/a</span><span class="sxs-lookup"><span data-stu-id="04d4d-138">n/a</span></span><br/>        | <span data-ttu-id="04d4d-139">True, False</span><span class="sxs-lookup"><span data-stu-id="04d4d-139">True, False</span></span><br/>                                                                                                                                                                | <span data-ttu-id="04d4d-140">Définit une option qui, lorsqu’elle est sélectionnée, désactive cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="04d4d-140">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="04d4d-141">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="04d4d-141">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="04d4d-142">Les mots clés de schéma d’impression publics sont définis dans l' https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords espace de noms.</span><span class="sxs-lookup"><span data-stu-id="04d4d-142">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="04d4d-143">Le contenu de la Extensible Markup Language publique (XML) pour ce mot clé est défini ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="04d4d-143">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageOutputQuality">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies the intent for automatic output (allow the client to automatically choose the best settings). -->
  <psf:Option name="psk:Automatic" />
  <!-- Specifies the intent for draft output (balanced for draft quality text and graphics). -->
  <psf:Option name="psk:Draft" />
  <!-- Specifies the intent for fax output (balanced for standard fax quality). -->
  <psf:Option name="psk:Fax" />
  <!-- Specifies the intent for high quality output (balanced for high quality text and graphics). -->
  <psf:Option name="psk:High" />
  <!-- Specifies the intent for normal output (balanced for good quality text and graphics). -->
  <psf:Option name="psk:Normal" />
  <!-- Specifies the intent for photographic output (images should have the highest quality). -->
  <psf:Option name="psk:Photographic" />
  <!-- Specifies the intent for text only output (graphics may output poorly or not at all). -->
  <psf:Option name="psk:Text" />
</psf:Feature>
    
```

## <a name="related-topics"></a><span data-ttu-id="04d4d-144">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="04d4d-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="04d4d-145">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="04d4d-145">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




