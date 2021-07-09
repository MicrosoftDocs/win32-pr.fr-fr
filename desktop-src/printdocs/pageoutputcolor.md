---
description: En savoir plus sur l’élément configurable par l’utilisateur PageOutputColor. Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: 1afcf2e6-5d6d-4b87-a005-15d42a610f69
title: PageOutputColor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79fc71f58bde44224642d3a5f6979e3aef929976
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/09/2021
ms.locfileid: "113548987"
---
# <a name="pageoutputcolor"></a><span data-ttu-id="fe888-105">PageOutputColor</span><span class="sxs-lookup"><span data-stu-id="fe888-105">PageOutputColor</span></span>

<span data-ttu-id="fe888-106">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="fe888-106">This topic is not current.</span></span> <span data-ttu-id="fe888-107">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="fe888-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="fe888-108">Décrit les caractéristiques des paramètres de couleur pour la sortie.</span><span class="sxs-lookup"><span data-stu-id="fe888-108">Describes the characteristics of the color settings for the output.</span></span>

-   [<span data-ttu-id="fe888-109">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="fe888-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="fe888-110">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="fe888-110">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="fe888-111">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="fe888-111">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="fe888-112">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="fe888-112">Element Information</span></span>



| <span data-ttu-id="fe888-113">Nom</span><span class="sxs-lookup"><span data-stu-id="fe888-113">Name</span></span> | <span data-ttu-id="fe888-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="fe888-114">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="fe888-115">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="fe888-115">Element Type</span></span> <br/>   | <span data-ttu-id="fe888-116">Composant</span><span class="sxs-lookup"><span data-stu-id="fe888-116">Feature</span></span><br/> |
| <span data-ttu-id="fe888-117">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="fe888-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="fe888-118">Page</span><span class="sxs-lookup"><span data-stu-id="fe888-118">Page</span></span><br/>    |
| <span data-ttu-id="fe888-119">Notes</span><span class="sxs-lookup"><span data-stu-id="fe888-119">Notes</span></span> <br/>          | <span data-ttu-id="fe888-120">Aucun</span><span class="sxs-lookup"><span data-stu-id="fe888-120">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="fe888-121">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="fe888-121">Structural Content</span></span>

<span data-ttu-id="fe888-122">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="fe888-122">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="fe888-123">Variables de structure</span><span class="sxs-lookup"><span data-stu-id="fe888-123">Structure Variables</span></span>

<span data-ttu-id="fe888-124">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="fe888-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="fe888-125">Nom</span><span class="sxs-lookup"><span data-stu-id="fe888-125">Name</span></span>                                   | <span data-ttu-id="fe888-126">Type de données</span><span class="sxs-lookup"><span data-stu-id="fe888-126">Data type</span></span>          | <span data-ttu-id="fe888-127">Unité</span><span class="sxs-lookup"><span data-stu-id="fe888-127">Unit</span></span>                      | <span data-ttu-id="fe888-128">Valeurs prises en charge</span><span class="sxs-lookup"><span data-stu-id="fe888-128">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="fe888-129">Résumé</span><span class="sxs-lookup"><span data-stu-id="fe888-129">Summary</span></span>                                                                                                                           |
|----------------------------------------|--------------------|---------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe888-130">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="fe888-130">\_OptionName\_</span></span><br/>              | <span data-ttu-id="fe888-131">string</span><span class="sxs-lookup"><span data-stu-id="fe888-131">string</span></span><br/>  | <span data-ttu-id="fe888-132">caractères</span><span class="sxs-lookup"><span data-stu-id="fe888-132">characters</span></span><br/>     | <span data-ttu-id="fe888-133">Nom complet valide tel que défini par les [espaces de noms dans XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="fe888-133">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="fe888-134">Si aucun espace de noms n’est spécifié, l’espace de noms par défaut est utilisé.</span><span class="sxs-lookup"><span data-stu-id="fe888-134">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="fe888-135">Nom de l'option.</span><span class="sxs-lookup"><span data-stu-id="fe888-135">The name of the option.</span></span><br/>                                                                                                |
| <span data-ttu-id="fe888-136">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="fe888-136">\_IdentityOptionValue\_</span></span><br/>     | <span data-ttu-id="fe888-137">string</span><span class="sxs-lookup"><span data-stu-id="fe888-137">string</span></span><br/>  | <span data-ttu-id="fe888-138">n/a</span><span class="sxs-lookup"><span data-stu-id="fe888-138">n/a</span></span><br/>            | <span data-ttu-id="fe888-139">True, False.</span><span class="sxs-lookup"><span data-stu-id="fe888-139">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="fe888-140">Définit une option qui, lorsqu’elle est sélectionnée, désactive cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="fe888-140">Defines an Option which when selected would disable this feature.</span></span><br/>                                                      |
| <span data-ttu-id="fe888-141">\_DeviceBitsPerPixelValue\_</span><span class="sxs-lookup"><span data-stu-id="fe888-141">\_DeviceBitsPerPixelValue\_</span></span><br/> | <span data-ttu-id="fe888-142">entier</span><span class="sxs-lookup"><span data-stu-id="fe888-142">integer</span></span><br/> | <span data-ttu-id="fe888-143">bits par pixel</span><span class="sxs-lookup"><span data-stu-id="fe888-143">bits per pixel</span></span><br/> | <span data-ttu-id="fe888-144">Valeur supérieure à 0, inférieure à la valeur maximale prise en charge du périphérique.</span><span class="sxs-lookup"><span data-stu-id="fe888-144">Greater than 0, less than maximum device support value.</span></span><br/>                                                                                                                    | <span data-ttu-id="fe888-145">Valeur numérique indiquant le nombre de bits par pixel des données de couleur prises en charge par l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="fe888-145">Numeric value indicating the number of bits per pixel of color data supported by the printer.</span></span><br/>                          |
| <span data-ttu-id="fe888-146">\_DriverBitsPerPixelValue\_</span><span class="sxs-lookup"><span data-stu-id="fe888-146">\_DriverBitsPerPixelValue\_</span></span><br/> | <span data-ttu-id="fe888-147">entier</span><span class="sxs-lookup"><span data-stu-id="fe888-147">integer</span></span><br/> | <span data-ttu-id="fe888-148">bits par pixel</span><span class="sxs-lookup"><span data-stu-id="fe888-148">bits per pixel</span></span><br/> | <span data-ttu-id="fe888-149">Valeur supérieure à 0, inférieure à la valeur maximale prise en charge du périphérique.</span><span class="sxs-lookup"><span data-stu-id="fe888-149">Greater than 0, less than maximum device support value.</span></span><br/>                                                                                                                    | <span data-ttu-id="fe888-150">Valeur numérique indiquant le nombre de bits par pixel que le pilote de base doit utiliser pour sa mémoire tampon de rendu bitmap.</span><span class="sxs-lookup"><span data-stu-id="fe888-150">Numeric value indicating the number of bits per pixel that the core driver should use for its bitmap rendering buffer.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="fe888-151">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="fe888-151">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="fe888-152">Les mots clés de schéma d’impression publics sont définis dans l' https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords espace de noms.</span><span class="sxs-lookup"><span data-stu-id="fe888-152">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="fe888-153">Le contenu de la Extensible Markup Language publique (XML) pour ce mot clé est défini ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="fe888-153">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="fe888-154">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="fe888-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fe888-155">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="fe888-155">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




