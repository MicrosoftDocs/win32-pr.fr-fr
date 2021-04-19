---
title: GetPhysicalMonitors fonction)
description: Obtient les moniteurs physiques associés à un périphérique d’affichage.
ms.assetid: 8bbbad0a-2e45-439c-9312-f922a920c7fd
keywords:
- Configuration de l’analyse de fonction GetPhysicalMonitors
topic_type:
- apiref
api_name:
- GetPhysicalMonitors
api_location:
- gdi32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d95ccb801dbf06e096534754bd0adffbe36b5084
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106532047"
---
# <a name="getphysicalmonitors-function"></a><span data-ttu-id="6cd2d-104">GetPhysicalMonitors fonction)</span><span class="sxs-lookup"><span data-stu-id="6cd2d-104">GetPhysicalMonitors function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6cd2d-105">Cette fonction est utilisée par l’API de configuration de l’analyse pour accéder aux fonctionnalités dans le pilote d’affichage.</span><span class="sxs-lookup"><span data-stu-id="6cd2d-105">This function is used by the monitor configuration API to access functionality in the display driver.</span></span> <span data-ttu-id="6cd2d-106">Les applications ne doivent pas appeler cette fonction.</span><span class="sxs-lookup"><span data-stu-id="6cd2d-106">Applications should not call this function.</span></span>

 

<span data-ttu-id="6cd2d-107">Obtient les moniteurs physiques associés à un périphérique d’affichage.</span><span class="sxs-lookup"><span data-stu-id="6cd2d-107">Gets the physical monitors associated with a display device.</span></span>

## <a name="syntax"></a><span data-ttu-id="6cd2d-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6cd2d-108">Syntax</span></span>


```C++
NTSTATUS WINAPI GetPhysicalMonitors(
  _In_  UNICODE_STRING *pstrDeviceName,
  _In_  DWORD          dwPhysicalMonitorArraySize,
  _Out_ DWORD          *pdwNumPhysicalMonitorHandlesInArray,
  _Out_ HANDLE         *phPhysicalMonitorArray
);
```



## <a name="parameters"></a><span data-ttu-id="6cd2d-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6cd2d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6cd2d-110">*pstrDeviceName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6cd2d-110">*pstrDeviceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6cd2d-111">Pointeur vers une structure [**de \_ chaîne Unicode**](/windows/desktop/api/subauth/ns-subauth-unicode_string) qui contient le nom du périphérique d’affichage, tel que retourné par la fonction [**GetMonitorInfo**](/windows/desktop/api/winuser/nf-winuser-getmonitorinfoa) .</span><span class="sxs-lookup"><span data-stu-id="6cd2d-111">A pointer to a [**UNICODE\_STRING**](/windows/desktop/api/subauth/ns-subauth-unicode_string) structure that contains the name of the display device, as returned by the [**GetMonitorInfo**](/windows/desktop/api/winuser/nf-winuser-getmonitorinfoa) function.</span></span>

</dd> <dt>

<span data-ttu-id="6cd2d-112">*dwPhysicalMonitorArraySize* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6cd2d-112">*dwPhysicalMonitorArraySize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6cd2d-113">Nombre d’éléments dans le tableau *pdwNumPhysicalMonitorHandlesInArray* .</span><span class="sxs-lookup"><span data-stu-id="6cd2d-113">The number of elements in the *pdwNumPhysicalMonitorHandlesInArray* array.</span></span> <span data-ttu-id="6cd2d-114">Pour connaître la taille requise du tableau, appelez [**GetNumberOfPhysicalMonitors**](getnumberofphysicalmonitors.md).</span><span class="sxs-lookup"><span data-stu-id="6cd2d-114">To get the required size of the array, call [**GetNumberOfPhysicalMonitors**](getnumberofphysicalmonitors.md).</span></span>

</dd> <dt>

<span data-ttu-id="6cd2d-115">*pdwNumPhysicalMonitorHandlesInArray* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="6cd2d-115">*pdwNumPhysicalMonitorHandlesInArray* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6cd2d-116">Reçoit le nombre d’éléments que la fonction copie dans le tableau *phPhysicalMonitorArray* .</span><span class="sxs-lookup"><span data-stu-id="6cd2d-116">Receives the number of items that the function copies to the *phPhysicalMonitorArray* array.</span></span>

</dd> <dt>

<span data-ttu-id="6cd2d-117">*phPhysicalMonitorArray* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="6cd2d-117">*phPhysicalMonitorArray* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6cd2d-118">Tableau qui reçoit des handles vers les analyses physiques.</span><span class="sxs-lookup"><span data-stu-id="6cd2d-118">An array that receives handles to the physical monitors.</span></span> <span data-ttu-id="6cd2d-119">Chaque descripteur doit être libéré en appelant [**DestroyPhysicalMonitor**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-destroyphysicalmonitor).</span><span class="sxs-lookup"><span data-stu-id="6cd2d-119">Each handle must be released by calling [**DestroyPhysicalMonitor**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-destroyphysicalmonitor).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6cd2d-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6cd2d-120">Return value</span></span>

<span data-ttu-id="6cd2d-121">Si la méthode réussit, elle retourne l' **état \_ Success**.</span><span class="sxs-lookup"><span data-stu-id="6cd2d-121">If the method succeeds, it returns **STATUS\_SUCCESS**.</span></span> <span data-ttu-id="6cd2d-122">Sinon, elle retourne un code d’erreur **NTSTATUS** .</span><span class="sxs-lookup"><span data-stu-id="6cd2d-122">Otherwise, it returns an **NTSTATUS** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="6cd2d-123">Notes</span><span class="sxs-lookup"><span data-stu-id="6cd2d-123">Remarks</span></span>

<span data-ttu-id="6cd2d-124">Au lieu d’utiliser cette fonction, les applications doivent appeler l’une des fonctions suivantes :</span><span class="sxs-lookup"><span data-stu-id="6cd2d-124">Instead of using this function, applications should call one of the following functions:</span></span>

-   [<span data-ttu-id="6cd2d-125">**GetPhysicalMonitorsFromHMONITOR**</span><span class="sxs-lookup"><span data-stu-id="6cd2d-125">**GetPhysicalMonitorsFromHMONITOR**</span></span>](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromhmonitor)
-   [<span data-ttu-id="6cd2d-126">**GetPhysicalMonitorsFromIDirect3DDevice9**</span><span class="sxs-lookup"><span data-stu-id="6cd2d-126">**GetPhysicalMonitorsFromIDirect3DDevice9**</span></span>](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromidirect3ddevice9)

<span data-ttu-id="6cd2d-127">Cette fonction n’a pas de bibliothèque d’importation associée.</span><span class="sxs-lookup"><span data-stu-id="6cd2d-127">This function has no associated import library.</span></span> <span data-ttu-id="6cd2d-128">Pour appeler cette fonction, vous devez utiliser les fonctions [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) pour établir une liaison dynamique à Gdi32.dll.</span><span class="sxs-lookup"><span data-stu-id="6cd2d-128">To call this function, you must use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Gdi32.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="6cd2d-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6cd2d-129">Requirements</span></span>



| <span data-ttu-id="6cd2d-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6cd2d-130">Requirement</span></span> | <span data-ttu-id="6cd2d-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="6cd2d-131">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="6cd2d-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6cd2d-132">Minimum supported client</span></span><br/> | <span data-ttu-id="6cd2d-133">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6cd2d-133">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="6cd2d-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6cd2d-134">Minimum supported server</span></span><br/> | <span data-ttu-id="6cd2d-135">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6cd2d-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="6cd2d-136">DLL</span><span class="sxs-lookup"><span data-stu-id="6cd2d-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6cd2d-137"><dt>Gdi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6cd2d-137"><dt>Gdi32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6cd2d-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6cd2d-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6cd2d-139">Surveiller les fonctions de configuration</span><span class="sxs-lookup"><span data-stu-id="6cd2d-139">Monitor Configuration Functions</span></span>](monitor-configuration-functions.md)
</dt> </dl>

 

