---
title: Type complexe KeywordListType
description: Définit une liste de mots clés qui classent les événements. | Type complexe KeywordListType
ms.assetid: 7aeb5ca1-b23f-40f5-a77b-894deaf9c6bb
keywords:
- KeywordListType type complexe EventLog
topic_type:
- apiref
api_name:
- KeywordListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7132e2e85015aaf9d38adbd6278ea4d3e1296446
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106537212"
---
# <a name="keywordlisttype-complex-type"></a><span data-ttu-id="16a89-105">Type complexe KeywordListType</span><span class="sxs-lookup"><span data-stu-id="16a89-105">KeywordListType Complex Type</span></span>

<span data-ttu-id="16a89-106">Définit une liste de mots clés qui classent les événements.</span><span class="sxs-lookup"><span data-stu-id="16a89-106">Defines a list of keywords that categorize events.</span></span>

``` syntax
<xs:complexType name="KeywordListType">
    <xs:sequence>
        <xs:element name="keyword"
            type="KeywordType"
            minOccurs="0"
            maxOccurs="unbounded"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="16a89-107">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="16a89-107">Child elements</span></span>



| <span data-ttu-id="16a89-108">Élément</span><span class="sxs-lookup"><span data-stu-id="16a89-108">Element</span></span>                                                                | <span data-ttu-id="16a89-109">Type</span><span class="sxs-lookup"><span data-stu-id="16a89-109">Type</span></span>                                                               | <span data-ttu-id="16a89-110">Description</span><span class="sxs-lookup"><span data-stu-id="16a89-110">Description</span></span>                                                                                                  |
|------------------------------------------------------------------------|--------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="16a89-111">**keyword**</span><span class="sxs-lookup"><span data-stu-id="16a89-111">**keyword**</span></span>](eventmanifestschema-keyword-keywordlisttype-element.md) | [<span data-ttu-id="16a89-112">**KeywordType**</span><span class="sxs-lookup"><span data-stu-id="16a89-112">**KeywordType**</span></span>](eventmanifestschema-keywordtype-complextype.md) | <span data-ttu-id="16a89-113">Définit un mot clé qui identifie une catégorie d’événements.</span><span class="sxs-lookup"><span data-stu-id="16a89-113">Defines a keyword that identifies a category of events.</span></span> <span data-ttu-id="16a89-114">Vous pouvez spécifier un maximum de 48 Mots-clés.</span><span class="sxs-lookup"><span data-stu-id="16a89-114">You can specify a maximum of 48 keywords.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="16a89-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="16a89-115">Requirements</span></span>



| <span data-ttu-id="16a89-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="16a89-116">Requirement</span></span> | <span data-ttu-id="16a89-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="16a89-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="16a89-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="16a89-118">Minimum supported client</span></span><br/> | <span data-ttu-id="16a89-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="16a89-119">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="16a89-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="16a89-120">Minimum supported server</span></span><br/> | <span data-ttu-id="16a89-121">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="16a89-121">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





