---
title: Élément Suppress (QueryType)
description: Requête XPath qui identifie les événements à exclure du jeu de résultats de la requête.
ms.assetid: 41304a3c-bde1-49c3-8cb3-e95fc428bd96
keywords:
- Supprimer l’élément EventLog
topic_type:
- apiref
api_name:
- Suppress
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3a1d7fcec98d32167155ebcafc4f13d2a727d59a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106330"
---
# <a name="suppress-querytype-element"></a><span data-ttu-id="a06dc-104">Élément Suppress (QueryType)</span><span class="sxs-lookup"><span data-stu-id="a06dc-104">Suppress (QueryType) Element</span></span>

<span data-ttu-id="a06dc-105">Requête XPath qui identifie les événements à exclure du jeu de résultats de la requête.</span><span class="sxs-lookup"><span data-stu-id="a06dc-105">An XPath query that identifies the events to exclude from the query result set.</span></span>

``` syntax
<xs:element name="Suppress">
    <xs:complexType
        mixed="true"
    >
        <xs:attribute name="Path"
            type="anyURI"
         />
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="a06dc-106">L’élément de **suppression** est défini par le type complexe [**QueryType**](queryschema-querytype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="a06dc-106">The **Suppress** element is defined by the [**QueryType**](queryschema-querytype-complextype.md) complex type.</span></span>

## <a name="attributes"></a><span data-ttu-id="a06dc-107">Attributs</span><span class="sxs-lookup"><span data-stu-id="a06dc-107">Attributes</span></span>



| <span data-ttu-id="a06dc-108">Nom</span><span class="sxs-lookup"><span data-stu-id="a06dc-108">Name</span></span> | <span data-ttu-id="a06dc-109">Type</span><span class="sxs-lookup"><span data-stu-id="a06dc-109">Type</span></span>   | <span data-ttu-id="a06dc-110">Description</span><span class="sxs-lookup"><span data-stu-id="a06dc-110">Description</span></span>                                                                              |
|------|--------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a06dc-111">Path</span><span class="sxs-lookup"><span data-stu-id="a06dc-111">Path</span></span> | <span data-ttu-id="a06dc-112">anyURI</span><span class="sxs-lookup"><span data-stu-id="a06dc-112">anyURI</span></span> | <span data-ttu-id="a06dc-113">Nom du canal ou chemin d’accès au fichier journal qui contient les événements.</span><span class="sxs-lookup"><span data-stu-id="a06dc-113">The name of the channel or the path to the log file that contains the events.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="a06dc-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a06dc-114">Requirements</span></span>



| <span data-ttu-id="a06dc-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a06dc-115">Requirement</span></span> | <span data-ttu-id="a06dc-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="a06dc-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a06dc-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a06dc-117">Minimum supported client</span></span><br/> | <span data-ttu-id="a06dc-118">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a06dc-118">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="a06dc-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a06dc-119">Minimum supported server</span></span><br/> | <span data-ttu-id="a06dc-120">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a06dc-120">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a06dc-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a06dc-121">See also</span></span>

<dl> <dt>

<span data-ttu-id="a06dc-122">**Élément parent**</span><span class="sxs-lookup"><span data-stu-id="a06dc-122">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="a06dc-123">**Requête (QueryListType)**</span><span class="sxs-lookup"><span data-stu-id="a06dc-123">**Query (QueryListType)**</span></span>](queryschema-query-querylisttype-element.md)
</dt> </dl>

 

 





