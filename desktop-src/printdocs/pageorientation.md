---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: 52f02fc1-56fb-404d-8939-df3a4b21570d
title: PageOrientation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f7f004329c217d4aab6ddc3c1d166037e7c7b5a
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "104393903"
---
# <a name="pageorientation"></a><span data-ttu-id="38bbe-104">PageOrientation</span><span class="sxs-lookup"><span data-stu-id="38bbe-104">PageOrientation</span></span>

<span data-ttu-id="38bbe-105">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="38bbe-105">This topic is not current.</span></span> <span data-ttu-id="38bbe-106">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="38bbe-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="38bbe-107">Décrit l’orientation de la feuille de média physique.</span><span class="sxs-lookup"><span data-stu-id="38bbe-107">Describes the orientation of the physical media sheet.</span></span>



| <span data-ttu-id="38bbe-108">Option</span><span class="sxs-lookup"><span data-stu-id="38bbe-108">Option</span></span>                       | <span data-ttu-id="38bbe-109">Définition</span><span class="sxs-lookup"><span data-stu-id="38bbe-109">Definition</span></span>                                                                                              |
|------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="38bbe-110">Paysage</span><span class="sxs-lookup"><span data-stu-id="38bbe-110">Landscape</span></span> <br/>        | <span data-ttu-id="38bbe-111">Le contenu est pivoté sur la page 90 ? degrés CCW par rapport à l’orientation standard (portrait).</span><span class="sxs-lookup"><span data-stu-id="38bbe-111">Content is rotated on the page 90??degrees CCW relative to standard (portrait) orientation.</span></span><br/>  |
| <span data-ttu-id="38bbe-112">Portrait</span><span class="sxs-lookup"><span data-stu-id="38bbe-112">Portrait</span></span> <br/>         | <span data-ttu-id="38bbe-113">Orientation standard.</span><span class="sxs-lookup"><span data-stu-id="38bbe-113">Standard Orientation.</span></span><br/>                                                                        |
| <span data-ttu-id="38bbe-114">ReverseLandscape</span><span class="sxs-lookup"><span data-stu-id="38bbe-114">ReverseLandscape</span></span> <br/> | <span data-ttu-id="38bbe-115">Le contenu est pivoté sur la page 270 ? degrés CCW par rapport à l’orientation standard (portrait).</span><span class="sxs-lookup"><span data-stu-id="38bbe-115">Content is rotated on the page 270??degrees CCW relative to standard (portrait) orientation.</span></span><br/> |
| <span data-ttu-id="38bbe-116">ReversePortrait</span><span class="sxs-lookup"><span data-stu-id="38bbe-116">ReversePortrait</span></span> <br/>  | <span data-ttu-id="38bbe-117">Le contenu est pivoté sur la page 180 ? degrés par rapport à l’orientation standard (portrait).</span><span class="sxs-lookup"><span data-stu-id="38bbe-117">Content is rotated on the page 180??degrees relative to standard (portrait) orientation.</span></span><br/>     |



 

-   [<span data-ttu-id="38bbe-118">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="38bbe-118">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="38bbe-119">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="38bbe-119">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="38bbe-120">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="38bbe-120">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="38bbe-121">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="38bbe-121">Element Information</span></span>



| <span data-ttu-id="38bbe-122">Nom</span><span class="sxs-lookup"><span data-stu-id="38bbe-122">Name</span></span>                       |                                                                                                                                                                                                         |
|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="38bbe-123">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="38bbe-123">Element Type</span></span> <br/>   | <span data-ttu-id="38bbe-124">Fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="38bbe-124">Feature</span></span><br/>                                                                                                                                                                                      |
| <span data-ttu-id="38bbe-125">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="38bbe-125">Scoping Prefix</span></span> <br/> | <span data-ttu-id="38bbe-126">Page</span><span class="sxs-lookup"><span data-stu-id="38bbe-126">Page</span></span><br/>                                                                                                                                                                                         |
| <span data-ttu-id="38bbe-127">Notes</span><span class="sxs-lookup"><span data-stu-id="38bbe-127">Notes</span></span> <br/>          | <span data-ttu-id="38bbe-128">Si un périphérique d’impression ne peut prendre en charge qu’une seule direction paysage et que cette direction est dite « inversée », l’orientation de la page sera toujours considérée comme « paysage ».</span><span class="sxs-lookup"><span data-stu-id="38bbe-128">If a Printer Device can only support one landscape direction and this direction is referred to as "Reverse Landscape", then the page orientation will still be considered to be "Landscape".</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="38bbe-129">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="38bbe-129">Structural Content</span></span>

<span data-ttu-id="38bbe-130">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="38bbe-130">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageOrientation">
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

## <a name="structure-variables"></a><span data-ttu-id="38bbe-131">Variables de structure</span><span class="sxs-lookup"><span data-stu-id="38bbe-131">Structure Variables</span></span>

<span data-ttu-id="38bbe-132">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="38bbe-132">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="38bbe-133">Nom</span><span class="sxs-lookup"><span data-stu-id="38bbe-133">Name</span></span>                               | <span data-ttu-id="38bbe-134">Type de données</span><span class="sxs-lookup"><span data-stu-id="38bbe-134">Data type</span></span>         | <span data-ttu-id="38bbe-135">Unité</span><span class="sxs-lookup"><span data-stu-id="38bbe-135">Unit</span></span>                  | <span data-ttu-id="38bbe-136">Valeurs prises en charge</span><span class="sxs-lookup"><span data-stu-id="38bbe-136">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="38bbe-137">Résumé</span><span class="sxs-lookup"><span data-stu-id="38bbe-137">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="38bbe-138">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="38bbe-138">\_OptionName\_</span></span><br/>          | <span data-ttu-id="38bbe-139">string</span><span class="sxs-lookup"><span data-stu-id="38bbe-139">string</span></span><br/> | <span data-ttu-id="38bbe-140">caractères</span><span class="sxs-lookup"><span data-stu-id="38bbe-140">characters</span></span><br/> | <span data-ttu-id="38bbe-141">Nom complet valide tel que défini par les [espaces de noms dans XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="38bbe-141">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="38bbe-142">Si aucun espace de noms n’est spécifié, l’espace de noms par défaut est utilisé.</span><span class="sxs-lookup"><span data-stu-id="38bbe-142">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="38bbe-143">Nom de l'option.</span><span class="sxs-lookup"><span data-stu-id="38bbe-143">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="38bbe-144">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="38bbe-144">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="38bbe-145">string</span><span class="sxs-lookup"><span data-stu-id="38bbe-145">string</span></span><br/> | <span data-ttu-id="38bbe-146">n/a</span><span class="sxs-lookup"><span data-stu-id="38bbe-146">n/a</span></span><br/>        | <span data-ttu-id="38bbe-147">True, False.</span><span class="sxs-lookup"><span data-stu-id="38bbe-147">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="38bbe-148">Définit une option qui, lorsqu’elle est sélectionnée, désactive cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="38bbe-148">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="38bbe-149">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="38bbe-149">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="38bbe-150">Les mots clés de schéma d’impression publics sont définis dans l' https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords espace de noms.</span><span class="sxs-lookup"><span data-stu-id="38bbe-150">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="38bbe-151">Le contenu de la Extensible Markup Language publique (XML) pour ce mot clé est défini ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="38bbe-151">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageOrientation">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Content is rotated on the page 90??degrees CCW relative to standard (portrait) orientation.??-->
  <psf:Option name="psk:Landscape" />
  <!-- Standard Orientation-->
  <psf:Option name="psk:Portrait" />
  <!-- Content is rotated on the page 270??degrees CCW relative to standard (portrait) orientation??-->
  <psf:Option name="psk:ReverseLandscape" />
  <!-- Content is rotated on the page 180??degrees relative to standard (portrait) orientation??-->
  <psf:Option name="psk:ReversePortrait" />
</psf:Feature>
    
```

## <a name="related-topics"></a><span data-ttu-id="38bbe-152">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="38bbe-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="38bbe-153">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="38bbe-153">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




