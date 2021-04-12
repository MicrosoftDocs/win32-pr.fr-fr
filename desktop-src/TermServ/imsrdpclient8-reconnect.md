---
title: Méthode de reconnexion IMsRdpClient8
description: Se reconnecte à la session à distance avec la largeur et la hauteur du nouveau bureau.
ms.assetid: A2C4101D-780A-4973-B87C-025D9140C4BC
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode de reconnexion
- Services Bureau à distance de la méthode de reconnexion, interface IMsRdpClient8
- Services Bureau à distance de l’interface IMsRdpClient8, méthode de reconnexion
- Services Bureau à distance de la méthode de reconnexion, interface IMsRdpClient9
- Services Bureau à distance de l’interface IMsRdpClient9, méthode de reconnexion
- Services Bureau à distance de la méthode de reconnexion, interface IMsRdpClient10
- Services Bureau à distance de l’interface IMsRdpClient10, méthode de reconnexion
topic_type:
- apiref
api_name:
- IMsRdpClient8.Reconnect
- IMsRdpClient9.Reconnect
- IMsRdpClient10.Reconnect
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d62072c56852af6be2965ce63aecf4634de87d11
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519249"
---
# <a name="imsrdpclient8reconnect-method"></a><span data-ttu-id="8d860-110">IMsRdpClient8 :: reconnect, méthode</span><span class="sxs-lookup"><span data-stu-id="8d860-110">IMsRdpClient8::Reconnect method</span></span>

<span data-ttu-id="8d860-111">Se reconnecte à la session à distance avec la largeur et la hauteur du nouveau bureau.</span><span class="sxs-lookup"><span data-stu-id="8d860-111">Reconnects to the remote session with the new desktop width and height.</span></span> <span data-ttu-id="8d860-112">Le contrôle doit déjà être connecté à une session distante pour que cette méthode aboutisse.</span><span class="sxs-lookup"><span data-stu-id="8d860-112">The control must already be connected to a remote session for this method to succeed.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d860-113">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8d860-113">Syntax</span></span>


```C++
HRESULT Reconnect(
  [in]          ULONG                  ulWidth,
  [in]          ULONG                  ulHeight,
  [out, retval] ControlReconnectStatus *pReconnectStatus
);
```



## <a name="parameters"></a><span data-ttu-id="8d860-114">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8d860-114">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8d860-115">*ulWidth* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8d860-115">*ulWidth* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d860-116">Type : **ULong**</span><span class="sxs-lookup"><span data-stu-id="8d860-116">Type: **ULONG**</span></span>

<span data-ttu-id="8d860-117">Nouvelle largeur du bureau, en pixels.</span><span class="sxs-lookup"><span data-stu-id="8d860-117">The new desktop width, in pixels.</span></span> <span data-ttu-id="8d860-118">Consultez la propriété [**DesktopWidth**](imstscax-desktopwidth.md) pour connaître les restrictions de valeur.</span><span class="sxs-lookup"><span data-stu-id="8d860-118">See the [**DesktopWidth**](imstscax-desktopwidth.md) property for value restrictions.</span></span>

</dd> <dt>

<span data-ttu-id="8d860-119">*ulHeight* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8d860-119">*ulHeight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d860-120">Type : **ULong**</span><span class="sxs-lookup"><span data-stu-id="8d860-120">Type: **ULONG**</span></span>

<span data-ttu-id="8d860-121">Nouvelle hauteur du bureau, en pixels.</span><span class="sxs-lookup"><span data-stu-id="8d860-121">The new desktop height, in pixels.</span></span> <span data-ttu-id="8d860-122">Consultez la propriété [**DesktopHeight**](imstscax-desktopheight.md) pour connaître les restrictions de valeur.</span><span class="sxs-lookup"><span data-stu-id="8d860-122">See the [**DesktopHeight**](imstscax-desktopheight.md) property for value restrictions.</span></span>

</dd> <dt>

<span data-ttu-id="8d860-123">*pReconnectStatus* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="8d860-123">*pReconnectStatus* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="8d860-124">Tapez : \**[**ControlReconnectStatus**](controlreconnectstatus.md) \** _</span><span class="sxs-lookup"><span data-stu-id="8d860-124">Type: \**[**ControlReconnectStatus**](controlreconnectstatus.md)\** _</span></span>

<span data-ttu-id="8d860-125">Pointeur vers une variable [_ *ControlReconnectStatus* \*](controlreconnectstatus.md) qui reçoit l’état de l’opération de reconnexion.</span><span class="sxs-lookup"><span data-stu-id="8d860-125">A pointer to a [_ *ControlReconnectStatus*\*](controlreconnectstatus.md) variable that receives the status of the reconnect operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8d860-126">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8d860-126">Return value</span></span>

<span data-ttu-id="8d860-127">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="8d860-127">Type: **HRESULT**</span></span>

<span data-ttu-id="8d860-128">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="8d860-128">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="8d860-129">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="8d860-129">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="8d860-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8d860-130">Requirements</span></span>



| <span data-ttu-id="8d860-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8d860-131">Requirement</span></span> | <span data-ttu-id="8d860-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="8d860-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8d860-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8d860-133">Minimum supported client</span></span><br/> | <span data-ttu-id="8d860-134">Windows 8</span><span class="sxs-lookup"><span data-stu-id="8d860-134">Windows 8</span></span><br/>                                                                   |
| <span data-ttu-id="8d860-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8d860-135">Minimum supported server</span></span><br/> | <span data-ttu-id="8d860-136">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8d860-136">Windows Server 2012</span></span><br/>                                                         |
| <span data-ttu-id="8d860-137">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="8d860-137">Type library</span></span><br/>             | <dl> <span data-ttu-id="8d860-138"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8d860-138"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="8d860-139">DLL</span><span class="sxs-lookup"><span data-stu-id="8d860-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8d860-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8d860-140"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="8d860-141">IID</span><span class="sxs-lookup"><span data-stu-id="8d860-141">IID</span></span><br/>                      | <span data-ttu-id="8d860-142">IID \_ IMsRdpClient8 est défini en tant que 4247E044-9271-43A9-BC49-E2AD9E855D62</span><span class="sxs-lookup"><span data-stu-id="8d860-142">IID\_IMsRdpClient8 is defined as 4247E044-9271-43A9-BC49-E2AD9E855D62</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="8d860-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8d860-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d860-144">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="8d860-144">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="8d860-145">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="8d860-145">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="8d860-146">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="8d860-146">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> <dt>

[<span data-ttu-id="8d860-147">**ControlReconnectStatus**</span><span class="sxs-lookup"><span data-stu-id="8d860-147">**ControlReconnectStatus**</span></span>](controlreconnectstatus.md)
</dt> </dl>

 

 





