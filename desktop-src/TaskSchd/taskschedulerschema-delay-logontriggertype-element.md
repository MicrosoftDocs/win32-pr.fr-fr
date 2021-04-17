---
title: Élément Delay (logonTriggerType)
description: Intervalle de temps entre le moment où l’utilisateur ouvre une session et le moment où la tâche est démarrée.
ms.assetid: daab29f7-5d05-4e6d-a0c0-7b83b4d0b941
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
ms.openlocfilehash: a820bad3d68cfb0a697f795a9fd7326c9e52abe9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466766"
---
# <a name="delay-logontriggertype-element"></a><span data-ttu-id="75be0-104">Élément Delay (logonTriggerType)</span><span class="sxs-lookup"><span data-stu-id="75be0-104">Delay (logonTriggerType) Element</span></span>

<span data-ttu-id="75be0-105">Intervalle de temps entre le moment où l’utilisateur ouvre une session et le moment où la tâche est démarrée.</span><span class="sxs-lookup"><span data-stu-id="75be0-105">Amount of time between when the user logs on and when the task is started.</span></span> <span data-ttu-id="75be0-106">Le format de cette chaîne est PnYnMnDTnHnMnS, où nY est le nombre d’années, nM est le nombre de mois, nD le nombre de jours, 't’est le séparateur de date/heure, nH est le nombre d’heures, nM est le nombre de minutes et nS est le nombre de secondes (par exemple, PT5M spécifie 5 minutes et P1M4DT2H5M spécifie un mois, quatre jours, deux heures et cinq minutes).</span><span class="sxs-lookup"><span data-stu-id="75be0-106">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span> <span data-ttu-id="75be0-107">Pour plus d’informations sur le type de durée, consultez <https://go.microsoft.com/fwlink/p/?linkid=106886> .</span><span class="sxs-lookup"><span data-stu-id="75be0-107">For more information about the duration type, see <https://go.microsoft.com/fwlink/p/?linkid=106886>.</span></span>

``` syntax
<xs:element name="Delay"
    type="duration"
 />
```

<span data-ttu-id="75be0-108">L’élément **delay** est défini par le type complexe [**logonTriggerType**](taskschedulerschema-logontriggertype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="75be0-108">The **Delay** element is defined by the [**logonTriggerType**](taskschedulerschema-logontriggertype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="75be0-109">Élément parent</span><span class="sxs-lookup"><span data-stu-id="75be0-109">Parent element</span></span>



| <span data-ttu-id="75be0-110">Élément</span><span class="sxs-lookup"><span data-stu-id="75be0-110">Element</span></span>                                                                       | <span data-ttu-id="75be0-111">Dérivé de</span><span class="sxs-lookup"><span data-stu-id="75be0-111">Derived from</span></span>                                                                 | <span data-ttu-id="75be0-112">Description</span><span class="sxs-lookup"><span data-stu-id="75be0-112">Description</span></span>                                                            |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="75be0-113">**LogonTrigger**</span><span class="sxs-lookup"><span data-stu-id="75be0-113">**LogonTrigger**</span></span>](taskschedulerschema-logontrigger-triggergroup-element.md) | [<span data-ttu-id="75be0-114">**logonTriggerType**</span><span class="sxs-lookup"><span data-stu-id="75be0-114">**logonTriggerType**</span></span>](taskschedulerschema-logontriggertype-complextype.md) | <span data-ttu-id="75be0-115">Spécifie un déclencheur qui démarre une tâche lorsqu’un utilisateur ouvre une session.</span><span class="sxs-lookup"><span data-stu-id="75be0-115">Specifies a trigger that starts a task when a user logs on.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="75be0-116">Notes</span><span class="sxs-lookup"><span data-stu-id="75be0-116">Remarks</span></span>

<span data-ttu-id="75be0-117">Pour le développement de scripts, le délai de déclenchement de connexion est spécifié à l’aide de la propriété [**LogonTrigger. Delay**](logontrigger-delay.md) .</span><span class="sxs-lookup"><span data-stu-id="75be0-117">For scripting development, the logon trigger delay is specified using the [**LogonTrigger.Delay**](logontrigger-delay.md) property.</span></span>

<span data-ttu-id="75be0-118">Pour le développement C++, l’identificateur d’utilisateur du déclencheur LOGON est spécifié à l’aide de la propriété [**ILogonTrigger ::D Nouv**](/windows/desktop/api/taskschd/nf-taskschd-ilogontrigger-get_delay) .</span><span class="sxs-lookup"><span data-stu-id="75be0-118">For C++ development, the user identifier for the logon trigger is specified using the [**ILogonTrigger::Delay**](/windows/desktop/api/taskschd/nf-taskschd-ilogontrigger-get_delay) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="75be0-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="75be0-119">Requirements</span></span>



| <span data-ttu-id="75be0-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="75be0-120">Requirement</span></span> | <span data-ttu-id="75be0-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="75be0-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="75be0-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="75be0-122">Minimum supported client</span></span><br/> | <span data-ttu-id="75be0-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="75be0-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="75be0-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="75be0-124">Minimum supported server</span></span><br/> | <span data-ttu-id="75be0-125">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="75be0-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="75be0-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="75be0-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75be0-127">Éléments de schéma Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="75be0-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="75be0-128">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="75be0-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





