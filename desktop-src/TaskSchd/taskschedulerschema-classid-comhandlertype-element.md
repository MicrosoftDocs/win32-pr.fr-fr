---
title: ClassId (comHandlerType) (élément)
description: Spécifie l’identificateur de la classe de gestionnaire.
ms.assetid: 38ebcc39-85f2-4f61-8cb6-556c242a63d9
keywords:
- ClassId, élément Planificateur de tâches
topic_type:
- apiref
api_name:
- ClassId
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c89af2f39ae6a4a529fe7a728cf4b821245aa034
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466990"
---
# <a name="classid-comhandlertype-element"></a><span data-ttu-id="7cb7e-104">ClassId (comHandlerType) (élément)</span><span class="sxs-lookup"><span data-stu-id="7cb7e-104">ClassId (comHandlerType) Element</span></span>

<span data-ttu-id="7cb7e-105">Spécifie l’identificateur de la classe de gestionnaire.</span><span class="sxs-lookup"><span data-stu-id="7cb7e-105">Specifies the identifier of the handler class.</span></span>

``` syntax
<xs:element name="ClassId"
    type="guidType"
 />
```

<span data-ttu-id="7cb7e-106">L’élément **ClassID** est défini par le type complexe [**comHandlerType**](taskschedulerschema-comhandlertype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="7cb7e-106">The **ClassId** element is defined by the [**comHandlerType**](taskschedulerschema-comhandlertype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="7cb7e-107">Élément parent</span><span class="sxs-lookup"><span data-stu-id="7cb7e-107">Parent element</span></span>



| <span data-ttu-id="7cb7e-108">Élément</span><span class="sxs-lookup"><span data-stu-id="7cb7e-108">Element</span></span>                                                                  | <span data-ttu-id="7cb7e-109">Dérivé de</span><span class="sxs-lookup"><span data-stu-id="7cb7e-109">Derived from</span></span>                                                             | <span data-ttu-id="7cb7e-110">Description</span><span class="sxs-lookup"><span data-stu-id="7cb7e-110">Description</span></span>                                          |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------|
| [<span data-ttu-id="7cb7e-111">**Comgérer**</span><span class="sxs-lookup"><span data-stu-id="7cb7e-111">**ComHandler**</span></span>](taskschedulerschema-comhandler-actiongroup-element.md) | [<span data-ttu-id="7cb7e-112">**comHandlerType**</span><span class="sxs-lookup"><span data-stu-id="7cb7e-112">**comHandlerType**</span></span>](taskschedulerschema-comhandlertype-complextype.md) | <span data-ttu-id="7cb7e-113">Spécifie une action qui déclenche un gestionnaire.</span><span class="sxs-lookup"><span data-stu-id="7cb7e-113">Specifies an action that fires a handler.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="7cb7e-114">Notes</span><span class="sxs-lookup"><span data-stu-id="7cb7e-114">Remarks</span></span>

<span data-ttu-id="7cb7e-115">Les applications définissent l’identificateur de classe à l’aide de la propriété [**ClassID**](/windows/desktop/api/taskschd/nf-taskschd-icomhandleraction-get_classid) de l’interface [**IComHandlerAction**](/windows/desktop/api/taskschd/nn-taskschd-icomhandleraction) .</span><span class="sxs-lookup"><span data-stu-id="7cb7e-115">Applications define the class identifier using the [**ClassId**](/windows/desktop/api/taskschd/nf-taskschd-icomhandleraction-get_classid) property of the [**IComHandlerAction**](/windows/desktop/api/taskschd/nn-taskschd-icomhandleraction) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="7cb7e-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7cb7e-116">Requirements</span></span>



| <span data-ttu-id="7cb7e-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7cb7e-117">Requirement</span></span> | <span data-ttu-id="7cb7e-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="7cb7e-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="7cb7e-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7cb7e-119">Minimum supported client</span></span><br/> | <span data-ttu-id="7cb7e-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7cb7e-120">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="7cb7e-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7cb7e-121">Minimum supported server</span></span><br/> | <span data-ttu-id="7cb7e-122">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7cb7e-122">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7cb7e-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7cb7e-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7cb7e-124">Éléments de schéma Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="7cb7e-124">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





