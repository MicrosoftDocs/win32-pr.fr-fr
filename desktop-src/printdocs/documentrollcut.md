---
description: En savoir plus sur l’élément DocumentRollCut, qui décrit la méthode de coupe pour le papier en rouleau. Chaque document est géré séparément.
ms.assetid: 8eb4e574-3209-459c-9a25-95377b2f7439
title: DocumentRollCut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92f7232cbe9dafce25aa2ee482ca40bf99145841
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409182"
---
# <a name="documentrollcut"></a><span data-ttu-id="700c9-104">DocumentRollCut</span><span class="sxs-lookup"><span data-stu-id="700c9-104">DocumentRollCut</span></span>

<span data-ttu-id="700c9-105">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="700c9-105">This topic is not current.</span></span> <span data-ttu-id="700c9-106">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="700c9-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="700c9-107">Décrit la méthode de coupe pour le papier en rouleau.</span><span class="sxs-lookup"><span data-stu-id="700c9-107">Describes the cutting method for roll paper.</span></span> <span data-ttu-id="700c9-108">Chaque document est géré séparément.</span><span class="sxs-lookup"><span data-stu-id="700c9-108">Each document is handled separately.</span></span> <span data-ttu-id="700c9-109">Les options spécifiées décrivent les différentes méthodes de coupe des rouleaux.</span><span class="sxs-lookup"><span data-stu-id="700c9-109">The specified options describe the different methods for roll cut.</span></span>

-   [<span data-ttu-id="700c9-110">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="700c9-110">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="700c9-111">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="700c9-111">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="700c9-112">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="700c9-112">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="700c9-113">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="700c9-113">Element Information</span></span>



| <span data-ttu-id="700c9-114">Nom</span><span class="sxs-lookup"><span data-stu-id="700c9-114">Name</span></span> | <span data-ttu-id="700c9-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="700c9-115">Value</span></span> |
|----------------------------|---------------------|
| <span data-ttu-id="700c9-116">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="700c9-116">Element Type</span></span> <br/>   | <span data-ttu-id="700c9-117">Fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="700c9-117">Feature</span></span><br/>  |
| <span data-ttu-id="700c9-118">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="700c9-118">Scoping Prefix</span></span> <br/> | <span data-ttu-id="700c9-119">Document</span><span class="sxs-lookup"><span data-stu-id="700c9-119">Document</span></span><br/> |
| <span data-ttu-id="700c9-120">Notes</span><span class="sxs-lookup"><span data-stu-id="700c9-120">Notes</span></span> <br/>          | <span data-ttu-id="700c9-121">Aucun</span><span class="sxs-lookup"><span data-stu-id="700c9-121">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="700c9-122">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="700c9-122">Structural Content</span></span>

<span data-ttu-id="700c9-123">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="700c9-123">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="700c9-124">Variables de structure</span><span class="sxs-lookup"><span data-stu-id="700c9-124">Structure Variables</span></span>

<span data-ttu-id="700c9-125">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="700c9-125">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="700c9-126">Nom</span><span class="sxs-lookup"><span data-stu-id="700c9-126">Name</span></span>                               | <span data-ttu-id="700c9-127">Type de données</span><span class="sxs-lookup"><span data-stu-id="700c9-127">Data type</span></span>         | <span data-ttu-id="700c9-128">Unité</span><span class="sxs-lookup"><span data-stu-id="700c9-128">Unit</span></span>                  | <span data-ttu-id="700c9-129">Valeurs prises en charge</span><span class="sxs-lookup"><span data-stu-id="700c9-129">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="700c9-130">Résumé</span><span class="sxs-lookup"><span data-stu-id="700c9-130">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="700c9-131">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="700c9-131">\_OptionName\_</span></span><br/>          | <span data-ttu-id="700c9-132">string</span><span class="sxs-lookup"><span data-stu-id="700c9-132">string</span></span><br/> | <span data-ttu-id="700c9-133">caractères</span><span class="sxs-lookup"><span data-stu-id="700c9-133">characters</span></span><br/> | <span data-ttu-id="700c9-134">Nom complet valide tel que défini par les [espaces de noms dans XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="700c9-134">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="700c9-135">Si aucun espace de noms n’est spécifié, l’espace de noms par défaut est utilisé.</span><span class="sxs-lookup"><span data-stu-id="700c9-135">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="700c9-136">Nom de l'option.</span><span class="sxs-lookup"><span data-stu-id="700c9-136">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="700c9-137">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="700c9-137">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="700c9-138">string</span><span class="sxs-lookup"><span data-stu-id="700c9-138">string</span></span><br/> | <span data-ttu-id="700c9-139">n/a</span><span class="sxs-lookup"><span data-stu-id="700c9-139">n/a</span></span><br/>        | <span data-ttu-id="700c9-140">True, False.</span><span class="sxs-lookup"><span data-stu-id="700c9-140">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="700c9-141">Définit une option qui, lorsqu’elle est sélectionnée, désactive cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="700c9-141">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="700c9-142">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="700c9-142">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="700c9-143">Les mots clés de schéma d’impression publics sont définis dans l' https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords espace de noms.</span><span class="sxs-lookup"><span data-stu-id="700c9-143">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="700c9-144">Le contenu de la Extensible Markup Language publique (XML) pour ce mot clé est défini ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="700c9-144">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="700c9-145">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="700c9-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="700c9-146">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="700c9-146">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




