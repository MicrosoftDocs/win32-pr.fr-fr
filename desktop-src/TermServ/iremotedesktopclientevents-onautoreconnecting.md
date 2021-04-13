---
title: Méthode IRemoteDesktopClientEvents OnAutoReconnecting
description: Appelé lorsque le contrôle client tente de rétablir automatiquement une connexion à une session à distance.
ms.assetid: 299408A9-ED14-42F4-B324-AF4C86FEDABE
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode OnAutoReconnecting
- Méthode OnAutoReconnecting Services Bureau à distance, interface IRemoteDesktopClientEvents
- Services Bureau à distance de l’interface IRemoteDesktopClientEvents, méthode OnAutoReconnecting
topic_type:
- apiref
api_name:
- IRemoteDesktopClientEvents.OnAutoReconnecting
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d74c37919384727fdf51aad004349478798a3ffd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509394"
---
# <a name="iremotedesktopclienteventsonautoreconnecting-method"></a><span data-ttu-id="f5b96-106">IRemoteDesktopClientEvents :: OnAutoReconnecting, méthode</span><span class="sxs-lookup"><span data-stu-id="f5b96-106">IRemoteDesktopClientEvents::OnAutoReconnecting method</span></span>

<span data-ttu-id="f5b96-107">Appelé lorsque le contrôle client tente de rétablir automatiquement une connexion à une session à distance.</span><span class="sxs-lookup"><span data-stu-id="f5b96-107">Called when the client control attempts to automatically reestablish a connection to a remote session.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5b96-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f5b96-108">Syntax</span></span>


```C++
void OnAutoReconnecting(
  [in] long         disconnectReason,
  [in] long         ExtendedDisconnectReason,
  [in] BSTR         disconnectErrorMessage,
  [in] VARIANT_BOOL networkAvailable,
  [in] long         attemptCount,
  [in] long         maxAttemptCount
);
```



## <a name="parameters"></a><span data-ttu-id="f5b96-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f5b96-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5b96-110">*disconnectReason* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f5b96-110">*disconnectReason* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f5b96-111">Raison de l’événement de déconnexion.</span><span class="sxs-lookup"><span data-stu-id="f5b96-111">The reason for the disconnect event.</span></span>

</dd> <dt>

<span data-ttu-id="f5b96-112">*ExtendedDisconnectReason* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f5b96-112">*ExtendedDisconnectReason* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f5b96-113">Informations étendues pour l’événement de déconnexion.</span><span class="sxs-lookup"><span data-stu-id="f5b96-113">Extended information for the disconnect event.</span></span>

</dd> <dt>

<span data-ttu-id="f5b96-114">*disconnectErrorMessage* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f5b96-114">*disconnectErrorMessage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f5b96-115">Message d’erreur pour l’événement de déconnexion.</span><span class="sxs-lookup"><span data-stu-id="f5b96-115">The error message for the disconnect event.</span></span>

</dd> <dt>

<span data-ttu-id="f5b96-116">*networkAvailable* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f5b96-116">*networkAvailable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f5b96-117">Indique si le réseau est disponible.</span><span class="sxs-lookup"><span data-stu-id="f5b96-117">Whether the network is available.</span></span>

</dd> <dt>

<span data-ttu-id="f5b96-118">*attemptCount* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f5b96-118">*attemptCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f5b96-119">La tentative est.</span><span class="sxs-lookup"><span data-stu-id="f5b96-119">Which attempt this is.</span></span>

</dd> <dt>

<span data-ttu-id="f5b96-120">*maxAttemptCount* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f5b96-120">*maxAttemptCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f5b96-121">Le nombre maximal de tentatives de reconnexion est effectué.</span><span class="sxs-lookup"><span data-stu-id="f5b96-121">The maximum number of reconnect attempts will be performed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f5b96-122">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f5b96-122">Return value</span></span>

<span data-ttu-id="f5b96-123">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="f5b96-123">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5b96-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f5b96-124">Requirements</span></span>



| <span data-ttu-id="f5b96-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f5b96-125">Requirement</span></span> | <span data-ttu-id="f5b96-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="f5b96-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5b96-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f5b96-127">Minimum supported client</span></span><br/> | <span data-ttu-id="f5b96-128">Windows 8</span><span class="sxs-lookup"><span data-stu-id="f5b96-128">Windows 8</span></span><br/>                                                                           |
| <span data-ttu-id="f5b96-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f5b96-129">Minimum supported server</span></span><br/> | <span data-ttu-id="f5b96-130">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f5b96-130">Windows Server 2012</span></span><br/>                                                                 |
| <span data-ttu-id="f5b96-131">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="f5b96-131">Type library</span></span><br/>             | <dl> <span data-ttu-id="f5b96-132"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f5b96-132"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="f5b96-133">DLL</span><span class="sxs-lookup"><span data-stu-id="f5b96-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f5b96-134"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f5b96-134"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="f5b96-135">IID</span><span class="sxs-lookup"><span data-stu-id="f5b96-135">IID</span></span><br/>                      | <span data-ttu-id="f5b96-136">DIID \_ IRemoteDesktopClientEvents est défini comme 079863B7-6D47-4105-8BFE-0CDCB360E67D</span><span class="sxs-lookup"><span data-stu-id="f5b96-136">DIID\_IRemoteDesktopClientEvents is defined as 079863B7-6D47-4105-8BFE-0CDCB360E67D</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f5b96-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f5b96-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5b96-138">**IRemoteDesktopClientEvents**</span><span class="sxs-lookup"><span data-stu-id="f5b96-138">**IRemoteDesktopClientEvents**</span></span>](iremotedesktopclientevents.md)
</dt> </dl>

 

 





