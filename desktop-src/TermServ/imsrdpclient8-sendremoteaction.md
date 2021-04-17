---
title: Méthode IMsRdpClient8 SendRemoteAction
description: Entraîne l’exécution d’une action dans la session à distance.
ms.assetid: d6a43662-7e51-404a-a3f9-a8b51cbc69d1
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SendRemoteAction
- Méthode SendRemoteAction Services Bureau à distance, interface IMsRdpClient8
- Services Bureau à distance de l’interface IMsRdpClient8, méthode SendRemoteAction
- Méthode SendRemoteAction Services Bureau à distance, interface IMsRdpClient9
- Services Bureau à distance de l’interface IMsRdpClient9, méthode SendRemoteAction
- Méthode SendRemoteAction Services Bureau à distance, interface IMsRdpClient10
- Services Bureau à distance de l’interface IMsRdpClient10, méthode SendRemoteAction
topic_type:
- apiref
api_name:
- IMsRdpClient8.SendRemoteAction
- IMsRdpClient9.SendRemoteAction
- IMsRdpClient10.SendRemoteAction
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a28fc9695686402e0a8e98ed17fc1bc6a47939d8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104467031"
---
# <a name="imsrdpclient8sendremoteaction-method"></a><span data-ttu-id="14cb4-110">IMsRdpClient8 :: SendRemoteAction, méthode</span><span class="sxs-lookup"><span data-stu-id="14cb4-110">IMsRdpClient8::SendRemoteAction method</span></span>

<span data-ttu-id="14cb4-111">Entraîne l’exécution d’une action dans la session à distance.</span><span class="sxs-lookup"><span data-stu-id="14cb4-111">Causes an action to be performed in the remote session.</span></span>

## <a name="syntax"></a><span data-ttu-id="14cb4-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="14cb4-112">Syntax</span></span>


```C++
HRESULT SendRemoteAction(
  [in] RemoteSessionActionType actionType
);
```



## <a name="parameters"></a><span data-ttu-id="14cb4-113">Paramètres</span><span class="sxs-lookup"><span data-stu-id="14cb4-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14cb4-114">*ActionType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="14cb4-114">*actionType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14cb4-115">Valeur de l’énumération [**RemoteSessionActionType**](remotesessionactiontype.md) qui spécifie l’action à envoyer à la session à distance.</span><span class="sxs-lookup"><span data-stu-id="14cb4-115">A value of the [**RemoteSessionActionType**](remotesessionactiontype.md) enumeration that specifies the action to send to the remote session.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14cb4-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="14cb4-116">Return value</span></span>

<span data-ttu-id="14cb4-117">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="14cb4-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="14cb4-118">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="14cb4-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="14cb4-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="14cb4-119">Requirements</span></span>



| <span data-ttu-id="14cb4-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="14cb4-120">Requirement</span></span> | <span data-ttu-id="14cb4-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="14cb4-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="14cb4-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="14cb4-122">Minimum supported client</span></span><br/> | <span data-ttu-id="14cb4-123">Windows 8</span><span class="sxs-lookup"><span data-stu-id="14cb4-123">Windows 8</span></span><br/>                                                                   |
| <span data-ttu-id="14cb4-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="14cb4-124">Minimum supported server</span></span><br/> | <span data-ttu-id="14cb4-125">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="14cb4-125">Windows Server 2012</span></span><br/>                                                         |
| <span data-ttu-id="14cb4-126">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="14cb4-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="14cb4-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="14cb4-127"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="14cb4-128">DLL</span><span class="sxs-lookup"><span data-stu-id="14cb4-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="14cb4-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="14cb4-129"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="14cb4-130">IID</span><span class="sxs-lookup"><span data-stu-id="14cb4-130">IID</span></span><br/>                      | <span data-ttu-id="14cb4-131">IID \_ IMsRdpClient8 est défini en tant que 4247E044-9271-43A9-BC49-E2AD9E855D62</span><span class="sxs-lookup"><span data-stu-id="14cb4-131">IID\_IMsRdpClient8 is defined as 4247E044-9271-43A9-BC49-E2AD9E855D62</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="14cb4-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="14cb4-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14cb4-133">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="14cb4-133">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="14cb4-134">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="14cb4-134">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="14cb4-135">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="14cb4-135">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





