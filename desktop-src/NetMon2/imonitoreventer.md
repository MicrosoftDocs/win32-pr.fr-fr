---
description: L’interface IMonitorEventer fournit des méthodes pour soumettre des événements et allouer et libérer des ressources de surveillance.
ms.assetid: d59a8b42-cce3-410b-a62e-97d66d058d90
title: Interface IMonitorEventer (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitorEventer
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: 7d4ca58b5a0787638eee54b7733b4e1a8fbf7ffe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862410"
---
# <a name="imonitoreventer-interface"></a><span data-ttu-id="4c526-103">Interface IMonitorEventer</span><span class="sxs-lookup"><span data-stu-id="4c526-103">IMonitorEventer interface</span></span>

<span data-ttu-id="4c526-104">L’interface **IMonitorEventer** fournit des méthodes pour soumettre des événements et allouer et libérer des ressources de surveillance.</span><span class="sxs-lookup"><span data-stu-id="4c526-104">The **IMonitorEventer** interface provides methods for submitting events and allocating and freeing monitor resources.</span></span>

## <a name="members"></a><span data-ttu-id="4c526-105">Membres</span><span class="sxs-lookup"><span data-stu-id="4c526-105">Members</span></span>

<span data-ttu-id="4c526-106">L’interface **IMonitorEventer** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="4c526-106">The **IMonitorEventer** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="4c526-107">**IMonitorEventer** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="4c526-107">**IMonitorEventer** also has these types of members:</span></span>

-   [<span data-ttu-id="4c526-108">Méthodes</span><span class="sxs-lookup"><span data-stu-id="4c526-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="4c526-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="4c526-109">Methods</span></span>

<span data-ttu-id="4c526-110">L’interface **IMonitorEventer** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="4c526-110">The **IMonitorEventer** interface has these methods.</span></span>



| <span data-ttu-id="4c526-111">Méthode</span><span class="sxs-lookup"><span data-stu-id="4c526-111">Method</span></span>                                                 | <span data-ttu-id="4c526-112">Description</span><span class="sxs-lookup"><span data-stu-id="4c526-112">Description</span></span>                                        |
|:-------------------------------------------------------|:---------------------------------------------------|
| [<span data-ttu-id="4c526-113">**FreeEventData**</span><span class="sxs-lookup"><span data-stu-id="4c526-113">**FreeEventData**</span></span>](imonitoreventer-freeeventdata.md) | <span data-ttu-id="4c526-114">Libère de l’espace alloué pour les données du moniteur.</span><span class="sxs-lookup"><span data-stu-id="4c526-114">Frees space allocated for monitor data.</span></span><br/> |
| [<span data-ttu-id="4c526-115">**GetEventData**</span><span class="sxs-lookup"><span data-stu-id="4c526-115">**GetEventData**</span></span>](imonitoreventer-geteventdata.md)   | <span data-ttu-id="4c526-116">Alloue de l’espace pour les données du moniteur.</span><span class="sxs-lookup"><span data-stu-id="4c526-116">Allocates space for monitor data.</span></span><br/>       |
| [<span data-ttu-id="4c526-117">**SendNMEvent**</span><span class="sxs-lookup"><span data-stu-id="4c526-117">**SendNMEvent**</span></span>](imonitoreventer-sendnmevent.md)     | <span data-ttu-id="4c526-118">Envoie des événements à WMI.</span><span class="sxs-lookup"><span data-stu-id="4c526-118">Submits events to WMI.</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="4c526-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4c526-119">Requirements</span></span>



| <span data-ttu-id="4c526-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4c526-120">Requirement</span></span> | <span data-ttu-id="4c526-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="4c526-121">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="4c526-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4c526-122">Minimum supported client</span></span><br/> | <span data-ttu-id="4c526-123">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4c526-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="4c526-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4c526-124">Minimum supported server</span></span><br/> | <span data-ttu-id="4c526-125">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4c526-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="4c526-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="4c526-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="4c526-127"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="4c526-127"><dt>Netmon.h</dt></span></span> </dl> |



 

