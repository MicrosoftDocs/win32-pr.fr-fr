---
title: Élément StopOnIdleEnd (idleSettingsType)
description: Spécifie que l’Planificateur de tâches arrêtera la tâche si la condition d’inactivité se termine avant la fin de la tâche.
ms.assetid: 5e8e4fd9-bba1-4ede-a0b3-9f50feb1b6f3
keywords:
- Élément StopOnIdleEnd Planificateur de tâches
topic_type:
- apiref
api_name:
- TerminateOnIdleEnd
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a47a01d7d77f3dd20f055bce8e4bb12fad82c771
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942729"
---
# <a name="stoponidleend-idlesettingstype-element"></a><span data-ttu-id="ae2f7-104">Élément StopOnIdleEnd (idleSettingsType)</span><span class="sxs-lookup"><span data-stu-id="ae2f7-104">StopOnIdleEnd (idleSettingsType) Element</span></span>

<span data-ttu-id="ae2f7-105">Spécifie que l’Planificateur de tâches arrêtera la tâche si la condition d’inactivité se termine avant la fin de la tâche.</span><span class="sxs-lookup"><span data-stu-id="ae2f7-105">Specifies that the Task Scheduler will stop the task if the idle condition ends before the task is completed.</span></span>

``` syntax
<xs:element name="StopOnIdleEnd"
    type="boolean"
    minOccurs="0"
    default="true"
 />
```

<span data-ttu-id="ae2f7-106">L’élément **StopOnIdleEnd** est défini par le type complexe [**idleSettingsType**](taskschedulerschema-idlesettingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="ae2f7-106">The **StopOnIdleEnd** element is defined by the [**idleSettingsType**](taskschedulerschema-idlesettingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="ae2f7-107">Élément parent</span><span class="sxs-lookup"><span data-stu-id="ae2f7-107">Parent element</span></span>



| <span data-ttu-id="ae2f7-108">Élément</span><span class="sxs-lookup"><span data-stu-id="ae2f7-108">Element</span></span>                                                                       | <span data-ttu-id="ae2f7-109">Dérivé de</span><span class="sxs-lookup"><span data-stu-id="ae2f7-109">Derived from</span></span>                                                                 | <span data-ttu-id="ae2f7-110">Description</span><span class="sxs-lookup"><span data-stu-id="ae2f7-110">Description</span></span>                                                                                       |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ae2f7-111">**IdleSettings**</span><span class="sxs-lookup"><span data-stu-id="ae2f7-111">**IdleSettings**</span></span>](taskschedulerschema-idlesettings-settingstype-element.md) | [<span data-ttu-id="ae2f7-112">**idleSettingsType**</span><span class="sxs-lookup"><span data-stu-id="ae2f7-112">**idleSettingsType**</span></span>](taskschedulerschema-idlesettingstype-complextype.md) | <span data-ttu-id="ae2f7-113">Spécifie comment l’Planificateur de tâches effectue des tâches lorsque l’ordinateur est dans un état d’inactivité.</span><span class="sxs-lookup"><span data-stu-id="ae2f7-113">Specifies how the Task Scheduler performs tasks when the computer is in an idle state.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="ae2f7-114">Notes</span><span class="sxs-lookup"><span data-stu-id="ae2f7-114">Remarks</span></span>

<span data-ttu-id="ae2f7-115">Pour le développement C++, consultez la [**propriété StopOnIdleEnd de IIdleSettings**](/windows/desktop/api/taskschd/nf-taskschd-iidlesettings-get_stoponidleend).</span><span class="sxs-lookup"><span data-stu-id="ae2f7-115">For C++ development, see [**StopOnIdleEnd Property of IIdleSettings**](/windows/desktop/api/taskschd/nf-taskschd-iidlesettings-get_stoponidleend).</span></span>

<span data-ttu-id="ae2f7-116">Pour le développement de scripts, consultez [**IdleSettings. StopOnIdleEnd**](idlesettings-stoponidleend.md).</span><span class="sxs-lookup"><span data-stu-id="ae2f7-116">For script development, see [**IdleSettings.StopOnIdleEnd**](idlesettings-stoponidleend.md).</span></span>

## <a name="examples"></a><span data-ttu-id="ae2f7-117">Exemples</span><span class="sxs-lookup"><span data-stu-id="ae2f7-117">Examples</span></span>

<span data-ttu-id="ae2f7-118">Le code XML suivant définit un paramètre inactif qui indique que la tâche ne doit pas être exécutée lorsque la condition d’inactivité se termine.</span><span class="sxs-lookup"><span data-stu-id="ae2f7-118">The following XML defines an idle setting that indicates the task should not be performed when the idle condition ends.</span></span>


```XML
<IdleSettings>
    <StopOnIdleEnd>false</StopOnIdleEnd>
</IdleSettings>
```



## <a name="requirements"></a><span data-ttu-id="ae2f7-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ae2f7-119">Requirements</span></span>



| <span data-ttu-id="ae2f7-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ae2f7-120">Requirement</span></span> | <span data-ttu-id="ae2f7-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="ae2f7-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ae2f7-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ae2f7-122">Minimum supported client</span></span><br/> | <span data-ttu-id="ae2f7-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ae2f7-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="ae2f7-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ae2f7-124">Minimum supported server</span></span><br/> | <span data-ttu-id="ae2f7-125">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ae2f7-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ae2f7-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ae2f7-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae2f7-127">Éléments de schéma Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="ae2f7-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





