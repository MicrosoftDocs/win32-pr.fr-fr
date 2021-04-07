---
description: L’interface IMonitor fournit des méthodes qui contrôlent l’opération de surveillance. Ces méthodes sont appelées par le service de contrôle d’analyse (MCSVC).
ms.assetid: 53140e7d-c3a1-45cd-aaa4-c6f5021a6102
title: Interface IMonitor (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitor
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: 1b6ba91860905010fd14a46cd4608eaee3da80fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863270"
---
# <a name="imonitor-interface"></a><span data-ttu-id="221e5-104">Interface IMonitor</span><span class="sxs-lookup"><span data-stu-id="221e5-104">IMonitor interface</span></span>

<span data-ttu-id="221e5-105">L’interface **Imonitor** fournit des méthodes qui contrôlent l’opération de surveillance.</span><span class="sxs-lookup"><span data-stu-id="221e5-105">The **IMonitor** interface provides methods that control monitor operation.</span></span> <span data-ttu-id="221e5-106">Ces méthodes sont appelées par le [*service de contrôle d’analyse*](m.md) (MCSVC).</span><span class="sxs-lookup"><span data-stu-id="221e5-106">These methods are called by the [*Monitor Control Service*](m.md) (MCSVC).</span></span>

## <a name="members"></a><span data-ttu-id="221e5-107">Membres</span><span class="sxs-lookup"><span data-stu-id="221e5-107">Members</span></span>

<span data-ttu-id="221e5-108">L’interface **Imonitor** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="221e5-108">The **IMonitor** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="221e5-109">**Imonitor** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="221e5-109">**IMonitor** also has these types of members:</span></span>

-   [<span data-ttu-id="221e5-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="221e5-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="221e5-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="221e5-111">Methods</span></span>

<span data-ttu-id="221e5-112">L’interface **Imonitor** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="221e5-112">The **IMonitor** interface has these methods.</span></span>



| <span data-ttu-id="221e5-113">Méthode</span><span class="sxs-lookup"><span data-stu-id="221e5-113">Method</span></span>                                        | <span data-ttu-id="221e5-114">Description</span><span class="sxs-lookup"><span data-stu-id="221e5-114">Description</span></span>                                                                                                         |
|:----------------------------------------------|:--------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="221e5-115">**Configurer**</span><span class="sxs-lookup"><span data-stu-id="221e5-115">**DoConfigure**</span></span>](imonitor-doconfigure.md)   | <span data-ttu-id="221e5-116">Met à jour la configuration de l’analyse.</span><span class="sxs-lookup"><span data-stu-id="221e5-116">Updates monitor configuration.</span></span><br/>                                                                           |
| [<span data-ttu-id="221e5-117">**Ininitialize**</span><span class="sxs-lookup"><span data-stu-id="221e5-117">**DoInitialize**</span></span>](imonitor-doinitialize.md) | <span data-ttu-id="221e5-118">Initialise une analyse.</span><span class="sxs-lookup"><span data-stu-id="221e5-118">Initializes a monitor.</span></span><br/>                                                                                   |
| [<span data-ttu-id="221e5-119">**OnFrames**</span><span class="sxs-lookup"><span data-stu-id="221e5-119">**OnFrames**</span></span>](imonitor-onframes.md)         | <span data-ttu-id="221e5-120">Indique l’état d’un événement Frame.</span><span class="sxs-lookup"><span data-stu-id="221e5-120">Indicates the status of a frame event.</span></span><br/>                                                                   |
| [<span data-ttu-id="221e5-121">**OnStart**</span><span class="sxs-lookup"><span data-stu-id="221e5-121">**OnStart**</span></span>](imonitor-onstart.md)           | <span data-ttu-id="221e5-122">Indique que l’analyse a été correctement configurée et que la capture de données va commencer.</span><span class="sxs-lookup"><span data-stu-id="221e5-122">Indicates that the monitor has been configured successfully and that the data capture is about to begin.</span></span><br/> |
| [<span data-ttu-id="221e5-123">**OnStatus**</span><span class="sxs-lookup"><span data-stu-id="221e5-123">**OnStatus**</span></span>](imonitor-onstatus.md)         | <span data-ttu-id="221e5-124">Indique un événement de statut NPP.</span><span class="sxs-lookup"><span data-stu-id="221e5-124">Indicates an NPP status event.</span></span><br/>                                                                           |
| [<span data-ttu-id="221e5-125">**OnStop**</span><span class="sxs-lookup"><span data-stu-id="221e5-125">**OnStop**</span></span>](imonitor-onstop.md)             | <span data-ttu-id="221e5-126">Indique la fin de la capture des données.</span><span class="sxs-lookup"><span data-stu-id="221e5-126">Indicates data capture completion.</span></span><br/>                                                                       |



 

## <a name="requirements"></a><span data-ttu-id="221e5-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="221e5-127">Requirements</span></span>



| <span data-ttu-id="221e5-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="221e5-128">Requirement</span></span> | <span data-ttu-id="221e5-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="221e5-129">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="221e5-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="221e5-130">Minimum supported client</span></span><br/> | <span data-ttu-id="221e5-131">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="221e5-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="221e5-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="221e5-132">Minimum supported server</span></span><br/> | <span data-ttu-id="221e5-133">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="221e5-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="221e5-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="221e5-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="221e5-135"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="221e5-135"><dt>Netmon.h</dt></span></span> </dl> |



 

