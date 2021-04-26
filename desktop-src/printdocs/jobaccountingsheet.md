---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: fd16bd46-32e3-4896-ac5c-03c1bf6ad515
title: JobAccountingSheet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30ffb70ba0ac1a78eefc1024d8e93dc642439aed
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998426"
---
# <a name="jobaccountingsheet"></a><span data-ttu-id="02efb-104">JobAccountingSheet</span><span class="sxs-lookup"><span data-stu-id="02efb-104">JobAccountingSheet</span></span>

<span data-ttu-id="02efb-105">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="02efb-105">This topic is not current.</span></span> <span data-ttu-id="02efb-106">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="02efb-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="02efb-107">Décrit le tableau de comptabilité à générer pour le travail.</span><span class="sxs-lookup"><span data-stu-id="02efb-107">Describes the accounting sheet to be output for the job.</span></span> <span data-ttu-id="02efb-108">La feuille de gestion doit être sortie sur le PageMediaSize par défaut et utiliser le PageMediaType par défaut.</span><span class="sxs-lookup"><span data-stu-id="02efb-108">The accounting sheet should be output on the default PageMediaSize and using the default PageMediaType.</span></span> <span data-ttu-id="02efb-109">Le tableau comptable doit être isolé du reste du travail.</span><span class="sxs-lookup"><span data-stu-id="02efb-109">The accounting sheet should to be isolated from the remainder of the job.</span></span> <span data-ttu-id="02efb-110">Cela signifie que les options de finition ou de traitement (telles que JobDuplex, JobStaple ou JobBinding) ne doivent pas inclure la feuille de comptabilité.</span><span class="sxs-lookup"><span data-stu-id="02efb-110">This means that any finishing or processing options (such as JobDuplex, JobStaple, or JobBinding) should not include the accounting sheet.</span></span> <span data-ttu-id="02efb-111">La feuille de comptabilité peut se présenter comme la première ou la dernière page du travail à la discrétion du responsable de l’implémentation.</span><span class="sxs-lookup"><span data-stu-id="02efb-111">The accounting sheet may occur as the first or last page of the job at the implementer's discretion.</span></span>

-   [<span data-ttu-id="02efb-112">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="02efb-112">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="02efb-113">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="02efb-113">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="02efb-114">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="02efb-114">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="02efb-115">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="02efb-115">Element Information</span></span>



| <span data-ttu-id="02efb-116">Nom</span><span class="sxs-lookup"><span data-stu-id="02efb-116">Name</span></span> | <span data-ttu-id="02efb-117">Value</span><span class="sxs-lookup"><span data-stu-id="02efb-117">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="02efb-118">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="02efb-118">Element Type</span></span> <br/>   | <span data-ttu-id="02efb-119">Fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="02efb-119">Feature</span></span><br/> |
| <span data-ttu-id="02efb-120">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="02efb-120">Scoping Prefix</span></span> <br/> | <span data-ttu-id="02efb-121">Travail</span><span class="sxs-lookup"><span data-stu-id="02efb-121">Job</span></span><br/>     |
| <span data-ttu-id="02efb-122">Notes</span><span class="sxs-lookup"><span data-stu-id="02efb-122">Notes</span></span> <br/>          | <span data-ttu-id="02efb-123">Aucun</span><span class="sxs-lookup"><span data-stu-id="02efb-123">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="02efb-124">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="02efb-124">Structural Content</span></span>

<span data-ttu-id="02efb-125">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="02efb-125">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="02efb-126">Variables de structure</span><span class="sxs-lookup"><span data-stu-id="02efb-126">Structure Variables</span></span>

<span data-ttu-id="02efb-127">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="02efb-127">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="02efb-128">Nom</span><span class="sxs-lookup"><span data-stu-id="02efb-128">Name</span></span>                               | <span data-ttu-id="02efb-129">Type de données</span><span class="sxs-lookup"><span data-stu-id="02efb-129">Data type</span></span>         | <span data-ttu-id="02efb-130">Unité</span><span class="sxs-lookup"><span data-stu-id="02efb-130">Unit</span></span>                  | <span data-ttu-id="02efb-131">Valeurs prises en charge</span><span class="sxs-lookup"><span data-stu-id="02efb-131">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="02efb-132">Résumé</span><span class="sxs-lookup"><span data-stu-id="02efb-132">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="02efb-133">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="02efb-133">\_OptionName\_</span></span><br/>          | <span data-ttu-id="02efb-134">string</span><span class="sxs-lookup"><span data-stu-id="02efb-134">string</span></span><br/> | <span data-ttu-id="02efb-135">caractères</span><span class="sxs-lookup"><span data-stu-id="02efb-135">characters</span></span><br/> | <span data-ttu-id="02efb-136">Nom complet valide tel que défini par les [espaces de noms dans XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="02efb-136">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="02efb-137">Si aucun espace de noms n’est spécifié, l’espace de noms par défaut est utilisé.</span><span class="sxs-lookup"><span data-stu-id="02efb-137">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="02efb-138">Nom de l'option.</span><span class="sxs-lookup"><span data-stu-id="02efb-138">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="02efb-139">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="02efb-139">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="02efb-140">string</span><span class="sxs-lookup"><span data-stu-id="02efb-140">string</span></span><br/> | <span data-ttu-id="02efb-141">n/a</span><span class="sxs-lookup"><span data-stu-id="02efb-141">n/a</span></span><br/>        | <span data-ttu-id="02efb-142">True, False.</span><span class="sxs-lookup"><span data-stu-id="02efb-142">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="02efb-143">Définit une option qui, lorsqu’elle est sélectionnée, désactive cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="02efb-143">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="02efb-144">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="02efb-144">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="02efb-145">Les mots clés de schéma d’impression publics sont définis dans l' https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords espace de noms.</span><span class="sxs-lookup"><span data-stu-id="02efb-145">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="02efb-146">Le contenu de la Extensible Markup Language publique (XML) pour ce mot clé est défini ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="02efb-146">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="02efb-147">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="02efb-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="02efb-148">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="02efb-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




