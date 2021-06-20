---
description: En savoir plus sur l’élément JobAccountingSheet, qui décrit la feuille de comptabilité à générer pour le travail.
ms.assetid: fd16bd46-32e3-4896-ac5c-03c1bf6ad515
title: JobAccountingSheet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 499d78db7a967e256ee79cd6e0c35d2f7d59dff4
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409093"
---
# <a name="jobaccountingsheet"></a><span data-ttu-id="94113-103">JobAccountingSheet</span><span class="sxs-lookup"><span data-stu-id="94113-103">JobAccountingSheet</span></span>

<span data-ttu-id="94113-104">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="94113-104">This topic is not current.</span></span> <span data-ttu-id="94113-105">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="94113-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="94113-106">Décrit le tableau de comptabilité à générer pour le travail.</span><span class="sxs-lookup"><span data-stu-id="94113-106">Describes the accounting sheet to be output for the job.</span></span> <span data-ttu-id="94113-107">La feuille de gestion doit être sortie sur le PageMediaSize par défaut et utiliser le PageMediaType par défaut.</span><span class="sxs-lookup"><span data-stu-id="94113-107">The accounting sheet should be output on the default PageMediaSize and using the default PageMediaType.</span></span> <span data-ttu-id="94113-108">Le tableau comptable doit être isolé du reste du travail.</span><span class="sxs-lookup"><span data-stu-id="94113-108">The accounting sheet should to be isolated from the remainder of the job.</span></span> <span data-ttu-id="94113-109">Cela signifie que les options de finition ou de traitement (telles que JobDuplex, JobStaple ou JobBinding) ne doivent pas inclure la feuille de comptabilité.</span><span class="sxs-lookup"><span data-stu-id="94113-109">This means that any finishing or processing options (such as JobDuplex, JobStaple, or JobBinding) should not include the accounting sheet.</span></span> <span data-ttu-id="94113-110">La feuille de comptabilité peut se présenter comme la première ou la dernière page du travail à la discrétion du responsable de l’implémentation.</span><span class="sxs-lookup"><span data-stu-id="94113-110">The accounting sheet may occur as the first or last page of the job at the implementer's discretion.</span></span>

-   [<span data-ttu-id="94113-111">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="94113-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="94113-112">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="94113-112">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="94113-113">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="94113-113">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="94113-114">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="94113-114">Element Information</span></span>



| <span data-ttu-id="94113-115">Nom</span><span class="sxs-lookup"><span data-stu-id="94113-115">Name</span></span> | <span data-ttu-id="94113-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="94113-116">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="94113-117">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="94113-117">Element Type</span></span> <br/>   | <span data-ttu-id="94113-118">Fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="94113-118">Feature</span></span><br/> |
| <span data-ttu-id="94113-119">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="94113-119">Scoping Prefix</span></span> <br/> | <span data-ttu-id="94113-120">Travail</span><span class="sxs-lookup"><span data-stu-id="94113-120">Job</span></span><br/>     |
| <span data-ttu-id="94113-121">Notes</span><span class="sxs-lookup"><span data-stu-id="94113-121">Notes</span></span> <br/>          | <span data-ttu-id="94113-122">Aucun</span><span class="sxs-lookup"><span data-stu-id="94113-122">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="94113-123">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="94113-123">Structural Content</span></span>

<span data-ttu-id="94113-124">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="94113-124">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:JobAccountingSheet">
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

## <a name="structure-variables"></a><span data-ttu-id="94113-125">Variables de structure</span><span class="sxs-lookup"><span data-stu-id="94113-125">Structure Variables</span></span>

<span data-ttu-id="94113-126">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="94113-126">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="94113-127">Nom</span><span class="sxs-lookup"><span data-stu-id="94113-127">Name</span></span>                               | <span data-ttu-id="94113-128">Type de données</span><span class="sxs-lookup"><span data-stu-id="94113-128">Data type</span></span>         | <span data-ttu-id="94113-129">Unité</span><span class="sxs-lookup"><span data-stu-id="94113-129">Unit</span></span>                  | <span data-ttu-id="94113-130">Valeurs prises en charge</span><span class="sxs-lookup"><span data-stu-id="94113-130">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="94113-131">Résumé</span><span class="sxs-lookup"><span data-stu-id="94113-131">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="94113-132">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="94113-132">\_OptionName\_</span></span><br/>          | <span data-ttu-id="94113-133">string</span><span class="sxs-lookup"><span data-stu-id="94113-133">string</span></span><br/> | <span data-ttu-id="94113-134">caractères</span><span class="sxs-lookup"><span data-stu-id="94113-134">characters</span></span><br/> | <span data-ttu-id="94113-135">Nom complet valide tel que défini par les [espaces de noms dans XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="94113-135">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="94113-136">Si aucun espace de noms n’est spécifié, l’espace de noms par défaut est utilisé.</span><span class="sxs-lookup"><span data-stu-id="94113-136">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="94113-137">Nom de l'option.</span><span class="sxs-lookup"><span data-stu-id="94113-137">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="94113-138">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="94113-138">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="94113-139">string</span><span class="sxs-lookup"><span data-stu-id="94113-139">string</span></span><br/> | <span data-ttu-id="94113-140">n/a</span><span class="sxs-lookup"><span data-stu-id="94113-140">n/a</span></span><br/>        | <span data-ttu-id="94113-141">True, False.</span><span class="sxs-lookup"><span data-stu-id="94113-141">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="94113-142">Définit une option qui, lorsqu’elle est sélectionnée, désactive cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="94113-142">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="94113-143">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="94113-143">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="94113-144">Les mots clés de schéma d’impression publics sont définis dans l' https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords espace de noms.</span><span class="sxs-lookup"><span data-stu-id="94113-144">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="94113-145">Le contenu de la Extensible Markup Language publique (XML) pour ce mot clé est défini ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="94113-145">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:JobAccountingSheet">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies no accounting sheet will be output. -->
  <psf:Option name="psk:None" />
  <!-- Specifies the standard (device defined) accounting sheet should be output. -->
  <psf:Option name="psk:Standard" />
</psf:Feature>
        
```

## <a name="related-topics"></a><span data-ttu-id="94113-146">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="94113-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="94113-147">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="94113-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




