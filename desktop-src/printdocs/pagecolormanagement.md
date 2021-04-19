---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: 27408582-9c39-4d39-8314-a495d1c7766d
title: PageColorManagement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83ae8d161035d23149759345e8eb139dd3fb7a48
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "106531270"
---
# <a name="pagecolormanagement"></a><span data-ttu-id="0600e-104">PageColorManagement</span><span class="sxs-lookup"><span data-stu-id="0600e-104">PageColorManagement</span></span>

<span data-ttu-id="0600e-105">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="0600e-105">This topic is not current.</span></span> <span data-ttu-id="0600e-106">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="0600e-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="0600e-107">Configure la gestion des couleurs pour la page actuelle.</span><span class="sxs-lookup"><span data-stu-id="0600e-107">Configures color management for the current page.</span></span> <span data-ttu-id="0600e-108">Cela est considéré comme automatique dans SHIM-DM \_ ICMMethod Add System.</span><span class="sxs-lookup"><span data-stu-id="0600e-108">This is considered automatic in SHIM - DM\_ICMMethod Add System.</span></span> <span data-ttu-id="0600e-109">Décrit le composant qui doit effectuer la gestion des couleurs (par exemple, le pilote).</span><span class="sxs-lookup"><span data-stu-id="0600e-109">Describes what component should perform color management (i.e. Driver).</span></span>

-   [<span data-ttu-id="0600e-110">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="0600e-110">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="0600e-111">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="0600e-111">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="0600e-112">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="0600e-112">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="0600e-113">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="0600e-113">Element Information</span></span>



| <span data-ttu-id="0600e-114">Nom</span><span class="sxs-lookup"><span data-stu-id="0600e-114">Name</span></span>                       |                    |
|----------------------------|--------------------|
| <span data-ttu-id="0600e-115">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="0600e-115">Element Type</span></span> <br/>   | <span data-ttu-id="0600e-116">Fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="0600e-116">Feature</span></span><br/> |
| <span data-ttu-id="0600e-117">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="0600e-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="0600e-118">Page</span><span class="sxs-lookup"><span data-stu-id="0600e-118">Page</span></span><br/>    |
| <span data-ttu-id="0600e-119">Notes</span><span class="sxs-lookup"><span data-stu-id="0600e-119">Notes</span></span> <br/>          | <span data-ttu-id="0600e-120">Aucun</span><span class="sxs-lookup"><span data-stu-id="0600e-120">None</span></span> <br/>   |



 

## <a name="structural-content"></a><span data-ttu-id="0600e-121">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="0600e-121">Structural Content</span></span>

<span data-ttu-id="0600e-122">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="0600e-122">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="0600e-123">Variables de structure</span><span class="sxs-lookup"><span data-stu-id="0600e-123">Structure Variables</span></span>

<span data-ttu-id="0600e-124">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="0600e-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="0600e-125">Nom</span><span class="sxs-lookup"><span data-stu-id="0600e-125">Name</span></span>                               | <span data-ttu-id="0600e-126">Type de données</span><span class="sxs-lookup"><span data-stu-id="0600e-126">Data type</span></span>         | <span data-ttu-id="0600e-127">Unité</span><span class="sxs-lookup"><span data-stu-id="0600e-127">Unit</span></span>                  | <span data-ttu-id="0600e-128">Valeurs prises en charge</span><span class="sxs-lookup"><span data-stu-id="0600e-128">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="0600e-129">Résumé</span><span class="sxs-lookup"><span data-stu-id="0600e-129">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="0600e-130">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="0600e-130">\_OptionName\_</span></span><br/>          | <span data-ttu-id="0600e-131">string</span><span class="sxs-lookup"><span data-stu-id="0600e-131">string</span></span><br/> | <span data-ttu-id="0600e-132">caractères</span><span class="sxs-lookup"><span data-stu-id="0600e-132">characters</span></span><br/> | <span data-ttu-id="0600e-133">Nom complet valide tel que défini par les [espaces de noms dans XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="0600e-133">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="0600e-134">Si aucun espace de noms n’est spécifié, l’espace de noms par défaut est utilisé.</span><span class="sxs-lookup"><span data-stu-id="0600e-134">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="0600e-135">Nom de l'option.</span><span class="sxs-lookup"><span data-stu-id="0600e-135">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="0600e-136">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="0600e-136">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="0600e-137">string</span><span class="sxs-lookup"><span data-stu-id="0600e-137">string</span></span><br/> | <span data-ttu-id="0600e-138">n/a</span><span class="sxs-lookup"><span data-stu-id="0600e-138">n/a</span></span><br/>        | <span data-ttu-id="0600e-139">True, False.</span><span class="sxs-lookup"><span data-stu-id="0600e-139">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="0600e-140">Définit une option qui, lorsqu’elle est sélectionnée, désactive cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="0600e-140">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="0600e-141">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="0600e-141">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="0600e-142">Les mots clés de schéma d’impression publics sont définis dans l' https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords espace de noms.</span><span class="sxs-lookup"><span data-stu-id="0600e-142">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="0600e-143">Le contenu de la Extensible Markup Language publique (XML) pour ce mot clé est défini ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="0600e-143">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="0600e-144">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0600e-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0600e-145">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="0600e-145">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




