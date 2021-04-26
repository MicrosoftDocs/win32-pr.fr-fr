---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: c7abb657-6c9d-435a-a700-2eb0f14707c0
title: JobURI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3c80611a4e7dbd10f4841fae098578f0a8fdc96
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107993886"
---
# <a name="joburi"></a><span data-ttu-id="7df31-104">JobURI</span><span class="sxs-lookup"><span data-stu-id="7df31-104">JobURI</span></span>

<span data-ttu-id="7df31-105">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="7df31-105">This topic is not current.</span></span> <span data-ttu-id="7df31-106">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="7df31-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="7df31-107">Spécifie un URI (Uniform Resource Identifier) pour le document.</span><span class="sxs-lookup"><span data-stu-id="7df31-107">Specifies a uniform resource identifier (URI) for the document.</span></span>

-   [<span data-ttu-id="7df31-108">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="7df31-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="7df31-109">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="7df31-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="7df31-110">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="7df31-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="7df31-111">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="7df31-111">Element Information</span></span>



| <span data-ttu-id="7df31-112">Nom</span><span class="sxs-lookup"><span data-stu-id="7df31-112">Name</span></span> | <span data-ttu-id="7df31-113">Value</span><span class="sxs-lookup"><span data-stu-id="7df31-113">Value</span></span> |
|----------------------------|---------------------|
| <span data-ttu-id="7df31-114">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="7df31-114">Element Type</span></span> <br/>   | <span data-ttu-id="7df31-115">Propriété</span><span class="sxs-lookup"><span data-stu-id="7df31-115">Property</span></span><br/> |
| <span data-ttu-id="7df31-116">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="7df31-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="7df31-117">Travail</span><span class="sxs-lookup"><span data-stu-id="7df31-117">Job</span></span><br/>      |
| <span data-ttu-id="7df31-118">Notes</span><span class="sxs-lookup"><span data-stu-id="7df31-118">Notes</span></span> <br/>          | <span data-ttu-id="7df31-119">Aucun</span><span class="sxs-lookup"><span data-stu-id="7df31-119">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="7df31-120">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="7df31-120">Structural Content</span></span>

<span data-ttu-id="7df31-121">La structure XML de cet élément est la suivante :</span><span class="sxs-lookup"><span data-stu-id="7df31-121">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:Property name="psk:JobURI">
    <psf:Value xsi:type="xs:string">_JobURIValue_</psf:Value>
</psf:Property>
      
```

## <a name="structure-variables"></a><span data-ttu-id="7df31-122">Variables de structure</span><span class="sxs-lookup"><span data-stu-id="7df31-122">Structure Variables</span></span>

<span data-ttu-id="7df31-123">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="7df31-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="7df31-124">Nom</span><span class="sxs-lookup"><span data-stu-id="7df31-124">Name</span></span>                       | <span data-ttu-id="7df31-125">Type de données</span><span class="sxs-lookup"><span data-stu-id="7df31-125">Data type</span></span>         | <span data-ttu-id="7df31-126">Unité</span><span class="sxs-lookup"><span data-stu-id="7df31-126">Unit</span></span> | <span data-ttu-id="7df31-127">Valeurs prises en charge</span><span class="sxs-lookup"><span data-stu-id="7df31-127">Supported values</span></span> | <span data-ttu-id="7df31-128">Résumé</span><span class="sxs-lookup"><span data-stu-id="7df31-128">Summary</span></span> |
|----------------------------|-------------------|------|------------------|---------|
| <span data-ttu-id="7df31-129">\_JobURIValue\_</span><span class="sxs-lookup"><span data-stu-id="7df31-129">\_JobURIValue\_</span></span><br/> | <span data-ttu-id="7df31-130">string</span><span class="sxs-lookup"><span data-stu-id="7df31-130">string</span></span><br/> |      |                  |         |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="7df31-131">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="7df31-131">Extensible Markup Language (XML) Content</span></span>

``` syntax
<psf:Property name="psk:JobURI">
    <psf:Value xsi:type="xs:string"></psf:Value> <!-- undefined -->
</psf:Property>
```

## <a name="related-topics"></a><span data-ttu-id="7df31-132">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7df31-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7df31-133">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="7df31-133">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




