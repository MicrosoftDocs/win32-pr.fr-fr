---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: 0592f7a4-cace-41b0-91e3-2811f72aeb3e
title: JobDigitalSignatureProcessing
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aad9dbe0ba82d219a28602178efa2e102ccf167b
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998286"
---
# <a name="jobdigitalsignatureprocessing"></a><span data-ttu-id="ac765-104">JobDigitalSignatureProcessing</span><span class="sxs-lookup"><span data-stu-id="ac765-104">JobDigitalSignatureProcessing</span></span>

<span data-ttu-id="ac765-105">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="ac765-105">This topic is not current.</span></span> <span data-ttu-id="ac765-106">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="ac765-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="ac765-107">Décrit la configuration du traitement de signature numérique pour l’ensemble du travail.</span><span class="sxs-lookup"><span data-stu-id="ac765-107">Describes configuring the digital signature processing for the entire job.</span></span> <span data-ttu-id="ac765-108">S’applique uniquement au contenu qui contient des signatures numériques.</span><span class="sxs-lookup"><span data-stu-id="ac765-108">Applicable only to content that contains digital signatures.</span></span>

-   [<span data-ttu-id="ac765-109">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="ac765-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="ac765-110">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="ac765-110">Structural Content</span></span>](#structural-content)

## <a name="element-information"></a><span data-ttu-id="ac765-111">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="ac765-111">Element Information</span></span>



| <span data-ttu-id="ac765-112">Nom</span><span class="sxs-lookup"><span data-stu-id="ac765-112">Name</span></span> | <span data-ttu-id="ac765-113">Value</span><span class="sxs-lookup"><span data-stu-id="ac765-113">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="ac765-114">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="ac765-114">Element Type</span></span> <br/>   | <span data-ttu-id="ac765-115">Fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="ac765-115">Feature</span></span><br/> |
| <span data-ttu-id="ac765-116">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="ac765-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="ac765-117">Travail</span><span class="sxs-lookup"><span data-stu-id="ac765-117">Job</span></span><br/>     |
| <span data-ttu-id="ac765-118">Notes</span><span class="sxs-lookup"><span data-stu-id="ac765-118">Notes</span></span> <br/>          | <span data-ttu-id="ac765-119">Aucun</span><span class="sxs-lookup"><span data-stu-id="ac765-119">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="ac765-120">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="ac765-120">Structural Content</span></span>

<span data-ttu-id="ac765-121">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="ac765-121">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:JobDigitalSignatureProcessing">
  <psf:Property name="SelectionType">
    <psf:Value xsi:type="xs:string">PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
  </psf:Feature>
```

## <a name="structure-variables"></a><span data-ttu-id="ac765-122">Variables de structure</span><span class="sxs-lookup"><span data-stu-id="ac765-122">Structure Variables</span></span>

<span data-ttu-id="ac765-123">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="ac765-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="ac765-124">Nom</span><span class="sxs-lookup"><span data-stu-id="ac765-124">Name</span></span>                               | <span data-ttu-id="ac765-125">Type de données</span><span class="sxs-lookup"><span data-stu-id="ac765-125">Data type</span></span>         | <span data-ttu-id="ac765-126">Unité</span><span class="sxs-lookup"><span data-stu-id="ac765-126">Unit</span></span>                   | <span data-ttu-id="ac765-127">Valeurs prises en charge</span><span class="sxs-lookup"><span data-stu-id="ac765-127">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="ac765-128">Résumé</span><span class="sxs-lookup"><span data-stu-id="ac765-128">Summary</span></span>                                                                      |
|------------------------------------|-------------------|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="ac765-129">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="ac765-129">\_OptionName\_</span></span><br/>          | <span data-ttu-id="ac765-130">string</span><span class="sxs-lookup"><span data-stu-id="ac765-130">string</span></span><br/> | <span data-ttu-id="ac765-131">caractères</span><span class="sxs-lookup"><span data-stu-id="ac765-131">characters</span></span> <br/> | <span data-ttu-id="ac765-132">Nom complet valide tel que défini par les [espaces de noms dans XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="ac765-132">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="ac765-133">Si aucun espace de noms n’est spécifié, l’espace de noms par défaut est utilisé.</span><span class="sxs-lookup"><span data-stu-id="ac765-133">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="ac765-134">Nom de l’option</span><span class="sxs-lookup"><span data-stu-id="ac765-134">The name of the option</span></span><br/>                                            |
| <span data-ttu-id="ac765-135">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="ac765-135">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="ac765-136">string</span><span class="sxs-lookup"><span data-stu-id="ac765-136">string</span></span><br/> | <span data-ttu-id="ac765-137">n/a</span><span class="sxs-lookup"><span data-stu-id="ac765-137">n/a</span></span><br/>         | <span data-ttu-id="ac765-138">True, False</span><span class="sxs-lookup"><span data-stu-id="ac765-138">True, False</span></span><br/>                                                                                                                                                                | <span data-ttu-id="ac765-139">Définit une option qui, lorsqu’elle est sélectionnée, désactive cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="ac765-139">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="ac765-140">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="ac765-140">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="ac765-141">Les mots clés de schéma d’impression publics sont définis dans l' https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords espace de noms.</span><span class="sxs-lookup"><span data-stu-id="ac765-141">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="ac765-142">Le contenu de la Extensible Markup Language publique (XML) pour ce mot clé est défini ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="ac765-142">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:JobDigitalSignatureProcessing">
  <psf:Property name="SelectionType">
    <psf:Value xsi:type="xs:string">PickOne</psf:Value>
  </psf:Property>
  <!-- Print the job regardless of the validity of the digital signatures. Digital signatures MAY be ignored.  -->
  <psf:Option name="psk:PrintInvalidSignatures" />
  <!-- Print the job regardless of the validity of the digital signatures.  In the event an invalid signature is encountered, an error page should print at the end of the job.  Digital signatures MUST not be ignored. -->
  <psf:Option name="psk:PrintInvalidSignaturesWithErrorReport" />
  <!-- Print the job only if all digital signatures are valid.  Digital signatures MUST not be ignored. -->
  <psf:Option name="psk:PrintOnlyValidSignatures" />
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="ac765-143">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ac765-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ac765-144">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="ac765-144">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




