---
description: En savoir plus sur l’élément configurable par l’utilisateur PageColorManagement. Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: 27408582-9c39-4d39-8314-a495d1c7766d
title: PageColorManagement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 685794f1c9bb64c8bb3e966c4ec03bcac8821369
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/09/2021
ms.locfileid: "113549227"
---
# <a name="pagecolormanagement"></a><span data-ttu-id="a2ba7-105">PageColorManagement</span><span class="sxs-lookup"><span data-stu-id="a2ba7-105">PageColorManagement</span></span>

<span data-ttu-id="a2ba7-106">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="a2ba7-106">This topic is not current.</span></span> <span data-ttu-id="a2ba7-107">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="a2ba7-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="a2ba7-108">Configure la gestion des couleurs pour la page actuelle.</span><span class="sxs-lookup"><span data-stu-id="a2ba7-108">Configures color management for the current page.</span></span> <span data-ttu-id="a2ba7-109">Cela est considéré comme automatique dans SHIM-DM \_ ICMMethod Add System.</span><span class="sxs-lookup"><span data-stu-id="a2ba7-109">This is considered automatic in SHIM - DM\_ICMMethod Add System.</span></span> <span data-ttu-id="a2ba7-110">Décrit le composant qui doit effectuer la gestion des couleurs (par exemple, le pilote).</span><span class="sxs-lookup"><span data-stu-id="a2ba7-110">Describes what component should perform color management (i.e. Driver).</span></span>

-   [<span data-ttu-id="a2ba7-111">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="a2ba7-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="a2ba7-112">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="a2ba7-112">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="a2ba7-113">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="a2ba7-113">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="a2ba7-114">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="a2ba7-114">Element Information</span></span>



| <span data-ttu-id="a2ba7-115">Nom</span><span class="sxs-lookup"><span data-stu-id="a2ba7-115">Name</span></span> | <span data-ttu-id="a2ba7-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="a2ba7-116">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="a2ba7-117">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="a2ba7-117">Element Type</span></span> <br/>   | <span data-ttu-id="a2ba7-118">Composant</span><span class="sxs-lookup"><span data-stu-id="a2ba7-118">Feature</span></span><br/> |
| <span data-ttu-id="a2ba7-119">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="a2ba7-119">Scoping Prefix</span></span> <br/> | <span data-ttu-id="a2ba7-120">Page</span><span class="sxs-lookup"><span data-stu-id="a2ba7-120">Page</span></span><br/>    |
| <span data-ttu-id="a2ba7-121">Notes</span><span class="sxs-lookup"><span data-stu-id="a2ba7-121">Notes</span></span> <br/>          | <span data-ttu-id="a2ba7-122">Aucun</span><span class="sxs-lookup"><span data-stu-id="a2ba7-122">None</span></span> <br/>   |



 

## <a name="structural-content"></a><span data-ttu-id="a2ba7-123">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="a2ba7-123">Structural Content</span></span>

<span data-ttu-id="a2ba7-124">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="a2ba7-124">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageColorManagement">
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

## <a name="structure-variables"></a><span data-ttu-id="a2ba7-125">Variables de structure</span><span class="sxs-lookup"><span data-stu-id="a2ba7-125">Structure Variables</span></span>

<span data-ttu-id="a2ba7-126">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="a2ba7-126">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="a2ba7-127">Nom</span><span class="sxs-lookup"><span data-stu-id="a2ba7-127">Name</span></span>                               | <span data-ttu-id="a2ba7-128">Type de données</span><span class="sxs-lookup"><span data-stu-id="a2ba7-128">Data type</span></span>         | <span data-ttu-id="a2ba7-129">Unité</span><span class="sxs-lookup"><span data-stu-id="a2ba7-129">Unit</span></span>                  | <span data-ttu-id="a2ba7-130">Valeurs prises en charge</span><span class="sxs-lookup"><span data-stu-id="a2ba7-130">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="a2ba7-131">Résumé</span><span class="sxs-lookup"><span data-stu-id="a2ba7-131">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="a2ba7-132">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="a2ba7-132">\_OptionName\_</span></span><br/>          | <span data-ttu-id="a2ba7-133">string</span><span class="sxs-lookup"><span data-stu-id="a2ba7-133">string</span></span><br/> | <span data-ttu-id="a2ba7-134">caractères</span><span class="sxs-lookup"><span data-stu-id="a2ba7-134">characters</span></span><br/> | <span data-ttu-id="a2ba7-135">Nom complet valide tel que défini par les [espaces de noms dans XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="a2ba7-135">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="a2ba7-136">Si aucun espace de noms n’est spécifié, l’espace de noms par défaut est utilisé.</span><span class="sxs-lookup"><span data-stu-id="a2ba7-136">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="a2ba7-137">Nom de l'option.</span><span class="sxs-lookup"><span data-stu-id="a2ba7-137">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="a2ba7-138">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="a2ba7-138">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="a2ba7-139">string</span><span class="sxs-lookup"><span data-stu-id="a2ba7-139">string</span></span><br/> | <span data-ttu-id="a2ba7-140">n/a</span><span class="sxs-lookup"><span data-stu-id="a2ba7-140">n/a</span></span><br/>        | <span data-ttu-id="a2ba7-141">True, False.</span><span class="sxs-lookup"><span data-stu-id="a2ba7-141">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="a2ba7-142">Définit une option qui, lorsqu’elle est sélectionnée, désactive cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="a2ba7-142">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="a2ba7-143">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="a2ba7-143">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="a2ba7-144">Les mots clés de schéma d’impression publics sont définis dans l' https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords espace de noms.</span><span class="sxs-lookup"><span data-stu-id="a2ba7-144">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="a2ba7-145">Le contenu de la Extensible Markup Language publique (XML) pour ce mot clé est défini ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="a2ba7-145">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageColorManagement">
  <psf:Property name="SelectionType">
    <psf:Value xsi:type="xs:string">PickOne</psf:Value>
  </psf:Property>
  <!-- Application has performed color management to the destination profile. -->
  <psf:Option name="psk:None" />
  <!--  Application has not performed color management and the device determines color management.-->
  <psf:Option name="psk:Device" />
  <!--  Application has not performed color management and the driver determines color management.-->
  <psf:Option name="psk:Driver" />
  <!--Color management is performed by the system. Not to be used when printing to XPSDrv print drivers -->
  <psf:Option name="psk:System" />
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="a2ba7-146">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a2ba7-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a2ba7-147">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="a2ba7-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




