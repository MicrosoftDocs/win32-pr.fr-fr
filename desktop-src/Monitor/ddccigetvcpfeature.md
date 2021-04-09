---
title: DDCCIGetVCPFeature fonction)
description: Obtient la valeur actuelle, la valeur maximale et le type de code d’un code du panneau de configuration virtuel (VCP) pour une analyse.
ms.assetid: 7749d45c-a0d5-44ee-8f91-811677cbf59f
keywords:
- Configuration de l’analyse de fonction DDCCIGetVCPFeature
topic_type:
- apiref
api_name:
- DDCCIGetVCPFeature
api_location:
- gdi32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5758bbd1c86b9f228b64063fdd05c04cb05bedcb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942100"
---
# <a name="ddccigetvcpfeature-function"></a><span data-ttu-id="ba035-104">DDCCIGetVCPFeature fonction)</span><span class="sxs-lookup"><span data-stu-id="ba035-104">DDCCIGetVCPFeature function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ba035-105">Cette fonction est utilisée par l’API de configuration de l’analyse pour accéder aux fonctionnalités dans le pilote d’affichage.</span><span class="sxs-lookup"><span data-stu-id="ba035-105">This function is used by the monitor configuration API to access functionality in the display driver.</span></span> <span data-ttu-id="ba035-106">Les applications ne doivent pas appeler cette fonction.</span><span class="sxs-lookup"><span data-stu-id="ba035-106">Applications should not call this function.</span></span>

 

<span data-ttu-id="ba035-107">Obtient la valeur actuelle, la valeur maximale et le type de code d’un code du panneau de configuration virtuel (VCP) pour une analyse.</span><span class="sxs-lookup"><span data-stu-id="ba035-107">Gets the current value, maximum value, and code type of a Virtual Control Panel (VCP) code for a monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba035-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ba035-108">Syntax</span></span>


```C++
NTSTATUS WINAPI DDCCIGetVCPFeature(
  _In_      HANDLE             hMonitor,
  _In_      DWORD              dwVCPCode,
  _Out_opt_ LPMC_VCP_CODE_TYPE pvct,
  _Out_     DWORD              *pdwCurrentValue,
  _Out_opt_ DWORD              *pdwMaximumValue
);
```



## <a name="parameters"></a><span data-ttu-id="ba035-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ba035-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ba035-110">*hMonitor* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ba035-110">*hMonitor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ba035-111">Handle d’une analyse physique.</span><span class="sxs-lookup"><span data-stu-id="ba035-111">A handle to a physical monitor.</span></span>

</dd> <dt>

<span data-ttu-id="ba035-112">*dwVCPCode* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ba035-112">*dwVCPCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ba035-113">Code VCP à interroger.</span><span class="sxs-lookup"><span data-stu-id="ba035-113">The VCP code to query.</span></span>

</dd> <dt>

<span data-ttu-id="ba035-114">*pvct* \[ out, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="ba035-114">*pvct* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ba035-115">Reçoit le type de code VCP, en tant que membre de l’énumération de [**\_ \_ \_ type de code VCP MD**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/ne-lowlevelmonitorconfigurationapi-mc_vcp_code_type) .</span><span class="sxs-lookup"><span data-stu-id="ba035-115">Receives the VCP code type, as a member of the [**MC\_VCP\_CODE\_TYPE**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/ne-lowlevelmonitorconfigurationapi-mc_vcp_code_type) enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="ba035-116">*pdwCurrentValue* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="ba035-116">*pdwCurrentValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ba035-117">Reçoit la valeur actuelle du code VCP.</span><span class="sxs-lookup"><span data-stu-id="ba035-117">Receives the current value of the VCP code.</span></span>

</dd> <dt>

<span data-ttu-id="ba035-118">*pdwMaximumValue* \[ out, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="ba035-118">*pdwMaximumValue* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ba035-119">Reçoit la valeur maximale du code VCP.</span><span class="sxs-lookup"><span data-stu-id="ba035-119">Receives the maximum value of the VCP code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ba035-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ba035-120">Return value</span></span>

<span data-ttu-id="ba035-121">Si la méthode réussit, elle retourne l' **état \_ Success**.</span><span class="sxs-lookup"><span data-stu-id="ba035-121">If the method succeeds, it returns **STATUS\_SUCCESS**.</span></span> <span data-ttu-id="ba035-122">Sinon, elle retourne un code d’erreur **NTSTATUS** .</span><span class="sxs-lookup"><span data-stu-id="ba035-122">Otherwise, it returns an **NTSTATUS** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="ba035-123">Notes</span><span class="sxs-lookup"><span data-stu-id="ba035-123">Remarks</span></span>

<span data-ttu-id="ba035-124">Les applications doivent appeler [**GetVCPFeatureAndVCPFeatureReply**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-getvcpfeatureandvcpfeaturereply) au lieu d’appeler cette fonction.</span><span class="sxs-lookup"><span data-stu-id="ba035-124">Applications should call [**GetVCPFeatureAndVCPFeatureReply**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-getvcpfeatureandvcpfeaturereply) instead of calling this function.</span></span>

<span data-ttu-id="ba035-125">Cette fonction n’a pas de bibliothèque d’importation associée.</span><span class="sxs-lookup"><span data-stu-id="ba035-125">This function has no associated import library.</span></span> <span data-ttu-id="ba035-126">Pour appeler cette fonction, vous devez utiliser les fonctions [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) pour établir une liaison dynamique à Gdi32.dll.</span><span class="sxs-lookup"><span data-stu-id="ba035-126">To call this function, you must use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Gdi32.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="ba035-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ba035-127">Requirements</span></span>



| <span data-ttu-id="ba035-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ba035-128">Requirement</span></span> | <span data-ttu-id="ba035-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="ba035-129">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="ba035-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ba035-130">Minimum supported client</span></span><br/> | <span data-ttu-id="ba035-131">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ba035-131">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="ba035-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ba035-132">Minimum supported server</span></span><br/> | <span data-ttu-id="ba035-133">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ba035-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="ba035-134">DLL</span><span class="sxs-lookup"><span data-stu-id="ba035-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ba035-135"><dt>Gdi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ba035-135"><dt>Gdi32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ba035-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ba035-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba035-137">Surveiller les fonctions de configuration</span><span class="sxs-lookup"><span data-stu-id="ba035-137">Monitor Configuration Functions</span></span>](monitor-configuration-functions.md)
</dt> </dl>

 

