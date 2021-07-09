---
description: Obtenir des informations sur l’élément configurable par l’utilisateur PagePoster. Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: 66a3ac9a-674e-4f16-a2d8-8f5b753f876c
title: PagePoster
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72b8bb7b57074fe058c7cc5be8dd609577ceb6c1
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/09/2021
ms.locfileid: "113548967"
---
# <a name="pageposter"></a><span data-ttu-id="c34dd-105">PagePoster</span><span class="sxs-lookup"><span data-stu-id="c34dd-105">PagePoster</span></span>

<span data-ttu-id="c34dd-106">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="c34dd-106">This topic is not current.</span></span> <span data-ttu-id="c34dd-107">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="c34dd-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="c34dd-108">Décrit la sortie d’une page unique à plusieurs feuilles de média physiques.</span><span class="sxs-lookup"><span data-stu-id="c34dd-108">Describes the output of a single page to multiple physical media sheets.</span></span>

-   [<span data-ttu-id="c34dd-109">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="c34dd-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="c34dd-110">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="c34dd-110">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="c34dd-111">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="c34dd-111">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="c34dd-112">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="c34dd-112">Element Information</span></span>



| <span data-ttu-id="c34dd-113">Nom</span><span class="sxs-lookup"><span data-stu-id="c34dd-113">Name</span></span> | <span data-ttu-id="c34dd-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="c34dd-114">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="c34dd-115">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="c34dd-115">Element Type</span></span> <br/>   | <span data-ttu-id="c34dd-116">Composant</span><span class="sxs-lookup"><span data-stu-id="c34dd-116">Feature</span></span><br/> |
| <span data-ttu-id="c34dd-117">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="c34dd-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="c34dd-118">Page</span><span class="sxs-lookup"><span data-stu-id="c34dd-118">Page</span></span><br/>    |
| <span data-ttu-id="c34dd-119">Notes</span><span class="sxs-lookup"><span data-stu-id="c34dd-119">Notes</span></span> <br/>          | <span data-ttu-id="c34dd-120">Aucun</span><span class="sxs-lookup"><span data-stu-id="c34dd-120">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="c34dd-121">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="c34dd-121">Structural Content</span></span>

<span data-ttu-id="c34dd-122">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="c34dd-122">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PagePoster">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <psf:ScoredProperty name="psk:SheetsPerPage">
      <psf:Value xsi:type="xs:integer">_SheetsPerPageValue_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
      
```

## <a name="structure-variables"></a><span data-ttu-id="c34dd-123">Variables de structure</span><span class="sxs-lookup"><span data-stu-id="c34dd-123">Structure Variables</span></span>

<span data-ttu-id="c34dd-124">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="c34dd-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="c34dd-125">Nom</span><span class="sxs-lookup"><span data-stu-id="c34dd-125">Name</span></span>                               | <span data-ttu-id="c34dd-126">Type de données</span><span class="sxs-lookup"><span data-stu-id="c34dd-126">Data type</span></span>          | <span data-ttu-id="c34dd-127">Unité</span><span class="sxs-lookup"><span data-stu-id="c34dd-127">Unit</span></span>                  | <span data-ttu-id="c34dd-128">Valeurs prises en charge</span><span class="sxs-lookup"><span data-stu-id="c34dd-128">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="c34dd-129">Résumé</span><span class="sxs-lookup"><span data-stu-id="c34dd-129">Summary</span></span>                                                                      |
|------------------------------------|--------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="c34dd-130">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="c34dd-130">\_OptionName\_</span></span><br/>          | <span data-ttu-id="c34dd-131">string</span><span class="sxs-lookup"><span data-stu-id="c34dd-131">string</span></span><br/>  | <span data-ttu-id="c34dd-132">caractères</span><span class="sxs-lookup"><span data-stu-id="c34dd-132">characters</span></span><br/> | <span data-ttu-id="c34dd-133">Nom complet valide tel que défini par les [espaces de noms dans XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="c34dd-133">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="c34dd-134">Si aucun espace de noms n’est spécifié, l’espace de noms par défaut est utilisé.</span><span class="sxs-lookup"><span data-stu-id="c34dd-134">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="c34dd-135">Nom de l’option</span><span class="sxs-lookup"><span data-stu-id="c34dd-135">The name of the option</span></span><br/>                                            |
| <span data-ttu-id="c34dd-136">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="c34dd-136">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="c34dd-137">string</span><span class="sxs-lookup"><span data-stu-id="c34dd-137">string</span></span><br/>  | <span data-ttu-id="c34dd-138">n/a</span><span class="sxs-lookup"><span data-stu-id="c34dd-138">n/a</span></span><br/>        | <span data-ttu-id="c34dd-139">True, False</span><span class="sxs-lookup"><span data-stu-id="c34dd-139">True, False</span></span><br/>                                                                                                                                                                | <span data-ttu-id="c34dd-140">Définit une option qui, lorsqu’elle est sélectionnée, désactive cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="c34dd-140">Defines an Option which when selected would disable this feature.</span></span><br/> |
| <span data-ttu-id="c34dd-141">\_SheetsPerPageValue\_</span><span class="sxs-lookup"><span data-stu-id="c34dd-141">\_SheetsPerPageValue\_</span></span><br/>  | <span data-ttu-id="c34dd-142">entier</span><span class="sxs-lookup"><span data-stu-id="c34dd-142">integer</span></span><br/> | <span data-ttu-id="c34dd-143">pages</span><span class="sxs-lookup"><span data-stu-id="c34dd-143">pages</span></span><br/>      | <span data-ttu-id="c34dd-144">Supérieur ou égal à 0.</span><span class="sxs-lookup"><span data-stu-id="c34dd-144">Greater than or equal to 0.</span></span><br/>                                                                                                                                                | <span data-ttu-id="c34dd-145">Spécifie le nombre de feuilles physiques par page logique.</span><span class="sxs-lookup"><span data-stu-id="c34dd-145">Specifies the number of physical sheets per logical page.</span></span><br/>         |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="c34dd-146">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="c34dd-146">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="c34dd-147">Les mots clés de schéma d’impression publics sont définis dans l' https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords espace de noms.</span><span class="sxs-lookup"><span data-stu-id="c34dd-147">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="c34dd-148">Le contenu de la Extensible Markup Language publique (XML) pour ce mot clé est défini ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="c34dd-148">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PagePoster">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies media sheets per page. -->
  <psf:Option>
    <psf:ScoredProperty name="psk:SheetsPerPage">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="c34dd-149">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c34dd-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c34dd-150">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="c34dd-150">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




