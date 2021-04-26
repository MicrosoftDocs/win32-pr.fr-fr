---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: 3e0e2cb2-cb51-446d-a6ff-f76aa8c305f6
title: PageMediaColor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60c9a314bf435664d121fd35e588b62903da323e
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994506"
---
# <a name="pagemediacolor"></a><span data-ttu-id="58a74-104">PageMediaColor</span><span class="sxs-lookup"><span data-stu-id="58a74-104">PageMediaColor</span></span>

<span data-ttu-id="58a74-105">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="58a74-105">This topic is not current.</span></span> <span data-ttu-id="58a74-106">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="58a74-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="58a74-107">Décrit les options de couleur du média et les caractéristiques de chaque option.</span><span class="sxs-lookup"><span data-stu-id="58a74-107">Describes the Media Color options and the characteristics of each option.</span></span>

-   [<span data-ttu-id="58a74-108">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="58a74-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="58a74-109">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="58a74-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="58a74-110">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="58a74-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="58a74-111">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="58a74-111">Element Information</span></span>



| <span data-ttu-id="58a74-112">Nom</span><span class="sxs-lookup"><span data-stu-id="58a74-112">Name</span></span> | <span data-ttu-id="58a74-113">Value</span><span class="sxs-lookup"><span data-stu-id="58a74-113">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="58a74-114">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="58a74-114">Element Type</span></span> <br/>   | <span data-ttu-id="58a74-115">Fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="58a74-115">Feature</span></span><br/> |
| <span data-ttu-id="58a74-116">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="58a74-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="58a74-117">Page</span><span class="sxs-lookup"><span data-stu-id="58a74-117">Page</span></span><br/>    |
| <span data-ttu-id="58a74-118">Notes</span><span class="sxs-lookup"><span data-stu-id="58a74-118">Notes</span></span> <br/>          | <span data-ttu-id="58a74-119">Aucun</span><span class="sxs-lookup"><span data-stu-id="58a74-119">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="58a74-120">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="58a74-120">Structural Content</span></span>

<span data-ttu-id="58a74-121">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="58a74-121">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageMediaColor">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">_MediaColorsRGBValue_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
      
```

## <a name="structure-variables"></a><span data-ttu-id="58a74-122">Variables de structure</span><span class="sxs-lookup"><span data-stu-id="58a74-122">Structure Variables</span></span>

<span data-ttu-id="58a74-123">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="58a74-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="58a74-124">Nom</span><span class="sxs-lookup"><span data-stu-id="58a74-124">Name</span></span>                               | <span data-ttu-id="58a74-125">Type de données</span><span class="sxs-lookup"><span data-stu-id="58a74-125">Data type</span></span>         | <span data-ttu-id="58a74-126">Unité</span><span class="sxs-lookup"><span data-stu-id="58a74-126">Unit</span></span>                  | <span data-ttu-id="58a74-127">Valeurs prises en charge</span><span class="sxs-lookup"><span data-stu-id="58a74-127">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="58a74-128">Résumé</span><span class="sxs-lookup"><span data-stu-id="58a74-128">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="58a74-129">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="58a74-129">\_OptionName\_</span></span><br/>          | <span data-ttu-id="58a74-130">string</span><span class="sxs-lookup"><span data-stu-id="58a74-130">string</span></span><br/> | <span data-ttu-id="58a74-131">caractères</span><span class="sxs-lookup"><span data-stu-id="58a74-131">characters</span></span><br/> | <span data-ttu-id="58a74-132">Nom complet valide tel que défini par les [espaces de noms dans XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="58a74-132">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="58a74-133">Si aucun espace de noms n’est spécifié, l’espace de noms par défaut est utilisé.</span><span class="sxs-lookup"><span data-stu-id="58a74-133">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="58a74-134">Nom de l'option.</span><span class="sxs-lookup"><span data-stu-id="58a74-134">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="58a74-135">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="58a74-135">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="58a74-136">string</span><span class="sxs-lookup"><span data-stu-id="58a74-136">string</span></span><br/> | <span data-ttu-id="58a74-137">n/a</span><span class="sxs-lookup"><span data-stu-id="58a74-137">n/a</span></span><br/>        | <span data-ttu-id="58a74-138">True, False.</span><span class="sxs-lookup"><span data-stu-id="58a74-138">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="58a74-139">Définit une option qui, lorsqu’elle est sélectionnée, désactive cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="58a74-139">Defines an Option which when selected would disable this feature.</span></span><br/> |
| <span data-ttu-id="58a74-140">\_MediaColorsRGBValue\_</span><span class="sxs-lookup"><span data-stu-id="58a74-140">\_MediaColorsRGBValue\_</span></span><br/> | <span data-ttu-id="58a74-141">string</span><span class="sxs-lookup"><span data-stu-id="58a74-141">string</span></span><br/> | <span data-ttu-id="58a74-142">Couleur sRVB</span><span class="sxs-lookup"><span data-stu-id="58a74-142">sRGB Color</span></span><br/> | <span data-ttu-id="58a74-143">\#AARRVVBB où A, R, G, B représentent des chiffres hexadécimaux.</span><span class="sxs-lookup"><span data-stu-id="58a74-143">\#AARRGGBB where A, R, G, B represent hexadecimal digits.</span></span><br/>                                                                                                                  | <span data-ttu-id="58a74-144">Définit la couleur sRVB pour la feuille de média physique.</span><span class="sxs-lookup"><span data-stu-id="58a74-144">Defines the sRGB color for the physical media sheet.</span></span> <br/>             |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="58a74-145">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="58a74-145">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="58a74-146">Les mots clés de schéma d’impression publics sont définis dans l' `https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords` espace de noms.</span><span class="sxs-lookup"><span data-stu-id="58a74-146">The public Print Schema keywords are defined in the `https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords` namespace.</span></span> <span data-ttu-id="58a74-147">Le contenu de la Extensible Markup Language publique (XML) pour ce mot clé est défini ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="58a74-147">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageMediaColor">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:Black">
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">#FF000000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:Blue">
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">#FF0000FF</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:Brown">
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">#FFA52A2A</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:Gold">
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">#FFFFD700</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:GoldenRod">
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">#FFDAA520</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:Gray">
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">#FF808080</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:Green">
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">#FF008000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:Ivory">
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">#FFFFFFF0</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NoColor">
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:Orange">
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">#FFFFA500</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:Pink">
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">#FFFFC0CB</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:Red">
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">#FFFF0000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:Silver">
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">#FFC0C0C0</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:Turquoise">
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">#FF40E0D0</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:Violet">
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">#FFEE82EE</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:White">
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">#FFFFFFFF</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:Yellow">
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">#FFFFFF00</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies a custom page color. -->
  <psf:Option name="psk:Custom">
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="58a74-148">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="58a74-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="58a74-149">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="58a74-149">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>
