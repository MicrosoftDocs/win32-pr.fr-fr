---
description: En savoir plus sur l’élément configurable par l’utilisateur PageICMRenderingIntent. Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: df11ee89-fe62-4fe5-a1d6-0f925360ca39
title: PageICMRenderingIntent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab595bac5a7136510335167c37bc36d8a7e44056
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/09/2021
ms.locfileid: "113549177"
---
# <a name="pageicmrenderingintent"></a><span data-ttu-id="ca14d-105">PageICMRenderingIntent</span><span class="sxs-lookup"><span data-stu-id="ca14d-105">PageICMRenderingIntent</span></span>

<span data-ttu-id="ca14d-106">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="ca14d-106">This topic is not current.</span></span> <span data-ttu-id="ca14d-107">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="ca14d-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="ca14d-108">Décrit l’intention de rendu telle que définie par la spécification ICC v2.</span><span class="sxs-lookup"><span data-stu-id="ca14d-108">Describes the rendering intent as defined by the ICC v2 Specification.</span></span> <span data-ttu-id="ca14d-109">Cette valeur doit être ignorée si une image ou un élément graphique a un profil incorporé qui spécifie l’intention de rendu.</span><span class="sxs-lookup"><span data-stu-id="ca14d-109">This value should be ignored if an image or graphical element has an embedded profile that specifies the Rendering intent.</span></span>

-   [<span data-ttu-id="ca14d-110">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="ca14d-110">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="ca14d-111">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="ca14d-111">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="ca14d-112">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="ca14d-112">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="ca14d-113">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="ca14d-113">Element Information</span></span>



| <span data-ttu-id="ca14d-114">Nom</span><span class="sxs-lookup"><span data-stu-id="ca14d-114">Name</span></span> | <span data-ttu-id="ca14d-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="ca14d-115">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="ca14d-116">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="ca14d-116">Element Type</span></span> <br/>   | <span data-ttu-id="ca14d-117">Composant</span><span class="sxs-lookup"><span data-stu-id="ca14d-117">Feature</span></span><br/> |
| <span data-ttu-id="ca14d-118">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="ca14d-118">Scoping Prefix</span></span> <br/> | <span data-ttu-id="ca14d-119">Page</span><span class="sxs-lookup"><span data-stu-id="ca14d-119">Page</span></span><br/>    |
| <span data-ttu-id="ca14d-120">Notes</span><span class="sxs-lookup"><span data-stu-id="ca14d-120">Notes</span></span> <br/>          | <span data-ttu-id="ca14d-121">Aucun</span><span class="sxs-lookup"><span data-stu-id="ca14d-121">None</span></span> <br/>   |



 

## <a name="structural-content"></a><span data-ttu-id="ca14d-122">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="ca14d-122">Structural Content</span></span>

<span data-ttu-id="ca14d-123">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="ca14d-123">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageICMRenderingIntent">
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

## <a name="structure-variables"></a><span data-ttu-id="ca14d-124">Variables de structure</span><span class="sxs-lookup"><span data-stu-id="ca14d-124">Structure Variables</span></span>

<span data-ttu-id="ca14d-125">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="ca14d-125">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="ca14d-126">Nom</span><span class="sxs-lookup"><span data-stu-id="ca14d-126">Name</span></span>                               | <span data-ttu-id="ca14d-127">Type de données</span><span class="sxs-lookup"><span data-stu-id="ca14d-127">Data type</span></span>         | <span data-ttu-id="ca14d-128">Unité</span><span class="sxs-lookup"><span data-stu-id="ca14d-128">Unit</span></span>                  | <span data-ttu-id="ca14d-129">Valeurs prises en charge</span><span class="sxs-lookup"><span data-stu-id="ca14d-129">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="ca14d-130">Résumé</span><span class="sxs-lookup"><span data-stu-id="ca14d-130">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="ca14d-131">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="ca14d-131">\_OptionName\_</span></span><br/>          | <span data-ttu-id="ca14d-132">string</span><span class="sxs-lookup"><span data-stu-id="ca14d-132">string</span></span><br/> | <span data-ttu-id="ca14d-133">caractères</span><span class="sxs-lookup"><span data-stu-id="ca14d-133">characters</span></span><br/> | <span data-ttu-id="ca14d-134">Nom complet valide tel que défini par les [espaces de noms dans XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="ca14d-134">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="ca14d-135">Si aucun espace de noms n’est spécifié, l’espace de noms par défaut est utilisé.</span><span class="sxs-lookup"><span data-stu-id="ca14d-135">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="ca14d-136">Nom de l'option.</span><span class="sxs-lookup"><span data-stu-id="ca14d-136">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="ca14d-137">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="ca14d-137">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="ca14d-138">string</span><span class="sxs-lookup"><span data-stu-id="ca14d-138">string</span></span><br/> | <span data-ttu-id="ca14d-139">n/a</span><span class="sxs-lookup"><span data-stu-id="ca14d-139">n/a</span></span><br/>        | <span data-ttu-id="ca14d-140">True, False.</span><span class="sxs-lookup"><span data-stu-id="ca14d-140">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="ca14d-141">Définit une option qui, lorsqu’elle est sélectionnée, désactive cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="ca14d-141">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="ca14d-142">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="ca14d-142">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="ca14d-143">Les mots clés de schéma d’impression publics sont définis dans l' https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords espace de noms.</span><span class="sxs-lookup"><span data-stu-id="ca14d-143">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="ca14d-144">Le contenu de la Extensible Markup Language publique (XML) pour ce mot clé est défini ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="ca14d-144">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageICMRenderingIntent">
  <psf:Property name="SelectionType">
    <psf:Value xsi:type="xs:string">PickOne</psf:Value>
  </psf:Property>
  <!--Absolute Colorimetric Rendering intent-->
  <psf:Option name="psk:AbsoluteColorimetric" />
  <!--Relative Colorimetric Rendering intent -->
  <psf:Option name="psk:RelativeColorimetric" />
  <!--Photographs Rendering intent -->
  <psf:Option name="psk:Photographs" />
  <!--Business Graphics Rendering intent -->
  <psf:Option name="psk:BusinessGraphics" />
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="ca14d-145">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ca14d-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ca14d-146">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="ca14d-146">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




