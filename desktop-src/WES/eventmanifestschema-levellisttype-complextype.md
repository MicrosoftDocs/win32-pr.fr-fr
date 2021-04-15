---
title: Type complexe LevelListType
description: Définit une liste de niveaux de gravité qui spécifient le niveau de détail d’un événement.
ms.assetid: 82102f8a-271e-4c3d-9b0a-1e20eaa87497
keywords:
- LevelListType type complexe EventLog
topic_type:
- apiref
api_name:
- LevelListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4456ade3977603948997304393a1c9414cb0c458
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466962"
---
# <a name="levellisttype-complex-type"></a><span data-ttu-id="8cec7-104">Type complexe LevelListType</span><span class="sxs-lookup"><span data-stu-id="8cec7-104">LevelListType Complex Type</span></span>

<span data-ttu-id="8cec7-105">Définit une liste de niveaux de gravité qui spécifient le niveau de détail d’un événement.</span><span class="sxs-lookup"><span data-stu-id="8cec7-105">Defines a list of severity levels that specify the verbosity of an event.</span></span>

``` syntax
<xs:complexType name="LevelListType">
    <xs:sequence>
        <xs:element name="level"
            type="LevelType"
            minOccurs="0"
            maxOccurs="unbounded"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="8cec7-106">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="8cec7-106">Child elements</span></span>



| <span data-ttu-id="8cec7-107">Élément</span><span class="sxs-lookup"><span data-stu-id="8cec7-107">Element</span></span>                                                          | <span data-ttu-id="8cec7-108">Type</span><span class="sxs-lookup"><span data-stu-id="8cec7-108">Type</span></span>                                                           | <span data-ttu-id="8cec7-109">Description</span><span class="sxs-lookup"><span data-stu-id="8cec7-109">Description</span></span>                                                                                 |
|------------------------------------------------------------------|----------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8cec7-110">**niveau**</span><span class="sxs-lookup"><span data-stu-id="8cec7-110">**level**</span></span>](eventmanifestschema-level-levellisttype-element.md) | [<span data-ttu-id="8cec7-111">**LevelType**</span><span class="sxs-lookup"><span data-stu-id="8cec7-111">**LevelType**</span></span>](eventmanifestschema-leveltype-complextype.md) | <span data-ttu-id="8cec7-112">Définit une valeur de gravité qui détermine le niveau de détail des événements lors de la journalisation.</span><span class="sxs-lookup"><span data-stu-id="8cec7-112">Defines a severity value that determines the verbosity of events during logging.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="8cec7-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8cec7-113">Requirements</span></span>



| <span data-ttu-id="8cec7-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8cec7-114">Requirement</span></span> | <span data-ttu-id="8cec7-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="8cec7-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="8cec7-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8cec7-116">Minimum supported client</span></span><br/> | <span data-ttu-id="8cec7-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8cec7-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="8cec7-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8cec7-118">Minimum supported server</span></span><br/> | <span data-ttu-id="8cec7-119">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8cec7-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





