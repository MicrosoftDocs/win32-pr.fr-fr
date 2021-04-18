---
title: Élément WaitTimeout (idleSettingsType)
description: Spécifie la durée pendant laquelle le Planificateur de tâches attendra qu’une condition d’inactivité se produise.
ms.assetid: 6a4cc80d-adc2-47a7-946f-a9f12eeb35a4
keywords:
- Élément WaitTimeout Planificateur de tâches
topic_type:
- apiref
api_name:
- WaitTimeout
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 16f71a014358a8e0520274d1ff853cf6146aa05d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509042"
---
# <a name="waittimeout-idlesettingstype-element"></a><span data-ttu-id="e92a1-104">Élément WaitTimeout (idleSettingsType)</span><span class="sxs-lookup"><span data-stu-id="e92a1-104">WaitTimeout (idleSettingsType) Element</span></span>

<span data-ttu-id="e92a1-105">Spécifie la durée pendant laquelle le Planificateur de tâches attendra qu’une condition d’inactivité se produise.</span><span class="sxs-lookup"><span data-stu-id="e92a1-105">Specifies the amount of time that the Task Scheduler will wait for an idle condition to occur.</span></span> <span data-ttu-id="e92a1-106">Si aucune valeur n’est spécifiée pour cet élément, le service Planificateur de tâches attend indéfiniment qu’une condition d’inactivité se produise.</span><span class="sxs-lookup"><span data-stu-id="e92a1-106">If no value is specified for this element, then the Task Scheduler service will wait indefinitely for an idle condition to occur.</span></span> <span data-ttu-id="e92a1-107">Le format de cette chaîne est PnYnMnDTnHnMnS, où nY est le nombre d’années, nM est le nombre de mois, nD le nombre de jours, 't’est le séparateur de date/heure, nH est le nombre d’heures, nM est le nombre de minutes et nS est le nombre de secondes (par exemple, PT5M spécifie 5 minutes et P1M4DT2H5M spécifie un mois, quatre jours, deux heures et cinq minutes).</span><span class="sxs-lookup"><span data-stu-id="e92a1-107">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span> <span data-ttu-id="e92a1-108">Pour plus d’informations sur le type de durée, consultez <https://go.microsoft.com/fwlink/p/?linkid=106886> .</span><span class="sxs-lookup"><span data-stu-id="e92a1-108">For more information about the duration type, see <https://go.microsoft.com/fwlink/p/?linkid=106886>.</span></span> <span data-ttu-id="e92a1-109">La durée minimale autorisée est de 1 minute.</span><span class="sxs-lookup"><span data-stu-id="e92a1-109">The minimum time allowed is 1 minute.</span></span>

``` syntax
<xs:element name="WaitTimeout"
    default="PT1H"
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

<span data-ttu-id="e92a1-110">L’élément est défini par le type complexe [**idleSettingsType**](taskschedulerschema-idlesettingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="e92a1-110">The element is defined by the [**idleSettingsType**](taskschedulerschema-idlesettingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="e92a1-111">Élément parent</span><span class="sxs-lookup"><span data-stu-id="e92a1-111">Parent element</span></span>



| <span data-ttu-id="e92a1-112">Élément</span><span class="sxs-lookup"><span data-stu-id="e92a1-112">Element</span></span>                                                                       | <span data-ttu-id="e92a1-113">Dérivé de</span><span class="sxs-lookup"><span data-stu-id="e92a1-113">Derived from</span></span>                                                                 | <span data-ttu-id="e92a1-114">Description</span><span class="sxs-lookup"><span data-stu-id="e92a1-114">Description</span></span>                                                                                       |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e92a1-115">**IdleSettings**</span><span class="sxs-lookup"><span data-stu-id="e92a1-115">**IdleSettings**</span></span>](taskschedulerschema-idlesettings-settingstype-element.md) | [<span data-ttu-id="e92a1-116">**idleSettingsType**</span><span class="sxs-lookup"><span data-stu-id="e92a1-116">**idleSettingsType**</span></span>](taskschedulerschema-idlesettingstype-complextype.md) | <span data-ttu-id="e92a1-117">Spécifie comment l’Planificateur de tâches effectue des tâches lorsque l’ordinateur est dans un état d’inactivité.</span><span class="sxs-lookup"><span data-stu-id="e92a1-117">Specifies how the Task Scheduler performs tasks when the computer is in an idle state.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="e92a1-118">Notes</span><span class="sxs-lookup"><span data-stu-id="e92a1-118">Remarks</span></span>

<span data-ttu-id="e92a1-119">Pour le développement de scripts, ce paramètre inactif est spécifié à l’aide de la propriété [**IdleSettings. WaitTimeout**](idlesettings-waittimeout.md) .</span><span class="sxs-lookup"><span data-stu-id="e92a1-119">For script development, this idle setting is specified using the [**IdleSettings.WaitTimeout**](idlesettings-waittimeout.md) property.</span></span>

<span data-ttu-id="e92a1-120">Pour le développement C++, ce paramètre inactif est spécifié à l’aide de la propriété [**IIdleSettings :: WaitTimeout**](/windows/desktop/api/taskschd/nf-taskschd-iidlesettings-get_waittimeout) .</span><span class="sxs-lookup"><span data-stu-id="e92a1-120">For C++ development, this idle setting is specified using the [**IIdleSettings::WaitTimeout**](/windows/desktop/api/taskschd/nf-taskschd-iidlesettings-get_waittimeout) property.</span></span>

## <a name="examples"></a><span data-ttu-id="e92a1-121">Exemples</span><span class="sxs-lookup"><span data-stu-id="e92a1-121">Examples</span></span>

<span data-ttu-id="e92a1-122">Le code XML suivant définit un paramètre inactif qui attend 24 heures qu’une condition d’inactivité se produise.</span><span class="sxs-lookup"><span data-stu-id="e92a1-122">The following XML defines an idle setting that waits 24 hours for an idle condition to occur.</span></span>


```XML
<IdleSettings>
    <WaitTimeout>PT24H</WaitTimeout>
</IdleSettings>
```



## <a name="requirements"></a><span data-ttu-id="e92a1-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e92a1-123">Requirements</span></span>



| <span data-ttu-id="e92a1-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e92a1-124">Requirement</span></span> | <span data-ttu-id="e92a1-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="e92a1-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e92a1-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e92a1-126">Minimum supported client</span></span><br/> | <span data-ttu-id="e92a1-127">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e92a1-127">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="e92a1-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e92a1-128">Minimum supported server</span></span><br/> | <span data-ttu-id="e92a1-129">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e92a1-129">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e92a1-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e92a1-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e92a1-131">Éléments de schéma Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="e92a1-131">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="e92a1-132">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="e92a1-132">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





