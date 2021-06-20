---
description: En savoir plus sur l’élément JobOptimalDestinationColorProfile qui spécifie le profil de couleurs optimal en fonction de la configuration actuelle de l’appareil.
ms.assetid: 70790dc2-180a-4e04-91a9-a10ee76c836b
title: JobOptimalDestinationColorProfile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e7ad2ea269594809b047922ea4f6c99b924e5ae
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408842"
---
# <a name="joboptimaldestinationcolorprofile"></a><span data-ttu-id="2d6af-103">JobOptimalDestinationColorProfile</span><span class="sxs-lookup"><span data-stu-id="2d6af-103">JobOptimalDestinationColorProfile</span></span>

<span data-ttu-id="2d6af-104">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="2d6af-104">This topic is not current.</span></span> <span data-ttu-id="2d6af-105">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="2d6af-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="2d6af-106">Spécifie le profil de couleurs optimal en fonction de la configuration actuelle de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="2d6af-106">Specifies the optimal color profile given the current device configuration.</span></span>

-   [<span data-ttu-id="2d6af-107">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="2d6af-107">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="2d6af-108">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="2d6af-108">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="2d6af-109">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="2d6af-109">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="2d6af-110">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="2d6af-110">Element Information</span></span>



| <span data-ttu-id="2d6af-111">Nom</span><span class="sxs-lookup"><span data-stu-id="2d6af-111">Name</span></span> | <span data-ttu-id="2d6af-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="2d6af-112">Value</span></span> |
|----------------------------|---------------------|
| <span data-ttu-id="2d6af-113">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="2d6af-113">Element Type</span></span> <br/>   | <span data-ttu-id="2d6af-114">Propriété</span><span class="sxs-lookup"><span data-stu-id="2d6af-114">Property</span></span><br/> |
| <span data-ttu-id="2d6af-115">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="2d6af-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="2d6af-116">Travail</span><span class="sxs-lookup"><span data-stu-id="2d6af-116">Job</span></span><br/>      |
| <span data-ttu-id="2d6af-117">Notes</span><span class="sxs-lookup"><span data-stu-id="2d6af-117">Notes</span></span> <br/>          | <span data-ttu-id="2d6af-118">Aucun</span><span class="sxs-lookup"><span data-stu-id="2d6af-118">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="2d6af-119">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="2d6af-119">Structural Content</span></span>

<span data-ttu-id="2d6af-120">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="2d6af-120">The XML structure of this element is:</span></span>

``` syntax
<psf:Property name="psk:JobOptimalDestinationColorProfile">
  <psf:Property name="psk:Profile">
    <psf:Value xsi:type="xs:string">_ProfileValue_</psf:Value>
    <psf:Property name="psk:ProfileData">
      <psf:Value xsi:type="xs:string">_ProfileDataValue_</psf:Value>
    </psf:Property>
    <psf:Property name="psk:Path">
      <psf:Value xsi:type="xs:string">_PathValue_</psf:Value>
    </psf:Property>
  </psf:Property>
</psf:Property>
```

## <a name="structure-variables"></a><span data-ttu-id="2d6af-121">Variables de structure</span><span class="sxs-lookup"><span data-stu-id="2d6af-121">Structure Variables</span></span>

<span data-ttu-id="2d6af-122">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="2d6af-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="2d6af-123">Nom</span><span class="sxs-lookup"><span data-stu-id="2d6af-123">Name</span></span>                            | <span data-ttu-id="2d6af-124">Type de données</span><span class="sxs-lookup"><span data-stu-id="2d6af-124">Data type</span></span>         | <span data-ttu-id="2d6af-125">Unité</span><span class="sxs-lookup"><span data-stu-id="2d6af-125">Unit</span></span>           | <span data-ttu-id="2d6af-126">Valeurs prises en charge</span><span class="sxs-lookup"><span data-stu-id="2d6af-126">Supported values</span></span>          | <span data-ttu-id="2d6af-127">Résumé</span><span class="sxs-lookup"><span data-stu-id="2d6af-127">Summary</span></span>                                        |
|---------------------------------|-------------------|----------------|---------------------------|------------------------------------------------|
| <span data-ttu-id="2d6af-128">\_ProfileValue\_</span><span class="sxs-lookup"><span data-stu-id="2d6af-128">\_ProfileValue\_</span></span><br/>     | <span data-ttu-id="2d6af-129">string</span><span class="sxs-lookup"><span data-stu-id="2d6af-129">string</span></span><br/> | <span data-ttu-id="2d6af-130">n/a</span><span class="sxs-lookup"><span data-stu-id="2d6af-130">n/a</span></span><br/> | <span data-ttu-id="2d6af-131">RGB, ICC, CMJN</span><span class="sxs-lookup"><span data-stu-id="2d6af-131">RGB, ICC, CMYK</span></span><br/> | <span data-ttu-id="2d6af-132">Spécifie le profil de couleurs.</span><span class="sxs-lookup"><span data-stu-id="2d6af-132">Specifies the color profile.</span></span><br/>        |
| <span data-ttu-id="2d6af-133">\_PathValue\_</span><span class="sxs-lookup"><span data-stu-id="2d6af-133">\_PathValue\_</span></span><br/>        | <span data-ttu-id="2d6af-134">string</span><span class="sxs-lookup"><span data-stu-id="2d6af-134">string</span></span><br/> | <span data-ttu-id="2d6af-135">n/a</span><span class="sxs-lookup"><span data-stu-id="2d6af-135">n/a</span></span><br/> | <span data-ttu-id="2d6af-136">n/a</span><span class="sxs-lookup"><span data-stu-id="2d6af-136">n/a</span></span><br/>            | <span data-ttu-id="2d6af-137">Spécifie le chemin d’accès au profil.</span><span class="sxs-lookup"><span data-stu-id="2d6af-137">Specifies file path to the profile.</span></span><br/> |
| <span data-ttu-id="2d6af-138">\_ProfileDataValue\_</span><span class="sxs-lookup"><span data-stu-id="2d6af-138">\_ProfileDataValue\_</span></span><br/> | <span data-ttu-id="2d6af-139">string</span><span class="sxs-lookup"><span data-stu-id="2d6af-139">string</span></span><br/> | <span data-ttu-id="2d6af-140">n/a</span><span class="sxs-lookup"><span data-stu-id="2d6af-140">n/a</span></span><br/> | <span data-ttu-id="2d6af-141">n/a</span><span class="sxs-lookup"><span data-stu-id="2d6af-141">n/a</span></span><br/>            | <span data-ttu-id="2d6af-142">Contient le contenu des données de profil.</span><span class="sxs-lookup"><span data-stu-id="2d6af-142">Contains profile data content.</span></span><br/>      |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="2d6af-143">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="2d6af-143">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="2d6af-144">Les mots clés de schéma d’impression publics sont définis dans l' https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords espace de noms.</span><span class="sxs-lookup"><span data-stu-id="2d6af-144">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="2d6af-145">Le contenu de la Extensible Markup Language publique (XML) pour ce mot clé est défini ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="2d6af-145">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
 <psf:Property name="psk:JobOptimalDestinationColorProfile">
  <psf:Property name="psk:Profile">
    <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    <psf:Property name="psk:ProfileData">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:Property>
    <psf:Property name="psk:Path">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:Property>
  </psf:Property>
</psf:Property>
```

## <a name="related-topics"></a><span data-ttu-id="2d6af-146">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2d6af-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2d6af-147">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="2d6af-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




