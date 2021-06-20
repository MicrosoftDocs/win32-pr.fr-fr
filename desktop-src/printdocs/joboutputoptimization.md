---
description: En savoir plus sur le JobOutputOptimization, qui décrit le traitement du travail, destiné à optimiser la sortie pour des scénarios d’utilisation particuliers, comme indiqué par l’option spécifiée.
ms.assetid: 40925dfe-494c-49b5-ae57-de369723ba76
title: JobOutputOptimization
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdbb65f86b5ed4fd30c056e234b88197d4ab475d
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408792"
---
# <a name="joboutputoptimization"></a><span data-ttu-id="65689-103">JobOutputOptimization</span><span class="sxs-lookup"><span data-stu-id="65689-103">JobOutputOptimization</span></span>

<span data-ttu-id="65689-104">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="65689-104">This topic is not current.</span></span> <span data-ttu-id="65689-105">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="65689-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="65689-106">Décrit le traitement du travail, destiné à optimiser la sortie pour des scénarios d’utilisation particuliers, comme indiqué par l’option spécifiée.</span><span class="sxs-lookup"><span data-stu-id="65689-106">Describes the job processing, intended to optimize the output for particular use scenarios as indicated by the option specified.</span></span>

-   [<span data-ttu-id="65689-107">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="65689-107">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="65689-108">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="65689-108">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="65689-109">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="65689-109">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="65689-110">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="65689-110">Element Information</span></span>



| <span data-ttu-id="65689-111">Nom</span><span class="sxs-lookup"><span data-stu-id="65689-111">Name</span></span> | <span data-ttu-id="65689-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="65689-112">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="65689-113">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="65689-113">Element Type</span></span> <br/>   | <span data-ttu-id="65689-114">Fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="65689-114">Feature</span></span><br/> |
| <span data-ttu-id="65689-115">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="65689-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="65689-116">Travail</span><span class="sxs-lookup"><span data-stu-id="65689-116">Job</span></span><br/>     |
| <span data-ttu-id="65689-117">Notes</span><span class="sxs-lookup"><span data-stu-id="65689-117">Notes</span></span> <br/>          | <span data-ttu-id="65689-118">Aucun</span><span class="sxs-lookup"><span data-stu-id="65689-118">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="65689-119">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="65689-119">Structural Content</span></span>

<span data-ttu-id="65689-120">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="65689-120">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:JobOutputOptimization">
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

## <a name="structure-variables"></a><span data-ttu-id="65689-121">Variables de structure</span><span class="sxs-lookup"><span data-stu-id="65689-121">Structure Variables</span></span>

<span data-ttu-id="65689-122">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="65689-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="65689-123">Nom</span><span class="sxs-lookup"><span data-stu-id="65689-123">Name</span></span>                               | <span data-ttu-id="65689-124">Type de données</span><span class="sxs-lookup"><span data-stu-id="65689-124">Data type</span></span>         | <span data-ttu-id="65689-125">Unité</span><span class="sxs-lookup"><span data-stu-id="65689-125">Unit</span></span>                  | <span data-ttu-id="65689-126">Valeurs prises en charge</span><span class="sxs-lookup"><span data-stu-id="65689-126">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="65689-127">Résumé</span><span class="sxs-lookup"><span data-stu-id="65689-127">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="65689-128">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="65689-128">\_OptionName\_</span></span><br/>          | <span data-ttu-id="65689-129">string</span><span class="sxs-lookup"><span data-stu-id="65689-129">string</span></span><br/> | <span data-ttu-id="65689-130">caractères</span><span class="sxs-lookup"><span data-stu-id="65689-130">characters</span></span><br/> | <span data-ttu-id="65689-131">Nom complet valide tel que défini par les [espaces de noms dans XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="65689-131">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="65689-132">Si aucun espace de noms n’est spécifié, l’espace de noms par défaut est utilisé.</span><span class="sxs-lookup"><span data-stu-id="65689-132">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="65689-133">Nom de l'option.</span><span class="sxs-lookup"><span data-stu-id="65689-133">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="65689-134">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="65689-134">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="65689-135">string</span><span class="sxs-lookup"><span data-stu-id="65689-135">string</span></span><br/> | <span data-ttu-id="65689-136">n/a</span><span class="sxs-lookup"><span data-stu-id="65689-136">n/a</span></span><br/>        | <span data-ttu-id="65689-137">True, False.</span><span class="sxs-lookup"><span data-stu-id="65689-137">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="65689-138">Définit une option qui, lorsqu’elle est sélectionnée, désactive cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="65689-138">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="65689-139">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="65689-139">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="65689-140">Les mots clés de schéma d’impression publics sont définis dans l' https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords espace de noms.</span><span class="sxs-lookup"><span data-stu-id="65689-140">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="65689-141">Le contenu de la Extensible Markup Language publique (XML) pour ce mot clé est défini ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="65689-141">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:JobOutputOptimization">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies the job processing be optimized for archive output. -->
  <psf:Option name="psk:ArchiveFormat" />
  <!-- Specifies the job processing be optimized for portability (cross-device) of output. -->
  <psf:Option name="psk:OptimizeForPortability" />
  <!-- Specifies the job processing be optimized for quality of output. -->
  <psf:Option name="psk:OptimizeForQuality" />
  <!-- Specifies the job processing be optimized for speed of output. -->
  <psf:Option name="psk:OptimizeForSpeed" />
  <!-- Specifies the job processing should not be optimized for a particular scenario. -->
  <psf:Option name="psk:None" />
</psf:Feature>
    
```

## <a name="related-topics"></a><span data-ttu-id="65689-142">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="65689-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="65689-143">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="65689-143">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




