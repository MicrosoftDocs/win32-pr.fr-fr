---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: 40925dfe-494c-49b5-ae57-de369723ba76
title: JobOutputOptimization
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b76364aca1a9b6c8019a709c1cd0b7b1ad03020c
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997746"
---
# <a name="joboutputoptimization"></a><span data-ttu-id="364fb-104">JobOutputOptimization</span><span class="sxs-lookup"><span data-stu-id="364fb-104">JobOutputOptimization</span></span>

<span data-ttu-id="364fb-105">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="364fb-105">This topic is not current.</span></span> <span data-ttu-id="364fb-106">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="364fb-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="364fb-107">Décrit le traitement du travail, destiné à optimiser la sortie pour des scénarios d’utilisation particuliers, comme indiqué par l’option spécifiée.</span><span class="sxs-lookup"><span data-stu-id="364fb-107">Describes the job processing, intended to optimize the output for particular use scenarios as indicated by the option specified.</span></span>

-   [<span data-ttu-id="364fb-108">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="364fb-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="364fb-109">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="364fb-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="364fb-110">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="364fb-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="364fb-111">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="364fb-111">Element Information</span></span>



| <span data-ttu-id="364fb-112">Nom</span><span class="sxs-lookup"><span data-stu-id="364fb-112">Name</span></span> | <span data-ttu-id="364fb-113">Value</span><span class="sxs-lookup"><span data-stu-id="364fb-113">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="364fb-114">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="364fb-114">Element Type</span></span> <br/>   | <span data-ttu-id="364fb-115">Fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="364fb-115">Feature</span></span><br/> |
| <span data-ttu-id="364fb-116">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="364fb-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="364fb-117">Travail</span><span class="sxs-lookup"><span data-stu-id="364fb-117">Job</span></span><br/>     |
| <span data-ttu-id="364fb-118">Notes</span><span class="sxs-lookup"><span data-stu-id="364fb-118">Notes</span></span> <br/>          | <span data-ttu-id="364fb-119">Aucun</span><span class="sxs-lookup"><span data-stu-id="364fb-119">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="364fb-120">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="364fb-120">Structural Content</span></span>

<span data-ttu-id="364fb-121">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="364fb-121">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="364fb-122">Variables de structure</span><span class="sxs-lookup"><span data-stu-id="364fb-122">Structure Variables</span></span>

<span data-ttu-id="364fb-123">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="364fb-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="364fb-124">Nom</span><span class="sxs-lookup"><span data-stu-id="364fb-124">Name</span></span>                               | <span data-ttu-id="364fb-125">Type de données</span><span class="sxs-lookup"><span data-stu-id="364fb-125">Data type</span></span>         | <span data-ttu-id="364fb-126">Unité</span><span class="sxs-lookup"><span data-stu-id="364fb-126">Unit</span></span>                  | <span data-ttu-id="364fb-127">Valeurs prises en charge</span><span class="sxs-lookup"><span data-stu-id="364fb-127">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="364fb-128">Résumé</span><span class="sxs-lookup"><span data-stu-id="364fb-128">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="364fb-129">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="364fb-129">\_OptionName\_</span></span><br/>          | <span data-ttu-id="364fb-130">string</span><span class="sxs-lookup"><span data-stu-id="364fb-130">string</span></span><br/> | <span data-ttu-id="364fb-131">caractères</span><span class="sxs-lookup"><span data-stu-id="364fb-131">characters</span></span><br/> | <span data-ttu-id="364fb-132">Nom complet valide tel que défini par les [espaces de noms dans XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="364fb-132">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="364fb-133">Si aucun espace de noms n’est spécifié, l’espace de noms par défaut est utilisé.</span><span class="sxs-lookup"><span data-stu-id="364fb-133">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="364fb-134">Nom de l'option.</span><span class="sxs-lookup"><span data-stu-id="364fb-134">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="364fb-135">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="364fb-135">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="364fb-136">string</span><span class="sxs-lookup"><span data-stu-id="364fb-136">string</span></span><br/> | <span data-ttu-id="364fb-137">n/a</span><span class="sxs-lookup"><span data-stu-id="364fb-137">n/a</span></span><br/>        | <span data-ttu-id="364fb-138">True, False.</span><span class="sxs-lookup"><span data-stu-id="364fb-138">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="364fb-139">Définit une option qui, lorsqu’elle est sélectionnée, désactive cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="364fb-139">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="364fb-140">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="364fb-140">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="364fb-141">Les mots clés de schéma d’impression publics sont définis dans l' https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords espace de noms.</span><span class="sxs-lookup"><span data-stu-id="364fb-141">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="364fb-142">Le contenu de la Extensible Markup Language publique (XML) pour ce mot clé est défini ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="364fb-142">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="364fb-143">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="364fb-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="364fb-144">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="364fb-144">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




