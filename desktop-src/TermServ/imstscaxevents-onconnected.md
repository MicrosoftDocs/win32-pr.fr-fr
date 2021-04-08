---
title: Méthode IMsTscAxEvents OnConnected
description: Appelé lorsque le contrôle client est en train d’établir une connexion avec un serveur d’hôte de session Bureau à distance (hôte de session Bureau à distance).
ms.assetid: 9c26d112-c070-4870-93d5-2fcc84a1331f
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode OnConnected
- Méthode OnConnected Services Bureau à distance, interface IMsTscAxEvents
- Services Bureau à distance de l’interface IMsTscAxEvents, méthode OnConnected
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnConnected
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d83a6a14f58a0704f0a3110532ad8cf8c0d7dc8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741324"
---
# <a name="imstscaxeventsonconnected-method"></a><span data-ttu-id="80552-106">IMsTscAxEvents :: OnConnected, méthode</span><span class="sxs-lookup"><span data-stu-id="80552-106">IMsTscAxEvents::OnConnected method</span></span>

<span data-ttu-id="80552-107">Appelé lorsque le contrôle client est en train d’établir une connexion avec un serveur d’hôte de session Bureau à distance (hôte de session Bureau à distance).</span><span class="sxs-lookup"><span data-stu-id="80552-107">Called when the client control is in the process of establishing a connection with a Remote Desktop Session Host (RD Session Host) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="80552-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="80552-108">Syntax</span></span>


```C++
void OnConnected();
```



## <a name="parameters"></a><span data-ttu-id="80552-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="80552-109">Parameters</span></span>

<span data-ttu-id="80552-110">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="80552-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="80552-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="80552-111">Return value</span></span>

<span data-ttu-id="80552-112">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="80552-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="80552-113">Notes</span><span class="sxs-lookup"><span data-stu-id="80552-113">Remarks</span></span>

<span data-ttu-id="80552-114">Implémentez cette méthode dans votre récepteur d’événements pour recevoir une notification indiquant que le contrôle a établi une connexion avec un serveur hôte de session Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="80552-114">Implement this method in your event sink to receive notification that the control has established a connection with an RD Session Host server.</span></span>

<span data-ttu-id="80552-115">Pour plus d’informations sur l’appel de cette méthode, reportez-vous à l’événement [**IMsTscAxEvents :: OnLoginComplete**](imstscaxevents-onlogincomplete.md) .</span><span class="sxs-lookup"><span data-stu-id="80552-115">Refer to the [**IMsTscAxEvents::OnLoginComplete**](imstscaxevents-onlogincomplete.md) event for more information on calling this method.</span></span>

<span data-ttu-id="80552-116">Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="80552-116">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="80552-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="80552-117">Requirements</span></span>



| <span data-ttu-id="80552-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="80552-118">Requirement</span></span> | <span data-ttu-id="80552-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="80552-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="80552-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="80552-120">Minimum supported client</span></span><br/> | <span data-ttu-id="80552-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="80552-121">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="80552-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="80552-122">Minimum supported server</span></span><br/> | <span data-ttu-id="80552-123">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="80552-123">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="80552-124">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="80552-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="80552-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="80552-125"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="80552-126">DLL</span><span class="sxs-lookup"><span data-stu-id="80552-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="80552-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="80552-127"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="80552-128">IID</span><span class="sxs-lookup"><span data-stu-id="80552-128">IID</span></span><br/>                      | <span data-ttu-id="80552-129">IMsTscAxEvents est défini en tant que 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="80552-129">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="80552-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="80552-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80552-131">**IMsTscAxEvents**</span><span class="sxs-lookup"><span data-stu-id="80552-131">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





