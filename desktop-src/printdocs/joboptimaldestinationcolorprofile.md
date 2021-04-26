---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: 70790dc2-180a-4e04-91a9-a10ee76c836b
title: JobOptimalDestinationColorProfile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45630b2ddbe94f19905f01c508fc4d852d29566b
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107999249"
---
# <a name="joboptimaldestinationcolorprofile"></a><span data-ttu-id="257b2-104">JobOptimalDestinationColorProfile</span><span class="sxs-lookup"><span data-stu-id="257b2-104">JobOptimalDestinationColorProfile</span></span>

<span data-ttu-id="257b2-105">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="257b2-105">This topic is not current.</span></span> <span data-ttu-id="257b2-106">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="257b2-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="257b2-107">Spécifie le profil de couleurs optimal en fonction de la configuration actuelle de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="257b2-107">Specifies the optimal color profile given the current device configuration.</span></span>

-   [<span data-ttu-id="257b2-108">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="257b2-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="257b2-109">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="257b2-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="257b2-110">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="257b2-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="257b2-111">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="257b2-111">Element Information</span></span>



| <span data-ttu-id="257b2-112">Nom</span><span class="sxs-lookup"><span data-stu-id="257b2-112">Name</span></span> | <span data-ttu-id="257b2-113">Value</span><span class="sxs-lookup"><span data-stu-id="257b2-113">Value</span></span> |
|----------------------------|---------------------|
| <span data-ttu-id="257b2-114">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="257b2-114">Element Type</span></span> <br/>   | <span data-ttu-id="257b2-115">Propriété</span><span class="sxs-lookup"><span data-stu-id="257b2-115">Property</span></span><br/> |
| <span data-ttu-id="257b2-116">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="257b2-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="257b2-117">Travail</span><span class="sxs-lookup"><span data-stu-id="257b2-117">Job</span></span><br/>      |
| <span data-ttu-id="257b2-118">Notes</span><span class="sxs-lookup"><span data-stu-id="257b2-118">Notes</span></span> <br/>          | <span data-ttu-id="257b2-119">Aucun</span><span class="sxs-lookup"><span data-stu-id="257b2-119">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="257b2-120">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="257b2-120">Structural Content</span></span>

<span data-ttu-id="257b2-121">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="257b2-121">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="257b2-122">Variables de structure</span><span class="sxs-lookup"><span data-stu-id="257b2-122">Structure Variables</span></span>

<span data-ttu-id="257b2-123">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="257b2-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="257b2-124">Nom</span><span class="sxs-lookup"><span data-stu-id="257b2-124">Name</span></span>                            | <span data-ttu-id="257b2-125">Type de données</span><span class="sxs-lookup"><span data-stu-id="257b2-125">Data type</span></span>         | <span data-ttu-id="257b2-126">Unité</span><span class="sxs-lookup"><span data-stu-id="257b2-126">Unit</span></span>           | <span data-ttu-id="257b2-127">Valeurs prises en charge</span><span class="sxs-lookup"><span data-stu-id="257b2-127">Supported values</span></span>          | <span data-ttu-id="257b2-128">Résumé</span><span class="sxs-lookup"><span data-stu-id="257b2-128">Summary</span></span>                                        |
|---------------------------------|-------------------|----------------|---------------------------|------------------------------------------------|
| <span data-ttu-id="257b2-129">\_ProfileValue\_</span><span class="sxs-lookup"><span data-stu-id="257b2-129">\_ProfileValue\_</span></span><br/>     | <span data-ttu-id="257b2-130">string</span><span class="sxs-lookup"><span data-stu-id="257b2-130">string</span></span><br/> | <span data-ttu-id="257b2-131">n/a</span><span class="sxs-lookup"><span data-stu-id="257b2-131">n/a</span></span><br/> | <span data-ttu-id="257b2-132">RGB, ICC, CMJN</span><span class="sxs-lookup"><span data-stu-id="257b2-132">RGB, ICC, CMYK</span></span><br/> | <span data-ttu-id="257b2-133">Spécifie le profil de couleurs.</span><span class="sxs-lookup"><span data-stu-id="257b2-133">Specifies the color profile.</span></span><br/>        |
| <span data-ttu-id="257b2-134">\_PathValue\_</span><span class="sxs-lookup"><span data-stu-id="257b2-134">\_PathValue\_</span></span><br/>        | <span data-ttu-id="257b2-135">string</span><span class="sxs-lookup"><span data-stu-id="257b2-135">string</span></span><br/> | <span data-ttu-id="257b2-136">n/a</span><span class="sxs-lookup"><span data-stu-id="257b2-136">n/a</span></span><br/> | <span data-ttu-id="257b2-137">n/a</span><span class="sxs-lookup"><span data-stu-id="257b2-137">n/a</span></span><br/>            | <span data-ttu-id="257b2-138">Spécifie le chemin d’accès au profil.</span><span class="sxs-lookup"><span data-stu-id="257b2-138">Specifies file path to the profile.</span></span><br/> |
| <span data-ttu-id="257b2-139">\_ProfileDataValue\_</span><span class="sxs-lookup"><span data-stu-id="257b2-139">\_ProfileDataValue\_</span></span><br/> | <span data-ttu-id="257b2-140">string</span><span class="sxs-lookup"><span data-stu-id="257b2-140">string</span></span><br/> | <span data-ttu-id="257b2-141">n/a</span><span class="sxs-lookup"><span data-stu-id="257b2-141">n/a</span></span><br/> | <span data-ttu-id="257b2-142">n/a</span><span class="sxs-lookup"><span data-stu-id="257b2-142">n/a</span></span><br/>            | <span data-ttu-id="257b2-143">Contient le contenu des données de profil.</span><span class="sxs-lookup"><span data-stu-id="257b2-143">Contains profile data content.</span></span><br/>      |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="257b2-144">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="257b2-144">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="257b2-145">Les mots clés de schéma d’impression publics sont définis dans l' https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords espace de noms.</span><span class="sxs-lookup"><span data-stu-id="257b2-145">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="257b2-146">Le contenu de la Extensible Markup Language publique (XML) pour ce mot clé est défini ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="257b2-146">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="257b2-147">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="257b2-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="257b2-148">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="257b2-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




