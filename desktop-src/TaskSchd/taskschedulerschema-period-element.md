---
title: Élément period
description: Spécifie la fréquence à laquelle la tâche doit être démarrée pendant la maintenance automatique.
ms.assetid: E4BE2466-3119-41F8-8238-4627C28B26E5
keywords:
- Point, élément Planificateur de tâches
topic_type:
- apiref
api_name:
- Period
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7a507a9b0a8f97d1ae4e6c8df654a45d67b77767
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466983"
---
# <a name="period-element"></a><span data-ttu-id="b8052-104">Élément period</span><span class="sxs-lookup"><span data-stu-id="b8052-104">Period Element</span></span>

<span data-ttu-id="b8052-105">Spécifie la fréquence à laquelle la tâche doit être démarrée pendant la maintenance automatique.</span><span class="sxs-lookup"><span data-stu-id="b8052-105">Specifies how often the task needs to be started during Automatic maintenance.</span></span>

<span data-ttu-id="b8052-106">Le format de cette chaîne est *PnYnMnDTnHnMnS*, où *NY* est le nombre d’années, nm est le nombre de mois, *ND* est le nombre de jours, *T* est le séparateur de date/heure, *NH* est le nombre d’heures, *nm* est le nombre de minutes et *NS* est le nombre de secondes (par exemple, « PT5M » spécifie 5 minutes et « P1M4DT2H5M » indique un mois, quatre jours, deux heures et cinq minutes).</span><span class="sxs-lookup"><span data-stu-id="b8052-106">The format for this string is *PnYnMnDTnHnMnS*, where *nY* is the number of years, nM is the number of months, *nD* is the number of days, *T* is the date/time separator, *nH* is the number of hours, *nM* is the number of minutes, and *nS* is the number of seconds (for example, "PT5M" specifies 5 minutes and "P1M4DT2H5M" specifies one month, four days, two hours, and five minutes).</span></span> <span data-ttu-id="b8052-107">La valeur minimale est d’une minute.</span><span class="sxs-lookup"><span data-stu-id="b8052-107">The minimum value is one minute.</span></span> <span data-ttu-id="b8052-108">Pour plus d’informations sur le type de durée, consultez [XML Schema Part 2 : Datatypes Second Edition](https://www.w3.org/TR/xmlschema-2/#duration).</span><span class="sxs-lookup"><span data-stu-id="b8052-108">For more information about the duration type, see [XML Schema Part 2: Datatypes Second Edition](https://www.w3.org/TR/xmlschema-2/#duration).</span></span>

``` syntax
<xs:element name="Period"
    maxOccurs="1"
    minOccurs="1"
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

<span data-ttu-id="b8052-109">L’élément **period** est défini par le type complexe [**maintenanceSettingsType**](taskschedulerschema-maintenancesettingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="b8052-109">The **Period** element is defined by the [**maintenanceSettingsType**](taskschedulerschema-maintenancesettingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="b8052-110">Élément parent</span><span class="sxs-lookup"><span data-stu-id="b8052-110">Parent element</span></span>



| <span data-ttu-id="b8052-111">Élément</span><span class="sxs-lookup"><span data-stu-id="b8052-111">Element</span></span>                                                                                                                          | <span data-ttu-id="b8052-112">Dérivé de</span><span class="sxs-lookup"><span data-stu-id="b8052-112">Derived from</span></span>                                                                               | <span data-ttu-id="b8052-113">Description</span><span class="sxs-lookup"><span data-stu-id="b8052-113">Description</span></span>                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b8052-114">**MaintenanceSettings (maintenanceSettingsType)**</span><span class="sxs-lookup"><span data-stu-id="b8052-114">**MaintenanceSettings (maintenanceSettingsType)**</span></span>](taskschedulerschema-maintenancesettings-maintenancesettingstype-element.md) | [<span data-ttu-id="b8052-115">**maintenanceSettingsType**</span><span class="sxs-lookup"><span data-stu-id="b8052-115">**maintenanceSettingsType**</span></span>](taskschedulerschema-maintenancesettingstype-complextype.md) | <span data-ttu-id="b8052-116">Spécifie les paramètres de tâche que le planificateur de tâches utilisera pour démarrer la tâche pendant la maintenance automatique.</span><span class="sxs-lookup"><span data-stu-id="b8052-116">Specifies the task settings the Task scheduler will use to start task during Automatic maintenance.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="b8052-117">Notes</span><span class="sxs-lookup"><span data-stu-id="b8052-117">Remarks</span></span>

<span data-ttu-id="b8052-118">Pour la programmation en C++, ce paramètre inactif est spécifié à l’aide de la propriété [**IMaintenanceSettings ::P eriod**](/windows/desktop/api/Taskschd/nf-taskschd-imaintenancesettings-get_period) .</span><span class="sxs-lookup"><span data-stu-id="b8052-118">For C++ programming, this idle setting is specified using the [**IMaintenanceSettings::Period**](/windows/desktop/api/Taskschd/nf-taskschd-imaintenancesettings-get_period) property.</span></span>

## <a name="examples"></a><span data-ttu-id="b8052-119">Exemples</span><span class="sxs-lookup"><span data-stu-id="b8052-119">Examples</span></span>

<span data-ttu-id="b8052-120">Le code XML suivant définit la tâche de maintenance avec une exigence de périodicité définie sur 5 jours.</span><span class="sxs-lookup"><span data-stu-id="b8052-120">The following XML defines maintenance task with periodicity requirement set to 5 days.</span></span>


```XML
<MaintenanceSettings>
    <Period>P5D</Period>
</MaintenanceSettings>
```



## <a name="requirements"></a><span data-ttu-id="b8052-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b8052-121">Requirements</span></span>



| <span data-ttu-id="b8052-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b8052-122">Requirement</span></span> | <span data-ttu-id="b8052-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="b8052-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b8052-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b8052-124">Minimum supported client</span></span><br/> | <span data-ttu-id="b8052-125">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b8052-125">Windows 8 \[desktop apps only\]</span></span><br/>           |
| <span data-ttu-id="b8052-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b8052-126">Minimum supported server</span></span><br/> | <span data-ttu-id="b8052-127">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b8052-127">Windows Server 2012 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b8052-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b8052-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8052-129">Éléments de schéma Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="b8052-129">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="b8052-130">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="b8052-130">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





