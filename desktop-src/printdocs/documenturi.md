---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: 7926ae9b-e195-4391-9006-1eb4cf386f88
title: DocumentURI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0d339b1b469f276492f7989b0ed7951ca1edad8
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997066"
---
# <a name="documenturi"></a><span data-ttu-id="b6be8-104">DocumentURI</span><span class="sxs-lookup"><span data-stu-id="b6be8-104">DocumentURI</span></span>

<span data-ttu-id="b6be8-105">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="b6be8-105">This topic is not current.</span></span> <span data-ttu-id="b6be8-106">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="b6be8-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="b6be8-107">Spécifie un URI (Uniform Resource Identifier) pour le document.</span><span class="sxs-lookup"><span data-stu-id="b6be8-107">Specifies a uniform resource identifier (URI) for the document.</span></span>

-   [<span data-ttu-id="b6be8-108">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="b6be8-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="b6be8-109">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="b6be8-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="b6be8-110">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="b6be8-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="b6be8-111">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="b6be8-111">Element Information</span></span>



| <span data-ttu-id="b6be8-112">Nom</span><span class="sxs-lookup"><span data-stu-id="b6be8-112">Name</span></span> | <span data-ttu-id="b6be8-113">Value</span><span class="sxs-lookup"><span data-stu-id="b6be8-113">Value</span></span> |
|----------------------------|---------------------|
| <span data-ttu-id="b6be8-114">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="b6be8-114">Element Type</span></span> <br/>   | <span data-ttu-id="b6be8-115">Propriété</span><span class="sxs-lookup"><span data-stu-id="b6be8-115">Property</span></span><br/> |
| <span data-ttu-id="b6be8-116">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="b6be8-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="b6be8-117">Document</span><span class="sxs-lookup"><span data-stu-id="b6be8-117">Document</span></span><br/> |
| <span data-ttu-id="b6be8-118">Notes</span><span class="sxs-lookup"><span data-stu-id="b6be8-118">Notes</span></span> <br/>          | <span data-ttu-id="b6be8-119">Aucun</span><span class="sxs-lookup"><span data-stu-id="b6be8-119">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="b6be8-120">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="b6be8-120">Structural Content</span></span>

<span data-ttu-id="b6be8-121">La structure XML de cet élément est la suivante :</span><span class="sxs-lookup"><span data-stu-id="b6be8-121">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:Property name="psk:DocumentURI">
    <psf:Value xsi:type="xs:string">_DocumentURIValue_</psf:Value>
</psf:Property>
```

## <a name="structure-variables"></a><span data-ttu-id="b6be8-122">Variables de structure</span><span class="sxs-lookup"><span data-stu-id="b6be8-122">Structure Variables</span></span>

<span data-ttu-id="b6be8-123">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="b6be8-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="b6be8-124">Nom</span><span class="sxs-lookup"><span data-stu-id="b6be8-124">Name</span></span>                            | <span data-ttu-id="b6be8-125">Type de données</span><span class="sxs-lookup"><span data-stu-id="b6be8-125">Data type</span></span>         | <span data-ttu-id="b6be8-126">Unité</span><span class="sxs-lookup"><span data-stu-id="b6be8-126">Unit</span></span> | <span data-ttu-id="b6be8-127">Valeurs prises en charge</span><span class="sxs-lookup"><span data-stu-id="b6be8-127">Supported values</span></span> | <span data-ttu-id="b6be8-128">Résumé</span><span class="sxs-lookup"><span data-stu-id="b6be8-128">Summary</span></span> |
|---------------------------------|-------------------|------|------------------|---------|
| <span data-ttu-id="b6be8-129">\_DocumentURIValue\_</span><span class="sxs-lookup"><span data-stu-id="b6be8-129">\_DocumentURIValue\_</span></span><br/> | <span data-ttu-id="b6be8-130">string</span><span class="sxs-lookup"><span data-stu-id="b6be8-130">string</span></span><br/> |      |                  |         |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="b6be8-131">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="b6be8-131">Extensible Markup Language (XML) Content</span></span>

``` syntax
<psf:Property name="psk:DocumentURI">
    <psf:Value xsi:type="xs:string"></psf:Value> <!-- undefined -->
</psf:Property>
```

## <a name="related-topics"></a><span data-ttu-id="b6be8-132">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b6be8-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b6be8-133">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="b6be8-133">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




