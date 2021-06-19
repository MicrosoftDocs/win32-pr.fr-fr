---
description: En savoir plus sur la propriété DocumentName, qui spécifie un nom descriptif pour le document.
ms.assetid: acb25fd6-6706-43ee-9ac0-539f20c13390
title: DocumentName
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d202ff1f5bac85fec3feac9f141834adfcd37e70
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409272"
---
# <a name="documentname"></a><span data-ttu-id="e3d9d-103">DocumentName</span><span class="sxs-lookup"><span data-stu-id="e3d9d-103">DocumentName</span></span>

<span data-ttu-id="e3d9d-104">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="e3d9d-104">This topic is not current.</span></span> <span data-ttu-id="e3d9d-105">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="e3d9d-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="e3d9d-106">Spécifie un nom descriptif pour le document.</span><span class="sxs-lookup"><span data-stu-id="e3d9d-106">Specifies a descriptive name for the document.</span></span>

-   [<span data-ttu-id="e3d9d-107">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="e3d9d-107">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="e3d9d-108">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="e3d9d-108">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="e3d9d-109">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="e3d9d-109">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="e3d9d-110">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="e3d9d-110">Element Information</span></span>



| <span data-ttu-id="e3d9d-111">Nom</span><span class="sxs-lookup"><span data-stu-id="e3d9d-111">Name</span></span> | <span data-ttu-id="e3d9d-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="e3d9d-112">Value</span></span> |
|----------------------------|---------------------|
| <span data-ttu-id="e3d9d-113">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="e3d9d-113">Element Type</span></span> <br/>   | <span data-ttu-id="e3d9d-114">Propriété</span><span class="sxs-lookup"><span data-stu-id="e3d9d-114">Property</span></span><br/> |
| <span data-ttu-id="e3d9d-115">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="e3d9d-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="e3d9d-116">Document</span><span class="sxs-lookup"><span data-stu-id="e3d9d-116">Document</span></span><br/> |
| <span data-ttu-id="e3d9d-117">Notes</span><span class="sxs-lookup"><span data-stu-id="e3d9d-117">Notes</span></span> <br/>          | <span data-ttu-id="e3d9d-118">Aucun</span><span class="sxs-lookup"><span data-stu-id="e3d9d-118">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="e3d9d-119">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="e3d9d-119">Structural Content</span></span>

<span data-ttu-id="e3d9d-120">La structure XML de cet élément est la suivante :</span><span class="sxs-lookup"><span data-stu-id="e3d9d-120">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:Property name="psk:DocumentName">
    <psf:Value xsi:type="xs:string">_DocumentNameValue_</psf:Value>
</psf:Property>
```

## <a name="structure-variables"></a><span data-ttu-id="e3d9d-121">Variables de structure</span><span class="sxs-lookup"><span data-stu-id="e3d9d-121">Structure Variables</span></span>

<span data-ttu-id="e3d9d-122">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="e3d9d-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="e3d9d-123">Nom</span><span class="sxs-lookup"><span data-stu-id="e3d9d-123">Name</span></span>                             | <span data-ttu-id="e3d9d-124">Type de données</span><span class="sxs-lookup"><span data-stu-id="e3d9d-124">Data type</span></span>         | <span data-ttu-id="e3d9d-125">Unité</span><span class="sxs-lookup"><span data-stu-id="e3d9d-125">Unit</span></span> | <span data-ttu-id="e3d9d-126">Valeurs prises en charge</span><span class="sxs-lookup"><span data-stu-id="e3d9d-126">Supported values</span></span> | <span data-ttu-id="e3d9d-127">Résumé</span><span class="sxs-lookup"><span data-stu-id="e3d9d-127">Summary</span></span> |
|----------------------------------|-------------------|------|------------------|---------|
| <span data-ttu-id="e3d9d-128">\_DocumentNameValue\_</span><span class="sxs-lookup"><span data-stu-id="e3d9d-128">\_DocumentNameValue\_</span></span><br/> | <span data-ttu-id="e3d9d-129">string</span><span class="sxs-lookup"><span data-stu-id="e3d9d-129">string</span></span><br/> |      |                  |         |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="e3d9d-130">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="e3d9d-130">Extensible Markup Language (XML) Content</span></span>

``` syntax
<psf:Property name="psk:DocumentName">
    <psf:Value xsi:type="xs:string"></psf:Value> <!-- undefined -->
</psf:Property>
```

## <a name="related-topics"></a><span data-ttu-id="e3d9d-131">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e3d9d-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e3d9d-132">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="e3d9d-132">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




