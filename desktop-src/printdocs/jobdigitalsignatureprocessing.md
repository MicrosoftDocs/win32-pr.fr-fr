---
description: En savoir plus sur l’élément JobDigitalSignatureProcessing, qui décrit la configuration du traitement des signatures numériques pour l’ensemble du travail.
ms.assetid: 0592f7a4-cace-41b0-91e3-2811f72aeb3e
title: JobDigitalSignatureProcessing
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9491a921d9d733dd0de0a4e5133d5c6690b2b4a
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408942"
---
# <a name="jobdigitalsignatureprocessing"></a><span data-ttu-id="53362-103">JobDigitalSignatureProcessing</span><span class="sxs-lookup"><span data-stu-id="53362-103">JobDigitalSignatureProcessing</span></span>

<span data-ttu-id="53362-104">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="53362-104">This topic is not current.</span></span> <span data-ttu-id="53362-105">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="53362-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="53362-106">Décrit la configuration du traitement de signature numérique pour l’ensemble du travail.</span><span class="sxs-lookup"><span data-stu-id="53362-106">Describes configuring the digital signature processing for the entire job.</span></span> <span data-ttu-id="53362-107">S’applique uniquement au contenu qui contient des signatures numériques.</span><span class="sxs-lookup"><span data-stu-id="53362-107">Applicable only to content that contains digital signatures.</span></span>

-   [<span data-ttu-id="53362-108">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="53362-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="53362-109">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="53362-109">Structural Content</span></span>](#structural-content)

## <a name="element-information"></a><span data-ttu-id="53362-110">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="53362-110">Element Information</span></span>



| <span data-ttu-id="53362-111">Nom</span><span class="sxs-lookup"><span data-stu-id="53362-111">Name</span></span> | <span data-ttu-id="53362-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="53362-112">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="53362-113">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="53362-113">Element Type</span></span> <br/>   | <span data-ttu-id="53362-114">Fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="53362-114">Feature</span></span><br/> |
| <span data-ttu-id="53362-115">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="53362-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="53362-116">Travail</span><span class="sxs-lookup"><span data-stu-id="53362-116">Job</span></span><br/>     |
| <span data-ttu-id="53362-117">Notes</span><span class="sxs-lookup"><span data-stu-id="53362-117">Notes</span></span> <br/>          | <span data-ttu-id="53362-118">Aucun</span><span class="sxs-lookup"><span data-stu-id="53362-118">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="53362-119">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="53362-119">Structural Content</span></span>

<span data-ttu-id="53362-120">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="53362-120">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="53362-121">Variables de structure</span><span class="sxs-lookup"><span data-stu-id="53362-121">Structure Variables</span></span>

<span data-ttu-id="53362-122">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="53362-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="53362-123">Nom</span><span class="sxs-lookup"><span data-stu-id="53362-123">Name</span></span>                               | <span data-ttu-id="53362-124">Type de données</span><span class="sxs-lookup"><span data-stu-id="53362-124">Data type</span></span>         | <span data-ttu-id="53362-125">Unité</span><span class="sxs-lookup"><span data-stu-id="53362-125">Unit</span></span>                   | <span data-ttu-id="53362-126">Valeurs prises en charge</span><span class="sxs-lookup"><span data-stu-id="53362-126">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="53362-127">Résumé</span><span class="sxs-lookup"><span data-stu-id="53362-127">Summary</span></span>                                                                      |
|------------------------------------|-------------------|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="53362-128">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="53362-128">\_OptionName\_</span></span><br/>          | <span data-ttu-id="53362-129">string</span><span class="sxs-lookup"><span data-stu-id="53362-129">string</span></span><br/> | <span data-ttu-id="53362-130">caractères</span><span class="sxs-lookup"><span data-stu-id="53362-130">characters</span></span> <br/> | <span data-ttu-id="53362-131">Nom complet valide tel que défini par les [espaces de noms dans XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="53362-131">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="53362-132">Si aucun espace de noms n’est spécifié, l’espace de noms par défaut est utilisé.</span><span class="sxs-lookup"><span data-stu-id="53362-132">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="53362-133">Nom de l’option</span><span class="sxs-lookup"><span data-stu-id="53362-133">The name of the option</span></span><br/>                                            |
| <span data-ttu-id="53362-134">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="53362-134">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="53362-135">string</span><span class="sxs-lookup"><span data-stu-id="53362-135">string</span></span><br/> | <span data-ttu-id="53362-136">n/a</span><span class="sxs-lookup"><span data-stu-id="53362-136">n/a</span></span><br/>         | <span data-ttu-id="53362-137">True, False</span><span class="sxs-lookup"><span data-stu-id="53362-137">True, False</span></span><br/>                                                                                                                                                                | <span data-ttu-id="53362-138">Définit une option qui, lorsqu’elle est sélectionnée, désactive cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="53362-138">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="53362-139">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="53362-139">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="53362-140">Les mots clés de schéma d’impression publics sont définis dans l' https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords espace de noms.</span><span class="sxs-lookup"><span data-stu-id="53362-140">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="53362-141">Le contenu de la Extensible Markup Language publique (XML) pour ce mot clé est défini ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="53362-141">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="53362-142">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="53362-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="53362-143">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="53362-143">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




