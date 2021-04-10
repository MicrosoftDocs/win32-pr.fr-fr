---
title: Type complexe namedValue
description: Définit un nom qui est associé à une valeur dans une paire nom-valeur.
ms.assetid: 5e3ce01a-9be6-4f12-be02-42065aba46cd
keywords:
- Planificateur de tâches de type complexe namedValue
topic_type:
- apiref
api_name:
- namedValue
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 39d6990194350dcc032d42838f30bdd7339b0d38
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942424"
---
# <a name="namedvalue-complex-type"></a><span data-ttu-id="e4f4c-104">Type complexe namedValue</span><span class="sxs-lookup"><span data-stu-id="e4f4c-104">namedValue Complex Type</span></span>

<span data-ttu-id="e4f4c-105">Définit un nom qui est associé à une valeur dans une paire nom-valeur.</span><span class="sxs-lookup"><span data-stu-id="e4f4c-105">Defines a name that is associated with a value in a name-value pair.</span></span>

``` syntax
<xs:complexType name="namedValue">
    <xs:simpleContent>
        <xs:extension
            base="nonEmptyString"
        >
            <xs:attribute name="name"
                type="nonEmptyString"
                use="required"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a><span data-ttu-id="e4f4c-106">Attributs</span><span class="sxs-lookup"><span data-stu-id="e4f4c-106">Attributes</span></span>



| <span data-ttu-id="e4f4c-107">Nom</span><span class="sxs-lookup"><span data-stu-id="e4f4c-107">Name</span></span> | <span data-ttu-id="e4f4c-108">Type</span><span class="sxs-lookup"><span data-stu-id="e4f4c-108">Type</span></span>                                                                    | <span data-ttu-id="e4f4c-109">Description</span><span class="sxs-lookup"><span data-stu-id="e4f4c-109">Description</span></span>                                                                          |
|------|-------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e4f4c-110">name</span><span class="sxs-lookup"><span data-stu-id="e4f4c-110">name</span></span> | [<span data-ttu-id="e4f4c-111">**nonEmptyString**</span><span class="sxs-lookup"><span data-stu-id="e4f4c-111">**nonEmptyString**</span></span>](taskschedulerschema-nonemptystring-simpletype.md) | <span data-ttu-id="e4f4c-112">Spécifie le nom qui est associé à une valeur dans une paire nom-valeur.</span><span class="sxs-lookup"><span data-stu-id="e4f4c-112">Specifies the name that is associated with a value in a name-value pair.</span></span> <br/> |



## <a name="requirements"></a><span data-ttu-id="e4f4c-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e4f4c-113">Requirements</span></span>



| <span data-ttu-id="e4f4c-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e4f4c-114">Requirement</span></span> | <span data-ttu-id="e4f4c-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="e4f4c-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e4f4c-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e4f4c-116">Minimum supported client</span></span><br/> | <span data-ttu-id="e4f4c-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e4f4c-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="e4f4c-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e4f4c-118">Minimum supported server</span></span><br/> | <span data-ttu-id="e4f4c-119">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e4f4c-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





