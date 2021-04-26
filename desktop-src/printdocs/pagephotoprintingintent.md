---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: f9a00828-52df-449e-914b-4c6cd7c29f3a
title: PagePhotoPrintingIntent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01d56a0b46c73bb3afdcefe96dc2131c861d5419
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997976"
---
# <a name="pagephotoprintingintent"></a><span data-ttu-id="0d25a-104">PagePhotoPrintingIntent</span><span class="sxs-lookup"><span data-stu-id="0d25a-104">PagePhotoPrintingIntent</span></span>

<span data-ttu-id="0d25a-105">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="0d25a-105">This topic is not current.</span></span> <span data-ttu-id="0d25a-106">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="0d25a-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="0d25a-107">Indique un objectif de haut niveau pour le pilote pour le remplissage des paramètres d’impression de photos.</span><span class="sxs-lookup"><span data-stu-id="0d25a-107">Indicates a high-level intent to the driver for population of photo printing settings.</span></span> <span data-ttu-id="0d25a-108">Ces paramètres concernent la qualité de sortie attendue qu’un utilisateur peut spécifier lors de l’impression des photos.</span><span class="sxs-lookup"><span data-stu-id="0d25a-108">These settings deal with the expected output quality a user may specify when printing photos.</span></span>

-   [<span data-ttu-id="0d25a-109">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="0d25a-109">Element Information</span></span>](#element-information)

-   [<span data-ttu-id="0d25a-110">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="0d25a-110">Structural Content</span></span>](#structural-content)

-   [<span data-ttu-id="0d25a-111">Contenu XML</span><span class="sxs-lookup"><span data-stu-id="0d25a-111">XML Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="0d25a-112">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="0d25a-112">Element Information</span></span>



| <span data-ttu-id="0d25a-113">Nom</span><span class="sxs-lookup"><span data-stu-id="0d25a-113">Name</span></span> | <span data-ttu-id="0d25a-114">Value</span><span class="sxs-lookup"><span data-stu-id="0d25a-114">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="0d25a-115">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="0d25a-115">Element Type</span></span> <br/>   | <span data-ttu-id="0d25a-116">Fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="0d25a-116">Feature</span></span><br/> |
| <span data-ttu-id="0d25a-117">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="0d25a-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="0d25a-118">Page</span><span class="sxs-lookup"><span data-stu-id="0d25a-118">Page</span></span><br/>    |
| <span data-ttu-id="0d25a-119">Notes</span><span class="sxs-lookup"><span data-stu-id="0d25a-119">Notes</span></span> <br/>          | <span data-ttu-id="0d25a-120">Aucun</span><span class="sxs-lookup"><span data-stu-id="0d25a-120">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="0d25a-121">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="0d25a-121">Structural Content</span></span>

<span data-ttu-id="0d25a-122">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="0d25a-122">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PagePhotoPrintingIntent">  
  <psf:Property name="SelectionType">
    <psf:Value xsi:type="xs:string">PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
    <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
  </psf:Property>
</psf:Feature>
      
```

## <a name="structure-variables"></a><span data-ttu-id="0d25a-123">Variables de structure</span><span class="sxs-lookup"><span data-stu-id="0d25a-123">Structure Variables</span></span>

<span data-ttu-id="0d25a-124">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="0d25a-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="0d25a-125">Nom</span><span class="sxs-lookup"><span data-stu-id="0d25a-125">Name</span></span>                               | <span data-ttu-id="0d25a-126">Type de données</span><span class="sxs-lookup"><span data-stu-id="0d25a-126">Data type</span></span>         | <span data-ttu-id="0d25a-127">Unité</span><span class="sxs-lookup"><span data-stu-id="0d25a-127">Unit</span></span>                  | <span data-ttu-id="0d25a-128">Valeurs prises en charge</span><span class="sxs-lookup"><span data-stu-id="0d25a-128">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="0d25a-129">Résumé</span><span class="sxs-lookup"><span data-stu-id="0d25a-129">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="0d25a-130">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="0d25a-130">\_OptionName\_</span></span><br/>          | <span data-ttu-id="0d25a-131">string</span><span class="sxs-lookup"><span data-stu-id="0d25a-131">string</span></span><br/> | <span data-ttu-id="0d25a-132">caractères</span><span class="sxs-lookup"><span data-stu-id="0d25a-132">characters</span></span><br/> | <span data-ttu-id="0d25a-133">Nom complet valide tel que défini par les [espaces de noms dans XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="0d25a-133">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="0d25a-134">Si aucun espace de noms n’est spécifié, l’espace de noms par défaut est utilisé.</span><span class="sxs-lookup"><span data-stu-id="0d25a-134">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="0d25a-135">Nom de l’option</span><span class="sxs-lookup"><span data-stu-id="0d25a-135">The name of the option</span></span><br/>                                            |
| <span data-ttu-id="0d25a-136">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="0d25a-136">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="0d25a-137">string</span><span class="sxs-lookup"><span data-stu-id="0d25a-137">string</span></span><br/> | <span data-ttu-id="0d25a-138">n/a</span><span class="sxs-lookup"><span data-stu-id="0d25a-138">n/a</span></span><br/>        | <span data-ttu-id="0d25a-139">True, False</span><span class="sxs-lookup"><span data-stu-id="0d25a-139">True, False</span></span><br/>                                                                                                                                                                | <span data-ttu-id="0d25a-140">Définit une option qui, lorsqu’elle est sélectionnée, désactive cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="0d25a-140">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="0d25a-141">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="0d25a-141">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="0d25a-142">Les mots clés de schéma d’impression publics sont définis dans l' https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords espace de noms.</span><span class="sxs-lookup"><span data-stu-id="0d25a-142">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="0d25a-143">Le contenu de la Extensible Markup Language publique (XML) pour ce mot clé est défini ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="0d25a-143">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PagePhotoPrintingIntent">
  <psf:Property name="SelectionType">
    <psf:Value xsi:type="xs:string">PickOne</psf:Value>
  </psf:Property>
  <!-- No Photoprinting Intent (Allows the application to specify no intent resolution.  (PrintTicket settings should not be altered) -->
  <psf:Option name="psk:None" />
  <!-- Best Quality Photoprinting (Provided mostly for marketing reasons; utilizes the highest capabilities of the device) -->
  <psf:Option name="psk:PhotoBest" />
  <!-- Draft Quality Photoprinting (Quick, low ink volume print for proofing purposes) -->
  <psf:Option name="psk:PhotoDraft" />
  <!-- Standard Quality Photoprinting (OEM suggested settings for standard photo-printing) -->
  <psf:Option name="psk:PhotoStandard" />
</psf:Feature>    
```

## <a name="related-topics"></a><span data-ttu-id="0d25a-144">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0d25a-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0d25a-145">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="0d25a-145">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




