---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: 36b1de5d-8575-42cf-b158-dcf7705ec157
title: PageTrueTypeFontMode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9d9a56e2a8a7ec74403a4b59be2a2f5d23a3a41
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995565"
---
# <a name="pagetruetypefontmode"></a><span data-ttu-id="09648-104">PageTrueTypeFontMode</span><span class="sxs-lookup"><span data-stu-id="09648-104">PageTrueTypeFontMode</span></span>

<span data-ttu-id="09648-105">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="09648-105">This topic is not current.</span></span> <span data-ttu-id="09648-106">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="09648-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="09648-107">Décrit la méthode de gestion des polices TrueType à utiliser.</span><span class="sxs-lookup"><span data-stu-id="09648-107">Describes the method of TrueType font handling to be used.</span></span>

-   [<span data-ttu-id="09648-108">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="09648-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="09648-109">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="09648-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="09648-110">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="09648-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="09648-111">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="09648-111">Element Information</span></span>



| <span data-ttu-id="09648-112">Nom</span><span class="sxs-lookup"><span data-stu-id="09648-112">Name</span></span> | <span data-ttu-id="09648-113">Value</span><span class="sxs-lookup"><span data-stu-id="09648-113">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="09648-114">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="09648-114">Element Type</span></span> <br/>   | <span data-ttu-id="09648-115">Fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="09648-115">Feature</span></span><br/> |
| <span data-ttu-id="09648-116">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="09648-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="09648-117">Page</span><span class="sxs-lookup"><span data-stu-id="09648-117">Page</span></span><br/>    |
| <span data-ttu-id="09648-118">Notes</span><span class="sxs-lookup"><span data-stu-id="09648-118">Notes</span></span> <br/>          | <span data-ttu-id="09648-119">Aucun</span><span class="sxs-lookup"><span data-stu-id="09648-119">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="09648-120">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="09648-120">Structural Content</span></span>

<span data-ttu-id="09648-121">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="09648-121">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageTrueTypeFontMode">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
  </psf:Option>
</psf:Feature>
      
```

## <a name="structure-variables"></a><span data-ttu-id="09648-122">Variables de structure</span><span class="sxs-lookup"><span data-stu-id="09648-122">Structure Variables</span></span>

<span data-ttu-id="09648-123">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="09648-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="09648-124">Nom</span><span class="sxs-lookup"><span data-stu-id="09648-124">Name</span></span>                               | <span data-ttu-id="09648-125">Type de données</span><span class="sxs-lookup"><span data-stu-id="09648-125">Data type</span></span>         | <span data-ttu-id="09648-126">Unité</span><span class="sxs-lookup"><span data-stu-id="09648-126">Unit</span></span>                  | <span data-ttu-id="09648-127">Valeurs prises en charge</span><span class="sxs-lookup"><span data-stu-id="09648-127">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="09648-128">Résumé</span><span class="sxs-lookup"><span data-stu-id="09648-128">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="09648-129">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="09648-129">\_OptionName\_</span></span><br/>          | <span data-ttu-id="09648-130">string</span><span class="sxs-lookup"><span data-stu-id="09648-130">string</span></span><br/> | <span data-ttu-id="09648-131">caractères</span><span class="sxs-lookup"><span data-stu-id="09648-131">characters</span></span><br/> | <span data-ttu-id="09648-132">Nom complet valide tel que défini par les [espaces de noms dans XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="09648-132">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="09648-133">Si aucun espace de noms n’est spécifié, l’espace de noms par défaut est utilisé.</span><span class="sxs-lookup"><span data-stu-id="09648-133">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="09648-134">Nom de l'option.</span><span class="sxs-lookup"><span data-stu-id="09648-134">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="09648-135">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="09648-135">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="09648-136">string</span><span class="sxs-lookup"><span data-stu-id="09648-136">string</span></span><br/> | <span data-ttu-id="09648-137">n/a</span><span class="sxs-lookup"><span data-stu-id="09648-137">n/a</span></span><br/>        | <span data-ttu-id="09648-138">True, False.</span><span class="sxs-lookup"><span data-stu-id="09648-138">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="09648-139">Définit une option qui, lorsqu’elle est sélectionnée, désactive cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="09648-139">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="09648-140">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="09648-140">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="09648-141">Les mots clés de schéma d’impression publics sont définis dans l' https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords espace de noms.</span><span class="sxs-lookup"><span data-stu-id="09648-141">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="09648-142">Le contenu de la Extensible Markup Language publique (XML) pour ce mot clé est défini ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="09648-142">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageTrueTypeFontMode">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!--Automatic handling of TrueType font-->
  <psf:Option name="psk:Automatic" />
  <!--TrueType font is downloaded as outline font-->
  <psf:Option name="psk:DownloadAsOutlineFont" />
  <!--TrueType font is downloaded as raster font-->
  <psf:Option name="psk:DownloadAsRasterFont" />
  <!--TrueType font is downloaded as native true type font-->
  <psf:Option name="psk:DownloadAsNativeTrueTypeFont" />
  <!--TrueType font is rendered as a bitmap-->
  <psf:Option name="psk:RenderAsBitmap" />
</psf:Feature>    
```

## <a name="related-topics"></a><span data-ttu-id="09648-143">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="09648-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="09648-144">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="09648-144">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




