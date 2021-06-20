---
description: En savoir plus sur l’élément JobName, qui spécifie un nom descriptif pour le travail. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: 1e7b0681-a29b-4fd6-8518-dc9d0b716b12
title: JobName
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bfb63a54e9501ff5dc45ff09a925396c168b20c
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408872"
---
# <a name="jobname"></a><span data-ttu-id="5aef4-104">JobName</span><span class="sxs-lookup"><span data-stu-id="5aef4-104">JobName</span></span>

<span data-ttu-id="5aef4-105">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="5aef4-105">This topic is not current.</span></span> <span data-ttu-id="5aef4-106">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="5aef4-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="5aef4-107">Spécifie un nom descriptif pour le travail.</span><span class="sxs-lookup"><span data-stu-id="5aef4-107">Specifies a descriptive name for the job.</span></span>

-   [<span data-ttu-id="5aef4-108">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="5aef4-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="5aef4-109">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="5aef4-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="5aef4-110">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="5aef4-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="5aef4-111">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="5aef4-111">Element Information</span></span>



| <span data-ttu-id="5aef4-112">Nom</span><span class="sxs-lookup"><span data-stu-id="5aef4-112">Name</span></span> | <span data-ttu-id="5aef4-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="5aef4-113">Value</span></span> |
|----------------------------|---------------------|
| <span data-ttu-id="5aef4-114">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="5aef4-114">Element Type</span></span> <br/>   | <span data-ttu-id="5aef4-115">Propriété</span><span class="sxs-lookup"><span data-stu-id="5aef4-115">Property</span></span><br/> |
| <span data-ttu-id="5aef4-116">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="5aef4-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="5aef4-117">Travail</span><span class="sxs-lookup"><span data-stu-id="5aef4-117">Job</span></span><br/>      |
| <span data-ttu-id="5aef4-118">Notes</span><span class="sxs-lookup"><span data-stu-id="5aef4-118">Notes</span></span> <br/>          | <span data-ttu-id="5aef4-119">Aucun</span><span class="sxs-lookup"><span data-stu-id="5aef4-119">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="5aef4-120">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="5aef4-120">Structural Content</span></span>

<span data-ttu-id="5aef4-121">La structure XML de cet élément est la suivante :</span><span class="sxs-lookup"><span data-stu-id="5aef4-121">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:Property name="psk:JobName">
    <psf:Value xsi:type="xs:string">_JobNameValue_</psf:Value>
</psf:Property>
```

## <a name="structure-variables"></a><span data-ttu-id="5aef4-122">Variables de structure</span><span class="sxs-lookup"><span data-stu-id="5aef4-122">Structure Variables</span></span>

<span data-ttu-id="5aef4-123">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="5aef4-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="5aef4-124">Nom</span><span class="sxs-lookup"><span data-stu-id="5aef4-124">Name</span></span>                        | <span data-ttu-id="5aef4-125">Type de données</span><span class="sxs-lookup"><span data-stu-id="5aef4-125">Data type</span></span>         | <span data-ttu-id="5aef4-126">Unité</span><span class="sxs-lookup"><span data-stu-id="5aef4-126">Unit</span></span> | <span data-ttu-id="5aef4-127">Valeurs prises en charge</span><span class="sxs-lookup"><span data-stu-id="5aef4-127">Supported values</span></span> | <span data-ttu-id="5aef4-128">Résumé</span><span class="sxs-lookup"><span data-stu-id="5aef4-128">Summary</span></span> |
|-----------------------------|-------------------|------|------------------|---------|
| <span data-ttu-id="5aef4-129">\_JobNameValue\_</span><span class="sxs-lookup"><span data-stu-id="5aef4-129">\_JobNameValue\_</span></span><br/> | <span data-ttu-id="5aef4-130">string</span><span class="sxs-lookup"><span data-stu-id="5aef4-130">string</span></span><br/> |      |                  |         |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="5aef4-131">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="5aef4-131">Extensible Markup Language (XML) Content</span></span>

``` syntax
<psf:Property name="psk:JobName">
    <psf:Value xsi:type="xs:string"></psf:Value> <!-- undefined -->
</psf:Property>
```

## <a name="related-topics"></a><span data-ttu-id="5aef4-132">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5aef4-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5aef4-133">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="5aef4-133">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




