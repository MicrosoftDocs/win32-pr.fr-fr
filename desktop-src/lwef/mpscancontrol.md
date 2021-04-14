---
title: MpScanControl, fonction (MpClient. h)
description: Permet le contrôle d’une analyse qui a été initialisée de façon asynchrone par le biais de MpScanStart.
ms.assetid: 00855686-8C46-4B58-829C-AEAB53888704
keywords:
- Fonctionnalités d’environnement Windows hérités de la fonction MpScanControl
topic_type:
- apiref
api_name:
- MpScanControl
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce74736c4ca8c589e2ffa5570f2b6666838d820f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465162"
---
# <a name="mpscancontrol-function"></a><span data-ttu-id="a7636-104">MpScanControl fonction)</span><span class="sxs-lookup"><span data-stu-id="a7636-104">MpScanControl function</span></span>

<span data-ttu-id="a7636-105">Permet le contrôle d’une analyse qui a été initialisée de façon asynchrone par le biais de [**MpScanStart**](mpscanstart.md).</span><span class="sxs-lookup"><span data-stu-id="a7636-105">Allows the control of a scan that was asynchronously initiated via [**MpScanStart**](mpscanstart.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="a7636-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a7636-106">Syntax</span></span>


```C++
HRESULT WINAPI MpScanControl(
  _In_ MPHANDLE  hScanHandle,
  _In_ MPCONTROL ScanControl
);
```



## <a name="parameters"></a><span data-ttu-id="a7636-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a7636-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a7636-108">*hScanHandle* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a7636-108">*hScanHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a7636-109">Type : **MPHANDLE**</span><span class="sxs-lookup"><span data-stu-id="a7636-109">Type: **MPHANDLE**</span></span>

<span data-ttu-id="a7636-110">Handle vers une opération d’analyse asynchrone.</span><span class="sxs-lookup"><span data-stu-id="a7636-110">Handle to an asynchronous scan operation.</span></span> <span data-ttu-id="a7636-111">Ce descripteur est retourné par la fonction [**MpScanStart**](mpscanstart.md) .</span><span class="sxs-lookup"><span data-stu-id="a7636-111">This handle is returned by the [**MpScanStart**](mpscanstart.md) function.</span></span> <span data-ttu-id="a7636-112">Ce paramètre peut également être défini sur le descripteur de l’interface du gestionnaire de protection contre les programmes malveillants renvoyé par la fonction [**MpManagerOpen**](mpmanageropen.md) pour contrôler une analyse initiée par le système, auquel cas l’appelant doit avoir des privilèges d’administrateur.</span><span class="sxs-lookup"><span data-stu-id="a7636-112">This parameter can also be set to the malware protection manager interface handle returned by [**MpManagerOpen**](mpmanageropen.md) function to control a system initiated scan, in which case the caller must have administrative privilege.</span></span>

</dd> <dt>

<span data-ttu-id="a7636-113">*ScanControl* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a7636-113">*ScanControl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a7636-114">Type : **fichier mpcontrol**</span><span class="sxs-lookup"><span data-stu-id="a7636-114">Type: **MPCONTROL**</span></span>

<span data-ttu-id="a7636-115">Spécifie une option de contrôle de l’analyse.</span><span class="sxs-lookup"><span data-stu-id="a7636-115">Specifies a scan control option.</span></span> <span data-ttu-id="a7636-116">Ce paramètre doit être l’une des options de contrôle suivantes :</span><span class="sxs-lookup"><span data-stu-id="a7636-116">This parameter must be one of the following control options:</span></span>



| <span data-ttu-id="a7636-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="a7636-117">Value</span></span>                                                                                                                                                                  | <span data-ttu-id="a7636-118">Signification</span><span class="sxs-lookup"><span data-stu-id="a7636-118">Meaning</span></span>                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <span id="MPCONTROL_ABORT"></span><span id="mpcontrol_abort"></span><dl> <span data-ttu-id="a7636-119"><dt>**\_abandon fichier mpcontrol**</dt></span><span class="sxs-lookup"><span data-stu-id="a7636-119"><dt>**MPCONTROL\_ABORT**</dt></span></span> </dl>    | <span data-ttu-id="a7636-120">Abandon de l’opération d’analyse.</span><span class="sxs-lookup"><span data-stu-id="a7636-120">Abort the scan operation.</span></span><br/>         |
| <span id="MPCONTROL_PAUSE"></span><span id="mpcontrol_pause"></span><dl> <span data-ttu-id="a7636-121"><dt>**\_Pause fichier mpcontrol**</dt></span><span class="sxs-lookup"><span data-stu-id="a7636-121"><dt>**MPCONTROL\_PAUSE**</dt></span></span> </dl>    | <span data-ttu-id="a7636-122">Interrompez l’opération d’analyse.</span><span class="sxs-lookup"><span data-stu-id="a7636-122">Pause the scan operation.</span></span><br/>         |
| <span id="MPCONTROL_RESUME"></span><span id="mpcontrol_resume"></span><dl> <span data-ttu-id="a7636-123"><dt>**FICHIER MPCONTROL \_ Resume**</dt></span><span class="sxs-lookup"><span data-stu-id="a7636-123"><dt>**MPCONTROL\_RESUME**</dt></span></span> </dl> | <span data-ttu-id="a7636-124">Reprise de l’opération d’analyse en pause.</span><span class="sxs-lookup"><span data-stu-id="a7636-124">Resume the paused scan operation.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a7636-125">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a7636-125">Return value</span></span>

<span data-ttu-id="a7636-126">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="a7636-126">Type: **HRESULT**</span></span>

<span data-ttu-id="a7636-127">Si la fonction s’exécute correctement, la valeur de retour est **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="a7636-127">If the function succeeds the return value is **S\_OK**.</span></span>

<span data-ttu-id="a7636-128">Si la fonction échoue, la valeur de retour est un code **HRESULT** en échec.</span><span class="sxs-lookup"><span data-stu-id="a7636-128">If the function fails then the return value is a failed **HRESULT** code.</span></span> <span data-ttu-id="a7636-129">L’appelant peut utiliser la fonction [**MpErrorMessageFormat**](mperrormessageformat.md) pour obtenir une description générique du message d’erreur.</span><span class="sxs-lookup"><span data-stu-id="a7636-129">The caller can use the [**MpErrorMessageFormat**](mperrormessageformat.md) function to get a generic description of the error message.</span></span>

## <a name="requirements"></a><span data-ttu-id="a7636-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a7636-130">Requirements</span></span>



| <span data-ttu-id="a7636-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a7636-131">Requirement</span></span> | <span data-ttu-id="a7636-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="a7636-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a7636-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a7636-133">Minimum supported client</span></span><br/> | <span data-ttu-id="a7636-134">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a7636-134">Windows 8 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="a7636-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a7636-135">Minimum supported server</span></span><br/> | <span data-ttu-id="a7636-136">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a7636-136">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a7636-137">En-tête</span><span class="sxs-lookup"><span data-stu-id="a7636-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="a7636-138"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="a7636-138"><dt>MpClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="a7636-139">DLL</span><span class="sxs-lookup"><span data-stu-id="a7636-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a7636-140"><dt>MpClient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a7636-140"><dt>MpClient.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a7636-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a7636-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7636-142">**MpErrorMessageFormat**</span><span class="sxs-lookup"><span data-stu-id="a7636-142">**MpErrorMessageFormat**</span></span>](mperrormessageformat.md)
</dt> <dt>

[<span data-ttu-id="a7636-143">**MpManagerOpen**</span><span class="sxs-lookup"><span data-stu-id="a7636-143">**MpManagerOpen**</span></span>](mpmanageropen.md)
</dt> <dt>

[<span data-ttu-id="a7636-144">**MpScanStart**</span><span class="sxs-lookup"><span data-stu-id="a7636-144">**MpScanStart**</span></span>](mpscanstart.md)
</dt> </dl>

 

 





