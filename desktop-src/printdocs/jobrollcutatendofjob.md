---
description: En savoir plus sur l’élément JobRollCutAtEndOfJob, qui décrit la méthode de coupe pour le papier en rouleau. Le rouleau doit être coupé à la fin du travail.
ms.assetid: 1e2cd767-685b-47d8-9020-a0a5dda63506
title: JobRollCutAtEndOfJob
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11fdb973f3fda9fea28f64f0edb232910f2d2201
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408662"
---
# <a name="jobrollcutatendofjob"></a><span data-ttu-id="57736-104">JobRollCutAtEndOfJob</span><span class="sxs-lookup"><span data-stu-id="57736-104">JobRollCutAtEndOfJob</span></span>

<span data-ttu-id="57736-105">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="57736-105">This topic is not current.</span></span> <span data-ttu-id="57736-106">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="57736-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="57736-107">Décrit la méthode de coupe pour le papier en rouleau.</span><span class="sxs-lookup"><span data-stu-id="57736-107">Describes the cutting method for roll paper.</span></span> <span data-ttu-id="57736-108">Le rouleau doit être coupé à la fin du travail.</span><span class="sxs-lookup"><span data-stu-id="57736-108">The roll should be cut at the end of the job.</span></span>

-   [<span data-ttu-id="57736-109">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="57736-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="57736-110">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="57736-110">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="57736-111">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="57736-111">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="57736-112">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="57736-112">Element Information</span></span>



| <span data-ttu-id="57736-113">Nom</span><span class="sxs-lookup"><span data-stu-id="57736-113">Name</span></span> | <span data-ttu-id="57736-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="57736-114">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="57736-115">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="57736-115">Element Type</span></span> <br/>   | <span data-ttu-id="57736-116">Fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="57736-116">Feature</span></span><br/> |
| <span data-ttu-id="57736-117">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="57736-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="57736-118">Travail</span><span class="sxs-lookup"><span data-stu-id="57736-118">Job</span></span><br/>     |
| <span data-ttu-id="57736-119">Notes</span><span class="sxs-lookup"><span data-stu-id="57736-119">Notes</span></span> <br/>          | <span data-ttu-id="57736-120">Aucun</span><span class="sxs-lookup"><span data-stu-id="57736-120">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="57736-121">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="57736-121">Structural Content</span></span>

<span data-ttu-id="57736-122">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="57736-122">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="57736-123">Variables de structure</span><span class="sxs-lookup"><span data-stu-id="57736-123">Structure Variables</span></span>

<span data-ttu-id="57736-124">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="57736-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="57736-125">Nom</span><span class="sxs-lookup"><span data-stu-id="57736-125">Name</span></span>                               | <span data-ttu-id="57736-126">Type de données</span><span class="sxs-lookup"><span data-stu-id="57736-126">Data type</span></span>         | <span data-ttu-id="57736-127">Unité</span><span class="sxs-lookup"><span data-stu-id="57736-127">Unit</span></span>                  | <span data-ttu-id="57736-128">Valeurs prises en charge</span><span class="sxs-lookup"><span data-stu-id="57736-128">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="57736-129">Résumé</span><span class="sxs-lookup"><span data-stu-id="57736-129">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="57736-130">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="57736-130">\_OptionName\_</span></span><br/>          | <span data-ttu-id="57736-131">string</span><span class="sxs-lookup"><span data-stu-id="57736-131">string</span></span><br/> | <span data-ttu-id="57736-132">caractères</span><span class="sxs-lookup"><span data-stu-id="57736-132">characters</span></span><br/> | <span data-ttu-id="57736-133">Nom complet valide tel que défini par les [espaces de noms dans XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="57736-133">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="57736-134">Si aucun espace de noms n’est spécifié, l’espace de noms par défaut est utilisé.</span><span class="sxs-lookup"><span data-stu-id="57736-134">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="57736-135">Nom de l'option.</span><span class="sxs-lookup"><span data-stu-id="57736-135">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="57736-136">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="57736-136">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="57736-137">string</span><span class="sxs-lookup"><span data-stu-id="57736-137">string</span></span><br/> | <span data-ttu-id="57736-138">n/a</span><span class="sxs-lookup"><span data-stu-id="57736-138">n/a</span></span><br/>        | <span data-ttu-id="57736-139">True, False.</span><span class="sxs-lookup"><span data-stu-id="57736-139">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="57736-140">Définit une option qui, lorsqu’elle est sélectionnée, désactive cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="57736-140">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="57736-141">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="57736-141">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="57736-142">Les mots clés de schéma d’impression publics sont définis dans l' https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords espace de noms.</span><span class="sxs-lookup"><span data-stu-id="57736-142">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="57736-143">Le contenu de la Extensible Markup Language publique (XML) pour ce mot clé est défini ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="57736-143">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="57736-144">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="57736-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="57736-145">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="57736-145">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




