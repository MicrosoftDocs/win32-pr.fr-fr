---
title: Type simple runLevelType
description: Définit les valeurs possibles pour l’élément RunLevel (principalType).
ms.assetid: d6b73dc5-97ac-4f94-99c1-c241a25cc252
keywords:
- Planificateur de tâches de type simple runLevelType
topic_type:
- apiref
api_name:
- runLevelType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d037dceeb3e6e4957cc96a17a2ac511a03a94b94
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106542864"
---
# <a name="runleveltype-simple-type"></a><span data-ttu-id="8c547-104">Type simple runLevelType</span><span class="sxs-lookup"><span data-stu-id="8c547-104">runLevelType Simple Type</span></span>

<span data-ttu-id="8c547-105">Définit les valeurs possibles pour l’élément [**runlevel (principalType)**](taskschedulerschema-runlevel-principaltype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="8c547-105">Defines the possible values for the [**RunLevel (principalType)**](taskschedulerschema-runlevel-principaltype-element.md) element.</span></span>

``` syntax
<xs:simpleType name="runLevelType">
    <xs:restriction
        base="string"
    >
        <xs:enumeration
            value="LeastPrivilege"
         />
        <xs:enumeration
            value="HighestAvailable"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a><span data-ttu-id="8c547-106">Valeurs d’énumération</span><span class="sxs-lookup"><span data-stu-id="8c547-106">Enumeration values</span></span>

<span data-ttu-id="8c547-107">Le type simple **runLevelType** définit les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="8c547-107">The **runLevelType** simple type defines the following values.</span></span>



| <span data-ttu-id="8c547-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="8c547-108">Value</span></span>            | <span data-ttu-id="8c547-109">Description</span><span class="sxs-lookup"><span data-stu-id="8c547-109">Description</span></span>                                               |
|------------------|-----------------------------------------------------------|
| <span data-ttu-id="8c547-110">LeastPrivilege</span><span class="sxs-lookup"><span data-stu-id="8c547-110">LeastPrivilege</span></span>   | <span data-ttu-id="8c547-111">Les tâches sont exécutées avec le moins de privilèges (LUA).</span><span class="sxs-lookup"><span data-stu-id="8c547-111">Tasks are run with the least privileges (LUA).</span></span><br/> |
| <span data-ttu-id="8c547-112">HighestAvailable</span><span class="sxs-lookup"><span data-stu-id="8c547-112">HighestAvailable</span></span> | <span data-ttu-id="8c547-113">Les tâches sont exécutées avec les privilèges les plus élevés.</span><span class="sxs-lookup"><span data-stu-id="8c547-113">Tasks are run with the highest privileges.</span></span><br/>     |



## <a name="requirements"></a><span data-ttu-id="8c547-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8c547-114">Requirements</span></span>



| <span data-ttu-id="8c547-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8c547-115">Requirement</span></span> | <span data-ttu-id="8c547-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="8c547-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="8c547-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8c547-117">Minimum supported client</span></span><br/> | <span data-ttu-id="8c547-118">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8c547-118">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="8c547-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8c547-119">Minimum supported server</span></span><br/> | <span data-ttu-id="8c547-120">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8c547-120">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





