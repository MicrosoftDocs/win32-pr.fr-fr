---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: 0658c808-f050-41f3-90b6-2a013b616b58
title: PageForceFrontSide
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f277e357cf59bca455102f6ca29bd66bc09455ee
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "104211352"
---
# <a name="pageforcefrontside"></a><span data-ttu-id="ac76a-104">PageForceFrontSide</span><span class="sxs-lookup"><span data-stu-id="ac76a-104">PageForceFrontSide</span></span>

<span data-ttu-id="ac76a-105">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="ac76a-105">This topic is not current.</span></span> <span data-ttu-id="ac76a-106">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="ac76a-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="ac76a-107">Force l’affichage de la sortie sur l’avant d’une feuille de média.</span><span class="sxs-lookup"><span data-stu-id="ac76a-107">Forces the output to appear on the front of a media sheet.</span></span> <span data-ttu-id="ac76a-108">S’applique aux feuilles de médias avec différentes surfaces de chaque côté.</span><span class="sxs-lookup"><span data-stu-id="ac76a-108">Relevant to media sheets with different surfaces on each side.</span></span> <span data-ttu-id="ac76a-109">Dans les cas où cette fonctionnalité interfère avec les options de traitement (par exemple, DocumentDuplex), PageForceFrontSide est prioritaire pour la page spécifique à laquelle la fonctionnalité s’applique.</span><span class="sxs-lookup"><span data-stu-id="ac76a-109">In cases where this feature interferes with processing options (such as DocumentDuplex), PageForceFrontSide takes precedence for the specific page to which the feature applies.</span></span>

-   [<span data-ttu-id="ac76a-110">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="ac76a-110">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="ac76a-111">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="ac76a-111">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="ac76a-112">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="ac76a-112">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="ac76a-113">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="ac76a-113">Element Information</span></span>



| <span data-ttu-id="ac76a-114">Nom</span><span class="sxs-lookup"><span data-stu-id="ac76a-114">Name</span></span>                       |                    |
|----------------------------|--------------------|
| <span data-ttu-id="ac76a-115">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="ac76a-115">Element Type</span></span> <br/>   | <span data-ttu-id="ac76a-116">Fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="ac76a-116">Feature</span></span><br/> |
| <span data-ttu-id="ac76a-117">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="ac76a-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="ac76a-118">Page</span><span class="sxs-lookup"><span data-stu-id="ac76a-118">Page</span></span><br/>    |
| <span data-ttu-id="ac76a-119">Notes</span><span class="sxs-lookup"><span data-stu-id="ac76a-119">Notes</span></span> <br/>          | <span data-ttu-id="ac76a-120">Aucun</span><span class="sxs-lookup"><span data-stu-id="ac76a-120">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="ac76a-121">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="ac76a-121">Structural Content</span></span>

<span data-ttu-id="ac76a-122">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="ac76a-122">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="ac76a-123">Variables de structure</span><span class="sxs-lookup"><span data-stu-id="ac76a-123">Structure Variables</span></span>

<span data-ttu-id="ac76a-124">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="ac76a-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="ac76a-125">Nom</span><span class="sxs-lookup"><span data-stu-id="ac76a-125">Name</span></span>                               | <span data-ttu-id="ac76a-126">Type de données</span><span class="sxs-lookup"><span data-stu-id="ac76a-126">Data type</span></span>         | <span data-ttu-id="ac76a-127">Unité</span><span class="sxs-lookup"><span data-stu-id="ac76a-127">Unit</span></span>                  | <span data-ttu-id="ac76a-128">Valeurs prises en charge</span><span class="sxs-lookup"><span data-stu-id="ac76a-128">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="ac76a-129">Résumé</span><span class="sxs-lookup"><span data-stu-id="ac76a-129">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="ac76a-130">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="ac76a-130">\_OptionName\_</span></span><br/>          | <span data-ttu-id="ac76a-131">string</span><span class="sxs-lookup"><span data-stu-id="ac76a-131">string</span></span><br/> | <span data-ttu-id="ac76a-132">caractères</span><span class="sxs-lookup"><span data-stu-id="ac76a-132">characters</span></span><br/> | <span data-ttu-id="ac76a-133">Nom complet valide tel que défini par les [espaces de noms dans XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="ac76a-133">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="ac76a-134">Si aucun espace de noms n’est spécifié, l’espace de noms par défaut est utilisé.</span><span class="sxs-lookup"><span data-stu-id="ac76a-134">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="ac76a-135">Nom de l'option.</span><span class="sxs-lookup"><span data-stu-id="ac76a-135">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="ac76a-136">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="ac76a-136">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="ac76a-137">string</span><span class="sxs-lookup"><span data-stu-id="ac76a-137">string</span></span><br/> | <span data-ttu-id="ac76a-138">n/a</span><span class="sxs-lookup"><span data-stu-id="ac76a-138">n/a</span></span><br/>        | <span data-ttu-id="ac76a-139">True, False.</span><span class="sxs-lookup"><span data-stu-id="ac76a-139">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="ac76a-140">Définit une option qui, lorsqu’elle est sélectionnée, désactive cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="ac76a-140">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="ac76a-141">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="ac76a-141">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="ac76a-142">Les mots clés de schéma d’impression publics sont définis dans l' https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords espace de noms.</span><span class="sxs-lookup"><span data-stu-id="ac76a-142">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="ac76a-143">Le contenu de la Extensible Markup Language publique (XML) pour ce mot clé est défini ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="ac76a-143">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="ac76a-144">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ac76a-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ac76a-145">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="ac76a-145">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




