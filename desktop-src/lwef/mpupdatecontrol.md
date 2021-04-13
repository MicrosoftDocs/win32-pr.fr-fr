---
title: MpUpdateControl, fonction (MpClient. h)
description: Autorise le contrôle d’une opération de mise à jour de signature qui a été lancée de manière asynchrone via MpUpdateStart.
ms.assetid: 2780E472-6E8D-4839-88EE-46E3448C6BF5
keywords:
- Fonctionnalités d’environnement Windows hérités de la fonction MpUpdateControl
topic_type:
- apiref
api_name:
- MpUpdateControl
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91ea28c6ace349fd04fb9241d7eddbe7c1e5fbbe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465934"
---
# <a name="mpupdatecontrol-function"></a><span data-ttu-id="5c0c1-104">MpUpdateControl fonction)</span><span class="sxs-lookup"><span data-stu-id="5c0c1-104">MpUpdateControl function</span></span>

<span data-ttu-id="5c0c1-105">Autorise le contrôle d’une opération de mise à jour de signature qui a été lancée de manière asynchrone via [**MpUpdateStart**](mpupdatestart.md).</span><span class="sxs-lookup"><span data-stu-id="5c0c1-105">Allows the control of a signature update operation that was asynchronously initiated via [**MpUpdateStart**](mpupdatestart.md).</span></span> <span data-ttu-id="5c0c1-106">L’appel de cette fonction requiert des privilèges d’administrateur, car elle permet l’annulation d’une mise à jour de signature à l’ensemble du système.</span><span class="sxs-lookup"><span data-stu-id="5c0c1-106">Calling this function requires administrator privilege as it allows the cancellation of a system-wide signature update.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c0c1-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5c0c1-107">Syntax</span></span>


```C++
HRESULT WINAPI MpUpdateControl(
  _In_ MPHANDLE  hUpdateHandle,
  _In_ MPCONTROL UpdateControl
);
```



## <a name="parameters"></a><span data-ttu-id="5c0c1-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5c0c1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5c0c1-109">*hUpdateHandle* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5c0c1-109">*hUpdateHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5c0c1-110">Type : **MPHANDLE**</span><span class="sxs-lookup"><span data-stu-id="5c0c1-110">Type: **MPHANDLE**</span></span>

<span data-ttu-id="5c0c1-111">Handle vers une opération de mise à jour de signature asynchrone.</span><span class="sxs-lookup"><span data-stu-id="5c0c1-111">Handle to an asynchronous signature update operation.</span></span> <span data-ttu-id="5c0c1-112">Ce descripteur est retourné par la fonction [**MpScanStart**](mpscanstart.md) .</span><span class="sxs-lookup"><span data-stu-id="5c0c1-112">This handle is returned by the [**MpScanStart**](mpscanstart.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="5c0c1-113">*UpdateControl* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5c0c1-113">*UpdateControl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5c0c1-114">Type : **fichier mpcontrol**</span><span class="sxs-lookup"><span data-stu-id="5c0c1-114">Type: **MPCONTROL**</span></span>

<span data-ttu-id="5c0c1-115">Spécifie l’option de contrôle de mise à jour de signature.</span><span class="sxs-lookup"><span data-stu-id="5c0c1-115">Specifies the signature update control option.</span></span> <span data-ttu-id="5c0c1-116">Il doit s’agir de la valeur suivante :</span><span class="sxs-lookup"><span data-stu-id="5c0c1-116">It must be the following value:</span></span>



| <span data-ttu-id="5c0c1-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="5c0c1-117">Value</span></span>                                                                                                                                                               | <span data-ttu-id="5c0c1-118">Signification</span><span class="sxs-lookup"><span data-stu-id="5c0c1-118">Meaning</span></span>                                          |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <span id="MPCONTROL_ABORT"></span><span id="mpcontrol_abort"></span><dl> <span data-ttu-id="5c0c1-119"><dt>**\_abandon fichier mpcontrol**</dt></span><span class="sxs-lookup"><span data-stu-id="5c0c1-119"><dt>**MPCONTROL\_ABORT**</dt></span></span> </dl> | <span data-ttu-id="5c0c1-120">Abandonner l’opération de mise à jour de signature.</span><span class="sxs-lookup"><span data-stu-id="5c0c1-120">Abort the signature update operation.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5c0c1-121">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5c0c1-121">Return value</span></span>

<span data-ttu-id="5c0c1-122">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="5c0c1-122">Type: **HRESULT**</span></span>

<span data-ttu-id="5c0c1-123">Si la fonction s’exécute correctement, la valeur de retour est **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="5c0c1-123">If the function succeeds the return value is **S\_OK**.</span></span>

<span data-ttu-id="5c0c1-124">Si la fonction échoue, la valeur de retour est un code **HRESULT** en échec.</span><span class="sxs-lookup"><span data-stu-id="5c0c1-124">If the function fails then the return value is a failed **HRESULT** code.</span></span> <span data-ttu-id="5c0c1-125">L’appelant peut utiliser la fonction [**MpErrorMessageFormat**](mperrormessageformat.md) pour obtenir une description générique du message d’erreur.</span><span class="sxs-lookup"><span data-stu-id="5c0c1-125">The caller can use the [**MpErrorMessageFormat**](mperrormessageformat.md) function to get a generic description of the error message.</span></span>

## <a name="requirements"></a><span data-ttu-id="5c0c1-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5c0c1-126">Requirements</span></span>



| <span data-ttu-id="5c0c1-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5c0c1-127">Requirement</span></span> | <span data-ttu-id="5c0c1-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="5c0c1-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5c0c1-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5c0c1-129">Minimum supported client</span></span><br/> | <span data-ttu-id="5c0c1-130">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5c0c1-130">Windows 8 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="5c0c1-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5c0c1-131">Minimum supported server</span></span><br/> | <span data-ttu-id="5c0c1-132">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5c0c1-132">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="5c0c1-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="5c0c1-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="5c0c1-134"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="5c0c1-134"><dt>MpClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="5c0c1-135">DLL</span><span class="sxs-lookup"><span data-stu-id="5c0c1-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5c0c1-136"><dt>MpClient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5c0c1-136"><dt>MpClient.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5c0c1-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5c0c1-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c0c1-138">**MpErrorMessageFormat**</span><span class="sxs-lookup"><span data-stu-id="5c0c1-138">**MpErrorMessageFormat**</span></span>](mperrormessageformat.md)
</dt> <dt>

[<span data-ttu-id="5c0c1-139">**MpScanStart**</span><span class="sxs-lookup"><span data-stu-id="5c0c1-139">**MpScanStart**</span></span>](mpscanstart.md)
</dt> </dl>

 

 





