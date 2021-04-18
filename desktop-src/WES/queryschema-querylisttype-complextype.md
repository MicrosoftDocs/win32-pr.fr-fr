---
title: Type complexe QueryListType
description: Définit une liste de requêtes qui peuvent contenir un ensemble de sélecteurs et de suppressions utilisés pour inclure des événements dans ou exclure des événements du jeu de résultats.
ms.assetid: 3b9944e8-5913-4a77-a8fd-7efa43f3063f
keywords:
- QueryListType type complexe EventLog
topic_type:
- apiref
api_name:
- QueryListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 58cc6e83fb681f6244288088ea217097dd109c23
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509315"
---
# <a name="querylisttype-complex-type"></a><span data-ttu-id="6dfea-104">Type complexe QueryListType</span><span class="sxs-lookup"><span data-stu-id="6dfea-104">QueryListType Complex Type</span></span>

<span data-ttu-id="6dfea-105">Définit une liste de requêtes qui peuvent contenir un ensemble de sélecteurs et de suppressions utilisés pour inclure des événements dans ou exclure des événements du jeu de résultats.</span><span class="sxs-lookup"><span data-stu-id="6dfea-105">Defines a list of queries that can contain a set of selectors and suppressors that are used to include events in or exclude events from the result set.</span></span>

``` syntax
<xs:complexType name="QueryListType">
    <xs:sequence
        maxOccurs="unbounded"
    >
        <xs:element name="Query"
            type="QueryType"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="6dfea-106">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="6dfea-106">Child elements</span></span>



| <span data-ttu-id="6dfea-107">Élément</span><span class="sxs-lookup"><span data-stu-id="6dfea-107">Element</span></span>                                                  | <span data-ttu-id="6dfea-108">Type</span><span class="sxs-lookup"><span data-stu-id="6dfea-108">Type</span></span>                                                   | <span data-ttu-id="6dfea-109">Description</span><span class="sxs-lookup"><span data-stu-id="6dfea-109">Description</span></span>                                                                                                                     |
|----------------------------------------------------------|--------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6dfea-110">**Query**</span><span class="sxs-lookup"><span data-stu-id="6dfea-110">**Query**</span></span>](queryschema-query-querylisttype-element.md) | [<span data-ttu-id="6dfea-111">**Affectée**</span><span class="sxs-lookup"><span data-stu-id="6dfea-111">**QueryType**</span></span>](queryschema-querytype-complextype.md) | <span data-ttu-id="6dfea-112">Définit un ensemble de sélecteurs et de suppressions utilisés pour inclure des événements dans ou exclure des événements du jeu de résultats.</span><span class="sxs-lookup"><span data-stu-id="6dfea-112">Defines a set of selectors and suppressors that are used to include events in or exclude events from the result set.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="6dfea-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6dfea-113">Requirements</span></span>



| <span data-ttu-id="6dfea-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6dfea-114">Requirement</span></span> | <span data-ttu-id="6dfea-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="6dfea-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="6dfea-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6dfea-116">Minimum supported client</span></span><br/> | <span data-ttu-id="6dfea-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6dfea-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="6dfea-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6dfea-118">Minimum supported server</span></span><br/> | <span data-ttu-id="6dfea-119">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6dfea-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





