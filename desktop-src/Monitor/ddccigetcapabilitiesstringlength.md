---
title: DDCCIGetCapabilitiesStringLength fonction)
description: Obtient la longueur d’une chaîne de fonctionnalités pour une analyse.
ms.assetid: 8a26d17b-1535-49c7-8cfb-48feb283a3c4
keywords:
- Configuration de l’analyse de fonction DDCCIGetCapabilitiesStringLength
topic_type:
- apiref
api_name:
- DDCCIGetCapabilitiesStringLength
api_location:
- gdi32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28d82e2f0667d542c8fa4c9255fde765e4cea81d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106513768"
---
# <a name="ddccigetcapabilitiesstringlength-function"></a><span data-ttu-id="f6ab7-104">DDCCIGetCapabilitiesStringLength fonction)</span><span class="sxs-lookup"><span data-stu-id="f6ab7-104">DDCCIGetCapabilitiesStringLength function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f6ab7-105">Cette fonction est utilisée par l’API de configuration de l’analyse pour accéder aux fonctionnalités dans le pilote d’affichage.</span><span class="sxs-lookup"><span data-stu-id="f6ab7-105">This function is used by the monitor configuration API to access functionality in the display driver.</span></span> <span data-ttu-id="f6ab7-106">Les applications ne doivent pas appeler cette fonction.</span><span class="sxs-lookup"><span data-stu-id="f6ab7-106">Applications should not call this function.</span></span>

 

<span data-ttu-id="f6ab7-107">Obtient la longueur d’une chaîne de fonctionnalités pour une analyse.</span><span class="sxs-lookup"><span data-stu-id="f6ab7-107">Gets the length of a capabilities string for a monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6ab7-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f6ab7-108">Syntax</span></span>


```C++
NTSTATUS WINAPI DDCCIGetCapabilitiesStringLength(
  _In_  HANDLE hMonitor,
  _Out_ DWORD  *pdwLength
);
```



## <a name="parameters"></a><span data-ttu-id="f6ab7-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f6ab7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f6ab7-110">*hMonitor* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f6ab7-110">*hMonitor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f6ab7-111">Handle d’une analyse physique.</span><span class="sxs-lookup"><span data-stu-id="f6ab7-111">A handle to a physical monitor.</span></span>

</dd> <dt>

<span data-ttu-id="f6ab7-112">*pdwLength* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="f6ab7-112">*pdwLength* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f6ab7-113">Reçoit la longueur de la chaîne de fonctionnalités, en caractères, y compris le caractère null de fin.</span><span class="sxs-lookup"><span data-stu-id="f6ab7-113">Receives the length of the capabilities string, in characters, including the terminating null character.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f6ab7-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f6ab7-114">Return value</span></span>

<span data-ttu-id="f6ab7-115">Si la méthode réussit, elle retourne l' **état \_ Success**.</span><span class="sxs-lookup"><span data-stu-id="f6ab7-115">If the method succeeds, it returns **STATUS\_SUCCESS**.</span></span> <span data-ttu-id="f6ab7-116">Sinon, elle retourne un code d’erreur **NTSTATUS** .</span><span class="sxs-lookup"><span data-stu-id="f6ab7-116">Otherwise, it returns an **NTSTATUS** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="f6ab7-117">Notes</span><span class="sxs-lookup"><span data-stu-id="f6ab7-117">Remarks</span></span>

<span data-ttu-id="f6ab7-118">Les applications doivent appeler [**GetCapabilitiesStringLength**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-getcapabilitiesstringlength) au lieu d’appeler cette fonction.</span><span class="sxs-lookup"><span data-stu-id="f6ab7-118">Applications should call [**GetCapabilitiesStringLength**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-getcapabilitiesstringlength) instead of calling this function.</span></span>

<span data-ttu-id="f6ab7-119">Cette fonction n’a pas de bibliothèque d’importation associée.</span><span class="sxs-lookup"><span data-stu-id="f6ab7-119">This function has no associated import library.</span></span> <span data-ttu-id="f6ab7-120">Pour appeler cette fonction, vous devez utiliser les fonctions [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) pour établir une liaison dynamique à Gdi32.dll.</span><span class="sxs-lookup"><span data-stu-id="f6ab7-120">To call this function, you must use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Gdi32.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="f6ab7-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f6ab7-121">Requirements</span></span>



| <span data-ttu-id="f6ab7-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f6ab7-122">Requirement</span></span> | <span data-ttu-id="f6ab7-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="f6ab7-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="f6ab7-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f6ab7-124">Minimum supported client</span></span><br/> | <span data-ttu-id="f6ab7-125">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f6ab7-125">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="f6ab7-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f6ab7-126">Minimum supported server</span></span><br/> | <span data-ttu-id="f6ab7-127">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f6ab7-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="f6ab7-128">DLL</span><span class="sxs-lookup"><span data-stu-id="f6ab7-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f6ab7-129"><dt>Gdi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f6ab7-129"><dt>Gdi32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f6ab7-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f6ab7-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6ab7-131">Surveiller les fonctions de configuration</span><span class="sxs-lookup"><span data-stu-id="f6ab7-131">Monitor Configuration Functions</span></span>](monitor-configuration-functions.md)
</dt> </dl>

 

