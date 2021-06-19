---
description: En savoir plus sur l’élément JobURI, qui spécifie un URI (Uniform Resource Identifier) pour le document.
ms.assetid: c7abb657-6c9d-435a-a700-2eb0f14707c0
title: JobURI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecc145ac9a393c09ecab762b84e9ac7d58870ddf
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408612"
---
# <a name="joburi"></a><span data-ttu-id="b61f7-103">JobURI</span><span class="sxs-lookup"><span data-stu-id="b61f7-103">JobURI</span></span>

<span data-ttu-id="b61f7-104">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="b61f7-104">This topic is not current.</span></span> <span data-ttu-id="b61f7-105">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="b61f7-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="b61f7-106">Spécifie un URI (Uniform Resource Identifier) pour le document.</span><span class="sxs-lookup"><span data-stu-id="b61f7-106">Specifies a uniform resource identifier (URI) for the document.</span></span>

-   [<span data-ttu-id="b61f7-107">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="b61f7-107">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="b61f7-108">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="b61f7-108">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="b61f7-109">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="b61f7-109">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="b61f7-110">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="b61f7-110">Element Information</span></span>



| <span data-ttu-id="b61f7-111">Nom</span><span class="sxs-lookup"><span data-stu-id="b61f7-111">Name</span></span> | <span data-ttu-id="b61f7-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="b61f7-112">Value</span></span> |
|----------------------------|---------------------|
| <span data-ttu-id="b61f7-113">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="b61f7-113">Element Type</span></span> <br/>   | <span data-ttu-id="b61f7-114">Propriété</span><span class="sxs-lookup"><span data-stu-id="b61f7-114">Property</span></span><br/> |
| <span data-ttu-id="b61f7-115">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="b61f7-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="b61f7-116">Travail</span><span class="sxs-lookup"><span data-stu-id="b61f7-116">Job</span></span><br/>      |
| <span data-ttu-id="b61f7-117">Notes</span><span class="sxs-lookup"><span data-stu-id="b61f7-117">Notes</span></span> <br/>          | <span data-ttu-id="b61f7-118">Aucun</span><span class="sxs-lookup"><span data-stu-id="b61f7-118">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="b61f7-119">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="b61f7-119">Structural Content</span></span>

<span data-ttu-id="b61f7-120">La structure XML de cet élément est la suivante :</span><span class="sxs-lookup"><span data-stu-id="b61f7-120">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:Property name="psk:JobURI">
    <psf:Value xsi:type="xs:string">_JobURIValue_</psf:Value>
</psf:Property>
      
```

## <a name="structure-variables"></a><span data-ttu-id="b61f7-121">Variables de structure</span><span class="sxs-lookup"><span data-stu-id="b61f7-121">Structure Variables</span></span>

<span data-ttu-id="b61f7-122">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="b61f7-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="b61f7-123">Nom</span><span class="sxs-lookup"><span data-stu-id="b61f7-123">Name</span></span>                       | <span data-ttu-id="b61f7-124">Type de données</span><span class="sxs-lookup"><span data-stu-id="b61f7-124">Data type</span></span>         | <span data-ttu-id="b61f7-125">Unité</span><span class="sxs-lookup"><span data-stu-id="b61f7-125">Unit</span></span> | <span data-ttu-id="b61f7-126">Valeurs prises en charge</span><span class="sxs-lookup"><span data-stu-id="b61f7-126">Supported values</span></span> | <span data-ttu-id="b61f7-127">Résumé</span><span class="sxs-lookup"><span data-stu-id="b61f7-127">Summary</span></span> |
|----------------------------|-------------------|------|------------------|---------|
| <span data-ttu-id="b61f7-128">\_JobURIValue\_</span><span class="sxs-lookup"><span data-stu-id="b61f7-128">\_JobURIValue\_</span></span><br/> | <span data-ttu-id="b61f7-129">string</span><span class="sxs-lookup"><span data-stu-id="b61f7-129">string</span></span><br/> |      |                  |         |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="b61f7-130">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="b61f7-130">Extensible Markup Language (XML) Content</span></span>

``` syntax
<psf:Property name="psk:JobURI">
    <psf:Value xsi:type="xs:string"></psf:Value> <!-- undefined -->
</psf:Property>
```

## <a name="related-topics"></a><span data-ttu-id="b61f7-131">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b61f7-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b61f7-132">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="b61f7-132">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




