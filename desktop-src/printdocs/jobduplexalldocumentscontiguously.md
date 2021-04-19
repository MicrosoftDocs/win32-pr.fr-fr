---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: dd24166c-d5e2-420e-8a8c-e1a25728ab2f
title: JobDuplexAllDocumentsContiguously
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92c14e9c536d0ab24fafe308a8b11fa769842aab
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "106538448"
---
# <a name="jobduplexalldocumentscontiguously"></a><span data-ttu-id="6c51d-104">JobDuplexAllDocumentsContiguously</span><span class="sxs-lookup"><span data-stu-id="6c51d-104">JobDuplexAllDocumentsContiguously</span></span>

<span data-ttu-id="6c51d-105">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="6c51d-105">This topic is not current.</span></span> <span data-ttu-id="6c51d-106">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="6c51d-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="6c51d-107">Décrit les caractéristiques duplex de la sortie.</span><span class="sxs-lookup"><span data-stu-id="6c51d-107">Describes the duplex characteristics of the output.</span></span> <span data-ttu-id="6c51d-108">La fonctionnalité duplex permet l’impression des deux côtés du média.</span><span class="sxs-lookup"><span data-stu-id="6c51d-108">The duplex feature allows for printing on both sides of the media.</span></span> <span data-ttu-id="6c51d-109">Tous les documents du travail sont duplexés de manière contiguë.</span><span class="sxs-lookup"><span data-stu-id="6c51d-109">All Documents in the job are duplexed together contiguously.</span></span> <span data-ttu-id="6c51d-110">JobDuplexAllDocumentsContiguously et DocumentDuplex s’excluent mutuellement.</span><span class="sxs-lookup"><span data-stu-id="6c51d-110">JobDuplexAllDocumentsContiguously and DocumentDuplex are mutually exclusive.</span></span> <span data-ttu-id="6c51d-111">Il revient au pilote de déterminer la gestion des contraintes entre ces mots clés.</span><span class="sxs-lookup"><span data-stu-id="6c51d-111">It is up to the driver to determine constraint handling between these keywords.</span></span>

-   [<span data-ttu-id="6c51d-112">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="6c51d-112">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="6c51d-113">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="6c51d-113">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="6c51d-114">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="6c51d-114">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="6c51d-115">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="6c51d-115">Element Information</span></span>



| <span data-ttu-id="6c51d-116">Nom</span><span class="sxs-lookup"><span data-stu-id="6c51d-116">Name</span></span>                       |                    |
|----------------------------|--------------------|
| <span data-ttu-id="6c51d-117">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="6c51d-117">Element Type</span></span> <br/>   | <span data-ttu-id="6c51d-118">Fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="6c51d-118">Feature</span></span><br/> |
| <span data-ttu-id="6c51d-119">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="6c51d-119">Scoping Prefix</span></span> <br/> | <span data-ttu-id="6c51d-120">Travail</span><span class="sxs-lookup"><span data-stu-id="6c51d-120">Job</span></span><br/>     |
| <span data-ttu-id="6c51d-121">Notes</span><span class="sxs-lookup"><span data-stu-id="6c51d-121">Notes</span></span> <br/>          | <span data-ttu-id="6c51d-122">Aucun</span><span class="sxs-lookup"><span data-stu-id="6c51d-122">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="6c51d-123">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="6c51d-123">Structural Content</span></span>

<span data-ttu-id="6c51d-124">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="6c51d-124">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:JobDuplexAllDocumentsContiguously">
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

## <a name="structure-variables"></a><span data-ttu-id="6c51d-125">Variables de structure</span><span class="sxs-lookup"><span data-stu-id="6c51d-125">Structure Variables</span></span>

<span data-ttu-id="6c51d-126">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="6c51d-126">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="6c51d-127">Nom</span><span class="sxs-lookup"><span data-stu-id="6c51d-127">Name</span></span>                               | <span data-ttu-id="6c51d-128">Type de données</span><span class="sxs-lookup"><span data-stu-id="6c51d-128">Data type</span></span>         | <span data-ttu-id="6c51d-129">Unité</span><span class="sxs-lookup"><span data-stu-id="6c51d-129">Unit</span></span>                  | <span data-ttu-id="6c51d-130">Valeurs prises en charge</span><span class="sxs-lookup"><span data-stu-id="6c51d-130">Supported values</span></span>                                                                                                                                                             | <span data-ttu-id="6c51d-131">Résumé</span><span class="sxs-lookup"><span data-stu-id="6c51d-131">Summary</span></span>                                                                                                                                |
|------------------------------------|-------------------|-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c51d-132">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="6c51d-132">\_OptionName\_</span></span><br/>          | <span data-ttu-id="6c51d-133">string</span><span class="sxs-lookup"><span data-stu-id="6c51d-133">string</span></span><br/> | <span data-ttu-id="6c51d-134">caractères</span><span class="sxs-lookup"><span data-stu-id="6c51d-134">characters</span></span><br/> | <span data-ttu-id="6c51d-135">Nom complet valide tel que défini par https://www.w3.org/TR/1999/REC-xml-names-19990114/\#dt-qname .</span><span class="sxs-lookup"><span data-stu-id="6c51d-135">Valid fully qualified name as defined by https://www.w3.org/TR/1999/REC-xml-names-19990114/\#dt-qname.</span></span> <span data-ttu-id="6c51d-136">Si aucun espace de noms n’est spécifié, l’espace de noms par défaut est utilisé.</span><span class="sxs-lookup"><span data-stu-id="6c51d-136">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="6c51d-137">Nom de l'option.</span><span class="sxs-lookup"><span data-stu-id="6c51d-137">The name of the option.</span></span><br/>                                                                                                     |
| <span data-ttu-id="6c51d-138">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="6c51d-138">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="6c51d-139">string</span><span class="sxs-lookup"><span data-stu-id="6c51d-139">string</span></span><br/> | <span data-ttu-id="6c51d-140">n/a</span><span class="sxs-lookup"><span data-stu-id="6c51d-140">n/a</span></span><br/>        | <span data-ttu-id="6c51d-141">True, False.</span><span class="sxs-lookup"><span data-stu-id="6c51d-141">True, False.</span></span><br/>                                                                                                                                                      | <span data-ttu-id="6c51d-142">Définit une option qui, lorsqu’elle est sélectionnée, désactive cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="6c51d-142">Defines an Option which when selected would disable this feature.</span></span><br/>                                                           |
| <span data-ttu-id="6c51d-143">\_DuplexModeValue\_</span><span class="sxs-lookup"><span data-stu-id="6c51d-143">\_DuplexModeValue\_</span></span><br/>     | <span data-ttu-id="6c51d-144">string</span><span class="sxs-lookup"><span data-stu-id="6c51d-144">string</span></span><br/> | <span data-ttu-id="6c51d-145">n/a</span><span class="sxs-lookup"><span data-stu-id="6c51d-145">n/a</span></span><br/>        | <span data-ttu-id="6c51d-146">Automatique, manuel.</span><span class="sxs-lookup"><span data-stu-id="6c51d-146">Automatic, Manual.</span></span><br/>                                                                                                                                                | <span data-ttu-id="6c51d-147">Définit le mode duplex.</span><span class="sxs-lookup"><span data-stu-id="6c51d-147">Defines the duplex mode.</span></span> <span data-ttu-id="6c51d-148">Le duplex automatique est effectué par le matériel.</span><span class="sxs-lookup"><span data-stu-id="6c51d-148">Automatic duplex is performed by hardware.</span></span> <span data-ttu-id="6c51d-149">Le duplex manuel est effectué par les logiciels et l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="6c51d-149">Manual duplexing is performed by software and the user.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="6c51d-150">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="6c51d-150">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="6c51d-151">Les mots clés de schéma d’impression publics sont définis dans l' https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords espace de noms.</span><span class="sxs-lookup"><span data-stu-id="6c51d-151">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="6c51d-152">Le contenu de la Extensible Markup Language publique (XML) pour ce mot clé est défini ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="6c51d-152">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:JobDuplexAllDocumentsContiguously">
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

## <a name="related-topics"></a><span data-ttu-id="6c51d-153">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6c51d-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6c51d-154">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="6c51d-154">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




