---
title: Comgèrer (actionGroup) (élément)
description: Spécifie une action qui déclenche un gestionnaire.
ms.assetid: 18f16873-3879-4a3b-b8f2-17cc84647e25
keywords:
- Planificateur de tâches d’élément comgérer
topic_type:
- apiref
api_name:
- ComHandler
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2269464efb09e8c513ab2bdebb24744a6b32a671
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942583"
---
# <a name="comhandler-actiongroup-element"></a><span data-ttu-id="d8c4d-104">Comgèrer (actionGroup) (élément)</span><span class="sxs-lookup"><span data-stu-id="d8c4d-104">ComHandler (actionGroup) Element</span></span>

<span data-ttu-id="d8c4d-105">Spécifie une action qui déclenche un gestionnaire.</span><span class="sxs-lookup"><span data-stu-id="d8c4d-105">Specifies an action that fires a handler.</span></span>

``` syntax
<xs:element name="ComHandler"
    type="comHandlerType"
 />
```

<span data-ttu-id="d8c4d-106">L’élément **comgérer** est défini par [**actionGroup**](taskschedulerschema-actiongroup-group.md) .</span><span class="sxs-lookup"><span data-stu-id="d8c4d-106">The **ComHandler** element is defined by the [**actionGroup**](taskschedulerschema-actiongroup-group.md) .</span></span>

## <a name="parent-element"></a><span data-ttu-id="d8c4d-107">Élément parent</span><span class="sxs-lookup"><span data-stu-id="d8c4d-107">Parent element</span></span>



| <span data-ttu-id="d8c4d-108">Élément</span><span class="sxs-lookup"><span data-stu-id="d8c4d-108">Element</span></span>                                                         | <span data-ttu-id="d8c4d-109">Dérivé de</span><span class="sxs-lookup"><span data-stu-id="d8c4d-109">Derived from</span></span>                                                       | <span data-ttu-id="d8c4d-110">Description</span><span class="sxs-lookup"><span data-stu-id="d8c4d-110">Description</span></span>                                            |
|-----------------------------------------------------------------|--------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="d8c4d-111">**Actions**</span><span class="sxs-lookup"><span data-stu-id="d8c4d-111">**Actions**</span></span>](taskschedulerschema-actions-tasktype-element.md) | [<span data-ttu-id="d8c4d-112">**actionsType**</span><span class="sxs-lookup"><span data-stu-id="d8c4d-112">**actionsType**</span></span>](taskschedulerschema-actionstype-complextype.md) | <span data-ttu-id="d8c4d-113">Contient les actions effectuées par la tâche.</span><span class="sxs-lookup"><span data-stu-id="d8c4d-113">Contains the actions performed by the task.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="d8c4d-114">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="d8c4d-114">Child elements</span></span>



| <span data-ttu-id="d8c4d-115">Élément</span><span class="sxs-lookup"><span data-stu-id="d8c4d-115">Element</span></span>                                                               | <span data-ttu-id="d8c4d-116">Type</span><span class="sxs-lookup"><span data-stu-id="d8c4d-116">Type</span></span>                                                         | <span data-ttu-id="d8c4d-117">Description</span><span class="sxs-lookup"><span data-stu-id="d8c4d-117">Description</span></span>                                                       |
|-----------------------------------------------------------------------|--------------------------------------------------------------|-------------------------------------------------------------------|
| [<span data-ttu-id="d8c4d-118">**ClassId**</span><span class="sxs-lookup"><span data-stu-id="d8c4d-118">**ClassId**</span></span>](taskschedulerschema-classid-comhandlertype-element.md) | [<span data-ttu-id="d8c4d-119">**guidType**</span><span class="sxs-lookup"><span data-stu-id="d8c4d-119">**guidType**</span></span>](taskschedulerschema-guidtype-simpletype.md)  | <span data-ttu-id="d8c4d-120">Spécifie l’identificateur de la classe de gestionnaire.</span><span class="sxs-lookup"><span data-stu-id="d8c4d-120">Specifies the identifier of the handler class.</span></span><br/>         |
| [<span data-ttu-id="d8c4d-121">**Données**</span><span class="sxs-lookup"><span data-stu-id="d8c4d-121">**Data**</span></span>](taskschedulerschema-data-comhandlertype-element.md)       | [<span data-ttu-id="d8c4d-122">**Décimal**</span><span class="sxs-lookup"><span data-stu-id="d8c4d-122">**dataType**</span></span>](taskschedulerschema-datatype-complextype.md) | <span data-ttu-id="d8c4d-123">Spécifie des données supplémentaires associées au gestionnaire.</span><span class="sxs-lookup"><span data-stu-id="d8c4d-123">Specifies additional data associated with the handler.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="d8c4d-124">Notes</span><span class="sxs-lookup"><span data-stu-id="d8c4d-124">Remarks</span></span>

<span data-ttu-id="d8c4d-125">Les applications définissent une action de gestionnaire COM à l’aide de l’interface [**IComHandlerAction**](/windows/desktop/api/taskschd/nn-taskschd-icomhandleraction) .</span><span class="sxs-lookup"><span data-stu-id="d8c4d-125">Applications define a COM handler action using the [**IComHandlerAction**](/windows/desktop/api/taskschd/nn-taskschd-icomhandleraction) interface.</span></span>

### <a name="attributes"></a><span data-ttu-id="d8c4d-126">Attributs</span><span class="sxs-lookup"><span data-stu-id="d8c4d-126">Attributes</span></span>

<span data-ttu-id="d8c4d-127">L’attribut suivant est défini par le type complexe [**actionBaseType**](taskschedulerschema-actionbasetype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="d8c4d-127">The following attribute is defined by the [**actionBaseType**](taskschedulerschema-actionbasetype-complextype.md) complex type.</span></span>

-   <span data-ttu-id="d8c4d-128">ID : identificateur de l’action effectuée par la tâche.</span><span class="sxs-lookup"><span data-stu-id="d8c4d-128">ID: Identifier of the action performed by the task.</span></span>

## <a name="examples"></a><span data-ttu-id="d8c4d-129">Exemples</span><span class="sxs-lookup"><span data-stu-id="d8c4d-129">Examples</span></span>

<span data-ttu-id="d8c4d-130">Le code XML suivant définit une action de gestionnaire COM.</span><span class="sxs-lookup"><span data-stu-id="d8c4d-130">The following XML defines a COM handler action.</span></span>


```XML
<Actions>
    <ComHandler>
        <ClassId></ClassId>
        <Data></Data>
    </ComHandler>
</Actions>
```



## <a name="requirements"></a><span data-ttu-id="d8c4d-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d8c4d-131">Requirements</span></span>



| <span data-ttu-id="d8c4d-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d8c4d-132">Requirement</span></span> | <span data-ttu-id="d8c4d-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="d8c4d-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d8c4d-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d8c4d-134">Minimum supported client</span></span><br/> | <span data-ttu-id="d8c4d-135">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d8c4d-135">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="d8c4d-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d8c4d-136">Minimum supported server</span></span><br/> | <span data-ttu-id="d8c4d-137">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d8c4d-137">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d8c4d-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d8c4d-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8c4d-139">Éléments de schéma Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="d8c4d-139">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





