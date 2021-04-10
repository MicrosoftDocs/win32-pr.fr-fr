---
title: Élément Delay (sessionStateChangeTriggerType)
description: Contient une valeur qui indique la durée de délai pour l’heure de début d’une tâche, lorsqu’un changement d’état de session Terminal Server est détecté.
ms.assetid: 7fb87c4c-0b69-4c5b-b038-d61fb7c4ab9a
keywords:
- Retarder l’élément Planificateur de tâches
topic_type:
- apiref
api_name:
- Delay
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 03f230465f2e2b49ce83f1af358dfa1f84f21433
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106378"
---
# <a name="delay-sessionstatechangetriggertype-element"></a><span data-ttu-id="7b5d5-104">Élément Delay (sessionStateChangeTriggerType)</span><span class="sxs-lookup"><span data-stu-id="7b5d5-104">Delay (sessionStateChangeTriggerType) Element</span></span>

<span data-ttu-id="7b5d5-105">Contient une valeur qui indique la durée de délai pour l’heure de début d’une tâche, lorsqu’un changement d’état de session Terminal Server est détecté.</span><span class="sxs-lookup"><span data-stu-id="7b5d5-105">Contains a value that indicates the delay length for a task start time, when a Terminal Server session state change is detected.</span></span> <span data-ttu-id="7b5d5-106">Le format de cette chaîne est PnYnMnDTnHnMnS, où nY est le nombre d’années, nM est le nombre de mois, nD le nombre de jours, 't’est le séparateur de date/heure, nH est le nombre d’heures, nM est le nombre de minutes et nS est le nombre de secondes (par exemple, PT5M spécifie 5 minutes et P1M4DT2H5M spécifie un mois, quatre jours, deux heures et cinq minutes).</span><span class="sxs-lookup"><span data-stu-id="7b5d5-106">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span> <span data-ttu-id="7b5d5-107">Pour plus d’informations sur le type de durée, consultez <https://go.microsoft.com/fwlink/p/?linkid=106886> .</span><span class="sxs-lookup"><span data-stu-id="7b5d5-107">For more information about the duration type, see <https://go.microsoft.com/fwlink/p/?linkid=106886>.</span></span>

``` syntax
<xs:element name="Delay"
    type="duration"
 />
```

<span data-ttu-id="7b5d5-108">L’élément **delay** est défini par le type complexe [**sessionStateChangeTriggerType**](taskschedulerschema-sessionstatechangetriggertype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="7b5d5-108">The **Delay** element is defined by the [**sessionStateChangeTriggerType**](taskschedulerschema-sessionstatechangetriggertype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="7b5d5-109">Élément parent</span><span class="sxs-lookup"><span data-stu-id="7b5d5-109">Parent element</span></span>



| <span data-ttu-id="7b5d5-110">Élément</span><span class="sxs-lookup"><span data-stu-id="7b5d5-110">Element</span></span>                       | <span data-ttu-id="7b5d5-111">Dérivé de</span><span class="sxs-lookup"><span data-stu-id="7b5d5-111">Derived from</span></span>                                                                                           | <span data-ttu-id="7b5d5-112">Description</span><span class="sxs-lookup"><span data-stu-id="7b5d5-112">Description</span></span>                                                                                      |
|-------------------------------|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b5d5-113">**SessionStateChangeTrigger**</span><span class="sxs-lookup"><span data-stu-id="7b5d5-113">**SessionStateChangeTrigger**</span></span> | [<span data-ttu-id="7b5d5-114">**sessionStateChangeTriggerType**</span><span class="sxs-lookup"><span data-stu-id="7b5d5-114">**sessionStateChangeTriggerType**</span></span>](taskschedulerschema-sessionstatechangetriggertype-complextype.md) | <span data-ttu-id="7b5d5-115">Spécifie un déclencheur qui démarre une tâche quand une session de Terminal Server change d’État.</span><span class="sxs-lookup"><span data-stu-id="7b5d5-115">Specifies a trigger that starts a task when a Terminal Server session changes state.</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="7b5d5-116">Notes</span><span class="sxs-lookup"><span data-stu-id="7b5d5-116">Remarks</span></span>

<span data-ttu-id="7b5d5-117">Pour le développement de script, le délai de déclenchement du changement d’état de session est spécifié à l’aide de la propriété [**SessionStateChangeTrigger. Delay**](sessionstatechangetrigger-delay.md) .</span><span class="sxs-lookup"><span data-stu-id="7b5d5-117">For scripting development, the session state change trigger delay is specified using the [**SessionStateChangeTrigger.Delay**](sessionstatechangetrigger-delay.md) property.</span></span>

<span data-ttu-id="7b5d5-118">Pour le développement C++, le délai de déclenchement du changement d’état de session est spécifié à l’aide [**de la propriété Delay de ISessionStateChangeTrigger**](/windows/desktop/api/taskschd/nf-taskschd-isessionstatechangetrigger-get_delay).</span><span class="sxs-lookup"><span data-stu-id="7b5d5-118">For C++ development, the session state change trigger delay is specified using the [**Delay property of ISessionStateChangeTrigger**](/windows/desktop/api/taskschd/nf-taskschd-isessionstatechangetrigger-get_delay).</span></span>

## <a name="requirements"></a><span data-ttu-id="7b5d5-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7b5d5-119">Requirements</span></span>



| <span data-ttu-id="7b5d5-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7b5d5-120">Requirement</span></span> | <span data-ttu-id="7b5d5-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="7b5d5-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="7b5d5-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7b5d5-122">Minimum supported client</span></span><br/> | <span data-ttu-id="7b5d5-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7b5d5-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="7b5d5-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7b5d5-124">Minimum supported server</span></span><br/> | <span data-ttu-id="7b5d5-125">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7b5d5-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





