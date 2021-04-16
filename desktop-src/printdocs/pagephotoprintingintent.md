---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: f9a00828-52df-449e-914b-4c6cd7c29f3a
title: PagePhotoPrintingIntent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3985d6f21d0d7731d1c08d080d64a4948b58196d
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "104530603"
---
# <a name="pagephotoprintingintent"></a><span data-ttu-id="04a23-104">PagePhotoPrintingIntent</span><span class="sxs-lookup"><span data-stu-id="04a23-104">PagePhotoPrintingIntent</span></span>

<span data-ttu-id="04a23-105">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="04a23-105">This topic is not current.</span></span> <span data-ttu-id="04a23-106">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="04a23-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="04a23-107">Indique un objectif de haut niveau pour le pilote pour le remplissage des paramètres d’impression de photos.</span><span class="sxs-lookup"><span data-stu-id="04a23-107">Indicates a high-level intent to the driver for population of photo printing settings.</span></span> <span data-ttu-id="04a23-108">Ces paramètres concernent la qualité de sortie attendue qu’un utilisateur peut spécifier lors de l’impression des photos.</span><span class="sxs-lookup"><span data-stu-id="04a23-108">These settings deal with the expected output quality a user may specify when printing photos.</span></span>

-   [<span data-ttu-id="04a23-109">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="04a23-109">Element Information</span></span>](#element-information)

-   [<span data-ttu-id="04a23-110">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="04a23-110">Structural Content</span></span>](#structural-content)

-   [<span data-ttu-id="04a23-111">Contenu XML</span><span class="sxs-lookup"><span data-stu-id="04a23-111">XML Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="04a23-112">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="04a23-112">Element Information</span></span>



| <span data-ttu-id="04a23-113">Nom</span><span class="sxs-lookup"><span data-stu-id="04a23-113">Name</span></span>                       |                    |
|----------------------------|--------------------|
| <span data-ttu-id="04a23-114">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="04a23-114">Element Type</span></span> <br/>   | <span data-ttu-id="04a23-115">Fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="04a23-115">Feature</span></span><br/> |
| <span data-ttu-id="04a23-116">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="04a23-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="04a23-117">Page</span><span class="sxs-lookup"><span data-stu-id="04a23-117">Page</span></span><br/>    |
| <span data-ttu-id="04a23-118">Notes</span><span class="sxs-lookup"><span data-stu-id="04a23-118">Notes</span></span> <br/>          | <span data-ttu-id="04a23-119">Aucun</span><span class="sxs-lookup"><span data-stu-id="04a23-119">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="04a23-120">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="04a23-120">Structural Content</span></span>

<span data-ttu-id="04a23-121">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="04a23-121">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="04a23-122">Variables de structure</span><span class="sxs-lookup"><span data-stu-id="04a23-122">Structure Variables</span></span>

<span data-ttu-id="04a23-123">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="04a23-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="04a23-124">Nom</span><span class="sxs-lookup"><span data-stu-id="04a23-124">Name</span></span>                               | <span data-ttu-id="04a23-125">Type de données</span><span class="sxs-lookup"><span data-stu-id="04a23-125">Data type</span></span>         | <span data-ttu-id="04a23-126">Unité</span><span class="sxs-lookup"><span data-stu-id="04a23-126">Unit</span></span>                  | <span data-ttu-id="04a23-127">Valeurs prises en charge</span><span class="sxs-lookup"><span data-stu-id="04a23-127">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="04a23-128">Résumé</span><span class="sxs-lookup"><span data-stu-id="04a23-128">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="04a23-129">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="04a23-129">\_OptionName\_</span></span><br/>          | <span data-ttu-id="04a23-130">string</span><span class="sxs-lookup"><span data-stu-id="04a23-130">string</span></span><br/> | <span data-ttu-id="04a23-131">caractères</span><span class="sxs-lookup"><span data-stu-id="04a23-131">characters</span></span><br/> | <span data-ttu-id="04a23-132">Nom complet valide tel que défini par les [espaces de noms dans XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="04a23-132">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="04a23-133">Si aucun espace de noms n’est spécifié, l’espace de noms par défaut est utilisé.</span><span class="sxs-lookup"><span data-stu-id="04a23-133">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="04a23-134">Nom de l’option</span><span class="sxs-lookup"><span data-stu-id="04a23-134">The name of the option</span></span><br/>                                            |
| <span data-ttu-id="04a23-135">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="04a23-135">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="04a23-136">string</span><span class="sxs-lookup"><span data-stu-id="04a23-136">string</span></span><br/> | <span data-ttu-id="04a23-137">n/a</span><span class="sxs-lookup"><span data-stu-id="04a23-137">n/a</span></span><br/>        | <span data-ttu-id="04a23-138">True, False</span><span class="sxs-lookup"><span data-stu-id="04a23-138">True, False</span></span><br/>                                                                                                                                                                | <span data-ttu-id="04a23-139">Définit une option qui, lorsqu’elle est sélectionnée, désactive cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="04a23-139">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="04a23-140">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="04a23-140">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="04a23-141">Les mots clés de schéma d’impression publics sont définis dans l' https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords espace de noms.</span><span class="sxs-lookup"><span data-stu-id="04a23-141">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="04a23-142">Le contenu de la Extensible Markup Language publique (XML) pour ce mot clé est défini ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="04a23-142">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="04a23-143">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="04a23-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="04a23-144">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="04a23-144">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




