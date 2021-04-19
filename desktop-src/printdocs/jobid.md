---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: 138a0ae5-160d-46f2-91ae-596d8892351a
title: JobID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c182e5d0bfcfb395eb553570cca745b618fc56b5
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "106524787"
---
# <a name="jobid"></a><span data-ttu-id="d37b3-104">JobID</span><span class="sxs-lookup"><span data-stu-id="d37b3-104">JobID</span></span>

<span data-ttu-id="d37b3-105">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="d37b3-105">This topic is not current.</span></span> <span data-ttu-id="d37b3-106">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="d37b3-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="d37b3-107">Spécifie un ID unique pour le travail.</span><span class="sxs-lookup"><span data-stu-id="d37b3-107">Specifies a unique ID for the job.</span></span>

-   [<span data-ttu-id="d37b3-108">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="d37b3-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="d37b3-109">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="d37b3-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="d37b3-110">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="d37b3-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="d37b3-111">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="d37b3-111">Element Information</span></span>



| <span data-ttu-id="d37b3-112">Nom</span><span class="sxs-lookup"><span data-stu-id="d37b3-112">Name</span></span>                       |                     |
|----------------------------|---------------------|
| <span data-ttu-id="d37b3-113">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="d37b3-113">Element Type</span></span> <br/>   | <span data-ttu-id="d37b3-114">Propriété</span><span class="sxs-lookup"><span data-stu-id="d37b3-114">Property</span></span><br/> |
| <span data-ttu-id="d37b3-115">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="d37b3-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="d37b3-116">Travail</span><span class="sxs-lookup"><span data-stu-id="d37b3-116">Job</span></span><br/>      |
| <span data-ttu-id="d37b3-117">Notes</span><span class="sxs-lookup"><span data-stu-id="d37b3-117">Notes</span></span> <br/>          | <span data-ttu-id="d37b3-118">Aucun</span><span class="sxs-lookup"><span data-stu-id="d37b3-118">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="d37b3-119">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="d37b3-119">Structural Content</span></span>

<span data-ttu-id="d37b3-120">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="d37b3-120">The XML structure of this element is:</span></span>

``` syntax
<psf:Property name="psk:JobID">
    <psf:Value xsi:type="xs:string">_JobIDValue_</psf:Value>
</psf:Property>
```

## <a name="structure-variables"></a><span data-ttu-id="d37b3-121">Variables de structure</span><span class="sxs-lookup"><span data-stu-id="d37b3-121">Structure Variables</span></span>

<span data-ttu-id="d37b3-122">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="d37b3-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="d37b3-123">Nom</span><span class="sxs-lookup"><span data-stu-id="d37b3-123">Name</span></span>                      | <span data-ttu-id="d37b3-124">Type de données</span><span class="sxs-lookup"><span data-stu-id="d37b3-124">Data type</span></span>         | <span data-ttu-id="d37b3-125">Unité</span><span class="sxs-lookup"><span data-stu-id="d37b3-125">Unit</span></span> | <span data-ttu-id="d37b3-126">Valeurs prises en charge</span><span class="sxs-lookup"><span data-stu-id="d37b3-126">Supported values</span></span> | <span data-ttu-id="d37b3-127">Résumé</span><span class="sxs-lookup"><span data-stu-id="d37b3-127">Summary</span></span> |
|---------------------------|-------------------|------|------------------|---------|
| <span data-ttu-id="d37b3-128">\_JobIDValue\_</span><span class="sxs-lookup"><span data-stu-id="d37b3-128">\_JobIDValue\_</span></span><br/> | <span data-ttu-id="d37b3-129">string</span><span class="sxs-lookup"><span data-stu-id="d37b3-129">string</span></span><br/> |      |                  |         |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="d37b3-130">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="d37b3-130">Extensible Markup Language (XML) Content</span></span>

``` syntax
<psf:Property name="psk:JobID">
    <psf:Value xsi:type="xs:string"></psf:Value> <!-- undefined -->
</psf:Property>
```

## <a name="related-topics"></a><span data-ttu-id="d37b3-131">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d37b3-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d37b3-132">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="d37b3-132">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




