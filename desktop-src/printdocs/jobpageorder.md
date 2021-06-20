---
description: En savoir plus sur l’élément JobPageOrder, qui définit l’ordre des pages physiques pour la sortie.
ms.assetid: 0c255d50-8b0e-4ecd-876d-eaaccdca7b27
title: JobPageOrder
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa2216330034c458095af7e67ff0904100126451
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408742"
---
# <a name="jobpageorder"></a><span data-ttu-id="9d820-103">JobPageOrder</span><span class="sxs-lookup"><span data-stu-id="9d820-103">JobPageOrder</span></span>

<span data-ttu-id="9d820-104">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="9d820-104">This topic is not current.</span></span> <span data-ttu-id="9d820-105">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="9d820-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="9d820-106">Définit l’ordre des pages physiques pour la sortie.</span><span class="sxs-lookup"><span data-stu-id="9d820-106">Defines the order of physical pages for the output.</span></span>

-   [<span data-ttu-id="9d820-107">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="9d820-107">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="9d820-108">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="9d820-108">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="9d820-109">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="9d820-109">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="9d820-110">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="9d820-110">Element Information</span></span>



| <span data-ttu-id="9d820-111">Nom</span><span class="sxs-lookup"><span data-stu-id="9d820-111">Name</span></span> | <span data-ttu-id="9d820-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="9d820-112">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="9d820-113">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="9d820-113">Element Type</span></span> <br/>   | <span data-ttu-id="9d820-114">Fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="9d820-114">Feature</span></span><br/> |
| <span data-ttu-id="9d820-115">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="9d820-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="9d820-116">Travail</span><span class="sxs-lookup"><span data-stu-id="9d820-116">Job</span></span><br/>     |
| <span data-ttu-id="9d820-117">Notes</span><span class="sxs-lookup"><span data-stu-id="9d820-117">Notes</span></span> <br/>          | <span data-ttu-id="9d820-118">Aucun</span><span class="sxs-lookup"><span data-stu-id="9d820-118">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="9d820-119">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="9d820-119">Structural Content</span></span>

<span data-ttu-id="9d820-120">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="9d820-120">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:JobPageOrder">
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

## <a name="structure-variables"></a><span data-ttu-id="9d820-121">Variables de structure</span><span class="sxs-lookup"><span data-stu-id="9d820-121">Structure Variables</span></span>

<span data-ttu-id="9d820-122">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="9d820-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="9d820-123">Nom</span><span class="sxs-lookup"><span data-stu-id="9d820-123">Name</span></span>                               | <span data-ttu-id="9d820-124">Type de données</span><span class="sxs-lookup"><span data-stu-id="9d820-124">Data type</span></span>         | <span data-ttu-id="9d820-125">Unité</span><span class="sxs-lookup"><span data-stu-id="9d820-125">Unit</span></span>                  | <span data-ttu-id="9d820-126">Valeurs prises en charge</span><span class="sxs-lookup"><span data-stu-id="9d820-126">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="9d820-127">Résumé</span><span class="sxs-lookup"><span data-stu-id="9d820-127">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="9d820-128">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="9d820-128">\_OptionName\_</span></span><br/>          | <span data-ttu-id="9d820-129">string</span><span class="sxs-lookup"><span data-stu-id="9d820-129">string</span></span><br/> | <span data-ttu-id="9d820-130">caractères</span><span class="sxs-lookup"><span data-stu-id="9d820-130">characters</span></span><br/> | <span data-ttu-id="9d820-131">Nom complet valide tel que défini par les [espaces de noms dans XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="9d820-131">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="9d820-132">Si aucun espace de noms n’est spécifié, l’espace de noms par défaut est utilisé.</span><span class="sxs-lookup"><span data-stu-id="9d820-132">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="9d820-133">Nom de l'option.</span><span class="sxs-lookup"><span data-stu-id="9d820-133">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="9d820-134">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="9d820-134">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="9d820-135">string</span><span class="sxs-lookup"><span data-stu-id="9d820-135">string</span></span><br/> | <span data-ttu-id="9d820-136">n/a</span><span class="sxs-lookup"><span data-stu-id="9d820-136">n/a</span></span><br/>        | <span data-ttu-id="9d820-137">True, False.</span><span class="sxs-lookup"><span data-stu-id="9d820-137">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="9d820-138">Définit une option qui, lorsqu’elle est sélectionnée, désactive cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="9d820-138">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="9d820-139">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="9d820-139">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="9d820-140">Les mots clés de schéma d’impression publics sont définis dans l' https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords espace de noms.</span><span class="sxs-lookup"><span data-stu-id="9d820-140">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="9d820-141">Le contenu de la Extensible Markup Language publique (XML) pour ce mot clé est défini ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="9d820-141">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:JobPageOrder">
  <psf:Property name="psf:SelectionType">
   <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies front to back page order. -->
  <psf:Option name="psk:Standard" />
  <!-- Specifies back to front page order. -->
  <psf:Option name="psk:Reverse" />
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="9d820-142">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9d820-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9d820-143">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="9d820-143">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




