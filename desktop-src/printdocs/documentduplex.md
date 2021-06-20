---
description: En savoir plus sur l’élément DocumentDuplex, qui décrit les caractéristiques duplex de la sortie. La fonctionnalité duplex permet l’impression des deux côtés du média.
ms.assetid: dadc52e8-1733-4267-85aa-33d0ddd3dfa2
title: DocumentDuplex
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c2ad8521835213594f10507ab6fd4b9cca24040
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409342"
---
# <a name="documentduplex"></a><span data-ttu-id="a51b1-104">DocumentDuplex</span><span class="sxs-lookup"><span data-stu-id="a51b1-104">DocumentDuplex</span></span>

<span data-ttu-id="a51b1-105">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="a51b1-105">This topic is not current.</span></span> <span data-ttu-id="a51b1-106">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="a51b1-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="a51b1-107">Décrit les caractéristiques duplex de la sortie.</span><span class="sxs-lookup"><span data-stu-id="a51b1-107">Describes the duplex characteristics of the output.</span></span> <span data-ttu-id="a51b1-108">La fonctionnalité duplex permet l’impression des deux côtés du média.</span><span class="sxs-lookup"><span data-stu-id="a51b1-108">The duplex feature allows for printing on both sides of the media.</span></span> <span data-ttu-id="a51b1-109">Chaque document est séparé par un duplex.</span><span class="sxs-lookup"><span data-stu-id="a51b1-109">Each document is duplexed separately.</span></span> <span data-ttu-id="a51b1-110">DocumentDuplex et JobDuplexAllDocumentsContiguously s’excluent mutuellement.</span><span class="sxs-lookup"><span data-stu-id="a51b1-110">DocumentDuplex and JobDuplexAllDocumentsContiguously are mutually exclusive.</span></span> <span data-ttu-id="a51b1-111">Il revient au pilote de déterminer la gestion des contraintes entre ces mots clés.</span><span class="sxs-lookup"><span data-stu-id="a51b1-111">It is up to the driver to determine constraint handling between these keywords.</span></span>

-   [<span data-ttu-id="a51b1-112">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="a51b1-112">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="a51b1-113">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="a51b1-113">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="a51b1-114">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="a51b1-114">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="a51b1-115">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="a51b1-115">Element Information</span></span>



| <span data-ttu-id="a51b1-116">Nom</span><span class="sxs-lookup"><span data-stu-id="a51b1-116">Name</span></span> | <span data-ttu-id="a51b1-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="a51b1-117">Value</span></span> |
|----------------------------|---------------------|
| <span data-ttu-id="a51b1-118">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="a51b1-118">Element Type</span></span> <br/>   | <span data-ttu-id="a51b1-119">Fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="a51b1-119">Feature</span></span><br/>  |
| <span data-ttu-id="a51b1-120">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="a51b1-120">Scoping Prefix</span></span> <br/> | <span data-ttu-id="a51b1-121">Document</span><span class="sxs-lookup"><span data-stu-id="a51b1-121">Document</span></span><br/> |
| <span data-ttu-id="a51b1-122">Notes</span><span class="sxs-lookup"><span data-stu-id="a51b1-122">Notes</span></span> <br/>          | <span data-ttu-id="a51b1-123">Aucun</span><span class="sxs-lookup"><span data-stu-id="a51b1-123">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="a51b1-124">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="a51b1-124">Structural Content</span></span>

<span data-ttu-id="a51b1-125">La structure XML de cet élément est la suivante :</span><span class="sxs-lookup"><span data-stu-id="a51b1-125">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:Feature name="psk:DocumentDuplex">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <psf:ScoredProperty name="psk:DuplexMode">
      <psf:Value xsi:type="xs:string">_DuplexModeValue_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>      
```

## <a name="structure-variables"></a><span data-ttu-id="a51b1-126">Variables de structure</span><span class="sxs-lookup"><span data-stu-id="a51b1-126">Structure Variables</span></span>

<span data-ttu-id="a51b1-127">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="a51b1-127">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="a51b1-128">Nom</span><span class="sxs-lookup"><span data-stu-id="a51b1-128">Name</span></span>                               | <span data-ttu-id="a51b1-129">Type de données</span><span class="sxs-lookup"><span data-stu-id="a51b1-129">Data type</span></span>         | <span data-ttu-id="a51b1-130">Unité</span><span class="sxs-lookup"><span data-stu-id="a51b1-130">Unit</span></span>                  | <span data-ttu-id="a51b1-131">Valeurs prises en charge</span><span class="sxs-lookup"><span data-stu-id="a51b1-131">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="a51b1-132">Résumé</span><span class="sxs-lookup"><span data-stu-id="a51b1-132">Summary</span></span>                                                                                                                                |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a51b1-133">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="a51b1-133">\_OptionName\_</span></span><br/>          | <span data-ttu-id="a51b1-134">string</span><span class="sxs-lookup"><span data-stu-id="a51b1-134">string</span></span><br/> | <span data-ttu-id="a51b1-135">caractères</span><span class="sxs-lookup"><span data-stu-id="a51b1-135">characters</span></span><br/> | <span data-ttu-id="a51b1-136">Nom complet valide tel que défini par les [espaces de noms dans XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="a51b1-136">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="a51b1-137">Si aucun espace de noms n’est spécifié, l’espace de noms par défaut est utilisé.</span><span class="sxs-lookup"><span data-stu-id="a51b1-137">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="a51b1-138">Nom de l'option.</span><span class="sxs-lookup"><span data-stu-id="a51b1-138">The name of the option.</span></span><br/>                                                                                                     |
| <span data-ttu-id="a51b1-139">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="a51b1-139">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="a51b1-140">string</span><span class="sxs-lookup"><span data-stu-id="a51b1-140">string</span></span><br/> | <span data-ttu-id="a51b1-141">n/a</span><span class="sxs-lookup"><span data-stu-id="a51b1-141">n/a</span></span><br/>        | <span data-ttu-id="a51b1-142">True, False.</span><span class="sxs-lookup"><span data-stu-id="a51b1-142">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="a51b1-143">Définit une option qui, lorsqu’elle est sélectionnée, désactive cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="a51b1-143">Defines an Option which when selected would disable this feature.</span></span><br/>                                                           |
| <span data-ttu-id="a51b1-144">\_DuplexModeValue\_</span><span class="sxs-lookup"><span data-stu-id="a51b1-144">\_DuplexModeValue\_</span></span><br/>     | <span data-ttu-id="a51b1-145">string</span><span class="sxs-lookup"><span data-stu-id="a51b1-145">string</span></span><br/> | <span data-ttu-id="a51b1-146">n/a</span><span class="sxs-lookup"><span data-stu-id="a51b1-146">n/a</span></span><br/>        | <span data-ttu-id="a51b1-147">Automatique, manuel.</span><span class="sxs-lookup"><span data-stu-id="a51b1-147">Automatic, Manual.</span></span><br/>                                                                                                                                                         | <span data-ttu-id="a51b1-148">Définit le mode duplex.</span><span class="sxs-lookup"><span data-stu-id="a51b1-148">Defines the duplex mode.</span></span> <span data-ttu-id="a51b1-149">Le duplex automatique est effectué par le matériel.</span><span class="sxs-lookup"><span data-stu-id="a51b1-149">Automatic duplex is performed by hardware.</span></span> <span data-ttu-id="a51b1-150">Le duplex manuel est effectué par les logiciels et l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="a51b1-150">Manual duplexing is performed by software and the user.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="a51b1-151">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="a51b1-151">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="a51b1-152">Les mots clés de schéma d’impression publics sont définis dans l' https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords espace de noms.</span><span class="sxs-lookup"><span data-stu-id="a51b1-152">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="a51b1-153">Le contenu de la Extensible Markup Language publique (XML) pour ce mot clé est défini ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="a51b1-153">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:DocumentDuplex">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies one sided printing. -->
  <psf:Option name="psk:OneSided" />
  <!-- Specifies two sided printing such that the page is flipped parallel to the MediaSizeWidth direction. -->
  <psf:Option name="psk:TwoSidedShortEdge">
    <psf:ScoredProperty name="psk:DuplexMode">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies two sided printing such that the page is flipped parallel to the MediaSizeHeight direction. -->
  <psf:Option name="psk:TwoSidedLongEdge">
    <psf:ScoredProperty name="psk:DuplexMode">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>    
```

## <a name="related-topics"></a><span data-ttu-id="a51b1-154">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a51b1-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a51b1-155">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="a51b1-155">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




