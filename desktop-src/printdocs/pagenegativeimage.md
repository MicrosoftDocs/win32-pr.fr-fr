---
description: En savoir plus sur l’élément configurable par l’utilisateur PageNegativeImage. Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: 4f6ff85c-8cad-4b9b-8a1d-ce41ed7dfbed
title: PageNegativeImage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a1e1a9de2d82135adb82c68f45785ee3763e41a
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395654"
---
# <a name="pagenegativeimage"></a><span data-ttu-id="f45b9-105">PageNegativeImage</span><span class="sxs-lookup"><span data-stu-id="f45b9-105">PageNegativeImage</span></span>

<span data-ttu-id="f45b9-106">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="f45b9-106">This topic is not current.</span></span> <span data-ttu-id="f45b9-107">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="f45b9-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="f45b9-108">Décrit le paramètre négatif de la sortie.</span><span class="sxs-lookup"><span data-stu-id="f45b9-108">Describes the negative setting of the output.</span></span>

-   [<span data-ttu-id="f45b9-109">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="f45b9-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="f45b9-110">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="f45b9-110">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="f45b9-111">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="f45b9-111">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="f45b9-112">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="f45b9-112">Element Information</span></span>



| <span data-ttu-id="f45b9-113">Nom</span><span class="sxs-lookup"><span data-stu-id="f45b9-113">Name</span></span> | <span data-ttu-id="f45b9-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="f45b9-114">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="f45b9-115">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="f45b9-115">Element Type</span></span> <br/>   | <span data-ttu-id="f45b9-116">Fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="f45b9-116">Feature</span></span><br/> |
| <span data-ttu-id="f45b9-117">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="f45b9-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="f45b9-118">Page</span><span class="sxs-lookup"><span data-stu-id="f45b9-118">Page</span></span><br/>    |
| <span data-ttu-id="f45b9-119">Notes</span><span class="sxs-lookup"><span data-stu-id="f45b9-119">Notes</span></span> <br/>          | <span data-ttu-id="f45b9-120">Aucun</span><span class="sxs-lookup"><span data-stu-id="f45b9-120">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="f45b9-121">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="f45b9-121">Structural Content</span></span>

<span data-ttu-id="f45b9-122">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="f45b9-122">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageNegativeImage">
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

## <a name="structure-variables"></a><span data-ttu-id="f45b9-123">Variables de structure</span><span class="sxs-lookup"><span data-stu-id="f45b9-123">Structure Variables</span></span>

<span data-ttu-id="f45b9-124">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="f45b9-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="f45b9-125">Nom</span><span class="sxs-lookup"><span data-stu-id="f45b9-125">Name</span></span>                               | <span data-ttu-id="f45b9-126">Type de données</span><span class="sxs-lookup"><span data-stu-id="f45b9-126">Data type</span></span>         | <span data-ttu-id="f45b9-127">Unité</span><span class="sxs-lookup"><span data-stu-id="f45b9-127">Unit</span></span>                  | <span data-ttu-id="f45b9-128">Valeurs prises en charge</span><span class="sxs-lookup"><span data-stu-id="f45b9-128">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="f45b9-129">Résumé</span><span class="sxs-lookup"><span data-stu-id="f45b9-129">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="f45b9-130">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="f45b9-130">\_OptionName\_</span></span><br/>          | <span data-ttu-id="f45b9-131">string</span><span class="sxs-lookup"><span data-stu-id="f45b9-131">string</span></span><br/> | <span data-ttu-id="f45b9-132">caractères</span><span class="sxs-lookup"><span data-stu-id="f45b9-132">characters</span></span><br/> | <span data-ttu-id="f45b9-133">Nom complet valide tel que défini par les [espaces de noms dans XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="f45b9-133">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="f45b9-134">Si aucun espace de noms n’est spécifié, l’espace de noms par défaut est utilisé.</span><span class="sxs-lookup"><span data-stu-id="f45b9-134">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="f45b9-135">Nom de l'option.</span><span class="sxs-lookup"><span data-stu-id="f45b9-135">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="f45b9-136">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="f45b9-136">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="f45b9-137">string</span><span class="sxs-lookup"><span data-stu-id="f45b9-137">string</span></span><br/> | <span data-ttu-id="f45b9-138">n/a</span><span class="sxs-lookup"><span data-stu-id="f45b9-138">n/a</span></span><br/>        | <span data-ttu-id="f45b9-139">True, False.</span><span class="sxs-lookup"><span data-stu-id="f45b9-139">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="f45b9-140">Définit une option qui, lorsqu’elle est sélectionnée, désactive cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="f45b9-140">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="f45b9-141">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="f45b9-141">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="f45b9-142">Les mots clés de schéma d’impression publics sont définis dans l' https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords espace de noms.</span><span class="sxs-lookup"><span data-stu-id="f45b9-142">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="f45b9-143">Le contenu de la Extensible Markup Language publique (XML) pour ce mot clé est défini ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="f45b9-143">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageNegativeImage">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies the output should be the negative image. -->
  <psf:Option name="psk:Negative" />
  <!-- Specifies the output should be the non-negative image. -->
  <psf:Option name="psk:None" />
</psf:Feature>
    
```

## <a name="related-topics"></a><span data-ttu-id="f45b9-144">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f45b9-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f45b9-145">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="f45b9-145">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




