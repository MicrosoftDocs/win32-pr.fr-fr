---
title: Élément DisallowStartIfOnBatteries (settingsType)
description: Spécifie que la tâche ne sera pas démarrée si l’ordinateur fonctionne sur batterie.
ms.assetid: 48c0fd32-4441-4628-8090-c736f2945b4d
keywords:
- Élément DisallowStartIfOnBatteries Planificateur de tâches
topic_type:
- apiref
api_name:
- DisallowStartIfOnBatteries
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8a8d93bcabd0e121c44f4a7212d11491624a08d0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743773"
---
# <a name="disallowstartifonbatteries-settingstype-element"></a><span data-ttu-id="b981b-104">Élément DisallowStartIfOnBatteries (settingsType)</span><span class="sxs-lookup"><span data-stu-id="b981b-104">DisallowStartIfOnBatteries (settingsType) Element</span></span>

<span data-ttu-id="b981b-105">Spécifie que la tâche ne sera pas démarrée si l’ordinateur fonctionne sur batterie.</span><span class="sxs-lookup"><span data-stu-id="b981b-105">Specifies that the task will not be started if the computer is running on batteries.</span></span>

``` syntax
<xs:element name="DisallowStartIfOnBatteries"
    type="boolean"
 />
```

<span data-ttu-id="b981b-106">L’élément **DisallowStartIfOnBatteries** est défini par le type complexe [**settingsType**](taskschedulerschema-settingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="b981b-106">The **DisallowStartIfOnBatteries** element is defined by the [**settingsType**](taskschedulerschema-settingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="b981b-107">Élément parent</span><span class="sxs-lookup"><span data-stu-id="b981b-107">Parent element</span></span>



| <span data-ttu-id="b981b-108">Élément</span><span class="sxs-lookup"><span data-stu-id="b981b-108">Element</span></span>                                                           | <span data-ttu-id="b981b-109">Dérivé de</span><span class="sxs-lookup"><span data-stu-id="b981b-109">Derived from</span></span>                                                         | <span data-ttu-id="b981b-110">Description</span><span class="sxs-lookup"><span data-stu-id="b981b-110">Description</span></span>                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="b981b-111">**Paramètres**</span><span class="sxs-lookup"><span data-stu-id="b981b-111">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="b981b-112">**settingsType**</span><span class="sxs-lookup"><span data-stu-id="b981b-112">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md) | <span data-ttu-id="b981b-113">Contient les paramètres que le Planificateur de tâches utilise pour effectuer la tâche.</span><span class="sxs-lookup"><span data-stu-id="b981b-113">Contains the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="b981b-114">Notes</span><span class="sxs-lookup"><span data-stu-id="b981b-114">Remarks</span></span>

<span data-ttu-id="b981b-115">Le paramètre par défaut de cet élément est true.</span><span class="sxs-lookup"><span data-stu-id="b981b-115">The default setting for this element is True.</span></span>

<span data-ttu-id="b981b-116">Pour le développement de script, ces informations sont accessibles via la propriété [**TaskSettings. DisallowStartIfOnBatteries**](tasksettings-disallowstartifonbatteries.md) .</span><span class="sxs-lookup"><span data-stu-id="b981b-116">For scripting development, this information is accessed through the [**TaskSettings.DisallowStartIfOnBatteries**](tasksettings-disallowstartifonbatteries.md) property.</span></span>

<span data-ttu-id="b981b-117">Pour le développement C++, ces informations sont accessibles par le biais de la propriété [**ITaskSettings ::D isallowstartifonbatteries**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_disallowstartifonbatteries) .</span><span class="sxs-lookup"><span data-stu-id="b981b-117">For C++ development, this information is accessed through the [**ITaskSettings::DisallowStartIfOnBatteries**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_disallowstartifonbatteries) property.</span></span>

## <a name="examples"></a><span data-ttu-id="b981b-118">Exemples</span><span class="sxs-lookup"><span data-stu-id="b981b-118">Examples</span></span>

<span data-ttu-id="b981b-119">Le code XML suivant définit un élément Settings qui ne permet pas à la tâche de s’exécuter si l’ordinateur s’exécute sur des batteries.</span><span class="sxs-lookup"><span data-stu-id="b981b-119">The following XML defines a settings element that does not allow the task to run if the computer is running on batteries.</span></span>


```XML
<Settings>
    <DisallowStartIfOnBatteries>true</DisallowStartIfOnBatteries>
</Settings>
        
```



## <a name="requirements"></a><span data-ttu-id="b981b-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b981b-120">Requirements</span></span>



| <span data-ttu-id="b981b-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b981b-121">Requirement</span></span> | <span data-ttu-id="b981b-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="b981b-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b981b-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b981b-123">Minimum supported client</span></span><br/> | <span data-ttu-id="b981b-124">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b981b-124">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="b981b-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b981b-125">Minimum supported server</span></span><br/> | <span data-ttu-id="b981b-126">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b981b-126">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b981b-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b981b-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b981b-128">Éléments de schéma Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="b981b-128">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





