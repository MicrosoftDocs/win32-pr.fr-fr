---
title: Type simple dayOfMonthType
description: Définit les valeurs possibles pour la spécification d’un jour du mois.
ms.assetid: 13497cf4-e1e5-4d54-9dff-0fe89be1fed8
keywords:
- Planificateur de tâches de type simple dayOfMonthType
topic_type:
- apiref
api_name:
- dayOfMonthType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9a8428688ff429809c7509bae42adb156efe00ff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508393"
---
# <a name="dayofmonthtype-simple-type"></a><span data-ttu-id="43745-104">Type simple dayOfMonthType</span><span class="sxs-lookup"><span data-stu-id="43745-104">dayOfMonthType Simple Type</span></span>

<span data-ttu-id="43745-105">Définit les valeurs possibles pour la spécification d’un jour du mois.</span><span class="sxs-lookup"><span data-stu-id="43745-105">Defines the possible values for specifying a day of the month.</span></span>

``` syntax
<xs:simpleType name="dayOfMonthType">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="[1-9]|[1-2][0-9]|3[0-1]|Last"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a><span data-ttu-id="43745-106">Modèles</span><span class="sxs-lookup"><span data-stu-id="43745-106">Patterns</span></span>

<span data-ttu-id="43745-107">Le type simple **dayOfMonthType** est une **chaîne** qui est limitée par le modèle suivant :</span><span class="sxs-lookup"><span data-stu-id="43745-107">The **dayOfMonthType** simple type is a **string** that is restricted by the following pattern:</span></span>

-   `[1-9]|[1-2][0-9]|3[0-1]|Last`

    <span data-ttu-id="43745-108">Spécifie le 1er au 31 du mois, ou toujours le dernier jour du mois.</span><span class="sxs-lookup"><span data-stu-id="43745-108">Specifies the 1st through the 31st day of the month, or always the last day of the month.</span></span>

## <a name="requirements"></a><span data-ttu-id="43745-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="43745-109">Requirements</span></span>



| <span data-ttu-id="43745-110">Condition requise</span><span class="sxs-lookup"><span data-stu-id="43745-110">Requirement</span></span> | <span data-ttu-id="43745-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="43745-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="43745-112">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="43745-112">Minimum supported client</span></span><br/> | <span data-ttu-id="43745-113">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="43745-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="43745-114">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="43745-114">Minimum supported server</span></span><br/> | <span data-ttu-id="43745-115">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="43745-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="43745-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="43745-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43745-117">Types simples de schéma Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="43745-117">Task Scheduler Schema Simple Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="43745-118">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="43745-118">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





