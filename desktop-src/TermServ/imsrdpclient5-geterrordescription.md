---
title: Méthode IMsRdpClient5 GetErrorDescription
description: Récupère la description de l’erreur pour les événements de déconnexion de la session.
ms.assetid: 8c8f7b10-7f79-4586-845e-e99f5ca81905
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode GetErrorDescription
- Méthode GetErrorDescription Services Bureau à distance, interface IMsRdpClient5
- Services Bureau à distance de l’interface IMsRdpClient5, méthode GetErrorDescription
- Méthode GetErrorDescription Services Bureau à distance, interface IMsRdpClient6
- Services Bureau à distance de l’interface IMsRdpClient6, méthode GetErrorDescription
- Méthode GetErrorDescription Services Bureau à distance, interface IMsRdpClient7
- Services Bureau à distance de l’interface IMsRdpClient7, méthode GetErrorDescription
- Méthode GetErrorDescription Services Bureau à distance, interface IMsRdpClient8
- Services Bureau à distance de l’interface IMsRdpClient8, méthode GetErrorDescription
- Méthode GetErrorDescription Services Bureau à distance, interface IMsRdpClient9
- Services Bureau à distance de l’interface IMsRdpClient9, méthode GetErrorDescription
- Méthode GetErrorDescription Services Bureau à distance, interface IMsRdpClient10
- Services Bureau à distance de l’interface IMsRdpClient10, méthode GetErrorDescription
topic_type:
- apiref
api_name:
- IMsRdpClient5.GetErrorDescription
- IMsRdpClient6.GetErrorDescription
- IMsRdpClient7.GetErrorDescription
- IMsRdpClient8.GetErrorDescription
- IMsRdpClient9.GetErrorDescription
- IMsRdpClient10.GetErrorDescription
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c402a0128286964ddeb1c53cd805e4ef6414bfb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385175"
---
# <a name="imsrdpclient5geterrordescription-method"></a><span data-ttu-id="b7cfa-116">IMsRdpClient5 :: GetErrorDescription, méthode</span><span class="sxs-lookup"><span data-stu-id="b7cfa-116">IMsRdpClient5::GetErrorDescription method</span></span>

<span data-ttu-id="b7cfa-117">Récupère la description de l’erreur pour les événements de déconnexion de la session.</span><span class="sxs-lookup"><span data-stu-id="b7cfa-117">Retrieves the error description for the session disconnect events.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7cfa-118">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b7cfa-118">Syntax</span></span>


```C++
HRESULT GetErrorDescription(
  [in]  UINT disconnectReason,
  [in]  UINT extendedDisconnectReason,
  [out] BSTR *pBstrErrorMsg
);
```



## <a name="parameters"></a><span data-ttu-id="b7cfa-119">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b7cfa-119">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b7cfa-120">*disconnectReason* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b7cfa-120">*disconnectReason* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7cfa-121">Raison de la déconnexion.</span><span class="sxs-lookup"><span data-stu-id="b7cfa-121">The disconnect reason.</span></span>

</dd> <dt>

<span data-ttu-id="b7cfa-122">*extendedDisconnectReason* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b7cfa-122">*extendedDisconnectReason* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7cfa-123">Fournit des informations détaillées sur la raison pour laquelle une déconnexion a été lancée.</span><span class="sxs-lookup"><span data-stu-id="b7cfa-123">Provides detailed information about why a disconnect was initiated.</span></span>

</dd> <dt>

<span data-ttu-id="b7cfa-124">*pBstrErrorMsg* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="b7cfa-124">*pBstrErrorMsg* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b7cfa-125">Pointeur vers une variable **BSTR** qui reçoit le texte du message d’erreur.</span><span class="sxs-lookup"><span data-stu-id="b7cfa-125">A pointer to a **BSTR** variable that receives the error message text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b7cfa-126">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b7cfa-126">Return value</span></span>

<span data-ttu-id="b7cfa-127">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="b7cfa-127">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7cfa-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b7cfa-128">Requirements</span></span>



| <span data-ttu-id="b7cfa-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b7cfa-129">Requirement</span></span> | <span data-ttu-id="b7cfa-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="b7cfa-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b7cfa-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b7cfa-131">Minimum supported client</span></span><br/> | <span data-ttu-id="b7cfa-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b7cfa-132">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="b7cfa-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b7cfa-133">Minimum supported server</span></span><br/> | <span data-ttu-id="b7cfa-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b7cfa-134">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="b7cfa-135">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="b7cfa-135">Type library</span></span><br/>             | <dl> <span data-ttu-id="b7cfa-136"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b7cfa-136"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="b7cfa-137">DLL</span><span class="sxs-lookup"><span data-stu-id="b7cfa-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b7cfa-138"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b7cfa-138"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="b7cfa-139">IID</span><span class="sxs-lookup"><span data-stu-id="b7cfa-139">IID</span></span><br/>                      | <span data-ttu-id="b7cfa-140">IID \_ IMsRdpClient5 est défini en tant que 4eb5335b-6429-477D-B922-e06a28ecd8bf</span><span class="sxs-lookup"><span data-stu-id="b7cfa-140">IID\_IMsRdpClient5 is defined as 4eb5335b-6429-477d-b922-e06a28ecd8bf</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="b7cfa-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b7cfa-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7cfa-142">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="b7cfa-142">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="b7cfa-143">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="b7cfa-143">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="b7cfa-144">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="b7cfa-144">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="b7cfa-145">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="b7cfa-145">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="b7cfa-146">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="b7cfa-146">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="b7cfa-147">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="b7cfa-147">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





