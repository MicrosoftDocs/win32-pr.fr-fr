---
description: En savoir plus sur l’élément JobID, qui spécifie un ID unique pour le travail. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: 138a0ae5-160d-46f2-91ae-596d8892351a
title: JobID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bfd17d068f34b56d45e4851c06b7ed1d9bd6fcc
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408882"
---
# <a name="jobid"></a><span data-ttu-id="1fad6-104">JobID</span><span class="sxs-lookup"><span data-stu-id="1fad6-104">JobID</span></span>

<span data-ttu-id="1fad6-105">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="1fad6-105">This topic is not current.</span></span> <span data-ttu-id="1fad6-106">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="1fad6-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="1fad6-107">Spécifie un ID unique pour le travail.</span><span class="sxs-lookup"><span data-stu-id="1fad6-107">Specifies a unique ID for the job.</span></span>

-   [<span data-ttu-id="1fad6-108">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="1fad6-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="1fad6-109">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="1fad6-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="1fad6-110">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="1fad6-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="1fad6-111">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="1fad6-111">Element Information</span></span>



| <span data-ttu-id="1fad6-112">Nom</span><span class="sxs-lookup"><span data-stu-id="1fad6-112">Name</span></span> | <span data-ttu-id="1fad6-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="1fad6-113">Value</span></span> |
|----------------------------|---------------------|
| <span data-ttu-id="1fad6-114">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="1fad6-114">Element Type</span></span> <br/>   | <span data-ttu-id="1fad6-115">Propriété</span><span class="sxs-lookup"><span data-stu-id="1fad6-115">Property</span></span><br/> |
| <span data-ttu-id="1fad6-116">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="1fad6-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="1fad6-117">Travail</span><span class="sxs-lookup"><span data-stu-id="1fad6-117">Job</span></span><br/>      |
| <span data-ttu-id="1fad6-118">Notes</span><span class="sxs-lookup"><span data-stu-id="1fad6-118">Notes</span></span> <br/>          | <span data-ttu-id="1fad6-119">Aucun</span><span class="sxs-lookup"><span data-stu-id="1fad6-119">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="1fad6-120">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="1fad6-120">Structural Content</span></span>

<span data-ttu-id="1fad6-121">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="1fad6-121">The XML structure of this element is:</span></span>

``` syntax
<psf:Property name="psk:JobID">
    <psf:Value xsi:type="xs:string">_JobIDValue_</psf:Value>
</psf:Property>
```

## <a name="structure-variables"></a><span data-ttu-id="1fad6-122">Variables de structure</span><span class="sxs-lookup"><span data-stu-id="1fad6-122">Structure Variables</span></span>

<span data-ttu-id="1fad6-123">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="1fad6-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="1fad6-124">Nom</span><span class="sxs-lookup"><span data-stu-id="1fad6-124">Name</span></span>                      | <span data-ttu-id="1fad6-125">Type de données</span><span class="sxs-lookup"><span data-stu-id="1fad6-125">Data type</span></span>         | <span data-ttu-id="1fad6-126">Unité</span><span class="sxs-lookup"><span data-stu-id="1fad6-126">Unit</span></span> | <span data-ttu-id="1fad6-127">Valeurs prises en charge</span><span class="sxs-lookup"><span data-stu-id="1fad6-127">Supported values</span></span> | <span data-ttu-id="1fad6-128">Résumé</span><span class="sxs-lookup"><span data-stu-id="1fad6-128">Summary</span></span> |
|---------------------------|-------------------|------|------------------|---------|
| <span data-ttu-id="1fad6-129">\_JobIDValue\_</span><span class="sxs-lookup"><span data-stu-id="1fad6-129">\_JobIDValue\_</span></span><br/> | <span data-ttu-id="1fad6-130">string</span><span class="sxs-lookup"><span data-stu-id="1fad6-130">string</span></span><br/> |      |                  |         |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="1fad6-131">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="1fad6-131">Extensible Markup Language (XML) Content</span></span>

``` syntax
<psf:Property name="psk:JobID">
    <psf:Value xsi:type="xs:string"></psf:Value> <!-- undefined -->
</psf:Property>
```

## <a name="related-topics"></a><span data-ttu-id="1fad6-132">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1fad6-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1fad6-133">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="1fad6-133">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




