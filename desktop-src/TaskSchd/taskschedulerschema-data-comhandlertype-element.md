---
title: Élément Data (comHandlerType)
description: Spécifie des données supplémentaires associées au gestionnaire.
ms.assetid: 352cb92b-54bb-4bb0-8a43-123c88c80962
keywords:
- Planificateur de tâches d’élément de données
topic_type:
- apiref
api_name:
- Data
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d009005dc2bb889c8bd9e34e84d853665310330a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942582"
---
# <a name="data-comhandlertype-element"></a><span data-ttu-id="e859b-104">Élément Data (comHandlerType)</span><span class="sxs-lookup"><span data-stu-id="e859b-104">Data (comHandlerType) Element</span></span>

<span data-ttu-id="e859b-105">Spécifie des données supplémentaires associées au gestionnaire.</span><span class="sxs-lookup"><span data-stu-id="e859b-105">Specifies additional data associated with the handler.</span></span>

``` syntax
<xs:element name="Data"
    type="dataType"
 />
```

<span data-ttu-id="e859b-106">L’élément de **données** est défini par le type complexe [**comHandlerType**](taskschedulerschema-comhandlertype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="e859b-106">The **Data** element is defined by the [**comHandlerType**](taskschedulerschema-comhandlertype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="e859b-107">Élément parent</span><span class="sxs-lookup"><span data-stu-id="e859b-107">Parent element</span></span>



| <span data-ttu-id="e859b-108">Élément</span><span class="sxs-lookup"><span data-stu-id="e859b-108">Element</span></span>                                                                  | <span data-ttu-id="e859b-109">Dérivé de</span><span class="sxs-lookup"><span data-stu-id="e859b-109">Derived from</span></span>                                                             | <span data-ttu-id="e859b-110">Description</span><span class="sxs-lookup"><span data-stu-id="e859b-110">Description</span></span>                                          |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------|
| [<span data-ttu-id="e859b-111">**Comgérer**</span><span class="sxs-lookup"><span data-stu-id="e859b-111">**ComHandler**</span></span>](taskschedulerschema-comhandler-actiongroup-element.md) | [<span data-ttu-id="e859b-112">**comHandlerType**</span><span class="sxs-lookup"><span data-stu-id="e859b-112">**comHandlerType**</span></span>](taskschedulerschema-comhandlertype-complextype.md) | <span data-ttu-id="e859b-113">Spécifie une action qui déclenche un gestionnaire.</span><span class="sxs-lookup"><span data-stu-id="e859b-113">Specifies an action that fires a handler.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="e859b-114">Notes</span><span class="sxs-lookup"><span data-stu-id="e859b-114">Remarks</span></span>

<span data-ttu-id="e859b-115">Les applications définissent les données du gestionnaire à l’aide de la propriété [**Data**](/windows/desktop/api/taskschd/nf-taskschd-icomhandleraction-get_data) de l’interface [**IComHandlerAction**](/windows/desktop/api/taskschd/nn-taskschd-icomhandleraction) .</span><span class="sxs-lookup"><span data-stu-id="e859b-115">Applications define the handler data using the [**Data**](/windows/desktop/api/taskschd/nf-taskschd-icomhandleraction-get_data) property of the [**IComHandlerAction**](/windows/desktop/api/taskschd/nn-taskschd-icomhandleraction) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="e859b-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e859b-116">Requirements</span></span>



| <span data-ttu-id="e859b-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e859b-117">Requirement</span></span> | <span data-ttu-id="e859b-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="e859b-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e859b-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e859b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="e859b-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e859b-120">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="e859b-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e859b-121">Minimum supported server</span></span><br/> | <span data-ttu-id="e859b-122">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e859b-122">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e859b-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e859b-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e859b-124">Éléments de schéma Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="e859b-124">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





