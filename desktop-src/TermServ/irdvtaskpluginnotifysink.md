---
title: Interface IRDVTaskPluginNotifySink
description: L’interface IRDVTaskPluginNotifySink est utilisée par l’agent de tâche pour communiquer avec l’agent déclencheur.
ms.assetid: ccf19693-d3cc-4cf7-af35-947be047beeb
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de l’interface IRDVTaskPluginNotifySink
- Services Bureau à distance de l’interface IRDVTaskPluginNotifySink, Description
topic_type:
- apiref
api_name:
- IRDVTaskPluginNotifySink
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0dadaf387fcf6e8381404440e0d31dd210b9f8a6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742069"
---
# <a name="irdvtaskpluginnotifysink-interface"></a><span data-ttu-id="de6cc-105">Interface IRDVTaskPluginNotifySink</span><span class="sxs-lookup"><span data-stu-id="de6cc-105">IRDVTaskPluginNotifySink interface</span></span>

<span data-ttu-id="de6cc-106">L’interface **IRDVTaskPluginNotifySink** est utilisée par l’agent de tâche pour communiquer avec l’agent déclencheur.</span><span class="sxs-lookup"><span data-stu-id="de6cc-106">The **IRDVTaskPluginNotifySink** interface is used by the task agent to communicate with the trigger agent.</span></span> <span data-ttu-id="de6cc-107">Un pointeur vers cette interface est passé à l’agent de tâche dans la méthode [**IRDVTaskPlugin :: Initialize**](irdvtaskplugin-initialize.md) .</span><span class="sxs-lookup"><span data-stu-id="de6cc-107">A pointer to this interface is passed to the task agent in the [**IRDVTaskPlugin::Initialize**](irdvtaskplugin-initialize.md) method.</span></span>

## <a name="members"></a><span data-ttu-id="de6cc-108">Membres</span><span class="sxs-lookup"><span data-stu-id="de6cc-108">Members</span></span>

<span data-ttu-id="de6cc-109">L’interface **IRDVTaskPluginNotifySink** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="de6cc-109">The **IRDVTaskPluginNotifySink** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="de6cc-110">**IRDVTaskPluginNotifySink** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="de6cc-110">**IRDVTaskPluginNotifySink** also has these types of members:</span></span>

-   [<span data-ttu-id="de6cc-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="de6cc-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="de6cc-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="de6cc-112">Methods</span></span>

<span data-ttu-id="de6cc-113">L’interface **IRDVTaskPluginNotifySink** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="de6cc-113">The **IRDVTaskPluginNotifySink** interface has these methods.</span></span>



| <span data-ttu-id="de6cc-114">Méthode</span><span class="sxs-lookup"><span data-stu-id="de6cc-114">Method</span></span>                                                                  | <span data-ttu-id="de6cc-115">Description</span><span class="sxs-lookup"><span data-stu-id="de6cc-115">Description</span></span>                                                                       |
|:------------------------------------------------------------------------|:----------------------------------------------------------------------------------|
| [<span data-ttu-id="de6cc-116">**DeleteSchedule**</span><span class="sxs-lookup"><span data-stu-id="de6cc-116">**DeleteSchedule**</span></span>](irdvtaskpluginnotifysink-deleteschedule.md)       | <span data-ttu-id="de6cc-117">Appelé par l’agent de tâche pour supprimer une tâche planifiée.</span><span class="sxs-lookup"><span data-stu-id="de6cc-117">Called by the task agent to delete a scheduled task.</span></span><br/>                   |
| [<span data-ttu-id="de6cc-118">**OnTaskStateChange**</span><span class="sxs-lookup"><span data-stu-id="de6cc-118">**OnTaskStateChange**</span></span>](irdvtaskpluginnotifysink-ontaskstatechange.md) | <span data-ttu-id="de6cc-119">Permet d’informer l’agent déclencheur que l’état d’une tâche a changé.</span><span class="sxs-lookup"><span data-stu-id="de6cc-119">Used to notify the trigger agent that the state of a task has changed.</span></span><br/> |
| [<span data-ttu-id="de6cc-120">**OnTerminated**</span><span class="sxs-lookup"><span data-stu-id="de6cc-120">**OnTerminated**</span></span>](irdvtaskpluginnotifysink-onterminated.md)           | <span data-ttu-id="de6cc-121">Appelée par l’agent de tâche pour demander que l’agent de tâche soit arrêté.</span><span class="sxs-lookup"><span data-stu-id="de6cc-121">Called by the task agent to request that the task agent be shut down.</span></span><br/>  |
| [<span data-ttu-id="de6cc-122">**ScheduleTask,**</span><span class="sxs-lookup"><span data-stu-id="de6cc-122">**ScheduleTask**</span></span>](irdvtaskpluginnotifysink-scheduletask.md)           | <span data-ttu-id="de6cc-123">Appelé par l’agent de tâche pour planifier une tâche.</span><span class="sxs-lookup"><span data-stu-id="de6cc-123">Called by the task agent to schedule a task.</span></span><br/>                           |



 

## <a name="remarks"></a><span data-ttu-id="de6cc-124">Notes</span><span class="sxs-lookup"><span data-stu-id="de6cc-124">Remarks</span></span>

<span data-ttu-id="de6cc-125">Bien que cette interface soit prise en charge sur les systèmes d’exploitation identifiés dans la configuration requise ci-dessous, elle n’est utilisée que si la machine virtuelle est hébergée sur Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="de6cc-125">Although this interface is supported on the operating systems identified in the Requirements below, it will only be used if the virtual machine is hosted on Windows Server 2012.</span></span>

## <a name="requirements"></a><span data-ttu-id="de6cc-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="de6cc-126">Requirements</span></span>



| <span data-ttu-id="de6cc-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="de6cc-127">Requirement</span></span> | <span data-ttu-id="de6cc-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="de6cc-128">Value</span></span> |
|-------------------------------------|-----------------------------------|
| <span data-ttu-id="de6cc-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="de6cc-129">Minimum supported client</span></span><br/> | <span data-ttu-id="de6cc-130">Windows 7 Entreprise</span><span class="sxs-lookup"><span data-stu-id="de6cc-130">Windows 7 Enterprise</span></span><br/>   |
| <span data-ttu-id="de6cc-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="de6cc-131">Minimum supported server</span></span><br/> | <span data-ttu-id="de6cc-132">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="de6cc-132">Windows Server 2008 R2</span></span><br/> |



 

