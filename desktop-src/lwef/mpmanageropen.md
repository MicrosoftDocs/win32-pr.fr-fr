---
title: MpManagerOpen, fonction (MpClient. h)
description: Établit une connexion au gestionnaire de protection contre les programmes malveillants sur l’ordinateur local.
ms.assetid: 40513A74-AFCC-4E22-9B78-D46FEB575A00
keywords:
- Fonctionnalités d’environnement Windows hérités de la fonction MpManagerOpen
topic_type:
- apiref
api_name:
- MpManagerOpen
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af432cc7d91530fd3d37176592f7f457b31b6314
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743181"
---
# <a name="mpmanageropen-function"></a><span data-ttu-id="175fd-104">MpManagerOpen fonction)</span><span class="sxs-lookup"><span data-stu-id="175fd-104">MpManagerOpen function</span></span>

<span data-ttu-id="175fd-105">Établit une connexion au gestionnaire de protection contre les programmes malveillants sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="175fd-105">Establishes a connection to the malware protection manager on the local computer.</span></span>

## <a name="syntax"></a><span data-ttu-id="175fd-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="175fd-106">Syntax</span></span>


```C++
HRESULT WINAPI MpManagerOpen(
  _In_  DWORD     dwReserved,
  _Out_ PMPHANDLE phMpHandle
);
```



## <a name="parameters"></a><span data-ttu-id="175fd-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="175fd-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="175fd-108">*dwReserved* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="175fd-108">*dwReserved* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="175fd-109">Type : **DWORD**</span><span class="sxs-lookup"><span data-stu-id="175fd-109">Type: **DWORD**</span></span>

<span data-ttu-id="175fd-110">Réservé pour un usage futur.</span><span class="sxs-lookup"><span data-stu-id="175fd-110">Reserved for future use.</span></span> <span data-ttu-id="175fd-111">Doit avoir la valeur 0.</span><span class="sxs-lookup"><span data-stu-id="175fd-111">Must be set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="175fd-112">*phMpHandle* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="175fd-112">*phMpHandle* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="175fd-113">Type : **PMPHANDLE**</span><span class="sxs-lookup"><span data-stu-id="175fd-113">Type: **PMPHANDLE**</span></span>

<span data-ttu-id="175fd-114">Handle de l’interface du gestionnaire de protection contre les programmes malveillants.</span><span class="sxs-lookup"><span data-stu-id="175fd-114">Handle to the malware protection manager interface.</span></span> <span data-ttu-id="175fd-115">Ce descripteur doit être fermé avec la fonction [**MpHandleClose**](mphandleclose.md) .</span><span class="sxs-lookup"><span data-stu-id="175fd-115">This handle must be closed with the [**MpHandleClose**](mphandleclose.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="175fd-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="175fd-116">Return value</span></span>

<span data-ttu-id="175fd-117">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="175fd-117">Type: **HRESULT**</span></span>

<span data-ttu-id="175fd-118">Si la fonction s’exécute correctement, la valeur de retour est **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="175fd-118">If the function succeeds the return value is **S\_OK**.</span></span> <span data-ttu-id="175fd-119">Cet appel de fonction est garanti, même si un service anti-programme malveillant n’est pas en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="175fd-119">This function call is guaranteed to succeed even if an AntiMalware service is not running.</span></span>

<span data-ttu-id="175fd-120">Si la fonction échoue, la valeur de retour est un code **HRESULT** en échec.</span><span class="sxs-lookup"><span data-stu-id="175fd-120">If the function fails then the return value is a failed **HRESULT** code.</span></span> <span data-ttu-id="175fd-121">L’appelant peut utiliser la fonction [**MpErrorMessageFormat**](mperrormessageformat.md) pour obtenir une description générique du message d’erreur.</span><span class="sxs-lookup"><span data-stu-id="175fd-121">The caller can use the [**MpErrorMessageFormat**](mperrormessageformat.md) function to get a generic description of the error message.</span></span>

## <a name="requirements"></a><span data-ttu-id="175fd-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="175fd-122">Requirements</span></span>



| <span data-ttu-id="175fd-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="175fd-123">Requirement</span></span> | <span data-ttu-id="175fd-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="175fd-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="175fd-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="175fd-125">Minimum supported client</span></span><br/> | <span data-ttu-id="175fd-126">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="175fd-126">Windows 8 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="175fd-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="175fd-127">Minimum supported server</span></span><br/> | <span data-ttu-id="175fd-128">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="175fd-128">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="175fd-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="175fd-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="175fd-130"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="175fd-130"><dt>MpClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="175fd-131">DLL</span><span class="sxs-lookup"><span data-stu-id="175fd-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="175fd-132"><dt>MpClient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="175fd-132"><dt>MpClient.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="175fd-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="175fd-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="175fd-134">**MpErrorMessageFormat**</span><span class="sxs-lookup"><span data-stu-id="175fd-134">**MpErrorMessageFormat**</span></span>](mperrormessageformat.md)
</dt> <dt>

[<span data-ttu-id="175fd-135">**MpHandleClose**</span><span class="sxs-lookup"><span data-stu-id="175fd-135">**MpHandleClose**</span></span>](mphandleclose.md)
</dt> </dl>

 

 





