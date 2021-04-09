---
title: Interface IRDVTaskPlugin
description: L’interface IRDVTaskPlugin est implémentée par un agent de tâche de mise à jour de machine virtuelle pour permettre à l’agent de tâche de gérer les mises à jour système pour un ordinateur virtuel.
ms.assetid: e06eb707-be78-4d1f-96d3-21526b167e61
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de l’interface IRDVTaskPlugin
- Services Bureau à distance de l’interface IRDVTaskPlugin, Description
topic_type:
- apiref
api_name:
- IRDVTaskPlugin
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 59e90e899e8084f7fbc6b0b6f11067061eaa807b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942813"
---
# <a name="irdvtaskplugin-interface"></a><span data-ttu-id="7b446-105">Interface IRDVTaskPlugin</span><span class="sxs-lookup"><span data-stu-id="7b446-105">IRDVTaskPlugin interface</span></span>

<span data-ttu-id="7b446-106">L’interface **IRDVTaskPlugin** est implémentée par un agent de *tâche* de mise à jour de machine virtuelle pour permettre à l’agent de tâche de gérer les mises à jour système pour un ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="7b446-106">The **IRDVTaskPlugin** interface is implemented by a virtual machine update *task agent* to allow the task agent to manage system updates for a virtual machine.</span></span> <span data-ttu-id="7b446-107">Cette interface est utilisée par l' *agent déclencheur*, qui est implémenté par le système hôte.</span><span class="sxs-lookup"><span data-stu-id="7b446-107">This interface is used by the *trigger agent*, which is implemented by the host system.</span></span>

## <a name="members"></a><span data-ttu-id="7b446-108">Membres</span><span class="sxs-lookup"><span data-stu-id="7b446-108">Members</span></span>

<span data-ttu-id="7b446-109">L’interface **IRDVTaskPlugin** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="7b446-109">The **IRDVTaskPlugin** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="7b446-110">**IRDVTaskPlugin** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="7b446-110">**IRDVTaskPlugin** also has these types of members:</span></span>

-   [<span data-ttu-id="7b446-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="7b446-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="7b446-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="7b446-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="7b446-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="7b446-113">Methods</span></span>

<span data-ttu-id="7b446-114">L’interface **IRDVTaskPlugin** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="7b446-114">The **IRDVTaskPlugin** interface has these methods.</span></span>



| <span data-ttu-id="7b446-115">Méthode</span><span class="sxs-lookup"><span data-stu-id="7b446-115">Method</span></span>                                          | <span data-ttu-id="7b446-116">Description</span><span class="sxs-lookup"><span data-stu-id="7b446-116">Description</span></span>                                                        |
|:------------------------------------------------|:-------------------------------------------------------------------|
| [<span data-ttu-id="7b446-117">**Initialiser**</span><span class="sxs-lookup"><span data-stu-id="7b446-117">**Initialize**</span></span>](irdvtaskplugin-initialize.md) | <span data-ttu-id="7b446-118">Appelé pour initialiser l’agent de tâche.</span><span class="sxs-lookup"><span data-stu-id="7b446-118">Called to initialize the task agent.</span></span><br/>                    |
| [<span data-ttu-id="7b446-119">**StartTask**</span><span class="sxs-lookup"><span data-stu-id="7b446-119">**StartTask**</span></span>](irdvtaskplugin-starttask.md)   | <span data-ttu-id="7b446-120">Appelé pour démarrer la tâche de mise à jour sur la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="7b446-120">Called to start the update task on the virtual machine.</span></span><br/> |
| [<span data-ttu-id="7b446-121">**Terminate**</span><span class="sxs-lookup"><span data-stu-id="7b446-121">**Terminate**</span></span>](irdvtaskplugin-terminate.md)   | <span data-ttu-id="7b446-122">Appelé lorsque l’agent de tâche est arrêté.</span><span class="sxs-lookup"><span data-stu-id="7b446-122">Called when the task agent is being shut down.</span></span><br/>          |



 

### <a name="properties"></a><span data-ttu-id="7b446-123">Propriétés</span><span class="sxs-lookup"><span data-stu-id="7b446-123">Properties</span></span>

<span data-ttu-id="7b446-124">L’interface **IRDVTaskPlugin** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="7b446-124">The **IRDVTaskPlugin** interface has these properties.</span></span>



| <span data-ttu-id="7b446-125">Propriété</span><span class="sxs-lookup"><span data-stu-id="7b446-125">Property</span></span>                                                   | <span data-ttu-id="7b446-126">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="7b446-126">Access type</span></span>          | <span data-ttu-id="7b446-127">Description</span><span class="sxs-lookup"><span data-stu-id="7b446-127">Description</span></span>                                             |
|:-----------------------------------------------------------|:---------------------|:--------------------------------------------------------|
| [<span data-ttu-id="7b446-128">**PluginName**</span><span class="sxs-lookup"><span data-stu-id="7b446-128">**PluginName**</span></span>](irdvtaskplugin-pluginname.md)<br/> | <span data-ttu-id="7b446-129">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7b446-129">Read-only</span></span><br/> | <span data-ttu-id="7b446-130">Contient le nom complet de l’agent de tâche.</span><span class="sxs-lookup"><span data-stu-id="7b446-130">Contains the display name of the task agent.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="7b446-131">Notes</span><span class="sxs-lookup"><span data-stu-id="7b446-131">Remarks</span></span>

<span data-ttu-id="7b446-132">L’agent de tâche est exécuté sur l’ordinateur virtuel lorsque cet ordinateur virtuel est planifié pour une mise à jour du système.</span><span class="sxs-lookup"><span data-stu-id="7b446-132">The task agent is run on the virtual machine when that virtual machine is scheduled for a system update.</span></span> <span data-ttu-id="7b446-133">L’agent de tâche met à jour l’ordinateur virtuel lorsque la méthode [**StartTask**](irdvtaskplugin-starttask.md) est appelée.</span><span class="sxs-lookup"><span data-stu-id="7b446-133">The task agent updates the virtual machine when the [**StartTask**](irdvtaskplugin-starttask.md) method is called.</span></span>

<span data-ttu-id="7b446-134">Pour inscrire l’agent de tâche, ajoutez la clé suivante au registre de l’ordinateur virtuel :</span><span class="sxs-lookup"><span data-stu-id="7b446-134">To register the task agent, add the following key to the registry of the virtual machine:</span></span>

<span data-ttu-id="7b446-135">**HKEY \_ \_** Plug-ins des tâches de l’ordinateur local \\  \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **Terminal Server** \\  \\  \\ **TaskAgentName**</span><span class="sxs-lookup"><span data-stu-id="7b446-135">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**Windows NT**\\**CurrentVersion**\\**Terminal Server**\\**Task**\\**Plugins**\\**TaskAgentName**</span></span>

<span data-ttu-id="7b446-136">Sous cette clé de Registre, ajoutez les valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="7b446-136">Under this registry key, add the following values:</span></span>



| <span data-ttu-id="7b446-137">Nom</span><span class="sxs-lookup"><span data-stu-id="7b446-137">Name</span></span>                     | <span data-ttu-id="7b446-138">Type</span><span class="sxs-lookup"><span data-stu-id="7b446-138">Type</span></span>                      | <span data-ttu-id="7b446-139">Description</span><span class="sxs-lookup"><span data-stu-id="7b446-139">Description</span></span>                                                                   |
|--------------------------|---------------------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="7b446-140">**IDENTIFICATEUR**</span><span class="sxs-lookup"><span data-stu-id="7b446-140">**CLSID**</span></span><br/>     | <span data-ttu-id="7b446-141">**SZ de REG \_**</span><span class="sxs-lookup"><span data-stu-id="7b446-141">**REG\_SZ**</span></span><br/>    | <span data-ttu-id="7b446-142">Chaîne qui représente le **CLSID** de l’agent de tâche.</span><span class="sxs-lookup"><span data-stu-id="7b446-142">A string that represents the **CLSID** of the task agent.</span></span><br/>          |
| <span data-ttu-id="7b446-143">**IsEnabled**</span><span class="sxs-lookup"><span data-stu-id="7b446-143">**IsEnabled**</span></span><br/> | <span data-ttu-id="7b446-144">**\_valeur DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="7b446-144">**REG\_DWORD**</span></span><br/> | <span data-ttu-id="7b446-145">0 si l’agent de tâche est désactivé ou 1 si l’agent de tâche est activé.</span><span class="sxs-lookup"><span data-stu-id="7b446-145">0 if the task agent is disabled or 1 if the task agent is enabled.</span></span><br/> |



 

> [!Note]  
> <span data-ttu-id="7b446-146">Plusieurs agents de tâche peuvent être inscrits, mais un seul agent de tâche sera utilisé.</span><span class="sxs-lookup"><span data-stu-id="7b446-146">More than one task agent can be registered, but only one task agent will be used.</span></span> <span data-ttu-id="7b446-147">Si plusieurs agents de tâche sont activés, seul le premier est utilisé.</span><span class="sxs-lookup"><span data-stu-id="7b446-147">If more than one task agent is enabled, only the first one found will be used.</span></span>

 

<span data-ttu-id="7b446-148">Bien que cette interface soit prise en charge sur les systèmes d’exploitation identifiés dans la configuration requise ci-dessous, elle n’est utilisée que si la machine virtuelle est hébergée sur Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="7b446-148">Although this interface is supported on the operating systems identified in the Requirements below, it will only be used if the virtual machine is hosted on Windows Server 2012.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b446-149">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7b446-149">Requirements</span></span>



| <span data-ttu-id="7b446-150">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7b446-150">Requirement</span></span> | <span data-ttu-id="7b446-151">Valeur</span><span class="sxs-lookup"><span data-stu-id="7b446-151">Value</span></span> |
|-------------------------------------|-----------------------------------|
| <span data-ttu-id="7b446-152">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7b446-152">Minimum supported client</span></span><br/> | <span data-ttu-id="7b446-153">Windows 7 Entreprise</span><span class="sxs-lookup"><span data-stu-id="7b446-153">Windows 7 Enterprise</span></span><br/>   |
| <span data-ttu-id="7b446-154">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7b446-154">Minimum supported server</span></span><br/> | <span data-ttu-id="7b446-155">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7b446-155">Windows Server 2008 R2</span></span><br/> |



 

