---
title: Élément DeleteExpiredTaskAfter (settingsType)
description: Spécifie la durée d’attente de la Planificateur de tâches avant la suppression de la tâche après son expiration.
ms.assetid: 947a2fec-ceda-4726-aa1a-26fd1b258c1f
keywords:
- Élément DeleteExpiredTaskAfter Planificateur de tâches
topic_type:
- apiref
api_name:
- DeleteExpiredTaskAfter
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: cee7cfc48f62b58caf63125404fb07209b399fc1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509308"
---
# <a name="deleteexpiredtaskafter-settingstype-element"></a><span data-ttu-id="e6919-104">Élément DeleteExpiredTaskAfter (settingsType)</span><span class="sxs-lookup"><span data-stu-id="e6919-104">DeleteExpiredTaskAfter (settingsType) Element</span></span>

<span data-ttu-id="e6919-105">Spécifie la durée d’attente de la Planificateur de tâches avant la suppression de la tâche après son expiration.</span><span class="sxs-lookup"><span data-stu-id="e6919-105">Specifies the amount of time that the Task Scheduler will wait before deleting the task after it expires.</span></span> <span data-ttu-id="e6919-106">Si aucune valeur n’est spécifiée pour cet élément, le service Planificateur de tâches ne supprimera pas la tâche.</span><span class="sxs-lookup"><span data-stu-id="e6919-106">If no value is specified for this element, then the Task Scheduler service will not delete the task.</span></span> <span data-ttu-id="e6919-107">Le format de cette chaîne est PnYnMnDTnHnMnS, où nY est le nombre d’années, nM est le nombre de mois, nD le nombre de jours, 't’est le séparateur de date/heure, nH est le nombre d’heures, nM est le nombre de minutes et nS est le nombre de secondes (par exemple, PT5M spécifie 5 minutes et P1M4DT2H5M spécifie un mois, quatre jours, deux heures et cinq minutes).</span><span class="sxs-lookup"><span data-stu-id="e6919-107">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span> <span data-ttu-id="e6919-108">Pour plus d’informations sur le type de durée, consultez <https://go.microsoft.com/fwlink/p/?linkid=106886> .</span><span class="sxs-lookup"><span data-stu-id="e6919-108">For more information about the duration type, see <https://go.microsoft.com/fwlink/p/?linkid=106886>.</span></span>

``` syntax
<xs:element name="DeleteExpiredTaskAfter"
    type="duration"
    minOccurs="0"
    default="PT0S"
 />
```

<span data-ttu-id="e6919-109">L’élément **DeleteExpiredTaskAfter** est défini par le type complexe [**settingsType**](taskschedulerschema-settingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="e6919-109">The **DeleteExpiredTaskAfter** element is defined by the [**settingsType**](taskschedulerschema-settingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="e6919-110">Élément parent</span><span class="sxs-lookup"><span data-stu-id="e6919-110">Parent element</span></span>



| <span data-ttu-id="e6919-111">Élément</span><span class="sxs-lookup"><span data-stu-id="e6919-111">Element</span></span>                                                           | <span data-ttu-id="e6919-112">Dérivé de</span><span class="sxs-lookup"><span data-stu-id="e6919-112">Derived from</span></span>                                                         | <span data-ttu-id="e6919-113">Description</span><span class="sxs-lookup"><span data-stu-id="e6919-113">Description</span></span>                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="e6919-114">**Paramètres**</span><span class="sxs-lookup"><span data-stu-id="e6919-114">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="e6919-115">**settingsType**</span><span class="sxs-lookup"><span data-stu-id="e6919-115">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md) | <span data-ttu-id="e6919-116">Contient les paramètres que le Planificateur de tâches utilise pour effectuer la tâche.</span><span class="sxs-lookup"><span data-stu-id="e6919-116">Contains the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="e6919-117">Notes</span><span class="sxs-lookup"><span data-stu-id="e6919-117">Remarks</span></span>

<span data-ttu-id="e6919-118">Pour le développement C++, consultez la [**propriété DeleteExpiredTaskAfter de ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_deleteexpiredtaskafter).</span><span class="sxs-lookup"><span data-stu-id="e6919-118">For C++ development, see [**DeleteExpiredTaskAfter Property of ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_deleteexpiredtaskafter).</span></span>

<span data-ttu-id="e6919-119">Pour le développement de scripts, consultez [**TaskSettings. DeleteExpiredTaskAfter**](tasksettings-deleteexpiredtaskafter.md).</span><span class="sxs-lookup"><span data-stu-id="e6919-119">For script development, see [**TaskSettings.DeleteExpiredTaskAfter**](tasksettings-deleteexpiredtaskafter.md).</span></span>

## <a name="examples"></a><span data-ttu-id="e6919-120">Exemples</span><span class="sxs-lookup"><span data-stu-id="e6919-120">Examples</span></span>

<span data-ttu-id="e6919-121">Le code XML suivant définit un élément Settings qui supprime une tâche ayant expiré après une semaine.</span><span class="sxs-lookup"><span data-stu-id="e6919-121">The following XML defines a settings element that deletes an expired task after one week.</span></span>


```XML
<Settings>
    <DeleteExpiredTaskAfter>PT7D</DeleteExpiredTaskAfter>
</Settings>
```



## <a name="requirements"></a><span data-ttu-id="e6919-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e6919-122">Requirements</span></span>



| <span data-ttu-id="e6919-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e6919-123">Requirement</span></span> | <span data-ttu-id="e6919-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="e6919-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e6919-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e6919-125">Minimum supported client</span></span><br/> | <span data-ttu-id="e6919-126">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e6919-126">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="e6919-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e6919-127">Minimum supported server</span></span><br/> | <span data-ttu-id="e6919-128">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e6919-128">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e6919-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e6919-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6919-130">Éléments de schéma Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="e6919-130">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





