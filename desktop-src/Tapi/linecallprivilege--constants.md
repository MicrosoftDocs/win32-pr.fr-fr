---
description: Les \_ constantes d’indicateur de bit LINECALLPRIVILEGE décrivent les types de droits d’accès ou de privilèges qu’une application avec un descripteur d’appel peut avoir pour l’appel correspondant.
ms.assetid: a58b7e9e-696e-4421-9b31-1ba8afe6e03b
title: Constantes LINECALLPRIVILEGE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac2569ec255d2da3ad384292eb87afaa285f54b5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106534890"
---
# <a name="linecallprivilege_-constants"></a><span data-ttu-id="ffdc4-103">\_Constantes LINECALLPRIVILEGE</span><span class="sxs-lookup"><span data-stu-id="ffdc4-103">LINECALLPRIVILEGE\_ Constants</span></span>

<span data-ttu-id="ffdc4-104">Les constantes d’indicateur de bit **LINECALLPRIVILEGE \_** décrivent les types de droits d’accès ou de privilèges qu’une application avec un descripteur d’appel peut avoir pour l’appel correspondant.</span><span class="sxs-lookup"><span data-stu-id="ffdc4-104">The **LINECALLPRIVILEGE\_** bit-flag constants describe the kinds of access rights or privileges an application with a call handle may have to the corresponding call.</span></span>

<dl> <dt>

<span data-ttu-id="ffdc4-105"><span id="LINECALLPRIVILEGE_MONITOR"></span><span id="linecallprivilege_monitor"></span>**\_moniteur LINECALLPRIVILEGE**</span><span class="sxs-lookup"><span data-stu-id="ffdc4-105"><span id="LINECALLPRIVILEGE_MONITOR"></span><span id="linecallprivilege_monitor"></span>**LINECALLPRIVILEGE\_MONITOR**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ffdc4-106">L’application dispose des privilèges d’analyse pour l’appel.</span><span class="sxs-lookup"><span data-stu-id="ffdc4-106">The application has monitor privileges to the call.</span></span> <span data-ttu-id="ffdc4-107">Ces privilèges permettent à l’application de surveiller les modifications d’État et les informations de requête et l’état de l’appel.</span><span class="sxs-lookup"><span data-stu-id="ffdc4-107">These privileges allow the application to monitor state changes and query information and status about the call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ffdc4-108"><span id="LINECALLPRIVILEGE_NONE"></span><span id="linecallprivilege_none"></span>**LINECALLPRIVILEGE \_ aucun**</span><span class="sxs-lookup"><span data-stu-id="ffdc4-108"><span id="LINECALLPRIVILEGE_NONE"></span><span id="linecallprivilege_none"></span>**LINECALLPRIVILEGE\_NONE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ffdc4-109">L’application n’a aucun privilège pour l’appel.</span><span class="sxs-lookup"><span data-stu-id="ffdc4-109">The application has no privileges to the call.</span></span> <span data-ttu-id="ffdc4-110">Le descripteur de l’application est void et ne doit pas être utilisé.</span><span class="sxs-lookup"><span data-stu-id="ffdc4-110">The application's handle is void and should not be used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ffdc4-111"><span id="LINECALLPRIVILEGE_OWNER"></span><span id="linecallprivilege_owner"></span>**\_propriétaire LINECALLPRIVILEGE**</span><span class="sxs-lookup"><span data-stu-id="ffdc4-111"><span id="LINECALLPRIVILEGE_OWNER"></span><span id="linecallprivilege_owner"></span>**LINECALLPRIVILEGE\_OWNER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ffdc4-112">L’application dispose des privilèges de propriétaire pour l’appel.</span><span class="sxs-lookup"><span data-stu-id="ffdc4-112">The application has owner privileges to the call.</span></span> <span data-ttu-id="ffdc4-113">Ces privilèges permettent à l’application de manipuler l’appel de manière à affecter l’état de l’appel.</span><span class="sxs-lookup"><span data-stu-id="ffdc4-113">These privileges allow the application to manipulate the call in ways that affect the state of the call.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ffdc4-114">Notes</span><span class="sxs-lookup"><span data-stu-id="ffdc4-114">Remarks</span></span>

<span data-ttu-id="ffdc4-115">Aucune extensibilité.</span><span class="sxs-lookup"><span data-stu-id="ffdc4-115">No extensibility.</span></span> <span data-ttu-id="ffdc4-116">Tous les 32 bits sont réservés.</span><span class="sxs-lookup"><span data-stu-id="ffdc4-116">All 32 bits are reserved.</span></span>

<span data-ttu-id="ffdc4-117">Lorsqu’un descripteur d’appel est d’abord fourni à une application ou chaque fois que des privilèges d’appel de cette application sont modifiés, la [**ligne \_ CALLSTATE**](line-callstate.md) le message est envoyé à l’application.</span><span class="sxs-lookup"><span data-stu-id="ffdc4-117">When a call handle is first provided to an application or whenever call privileges of that application are modified, the [**LINE\_CALLSTATE**](line-callstate.md) message is sent to the application.</span></span> <span data-ttu-id="ffdc4-118">Lorsqu’une application transmet un appel et que l’application réceptrice n’a pas déjà de handle avec des privilèges de propriétaire, ce message informe l’application de ses nouveaux privilèges sur l’appel.</span><span class="sxs-lookup"><span data-stu-id="ffdc4-118">When an application hands off a call, and if the receiving application does not already have a handle with owner privileges, then this message informs the application about its new privileges to the call.</span></span>

## <a name="requirements"></a><span data-ttu-id="ffdc4-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ffdc4-119">Requirements</span></span>



| <span data-ttu-id="ffdc4-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ffdc4-120">Requirement</span></span> | <span data-ttu-id="ffdc4-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="ffdc4-121">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="ffdc4-122">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="ffdc4-122">TAPI version</span></span><br/> | <span data-ttu-id="ffdc4-123">Nécessite TAPI 2,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="ffdc4-123">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="ffdc4-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="ffdc4-124">Header</span></span><br/>       | <dl> <span data-ttu-id="ffdc4-125"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="ffdc4-125"><dt>Tapi.h</dt></span></span> </dl> |



 

 




