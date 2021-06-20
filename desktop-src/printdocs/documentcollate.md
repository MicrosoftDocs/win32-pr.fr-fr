---
description: En savoir plus sur l’élément DocumentCollate, qui décrit les caractéristiques de classement de la sortie.
ms.assetid: 752cccf7-1f95-4597-b0e2-a96fd22ffeef
title: DocumentCollate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4c3036cc64265ea8f88bfcc46aea0149f8af5ad
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409452"
---
# <a name="documentcollate"></a><span data-ttu-id="7b182-103">DocumentCollate</span><span class="sxs-lookup"><span data-stu-id="7b182-103">DocumentCollate</span></span>

<span data-ttu-id="7b182-104">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="7b182-104">This topic is not current.</span></span> <span data-ttu-id="7b182-105">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="7b182-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="7b182-106">Décrit les caractéristiques de classement de la sortie.</span><span class="sxs-lookup"><span data-stu-id="7b182-106">Describes the collating characteristics of the output.</span></span> <span data-ttu-id="7b182-107">Toutes les pages de chaque document sont assemblées.</span><span class="sxs-lookup"><span data-stu-id="7b182-107">All pages in each individual document are collated.</span></span> <span data-ttu-id="7b182-108">DocumentCollate et JobCollateAlldocuments s’excluent mutuellement.</span><span class="sxs-lookup"><span data-stu-id="7b182-108">DocumentCollate and JobCollateAlldocuments are mutually exclusive.</span></span> <span data-ttu-id="7b182-109">Le comportement et l’implémentation de si ou seulement un de ces mots clés est implémenté sont laissés au pilote.</span><span class="sxs-lookup"><span data-stu-id="7b182-109">The behavior and implementation of whether both or only one of these keywords is implemented is left to the driver.</span></span>

<span data-ttu-id="7b182-110">Voici les règles qui doivent être suivies pour l’implémentation de COLLATE</span><span class="sxs-lookup"><span data-stu-id="7b182-110">The following are the rules which should be followed for Collate implementation</span></span>

## <a name="element-definition-and-rules"></a><span data-ttu-id="7b182-111">Définition et règles de l’élément</span><span class="sxs-lookup"><span data-stu-id="7b182-111">Element Definition and Rules</span></span>

<span data-ttu-id="7b182-112">Vous devez d’abord suivre les règles pour JobCollateAllDocument, puis appliquer les règles pour DocumentCollate pour que les scénarios fonctionnent.</span><span class="sxs-lookup"><span data-stu-id="7b182-112">You must first follow the rules for JobCollateAllDocument, and then apply rules for DocumentCollate for the scenarios to work.</span></span> <span data-ttu-id="7b182-113">Notez que, dans un paramètre de conversion PrintTicket en DEVMODE, où JobCollateAllDocuments n’est pas pris en charge par le pilote, il revient au pilote de choisir le comportement approprié à prendre (JobCollateAllDocuments = ON ou OFF).</span><span class="sxs-lookup"><span data-stu-id="7b182-113">Note that in a PrintTicket to Devmode conversion setting, where JobCollateAllDocuments is not supported by the driver, it is up to the driver to choose the appropriate behavior to take (JobCollateAllDocuments = ON or OFF).</span></span> <span data-ttu-id="7b182-114">En outre, le choix peut être modifié en fonction d’autres paramètres PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="7b182-114">Also, the choice can be changed depending on other PrintTicket settings.</span></span>

### <a name="jobcollatealldocuments"></a><span data-ttu-id="7b182-115">JobCollateAllDocuments</span><span class="sxs-lookup"><span data-stu-id="7b182-115">JobCollateAllDocuments</span></span>

<span data-ttu-id="7b182-116">SUR : Print (DocumentCopiesAllPages) de chaque document, répéter JobCopiesAllDocuments fois.</span><span class="sxs-lookup"><span data-stu-id="7b182-116">ON: Print (DocumentCopiesAllPages) copies of each document, repeat JobCopiesAllDocuments times.</span></span>

<span data-ttu-id="7b182-117">OFF : pour chaque document, Print (JobCopiesAllDocuments x DocumentCopiesAllPages) copie ensemble.</span><span class="sxs-lookup"><span data-stu-id="7b182-117">OFF: For each document, print (JobCopiesAllDocuments x DocumentCopiesAllPages) copies together.</span></span>

### <a name="documentcollate"></a><span data-ttu-id="7b182-118">DocumentCollate</span><span class="sxs-lookup"><span data-stu-id="7b182-118">DocumentCollate</span></span>

<span data-ttu-id="7b182-119">SUR : pour toutes les copies (JobCopiesAllDocuments x DocumentCopiesAllPages) d’un document imprimé de manière contiguë, classez les feuilles dans ce document.</span><span class="sxs-lookup"><span data-stu-id="7b182-119">ON: For all copies (JobCopiesAllDocuments x DocumentCopiesAllPages) of a document printed contiguously, collate sheets in that document.</span></span>

<span data-ttu-id="7b182-120">OFF : pour toutes les copies (JobCopiesAllDocuments x DocumentCopiesAllPages) imprimées de façon contiguë, imprimez toutes les copies (JobCopiesAllDocuments x DocumentCopiesAllPages) de chaque feuille ensemble.</span><span class="sxs-lookup"><span data-stu-id="7b182-120">OFF: For all copies (JobCopiesAllDocuments x DocumentCopiesAllPages) printed contiguously, print all copies (JobCopiesAllDocuments x DocumentCopiesAllPages) of each sheet together.</span></span>

-   [<span data-ttu-id="7b182-121">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="7b182-121">Element Information</span></span>](#element-information)

-   [<span data-ttu-id="7b182-122">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="7b182-122">Structural Content</span></span>](#structural-content)

-   [<span data-ttu-id="7b182-123">Contenu XML</span><span class="sxs-lookup"><span data-stu-id="7b182-123">XML Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="7b182-124">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="7b182-124">Element Information</span></span>



| <span data-ttu-id="7b182-125">Nom</span><span class="sxs-lookup"><span data-stu-id="7b182-125">Name</span></span> | <span data-ttu-id="7b182-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="7b182-126">Value</span></span> |
|----------------------------|---------------------|
| <span data-ttu-id="7b182-127">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="7b182-127">Element Type</span></span> <br/>   | <span data-ttu-id="7b182-128">Fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="7b182-128">Feature</span></span><br/>  |
| <span data-ttu-id="7b182-129">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="7b182-129">Scoping Prefix</span></span> <br/> | <span data-ttu-id="7b182-130">Document</span><span class="sxs-lookup"><span data-stu-id="7b182-130">Document</span></span><br/> |
| <span data-ttu-id="7b182-131">Notes</span><span class="sxs-lookup"><span data-stu-id="7b182-131">Notes</span></span> <br/>          | <span data-ttu-id="7b182-132">Aucun</span><span class="sxs-lookup"><span data-stu-id="7b182-132">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="7b182-133">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="7b182-133">Structural Content</span></span>

<span data-ttu-id="7b182-134">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="7b182-134">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:DocumentCollate">
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

## <a name="structure-variables"></a><span data-ttu-id="7b182-135">Variables de structure</span><span class="sxs-lookup"><span data-stu-id="7b182-135">Structure Variables</span></span>

<span data-ttu-id="7b182-136">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="7b182-136">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="7b182-137">Nom</span><span class="sxs-lookup"><span data-stu-id="7b182-137">Name</span></span>                               | <span data-ttu-id="7b182-138">Type de données</span><span class="sxs-lookup"><span data-stu-id="7b182-138">Data type</span></span>         | <span data-ttu-id="7b182-139">Unité</span><span class="sxs-lookup"><span data-stu-id="7b182-139">Unit</span></span>                  | <span data-ttu-id="7b182-140">Valeurs prises en charge</span><span class="sxs-lookup"><span data-stu-id="7b182-140">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="7b182-141">Résumé</span><span class="sxs-lookup"><span data-stu-id="7b182-141">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="7b182-142">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="7b182-142">\_OptionName\_</span></span><br/>          | <span data-ttu-id="7b182-143">string</span><span class="sxs-lookup"><span data-stu-id="7b182-143">string</span></span><br/> | <span data-ttu-id="7b182-144">caractères</span><span class="sxs-lookup"><span data-stu-id="7b182-144">characters</span></span><br/> | <span data-ttu-id="7b182-145">Nom complet valide tel que défini par les [espaces de noms dans XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="7b182-145">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="7b182-146">Si aucun espace de noms n’est spécifié, l’espace de noms par défaut est utilisé.</span><span class="sxs-lookup"><span data-stu-id="7b182-146">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="7b182-147">Nom de l'option.</span><span class="sxs-lookup"><span data-stu-id="7b182-147">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="7b182-148">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="7b182-148">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="7b182-149">string</span><span class="sxs-lookup"><span data-stu-id="7b182-149">string</span></span><br/> | <span data-ttu-id="7b182-150">n/a</span><span class="sxs-lookup"><span data-stu-id="7b182-150">n/a</span></span><br/>        | <span data-ttu-id="7b182-151">True, False.</span><span class="sxs-lookup"><span data-stu-id="7b182-151">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="7b182-152">Définit une option qui, lorsqu’elle est sélectionnée, désactive cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="7b182-152">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="7b182-153">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="7b182-153">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="7b182-154">Les mots clés de schéma d’impression publics sont définis dans l' https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords espace de noms.</span><span class="sxs-lookup"><span data-stu-id="7b182-154">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="7b182-155">Le contenu de la Extensible Markup Language publique (XML) pour ce mot clé est défini ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="7b182-155">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:DocumentCollate">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies collating.  -->
  <psf:Option name="psk:Collated" />
  <!-- Specifies no collating. -->
  <psf:Option name="psk:Uncollated" />
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="7b182-156">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7b182-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7b182-157">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="7b182-157">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




