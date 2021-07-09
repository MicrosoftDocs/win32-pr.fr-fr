---
description: En savoir plus sur l’élément configurable par l’utilisateur PageForceFrontSide. Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: 0658c808-f050-41f3-90b6-2a013b616b58
title: PageForceFrontSide
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79f22e9ec52b7cee72e8f3a479d161e9abb765c4
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/09/2021
ms.locfileid: "113549187"
---
# <a name="pageforcefrontside"></a><span data-ttu-id="c57be-105">PageForceFrontSide</span><span class="sxs-lookup"><span data-stu-id="c57be-105">PageForceFrontSide</span></span>

<span data-ttu-id="c57be-106">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="c57be-106">This topic is not current.</span></span> <span data-ttu-id="c57be-107">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="c57be-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="c57be-108">Force l’affichage de la sortie sur l’avant d’une feuille de média.</span><span class="sxs-lookup"><span data-stu-id="c57be-108">Forces the output to appear on the front of a media sheet.</span></span> <span data-ttu-id="c57be-109">S’applique aux feuilles de médias avec différentes surfaces de chaque côté.</span><span class="sxs-lookup"><span data-stu-id="c57be-109">Relevant to media sheets with different surfaces on each side.</span></span> <span data-ttu-id="c57be-110">Dans les cas où cette fonctionnalité interfère avec les options de traitement (par exemple, DocumentDuplex), PageForceFrontSide est prioritaire pour la page spécifique à laquelle la fonctionnalité s’applique.</span><span class="sxs-lookup"><span data-stu-id="c57be-110">In cases where this feature interferes with processing options (such as DocumentDuplex), PageForceFrontSide takes precedence for the specific page to which the feature applies.</span></span>

-   [<span data-ttu-id="c57be-111">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="c57be-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="c57be-112">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="c57be-112">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="c57be-113">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="c57be-113">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="c57be-114">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="c57be-114">Element Information</span></span>



| <span data-ttu-id="c57be-115">Nom</span><span class="sxs-lookup"><span data-stu-id="c57be-115">Name</span></span> | <span data-ttu-id="c57be-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="c57be-116">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="c57be-117">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="c57be-117">Element Type</span></span> <br/>   | <span data-ttu-id="c57be-118">Composant</span><span class="sxs-lookup"><span data-stu-id="c57be-118">Feature</span></span><br/> |
| <span data-ttu-id="c57be-119">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="c57be-119">Scoping Prefix</span></span> <br/> | <span data-ttu-id="c57be-120">Page</span><span class="sxs-lookup"><span data-stu-id="c57be-120">Page</span></span><br/>    |
| <span data-ttu-id="c57be-121">Notes</span><span class="sxs-lookup"><span data-stu-id="c57be-121">Notes</span></span> <br/>          | <span data-ttu-id="c57be-122">Aucun</span><span class="sxs-lookup"><span data-stu-id="c57be-122">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="c57be-123">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="c57be-123">Structural Content</span></span>

<span data-ttu-id="c57be-124">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="c57be-124">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageForceFrontSide">
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

## <a name="structure-variables"></a><span data-ttu-id="c57be-125">Variables de structure</span><span class="sxs-lookup"><span data-stu-id="c57be-125">Structure Variables</span></span>

<span data-ttu-id="c57be-126">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="c57be-126">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="c57be-127">Nom</span><span class="sxs-lookup"><span data-stu-id="c57be-127">Name</span></span>                               | <span data-ttu-id="c57be-128">Type de données</span><span class="sxs-lookup"><span data-stu-id="c57be-128">Data type</span></span>         | <span data-ttu-id="c57be-129">Unité</span><span class="sxs-lookup"><span data-stu-id="c57be-129">Unit</span></span>                  | <span data-ttu-id="c57be-130">Valeurs prises en charge</span><span class="sxs-lookup"><span data-stu-id="c57be-130">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="c57be-131">Résumé</span><span class="sxs-lookup"><span data-stu-id="c57be-131">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="c57be-132">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="c57be-132">\_OptionName\_</span></span><br/>          | <span data-ttu-id="c57be-133">string</span><span class="sxs-lookup"><span data-stu-id="c57be-133">string</span></span><br/> | <span data-ttu-id="c57be-134">caractères</span><span class="sxs-lookup"><span data-stu-id="c57be-134">characters</span></span><br/> | <span data-ttu-id="c57be-135">Nom complet valide tel que défini par les [espaces de noms dans XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="c57be-135">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="c57be-136">Si aucun espace de noms n’est spécifié, l’espace de noms par défaut est utilisé.</span><span class="sxs-lookup"><span data-stu-id="c57be-136">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="c57be-137">Nom de l'option.</span><span class="sxs-lookup"><span data-stu-id="c57be-137">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="c57be-138">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="c57be-138">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="c57be-139">string</span><span class="sxs-lookup"><span data-stu-id="c57be-139">string</span></span><br/> | <span data-ttu-id="c57be-140">n/a</span><span class="sxs-lookup"><span data-stu-id="c57be-140">n/a</span></span><br/>        | <span data-ttu-id="c57be-141">True, False.</span><span class="sxs-lookup"><span data-stu-id="c57be-141">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="c57be-142">Définit une option qui, lorsqu’elle est sélectionnée, désactive cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="c57be-142">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="c57be-143">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="c57be-143">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="c57be-144">Les mots clés de schéma d’impression publics sont définis dans l' https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords espace de noms.</span><span class="sxs-lookup"><span data-stu-id="c57be-144">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="c57be-145">Le contenu de la Extensible Markup Language publique (XML) pour ce mot clé est défini ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="c57be-145">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageForceFrontSide">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies output is restricted to the front side of the sheet. -->
  <psf:Option name="psk:ForceFrontSide" />
  <!-- Specifies no output restrictions.  -->
  <psf:Option name="psk:None" />
</psf:Feature>    
```

## <a name="related-topics"></a><span data-ttu-id="c57be-146">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c57be-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c57be-147">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="c57be-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




