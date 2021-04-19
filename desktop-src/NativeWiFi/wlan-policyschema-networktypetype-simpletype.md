---
description: Définit les types de réseau sans fil.
ms.assetid: 03236db9-4f58-4fe3-82ff-d4b3a387490a
title: Type simple networkTypeType
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- networkTypeType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: d0acb998c879e718a0e201418610bb0aa6db8c31
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106541232"
---
# <a name="networktypetype-simple-type"></a><span data-ttu-id="68443-103">Type simple networkTypeType</span><span class="sxs-lookup"><span data-stu-id="68443-103">networkTypeType Simple Type</span></span>

<span data-ttu-id="68443-104">Le type simple networkTypeType définit les types de réseau sans fil.</span><span class="sxs-lookup"><span data-stu-id="68443-104">The networkTypeType simple type defines the wireless network types.</span></span> <span data-ttu-id="68443-105">Il existe deux types de réseaux : les réseaux d’infrastructure (ESS) et les réseaux ad hoc (IBSS).</span><span class="sxs-lookup"><span data-stu-id="68443-105">There are two types of networks: infrastructure networks (ESS) and ad-hoc networks (IBSS).</span></span>

``` syntax
<xs:simpleType name="networkTypeType">
    <xs:restriction
        base="string"
    >
        <xs:enumeration
            value="IBSS"
         />
        <xs:enumeration
            value="ESS"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a><span data-ttu-id="68443-106">Valeurs d’énumération</span><span class="sxs-lookup"><span data-stu-id="68443-106">Enumeration values</span></span>

<span data-ttu-id="68443-107">Le type simple **networkTypeType** définit les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="68443-107">The **networkTypeType** simple type defines the following values.</span></span>



| <span data-ttu-id="68443-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="68443-108">Value</span></span> | <span data-ttu-id="68443-109">Description</span><span class="sxs-lookup"><span data-stu-id="68443-109">Description</span></span> |
|-------|-------------|
| <span data-ttu-id="68443-110">IBSS</span><span class="sxs-lookup"><span data-stu-id="68443-110">IBSS</span></span>  |             |
| <span data-ttu-id="68443-111">CCÈS</span><span class="sxs-lookup"><span data-stu-id="68443-111">ESS</span></span>   |             |



## <a name="requirements"></a><span data-ttu-id="68443-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="68443-112">Requirements</span></span>



| <span data-ttu-id="68443-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="68443-113">Requirement</span></span> | <span data-ttu-id="68443-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="68443-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="68443-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="68443-115">Minimum supported client</span></span><br/> | <span data-ttu-id="68443-116">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="68443-116">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="68443-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="68443-117">Minimum supported server</span></span><br/> | <span data-ttu-id="68443-118">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="68443-118">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




