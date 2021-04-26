---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: 64fcd03f-8e0a-498d-82ea-0c69be0a3886
title: JobCollateAllDocuments
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53e7d3ba5b55ece6d7237846ae8ef969c0a3d17e
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998356"
---
# <a name="jobcollatealldocuments"></a><span data-ttu-id="5c69c-104">JobCollateAllDocuments</span><span class="sxs-lookup"><span data-stu-id="5c69c-104">JobCollateAllDocuments</span></span>

<span data-ttu-id="5c69c-105">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="5c69c-105">This topic is not current.</span></span> <span data-ttu-id="5c69c-106">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="5c69c-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="5c69c-107">Décrit les caractéristiques de classement de la sortie.</span><span class="sxs-lookup"><span data-stu-id="5c69c-107">Describes the collating characteristics of the output.</span></span> <span data-ttu-id="5c69c-108">Tous les documents de chaque travail individuel sont assemblés.</span><span class="sxs-lookup"><span data-stu-id="5c69c-108">All documents in each individual job are collated.</span></span> <span data-ttu-id="5c69c-109">DocumentCollate et JobCollateAlldocuments s’excluent mutuellement.</span><span class="sxs-lookup"><span data-stu-id="5c69c-109">DocumentCollate and JobCollateAlldocuments are mutually exclusive.</span></span> <span data-ttu-id="5c69c-110">Le comportement et l’implémentation de si ou seulement un de ces mots clés est implémenté sont laissés au pilote.</span><span class="sxs-lookup"><span data-stu-id="5c69c-110">The behavior and implementation of whether both or only one of these keywords is implemented is left to the driver.</span></span>

<span data-ttu-id="5c69c-111">Voici les règles qui doivent être suivies pour l’implémentation de COLLATE.</span><span class="sxs-lookup"><span data-stu-id="5c69c-111">The following are the rules that should be followed for Collate implementation.</span></span>

## <a name="element-definition-and-rules"></a><span data-ttu-id="5c69c-112">Définition et règles de l’élément</span><span class="sxs-lookup"><span data-stu-id="5c69c-112">Element Definition and Rules</span></span>

<span data-ttu-id="5c69c-113">Vous devez d’abord suivre les règles pour JobCollateAllDocument, puis appliquer les règles pour DocumentCollate pour que les scénarios fonctionnent.</span><span class="sxs-lookup"><span data-stu-id="5c69c-113">You must first follow the rules for JobCollateAllDocument, and then apply rules for DocumentCollate for the scenarios to work.</span></span> <span data-ttu-id="5c69c-114">Notez que, dans un paramètre de conversion PrintTicket en DEVMODE, où JobCollateAllDocuments n’est pas pris en charge par le pilote, il revient au pilote de choisir le comportement approprié à prendre (JobCollateAllDocuments = ON ou OFF).</span><span class="sxs-lookup"><span data-stu-id="5c69c-114">Note that in a PrintTicket to Devmode conversion setting, where JobCollateAllDocuments is not supported by the driver, it is up to the driver to choose the appropriate behavior to take (JobCollateAllDocuments = ON or OFF).</span></span> <span data-ttu-id="5c69c-115">En outre, le choix peut être modifié en fonction d’autres paramètres PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="5c69c-115">Also, the choice can be changed depending on other PrintTicket settings.</span></span>

### <a name="jobcollatealldocuments"></a><span data-ttu-id="5c69c-116">JobCollateAllDocuments</span><span class="sxs-lookup"><span data-stu-id="5c69c-116">JobCollateAllDocuments</span></span>

<span data-ttu-id="5c69c-117">SUR : Print (DocumentCopiesAllPages) de chaque document, répéter JobCopiesAllDocuments fois.</span><span class="sxs-lookup"><span data-stu-id="5c69c-117">ON: Print (DocumentCopiesAllPages) copies of each document, repeat JobCopiesAllDocuments times.</span></span>

<span data-ttu-id="5c69c-118">OFF : pour chaque document, Print (JobCopiesAllDocuments x DocumentCopiesAllPages) copie ensemble.</span><span class="sxs-lookup"><span data-stu-id="5c69c-118">OFF: For each document, print (JobCopiesAllDocuments x DocumentCopiesAllPages) copies together.</span></span>

### <a name="documentcollate"></a><span data-ttu-id="5c69c-119">DocumentCollate</span><span class="sxs-lookup"><span data-stu-id="5c69c-119">DocumentCollate</span></span>

<span data-ttu-id="5c69c-120">SUR : pour toutes les copies (JobCopiesAllDocuments x DocumentCopiesAllPages) d’un document imprimé de manière contiguë, classez les feuilles dans ce document.</span><span class="sxs-lookup"><span data-stu-id="5c69c-120">ON: For all copies (JobCopiesAllDocuments x DocumentCopiesAllPages) of a document printed contiguously, collate sheets in that document.</span></span>

<span data-ttu-id="5c69c-121">OFF : pour toutes les copies (JobCopiesAllDocuments x DocumentCopiesAllPages) imprimées de façon contiguë, imprimez toutes les copies (JobCopiesAllDocuments x DocumentCopiesAllPages) de chaque feuille ensemble.</span><span class="sxs-lookup"><span data-stu-id="5c69c-121">OFF: For all copies (JobCopiesAllDocuments x DocumentCopiesAllPages) printed contiguously, print all copies (JobCopiesAllDocuments x DocumentCopiesAllPages) of each sheet together.</span></span>

-   [<span data-ttu-id="5c69c-122">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="5c69c-122">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="5c69c-123">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="5c69c-123">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="5c69c-124">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="5c69c-124">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

### <a name="element-information"></a><span data-ttu-id="5c69c-125">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="5c69c-125">Element Information</span></span>



| <span data-ttu-id="5c69c-126">Nom</span><span class="sxs-lookup"><span data-stu-id="5c69c-126">Name</span></span> | <span data-ttu-id="5c69c-127">Value</span><span class="sxs-lookup"><span data-stu-id="5c69c-127">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="5c69c-128">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="5c69c-128">Element Type</span></span> <br/>   | <span data-ttu-id="5c69c-129">Fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="5c69c-129">Feature</span></span><br/> |
| <span data-ttu-id="5c69c-130">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="5c69c-130">Scoping Prefix</span></span> <br/> | <span data-ttu-id="5c69c-131">Travail</span><span class="sxs-lookup"><span data-stu-id="5c69c-131">Job</span></span><br/>     |
| <span data-ttu-id="5c69c-132">Notes</span><span class="sxs-lookup"><span data-stu-id="5c69c-132">Notes</span></span> <br/>          | <span data-ttu-id="5c69c-133">Aucun</span><span class="sxs-lookup"><span data-stu-id="5c69c-133">None</span></span><br/>    |



 

### <a name="structural-content"></a><span data-ttu-id="5c69c-134">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="5c69c-134">Structural Content</span></span>

<span data-ttu-id="5c69c-135">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="5c69c-135">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:JobCollateAllDocuments">
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

### <a name="structure-variables"></a><span data-ttu-id="5c69c-136">Variables de structure</span><span class="sxs-lookup"><span data-stu-id="5c69c-136">Structure Variables</span></span>

<span data-ttu-id="5c69c-137">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="5c69c-137">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="5c69c-138">Nom</span><span class="sxs-lookup"><span data-stu-id="5c69c-138">Name</span></span>                               | <span data-ttu-id="5c69c-139">Type de données</span><span class="sxs-lookup"><span data-stu-id="5c69c-139">Data type</span></span>         | <span data-ttu-id="5c69c-140">Unité</span><span class="sxs-lookup"><span data-stu-id="5c69c-140">Unit</span></span>                  | <span data-ttu-id="5c69c-141">Valeurs prises en charge</span><span class="sxs-lookup"><span data-stu-id="5c69c-141">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="5c69c-142">Résumé</span><span class="sxs-lookup"><span data-stu-id="5c69c-142">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="5c69c-143">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="5c69c-143">\_OptionName\_</span></span><br/>          | <span data-ttu-id="5c69c-144">string</span><span class="sxs-lookup"><span data-stu-id="5c69c-144">string</span></span><br/> | <span data-ttu-id="5c69c-145">caractères</span><span class="sxs-lookup"><span data-stu-id="5c69c-145">characters</span></span><br/> | <span data-ttu-id="5c69c-146">Nom complet valide tel que défini par les [espaces de noms dans XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="5c69c-146">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="5c69c-147">Si aucun espace de noms n’est spécifié, l’espace de noms par défaut est utilisé.</span><span class="sxs-lookup"><span data-stu-id="5c69c-147">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="5c69c-148">Nom de l'option.</span><span class="sxs-lookup"><span data-stu-id="5c69c-148">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="5c69c-149">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="5c69c-149">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="5c69c-150">string</span><span class="sxs-lookup"><span data-stu-id="5c69c-150">string</span></span><br/> | <span data-ttu-id="5c69c-151">n/a</span><span class="sxs-lookup"><span data-stu-id="5c69c-151">n/a</span></span><br/>        | <span data-ttu-id="5c69c-152">True, False.</span><span class="sxs-lookup"><span data-stu-id="5c69c-152">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="5c69c-153">Définit une option qui, lorsqu’elle est sélectionnée, désactive cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="5c69c-153">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

### <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="5c69c-154">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="5c69c-154">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="5c69c-155">Les mots clés de schéma d’impression publics sont définis dans l' https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords espace de noms.</span><span class="sxs-lookup"><span data-stu-id="5c69c-155">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="5c69c-156">Le contenu de la Extensible Markup Language publique (XML) pour ce mot clé est défini ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="5c69c-156">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:JobCollateAllDocuments">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies collating.  -->
  <psf:Option name="psk:Collated" />
  <!-- Specifies no collating. -->
  <psf:Option name="psk:Uncollated" />
</psf:Feature>
```

 

 




