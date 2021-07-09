---
description: Obtenir des informations sur la propriété DocumentURI. Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: 7926ae9b-e195-4391-9006-1eb4cf386f88
title: DocumentURI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cb4d1572417ac85e14c25c238be1d49611ba858
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/09/2021
ms.locfileid: "113548807"
---
# <a name="documenturi"></a><span data-ttu-id="d7eb8-105">DocumentURI</span><span class="sxs-lookup"><span data-stu-id="d7eb8-105">DocumentURI</span></span>

<span data-ttu-id="d7eb8-106">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="d7eb8-106">This topic is not current.</span></span> <span data-ttu-id="d7eb8-107">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="d7eb8-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="d7eb8-108">Spécifie un URI (Uniform Resource Identifier) pour le document.</span><span class="sxs-lookup"><span data-stu-id="d7eb8-108">Specifies a uniform resource identifier (URI) for the document.</span></span>

-   [<span data-ttu-id="d7eb8-109">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="d7eb8-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="d7eb8-110">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="d7eb8-110">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="d7eb8-111">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="d7eb8-111">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="d7eb8-112">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="d7eb8-112">Element Information</span></span>



| <span data-ttu-id="d7eb8-113">Nom</span><span class="sxs-lookup"><span data-stu-id="d7eb8-113">Name</span></span> | <span data-ttu-id="d7eb8-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="d7eb8-114">Value</span></span> |
|----------------------------|---------------------|
| <span data-ttu-id="d7eb8-115">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="d7eb8-115">Element Type</span></span> <br/>   | <span data-ttu-id="d7eb8-116">Propriété</span><span class="sxs-lookup"><span data-stu-id="d7eb8-116">Property</span></span><br/> |
| <span data-ttu-id="d7eb8-117">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="d7eb8-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="d7eb8-118">Document</span><span class="sxs-lookup"><span data-stu-id="d7eb8-118">Document</span></span><br/> |
| <span data-ttu-id="d7eb8-119">Notes</span><span class="sxs-lookup"><span data-stu-id="d7eb8-119">Notes</span></span> <br/>          | <span data-ttu-id="d7eb8-120">Aucun</span><span class="sxs-lookup"><span data-stu-id="d7eb8-120">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="d7eb8-121">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="d7eb8-121">Structural Content</span></span>

<span data-ttu-id="d7eb8-122">La structure XML de cet élément est la suivante :</span><span class="sxs-lookup"><span data-stu-id="d7eb8-122">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:Property name="psk:DocumentURI">
    <psf:Value xsi:type="xs:string">_DocumentURIValue_</psf:Value>
</psf:Property>
```

## <a name="structure-variables"></a><span data-ttu-id="d7eb8-123">Variables de structure</span><span class="sxs-lookup"><span data-stu-id="d7eb8-123">Structure Variables</span></span>

<span data-ttu-id="d7eb8-124">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="d7eb8-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="d7eb8-125">Nom</span><span class="sxs-lookup"><span data-stu-id="d7eb8-125">Name</span></span>                            | <span data-ttu-id="d7eb8-126">Type de données</span><span class="sxs-lookup"><span data-stu-id="d7eb8-126">Data type</span></span>         | <span data-ttu-id="d7eb8-127">Unité</span><span class="sxs-lookup"><span data-stu-id="d7eb8-127">Unit</span></span> | <span data-ttu-id="d7eb8-128">Valeurs prises en charge</span><span class="sxs-lookup"><span data-stu-id="d7eb8-128">Supported values</span></span> | <span data-ttu-id="d7eb8-129">Résumé</span><span class="sxs-lookup"><span data-stu-id="d7eb8-129">Summary</span></span> |
|---------------------------------|-------------------|------|------------------|---------|
| <span data-ttu-id="d7eb8-130">\_DocumentURIValue\_</span><span class="sxs-lookup"><span data-stu-id="d7eb8-130">\_DocumentURIValue\_</span></span><br/> | <span data-ttu-id="d7eb8-131">string</span><span class="sxs-lookup"><span data-stu-id="d7eb8-131">string</span></span><br/> |      |                  |         |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="d7eb8-132">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="d7eb8-132">Extensible Markup Language (XML) Content</span></span>

``` syntax
<psf:Property name="psk:DocumentURI">
    <psf:Value xsi:type="xs:string"></psf:Value> <!-- undefined -->
</psf:Property>
```

## <a name="related-topics"></a><span data-ttu-id="d7eb8-133">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d7eb8-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d7eb8-134">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="d7eb8-134">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




