---
title: Méthode IMsTscAxEvents OnConfirmClose
description: Appelée lorsque le client appelle la méthode IMsRdpClient RequestClose.
ms.assetid: fb149fbc-9415-4c4c-8d4b-e22214ac38cb
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode OnConfirmClose
- Méthode OnConfirmClose Services Bureau à distance, interface IMsTscAxEvents
- Services Bureau à distance de l’interface IMsTscAxEvents, méthode OnConfirmClose
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnConfirmClose
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 623196033e23a964857a6a604c7eca3904f32c60
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106486"
---
# <a name="imstscaxeventsonconfirmclose-method"></a><span data-ttu-id="e3dc3-106">IMsTscAxEvents :: OnConfirmClose, méthode</span><span class="sxs-lookup"><span data-stu-id="e3dc3-106">IMsTscAxEvents::OnConfirmClose method</span></span>

<span data-ttu-id="e3dc3-107">Appelée lorsque le client appelle la méthode [**IMsRdpClient :: RequestClose**](imsrdpclient-requestclose.md) .</span><span class="sxs-lookup"><span data-stu-id="e3dc3-107">Called when the client calls the [**IMsRdpClient::RequestClose**](imsrdpclient-requestclose.md) method.</span></span> <span data-ttu-id="e3dc3-108">En réponse à cet événement, l’utilisateur doit être invité à confirmer la fermeture de la connexion.</span><span class="sxs-lookup"><span data-stu-id="e3dc3-108">In response to this event, the user should be prompted to confirm closing the connection.</span></span> <span data-ttu-id="e3dc3-109">Pour plus d'informations, consultez la section Notes qui suit.</span><span class="sxs-lookup"><span data-stu-id="e3dc3-109">For more information, see the following Remarks section.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3dc3-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e3dc3-110">Syntax</span></span>


```C++
void OnConfirmClose(
  [out] VARIANT_BOOL *pfAllowClose
);
```



## <a name="parameters"></a><span data-ttu-id="e3dc3-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e3dc3-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3dc3-112">*pfAllowClose* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="e3dc3-112">*pfAllowClose* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e3dc3-113">Si **la \_ valeur de type Variant est true**, la valeur par défaut indique que l’utilisateur souhaite fermer la connexion.</span><span class="sxs-lookup"><span data-stu-id="e3dc3-113">If **VARIANT\_TRUE**, the default, indicates that the user wants to close the connection.</span></span> <span data-ttu-id="e3dc3-114">Si la **valeur de type Variant est \_ false**, indique que l’utilisateur ne souhaite pas fermer la connexion.</span><span class="sxs-lookup"><span data-stu-id="e3dc3-114">If **VARIANT\_FALSE**, indicates that the user does not want to close the connection.</span></span> <span data-ttu-id="e3dc3-115">Pour plus d'informations, consultez la section Notes qui suit.</span><span class="sxs-lookup"><span data-stu-id="e3dc3-115">For more information, see the following Remarks section.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e3dc3-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e3dc3-116">Return value</span></span>

<span data-ttu-id="e3dc3-117">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="e3dc3-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e3dc3-118">Notes</span><span class="sxs-lookup"><span data-stu-id="e3dc3-118">Remarks</span></span>

<span data-ttu-id="e3dc3-119">Quand une application conteneur appelle la méthode [**IMsRdpClient :: RequestClose**](imsrdpclient-requestclose.md) , cette méthode retourne une valeur indiquant si le conteneur doit attendre qu’un événement **OnConfirmClose** se produise avant de fermer la connexion de contrôle.</span><span class="sxs-lookup"><span data-stu-id="e3dc3-119">When a container application calls the [**IMsRdpClient::RequestClose**](imsrdpclient-requestclose.md) method, that method returns a value indicating whether the container should wait for an **OnConfirmClose** event to occur before closing the control connection.</span></span> <span data-ttu-id="e3dc3-120">Si **RequestClose** retourne **controlCloseWaitForEvents**, et que l’utilisateur est connecté et connecté à sa session services Bureau à distance, l’événement **OnConfirmClose** se déclenche.</span><span class="sxs-lookup"><span data-stu-id="e3dc3-120">If **RequestClose** returns **controlCloseWaitForEvents**, and the user is connected and logged on to their Remote Desktop Services session, the **OnConfirmClose** event fires.</span></span> <span data-ttu-id="e3dc3-121">À ce stade, l’application conteneur peut demander à l’utilisateur s’il souhaite fermer la connexion.</span><span class="sxs-lookup"><span data-stu-id="e3dc3-121">At that point the container application can prompt the user, asking whether the user wants to close the connection.</span></span> <span data-ttu-id="e3dc3-122">Si l’utilisateur souhaite fermer la connexion, l’application doit définir le paramètre *pfAllowClose* sur la **\_ valeur variant true** et procéder à la fermeture de la connexion.</span><span class="sxs-lookup"><span data-stu-id="e3dc3-122">If the user wants to close the connection, the application should set the *pfAllowClose* parameter to **VARIANT\_TRUE** and proceed with closing the connection.</span></span> <span data-ttu-id="e3dc3-123">Si l’utilisateur ne souhaite pas fermer, l’application doit affecter à *pfAllowClose* la valeur **Variant \_ false** et conserver la connexion ouverte.</span><span class="sxs-lookup"><span data-stu-id="e3dc3-123">If the user does not want to close, the application should set *pfAllowClose* to **VARIANT\_FALSE** and leave the connection open.</span></span>

<span data-ttu-id="e3dc3-124">Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="e3dc3-124">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e3dc3-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e3dc3-125">Requirements</span></span>



| <span data-ttu-id="e3dc3-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e3dc3-126">Requirement</span></span> | <span data-ttu-id="e3dc3-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="e3dc3-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e3dc3-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e3dc3-128">Minimum supported client</span></span><br/> | <span data-ttu-id="e3dc3-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e3dc3-129">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="e3dc3-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e3dc3-130">Minimum supported server</span></span><br/> | <span data-ttu-id="e3dc3-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e3dc3-131">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="e3dc3-132">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="e3dc3-132">Type library</span></span><br/>             | <dl> <span data-ttu-id="e3dc3-133"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e3dc3-133"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="e3dc3-134">DLL</span><span class="sxs-lookup"><span data-stu-id="e3dc3-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e3dc3-135"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e3dc3-135"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="e3dc3-136">IID</span><span class="sxs-lookup"><span data-stu-id="e3dc3-136">IID</span></span><br/>                      | <span data-ttu-id="e3dc3-137">IMsTscAxEvents est défini en tant que 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="e3dc3-137">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="e3dc3-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e3dc3-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3dc3-139">**IMsTscAxEvents**</span><span class="sxs-lookup"><span data-stu-id="e3dc3-139">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





