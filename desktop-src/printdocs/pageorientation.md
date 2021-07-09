---
description: En savoir plus sur l’élément configurable par l’utilisateur PageOrientation. Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: 52f02fc1-56fb-404d-8939-df3a4b21570d
title: PageOrientation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6f0af08fcd29f34bb55bd16b1eac50487e96ffb
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/09/2021
ms.locfileid: "113549117"
---
# <a name="pageorientation"></a><span data-ttu-id="4c2fc-105">PageOrientation</span><span class="sxs-lookup"><span data-stu-id="4c2fc-105">PageOrientation</span></span>

<span data-ttu-id="4c2fc-106">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="4c2fc-106">This topic is not current.</span></span> <span data-ttu-id="4c2fc-107">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="4c2fc-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="4c2fc-108">Décrit l’orientation de la feuille de média physique.</span><span class="sxs-lookup"><span data-stu-id="4c2fc-108">Describes the orientation of the physical media sheet.</span></span>



| <span data-ttu-id="4c2fc-109">Option</span><span class="sxs-lookup"><span data-stu-id="4c2fc-109">Option</span></span>                       | <span data-ttu-id="4c2fc-110">Définition</span><span class="sxs-lookup"><span data-stu-id="4c2fc-110">Definition</span></span>                                                                                              |
|------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4c2fc-111">Paysage</span><span class="sxs-lookup"><span data-stu-id="4c2fc-111">Landscape</span></span> <br/>        | <span data-ttu-id="4c2fc-112">Le contenu est pivoté sur la page 90 ? degrés CCW par rapport à l’orientation standard (portrait).</span><span class="sxs-lookup"><span data-stu-id="4c2fc-112">Content is rotated on the page 90??degrees CCW relative to standard (portrait) orientation.</span></span><br/>  |
| <span data-ttu-id="4c2fc-113">Portrait</span><span class="sxs-lookup"><span data-stu-id="4c2fc-113">Portrait</span></span> <br/>         | <span data-ttu-id="4c2fc-114">Orientation standard.</span><span class="sxs-lookup"><span data-stu-id="4c2fc-114">Standard Orientation.</span></span><br/>                                                                        |
| <span data-ttu-id="4c2fc-115">ReverseLandscape</span><span class="sxs-lookup"><span data-stu-id="4c2fc-115">ReverseLandscape</span></span> <br/> | <span data-ttu-id="4c2fc-116">Le contenu est pivoté sur la page 270 ? degrés CCW par rapport à l’orientation standard (portrait).</span><span class="sxs-lookup"><span data-stu-id="4c2fc-116">Content is rotated on the page 270??degrees CCW relative to standard (portrait) orientation.</span></span><br/> |
| <span data-ttu-id="4c2fc-117">ReversePortrait</span><span class="sxs-lookup"><span data-stu-id="4c2fc-117">ReversePortrait</span></span> <br/>  | <span data-ttu-id="4c2fc-118">Le contenu est pivoté sur la page 180 ? degrés par rapport à l’orientation standard (portrait).</span><span class="sxs-lookup"><span data-stu-id="4c2fc-118">Content is rotated on the page 180??degrees relative to standard (portrait) orientation.</span></span><br/>     |



 

-   [<span data-ttu-id="4c2fc-119">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="4c2fc-119">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="4c2fc-120">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="4c2fc-120">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="4c2fc-121">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="4c2fc-121">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="4c2fc-122">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="4c2fc-122">Element Information</span></span>



| <span data-ttu-id="4c2fc-123">Nom</span><span class="sxs-lookup"><span data-stu-id="4c2fc-123">Name</span></span> | <span data-ttu-id="4c2fc-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="4c2fc-124">Value</span></span> |
|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4c2fc-125">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="4c2fc-125">Element Type</span></span> <br/>   | <span data-ttu-id="4c2fc-126">Composant</span><span class="sxs-lookup"><span data-stu-id="4c2fc-126">Feature</span></span><br/>                                                                                                                                                                                      |
| <span data-ttu-id="4c2fc-127">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="4c2fc-127">Scoping Prefix</span></span> <br/> | <span data-ttu-id="4c2fc-128">Page</span><span class="sxs-lookup"><span data-stu-id="4c2fc-128">Page</span></span><br/>                                                                                                                                                                                         |
| <span data-ttu-id="4c2fc-129">Remarques</span><span class="sxs-lookup"><span data-stu-id="4c2fc-129">Notes</span></span> <br/>          | <span data-ttu-id="4c2fc-130">Si un périphérique d’impression ne peut prendre en charge qu’une seule direction paysage et que cette direction est dite « inversée », l’orientation de la page sera toujours considérée comme « paysage ».</span><span class="sxs-lookup"><span data-stu-id="4c2fc-130">If a Printer Device can only support one landscape direction and this direction is referred to as "Reverse Landscape", then the page orientation will still be considered to be "Landscape".</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="4c2fc-131">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="4c2fc-131">Structural Content</span></span>

<span data-ttu-id="4c2fc-132">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="4c2fc-132">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="4c2fc-133">Variables de structure</span><span class="sxs-lookup"><span data-stu-id="4c2fc-133">Structure Variables</span></span>

<span data-ttu-id="4c2fc-134">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="4c2fc-134">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="4c2fc-135">Nom</span><span class="sxs-lookup"><span data-stu-id="4c2fc-135">Name</span></span>                               | <span data-ttu-id="4c2fc-136">Type de données</span><span class="sxs-lookup"><span data-stu-id="4c2fc-136">Data type</span></span>         | <span data-ttu-id="4c2fc-137">Unité</span><span class="sxs-lookup"><span data-stu-id="4c2fc-137">Unit</span></span>                  | <span data-ttu-id="4c2fc-138">Valeurs prises en charge</span><span class="sxs-lookup"><span data-stu-id="4c2fc-138">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="4c2fc-139">Résumé</span><span class="sxs-lookup"><span data-stu-id="4c2fc-139">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="4c2fc-140">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="4c2fc-140">\_OptionName\_</span></span><br/>          | <span data-ttu-id="4c2fc-141">string</span><span class="sxs-lookup"><span data-stu-id="4c2fc-141">string</span></span><br/> | <span data-ttu-id="4c2fc-142">caractères</span><span class="sxs-lookup"><span data-stu-id="4c2fc-142">characters</span></span><br/> | <span data-ttu-id="4c2fc-143">Nom complet valide tel que défini par les [espaces de noms dans XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="4c2fc-143">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="4c2fc-144">Si aucun espace de noms n’est spécifié, l’espace de noms par défaut est utilisé.</span><span class="sxs-lookup"><span data-stu-id="4c2fc-144">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="4c2fc-145">Nom de l'option.</span><span class="sxs-lookup"><span data-stu-id="4c2fc-145">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="4c2fc-146">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="4c2fc-146">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="4c2fc-147">string</span><span class="sxs-lookup"><span data-stu-id="4c2fc-147">string</span></span><br/> | <span data-ttu-id="4c2fc-148">n/a</span><span class="sxs-lookup"><span data-stu-id="4c2fc-148">n/a</span></span><br/>        | <span data-ttu-id="4c2fc-149">True, False.</span><span class="sxs-lookup"><span data-stu-id="4c2fc-149">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="4c2fc-150">Définit une option qui, lorsqu’elle est sélectionnée, désactive cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="4c2fc-150">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="4c2fc-151">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="4c2fc-151">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="4c2fc-152">Les mots clés de schéma d’impression publics sont définis dans l' https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords espace de noms.</span><span class="sxs-lookup"><span data-stu-id="4c2fc-152">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="4c2fc-153">Le contenu de la Extensible Markup Language publique (XML) pour ce mot clé est défini ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="4c2fc-153">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="4c2fc-154">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4c2fc-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4c2fc-155">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="4c2fc-155">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




