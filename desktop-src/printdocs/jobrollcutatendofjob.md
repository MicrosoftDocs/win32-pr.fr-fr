---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: 1e2cd767-685b-47d8-9020-a0a5dda63506
title: JobRollCutAtEndOfJob
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62eda63fe0d801bc1039af2c514c284440b1be47
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "106524797"
---
# <a name="jobrollcutatendofjob"></a><span data-ttu-id="60dc9-104">JobRollCutAtEndOfJob</span><span class="sxs-lookup"><span data-stu-id="60dc9-104">JobRollCutAtEndOfJob</span></span>

<span data-ttu-id="60dc9-105">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="60dc9-105">This topic is not current.</span></span> <span data-ttu-id="60dc9-106">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="60dc9-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="60dc9-107">Décrit la méthode de coupe pour le papier en rouleau.</span><span class="sxs-lookup"><span data-stu-id="60dc9-107">Describes the cutting method for roll paper.</span></span> <span data-ttu-id="60dc9-108">Le rouleau doit être coupé à la fin du travail.</span><span class="sxs-lookup"><span data-stu-id="60dc9-108">The roll should be cut at the end of the job.</span></span>

-   [<span data-ttu-id="60dc9-109">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="60dc9-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="60dc9-110">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="60dc9-110">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="60dc9-111">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="60dc9-111">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="60dc9-112">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="60dc9-112">Element Information</span></span>



| <span data-ttu-id="60dc9-113">Nom</span><span class="sxs-lookup"><span data-stu-id="60dc9-113">Name</span></span>                       |                    |
|----------------------------|--------------------|
| <span data-ttu-id="60dc9-114">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="60dc9-114">Element Type</span></span> <br/>   | <span data-ttu-id="60dc9-115">Fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="60dc9-115">Feature</span></span><br/> |
| <span data-ttu-id="60dc9-116">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="60dc9-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="60dc9-117">Travail</span><span class="sxs-lookup"><span data-stu-id="60dc9-117">Job</span></span><br/>     |
| <span data-ttu-id="60dc9-118">Notes</span><span class="sxs-lookup"><span data-stu-id="60dc9-118">Notes</span></span> <br/>          | <span data-ttu-id="60dc9-119">Aucun</span><span class="sxs-lookup"><span data-stu-id="60dc9-119">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="60dc9-120">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="60dc9-120">Structural Content</span></span>

<span data-ttu-id="60dc9-121">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="60dc9-121">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:JobRollCutAtEndOfJobAtEndOfJob">
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

## <a name="structure-variables"></a><span data-ttu-id="60dc9-122">Variables de structure</span><span class="sxs-lookup"><span data-stu-id="60dc9-122">Structure Variables</span></span>

<span data-ttu-id="60dc9-123">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="60dc9-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="60dc9-124">Nom</span><span class="sxs-lookup"><span data-stu-id="60dc9-124">Name</span></span>                               | <span data-ttu-id="60dc9-125">Type de données</span><span class="sxs-lookup"><span data-stu-id="60dc9-125">Data type</span></span>         | <span data-ttu-id="60dc9-126">Unité</span><span class="sxs-lookup"><span data-stu-id="60dc9-126">Unit</span></span>                  | <span data-ttu-id="60dc9-127">Valeurs prises en charge</span><span class="sxs-lookup"><span data-stu-id="60dc9-127">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="60dc9-128">Résumé</span><span class="sxs-lookup"><span data-stu-id="60dc9-128">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="60dc9-129">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="60dc9-129">\_OptionName\_</span></span><br/>          | <span data-ttu-id="60dc9-130">string</span><span class="sxs-lookup"><span data-stu-id="60dc9-130">string</span></span><br/> | <span data-ttu-id="60dc9-131">caractères</span><span class="sxs-lookup"><span data-stu-id="60dc9-131">characters</span></span><br/> | <span data-ttu-id="60dc9-132">Nom complet valide tel que défini par les [espaces de noms dans XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="60dc9-132">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="60dc9-133">Si aucun espace de noms n’est spécifié, l’espace de noms par défaut est utilisé.</span><span class="sxs-lookup"><span data-stu-id="60dc9-133">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="60dc9-134">Nom de l'option.</span><span class="sxs-lookup"><span data-stu-id="60dc9-134">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="60dc9-135">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="60dc9-135">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="60dc9-136">string</span><span class="sxs-lookup"><span data-stu-id="60dc9-136">string</span></span><br/> | <span data-ttu-id="60dc9-137">n/a</span><span class="sxs-lookup"><span data-stu-id="60dc9-137">n/a</span></span><br/>        | <span data-ttu-id="60dc9-138">True, False.</span><span class="sxs-lookup"><span data-stu-id="60dc9-138">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="60dc9-139">Définit une option qui, lorsqu’elle est sélectionnée, désactive cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="60dc9-139">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="60dc9-140">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="60dc9-140">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="60dc9-141">Les mots clés de schéma d’impression publics sont définis dans l' https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords espace de noms.</span><span class="sxs-lookup"><span data-stu-id="60dc9-141">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="60dc9-142">Le contenu de la Extensible Markup Language publique (XML) pour ce mot clé est défini ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="60dc9-142">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:JobRollCutAtEndOfJob">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!--Specifies cutting at the edge of the image -->
  <psf:Option name="psk:CutSheetAtImageEdge" />
  <!--Specifies cutting for standard media size -->
  <psf:Option name="psk:CutSheetAtStandardMediaSize" />
  <!--Specifies no job roll cut -->
  <psf:Option name="psk:None" />
</psf:Feature>
    
```

## <a name="related-topics"></a><span data-ttu-id="60dc9-143">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="60dc9-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="60dc9-144">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="60dc9-144">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




