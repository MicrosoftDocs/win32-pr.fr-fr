---
title: Élément ExecutionTimeLimit (settingsType)
description: Durée d’exécution de la tâche.
ms.assetid: c42d0f42-4571-44ab-90b1-948fd7ea991b
keywords:
- Élément ExecutionTimeLimit Planificateur de tâches
topic_type:
- apiref
api_name:
- ExecutionTimeLimit
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: dd86f7ae4988211fdf100f69ac82e747e9ea0f49
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843229"
---
# <a name="executiontimelimit-settingstype-element"></a><span data-ttu-id="da652-104">Élément ExecutionTimeLimit (settingsType)</span><span class="sxs-lookup"><span data-stu-id="da652-104">ExecutionTimeLimit (settingsType) Element</span></span>

<span data-ttu-id="da652-105">Durée d’exécution de la tâche. Le format de cette chaîne est PnYnMnDTnHnMnS, où nY est le nombre d’années, nM est le nombre de mois, nD le nombre de jours, 't’est le séparateur de date/heure, nH est le nombre d’heures, nM est le nombre de minutes et nS est le nombre de secondes (par exemple, PT5M spécifie 5 minutes et P1M4DT2H5M spécifie un mois, quatre jours, deux heures et cinq minutes).</span><span class="sxs-lookup"><span data-stu-id="da652-105">Amount of time allowed to complete the task.The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span> <span data-ttu-id="da652-106">Pour plus d’informations sur le type de durée, consultez <https://go.microsoft.com/fwlink/p/?linkid=106886> .</span><span class="sxs-lookup"><span data-stu-id="da652-106">For more information about the duration type, see <https://go.microsoft.com/fwlink/p/?linkid=106886>.</span></span> <span data-ttu-id="da652-107">La valeur PT0S permet à la tâche de s’exécuter indéfiniment.</span><span class="sxs-lookup"><span data-stu-id="da652-107">A value of PT0S will enable the task to run indefinitely.</span></span>

``` syntax
<xs:element name="ExecutionTimeLimit"
    type="duration"
    minOccurs="0"
 />
```

<span data-ttu-id="da652-108">L’élément **ExecutionTimeLimit** est défini par le type complexe [**settingsType**](taskschedulerschema-settingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="da652-108">The **ExecutionTimeLimit** element is defined by the [**settingsType**](taskschedulerschema-settingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="da652-109">Élément parent</span><span class="sxs-lookup"><span data-stu-id="da652-109">Parent element</span></span>



| <span data-ttu-id="da652-110">Élément</span><span class="sxs-lookup"><span data-stu-id="da652-110">Element</span></span>                                                           | <span data-ttu-id="da652-111">Dérivé de</span><span class="sxs-lookup"><span data-stu-id="da652-111">Derived from</span></span>                                                         | <span data-ttu-id="da652-112">Description</span><span class="sxs-lookup"><span data-stu-id="da652-112">Description</span></span>                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="da652-113">**Paramètres**</span><span class="sxs-lookup"><span data-stu-id="da652-113">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="da652-114">**settingsType**</span><span class="sxs-lookup"><span data-stu-id="da652-114">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md) | <span data-ttu-id="da652-115">Contient les paramètres que le Planificateur de tâches utilise pour effectuer la tâche.</span><span class="sxs-lookup"><span data-stu-id="da652-115">Contains the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="da652-116">Notes</span><span class="sxs-lookup"><span data-stu-id="da652-116">Remarks</span></span>

<span data-ttu-id="da652-117">Pour le développement C++, consultez la [**propriété ExecutionTimeLimit de ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_executiontimelimit).</span><span class="sxs-lookup"><span data-stu-id="da652-117">For C++ development, see [**ExecutionTimeLimit Property of ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_executiontimelimit).</span></span>

<span data-ttu-id="da652-118">Pour le développement de scripts, consultez [**TaskSettings.ExecutionTimeLimit**](tasksettings-executiontimelimit.md).</span><span class="sxs-lookup"><span data-stu-id="da652-118">For script development, see [**TaskSettings.ExecutionTimeLimit**](tasksettings-executiontimelimit.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="da652-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="da652-119">Requirements</span></span>



| <span data-ttu-id="da652-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="da652-120">Requirement</span></span> | <span data-ttu-id="da652-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="da652-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="da652-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="da652-122">Minimum supported client</span></span><br/> | <span data-ttu-id="da652-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="da652-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="da652-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="da652-124">Minimum supported server</span></span><br/> | <span data-ttu-id="da652-125">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="da652-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="da652-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="da652-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da652-127">Éléments de schéma Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="da652-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





