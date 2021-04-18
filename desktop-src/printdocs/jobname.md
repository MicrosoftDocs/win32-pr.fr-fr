---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: 1e7b0681-a29b-4fd6-8518-dc9d0b716b12
title: JobName
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 161801e56a27e33cdf921cc07c93e59836d4dd90
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "106543143"
---
# <a name="jobname"></a><span data-ttu-id="cfe16-104">JobName</span><span class="sxs-lookup"><span data-stu-id="cfe16-104">JobName</span></span>

<span data-ttu-id="cfe16-105">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="cfe16-105">This topic is not current.</span></span> <span data-ttu-id="cfe16-106">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="cfe16-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="cfe16-107">Spécifie un nom descriptif pour le travail.</span><span class="sxs-lookup"><span data-stu-id="cfe16-107">Specifies a descriptive name for the job.</span></span>

-   [<span data-ttu-id="cfe16-108">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="cfe16-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="cfe16-109">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="cfe16-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="cfe16-110">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="cfe16-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="cfe16-111">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="cfe16-111">Element Information</span></span>



| <span data-ttu-id="cfe16-112">Nom</span><span class="sxs-lookup"><span data-stu-id="cfe16-112">Name</span></span>                       |                     |
|----------------------------|---------------------|
| <span data-ttu-id="cfe16-113">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="cfe16-113">Element Type</span></span> <br/>   | <span data-ttu-id="cfe16-114">Propriété</span><span class="sxs-lookup"><span data-stu-id="cfe16-114">Property</span></span><br/> |
| <span data-ttu-id="cfe16-115">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="cfe16-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="cfe16-116">Travail</span><span class="sxs-lookup"><span data-stu-id="cfe16-116">Job</span></span><br/>      |
| <span data-ttu-id="cfe16-117">Notes</span><span class="sxs-lookup"><span data-stu-id="cfe16-117">Notes</span></span> <br/>          | <span data-ttu-id="cfe16-118">Aucun</span><span class="sxs-lookup"><span data-stu-id="cfe16-118">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="cfe16-119">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="cfe16-119">Structural Content</span></span>

<span data-ttu-id="cfe16-120">La structure XML de cet élément est la suivante :</span><span class="sxs-lookup"><span data-stu-id="cfe16-120">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:Property name="psk:JobName">
    <psf:Value xsi:type="xs:string">_JobNameValue_</psf:Value>
</psf:Property>
```

## <a name="structure-variables"></a><span data-ttu-id="cfe16-121">Variables de structure</span><span class="sxs-lookup"><span data-stu-id="cfe16-121">Structure Variables</span></span>

<span data-ttu-id="cfe16-122">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="cfe16-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="cfe16-123">Nom</span><span class="sxs-lookup"><span data-stu-id="cfe16-123">Name</span></span>                        | <span data-ttu-id="cfe16-124">Type de données</span><span class="sxs-lookup"><span data-stu-id="cfe16-124">Data type</span></span>         | <span data-ttu-id="cfe16-125">Unité</span><span class="sxs-lookup"><span data-stu-id="cfe16-125">Unit</span></span> | <span data-ttu-id="cfe16-126">Valeurs prises en charge</span><span class="sxs-lookup"><span data-stu-id="cfe16-126">Supported values</span></span> | <span data-ttu-id="cfe16-127">Résumé</span><span class="sxs-lookup"><span data-stu-id="cfe16-127">Summary</span></span> |
|-----------------------------|-------------------|------|------------------|---------|
| <span data-ttu-id="cfe16-128">\_JobNameValue\_</span><span class="sxs-lookup"><span data-stu-id="cfe16-128">\_JobNameValue\_</span></span><br/> | <span data-ttu-id="cfe16-129">string</span><span class="sxs-lookup"><span data-stu-id="cfe16-129">string</span></span><br/> |      |                  |         |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="cfe16-130">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="cfe16-130">Extensible Markup Language (XML) Content</span></span>

``` syntax
<psf:Property name="psk:JobName">
    <psf:Value xsi:type="xs:string"></psf:Value> <!-- undefined -->
</psf:Property>
```

## <a name="related-topics"></a><span data-ttu-id="cfe16-131">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="cfe16-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cfe16-132">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="cfe16-132">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




