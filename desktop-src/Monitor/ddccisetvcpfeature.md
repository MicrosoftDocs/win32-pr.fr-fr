---
title: DDCCISetVCPFeature fonction)
description: Définit la valeur d’un code du panneau de configuration virtuel (VCP) pour une analyse.
ms.assetid: 1069588b-5f8a-49da-b857-6f0a0c737a11
keywords:
- Configuration de l’analyse de fonction DDCCISetVCPFeature
topic_type:
- apiref
api_name:
- DDCCISetVCPFeature
api_location:
- gdi32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a72da2b2540c73e023a753a3fdb28507f8cbb40d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103601"
---
# <a name="ddccisetvcpfeature-function"></a><span data-ttu-id="5a2b6-104">DDCCISetVCPFeature fonction)</span><span class="sxs-lookup"><span data-stu-id="5a2b6-104">DDCCISetVCPFeature function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5a2b6-105">Cette fonction est utilisée par l’API de configuration de l’analyse pour accéder aux fonctionnalités dans le pilote d’affichage.</span><span class="sxs-lookup"><span data-stu-id="5a2b6-105">This function is used by the monitor configuration API to access functionality in the display driver.</span></span> <span data-ttu-id="5a2b6-106">Les applications ne doivent pas appeler cette fonction.</span><span class="sxs-lookup"><span data-stu-id="5a2b6-106">Applications should not call this function.</span></span>

 

<span data-ttu-id="5a2b6-107">Définit la valeur d’un code du panneau de configuration virtuel (VCP) pour une analyse.</span><span class="sxs-lookup"><span data-stu-id="5a2b6-107">Sets the value of a Virtual Control Panel (VCP) code for a monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a2b6-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5a2b6-108">Syntax</span></span>


```C++
NTSTATUS WINAPI DDCCISetVCPFeature(
  _In_ HANDLE hMonitor,
  _In_ DWORD  dwVCPCode,
  _In_ DWORD  dwNewValue
);
```



## <a name="parameters"></a><span data-ttu-id="5a2b6-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5a2b6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a2b6-110">*hMonitor* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5a2b6-110">*hMonitor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a2b6-111">Handle d’une analyse physique.</span><span class="sxs-lookup"><span data-stu-id="5a2b6-111">A handle to a physical monitor.</span></span>

</dd> <dt>

<span data-ttu-id="5a2b6-112">*dwVCPCode* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5a2b6-112">*dwVCPCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a2b6-113">Code VCP à définir.</span><span class="sxs-lookup"><span data-stu-id="5a2b6-113">The VCP code to set.</span></span>

</dd> <dt>

<span data-ttu-id="5a2b6-114">*dwNewValue* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5a2b6-114">*dwNewValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a2b6-115">Valeur du code VCP.</span><span class="sxs-lookup"><span data-stu-id="5a2b6-115">The value of the VCP code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5a2b6-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5a2b6-116">Return value</span></span>

<span data-ttu-id="5a2b6-117">Si la méthode réussit, elle retourne l' **état \_ Success**.</span><span class="sxs-lookup"><span data-stu-id="5a2b6-117">If the method succeeds, it returns **STATUS\_SUCCESS**.</span></span> <span data-ttu-id="5a2b6-118">Sinon, elle retourne un code d’erreur **NTSTATUS** .</span><span class="sxs-lookup"><span data-stu-id="5a2b6-118">Otherwise, it returns an **NTSTATUS** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="5a2b6-119">Notes</span><span class="sxs-lookup"><span data-stu-id="5a2b6-119">Remarks</span></span>

<span data-ttu-id="5a2b6-120">Les applications doivent appeler [**SetVCPFeature**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-setvcpfeature) au lieu d’appeler cette fonction.</span><span class="sxs-lookup"><span data-stu-id="5a2b6-120">Applications should call [**SetVCPFeature**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-setvcpfeature) instead of calling this function.</span></span>

<span data-ttu-id="5a2b6-121">Cette fonction n’a pas de bibliothèque d’importation associée.</span><span class="sxs-lookup"><span data-stu-id="5a2b6-121">This function has no associated import library.</span></span> <span data-ttu-id="5a2b6-122">Pour appeler cette fonction, vous devez utiliser les fonctions [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) pour établir une liaison dynamique à Gdi32.dll.</span><span class="sxs-lookup"><span data-stu-id="5a2b6-122">To call this function, you must use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Gdi32.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="5a2b6-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5a2b6-123">Requirements</span></span>



| <span data-ttu-id="5a2b6-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5a2b6-124">Requirement</span></span> | <span data-ttu-id="5a2b6-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="5a2b6-125">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="5a2b6-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5a2b6-126">Minimum supported client</span></span><br/> | <span data-ttu-id="5a2b6-127">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5a2b6-127">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="5a2b6-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5a2b6-128">Minimum supported server</span></span><br/> | <span data-ttu-id="5a2b6-129">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5a2b6-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="5a2b6-130">DLL</span><span class="sxs-lookup"><span data-stu-id="5a2b6-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5a2b6-131"><dt>Gdi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5a2b6-131"><dt>Gdi32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5a2b6-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5a2b6-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a2b6-133">Surveiller les fonctions de configuration</span><span class="sxs-lookup"><span data-stu-id="5a2b6-133">Monitor Configuration Functions</span></span>](monitor-configuration-functions.md)
</dt> </dl>

 

