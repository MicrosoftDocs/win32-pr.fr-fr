---
title: DDCCIGetTimingReport fonction)
description: Obtient les fréquences de synchronisation horizontale et verticale d’une analyse.
ms.assetid: d490cb89-082a-42a1-ac0a-335c929cd5d7
keywords:
- Configuration de l’analyse de fonction DDCCIGetTimingReport
topic_type:
- apiref
api_name:
- DDCCIGetTimingReport
api_location:
- gdi32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b87cb4269c2cdff2303bbe763905cb572acfbb7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942101"
---
# <a name="ddccigettimingreport-function"></a><span data-ttu-id="30e0b-104">DDCCIGetTimingReport fonction)</span><span class="sxs-lookup"><span data-stu-id="30e0b-104">DDCCIGetTimingReport function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="30e0b-105">Cette fonction est utilisée par l’API de configuration de l’analyse pour accéder aux fonctionnalités dans le pilote d’affichage.</span><span class="sxs-lookup"><span data-stu-id="30e0b-105">This function is used by the monitor configuration API to access functionality in the display driver.</span></span> <span data-ttu-id="30e0b-106">Les applications ne doivent pas appeler cette fonction.</span><span class="sxs-lookup"><span data-stu-id="30e0b-106">Applications should not call this function.</span></span>

 

<span data-ttu-id="30e0b-107">Obtient les fréquences de synchronisation horizontale et verticale d’une analyse.</span><span class="sxs-lookup"><span data-stu-id="30e0b-107">Gets the horizontal and vertical synchronization frequencies of a monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="30e0b-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="30e0b-108">Syntax</span></span>


```C++
NTSTATUS WINAPI DDCCIGetTimingReport(
  _In_  HANDLE             hMonitor,
  _Out_ LPMC_TIMING_REPORT pmtr
);
```



## <a name="parameters"></a><span data-ttu-id="30e0b-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="30e0b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30e0b-110">*hMonitor* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="30e0b-110">*hMonitor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30e0b-111">Handle d’une analyse physique.</span><span class="sxs-lookup"><span data-stu-id="30e0b-111">A handle to a physical monitor.</span></span>

</dd> <dt>

<span data-ttu-id="30e0b-112">*PMTR* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="30e0b-112">*pmtr* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="30e0b-113">Pointeur vers une structure [**de \_ \_ rapport de minutage MC**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/ns-lowlevelmonitorconfigurationapi-mc_timing_report) qui reçoit les informations de minutage.</span><span class="sxs-lookup"><span data-stu-id="30e0b-113">A pointer to an [**MC\_TIMING\_REPORT**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/ns-lowlevelmonitorconfigurationapi-mc_timing_report) structure that receives the timing information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30e0b-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="30e0b-114">Return value</span></span>

<span data-ttu-id="30e0b-115">Si la méthode réussit, elle retourne l' **état \_ Success**.</span><span class="sxs-lookup"><span data-stu-id="30e0b-115">If the method succeeds, it returns **STATUS\_SUCCESS**.</span></span> <span data-ttu-id="30e0b-116">Sinon, elle retourne un code d’erreur **NTSTATUS** .</span><span class="sxs-lookup"><span data-stu-id="30e0b-116">Otherwise, it returns an **NTSTATUS** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="30e0b-117">Notes</span><span class="sxs-lookup"><span data-stu-id="30e0b-117">Remarks</span></span>

<span data-ttu-id="30e0b-118">Les applications doivent appeler [**GetTimingReport**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-gettimingreport) au lieu d’appeler cette fonction.</span><span class="sxs-lookup"><span data-stu-id="30e0b-118">Applications should call [**GetTimingReport**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-gettimingreport) instead of calling this function.</span></span>

<span data-ttu-id="30e0b-119">Cette fonction n’a pas de bibliothèque d’importation associée.</span><span class="sxs-lookup"><span data-stu-id="30e0b-119">This function has no associated import library.</span></span> <span data-ttu-id="30e0b-120">Pour appeler cette fonction, vous devez utiliser les fonctions [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) pour établir une liaison dynamique à Gdi32.dll.</span><span class="sxs-lookup"><span data-stu-id="30e0b-120">To call this function, you must use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Gdi32.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="30e0b-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="30e0b-121">Requirements</span></span>



| <span data-ttu-id="30e0b-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="30e0b-122">Requirement</span></span> | <span data-ttu-id="30e0b-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="30e0b-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="30e0b-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="30e0b-124">Minimum supported client</span></span><br/> | <span data-ttu-id="30e0b-125">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="30e0b-125">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="30e0b-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="30e0b-126">Minimum supported server</span></span><br/> | <span data-ttu-id="30e0b-127">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="30e0b-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="30e0b-128">DLL</span><span class="sxs-lookup"><span data-stu-id="30e0b-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="30e0b-129"><dt>Gdi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="30e0b-129"><dt>Gdi32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="30e0b-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="30e0b-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30e0b-131">Surveiller les fonctions de configuration</span><span class="sxs-lookup"><span data-stu-id="30e0b-131">Monitor Configuration Functions</span></span>](monitor-configuration-functions.md)
</dt> </dl>

 

