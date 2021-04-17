---
title: Élément Duration (idleSettingsType)
description: Spécifie la durée pendant laquelle l’ordinateur doit être dans un état inactif avant que la tâche ne soit exécutée.
ms.assetid: 89584694-0685-44e2-b8b7-69e47ee28d5d
keywords:
- Élément Duration Planificateur de tâches
topic_type:
- apiref
api_name:
- Duration
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 31ad092693c72dcc33357f4b7e21436e2cba8af8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508433"
---
# <a name="duration-idlesettingstype-element"></a><span data-ttu-id="49d9f-104">Élément Duration (idleSettingsType)</span><span class="sxs-lookup"><span data-stu-id="49d9f-104">Duration (idleSettingsType) Element</span></span>

<span data-ttu-id="49d9f-105">Spécifie la durée pendant laquelle l’ordinateur doit être dans un état inactif avant que la tâche ne soit exécutée.</span><span class="sxs-lookup"><span data-stu-id="49d9f-105">Specifies how long the computer must be in an idle state before the task is run.</span></span> <span data-ttu-id="49d9f-106">Le format de cette chaîne est PnYnMnDTnHnMnS, où nY est le nombre d’années, nM est le nombre de mois, nD le nombre de jours, 't’est le séparateur de date/heure, nH est le nombre d’heures, nM est le nombre de minutes et nS est le nombre de secondes (par exemple, PT5M spécifie 5 minutes et P1M4DT2H5M spécifie un mois, quatre jours, deux heures et cinq minutes).</span><span class="sxs-lookup"><span data-stu-id="49d9f-106">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span> <span data-ttu-id="49d9f-107">La valeur minimale est d’une minute.</span><span class="sxs-lookup"><span data-stu-id="49d9f-107">The minimum value is one minute.</span></span> <span data-ttu-id="49d9f-108">Pour plus d’informations sur le type de durée, consultez <https://go.microsoft.com/fwlink/p/?linkid=106886> .</span><span class="sxs-lookup"><span data-stu-id="49d9f-108">For more information about the duration type, see <https://go.microsoft.com/fwlink/p/?linkid=106886>.</span></span>

``` syntax
<xs:element name="Duration"
    default="PT10M"
    minOccurs="0"
>
    <xs:simpleType>
        <xs:restriction
            base="duration"
        >
            <xs:minInclusive
                value="PT1M"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="49d9f-109">L’élément est défini par le type complexe [**idleSettingsType**](taskschedulerschema-idlesettingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="49d9f-109">The element is defined by the [**idleSettingsType**](taskschedulerschema-idlesettingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="49d9f-110">Élément parent</span><span class="sxs-lookup"><span data-stu-id="49d9f-110">Parent element</span></span>



| <span data-ttu-id="49d9f-111">Élément</span><span class="sxs-lookup"><span data-stu-id="49d9f-111">Element</span></span>                                                                       | <span data-ttu-id="49d9f-112">Dérivé de</span><span class="sxs-lookup"><span data-stu-id="49d9f-112">Derived from</span></span>                                                                 | <span data-ttu-id="49d9f-113">Description</span><span class="sxs-lookup"><span data-stu-id="49d9f-113">Description</span></span>                                                                                       |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="49d9f-114">**IdleSettings**</span><span class="sxs-lookup"><span data-stu-id="49d9f-114">**IdleSettings**</span></span>](taskschedulerschema-idlesettings-settingstype-element.md) | [<span data-ttu-id="49d9f-115">**idleSettingsType**</span><span class="sxs-lookup"><span data-stu-id="49d9f-115">**idleSettingsType**</span></span>](taskschedulerschema-idlesettingstype-complextype.md) | <span data-ttu-id="49d9f-116">Spécifie comment l’Planificateur de tâches effectue des tâches lorsque l’ordinateur est dans un état d’inactivité.</span><span class="sxs-lookup"><span data-stu-id="49d9f-116">Specifies how the Task Scheduler performs tasks when the computer is in an idle state.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="49d9f-117">Notes</span><span class="sxs-lookup"><span data-stu-id="49d9f-117">Remarks</span></span>

<span data-ttu-id="49d9f-118">Pour la programmation de script, ce paramètre inactif est spécifié à l’aide de la propriété [**IdleSettings. IdleDuration**](idlesettings-idleduration.md) .</span><span class="sxs-lookup"><span data-stu-id="49d9f-118">For script programming, this idle setting is specified using the [**IdleSettings.IdleDuration**](idlesettings-idleduration.md) property.</span></span>

<span data-ttu-id="49d9f-119">Pour la programmation en C++, ce paramètre inactif est spécifié à l’aide de la propriété [**IIdleSettings :: IdleDuration**](/windows/desktop/api/taskschd/nf-taskschd-iidlesettings-get_idleduration) .</span><span class="sxs-lookup"><span data-stu-id="49d9f-119">For C++ programming, this idle setting is specified using the [**IIdleSettings::IdleDuration**](/windows/desktop/api/taskschd/nf-taskschd-iidlesettings-get_idleduration) property.</span></span>

## <a name="examples"></a><span data-ttu-id="49d9f-120">Exemples</span><span class="sxs-lookup"><span data-stu-id="49d9f-120">Examples</span></span>

<span data-ttu-id="49d9f-121">Le code XML suivant définit un paramètre inactif qui autorise 5 minutes à démarrer la tâche.</span><span class="sxs-lookup"><span data-stu-id="49d9f-121">The following XML defines an idle setting that allows 5 minutes for the task to start.</span></span>


```XML
<IdleSettings>
    <Duration>PT5M</Duration>
</IdleSettings>
```



## <a name="requirements"></a><span data-ttu-id="49d9f-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="49d9f-122">Requirements</span></span>



| <span data-ttu-id="49d9f-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="49d9f-123">Requirement</span></span> | <span data-ttu-id="49d9f-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="49d9f-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="49d9f-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="49d9f-125">Minimum supported client</span></span><br/> | <span data-ttu-id="49d9f-126">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="49d9f-126">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="49d9f-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="49d9f-127">Minimum supported server</span></span><br/> | <span data-ttu-id="49d9f-128">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="49d9f-128">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="49d9f-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="49d9f-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49d9f-130">Éléments de schéma Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="49d9f-130">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="49d9f-131">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="49d9f-131">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





