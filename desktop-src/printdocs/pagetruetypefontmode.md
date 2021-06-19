---
description: En savoir plus sur l’élément configurable par l’utilisateur PageTrueTypeFontMode. Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: 36b1de5d-8575-42cf-b158-dcf7705ec157
title: PageTrueTypeFontMode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf30af3684693f594f497dbad95d4f9a7743d624
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395614"
---
# <a name="pagetruetypefontmode"></a><span data-ttu-id="12fa2-105">PageTrueTypeFontMode</span><span class="sxs-lookup"><span data-stu-id="12fa2-105">PageTrueTypeFontMode</span></span>

<span data-ttu-id="12fa2-106">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="12fa2-106">This topic is not current.</span></span> <span data-ttu-id="12fa2-107">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="12fa2-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="12fa2-108">Décrit la méthode de gestion des polices TrueType à utiliser.</span><span class="sxs-lookup"><span data-stu-id="12fa2-108">Describes the method of TrueType font handling to be used.</span></span>

-   [<span data-ttu-id="12fa2-109">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="12fa2-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="12fa2-110">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="12fa2-110">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="12fa2-111">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="12fa2-111">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="12fa2-112">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="12fa2-112">Element Information</span></span>



| <span data-ttu-id="12fa2-113">Nom</span><span class="sxs-lookup"><span data-stu-id="12fa2-113">Name</span></span> | <span data-ttu-id="12fa2-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="12fa2-114">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="12fa2-115">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="12fa2-115">Element Type</span></span> <br/>   | <span data-ttu-id="12fa2-116">Fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="12fa2-116">Feature</span></span><br/> |
| <span data-ttu-id="12fa2-117">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="12fa2-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="12fa2-118">Page</span><span class="sxs-lookup"><span data-stu-id="12fa2-118">Page</span></span><br/>    |
| <span data-ttu-id="12fa2-119">Notes</span><span class="sxs-lookup"><span data-stu-id="12fa2-119">Notes</span></span> <br/>          | <span data-ttu-id="12fa2-120">Aucun</span><span class="sxs-lookup"><span data-stu-id="12fa2-120">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="12fa2-121">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="12fa2-121">Structural Content</span></span>

<span data-ttu-id="12fa2-122">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="12fa2-122">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="12fa2-123">Variables de structure</span><span class="sxs-lookup"><span data-stu-id="12fa2-123">Structure Variables</span></span>

<span data-ttu-id="12fa2-124">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="12fa2-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="12fa2-125">Nom</span><span class="sxs-lookup"><span data-stu-id="12fa2-125">Name</span></span>                               | <span data-ttu-id="12fa2-126">Type de données</span><span class="sxs-lookup"><span data-stu-id="12fa2-126">Data type</span></span>         | <span data-ttu-id="12fa2-127">Unité</span><span class="sxs-lookup"><span data-stu-id="12fa2-127">Unit</span></span>                  | <span data-ttu-id="12fa2-128">Valeurs prises en charge</span><span class="sxs-lookup"><span data-stu-id="12fa2-128">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="12fa2-129">Résumé</span><span class="sxs-lookup"><span data-stu-id="12fa2-129">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="12fa2-130">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="12fa2-130">\_OptionName\_</span></span><br/>          | <span data-ttu-id="12fa2-131">string</span><span class="sxs-lookup"><span data-stu-id="12fa2-131">string</span></span><br/> | <span data-ttu-id="12fa2-132">caractères</span><span class="sxs-lookup"><span data-stu-id="12fa2-132">characters</span></span><br/> | <span data-ttu-id="12fa2-133">Nom complet valide tel que défini par les [espaces de noms dans XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="12fa2-133">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="12fa2-134">Si aucun espace de noms n’est spécifié, l’espace de noms par défaut est utilisé.</span><span class="sxs-lookup"><span data-stu-id="12fa2-134">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="12fa2-135">Nom de l'option.</span><span class="sxs-lookup"><span data-stu-id="12fa2-135">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="12fa2-136">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="12fa2-136">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="12fa2-137">string</span><span class="sxs-lookup"><span data-stu-id="12fa2-137">string</span></span><br/> | <span data-ttu-id="12fa2-138">n/a</span><span class="sxs-lookup"><span data-stu-id="12fa2-138">n/a</span></span><br/>        | <span data-ttu-id="12fa2-139">True, False.</span><span class="sxs-lookup"><span data-stu-id="12fa2-139">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="12fa2-140">Définit une option qui, lorsqu’elle est sélectionnée, désactive cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="12fa2-140">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="12fa2-141">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="12fa2-141">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="12fa2-142">Les mots clés de schéma d’impression publics sont définis dans l' https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords espace de noms.</span><span class="sxs-lookup"><span data-stu-id="12fa2-142">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="12fa2-143">Le contenu de la Extensible Markup Language publique (XML) pour ce mot clé est défini ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="12fa2-143">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="12fa2-144">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="12fa2-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="12fa2-145">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="12fa2-145">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




