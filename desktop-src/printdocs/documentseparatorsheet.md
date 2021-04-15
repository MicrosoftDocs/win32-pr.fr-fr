---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: f0b2192d-4bb7-4ba2-8dd0-35a20183ea31
title: DocumentSeparatorSheet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8722e5db4f1a3bfebe8895c8a0777a849a88f11e
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "104321770"
---
# <a name="documentseparatorsheet"></a><span data-ttu-id="e2a5c-104">DocumentSeparatorSheet</span><span class="sxs-lookup"><span data-stu-id="e2a5c-104">DocumentSeparatorSheet</span></span>

<span data-ttu-id="e2a5c-105">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="e2a5c-105">This topic is not current.</span></span> <span data-ttu-id="e2a5c-106">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="e2a5c-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="e2a5c-107">Décrit l’utilisation de la feuille de séparation pour un document.</span><span class="sxs-lookup"><span data-stu-id="e2a5c-107">Describes the separator sheet usage for a document.</span></span> <span data-ttu-id="e2a5c-108">Les feuilles de séparation doivent apparaître dans la sortie, comme indiqué par l’option spécifiée ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="e2a5c-108">Separator sheets should appear in the output as indicated by the Option specified below.</span></span>

-   [<span data-ttu-id="e2a5c-109">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="e2a5c-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="e2a5c-110">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="e2a5c-110">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="e2a5c-111">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="e2a5c-111">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="e2a5c-112">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="e2a5c-112">Element Information</span></span>



| <span data-ttu-id="e2a5c-113">Nom</span><span class="sxs-lookup"><span data-stu-id="e2a5c-113">Name</span></span>                       |                     |
|----------------------------|---------------------|
| <span data-ttu-id="e2a5c-114">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="e2a5c-114">Element Type</span></span> <br/>   | <span data-ttu-id="e2a5c-115">Fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="e2a5c-115">Feature</span></span><br/>  |
| <span data-ttu-id="e2a5c-116">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="e2a5c-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="e2a5c-117">Document</span><span class="sxs-lookup"><span data-stu-id="e2a5c-117">Document</span></span><br/> |
| <span data-ttu-id="e2a5c-118">Notes</span><span class="sxs-lookup"><span data-stu-id="e2a5c-118">Notes</span></span> <br/>          | <span data-ttu-id="e2a5c-119">Aucun</span><span class="sxs-lookup"><span data-stu-id="e2a5c-119">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="e2a5c-120">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="e2a5c-120">Structural Content</span></span>

<span data-ttu-id="e2a5c-121">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="e2a5c-121">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:DocumentSeparatorSheet">
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

## <a name="structure-variables"></a><span data-ttu-id="e2a5c-122">Variables de structure</span><span class="sxs-lookup"><span data-stu-id="e2a5c-122">Structure Variables</span></span>

<span data-ttu-id="e2a5c-123">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="e2a5c-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="e2a5c-124">Nom</span><span class="sxs-lookup"><span data-stu-id="e2a5c-124">Name</span></span>                               | <span data-ttu-id="e2a5c-125">Type de données</span><span class="sxs-lookup"><span data-stu-id="e2a5c-125">Data type</span></span>         | <span data-ttu-id="e2a5c-126">Unité</span><span class="sxs-lookup"><span data-stu-id="e2a5c-126">Unit</span></span>                  | <span data-ttu-id="e2a5c-127">Valeurs prises en charge</span><span class="sxs-lookup"><span data-stu-id="e2a5c-127">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="e2a5c-128">Résumé</span><span class="sxs-lookup"><span data-stu-id="e2a5c-128">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="e2a5c-129">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="e2a5c-129">\_OptionName\_</span></span><br/>          | <span data-ttu-id="e2a5c-130">string</span><span class="sxs-lookup"><span data-stu-id="e2a5c-130">string</span></span><br/> | <span data-ttu-id="e2a5c-131">caractères</span><span class="sxs-lookup"><span data-stu-id="e2a5c-131">characters</span></span><br/> | <span data-ttu-id="e2a5c-132">Nom complet valide tel que défini par les [espaces de noms dans XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="e2a5c-132">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="e2a5c-133">Si aucun espace de noms n’est spécifié, l’espace de noms par défaut est utilisé.</span><span class="sxs-lookup"><span data-stu-id="e2a5c-133">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="e2a5c-134">Nom de l'option.</span><span class="sxs-lookup"><span data-stu-id="e2a5c-134">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="e2a5c-135">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="e2a5c-135">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="e2a5c-136">string</span><span class="sxs-lookup"><span data-stu-id="e2a5c-136">string</span></span><br/> | <span data-ttu-id="e2a5c-137">n/a</span><span class="sxs-lookup"><span data-stu-id="e2a5c-137">n/a</span></span><br/>        | <span data-ttu-id="e2a5c-138">True, False.</span><span class="sxs-lookup"><span data-stu-id="e2a5c-138">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="e2a5c-139">Définit une option qui, lorsqu’elle est sélectionnée, désactive cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="e2a5c-139">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="e2a5c-140">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="e2a5c-140">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="e2a5c-141">Les mots clés de schéma d’impression publics sont définis dans l' https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords espace de noms.</span><span class="sxs-lookup"><span data-stu-id="e2a5c-141">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="e2a5c-142">Le contenu de la Extensible Markup Language publique (XML) pour ce mot clé est défini ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="e2a5c-142">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:DocumentSeparatorSheet">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies a separator sheet at the start and end of the document. -->
  <psf:Option name="psk:BothSheets" />
  <!-- Specifies a separator sheet at the end of the document. -->
  <psf:Option name="psk:EndSheet" />
  <!-- Specifies no separator sheet(s). -->
  <psf:Option name="psk:None" />
  <!-- Specifies a separator sheet at the start of the document. -->
  <psf:Option name="psk:StartSheet" />
</psf:Feature>
    
```

## <a name="related-topics"></a><span data-ttu-id="e2a5c-143">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e2a5c-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e2a5c-144">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="e2a5c-144">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




