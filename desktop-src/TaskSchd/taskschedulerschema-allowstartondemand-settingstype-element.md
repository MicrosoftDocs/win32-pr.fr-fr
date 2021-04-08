---
title: Élément AllowStartOnDemand (settingsType)
description: Spécifie que la tâche peut être démarrée à l’aide de la commande exécuter ou du menu contextuel.
ms.assetid: 5a0f0842-9f09-4d52-bed2-45740945d9a5
keywords:
- Élément AllowStartOnDemand Planificateur de tâches
topic_type:
- apiref
api_name:
- AllowStartOnDemand
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ec396bf10efbd11024fe39e57bdf05025db0e610
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941825"
---
# <a name="allowstartondemand-settingstype-element"></a><span data-ttu-id="ef9db-104">Élément AllowStartOnDemand (settingsType)</span><span class="sxs-lookup"><span data-stu-id="ef9db-104">AllowStartOnDemand (settingsType) Element</span></span>

<span data-ttu-id="ef9db-105">Spécifie que la tâche peut être démarrée à l’aide de la commande exécuter ou du menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="ef9db-105">Specifies that the task can be started using either the Run command or the Context menu.</span></span>

``` syntax
<xs:element name="AllowStartOnDemand"
    type="boolean"
    minOccurs="0"
    default="true"
 />
```

<span data-ttu-id="ef9db-106">L’élément **AllowStartOnDemand** est défini par le type complexe [**settingsType**](taskschedulerschema-settingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="ef9db-106">The **AllowStartOnDemand** element is defined by the [**settingsType**](taskschedulerschema-settingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="ef9db-107">Élément parent</span><span class="sxs-lookup"><span data-stu-id="ef9db-107">Parent element</span></span>



| <span data-ttu-id="ef9db-108">Élément</span><span class="sxs-lookup"><span data-stu-id="ef9db-108">Element</span></span>                                                           | <span data-ttu-id="ef9db-109">Dérivé de</span><span class="sxs-lookup"><span data-stu-id="ef9db-109">Derived from</span></span>                                                         | <span data-ttu-id="ef9db-110">Description</span><span class="sxs-lookup"><span data-stu-id="ef9db-110">Description</span></span>                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="ef9db-111">**Paramètres**</span><span class="sxs-lookup"><span data-stu-id="ef9db-111">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="ef9db-112">**settingsType**</span><span class="sxs-lookup"><span data-stu-id="ef9db-112">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md) | <span data-ttu-id="ef9db-113">Contient les paramètres que le Planificateur de tâches utilise pour effectuer la tâche.</span><span class="sxs-lookup"><span data-stu-id="ef9db-113">Contains the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="ef9db-114">Notes</span><span class="sxs-lookup"><span data-stu-id="ef9db-114">Remarks</span></span>

<span data-ttu-id="ef9db-115">Lorsque cet élément est défini sur true, la tâche peut être démarrée indépendamment du moment où les déclencheurs démarrent la tâche.</span><span class="sxs-lookup"><span data-stu-id="ef9db-115">When this element is set to True, the task can be started independently of when any triggers start the task.</span></span>

<span data-ttu-id="ef9db-116">Pour le développement C++, consultez la [**propriété AllowDemandStart de ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_allowdemandstart).</span><span class="sxs-lookup"><span data-stu-id="ef9db-116">For C++ development, see the [**AllowDemandStart property of ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_allowdemandstart).</span></span>

<span data-ttu-id="ef9db-117">Pour le développement de scripts, consultez [**TaskSettings. AllowDemandStart**](tasksettings-allowdemandstart.md).</span><span class="sxs-lookup"><span data-stu-id="ef9db-117">For script development, see [**TaskSettings.AllowDemandStart**](tasksettings-allowdemandstart.md).</span></span>

## <a name="examples"></a><span data-ttu-id="ef9db-118">Exemples</span><span class="sxs-lookup"><span data-stu-id="ef9db-118">Examples</span></span>

<span data-ttu-id="ef9db-119">Pour obtenir un exemple complet du code XML d’une tâche qui autorise le démarrage à la demande, consultez [exemple de déclenchement de temps (XML)](time-trigger-example--xml-.md).</span><span class="sxs-lookup"><span data-stu-id="ef9db-119">For a complete example of the XML for a task that allows demand start, see [Time Trigger Example (XML)](time-trigger-example--xml-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ef9db-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ef9db-120">Requirements</span></span>



| <span data-ttu-id="ef9db-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ef9db-121">Requirement</span></span> | <span data-ttu-id="ef9db-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="ef9db-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ef9db-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ef9db-123">Minimum supported client</span></span><br/> | <span data-ttu-id="ef9db-124">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ef9db-124">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="ef9db-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ef9db-125">Minimum supported server</span></span><br/> | <span data-ttu-id="ef9db-126">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ef9db-126">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ef9db-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ef9db-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef9db-128">Éléments de schéma Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="ef9db-128">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





