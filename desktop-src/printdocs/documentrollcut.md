---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: 8eb4e574-3209-459c-9a25-95377b2f7439
title: DocumentRollCut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d3a20c02c50638d532660845efc1b3894f4a7e1
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "104211348"
---
# <a name="documentrollcut"></a><span data-ttu-id="86ec3-104">DocumentRollCut</span><span class="sxs-lookup"><span data-stu-id="86ec3-104">DocumentRollCut</span></span>

<span data-ttu-id="86ec3-105">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="86ec3-105">This topic is not current.</span></span> <span data-ttu-id="86ec3-106">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="86ec3-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="86ec3-107">Décrit la méthode de coupe pour le papier en rouleau.</span><span class="sxs-lookup"><span data-stu-id="86ec3-107">Describes the cutting method for roll paper.</span></span> <span data-ttu-id="86ec3-108">Chaque document est géré séparément.</span><span class="sxs-lookup"><span data-stu-id="86ec3-108">Each document is handled separately.</span></span> <span data-ttu-id="86ec3-109">Les options spécifiées décrivent les différentes méthodes de coupe des rouleaux.</span><span class="sxs-lookup"><span data-stu-id="86ec3-109">The specified options describe the different methods for roll cut.</span></span>

-   [<span data-ttu-id="86ec3-110">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="86ec3-110">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="86ec3-111">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="86ec3-111">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="86ec3-112">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="86ec3-112">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="86ec3-113">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="86ec3-113">Element Information</span></span>



| <span data-ttu-id="86ec3-114">Nom</span><span class="sxs-lookup"><span data-stu-id="86ec3-114">Name</span></span>                       |                     |
|----------------------------|---------------------|
| <span data-ttu-id="86ec3-115">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="86ec3-115">Element Type</span></span> <br/>   | <span data-ttu-id="86ec3-116">Fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="86ec3-116">Feature</span></span><br/>  |
| <span data-ttu-id="86ec3-117">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="86ec3-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="86ec3-118">Document</span><span class="sxs-lookup"><span data-stu-id="86ec3-118">Document</span></span><br/> |
| <span data-ttu-id="86ec3-119">Notes</span><span class="sxs-lookup"><span data-stu-id="86ec3-119">Notes</span></span> <br/>          | <span data-ttu-id="86ec3-120">Aucun</span><span class="sxs-lookup"><span data-stu-id="86ec3-120">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="86ec3-121">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="86ec3-121">Structural Content</span></span>

<span data-ttu-id="86ec3-122">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="86ec3-122">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:DocumentRollCut">
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

## <a name="structure-variables"></a><span data-ttu-id="86ec3-123">Variables de structure</span><span class="sxs-lookup"><span data-stu-id="86ec3-123">Structure Variables</span></span>

<span data-ttu-id="86ec3-124">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="86ec3-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="86ec3-125">Nom</span><span class="sxs-lookup"><span data-stu-id="86ec3-125">Name</span></span>                               | <span data-ttu-id="86ec3-126">Type de données</span><span class="sxs-lookup"><span data-stu-id="86ec3-126">Data type</span></span>         | <span data-ttu-id="86ec3-127">Unité</span><span class="sxs-lookup"><span data-stu-id="86ec3-127">Unit</span></span>                  | <span data-ttu-id="86ec3-128">Valeurs prises en charge</span><span class="sxs-lookup"><span data-stu-id="86ec3-128">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="86ec3-129">Résumé</span><span class="sxs-lookup"><span data-stu-id="86ec3-129">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="86ec3-130">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="86ec3-130">\_OptionName\_</span></span><br/>          | <span data-ttu-id="86ec3-131">string</span><span class="sxs-lookup"><span data-stu-id="86ec3-131">string</span></span><br/> | <span data-ttu-id="86ec3-132">caractères</span><span class="sxs-lookup"><span data-stu-id="86ec3-132">characters</span></span><br/> | <span data-ttu-id="86ec3-133">Nom complet valide tel que défini par les [espaces de noms dans XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="86ec3-133">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="86ec3-134">Si aucun espace de noms n’est spécifié, l’espace de noms par défaut est utilisé.</span><span class="sxs-lookup"><span data-stu-id="86ec3-134">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="86ec3-135">Nom de l'option.</span><span class="sxs-lookup"><span data-stu-id="86ec3-135">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="86ec3-136">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="86ec3-136">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="86ec3-137">string</span><span class="sxs-lookup"><span data-stu-id="86ec3-137">string</span></span><br/> | <span data-ttu-id="86ec3-138">n/a</span><span class="sxs-lookup"><span data-stu-id="86ec3-138">n/a</span></span><br/>        | <span data-ttu-id="86ec3-139">True, False.</span><span class="sxs-lookup"><span data-stu-id="86ec3-139">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="86ec3-140">Définit une option qui, lorsqu’elle est sélectionnée, désactive cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="86ec3-140">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="86ec3-141">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="86ec3-141">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="86ec3-142">Les mots clés de schéma d’impression publics sont définis dans l' https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords espace de noms.</span><span class="sxs-lookup"><span data-stu-id="86ec3-142">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="86ec3-143">Le contenu de la Extensible Markup Language publique (XML) pour ce mot clé est défini ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="86ec3-143">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:DocumentRollCut">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies cutting method for banner -->
  <psf:Option name="psk:Banner" />
  <!-- Specifies cutting at the edge of the image --> 
  <psf:Option name="psk:CutSheetAtImageEdge" />
  <!-- Specifies cutting for media size selected for PageMediaSize -->
  <psf:Option name="psk:CutSheetAtStandardMediaSize" />
  <!-- Specifies no document roll cut -->
  <psf:Option name="psk:None" />
</psf:Feature>
    
```

## <a name="related-topics"></a><span data-ttu-id="86ec3-144">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="86ec3-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="86ec3-145">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="86ec3-145">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




