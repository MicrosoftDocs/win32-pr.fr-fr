---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: 138a0ae5-160d-46f2-91ae-596d8892351a
title: JobID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd2d77d185ab7edc611a82f94a2ce92428d9f167
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998136"
---
# <a name="jobid"></a><span data-ttu-id="9bf6b-104">JobID</span><span class="sxs-lookup"><span data-stu-id="9bf6b-104">JobID</span></span>

<span data-ttu-id="9bf6b-105">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="9bf6b-105">This topic is not current.</span></span> <span data-ttu-id="9bf6b-106">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="9bf6b-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="9bf6b-107">Spécifie un ID unique pour le travail.</span><span class="sxs-lookup"><span data-stu-id="9bf6b-107">Specifies a unique ID for the job.</span></span>

-   [<span data-ttu-id="9bf6b-108">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="9bf6b-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="9bf6b-109">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="9bf6b-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="9bf6b-110">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="9bf6b-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="9bf6b-111">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="9bf6b-111">Element Information</span></span>



| <span data-ttu-id="9bf6b-112">Nom</span><span class="sxs-lookup"><span data-stu-id="9bf6b-112">Name</span></span> | <span data-ttu-id="9bf6b-113">Value</span><span class="sxs-lookup"><span data-stu-id="9bf6b-113">Value</span></span> |
|----------------------------|---------------------|
| <span data-ttu-id="9bf6b-114">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="9bf6b-114">Element Type</span></span> <br/>   | <span data-ttu-id="9bf6b-115">Propriété</span><span class="sxs-lookup"><span data-stu-id="9bf6b-115">Property</span></span><br/> |
| <span data-ttu-id="9bf6b-116">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="9bf6b-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="9bf6b-117">Travail</span><span class="sxs-lookup"><span data-stu-id="9bf6b-117">Job</span></span><br/>      |
| <span data-ttu-id="9bf6b-118">Notes</span><span class="sxs-lookup"><span data-stu-id="9bf6b-118">Notes</span></span> <br/>          | <span data-ttu-id="9bf6b-119">Aucun</span><span class="sxs-lookup"><span data-stu-id="9bf6b-119">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="9bf6b-120">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="9bf6b-120">Structural Content</span></span>

<span data-ttu-id="9bf6b-121">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="9bf6b-121">The XML structure of this element is:</span></span>

``` syntax
<psf:Property name="psk:JobID">
    <psf:Value xsi:type="xs:string">_JobIDValue_</psf:Value>
</psf:Property>
```

## <a name="structure-variables"></a><span data-ttu-id="9bf6b-122">Variables de structure</span><span class="sxs-lookup"><span data-stu-id="9bf6b-122">Structure Variables</span></span>

<span data-ttu-id="9bf6b-123">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="9bf6b-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="9bf6b-124">Nom</span><span class="sxs-lookup"><span data-stu-id="9bf6b-124">Name</span></span>                      | <span data-ttu-id="9bf6b-125">Type de données</span><span class="sxs-lookup"><span data-stu-id="9bf6b-125">Data type</span></span>         | <span data-ttu-id="9bf6b-126">Unité</span><span class="sxs-lookup"><span data-stu-id="9bf6b-126">Unit</span></span> | <span data-ttu-id="9bf6b-127">Valeurs prises en charge</span><span class="sxs-lookup"><span data-stu-id="9bf6b-127">Supported values</span></span> | <span data-ttu-id="9bf6b-128">Résumé</span><span class="sxs-lookup"><span data-stu-id="9bf6b-128">Summary</span></span> |
|---------------------------|-------------------|------|------------------|---------|
| <span data-ttu-id="9bf6b-129">\_JobIDValue\_</span><span class="sxs-lookup"><span data-stu-id="9bf6b-129">\_JobIDValue\_</span></span><br/> | <span data-ttu-id="9bf6b-130">string</span><span class="sxs-lookup"><span data-stu-id="9bf6b-130">string</span></span><br/> |      |                  |         |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="9bf6b-131">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="9bf6b-131">Extensible Markup Language (XML) Content</span></span>

``` syntax
<psf:Property name="psk:JobID">
    <psf:Value xsi:type="xs:string"></psf:Value> <!-- undefined -->
</psf:Property>
```

## <a name="related-topics"></a><span data-ttu-id="9bf6b-132">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9bf6b-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9bf6b-133">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="9bf6b-133">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




