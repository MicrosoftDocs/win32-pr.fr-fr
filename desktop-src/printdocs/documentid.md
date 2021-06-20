---
description: En savoir plus sur l’élément DocumentID, qui spécifie un ID unique pour le document. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: 6e7899e3-9b64-48bd-8683-aba627458f2a
title: DocumentID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b267fead0322351cde396bf2eb6d0efa8c523f0
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409282"
---
# <a name="documentid"></a><span data-ttu-id="3bafc-104">DocumentID</span><span class="sxs-lookup"><span data-stu-id="3bafc-104">DocumentID</span></span>

<span data-ttu-id="3bafc-105">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="3bafc-105">This topic is not current.</span></span> <span data-ttu-id="3bafc-106">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="3bafc-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="3bafc-107">Spécifie un ID unique pour le document.</span><span class="sxs-lookup"><span data-stu-id="3bafc-107">Specifies a unique ID for the document.</span></span>

-   [<span data-ttu-id="3bafc-108">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="3bafc-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="3bafc-109">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="3bafc-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="3bafc-110">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="3bafc-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="3bafc-111">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="3bafc-111">Element Information</span></span>



| <span data-ttu-id="3bafc-112">Nom</span><span class="sxs-lookup"><span data-stu-id="3bafc-112">Name</span></span> | <span data-ttu-id="3bafc-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="3bafc-113">Value</span></span> |
|----------------------------|---------------------|
| <span data-ttu-id="3bafc-114">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="3bafc-114">Element Type</span></span> <br/>   | <span data-ttu-id="3bafc-115">Propriété</span><span class="sxs-lookup"><span data-stu-id="3bafc-115">Property</span></span><br/> |
| <span data-ttu-id="3bafc-116">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="3bafc-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="3bafc-117">Document</span><span class="sxs-lookup"><span data-stu-id="3bafc-117">Document</span></span><br/> |
| <span data-ttu-id="3bafc-118">Notes</span><span class="sxs-lookup"><span data-stu-id="3bafc-118">Notes</span></span> <br/>          | <span data-ttu-id="3bafc-119">Aucun</span><span class="sxs-lookup"><span data-stu-id="3bafc-119">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="3bafc-120">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="3bafc-120">Structural Content</span></span>

<span data-ttu-id="3bafc-121">La structure XML de cet élément est la suivante :</span><span class="sxs-lookup"><span data-stu-id="3bafc-121">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:Property name="psk:DocumentID">
    <psf:Value xsi:type="xs:string">_DocumentIDValue_</psf:Value>
</psf:Property>
```

## <a name="structure-variables"></a><span data-ttu-id="3bafc-122">Variables de structure</span><span class="sxs-lookup"><span data-stu-id="3bafc-122">Structure Variables</span></span>

<span data-ttu-id="3bafc-123">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="3bafc-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="3bafc-124">Nom</span><span class="sxs-lookup"><span data-stu-id="3bafc-124">Name</span></span>                           | <span data-ttu-id="3bafc-125">Type de données</span><span class="sxs-lookup"><span data-stu-id="3bafc-125">Data type</span></span>         | <span data-ttu-id="3bafc-126">Unité</span><span class="sxs-lookup"><span data-stu-id="3bafc-126">Unit</span></span> | <span data-ttu-id="3bafc-127">Valeurs prises en charge</span><span class="sxs-lookup"><span data-stu-id="3bafc-127">Supported values</span></span> | <span data-ttu-id="3bafc-128">Résumé</span><span class="sxs-lookup"><span data-stu-id="3bafc-128">Summary</span></span> |
|--------------------------------|-------------------|------|------------------|---------|
| <span data-ttu-id="3bafc-129">\_DocumentIDValue\_</span><span class="sxs-lookup"><span data-stu-id="3bafc-129">\_DocumentIDValue\_</span></span><br/> | <span data-ttu-id="3bafc-130">string</span><span class="sxs-lookup"><span data-stu-id="3bafc-130">string</span></span><br/> |      |                  |         |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="3bafc-131">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="3bafc-131">Extensible Markup Language (XML) Content</span></span>

``` syntax
<psf:Property name="psk:DocumentID">
    <psf:Value xsi:type="xs:string"></psf:Value> <!-- undefined -->
</psf:Property>
```

## <a name="related-topics"></a><span data-ttu-id="3bafc-132">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3bafc-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3bafc-133">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="3bafc-133">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




