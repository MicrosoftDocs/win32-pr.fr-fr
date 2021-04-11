---
title: Type simple weekType
description: Définit les valeurs qui peuvent être utilisées dans l’élément week.
ms.assetid: 83a525ae-020b-4528-9e14-1e7d9df7b8c0
keywords:
- Planificateur de tâches de type simple weekType
topic_type:
- apiref
api_name:
- weekType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6513efe0fe0ef4fcbf6b849627d09ec9da6feb82
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103277"
---
# <a name="weektype-simple-type"></a><span data-ttu-id="befcd-104">Type simple weekType</span><span class="sxs-lookup"><span data-stu-id="befcd-104">weekType Simple Type</span></span>

<span data-ttu-id="befcd-105">Définit les valeurs qui peuvent être utilisées dans l’élément [**week**](taskschedulerschema-week-weekstype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="befcd-105">Defines the values that can be used in the [**Week**](taskschedulerschema-week-weekstype-element.md) element.</span></span>

``` syntax
<xs:simpleType name="weekType">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="[1-4]|Last"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a><span data-ttu-id="befcd-106">Modèles</span><span class="sxs-lookup"><span data-stu-id="befcd-106">Patterns</span></span>

<span data-ttu-id="befcd-107">Le type simple **weekType** est une **chaîne** qui est limitée par le modèle suivant :</span><span class="sxs-lookup"><span data-stu-id="befcd-107">The **weekType** simple type is a **string** that is restricted by the following pattern:</span></span>

-   `[1-4]|Last`

    <span data-ttu-id="befcd-108">Spécifie le premier jusqu’à la quatrième semaine du mois (1-4) ou toujours la dernière semaine du mois.</span><span class="sxs-lookup"><span data-stu-id="befcd-108">Specifies the first through the fourth week of the month (1-4) or always the last week of the month.</span></span>

## <a name="requirements"></a><span data-ttu-id="befcd-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="befcd-109">Requirements</span></span>



| <span data-ttu-id="befcd-110">Condition requise</span><span class="sxs-lookup"><span data-stu-id="befcd-110">Requirement</span></span> | <span data-ttu-id="befcd-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="befcd-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="befcd-112">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="befcd-112">Minimum supported client</span></span><br/> | <span data-ttu-id="befcd-113">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="befcd-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="befcd-114">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="befcd-114">Minimum supported server</span></span><br/> | <span data-ttu-id="befcd-115">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="befcd-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="befcd-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="befcd-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="befcd-117">Types simples de schéma Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="befcd-117">Task Scheduler Schema Simple Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="befcd-118">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="befcd-118">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





