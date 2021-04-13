---
title: Méthode IMsTscAxEvents OnAutoReconnecting
description: Appelée lorsqu’un client se trouve dans le processus de reconnexion automatique d’une session à un serveur hôte de session Bureau à distance (hôte de session Bureau à distance). | Méthode IMsTscAxEvents OnAutoReconnecting
ms.assetid: 9cb36052-8010-47df-bb46-f4ad81f47a73
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode OnAutoReconnecting
- Méthode OnAutoReconnecting Services Bureau à distance, interface IMsTscAxEvents
- Services Bureau à distance de l’interface IMsTscAxEvents, méthode OnAutoReconnecting
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnAutoReconnecting
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3435be46f2bb2c7bcf8ca662b039f3e5ef856d8b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104322370"
---
# <a name="imstscaxeventsonautoreconnecting-method"></a><span data-ttu-id="4b9e9-107">IMsTscAxEvents :: OnAutoReconnecting, méthode</span><span class="sxs-lookup"><span data-stu-id="4b9e9-107">IMsTscAxEvents::OnAutoReconnecting method</span></span>

<span data-ttu-id="4b9e9-108">Appelée lorsqu’un client se trouve dans le processus de reconnexion automatique d’une session à un serveur hôte de session Bureau à distance (hôte de session Bureau à distance).</span><span class="sxs-lookup"><span data-stu-id="4b9e9-108">Called when a client is in the process of automatically reconnecting a session with a Remote Desktop Session Host (RD Session Host) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b9e9-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4b9e9-109">Syntax</span></span>


```C++
void OnAutoReconnecting(
  [in]  LONG                       disconnectReason,
  [in]  LONG                       attemptCount,
  [out] AutoReconnectContinueState *pArcContinueStatus
);
```



## <a name="parameters"></a><span data-ttu-id="4b9e9-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4b9e9-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4b9e9-111">*disconnectReason* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4b9e9-111">*disconnectReason* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b9e9-112">Code décrivant la raison de la dernière déconnexion de la session.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-112">Code describing the reason for the last session disconnection.</span></span>

</dd> <dt>

<span data-ttu-id="4b9e9-113">*attemptCount* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4b9e9-113">*attemptCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b9e9-114">Nombre de tentatives effectuées dans le processus de reconnexion automatique en cours.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-114">Number of attempts that have been made in the current automatic reconnection process.</span></span> <span data-ttu-id="4b9e9-115">Ce nombre augmente d’une unité pour chaque tentative effectuée.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-115">This count increases by one for each attempt made.</span></span>

</dd> <dt>

<span data-ttu-id="4b9e9-116">*pArcContinueStatus* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="4b9e9-116">*pArcContinueStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4b9e9-117">Pointeur vers un code retourné qui spécifie l’état du processus de reconnexion automatique.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-117">Pointer to a returned code specifying the state of the automatic reconnection process.</span></span> <span data-ttu-id="4b9e9-118">Ce code peut être réinitialisé pour modifier l’état du processus de reconnexion automatique en cours.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-118">This code can be reset to change the state of the current automatic reconnection process.</span></span>

<span data-ttu-id="4b9e9-119">Pour plus d’informations sur la réinitialisation de ce code, reportez-vous à la section Notes.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-119">For more information about resetting this code, refer to the Remarks section.</span></span>

<dt>

<span id="autoReconnectContinueAutomatic"></span><span id="autoreconnectcontinueautomatic"></span><span id="AUTORECONNECTCONTINUEAUTOMATIC"></span>

<span data-ttu-id="4b9e9-120"><span id="autoReconnectContinueAutomatic"></span><span id="autoreconnectcontinueautomatic"></span><span id="AUTORECONNECTCONTINUEAUTOMATIC"></span>autoReconnectContinueAutomatic \* \* \* \* (0)</span><span class="sxs-lookup"><span data-stu-id="4b9e9-120"><span id="autoReconnectContinueAutomatic"></span><span id="autoreconnectcontinueautomatic"></span><span id="AUTORECONNECTCONTINUEAUTOMATIC"></span>\*\*\*\*autoReconnectContinueAutomatic\*\*\*\* (0)</span></span>


</dt> <dd>

<span data-ttu-id="4b9e9-121">Le processus de reconnexion se produit automatiquement.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-121">The reconnection process is occurring automatically.</span></span> <span data-ttu-id="4b9e9-122">Il s’agit de la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-122">This is the default value.</span></span>

</dd> <dt>

<span id="autoReconnectContinueStop"></span><span id="autoreconnectcontinuestop"></span><span id="AUTORECONNECTCONTINUESTOP"></span>

<span data-ttu-id="4b9e9-123"><span id="autoReconnectContinueStop"></span><span id="autoreconnectcontinuestop"></span><span id="AUTORECONNECTCONTINUESTOP"></span>autoReconnectContinueStop \* \* \* \* (1)</span><span class="sxs-lookup"><span data-stu-id="4b9e9-123"><span id="autoReconnectContinueStop"></span><span id="autoreconnectcontinuestop"></span><span id="AUTORECONNECTCONTINUESTOP"></span>\*\*\*\*autoReconnectContinueStop\*\*\*\* (1)</span></span>


</dt> <dd>

<span data-ttu-id="4b9e9-124">Le processus de reconnexion a été arrêté.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-124">The reconnection process has been stopped.</span></span>

</dd> <dt>

<span id="autoReconnectContinueManual"></span><span id="autoreconnectcontinuemanual"></span><span id="AUTORECONNECTCONTINUEMANUAL"></span>

<span data-ttu-id="4b9e9-125"><span id="autoReconnectContinueManual"></span><span id="autoreconnectcontinuemanual"></span><span id="AUTORECONNECTCONTINUEMANUAL"></span>autoReconnectContinueManual \* \* \* \* (2)</span><span class="sxs-lookup"><span data-stu-id="4b9e9-125"><span id="autoReconnectContinueManual"></span><span id="autoreconnectcontinuemanual"></span><span id="AUTORECONNECTCONTINUEMANUAL"></span>\*\*\*\*autoReconnectContinueManual\*\*\*\* (2)</span></span>


</dt> <dd>

<span data-ttu-id="4b9e9-126">Le processus de reconnexion se produit manuellement.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-126">The reconnection process is occurring manually.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4b9e9-127">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4b9e9-127">Return value</span></span>

<span data-ttu-id="4b9e9-128">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-128">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4b9e9-129">Notes</span><span class="sxs-lookup"><span data-stu-id="4b9e9-129">Remarks</span></span>

<span data-ttu-id="4b9e9-130">Implémentez cette méthode dans votre récepteur d’événements pour recevoir une notification indiquant que le contrôle rétablit une connexion avec un serveur hôte de session Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-130">Implement this method in your event sink to receive notification that the control is reestablishing a connection with an RD Session Host server.</span></span>

<span data-ttu-id="4b9e9-131">Lorsque l’état du processus de reconnexion automatique est modifié en affectant à la valeur du paramètre *pArcContinueStatus* la valeur **autoReconnectContinueAutomatic**, cette méthode fonctionne en mode purement consultatif.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-131">When the state of the automatic reconnection process is changed by setting the value of the *pArcContinueStatus* parameter to **autoReconnectContinueAutomatic**, this method functions in a purely advisory mode.</span></span> <span data-ttu-id="4b9e9-132">Les conteneurs peuvent écouter cet événement pour les notifications que le processus de reconnexion automatique est en cours.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-132">Containers can listen to this event for notifications that the automatic reconnection process is proceeding.</span></span> <span data-ttu-id="4b9e9-133">Le contrôle continue automatiquement d’essayer de rétablir une connexion en fonction de son propre minutage interne et des nombres de tentatives.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-133">The control will automatically keep trying to re-establish a connection based on its own internal timing and attempt counts.</span></span> <span data-ttu-id="4b9e9-134">Cette méthode est appelée lors de chaque tentative de reconnexion automatique afin d’avertir le conteneur.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-134">This method is called during each automatic reconnection attempt in order to notify the container.</span></span>

<span data-ttu-id="4b9e9-135">Lorsque l’état du processus de reconnexion automatique est modifié en définissant la valeur du paramètre *pArcContinueStatus* sur **autoReconnectContinueStop**, la tentative de reconnexion automatique en cours sera interrompue, une notification de déconnexion sera envoyée au conteneur et aucune autre notification de reconnexion automatique n’est émise.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-135">When the state of the automatic reconnection process is changed by setting the value of the *pArcContinueStatus* parameter to **autoReconnectContinueStop**, the current automatic reconnection attempt will be terminated, a disconnect notification will be sent to the container, and no further automatic reconnect notifications will be issued.</span></span>

> [!Note]  
> <span data-ttu-id="4b9e9-136">Utilisez la propriété [**EnableAutoReconnect**](imsrdpclientadvancedsettings2-enableautoreconnect.md) pour activer ou désactiver la reconnexion automatique.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-136">Use the [**EnableAutoReconnect**](imsrdpclientadvancedsettings2-enableautoreconnect.md) property to enable or disable automatic reconnection.</span></span>

 

<span data-ttu-id="4b9e9-137">Lorsque l’état du processus de reconnexion automatique est modifié en affectant à la valeur du paramètre *pArcContinueStatus* la valeur **autoReconnectContinueManual**, le conteneur contrôle manuellement le processus de reconnexion automatique en appelant [**Connect**](imstscax-connect.md) pour déclencher une tentative de connexion ou se [**déconnecter**](imstscax-disconnect.md) pour annuler le processus de reconnexion automatique.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-137">When the state of the automatic reconnection process is changed by setting the value of the *pArcContinueStatus* parameter to **autoReconnectContinueManual**, the container will manually control the automatic reconnection process by calling [**Connect**](imstscax-connect.md) to trigger a connection attempt or [**Disconnect**](imstscax-disconnect.md) to cancel the automatic reconnection process.</span></span> <span data-ttu-id="4b9e9-138">Une fois défini sur cette valeur, le contrôle cesse d’effectuer des tentatives de reconnexion automatique et devient la stratégie du conteneur pour effectuer des appels de **connexion** afin de déclencher des tentatives de reconnexion automatique.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-138">Once set to this value, the control will stop making automatic reconnection attempts and it becomes the policy of the container to make **Connect** calls to trigger automatic reconnection attempts.</span></span> <span data-ttu-id="4b9e9-139">Cette opération est effectuée lorsque le conteneur fournit un comportement personnalisé d’interface utilisateur pour la reconnexion automatique, par exemple le redémarrage d’une connexion RAS ou VPN abandonnée avant le processus de reconnexion automatique.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-139">This is done when the container provides customized UI behavior for automatic reconnection, such as restarting a dropped RAS or VPN connection before the automatic reconnection process.</span></span>

<span data-ttu-id="4b9e9-140">Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="4b9e9-140">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4b9e9-141">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4b9e9-141">Requirements</span></span>



| <span data-ttu-id="4b9e9-142">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4b9e9-142">Requirement</span></span> | <span data-ttu-id="4b9e9-143">Valeur</span><span class="sxs-lookup"><span data-stu-id="4b9e9-143">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4b9e9-144">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4b9e9-144">Minimum supported client</span></span><br/> | <span data-ttu-id="4b9e9-145">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4b9e9-145">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="4b9e9-146">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4b9e9-146">Minimum supported server</span></span><br/> | <span data-ttu-id="4b9e9-147">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4b9e9-147">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="4b9e9-148">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="4b9e9-148">Type library</span></span><br/>             | <dl> <span data-ttu-id="4b9e9-149"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4b9e9-149"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="4b9e9-150">DLL</span><span class="sxs-lookup"><span data-stu-id="4b9e9-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4b9e9-151"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4b9e9-151"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4b9e9-152">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4b9e9-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b9e9-153">**IMsTscAxEvents**</span><span class="sxs-lookup"><span data-stu-id="4b9e9-153">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





