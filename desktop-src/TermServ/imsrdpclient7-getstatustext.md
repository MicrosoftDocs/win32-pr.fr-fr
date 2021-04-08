---
title: Méthode IMsRdpClient7 GetStatusText (OpenService. h)
description: Récupère le texte d’État pour le code d’état spécifié.
ms.assetid: 1da2280a-c26d-4caa-b227-c289055f3aa9
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode GetStatusText
- Méthode GetStatusText Services Bureau à distance, interface IMsRdpClient7
- Services Bureau à distance de l’interface IMsRdpClient7, méthode GetStatusText
- Méthode GetStatusText Services Bureau à distance, interface IMsRdpClient8
- Services Bureau à distance de l’interface IMsRdpClient8, méthode GetStatusText
- Méthode GetStatusText Services Bureau à distance, interface IMsRdpClient9
- Services Bureau à distance de l’interface IMsRdpClient9, méthode GetStatusText
- Méthode GetStatusText Services Bureau à distance, interface IMsRdpClient10
- Services Bureau à distance de l’interface IMsRdpClient10, méthode GetStatusText
topic_type:
- apiref
api_name:
- IMsRdpClient7.GetStatusText
- IMsRdpClient8.GetStatusText
- IMsRdpClient9.GetStatusText
- IMsRdpClient10.GetStatusText
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 820628bfba59ec980e5128b9d9df3ee21b49a064
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742141"
---
# <a name="imsrdpclient7getstatustext-method"></a><span data-ttu-id="0a86a-112">IMsRdpClient7 :: GetStatusText, méthode</span><span class="sxs-lookup"><span data-stu-id="0a86a-112">IMsRdpClient7::GetStatusText method</span></span>

<span data-ttu-id="0a86a-113">Récupère le texte d’État pour le code d’état spécifié.</span><span class="sxs-lookup"><span data-stu-id="0a86a-113">Retrieves the status text for the specified status code.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a86a-114">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0a86a-114">Syntax</span></span>


```C++
HRESULT GetStatusText(
  [in]          UINT statusCode,
  [out, retval] BSTR *pBstrStatusText
);
```



## <a name="parameters"></a><span data-ttu-id="0a86a-115">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0a86a-115">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0a86a-116">*statusCode* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0a86a-116">*statusCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0a86a-117">**Uint** qui spécifie le code d’État pour lequel récupérer le texte.</span><span class="sxs-lookup"><span data-stu-id="0a86a-117">A **UINT** that specifies the status code to retrieve the text for.</span></span>

</dd> <dt>

<span data-ttu-id="0a86a-118">*pBstrStatusText* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="0a86a-118">*pBstrStatusText* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="0a86a-119">Adresse d’un **BSTR** qui reçoit le texte d’État.</span><span class="sxs-lookup"><span data-stu-id="0a86a-119">The address of a **BSTR** that receives the status text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0a86a-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0a86a-120">Return value</span></span>

<span data-ttu-id="0a86a-121">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="0a86a-121">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="0a86a-122">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0a86a-122">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="0a86a-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0a86a-123">Requirements</span></span>



| <span data-ttu-id="0a86a-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0a86a-124">Requirement</span></span> | <span data-ttu-id="0a86a-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="0a86a-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a86a-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0a86a-126">Minimum supported client</span></span><br/> | <span data-ttu-id="0a86a-127">Windows 7</span><span class="sxs-lookup"><span data-stu-id="0a86a-127">Windows 7</span></span><br/>                                                                     |
| <span data-ttu-id="0a86a-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0a86a-128">Minimum supported server</span></span><br/> | <span data-ttu-id="0a86a-129">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="0a86a-129">Windows Server 2008 R2</span></span><br/>                                                        |
| <span data-ttu-id="0a86a-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="0a86a-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="0a86a-131"><dt>OpenService. h</dt></span><span class="sxs-lookup"><span data-stu-id="0a86a-131"><dt>Openservice.h</dt></span></span> </dl> |
| <span data-ttu-id="0a86a-132">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="0a86a-132">Type library</span></span><br/>             | <dl> <span data-ttu-id="0a86a-133"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0a86a-133"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="0a86a-134">DLL</span><span class="sxs-lookup"><span data-stu-id="0a86a-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0a86a-135"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0a86a-135"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="0a86a-136">IID</span><span class="sxs-lookup"><span data-stu-id="0a86a-136">IID</span></span><br/>                      | <span data-ttu-id="0a86a-137">IID \_ IMsRdpClient7 est défini en tant que b2a5b5ce-3461-444A-91D4-add26d070638</span><span class="sxs-lookup"><span data-stu-id="0a86a-137">IID\_IMsRdpClient7 is defined as b2a5b5ce-3461-444a-91d4-add26d070638</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="0a86a-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0a86a-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a86a-139">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="0a86a-139">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="0a86a-140">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="0a86a-140">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="0a86a-141">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="0a86a-141">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="0a86a-142">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="0a86a-142">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





