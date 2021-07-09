---
description: En savoir plus sur l’élément configurable par l’utilisateur PageBorderless. Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: c5e75f57-7426-41fa-88f4-789153fcd0c5
title: PageBorderless
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66a0ff13edc1f4e5b36f55229559bb06ed17150b
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/09/2021
ms.locfileid: "113549307"
---
# <a name="pageborderless"></a><span data-ttu-id="a3a69-105">PageBorderless</span><span class="sxs-lookup"><span data-stu-id="a3a69-105">PageBorderless</span></span>

<span data-ttu-id="a3a69-106">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="a3a69-106">This topic is not current.</span></span> <span data-ttu-id="a3a69-107">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="a3a69-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="a3a69-108">Décrit le moment où le contenu de l’image doit être imprimé sur les bords physiques du média.</span><span class="sxs-lookup"><span data-stu-id="a3a69-108">Describes when image content should be printed to the physical edges of the media.</span></span>

-   [<span data-ttu-id="a3a69-109">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="a3a69-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="a3a69-110">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="a3a69-110">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="a3a69-111">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="a3a69-111">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="a3a69-112">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="a3a69-112">Element Information</span></span>



| <span data-ttu-id="a3a69-113">Nom</span><span class="sxs-lookup"><span data-stu-id="a3a69-113">Name</span></span> | <span data-ttu-id="a3a69-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="a3a69-114">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="a3a69-115">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="a3a69-115">Element Type</span></span> <br/>   | <span data-ttu-id="a3a69-116">Composant</span><span class="sxs-lookup"><span data-stu-id="a3a69-116">Feature</span></span><br/> |
| <span data-ttu-id="a3a69-117">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="a3a69-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="a3a69-118">Page</span><span class="sxs-lookup"><span data-stu-id="a3a69-118">Page</span></span><br/>    |
| <span data-ttu-id="a3a69-119">Notes</span><span class="sxs-lookup"><span data-stu-id="a3a69-119">Notes</span></span> <br/>          | <span data-ttu-id="a3a69-120">Aucun</span><span class="sxs-lookup"><span data-stu-id="a3a69-120">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="a3a69-121">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="a3a69-121">Structural Content</span></span>

<span data-ttu-id="a3a69-122">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="a3a69-122">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageBorderless">
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

## <a name="structure-variables"></a><span data-ttu-id="a3a69-123">Variables de structure</span><span class="sxs-lookup"><span data-stu-id="a3a69-123">Structure Variables</span></span>

<span data-ttu-id="a3a69-124">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="a3a69-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="a3a69-125">Nom</span><span class="sxs-lookup"><span data-stu-id="a3a69-125">Name</span></span>                               | <span data-ttu-id="a3a69-126">Type de données</span><span class="sxs-lookup"><span data-stu-id="a3a69-126">Data type</span></span>         | <span data-ttu-id="a3a69-127">Unité</span><span class="sxs-lookup"><span data-stu-id="a3a69-127">Unit</span></span>                  | <span data-ttu-id="a3a69-128">Valeurs prises en charge</span><span class="sxs-lookup"><span data-stu-id="a3a69-128">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="a3a69-129">Résumé</span><span class="sxs-lookup"><span data-stu-id="a3a69-129">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="a3a69-130">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="a3a69-130">\_OptionName\_</span></span><br/>          | <span data-ttu-id="a3a69-131">string</span><span class="sxs-lookup"><span data-stu-id="a3a69-131">string</span></span><br/> | <span data-ttu-id="a3a69-132">caractères</span><span class="sxs-lookup"><span data-stu-id="a3a69-132">characters</span></span><br/> | <span data-ttu-id="a3a69-133">Nom complet valide tel que défini par les [espaces de noms dans XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="a3a69-133">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="a3a69-134">Si aucun espace de noms n’est spécifié, l’espace de noms par défaut est utilisé.</span><span class="sxs-lookup"><span data-stu-id="a3a69-134">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="a3a69-135">Nom de l'option.</span><span class="sxs-lookup"><span data-stu-id="a3a69-135">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="a3a69-136">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="a3a69-136">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="a3a69-137">string</span><span class="sxs-lookup"><span data-stu-id="a3a69-137">string</span></span><br/> | <span data-ttu-id="a3a69-138">n/a</span><span class="sxs-lookup"><span data-stu-id="a3a69-138">n/a</span></span><br/>        | <span data-ttu-id="a3a69-139">True, False.</span><span class="sxs-lookup"><span data-stu-id="a3a69-139">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="a3a69-140">Définit une option qui, lorsqu’elle est sélectionnée, désactive cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="a3a69-140">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="a3a69-141">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="a3a69-141">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="a3a69-142">Les mots clés de schéma d’impression publics sont définis dans l' https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords espace de noms.</span><span class="sxs-lookup"><span data-stu-id="a3a69-142">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="a3a69-143">Le contenu de la Extensible Markup Language publique (XML) pour ce mot clé est défini ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="a3a69-143">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageBorderless">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies borderless printing. -->
  <psf:Option name="psk:Borderless" />
  <!-- Specifies no borderless printing. -->
  <psf:Option name="psk:None" />
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="a3a69-144">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a3a69-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a3a69-145">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="a3a69-145">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




