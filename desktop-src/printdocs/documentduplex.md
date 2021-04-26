---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: dadc52e8-1733-4267-85aa-33d0ddd3dfa2
title: DocumentDuplex
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 959bbddbfa06e47fe2bc744af3ead0a72b13af7b
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998416"
---
# <a name="documentduplex"></a><span data-ttu-id="cc4fb-104">DocumentDuplex</span><span class="sxs-lookup"><span data-stu-id="cc4fb-104">DocumentDuplex</span></span>

<span data-ttu-id="cc4fb-105">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="cc4fb-105">This topic is not current.</span></span> <span data-ttu-id="cc4fb-106">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="cc4fb-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="cc4fb-107">Décrit les caractéristiques duplex de la sortie.</span><span class="sxs-lookup"><span data-stu-id="cc4fb-107">Describes the duplex characteristics of the output.</span></span> <span data-ttu-id="cc4fb-108">La fonctionnalité duplex permet l’impression des deux côtés du média.</span><span class="sxs-lookup"><span data-stu-id="cc4fb-108">The duplex feature allows for printing on both sides of the media.</span></span> <span data-ttu-id="cc4fb-109">Chaque document est séparé par un duplex.</span><span class="sxs-lookup"><span data-stu-id="cc4fb-109">Each document is duplexed separately.</span></span> <span data-ttu-id="cc4fb-110">DocumentDuplex et JobDuplexAllDocumentsContiguously s’excluent mutuellement.</span><span class="sxs-lookup"><span data-stu-id="cc4fb-110">DocumentDuplex and JobDuplexAllDocumentsContiguously are mutually exclusive.</span></span> <span data-ttu-id="cc4fb-111">Il revient au pilote de déterminer la gestion des contraintes entre ces mots clés.</span><span class="sxs-lookup"><span data-stu-id="cc4fb-111">It is up to the driver to determine constraint handling between these keywords.</span></span>

-   [<span data-ttu-id="cc4fb-112">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="cc4fb-112">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="cc4fb-113">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="cc4fb-113">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="cc4fb-114">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="cc4fb-114">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="cc4fb-115">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="cc4fb-115">Element Information</span></span>



| <span data-ttu-id="cc4fb-116">Nom</span><span class="sxs-lookup"><span data-stu-id="cc4fb-116">Name</span></span> | <span data-ttu-id="cc4fb-117">Value</span><span class="sxs-lookup"><span data-stu-id="cc4fb-117">Value</span></span> |
|----------------------------|---------------------|
| <span data-ttu-id="cc4fb-118">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="cc4fb-118">Element Type</span></span> <br/>   | <span data-ttu-id="cc4fb-119">Fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="cc4fb-119">Feature</span></span><br/>  |
| <span data-ttu-id="cc4fb-120">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="cc4fb-120">Scoping Prefix</span></span> <br/> | <span data-ttu-id="cc4fb-121">Document</span><span class="sxs-lookup"><span data-stu-id="cc4fb-121">Document</span></span><br/> |
| <span data-ttu-id="cc4fb-122">Notes</span><span class="sxs-lookup"><span data-stu-id="cc4fb-122">Notes</span></span> <br/>          | <span data-ttu-id="cc4fb-123">Aucun</span><span class="sxs-lookup"><span data-stu-id="cc4fb-123">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="cc4fb-124">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="cc4fb-124">Structural Content</span></span>

<span data-ttu-id="cc4fb-125">La structure XML de cet élément est la suivante :</span><span class="sxs-lookup"><span data-stu-id="cc4fb-125">The XML structure of this element is as follows:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="cc4fb-126">Variables de structure</span><span class="sxs-lookup"><span data-stu-id="cc4fb-126">Structure Variables</span></span>

<span data-ttu-id="cc4fb-127">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="cc4fb-127">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="cc4fb-128">Nom</span><span class="sxs-lookup"><span data-stu-id="cc4fb-128">Name</span></span>                               | <span data-ttu-id="cc4fb-129">Type de données</span><span class="sxs-lookup"><span data-stu-id="cc4fb-129">Data type</span></span>         | <span data-ttu-id="cc4fb-130">Unité</span><span class="sxs-lookup"><span data-stu-id="cc4fb-130">Unit</span></span>                  | <span data-ttu-id="cc4fb-131">Valeurs prises en charge</span><span class="sxs-lookup"><span data-stu-id="cc4fb-131">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="cc4fb-132">Résumé</span><span class="sxs-lookup"><span data-stu-id="cc4fb-132">Summary</span></span>                                                                                                                                |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc4fb-133">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="cc4fb-133">\_OptionName\_</span></span><br/>          | <span data-ttu-id="cc4fb-134">string</span><span class="sxs-lookup"><span data-stu-id="cc4fb-134">string</span></span><br/> | <span data-ttu-id="cc4fb-135">caractères</span><span class="sxs-lookup"><span data-stu-id="cc4fb-135">characters</span></span><br/> | <span data-ttu-id="cc4fb-136">Nom complet valide tel que défini par les [espaces de noms dans XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="cc4fb-136">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="cc4fb-137">Si aucun espace de noms n’est spécifié, l’espace de noms par défaut est utilisé.</span><span class="sxs-lookup"><span data-stu-id="cc4fb-137">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="cc4fb-138">Nom de l'option.</span><span class="sxs-lookup"><span data-stu-id="cc4fb-138">The name of the option.</span></span><br/>                                                                                                     |
| <span data-ttu-id="cc4fb-139">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="cc4fb-139">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="cc4fb-140">string</span><span class="sxs-lookup"><span data-stu-id="cc4fb-140">string</span></span><br/> | <span data-ttu-id="cc4fb-141">n/a</span><span class="sxs-lookup"><span data-stu-id="cc4fb-141">n/a</span></span><br/>        | <span data-ttu-id="cc4fb-142">True, False.</span><span class="sxs-lookup"><span data-stu-id="cc4fb-142">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="cc4fb-143">Définit une option qui, lorsqu’elle est sélectionnée, désactive cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="cc4fb-143">Defines an Option which when selected would disable this feature.</span></span><br/>                                                           |
| <span data-ttu-id="cc4fb-144">\_DuplexModeValue\_</span><span class="sxs-lookup"><span data-stu-id="cc4fb-144">\_DuplexModeValue\_</span></span><br/>     | <span data-ttu-id="cc4fb-145">string</span><span class="sxs-lookup"><span data-stu-id="cc4fb-145">string</span></span><br/> | <span data-ttu-id="cc4fb-146">n/a</span><span class="sxs-lookup"><span data-stu-id="cc4fb-146">n/a</span></span><br/>        | <span data-ttu-id="cc4fb-147">Automatique, manuel.</span><span class="sxs-lookup"><span data-stu-id="cc4fb-147">Automatic, Manual.</span></span><br/>                                                                                                                                                         | <span data-ttu-id="cc4fb-148">Définit le mode duplex.</span><span class="sxs-lookup"><span data-stu-id="cc4fb-148">Defines the duplex mode.</span></span> <span data-ttu-id="cc4fb-149">Le duplex automatique est effectué par le matériel.</span><span class="sxs-lookup"><span data-stu-id="cc4fb-149">Automatic duplex is performed by hardware.</span></span> <span data-ttu-id="cc4fb-150">Le duplex manuel est effectué par les logiciels et l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="cc4fb-150">Manual duplexing is performed by software and the user.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="cc4fb-151">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="cc4fb-151">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="cc4fb-152">Les mots clés de schéma d’impression publics sont définis dans l' https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords espace de noms.</span><span class="sxs-lookup"><span data-stu-id="cc4fb-152">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="cc4fb-153">Le contenu de la Extensible Markup Language publique (XML) pour ce mot clé est défini ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="cc4fb-153">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="cc4fb-154">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="cc4fb-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cc4fb-155">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="cc4fb-155">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




