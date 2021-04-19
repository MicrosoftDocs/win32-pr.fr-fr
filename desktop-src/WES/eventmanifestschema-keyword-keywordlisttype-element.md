---
title: Keyword (élément KeywordListType)
description: Définit un mot clé qui identifie une catégorie d’événements. | Keyword (élément KeywordListType)
ms.assetid: c921eb01-f1b0-455c-8ff9-06895f1e40f9
keywords:
- Keyword, élément EventLog
topic_type:
- apiref
api_name:
- keyword
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f4b1b0b60502339db55c3227add9bb5a263200aa
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106523140"
---
# <a name="keyword-keywordlisttype-element"></a><span data-ttu-id="be91b-105">Keyword (élément KeywordListType)</span><span class="sxs-lookup"><span data-stu-id="be91b-105">keyword (KeywordListType) Element</span></span>

<span data-ttu-id="be91b-106">Définit un mot clé qui identifie une catégorie d’événements.</span><span class="sxs-lookup"><span data-stu-id="be91b-106">Defines a keyword that identifies a category of events.</span></span> <span data-ttu-id="be91b-107">Un mot clé est une balise que vous attachez à un événement pour regrouper des événements en fonction de leur utilisation.</span><span class="sxs-lookup"><span data-stu-id="be91b-107">A keyword is a tag that you attach to an event to group events based on their usage.</span></span>

``` syntax
<xs:element name="keyword"
    type="KeywordType"
 />
```

<span data-ttu-id="be91b-108">L’élément de **mot clé** est défini par le type complexe [**KeywordListType**](eventmanifestschema-keywordlisttype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="be91b-108">The **keyword** element is defined by the [**KeywordListType**](eventmanifestschema-keywordlisttype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="be91b-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="be91b-109">Requirements</span></span>



| <span data-ttu-id="be91b-110">Condition requise</span><span class="sxs-lookup"><span data-stu-id="be91b-110">Requirement</span></span> | <span data-ttu-id="be91b-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="be91b-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="be91b-112">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="be91b-112">Minimum supported client</span></span><br/> | <span data-ttu-id="be91b-113">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="be91b-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="be91b-114">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="be91b-114">Minimum supported server</span></span><br/> | <span data-ttu-id="be91b-115">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="be91b-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="be91b-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="be91b-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="be91b-117">**Éléments parents**</span><span class="sxs-lookup"><span data-stu-id="be91b-117">**Parent elements**</span></span>
</dt> <dt>

[<span data-ttu-id="be91b-118">**Mots clés (ProviderType)**</span><span class="sxs-lookup"><span data-stu-id="be91b-118">**keywords (ProviderType)**</span></span>](eventmanifestschema-keywords-providertype-element.md)
</dt> <dt>

[<span data-ttu-id="be91b-119">**Mots clés (type de données)**</span><span class="sxs-lookup"><span data-stu-id="be91b-119">**keywords (MetadataType)**</span></span>](eventmanifestschema-keywords-metadatatype-element.md)
</dt> </dl>

 

 





