---
title: Méthode IMsTscAxEvents OnAutoReconnecting2
description: Appelée lorsqu’un client se trouve dans le processus de reconnexion automatique d’une session à un serveur hôte de session Bureau à distance (hôte de session Bureau à distance). | Méthode IMsTscAxEvents OnAutoReconnecting2
ms.assetid: 20F69798-5397-440C-9D0D-45AE417623A7
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode OnAutoReconnecting2
- Méthode OnAutoReconnecting2 Services Bureau à distance, interface IMsTscAxEvents
- Services Bureau à distance de l’interface IMsTscAxEvents, méthode OnAutoReconnecting2
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnAutoReconnecting2
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 901bb196922d1772782ab7f1c911c96573c88b36
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106529572"
---
# <a name="imstscaxeventsonautoreconnecting2-method"></a><span data-ttu-id="9b6d9-107">IMsTscAxEvents :: OnAutoReconnecting2, méthode</span><span class="sxs-lookup"><span data-stu-id="9b6d9-107">IMsTscAxEvents::OnAutoReconnecting2 method</span></span>

<span data-ttu-id="9b6d9-108">Appelée lorsqu’un client se trouve dans le processus de reconnexion automatique d’une session à un serveur hôte de session Bureau à distance (hôte de session Bureau à distance).</span><span class="sxs-lookup"><span data-stu-id="9b6d9-108">Called when a client is in the process of automatically reconnecting a session with a Remote Desktop Session Host (RD Session Host) server.</span></span> <span data-ttu-id="9b6d9-109">Il s’agit d’une version améliorée de la méthode [**OnAutoReconnecting**](-imstscaxevents--onautoreconnecting.md) .</span><span class="sxs-lookup"><span data-stu-id="9b6d9-109">This is an enhanced version of the [**OnAutoReconnecting**](-imstscaxevents--onautoreconnecting.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b6d9-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9b6d9-110">Syntax</span></span>


```C++
void OnAutoReconnecting2(
  [in] LONG         disconnectReason,
  [in] VARIANT_BOOL networkAvailable,
  [in] LONG         attemptCount,
  [in] LONG         maxAttemptCount
);
```



## <a name="parameters"></a><span data-ttu-id="9b6d9-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9b6d9-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9b6d9-112">*disconnectReason* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9b6d9-112">*disconnectReason* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9b6d9-113">Code qui décrit la raison de la dernière déconnexion de la session.</span><span class="sxs-lookup"><span data-stu-id="9b6d9-113">Code that describes the reason for the last session disconnection.</span></span>

</dd> <dt>

<span data-ttu-id="9b6d9-114">*networkAvailable* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9b6d9-114">*networkAvailable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9b6d9-115">Spécifie si le réseau est disponible.</span><span class="sxs-lookup"><span data-stu-id="9b6d9-115">Specifies if the network is available.</span></span>

</dd> <dt>

<span data-ttu-id="9b6d9-116">*attemptCount* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9b6d9-116">*attemptCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9b6d9-117">Nombre de tentatives effectuées dans le processus de reconnexion automatique en cours.</span><span class="sxs-lookup"><span data-stu-id="9b6d9-117">Number of attempts that have been made in the current automatic reconnection process.</span></span> <span data-ttu-id="9b6d9-118">Ce nombre augmente d’une unité pour chaque tentative effectuée.</span><span class="sxs-lookup"><span data-stu-id="9b6d9-118">This count increases by one for each attempt made.</span></span>

</dd> <dt>

<span data-ttu-id="9b6d9-119">*maxAttemptCount* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9b6d9-119">*maxAttemptCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9b6d9-120">Nombre maximal de tentatives qui seront effectuées dans le processus de reconnexion automatique actuel.</span><span class="sxs-lookup"><span data-stu-id="9b6d9-120">The maximum number of attempts that will be made in the current automatic reconnection process.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9b6d9-121">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9b6d9-121">Return value</span></span>

<span data-ttu-id="9b6d9-122">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="9b6d9-122">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="9b6d9-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9b6d9-123">Requirements</span></span>



| <span data-ttu-id="9b6d9-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9b6d9-124">Requirement</span></span> | <span data-ttu-id="9b6d9-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="9b6d9-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9b6d9-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9b6d9-126">Minimum supported client</span></span><br/> | <span data-ttu-id="9b6d9-127">Windows 8</span><span class="sxs-lookup"><span data-stu-id="9b6d9-127">Windows 8</span></span><br/>                                                                   |
| <span data-ttu-id="9b6d9-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9b6d9-128">Minimum supported server</span></span><br/> | <span data-ttu-id="9b6d9-129">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9b6d9-129">Windows Server 2012</span></span><br/>                                                         |
| <span data-ttu-id="9b6d9-130">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="9b6d9-130">Type library</span></span><br/>             | <dl> <span data-ttu-id="9b6d9-131"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9b6d9-131"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="9b6d9-132">DLL</span><span class="sxs-lookup"><span data-stu-id="9b6d9-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9b6d9-133"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9b6d9-133"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9b6d9-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9b6d9-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b6d9-135">**IMsTscAxEvents**</span><span class="sxs-lookup"><span data-stu-id="9b6d9-135">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





