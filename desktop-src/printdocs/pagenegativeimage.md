---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: 4f6ff85c-8cad-4b9b-8a1d-ce41ed7dfbed
title: PageNegativeImage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8882c1a5aa026d06b43055a6a74a58c266ea009
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994493"
---
# <a name="pagenegativeimage"></a><span data-ttu-id="7ed99-104">PageNegativeImage</span><span class="sxs-lookup"><span data-stu-id="7ed99-104">PageNegativeImage</span></span>

<span data-ttu-id="7ed99-105">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="7ed99-105">This topic is not current.</span></span> <span data-ttu-id="7ed99-106">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="7ed99-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="7ed99-107">Décrit le paramètre négatif de la sortie.</span><span class="sxs-lookup"><span data-stu-id="7ed99-107">Describes the negative setting of the output.</span></span>

-   [<span data-ttu-id="7ed99-108">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="7ed99-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="7ed99-109">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="7ed99-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="7ed99-110">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="7ed99-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="7ed99-111">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="7ed99-111">Element Information</span></span>



| <span data-ttu-id="7ed99-112">Nom</span><span class="sxs-lookup"><span data-stu-id="7ed99-112">Name</span></span> | <span data-ttu-id="7ed99-113">Value</span><span class="sxs-lookup"><span data-stu-id="7ed99-113">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="7ed99-114">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="7ed99-114">Element Type</span></span> <br/>   | <span data-ttu-id="7ed99-115">Fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="7ed99-115">Feature</span></span><br/> |
| <span data-ttu-id="7ed99-116">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="7ed99-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="7ed99-117">Page</span><span class="sxs-lookup"><span data-stu-id="7ed99-117">Page</span></span><br/>    |
| <span data-ttu-id="7ed99-118">Notes</span><span class="sxs-lookup"><span data-stu-id="7ed99-118">Notes</span></span> <br/>          | <span data-ttu-id="7ed99-119">Aucun</span><span class="sxs-lookup"><span data-stu-id="7ed99-119">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="7ed99-120">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="7ed99-120">Structural Content</span></span>

<span data-ttu-id="7ed99-121">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="7ed99-121">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="7ed99-122">Variables de structure</span><span class="sxs-lookup"><span data-stu-id="7ed99-122">Structure Variables</span></span>

<span data-ttu-id="7ed99-123">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="7ed99-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="7ed99-124">Nom</span><span class="sxs-lookup"><span data-stu-id="7ed99-124">Name</span></span>                               | <span data-ttu-id="7ed99-125">Type de données</span><span class="sxs-lookup"><span data-stu-id="7ed99-125">Data type</span></span>         | <span data-ttu-id="7ed99-126">Unité</span><span class="sxs-lookup"><span data-stu-id="7ed99-126">Unit</span></span>                  | <span data-ttu-id="7ed99-127">Valeurs prises en charge</span><span class="sxs-lookup"><span data-stu-id="7ed99-127">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="7ed99-128">Résumé</span><span class="sxs-lookup"><span data-stu-id="7ed99-128">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="7ed99-129">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="7ed99-129">\_OptionName\_</span></span><br/>          | <span data-ttu-id="7ed99-130">string</span><span class="sxs-lookup"><span data-stu-id="7ed99-130">string</span></span><br/> | <span data-ttu-id="7ed99-131">caractères</span><span class="sxs-lookup"><span data-stu-id="7ed99-131">characters</span></span><br/> | <span data-ttu-id="7ed99-132">Nom complet valide tel que défini par les [espaces de noms dans XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="7ed99-132">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="7ed99-133">Si aucun espace de noms n’est spécifié, l’espace de noms par défaut est utilisé.</span><span class="sxs-lookup"><span data-stu-id="7ed99-133">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="7ed99-134">Nom de l'option.</span><span class="sxs-lookup"><span data-stu-id="7ed99-134">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="7ed99-135">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="7ed99-135">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="7ed99-136">string</span><span class="sxs-lookup"><span data-stu-id="7ed99-136">string</span></span><br/> | <span data-ttu-id="7ed99-137">n/a</span><span class="sxs-lookup"><span data-stu-id="7ed99-137">n/a</span></span><br/>        | <span data-ttu-id="7ed99-138">True, False.</span><span class="sxs-lookup"><span data-stu-id="7ed99-138">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="7ed99-139">Définit une option qui, lorsqu’elle est sélectionnée, désactive cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="7ed99-139">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="7ed99-140">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="7ed99-140">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="7ed99-141">Les mots clés de schéma d’impression publics sont définis dans l' https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords espace de noms.</span><span class="sxs-lookup"><span data-stu-id="7ed99-141">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="7ed99-142">Le contenu de la Extensible Markup Language publique (XML) pour ce mot clé est défini ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="7ed99-142">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="7ed99-143">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7ed99-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7ed99-144">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="7ed99-144">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




