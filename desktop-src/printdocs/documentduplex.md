---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: dadc52e8-1733-4267-85aa-33d0ddd3dfa2
title: DocumentDuplex
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb2d65ac1007b8413f9e5e6cc12802e0ac27dac3
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "104211351"
---
# <a name="documentduplex"></a><span data-ttu-id="1878e-104">DocumentDuplex</span><span class="sxs-lookup"><span data-stu-id="1878e-104">DocumentDuplex</span></span>

<span data-ttu-id="1878e-105">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="1878e-105">This topic is not current.</span></span> <span data-ttu-id="1878e-106">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="1878e-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="1878e-107">Décrit les caractéristiques duplex de la sortie.</span><span class="sxs-lookup"><span data-stu-id="1878e-107">Describes the duplex characteristics of the output.</span></span> <span data-ttu-id="1878e-108">La fonctionnalité duplex permet l’impression des deux côtés du média.</span><span class="sxs-lookup"><span data-stu-id="1878e-108">The duplex feature allows for printing on both sides of the media.</span></span> <span data-ttu-id="1878e-109">Chaque document est séparé par un duplex.</span><span class="sxs-lookup"><span data-stu-id="1878e-109">Each document is duplexed separately.</span></span> <span data-ttu-id="1878e-110">DocumentDuplex et JobDuplexAllDocumentsContiguously s’excluent mutuellement.</span><span class="sxs-lookup"><span data-stu-id="1878e-110">DocumentDuplex and JobDuplexAllDocumentsContiguously are mutually exclusive.</span></span> <span data-ttu-id="1878e-111">Il revient au pilote de déterminer la gestion des contraintes entre ces mots clés.</span><span class="sxs-lookup"><span data-stu-id="1878e-111">It is up to the driver to determine constraint handling between these keywords.</span></span>

-   [<span data-ttu-id="1878e-112">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="1878e-112">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="1878e-113">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="1878e-113">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="1878e-114">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="1878e-114">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="1878e-115">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="1878e-115">Element Information</span></span>



| <span data-ttu-id="1878e-116">Nom</span><span class="sxs-lookup"><span data-stu-id="1878e-116">Name</span></span>                       |                     |
|----------------------------|---------------------|
| <span data-ttu-id="1878e-117">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="1878e-117">Element Type</span></span> <br/>   | <span data-ttu-id="1878e-118">Fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="1878e-118">Feature</span></span><br/>  |
| <span data-ttu-id="1878e-119">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="1878e-119">Scoping Prefix</span></span> <br/> | <span data-ttu-id="1878e-120">Document</span><span class="sxs-lookup"><span data-stu-id="1878e-120">Document</span></span><br/> |
| <span data-ttu-id="1878e-121">Notes</span><span class="sxs-lookup"><span data-stu-id="1878e-121">Notes</span></span> <br/>          | <span data-ttu-id="1878e-122">Aucun</span><span class="sxs-lookup"><span data-stu-id="1878e-122">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="1878e-123">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="1878e-123">Structural Content</span></span>

<span data-ttu-id="1878e-124">La structure XML de cet élément est la suivante :</span><span class="sxs-lookup"><span data-stu-id="1878e-124">The XML structure of this element is as follows:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="1878e-125">Variables de structure</span><span class="sxs-lookup"><span data-stu-id="1878e-125">Structure Variables</span></span>

<span data-ttu-id="1878e-126">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="1878e-126">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="1878e-127">Nom</span><span class="sxs-lookup"><span data-stu-id="1878e-127">Name</span></span>                               | <span data-ttu-id="1878e-128">Type de données</span><span class="sxs-lookup"><span data-stu-id="1878e-128">Data type</span></span>         | <span data-ttu-id="1878e-129">Unité</span><span class="sxs-lookup"><span data-stu-id="1878e-129">Unit</span></span>                  | <span data-ttu-id="1878e-130">Valeurs prises en charge</span><span class="sxs-lookup"><span data-stu-id="1878e-130">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="1878e-131">Résumé</span><span class="sxs-lookup"><span data-stu-id="1878e-131">Summary</span></span>                                                                                                                                |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1878e-132">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="1878e-132">\_OptionName\_</span></span><br/>          | <span data-ttu-id="1878e-133">string</span><span class="sxs-lookup"><span data-stu-id="1878e-133">string</span></span><br/> | <span data-ttu-id="1878e-134">caractères</span><span class="sxs-lookup"><span data-stu-id="1878e-134">characters</span></span><br/> | <span data-ttu-id="1878e-135">Nom complet valide tel que défini par les [espaces de noms dans XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="1878e-135">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="1878e-136">Si aucun espace de noms n’est spécifié, l’espace de noms par défaut est utilisé.</span><span class="sxs-lookup"><span data-stu-id="1878e-136">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="1878e-137">Nom de l'option.</span><span class="sxs-lookup"><span data-stu-id="1878e-137">The name of the option.</span></span><br/>                                                                                                     |
| <span data-ttu-id="1878e-138">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="1878e-138">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="1878e-139">string</span><span class="sxs-lookup"><span data-stu-id="1878e-139">string</span></span><br/> | <span data-ttu-id="1878e-140">n/a</span><span class="sxs-lookup"><span data-stu-id="1878e-140">n/a</span></span><br/>        | <span data-ttu-id="1878e-141">True, False.</span><span class="sxs-lookup"><span data-stu-id="1878e-141">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="1878e-142">Définit une option qui, lorsqu’elle est sélectionnée, désactive cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="1878e-142">Defines an Option which when selected would disable this feature.</span></span><br/>                                                           |
| <span data-ttu-id="1878e-143">\_DuplexModeValue\_</span><span class="sxs-lookup"><span data-stu-id="1878e-143">\_DuplexModeValue\_</span></span><br/>     | <span data-ttu-id="1878e-144">string</span><span class="sxs-lookup"><span data-stu-id="1878e-144">string</span></span><br/> | <span data-ttu-id="1878e-145">n/a</span><span class="sxs-lookup"><span data-stu-id="1878e-145">n/a</span></span><br/>        | <span data-ttu-id="1878e-146">Automatique, manuel.</span><span class="sxs-lookup"><span data-stu-id="1878e-146">Automatic, Manual.</span></span><br/>                                                                                                                                                         | <span data-ttu-id="1878e-147">Définit le mode duplex.</span><span class="sxs-lookup"><span data-stu-id="1878e-147">Defines the duplex mode.</span></span> <span data-ttu-id="1878e-148">Le duplex automatique est effectué par le matériel.</span><span class="sxs-lookup"><span data-stu-id="1878e-148">Automatic duplex is performed by hardware.</span></span> <span data-ttu-id="1878e-149">Le duplex manuel est effectué par les logiciels et l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="1878e-149">Manual duplexing is performed by software and the user.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="1878e-150">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="1878e-150">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="1878e-151">Les mots clés de schéma d’impression publics sont définis dans l' https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords espace de noms.</span><span class="sxs-lookup"><span data-stu-id="1878e-151">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="1878e-152">Le contenu de la Extensible Markup Language publique (XML) pour ce mot clé est défini ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="1878e-152">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="1878e-153">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1878e-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1878e-154">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="1878e-154">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




