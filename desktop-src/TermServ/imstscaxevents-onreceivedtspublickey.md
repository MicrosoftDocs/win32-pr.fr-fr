---
title: Méthode IMsTscAxEvents OnReceivedTSPublicKey
description: Appelé pendant la séquence de connexion lorsque le client récupère la clé publique du serveur. Cet événement est appelé uniquement si la propriété NotifyTSPublicKey a la \_ valeur variant true.
ms.assetid: 1db98b8b-2f08-4252-ad8b-6764fa25b300
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode OnReceivedTSPublicKey
- Méthode OnReceivedTSPublicKey Services Bureau à distance, interface IMsTscAxEvents
- Services Bureau à distance de l’interface IMsTscAxEvents, méthode OnReceivedTSPublicKey
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnReceivedTSPublicKey
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 337a9efabe48dee7a5a4194c3b796b95f35a0592
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465786"
---
# <a name="imstscaxeventsonreceivedtspublickey-method"></a><span data-ttu-id="3fca1-107">IMsTscAxEvents :: OnReceivedTSPublicKey, méthode</span><span class="sxs-lookup"><span data-stu-id="3fca1-107">IMsTscAxEvents::OnReceivedTSPublicKey method</span></span>

<span data-ttu-id="3fca1-108">Appelé pendant la séquence de connexion lorsque le client récupère la clé publique du serveur.</span><span class="sxs-lookup"><span data-stu-id="3fca1-108">Called during the connection sequence when the client retrieves the public key from the server.</span></span> <span data-ttu-id="3fca1-109">Cet événement est appelé uniquement si la propriété **NotifyTSPublicKey** a **la \_ valeur variant true**.</span><span class="sxs-lookup"><span data-stu-id="3fca1-109">This event is only called if the **NotifyTSPublicKey** property is **VARIANT\_TRUE**.</span></span> <span data-ttu-id="3fca1-110">Cela se fait après [**OnConnecting**](imstscaxevents-onconnecting.md), mais avant [**OnAuthenticationWarningDisplayed**](imstscaxevents-onauthenticationwarningdisplayed.md) et [**OnConnected**](imstscaxevents-onconnected.md).</span><span class="sxs-lookup"><span data-stu-id="3fca1-110">This is after [**OnConnecting**](imstscaxevents-onconnecting.md), but before [**OnAuthenticationWarningDisplayed**](imstscaxevents-onauthenticationwarningdisplayed.md) and [**OnConnected**](imstscaxevents-onconnected.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="3fca1-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3fca1-111">Syntax</span></span>


```C++
void OnReceivedTSPublicKey(
  [in]  BSTR         publicKey,
  [out] VARIANT_BOOL *pfContinueLogon
);
```



## <a name="parameters"></a><span data-ttu-id="3fca1-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3fca1-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3fca1-113">*PublicKey* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3fca1-113">*publicKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3fca1-114">Contient la clé publique de l’ordinateur distant.</span><span class="sxs-lookup"><span data-stu-id="3fca1-114">Contains the public key of the remote machine.</span></span>

</dd> <dt>

<span data-ttu-id="3fca1-115">*pfContinueLogon* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="3fca1-115">*pfContinueLogon* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3fca1-116">Pointeur vers une variable **Variant \_ booléenne** qui reçoit une valeur indiquant si le processus d’ouverture de session doit continuer.</span><span class="sxs-lookup"><span data-stu-id="3fca1-116">A pointer to a **VARIANT\_BOOL** variable that receives whether the logon process should continue.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3fca1-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3fca1-117">Return value</span></span>

<span data-ttu-id="3fca1-118">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="3fca1-118">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3fca1-119">Notes</span><span class="sxs-lookup"><span data-stu-id="3fca1-119">Remarks</span></span>

<span data-ttu-id="3fca1-120">Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="3fca1-120">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3fca1-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3fca1-121">Requirements</span></span>



| <span data-ttu-id="3fca1-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3fca1-122">Requirement</span></span> | <span data-ttu-id="3fca1-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="3fca1-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3fca1-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3fca1-124">Minimum supported client</span></span><br/> | <span data-ttu-id="3fca1-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3fca1-125">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="3fca1-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3fca1-126">Minimum supported server</span></span><br/> | <span data-ttu-id="3fca1-127">Windows Server 2008, Windows Server 2008 avec SP1</span><span class="sxs-lookup"><span data-stu-id="3fca1-127">Windows Server 2008, Windows Server 2008 with SP1</span></span><br/>                           |
| <span data-ttu-id="3fca1-128">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="3fca1-128">Type library</span></span><br/>             | <dl> <span data-ttu-id="3fca1-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3fca1-129"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="3fca1-130">DLL</span><span class="sxs-lookup"><span data-stu-id="3fca1-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3fca1-131"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3fca1-131"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="3fca1-132">IID</span><span class="sxs-lookup"><span data-stu-id="3fca1-132">IID</span></span><br/>                      | <span data-ttu-id="3fca1-133">IMsTscAxEvents est défini en tant que 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="3fca1-133">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="3fca1-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3fca1-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3fca1-135">**IMsTscAxEvents**</span><span class="sxs-lookup"><span data-stu-id="3fca1-135">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





