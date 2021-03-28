---
description: Implémenté par le navigateur. Expose des méthodes qui gèrent le moniteur qui contient la barre des tâches Windows sur un système à plusieurs écrans.
title: Interface IMultiMonitorDockingSite
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMultiMonitorDockingSite
api_type:
- COM
api_location: ''
ms.assetid: af9a7a9e-bd7c-4b17-9cb6-008df5c820d8
ms.openlocfilehash: 3aa1ccb1c25fd2896ce9e18ba52ea3f46b1882af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104991821"
---
# <a name="imultimonitordockingsite-interface"></a><span data-ttu-id="b22ca-104">Interface IMultiMonitorDockingSite</span><span class="sxs-lookup"><span data-stu-id="b22ca-104">IMultiMonitorDockingSite interface</span></span>

<span data-ttu-id="b22ca-105">Implémenté par le navigateur.</span><span class="sxs-lookup"><span data-stu-id="b22ca-105">Implemented by the browser.</span></span> <span data-ttu-id="b22ca-106">Expose des méthodes qui gèrent le moniteur qui contient la barre des tâches Windows sur un système à plusieurs écrans.</span><span class="sxs-lookup"><span data-stu-id="b22ca-106">Exposes methods that manage which monitor contains the Windows taskbar on a multiple monitor system.</span></span>

## <a name="members"></a><span data-ttu-id="b22ca-107">Membres</span><span class="sxs-lookup"><span data-stu-id="b22ca-107">Members</span></span>

<span data-ttu-id="b22ca-108">L’interface **IMultiMonitorDockingSite** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="b22ca-108">The **IMultiMonitorDockingSite** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="b22ca-109">**IMultiMonitorDockingSite** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="b22ca-109">**IMultiMonitorDockingSite** also has these types of members:</span></span>

-   [<span data-ttu-id="b22ca-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="b22ca-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="b22ca-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="b22ca-111">Methods</span></span>

<span data-ttu-id="b22ca-112">L’interface **IMultiMonitorDockingSite** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="b22ca-112">The **IMultiMonitorDockingSite** interface has these methods.</span></span>



| <span data-ttu-id="b22ca-113">Méthode</span><span class="sxs-lookup"><span data-stu-id="b22ca-113">Method</span></span>                                                            | <span data-ttu-id="b22ca-114">Description</span><span class="sxs-lookup"><span data-stu-id="b22ca-114">Description</span></span>                                                                                |
|:------------------------------------------------------------------|:-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b22ca-115">**GetMonitor**</span><span class="sxs-lookup"><span data-stu-id="b22ca-115">**GetMonitor**</span></span>](imultimonitordockingsite-getmonitor.md)         | <span data-ttu-id="b22ca-116">Obtient l’analyseur par défaut actuel.</span><span class="sxs-lookup"><span data-stu-id="b22ca-116">Gets the current default monitor.</span></span><br/>                                               |
| [<span data-ttu-id="b22ca-117">**RequestMonitor**</span><span class="sxs-lookup"><span data-stu-id="b22ca-117">**RequestMonitor**</span></span>](imultimonitordockingsite-requestmonitor.md) | <span data-ttu-id="b22ca-118">Vérifie que le moniteur est actif et disponible.</span><span class="sxs-lookup"><span data-stu-id="b22ca-118">Verifies that the monitor is active and available.</span></span><br/>                              |
| [<span data-ttu-id="b22ca-119">**SetMonitor**</span><span class="sxs-lookup"><span data-stu-id="b22ca-119">**SetMonitor**</span></span>](imultimonitordockingsite-setmonitor.md)         | <span data-ttu-id="b22ca-120">Modifie l’analyse qui est utilisée pour les barres d’outils ancrées sur un système à plusieurs écrans.</span><span class="sxs-lookup"><span data-stu-id="b22ca-120">Changes which monitor is used for docked toolbars on a multiple monitor system.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="b22ca-121">Notes</span><span class="sxs-lookup"><span data-stu-id="b22ca-121">Remarks</span></span>

<span data-ttu-id="b22ca-122">En général, vous n’implémentez pas l’interface **IMultiMonitorDockingSite** .</span><span class="sxs-lookup"><span data-stu-id="b22ca-122">You do not typically implement the **IMultiMonitorDockingSite** interface.</span></span> <span data-ttu-id="b22ca-123">Le navigateur de l’interpréteur de commandes implémente cette interface pour prendre en charge plusieurs analyses.</span><span class="sxs-lookup"><span data-stu-id="b22ca-123">The Shell browser implements this interface to support multiple monitors.</span></span>

## <a name="requirements"></a><span data-ttu-id="b22ca-124">Spécifications</span><span class="sxs-lookup"><span data-stu-id="b22ca-124">Requirements</span></span>



| <span data-ttu-id="b22ca-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b22ca-125">Requirement</span></span> | <span data-ttu-id="b22ca-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="b22ca-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="b22ca-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b22ca-127">Minimum supported client</span></span><br/> | <span data-ttu-id="b22ca-128">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b22ca-128">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="b22ca-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b22ca-129">Minimum supported server</span></span><br/> | <span data-ttu-id="b22ca-130">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b22ca-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                   |



 

 
