---
title: Élément Hidden (settingsType)
description: Spécifie que la tâche ne sera pas visible dans l’interface utilisateur par défaut.
ms.assetid: a08c270f-6d4e-4473-9538-c1e1e21b3b10
keywords:
- Élément masqué Planificateur de tâches
topic_type:
- apiref
api_name:
- Hidden
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ef5ad479fe3107ed8fa79f0f86307254a9f33c4d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510579"
---
# <a name="hidden-settingstype-element"></a><span data-ttu-id="d0a1e-104">Élément Hidden (settingsType)</span><span class="sxs-lookup"><span data-stu-id="d0a1e-104">Hidden (settingsType) Element</span></span>

<span data-ttu-id="d0a1e-105">Spécifie que la tâche ne sera pas visible dans l’interface utilisateur par défaut.</span><span class="sxs-lookup"><span data-stu-id="d0a1e-105">Specifies that the task will not be visible in the UI by default.</span></span> <span data-ttu-id="d0a1e-106">Toutefois, les administrateurs peuvent remplacer ce paramètre à l’aide d’un « commutateur maître » qui rend toutes les tâches visibles dans l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="d0a1e-106">However, administrators can override this setting through the use of a "master switch" that makes all tasks visible in the UI.</span></span>

``` syntax
<xs:element name="Hidden"
    type="boolean"
    default="false"
    minOccurs="0"
 />
```

<span data-ttu-id="d0a1e-107">L’élément **masqué** est défini par le type complexe [**settingsType**](taskschedulerschema-settingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="d0a1e-107">The **Hidden** element is defined by the [**settingsType**](taskschedulerschema-settingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="d0a1e-108">Élément parent</span><span class="sxs-lookup"><span data-stu-id="d0a1e-108">Parent element</span></span>



| <span data-ttu-id="d0a1e-109">Élément</span><span class="sxs-lookup"><span data-stu-id="d0a1e-109">Element</span></span>                                                           | <span data-ttu-id="d0a1e-110">Dérivé de</span><span class="sxs-lookup"><span data-stu-id="d0a1e-110">Derived from</span></span>                                                         | <span data-ttu-id="d0a1e-111">Description</span><span class="sxs-lookup"><span data-stu-id="d0a1e-111">Description</span></span>                                                                    |
|-------------------------------------------------------------------|----------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="d0a1e-112">**Paramètres**</span><span class="sxs-lookup"><span data-stu-id="d0a1e-112">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="d0a1e-113">**settingsType**</span><span class="sxs-lookup"><span data-stu-id="d0a1e-113">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md) | <span data-ttu-id="d0a1e-114">Contient les paramètres que Planificateur de tâches utilise pour effectuer la tâche.</span><span class="sxs-lookup"><span data-stu-id="d0a1e-114">Contains the settings that Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="d0a1e-115">Notes</span><span class="sxs-lookup"><span data-stu-id="d0a1e-115">Remarks</span></span>

<span data-ttu-id="d0a1e-116">Pour le développement C++, consultez la [**propriété Hidden de ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_hidden).</span><span class="sxs-lookup"><span data-stu-id="d0a1e-116">For C++ development, see [**Hidden Property of ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_hidden).</span></span>

<span data-ttu-id="d0a1e-117">Pour le développement de scripts, consultez [**TaskSettings. Hidden**](tasksettings-hidden.md).</span><span class="sxs-lookup"><span data-stu-id="d0a1e-117">For script development, see [**TaskSettings.Hidden**](tasksettings-hidden.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d0a1e-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d0a1e-118">Requirements</span></span>



| <span data-ttu-id="d0a1e-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d0a1e-119">Requirement</span></span> | <span data-ttu-id="d0a1e-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="d0a1e-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d0a1e-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d0a1e-121">Minimum supported client</span></span><br/> | <span data-ttu-id="d0a1e-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d0a1e-122">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="d0a1e-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d0a1e-123">Minimum supported server</span></span><br/> | <span data-ttu-id="d0a1e-124">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d0a1e-124">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d0a1e-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d0a1e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0a1e-126">Éléments de schéma Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="d0a1e-126">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





