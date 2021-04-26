---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: 1afcf2e6-5d6d-4b87-a005-15d42a610f69
title: PageOutputColor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4791ca4a53b8bdcc43a32c5c7aa5a1e38bbe1e5
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998046"
---
# <a name="pageoutputcolor"></a><span data-ttu-id="6dd3e-104">PageOutputColor</span><span class="sxs-lookup"><span data-stu-id="6dd3e-104">PageOutputColor</span></span>

<span data-ttu-id="6dd3e-105">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="6dd3e-105">This topic is not current.</span></span> <span data-ttu-id="6dd3e-106">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="6dd3e-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="6dd3e-107">Décrit les caractéristiques des paramètres de couleur pour la sortie.</span><span class="sxs-lookup"><span data-stu-id="6dd3e-107">Describes the characteristics of the color settings for the output.</span></span>

-   [<span data-ttu-id="6dd3e-108">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="6dd3e-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="6dd3e-109">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="6dd3e-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="6dd3e-110">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="6dd3e-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="6dd3e-111">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="6dd3e-111">Element Information</span></span>



| <span data-ttu-id="6dd3e-112">Nom</span><span class="sxs-lookup"><span data-stu-id="6dd3e-112">Name</span></span> | <span data-ttu-id="6dd3e-113">Value</span><span class="sxs-lookup"><span data-stu-id="6dd3e-113">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="6dd3e-114">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="6dd3e-114">Element Type</span></span> <br/>   | <span data-ttu-id="6dd3e-115">Fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="6dd3e-115">Feature</span></span><br/> |
| <span data-ttu-id="6dd3e-116">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="6dd3e-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="6dd3e-117">Page</span><span class="sxs-lookup"><span data-stu-id="6dd3e-117">Page</span></span><br/>    |
| <span data-ttu-id="6dd3e-118">Notes</span><span class="sxs-lookup"><span data-stu-id="6dd3e-118">Notes</span></span> <br/>          | <span data-ttu-id="6dd3e-119">Aucun</span><span class="sxs-lookup"><span data-stu-id="6dd3e-119">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="6dd3e-120">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="6dd3e-120">Structural Content</span></span>

<span data-ttu-id="6dd3e-121">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="6dd3e-121">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageOutputColor">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <psf:ScoredProperty name=psk:DeviceBitsPerPixel>
      <psf:Value xsi:type="xs:integer">_DeviceBitsPerPixelValue_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name=psk:DriverBitsPerPixel>
      <psf:Value xsi:type="xs:integer">_DriverBitsPerPixelValue_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
      
```

## <a name="structure-variables"></a><span data-ttu-id="6dd3e-122">Variables de structure</span><span class="sxs-lookup"><span data-stu-id="6dd3e-122">Structure Variables</span></span>

<span data-ttu-id="6dd3e-123">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="6dd3e-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="6dd3e-124">Nom</span><span class="sxs-lookup"><span data-stu-id="6dd3e-124">Name</span></span>                                   | <span data-ttu-id="6dd3e-125">Type de données</span><span class="sxs-lookup"><span data-stu-id="6dd3e-125">Data type</span></span>          | <span data-ttu-id="6dd3e-126">Unité</span><span class="sxs-lookup"><span data-stu-id="6dd3e-126">Unit</span></span>                      | <span data-ttu-id="6dd3e-127">Valeurs prises en charge</span><span class="sxs-lookup"><span data-stu-id="6dd3e-127">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="6dd3e-128">Résumé</span><span class="sxs-lookup"><span data-stu-id="6dd3e-128">Summary</span></span>                                                                                                                           |
|----------------------------------------|--------------------|---------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6dd3e-129">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="6dd3e-129">\_OptionName\_</span></span><br/>              | <span data-ttu-id="6dd3e-130">string</span><span class="sxs-lookup"><span data-stu-id="6dd3e-130">string</span></span><br/>  | <span data-ttu-id="6dd3e-131">caractères</span><span class="sxs-lookup"><span data-stu-id="6dd3e-131">characters</span></span><br/>     | <span data-ttu-id="6dd3e-132">Nom complet valide tel que défini par les [espaces de noms dans XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="6dd3e-132">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="6dd3e-133">Si aucun espace de noms n’est spécifié, l’espace de noms par défaut est utilisé.</span><span class="sxs-lookup"><span data-stu-id="6dd3e-133">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="6dd3e-134">Nom de l'option.</span><span class="sxs-lookup"><span data-stu-id="6dd3e-134">The name of the option.</span></span><br/>                                                                                                |
| <span data-ttu-id="6dd3e-135">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="6dd3e-135">\_IdentityOptionValue\_</span></span><br/>     | <span data-ttu-id="6dd3e-136">string</span><span class="sxs-lookup"><span data-stu-id="6dd3e-136">string</span></span><br/>  | <span data-ttu-id="6dd3e-137">n/a</span><span class="sxs-lookup"><span data-stu-id="6dd3e-137">n/a</span></span><br/>            | <span data-ttu-id="6dd3e-138">True, False.</span><span class="sxs-lookup"><span data-stu-id="6dd3e-138">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="6dd3e-139">Définit une option qui, lorsqu’elle est sélectionnée, désactive cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="6dd3e-139">Defines an Option which when selected would disable this feature.</span></span><br/>                                                      |
| <span data-ttu-id="6dd3e-140">\_DeviceBitsPerPixelValue\_</span><span class="sxs-lookup"><span data-stu-id="6dd3e-140">\_DeviceBitsPerPixelValue\_</span></span><br/> | <span data-ttu-id="6dd3e-141">entier</span><span class="sxs-lookup"><span data-stu-id="6dd3e-141">integer</span></span><br/> | <span data-ttu-id="6dd3e-142">bits par pixel</span><span class="sxs-lookup"><span data-stu-id="6dd3e-142">bits per pixel</span></span><br/> | <span data-ttu-id="6dd3e-143">Valeur supérieure à 0, inférieure à la valeur maximale prise en charge du périphérique.</span><span class="sxs-lookup"><span data-stu-id="6dd3e-143">Greater than 0, less than maximum device support value.</span></span><br/>                                                                                                                    | <span data-ttu-id="6dd3e-144">Valeur numérique indiquant le nombre de bits par pixel des données de couleur prises en charge par l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="6dd3e-144">Numeric value indicating the number of bits per pixel of color data supported by the printer.</span></span><br/>                          |
| <span data-ttu-id="6dd3e-145">\_DriverBitsPerPixelValue\_</span><span class="sxs-lookup"><span data-stu-id="6dd3e-145">\_DriverBitsPerPixelValue\_</span></span><br/> | <span data-ttu-id="6dd3e-146">entier</span><span class="sxs-lookup"><span data-stu-id="6dd3e-146">integer</span></span><br/> | <span data-ttu-id="6dd3e-147">bits par pixel</span><span class="sxs-lookup"><span data-stu-id="6dd3e-147">bits per pixel</span></span><br/> | <span data-ttu-id="6dd3e-148">Valeur supérieure à 0, inférieure à la valeur maximale prise en charge du périphérique.</span><span class="sxs-lookup"><span data-stu-id="6dd3e-148">Greater than 0, less than maximum device support value.</span></span><br/>                                                                                                                    | <span data-ttu-id="6dd3e-149">Valeur numérique indiquant le nombre de bits par pixel que le pilote de base doit utiliser pour sa mémoire tampon de rendu bitmap.</span><span class="sxs-lookup"><span data-stu-id="6dd3e-149">Numeric value indicating the number of bits per pixel that the core driver should use for its bitmap rendering buffer.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="6dd3e-150">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="6dd3e-150">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="6dd3e-151">Les mots clés de schéma d’impression publics sont définis dans l' https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords espace de noms.</span><span class="sxs-lookup"><span data-stu-id="6dd3e-151">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="6dd3e-152">Le contenu de la Extensible Markup Language publique (XML) pour ce mot clé est défini ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="6dd3e-152">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageOutputColor">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies the output should be in color. -->
  <psf:Option name="psk:Color">
    <psf:ScoredProperty name="psk:DeviceBitsPerPixel">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:DriverBitsPerPixel">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies the output should be in grayscale. -->
  <psf:Option name="psk:Grayscale">
    <psf:ScoredProperty name="psk:DeviceBitsPerPixel">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:DriverBitsPerPixel">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies the output should be in monochrome (Black). -->
  <psf:Option name="psk:Monochrome">
    <psf:ScoredProperty name="psk:DeviceBitsPerPixel">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:DriverBitsPerPixel">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="6dd3e-153">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6dd3e-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6dd3e-154">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="6dd3e-154">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




