---
description: Signale l’état d’intégrité d’une application qui s’exécute sur un ordinateur virtuel aux composants d’intégration Hyper-V qui s’exécutent sur le même ordinateur virtuel.
ms.assetid: C463391B-669C-4CBA-9EC7-7E0ABC5A63A1
title: Interface IVmApplicationHealthMonitor
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IVmApplicationHealthMonitor
api_type:
- COM
api_location:
- VmApplicationHealthMonitor.idl
ms.openlocfilehash: ac9f6574dd8261a120e434cc0351fd07985c71a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106534160"
---
# <a name="ivmapplicationhealthmonitor-interface"></a><span data-ttu-id="94732-103">Interface IVmApplicationHealthMonitor</span><span class="sxs-lookup"><span data-stu-id="94732-103">IVmApplicationHealthMonitor interface</span></span>

<span data-ttu-id="94732-104">Signale l’état d’intégrité d’une application qui s’exécute sur un ordinateur virtuel aux composants d’intégration Hyper-V qui s’exécutent sur le même ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="94732-104">Reports the health status of an application that is running in a virtual machine to the Hyper-V integration components running in the same virtual machine.</span></span> <span data-ttu-id="94732-105">L’état des applications en cours d’exécution sur l’ordinateur virtuel est reflété dans la valeur de la propriété **OperationalStatus** \[ 1 \] de la classe [**MSVM \_ HeartbeatComponent**](msvm-heartbeatcomponent.md) .</span><span class="sxs-lookup"><span data-stu-id="94732-105">The state of the applications running in the virtual machine are reflected in the **OperationalStatus**\[1\] property value of the [**Msvm\_HeartbeatComponent**](msvm-heartbeatcomponent.md) class.</span></span> <span data-ttu-id="94732-106">Cette interface fournit également un moyen de réinitialiser l’ensemble de l’état de l’application accumulé dans Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="94732-106">This interface also provides a way to reset all of the application state accumulated in Hyper-V.</span></span>

<span data-ttu-id="94732-107">Cette interface est implémentée par les composants d’intégration Hyper-V de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="94732-107">This interface is implemented by the Windows 8 Hyper-V integration components.</span></span> <span data-ttu-id="94732-108">Une instance de cette interface est obtenue en créant une instance du CLSID **397a2e5f-348C-482D-b9a3-57d383b483cd** .</span><span class="sxs-lookup"><span data-stu-id="94732-108">An instance of this interface is obtained by creating an instance of the **397a2e5f-348c-482d-b9a3-57d383b483cd** CLSID.</span></span>

## <a name="members"></a><span data-ttu-id="94732-109">Membres</span><span class="sxs-lookup"><span data-stu-id="94732-109">Members</span></span>

<span data-ttu-id="94732-110">L’interface **IVmApplicationHealthMonitor** hérite de l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="94732-110">The **IVmApplicationHealthMonitor** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="94732-111">**IVmApplicationHealthMonitor** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="94732-111">**IVmApplicationHealthMonitor** also has these types of members:</span></span>

-   [<span data-ttu-id="94732-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="94732-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="94732-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="94732-113">Methods</span></span>

<span data-ttu-id="94732-114">L’interface **IVmApplicationHealthMonitor** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="94732-114">The **IVmApplicationHealthMonitor** interface has these methods.</span></span>



| <span data-ttu-id="94732-115">Méthode</span><span class="sxs-lookup"><span data-stu-id="94732-115">Method</span></span>                                                                                   | <span data-ttu-id="94732-116">Description</span><span class="sxs-lookup"><span data-stu-id="94732-116">Description</span></span>                                                                              |
|:-----------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------|
| [<span data-ttu-id="94732-117">**ResetAllApplicationState**</span><span class="sxs-lookup"><span data-stu-id="94732-117">**ResetAllApplicationState**</span></span>](ivmapplicationhealthmonitor-resetallapplicationstate.md) | <span data-ttu-id="94732-118">Réinitialise l’état d’intégrité de toutes les applications d’une machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="94732-118">Resets the health state for all applications in a virtual machine.</span></span><br/>            |
| [<span data-ttu-id="94732-119">**SetApplicationState**</span><span class="sxs-lookup"><span data-stu-id="94732-119">**SetApplicationState**</span></span>](ivmapplicationhealthmonitor-setapplicationstate.md)           | <span data-ttu-id="94732-120">Définit l’état d’intégrité d’une application qui s’exécute sur un ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="94732-120">Sets the health state of an application that is running in a virtual machine.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="94732-121">Notes</span><span class="sxs-lookup"><span data-stu-id="94732-121">Remarks</span></span>

<span data-ttu-id="94732-122">Pour utiliser cet élément de programmation, les composants d’intégration Windows 8 doivent être installés sur l’ordinateur virtuel dans lequel l’application s’exécute.</span><span class="sxs-lookup"><span data-stu-id="94732-122">To use this programming element, the Windows 8 integration components must be installed on the virtual machine that the application is running in.</span></span>

## <a name="requirements"></a><span data-ttu-id="94732-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="94732-123">Requirements</span></span>



| <span data-ttu-id="94732-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="94732-124">Requirement</span></span> | <span data-ttu-id="94732-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="94732-125">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="94732-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="94732-126">Minimum supported client</span></span><br/> | <span data-ttu-id="94732-127">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="94732-127">Windows 8 \[desktop apps only\]</span></span><br/>                                                                                                                                     |
| <span data-ttu-id="94732-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="94732-128">Minimum supported server</span></span><br/> | <span data-ttu-id="94732-129">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="94732-129">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                                                                                           |
| <span data-ttu-id="94732-130">Version</span><span class="sxs-lookup"><span data-stu-id="94732-130">Version</span></span><br/>                  | <span data-ttu-id="94732-131">Composants d’intégration pour Windows 8</span><span class="sxs-lookup"><span data-stu-id="94732-131">Integration components for Windows 8</span></span><br/>                                                                                                                                |
| <span data-ttu-id="94732-132">MIDL</span><span class="sxs-lookup"><span data-stu-id="94732-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="94732-133"><dt>VmApplicationHealthMonitor. idl</dt></span><span class="sxs-lookup"><span data-stu-id="94732-133"><dt>VmApplicationHealthMonitor.idl</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="94732-134">IID</span><span class="sxs-lookup"><span data-stu-id="94732-134">IID</span></span><br/>                      | <span data-ttu-id="94732-135">IID \_ IVmApplicationHealthMonitor est défini en tant que 267a0284-848f-447e-A096-5e10a1a76bca</span><span class="sxs-lookup"><span data-stu-id="94732-135">IID\_IVmApplicationHealthMonitor is defined as 267a0284-848f-447e-a096-5e10a1a76bca</span></span><br/> <span data-ttu-id="94732-136">L’identificateur d’objet est défini en tant que 397a2e5f-348C-482D-b9a3-57d383b483cd</span><span class="sxs-lookup"><span data-stu-id="94732-136">Object Identifier is defined as 397a2e5f-348c-482d-b9a3-57d383b483cd</span></span><br/> |



 

