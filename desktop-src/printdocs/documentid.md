---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: 6e7899e3-9b64-48bd-8683-aba627458f2a
title: DocumentID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d41bb96fe904a80210a951f700830604030eadd
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "106538268"
---
# <a name="documentid"></a><span data-ttu-id="aeddb-104">DocumentID</span><span class="sxs-lookup"><span data-stu-id="aeddb-104">DocumentID</span></span>

<span data-ttu-id="aeddb-105">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="aeddb-105">This topic is not current.</span></span> <span data-ttu-id="aeddb-106">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="aeddb-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="aeddb-107">Spécifie un ID unique pour le document.</span><span class="sxs-lookup"><span data-stu-id="aeddb-107">Specifies a unique ID for the document.</span></span>

-   [<span data-ttu-id="aeddb-108">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="aeddb-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="aeddb-109">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="aeddb-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="aeddb-110">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="aeddb-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="aeddb-111">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="aeddb-111">Element Information</span></span>



| <span data-ttu-id="aeddb-112">Nom</span><span class="sxs-lookup"><span data-stu-id="aeddb-112">Name</span></span>                       |                     |
|----------------------------|---------------------|
| <span data-ttu-id="aeddb-113">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="aeddb-113">Element Type</span></span> <br/>   | <span data-ttu-id="aeddb-114">Propriété</span><span class="sxs-lookup"><span data-stu-id="aeddb-114">Property</span></span><br/> |
| <span data-ttu-id="aeddb-115">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="aeddb-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="aeddb-116">Document</span><span class="sxs-lookup"><span data-stu-id="aeddb-116">Document</span></span><br/> |
| <span data-ttu-id="aeddb-117">Notes</span><span class="sxs-lookup"><span data-stu-id="aeddb-117">Notes</span></span> <br/>          | <span data-ttu-id="aeddb-118">Aucun</span><span class="sxs-lookup"><span data-stu-id="aeddb-118">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="aeddb-119">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="aeddb-119">Structural Content</span></span>

<span data-ttu-id="aeddb-120">La structure XML de cet élément est la suivante :</span><span class="sxs-lookup"><span data-stu-id="aeddb-120">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:Property name="psk:DocumentID">
    <psf:Value xsi:type="xs:string">_DocumentIDValue_</psf:Value>
</psf:Property>
```

## <a name="structure-variables"></a><span data-ttu-id="aeddb-121">Variables de structure</span><span class="sxs-lookup"><span data-stu-id="aeddb-121">Structure Variables</span></span>

<span data-ttu-id="aeddb-122">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="aeddb-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="aeddb-123">Nom</span><span class="sxs-lookup"><span data-stu-id="aeddb-123">Name</span></span>                           | <span data-ttu-id="aeddb-124">Type de données</span><span class="sxs-lookup"><span data-stu-id="aeddb-124">Data type</span></span>         | <span data-ttu-id="aeddb-125">Unité</span><span class="sxs-lookup"><span data-stu-id="aeddb-125">Unit</span></span> | <span data-ttu-id="aeddb-126">Valeurs prises en charge</span><span class="sxs-lookup"><span data-stu-id="aeddb-126">Supported values</span></span> | <span data-ttu-id="aeddb-127">Résumé</span><span class="sxs-lookup"><span data-stu-id="aeddb-127">Summary</span></span> |
|--------------------------------|-------------------|------|------------------|---------|
| <span data-ttu-id="aeddb-128">\_DocumentIDValue\_</span><span class="sxs-lookup"><span data-stu-id="aeddb-128">\_DocumentIDValue\_</span></span><br/> | <span data-ttu-id="aeddb-129">string</span><span class="sxs-lookup"><span data-stu-id="aeddb-129">string</span></span><br/> |      |                  |         |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="aeddb-130">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="aeddb-130">Extensible Markup Language (XML) Content</span></span>

``` syntax
<psf:Property name="psk:DocumentID">
    <psf:Value xsi:type="xs:string"></psf:Value> <!-- undefined -->
</psf:Property>
```

## <a name="related-topics"></a><span data-ttu-id="aeddb-131">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="aeddb-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aeddb-132">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="aeddb-132">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




