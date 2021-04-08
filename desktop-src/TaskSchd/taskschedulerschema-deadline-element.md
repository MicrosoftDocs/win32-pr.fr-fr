---
title: Élément échéance
description: Spécifie quand le planificateur de tâches doit démarrer la tâche pendant la maintenance automatique d’urgence, s’il n’a pas pu se terminer au cours d’une maintenance automatique normale.
ms.assetid: 34E33FAE-888E-4E82-83B8-059FB4A64B52
keywords:
- Élément échéance Planificateur de tâches
topic_type:
- apiref
api_name:
- Deadline
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3e12524971e8b713d4d17817a8a7c7602017bd68
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740829"
---
# <a name="deadline-element"></a><span data-ttu-id="638b1-104">Élément échéance</span><span class="sxs-lookup"><span data-stu-id="638b1-104">Deadline Element</span></span>

<span data-ttu-id="638b1-105">Spécifie quand le planificateur de tâches doit démarrer la tâche pendant la maintenance automatique d’urgence, s’il n’a pas pu se terminer au cours d’une maintenance automatique normale.</span><span class="sxs-lookup"><span data-stu-id="638b1-105">Specifies when the Task scheduler must to start the task during emergency Automatic maintenance, if it failed to complete during regular Automatic maintenance.</span></span>

<span data-ttu-id="638b1-106">Le format de cette chaîne est *PnYnMnDTnHnMnS*, où *NY* est le nombre d’années, nm est le nombre de mois, *ND* est le nombre de jours, *T* est le séparateur de date/heure, *NH* est le nombre d’heures, *nm* est le nombre de minutes et *NS* est le nombre de secondes (par exemple, « PT5M » spécifie 5 minutes et « P1M4DT2H5M » indique un mois, quatre jours, deux heures et cinq minutes).</span><span class="sxs-lookup"><span data-stu-id="638b1-106">The format for this string is *PnYnMnDTnHnMnS*, where *nY* is the number of years, nM is the number of months, *nD* is the number of days, *T* is the date/time separator, *nH* is the number of hours, *nM* is the number of minutes, and *nS* is the number of seconds (for example, "PT5M" specifies 5 minutes and "P1M4DT2H5M" specifies one month, four days, two hours, and five minutes).</span></span> <span data-ttu-id="638b1-107">La valeur minimale est d’une minute.</span><span class="sxs-lookup"><span data-stu-id="638b1-107">The minimum value is one minute.</span></span> <span data-ttu-id="638b1-108">Pour plus d’informations sur le type de durée, consultez [XML Schema Part 2 : Datatypes Second Edition](https://www.w3.org/TR/xmlschema-2/#duration).</span><span class="sxs-lookup"><span data-stu-id="638b1-108">For more information about the duration type, see [XML Schema Part 2: Datatypes Second Edition](https://www.w3.org/TR/xmlschema-2/#duration).</span></span> <span data-ttu-id="638b1-109">L’échéance minimale qu’une tâche peut utiliser est de 1 jour.</span><span class="sxs-lookup"><span data-stu-id="638b1-109">Minimum Deadline a task can use is 1 day.</span></span> <span data-ttu-id="638b1-110">La valeur de l’élément **échéance** doit être supérieure à la valeur de l’élément [**period**](taskschedulerschema-period-element.md) .</span><span class="sxs-lookup"><span data-stu-id="638b1-110">The value of the **Deadline** element should be greater than the value of the [**Period**](taskschedulerschema-period-element.md) element.</span></span> <span data-ttu-id="638b1-111">Si l’échéance n’est pas spécifiée, la tâche ne sera pas démarrée pendant la maintenance automatique d’urgence.</span><span class="sxs-lookup"><span data-stu-id="638b1-111">If the deadline is not specified the task will not be started during emergency Automatic maintenance.</span></span>

``` syntax
<xs:element name="Deadline"
    maxOccurs="1"
    minOccurs="0"
>
    <xs:simpleType>
        <xs:restriction
            base="duration"
        >
            <xs:minInclusive
                value="P1D"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="638b1-112">L’élément **échéance** est défini par le type complexe [**maintenanceSettingsType**](taskschedulerschema-maintenancesettingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="638b1-112">The **Deadline** element is defined by the [**maintenanceSettingsType**](taskschedulerschema-maintenancesettingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="638b1-113">Élément parent</span><span class="sxs-lookup"><span data-stu-id="638b1-113">Parent element</span></span>



| <span data-ttu-id="638b1-114">Élément</span><span class="sxs-lookup"><span data-stu-id="638b1-114">Element</span></span>                                                                                                                          | <span data-ttu-id="638b1-115">Dérivé de</span><span class="sxs-lookup"><span data-stu-id="638b1-115">Derived from</span></span>                                                                               | <span data-ttu-id="638b1-116">Description</span><span class="sxs-lookup"><span data-stu-id="638b1-116">Description</span></span>                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="638b1-117">**MaintenanceSettings (maintenanceSettingsType)**</span><span class="sxs-lookup"><span data-stu-id="638b1-117">**MaintenanceSettings (maintenanceSettingsType)**</span></span>](taskschedulerschema-maintenancesettings-maintenancesettingstype-element.md) | [<span data-ttu-id="638b1-118">**maintenanceSettingsType**</span><span class="sxs-lookup"><span data-stu-id="638b1-118">**maintenanceSettingsType**</span></span>](taskschedulerschema-maintenancesettingstype-complextype.md) | <span data-ttu-id="638b1-119">Spécifie les paramètres de tâche que le planificateur de tâches utilisera pour démarrer la tâche pendant la maintenance automatique.</span><span class="sxs-lookup"><span data-stu-id="638b1-119">Specifies the task settings the Task scheduler will use to start task during Automatic maintenance.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="638b1-120">Notes</span><span class="sxs-lookup"><span data-stu-id="638b1-120">Remarks</span></span>

<span data-ttu-id="638b1-121">Pour la programmation en C++, ce paramètre inactif est spécifié à l’aide de la propriété [**IMaintenanceSettings ::D échéanc**](/windows/desktop/api/Taskschd/nf-taskschd-imaintenancesettings-get_deadline) .</span><span class="sxs-lookup"><span data-stu-id="638b1-121">For C++ programming, this idle setting is specified using the [**IMaintenanceSettings::Deadline**](/windows/desktop/api/Taskschd/nf-taskschd-imaintenancesettings-get_deadline) property.</span></span>

## <a name="examples"></a><span data-ttu-id="638b1-122">Exemples</span><span class="sxs-lookup"><span data-stu-id="638b1-122">Examples</span></span>

<span data-ttu-id="638b1-123">Le code XML suivant définit un calendrier de mois qui exécute la tâche en mars.</span><span class="sxs-lookup"><span data-stu-id="638b1-123">The following XML defines a months calendar that runs the task in March.</span></span>


```XML
<MaintenanceSettings>
    <Period>P5D</Period>
    <Deadline>P15D</Deadline>
</MaintenanceSettings>
```



## <a name="requirements"></a><span data-ttu-id="638b1-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="638b1-124">Requirements</span></span>



| <span data-ttu-id="638b1-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="638b1-125">Requirement</span></span> | <span data-ttu-id="638b1-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="638b1-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="638b1-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="638b1-127">Minimum supported client</span></span><br/> | <span data-ttu-id="638b1-128">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="638b1-128">Windows 8 \[desktop apps only\]</span></span><br/>           |
| <span data-ttu-id="638b1-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="638b1-129">Minimum supported server</span></span><br/> | <span data-ttu-id="638b1-130">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="638b1-130">Windows Server 2012 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="638b1-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="638b1-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="638b1-132">Éléments de schéma Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="638b1-132">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="638b1-133">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="638b1-133">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





