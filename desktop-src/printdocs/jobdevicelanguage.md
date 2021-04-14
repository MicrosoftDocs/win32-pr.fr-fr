---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: 3894d9fa-2bf7-447a-bac3-e72a0fdb7187
title: JobDeviceLanguage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da5b128cd8a0bd06cc259d3da0daf834f3c2aebf
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "104321766"
---
# <a name="jobdevicelanguage"></a><span data-ttu-id="74add-104">JobDeviceLanguage</span><span class="sxs-lookup"><span data-stu-id="74add-104">JobDeviceLanguage</span></span>

<span data-ttu-id="74add-105">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="74add-105">This topic is not current.</span></span> <span data-ttu-id="74add-106">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="74add-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="74add-107">Décrit les langues de l’appareil prises en charge pour l’envoi de données du pilote vers l’appareil physique.</span><span class="sxs-lookup"><span data-stu-id="74add-107">Describes the device languages supported for sending data from driver to physical device.</span></span> <span data-ttu-id="74add-108">Cela est souvent appelé « langage de description de page ».</span><span class="sxs-lookup"><span data-stu-id="74add-108">This is often called "Page Description Language".</span></span> <span data-ttu-id="74add-109">Ce mot clé définit le langage de description de page pris en charge par le pilote et l’appareil physique.</span><span class="sxs-lookup"><span data-stu-id="74add-109">This keyword defines what page description language is supported by the driver and physical device.</span></span>

-   [<span data-ttu-id="74add-110">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="74add-110">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="74add-111">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="74add-111">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="74add-112">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="74add-112">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="74add-113">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="74add-113">Element Information</span></span>



| <span data-ttu-id="74add-114">Nom</span><span class="sxs-lookup"><span data-stu-id="74add-114">Name</span></span>                       |                    |
|----------------------------|--------------------|
| <span data-ttu-id="74add-115">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="74add-115">Element Type</span></span> <br/>   | <span data-ttu-id="74add-116">Fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="74add-116">Feature</span></span><br/> |
| <span data-ttu-id="74add-117">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="74add-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="74add-118">Travail</span><span class="sxs-lookup"><span data-stu-id="74add-118">Job</span></span><br/>     |
| <span data-ttu-id="74add-119">Notes</span><span class="sxs-lookup"><span data-stu-id="74add-119">Notes</span></span> <br/>          | <span data-ttu-id="74add-120">Aucun</span><span class="sxs-lookup"><span data-stu-id="74add-120">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="74add-121">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="74add-121">Structural Content</span></span>

<span data-ttu-id="74add-122">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="74add-122">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:JobDeviceLanguage">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_value_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_LanguageEncodingValue_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_LanguageVersionValue_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
      
```

## <a name="structure-variables"></a><span data-ttu-id="74add-123">Variables de structure</span><span class="sxs-lookup"><span data-stu-id="74add-123">Structure Variables</span></span>

<span data-ttu-id="74add-124">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="74add-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="74add-125">Nom</span><span class="sxs-lookup"><span data-stu-id="74add-125">Name</span></span>                                 | <span data-ttu-id="74add-126">Type de données</span><span class="sxs-lookup"><span data-stu-id="74add-126">Data type</span></span>         | <span data-ttu-id="74add-127">Unité</span><span class="sxs-lookup"><span data-stu-id="74add-127">Unit</span></span>                  | <span data-ttu-id="74add-128">Valeurs prises en charge</span><span class="sxs-lookup"><span data-stu-id="74add-128">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="74add-129">Résumé</span><span class="sxs-lookup"><span data-stu-id="74add-129">Summary</span></span>                                                                      |
|--------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="74add-130">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="74add-130">\_OptionName\_</span></span><br/>            | <span data-ttu-id="74add-131">string</span><span class="sxs-lookup"><span data-stu-id="74add-131">string</span></span><br/> | <span data-ttu-id="74add-132">caractères</span><span class="sxs-lookup"><span data-stu-id="74add-132">characters</span></span><br/> | <span data-ttu-id="74add-133">Nom complet valide tel que défini par les [espaces de noms dans XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="74add-133">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="74add-134">Si aucun espace de noms n’est spécifié, l’espace de noms par défaut est utilisé.</span><span class="sxs-lookup"><span data-stu-id="74add-134">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="74add-135">Nom de l'option.</span><span class="sxs-lookup"><span data-stu-id="74add-135">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="74add-136">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="74add-136">\_IdentityOptionValue\_</span></span><br/>   | <span data-ttu-id="74add-137">string</span><span class="sxs-lookup"><span data-stu-id="74add-137">string</span></span><br/> | <span data-ttu-id="74add-138">n/a</span><span class="sxs-lookup"><span data-stu-id="74add-138">n/a</span></span><br/>        | <span data-ttu-id="74add-139">True, False.</span><span class="sxs-lookup"><span data-stu-id="74add-139">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="74add-140">Définit une option qui, lorsqu’elle est sélectionnée, désactive cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="74add-140">Defines an Option which when selected would disable this feature.</span></span><br/> |
| <span data-ttu-id="74add-141">\_LanguageLevelValue\_</span><span class="sxs-lookup"><span data-stu-id="74add-141">\_LanguageLevelValue\_</span></span><br/>    | <span data-ttu-id="74add-142">string</span><span class="sxs-lookup"><span data-stu-id="74add-142">string</span></span><br/> | <span data-ttu-id="74add-143">n/a</span><span class="sxs-lookup"><span data-stu-id="74add-143">n/a</span></span><br/>        | <span data-ttu-id="74add-144">Aucun</span><span class="sxs-lookup"><span data-stu-id="74add-144">None.</span></span><br/>                                                                                                                                                                      | <span data-ttu-id="74add-145">Spécifie le niveau de langage (par exemple, PS de niveau 2).</span><span class="sxs-lookup"><span data-stu-id="74add-145">Specifies the language level (for example, PS Level 2).</span></span><br/>           |
| <span data-ttu-id="74add-146">\_LanguageEncodingValue\_</span><span class="sxs-lookup"><span data-stu-id="74add-146">\_LanguageEncodingValue\_</span></span><br/> | <span data-ttu-id="74add-147">string</span><span class="sxs-lookup"><span data-stu-id="74add-147">string</span></span><br/> | <span data-ttu-id="74add-148">n/a</span><span class="sxs-lookup"><span data-stu-id="74add-148">n/a</span></span><br/>        | <span data-ttu-id="74add-149">Aucun</span><span class="sxs-lookup"><span data-stu-id="74add-149">None.</span></span><br/>                                                                                                                                                                      | <span data-ttu-id="74add-150">Spécifie l’encodage de la langue (par exemple, ISOLatin1).</span><span class="sxs-lookup"><span data-stu-id="74add-150">Specifies the language encoding (for example, ISOLatin1).</span></span><br/>         |
| <span data-ttu-id="74add-151">\_LanguageVersionValue\_</span><span class="sxs-lookup"><span data-stu-id="74add-151">\_LanguageVersionValue\_</span></span><br/>  | <span data-ttu-id="74add-152">string</span><span class="sxs-lookup"><span data-stu-id="74add-152">string</span></span><br/> | <span data-ttu-id="74add-153">n/a</span><span class="sxs-lookup"><span data-stu-id="74add-153">n/a</span></span><br/>        | <span data-ttu-id="74add-154">Aucun</span><span class="sxs-lookup"><span data-stu-id="74add-154">None.</span></span><br/>                                                                                                                                                                      | <span data-ttu-id="74add-155">Spécifie la version du langage.</span><span class="sxs-lookup"><span data-stu-id="74add-155">Specifies the language version.</span></span><br/>                                   |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="74add-156">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="74add-156">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="74add-157">Les mots clés de schéma d’impression publics sont définis dans l' https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords espace de noms.</span><span class="sxs-lookup"><span data-stu-id="74add-157">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="74add-158">Le contenu de la Extensible Markup Language publique (XML) pour ce mot clé est défini ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="74add-158">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:JobDeviceLanguage">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!--Specifies device language is XPS-->
  <psf:Option name="psk:XPS">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specifies device language is PC-PR201 -->
  <psf:Option name="psk:_201PL">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is ART -->
  <psf:Option name="psk:ART">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is ASCII -->
  <psf:Option name="psk:ASCII">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is CaPSL-->
  <psf:Option name="psk:CaPSL">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is ESC/P2-->
  <psf:Option name="psk:ESCP2">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is ESC/Page-->
  <psf:Option name="psk:ESCPage">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is HP-GL/2-->
  <psf:Option name="psk:HPGL2">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is KPDL -->
  <psf:Option name="psk:KPDL">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is KS -->
  <psf:Option name="psk:KS">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is KSSM -->
  <psf:Option name="psk:KSSM">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is PCL -->
  <psf:Option name="psk:PCL">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is PCL5c -->
  <psf:Option name="psk:PCL5c">
    <psf:ScoredProperty name="LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is PCL5e -->
  <psf:Option name="psk:PCL5e">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is PCL-XL -->
  <psf:Option name="psk:PCL-XL">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is PostScript -->
  <psf:Option name="psk:PostScript">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is PPDS -->
  <psf:Option name="psk:PPDS">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is RPDL -->
  <psf:Option name="psk:RPDL">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is RTL -->
  <psf:Option name="psk:RTL">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>    
```

## <a name="related-topics"></a><span data-ttu-id="74add-159">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="74add-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="74add-160">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="74add-160">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




