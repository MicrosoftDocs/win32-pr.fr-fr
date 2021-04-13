---
title: MpHandleClose, fonction (MpClient. h)
description: Ferme le handle retourné par MpManagerOpen, MpScanStart, MpThreatOpen ou MpUpdateStart.
ms.assetid: 335776E2-7598-4DC1-92AB-B49B35222EF6
keywords:
- Fonctionnalités d’environnement Windows hérités de la fonction MpHandleClose
topic_type:
- apiref
api_name:
- MpHandleClose
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43c937548c8e1d3b98aa2e3d10d7577f8c69c1c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509226"
---
# <a name="mphandleclose-function"></a><span data-ttu-id="6a195-104">MpHandleClose fonction)</span><span class="sxs-lookup"><span data-stu-id="6a195-104">MpHandleClose function</span></span>

<span data-ttu-id="6a195-105">Ferme le handle retourné par [**MpManagerOpen**](mpmanageropen.md), [**MpScanStart**](mpscanstart.md), [**MpThreatOpen**](mpthreatopen.md)ou [**MpUpdateStart**](mpupdatestart.md).</span><span class="sxs-lookup"><span data-stu-id="6a195-105">Closes the handle returned by [**MpManagerOpen**](mpmanageropen.md), [**MpScanStart**](mpscanstart.md), [**MpThreatOpen**](mpthreatopen.md), or [**MpUpdateStart**](mpupdatestart.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="6a195-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6a195-106">Syntax</span></span>


```C++
HRESULT WINAPI MpHandleClose(
  _In_ MPHANDLE hMpHandle
);
```



## <a name="parameters"></a><span data-ttu-id="6a195-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6a195-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a195-108">*hMpHandle* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6a195-108">*hMpHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a195-109">Type : **MPHANDLE**</span><span class="sxs-lookup"><span data-stu-id="6a195-109">Type: **MPHANDLE**</span></span>

<span data-ttu-id="6a195-110">Handle à fermer.</span><span class="sxs-lookup"><span data-stu-id="6a195-110">Handle to close.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6a195-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6a195-111">Return value</span></span>

<span data-ttu-id="6a195-112">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="6a195-112">Type: **HRESULT**</span></span>

<span data-ttu-id="6a195-113">Si la fonction s’exécute correctement, la valeur de retour est **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="6a195-113">If the function succeeds the return value is **S\_OK**.</span></span>

<span data-ttu-id="6a195-114">Si la fonction échoue, la valeur de retour est un code **HRESULT** en échec.</span><span class="sxs-lookup"><span data-stu-id="6a195-114">If the function fails then the return value is a failed **HRESULT** code.</span></span> <span data-ttu-id="6a195-115">L’appelant peut utiliser la fonction [**MpErrorMessageFormat**](mperrormessageformat.md) pour obtenir une description générique du message d’erreur.</span><span class="sxs-lookup"><span data-stu-id="6a195-115">The caller can use the [**MpErrorMessageFormat**](mperrormessageformat.md) function to get a generic description of the error message.</span></span>

<span data-ttu-id="6a195-116">L’erreur spécifique suivante peut être retournée par la fonction :</span><span class="sxs-lookup"><span data-stu-id="6a195-116">The following specific error can be returned by the function:</span></span>

| <span data-ttu-id="6a195-117">Code de retour</span><span class="sxs-lookup"><span data-stu-id="6a195-117">Return Code</span></span>             | <span data-ttu-id="6a195-118">Description</span><span class="sxs-lookup"><span data-stu-id="6a195-118">Description</span></span>                      |
|-------------------------|----------------------------------|
| <span data-ttu-id="6a195-119">E \_ remporter un \_ \_ descripteur non valide</span><span class="sxs-lookup"><span data-stu-id="6a195-119">E\_WIN\_INVALID\_HANDLE</span></span> | <span data-ttu-id="6a195-120">Le handle spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="6a195-120">The specified handle is invalid.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="6a195-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6a195-121">Requirements</span></span>



| <span data-ttu-id="6a195-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6a195-122">Requirement</span></span> | <span data-ttu-id="6a195-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="6a195-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6a195-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6a195-124">Minimum supported client</span></span><br/> | <span data-ttu-id="6a195-125">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6a195-125">Windows 8 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="6a195-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6a195-126">Minimum supported server</span></span><br/> | <span data-ttu-id="6a195-127">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6a195-127">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6a195-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="6a195-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="6a195-129"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="6a195-129"><dt>MpClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="6a195-130">DLL</span><span class="sxs-lookup"><span data-stu-id="6a195-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6a195-131"><dt>MpClient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6a195-131"><dt>MpClient.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6a195-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6a195-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a195-133">**MpErrorMessageFormat**</span><span class="sxs-lookup"><span data-stu-id="6a195-133">**MpErrorMessageFormat**</span></span>](mperrormessageformat.md)
</dt> <dt>

[<span data-ttu-id="6a195-134">**MpManagerOpen**</span><span class="sxs-lookup"><span data-stu-id="6a195-134">**MpManagerOpen**</span></span>](mpmanageropen.md)
</dt> <dt>

[<span data-ttu-id="6a195-135">**MpScanStart**</span><span class="sxs-lookup"><span data-stu-id="6a195-135">**MpScanStart**</span></span>](mpscanstart.md)
</dt> <dt>

[<span data-ttu-id="6a195-136">**MpThreatOpen**</span><span class="sxs-lookup"><span data-stu-id="6a195-136">**MpThreatOpen**</span></span>](mpthreatopen.md)
</dt> </dl>

 

 





