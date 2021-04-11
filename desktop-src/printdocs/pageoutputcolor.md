---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: 1afcf2e6-5d6d-4b87-a005-15d42a610f69
title: PageOutputColor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71796bae9528fe6b32397f3467113630159c9954
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "104211359"
---
# <a name="pageoutputcolor"></a><span data-ttu-id="69b3a-104">PageOutputColor</span><span class="sxs-lookup"><span data-stu-id="69b3a-104">PageOutputColor</span></span>

<span data-ttu-id="69b3a-105">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="69b3a-105">This topic is not current.</span></span> <span data-ttu-id="69b3a-106">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="69b3a-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="69b3a-107">Décrit les caractéristiques des paramètres de couleur pour la sortie.</span><span class="sxs-lookup"><span data-stu-id="69b3a-107">Describes the characteristics of the color settings for the output.</span></span>

-   [<span data-ttu-id="69b3a-108">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="69b3a-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="69b3a-109">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="69b3a-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="69b3a-110">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="69b3a-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="69b3a-111">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="69b3a-111">Element Information</span></span>



| <span data-ttu-id="69b3a-112">Nom</span><span class="sxs-lookup"><span data-stu-id="69b3a-112">Name</span></span>                       |                    |
|----------------------------|--------------------|
| <span data-ttu-id="69b3a-113">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="69b3a-113">Element Type</span></span> <br/>   | <span data-ttu-id="69b3a-114">Fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="69b3a-114">Feature</span></span><br/> |
| <span data-ttu-id="69b3a-115">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="69b3a-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="69b3a-116">Page</span><span class="sxs-lookup"><span data-stu-id="69b3a-116">Page</span></span><br/>    |
| <span data-ttu-id="69b3a-117">Notes</span><span class="sxs-lookup"><span data-stu-id="69b3a-117">Notes</span></span> <br/>          | <span data-ttu-id="69b3a-118">Aucun</span><span class="sxs-lookup"><span data-stu-id="69b3a-118">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="69b3a-119">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="69b3a-119">Structural Content</span></span>

<span data-ttu-id="69b3a-120">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="69b3a-120">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="69b3a-121">Variables de structure</span><span class="sxs-lookup"><span data-stu-id="69b3a-121">Structure Variables</span></span>

<span data-ttu-id="69b3a-122">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="69b3a-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="69b3a-123">Nom</span><span class="sxs-lookup"><span data-stu-id="69b3a-123">Name</span></span>                                   | <span data-ttu-id="69b3a-124">Type de données</span><span class="sxs-lookup"><span data-stu-id="69b3a-124">Data type</span></span>          | <span data-ttu-id="69b3a-125">Unité</span><span class="sxs-lookup"><span data-stu-id="69b3a-125">Unit</span></span>                      | <span data-ttu-id="69b3a-126">Valeurs prises en charge</span><span class="sxs-lookup"><span data-stu-id="69b3a-126">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="69b3a-127">Résumé</span><span class="sxs-lookup"><span data-stu-id="69b3a-127">Summary</span></span>                                                                                                                           |
|----------------------------------------|--------------------|---------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="69b3a-128">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="69b3a-128">\_OptionName\_</span></span><br/>              | <span data-ttu-id="69b3a-129">string</span><span class="sxs-lookup"><span data-stu-id="69b3a-129">string</span></span><br/>  | <span data-ttu-id="69b3a-130">caractères</span><span class="sxs-lookup"><span data-stu-id="69b3a-130">characters</span></span><br/>     | <span data-ttu-id="69b3a-131">Nom complet valide tel que défini par les [espaces de noms dans XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="69b3a-131">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="69b3a-132">Si aucun espace de noms n’est spécifié, l’espace de noms par défaut est utilisé.</span><span class="sxs-lookup"><span data-stu-id="69b3a-132">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="69b3a-133">Nom de l'option.</span><span class="sxs-lookup"><span data-stu-id="69b3a-133">The name of the option.</span></span><br/>                                                                                                |
| <span data-ttu-id="69b3a-134">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="69b3a-134">\_IdentityOptionValue\_</span></span><br/>     | <span data-ttu-id="69b3a-135">string</span><span class="sxs-lookup"><span data-stu-id="69b3a-135">string</span></span><br/>  | <span data-ttu-id="69b3a-136">n/a</span><span class="sxs-lookup"><span data-stu-id="69b3a-136">n/a</span></span><br/>            | <span data-ttu-id="69b3a-137">True, False.</span><span class="sxs-lookup"><span data-stu-id="69b3a-137">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="69b3a-138">Définit une option qui, lorsqu’elle est sélectionnée, désactive cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="69b3a-138">Defines an Option which when selected would disable this feature.</span></span><br/>                                                      |
| <span data-ttu-id="69b3a-139">\_DeviceBitsPerPixelValue\_</span><span class="sxs-lookup"><span data-stu-id="69b3a-139">\_DeviceBitsPerPixelValue\_</span></span><br/> | <span data-ttu-id="69b3a-140">entier</span><span class="sxs-lookup"><span data-stu-id="69b3a-140">integer</span></span><br/> | <span data-ttu-id="69b3a-141">bits par pixel</span><span class="sxs-lookup"><span data-stu-id="69b3a-141">bits per pixel</span></span><br/> | <span data-ttu-id="69b3a-142">Valeur supérieure à 0, inférieure à la valeur maximale prise en charge du périphérique.</span><span class="sxs-lookup"><span data-stu-id="69b3a-142">Greater than 0, less than maximum device support value.</span></span><br/>                                                                                                                    | <span data-ttu-id="69b3a-143">Valeur numérique indiquant le nombre de bits par pixel des données de couleur prises en charge par l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="69b3a-143">Numeric value indicating the number of bits per pixel of color data supported by the printer.</span></span><br/>                          |
| <span data-ttu-id="69b3a-144">\_DriverBitsPerPixelValue\_</span><span class="sxs-lookup"><span data-stu-id="69b3a-144">\_DriverBitsPerPixelValue\_</span></span><br/> | <span data-ttu-id="69b3a-145">entier</span><span class="sxs-lookup"><span data-stu-id="69b3a-145">integer</span></span><br/> | <span data-ttu-id="69b3a-146">bits par pixel</span><span class="sxs-lookup"><span data-stu-id="69b3a-146">bits per pixel</span></span><br/> | <span data-ttu-id="69b3a-147">Valeur supérieure à 0, inférieure à la valeur maximale prise en charge du périphérique.</span><span class="sxs-lookup"><span data-stu-id="69b3a-147">Greater than 0, less than maximum device support value.</span></span><br/>                                                                                                                    | <span data-ttu-id="69b3a-148">Valeur numérique indiquant le nombre de bits par pixel que le pilote de base doit utiliser pour sa mémoire tampon de rendu bitmap.</span><span class="sxs-lookup"><span data-stu-id="69b3a-148">Numeric value indicating the number of bits per pixel that the core driver should use for its bitmap rendering buffer.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="69b3a-149">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="69b3a-149">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="69b3a-150">Les mots clés de schéma d’impression publics sont définis dans l' https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords espace de noms.</span><span class="sxs-lookup"><span data-stu-id="69b3a-150">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="69b3a-151">Le contenu de la Extensible Markup Language publique (XML) pour ce mot clé est défini ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="69b3a-151">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="69b3a-152">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="69b3a-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="69b3a-153">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="69b3a-153">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




