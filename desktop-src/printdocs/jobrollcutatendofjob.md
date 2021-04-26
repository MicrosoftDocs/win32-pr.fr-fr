---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: 1e2cd767-685b-47d8-9020-a0a5dda63506
title: JobRollCutAtEndOfJob
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 178b045546552048b2a66a1c0824645c1720b1a7
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107993936"
---
# <a name="jobrollcutatendofjob"></a><span data-ttu-id="85a35-104">JobRollCutAtEndOfJob</span><span class="sxs-lookup"><span data-stu-id="85a35-104">JobRollCutAtEndOfJob</span></span>

<span data-ttu-id="85a35-105">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="85a35-105">This topic is not current.</span></span> <span data-ttu-id="85a35-106">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="85a35-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="85a35-107">Décrit la méthode de coupe pour le papier en rouleau.</span><span class="sxs-lookup"><span data-stu-id="85a35-107">Describes the cutting method for roll paper.</span></span> <span data-ttu-id="85a35-108">Le rouleau doit être coupé à la fin du travail.</span><span class="sxs-lookup"><span data-stu-id="85a35-108">The roll should be cut at the end of the job.</span></span>

-   [<span data-ttu-id="85a35-109">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="85a35-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="85a35-110">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="85a35-110">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="85a35-111">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="85a35-111">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="85a35-112">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="85a35-112">Element Information</span></span>



| <span data-ttu-id="85a35-113">Nom</span><span class="sxs-lookup"><span data-stu-id="85a35-113">Name</span></span> | <span data-ttu-id="85a35-114">Value</span><span class="sxs-lookup"><span data-stu-id="85a35-114">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="85a35-115">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="85a35-115">Element Type</span></span> <br/>   | <span data-ttu-id="85a35-116">Fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="85a35-116">Feature</span></span><br/> |
| <span data-ttu-id="85a35-117">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="85a35-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="85a35-118">Travail</span><span class="sxs-lookup"><span data-stu-id="85a35-118">Job</span></span><br/>     |
| <span data-ttu-id="85a35-119">Notes</span><span class="sxs-lookup"><span data-stu-id="85a35-119">Notes</span></span> <br/>          | <span data-ttu-id="85a35-120">Aucun</span><span class="sxs-lookup"><span data-stu-id="85a35-120">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="85a35-121">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="85a35-121">Structural Content</span></span>

<span data-ttu-id="85a35-122">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="85a35-122">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="85a35-123">Variables de structure</span><span class="sxs-lookup"><span data-stu-id="85a35-123">Structure Variables</span></span>

<span data-ttu-id="85a35-124">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="85a35-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="85a35-125">Nom</span><span class="sxs-lookup"><span data-stu-id="85a35-125">Name</span></span>                               | <span data-ttu-id="85a35-126">Type de données</span><span class="sxs-lookup"><span data-stu-id="85a35-126">Data type</span></span>         | <span data-ttu-id="85a35-127">Unité</span><span class="sxs-lookup"><span data-stu-id="85a35-127">Unit</span></span>                  | <span data-ttu-id="85a35-128">Valeurs prises en charge</span><span class="sxs-lookup"><span data-stu-id="85a35-128">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="85a35-129">Résumé</span><span class="sxs-lookup"><span data-stu-id="85a35-129">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="85a35-130">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="85a35-130">\_OptionName\_</span></span><br/>          | <span data-ttu-id="85a35-131">string</span><span class="sxs-lookup"><span data-stu-id="85a35-131">string</span></span><br/> | <span data-ttu-id="85a35-132">caractères</span><span class="sxs-lookup"><span data-stu-id="85a35-132">characters</span></span><br/> | <span data-ttu-id="85a35-133">Nom complet valide tel que défini par les [espaces de noms dans XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="85a35-133">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="85a35-134">Si aucun espace de noms n’est spécifié, l’espace de noms par défaut est utilisé.</span><span class="sxs-lookup"><span data-stu-id="85a35-134">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="85a35-135">Nom de l'option.</span><span class="sxs-lookup"><span data-stu-id="85a35-135">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="85a35-136">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="85a35-136">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="85a35-137">string</span><span class="sxs-lookup"><span data-stu-id="85a35-137">string</span></span><br/> | <span data-ttu-id="85a35-138">n/a</span><span class="sxs-lookup"><span data-stu-id="85a35-138">n/a</span></span><br/>        | <span data-ttu-id="85a35-139">True, False.</span><span class="sxs-lookup"><span data-stu-id="85a35-139">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="85a35-140">Définit une option qui, lorsqu’elle est sélectionnée, désactive cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="85a35-140">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="85a35-141">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="85a35-141">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="85a35-142">Les mots clés de schéma d’impression publics sont définis dans l' https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords espace de noms.</span><span class="sxs-lookup"><span data-stu-id="85a35-142">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="85a35-143">Le contenu de la Extensible Markup Language publique (XML) pour ce mot clé est défini ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="85a35-143">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="85a35-144">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="85a35-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="85a35-145">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="85a35-145">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




