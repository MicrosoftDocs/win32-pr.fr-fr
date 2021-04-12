---
title: Select (QueryType) (élément)
description: Requête XPath qui identifie les événements à inclure dans le jeu de résultats de la requête.
ms.assetid: b6aa747b-3586-460b-b51c-52fb112739c3
keywords:
- Sélectionner l’élément EventLog
topic_type:
- apiref
api_name:
- Select
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b1735f5de49853357eed1ce00b8d181edf2279ab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385147"
---
# <a name="select-querytype-element"></a><span data-ttu-id="1fb77-104">Select (QueryType) (élément)</span><span class="sxs-lookup"><span data-stu-id="1fb77-104">Select (QueryType) Element</span></span>

<span data-ttu-id="1fb77-105">Requête XPath qui identifie les événements à inclure dans le jeu de résultats de la requête.</span><span class="sxs-lookup"><span data-stu-id="1fb77-105">An XPath query that identifies the events to include in the query result set.</span></span>

``` syntax
<xs:element name="Select">
    <xs:complexType
        mixed="true"
    >
        <xs:attribute name="Path"
            type="anyURI"
         />
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="1fb77-106">L’élément **Select** est défini par le type complexe [**QueryType**](queryschema-querytype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="1fb77-106">The **Select** element is defined by the [**QueryType**](queryschema-querytype-complextype.md) complex type.</span></span>

## <a name="attributes"></a><span data-ttu-id="1fb77-107">Attributs</span><span class="sxs-lookup"><span data-stu-id="1fb77-107">Attributes</span></span>



| <span data-ttu-id="1fb77-108">Nom</span><span class="sxs-lookup"><span data-stu-id="1fb77-108">Name</span></span> | <span data-ttu-id="1fb77-109">Type</span><span class="sxs-lookup"><span data-stu-id="1fb77-109">Type</span></span>   | <span data-ttu-id="1fb77-110">Description</span><span class="sxs-lookup"><span data-stu-id="1fb77-110">Description</span></span>                                                                              |
|------|--------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="1fb77-111">Path</span><span class="sxs-lookup"><span data-stu-id="1fb77-111">Path</span></span> | <span data-ttu-id="1fb77-112">anyURI</span><span class="sxs-lookup"><span data-stu-id="1fb77-112">anyURI</span></span> | <span data-ttu-id="1fb77-113">Nom du canal ou chemin d’accès au fichier journal qui contient les événements.</span><span class="sxs-lookup"><span data-stu-id="1fb77-113">The name of the channel or the path to the log file that contains the events.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="1fb77-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1fb77-114">Requirements</span></span>



| <span data-ttu-id="1fb77-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1fb77-115">Requirement</span></span> | <span data-ttu-id="1fb77-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="1fb77-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------|
| <span data-ttu-id="1fb77-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1fb77-117">Minimum supported client</span></span><br/> | <span data-ttu-id="1fb77-118">Applications de bureau Windows Vista- \[ \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="1fb77-118">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>       |
| <span data-ttu-id="1fb77-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1fb77-119">Minimum supported server</span></span><br/> | <span data-ttu-id="1fb77-120">Applications de bureau Windows Server 2008 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="1fb77-120">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1fb77-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1fb77-121">See also</span></span>

<dl> <dt>

<span data-ttu-id="1fb77-122">**Élément parent**</span><span class="sxs-lookup"><span data-stu-id="1fb77-122">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="1fb77-123">**Requête (QueryListType)**</span><span class="sxs-lookup"><span data-stu-id="1fb77-123">**Query (QueryListType)**</span></span>](queryschema-query-querylisttype-element.md)
</dt> </dl>

 

 





