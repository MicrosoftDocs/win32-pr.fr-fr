---
title: GetNumberOfPhysicalMonitors fonction)
description: Obtient le nombre d’analyses phyical associées à un périphérique d’affichage.
ms.assetid: 498404e7-867d-4971-bea1-16e9f8fd9838
keywords:
- Configuration de l’analyse de fonction GetNumberOfPhysicalMonitors
topic_type:
- apiref
api_name:
- GetNumberOfPhysicalMonitors
api_location:
- gdi32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09bec6abf296d807f80ab77cdc7ad8b4062fea9b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843525"
---
# <a name="getnumberofphysicalmonitors-function"></a><span data-ttu-id="27963-104">GetNumberOfPhysicalMonitors fonction)</span><span class="sxs-lookup"><span data-stu-id="27963-104">GetNumberOfPhysicalMonitors function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="27963-105">Cette fonction est utilisée par l’API de configuration de l’analyse pour accéder aux fonctionnalités dans le pilote d’affichage.</span><span class="sxs-lookup"><span data-stu-id="27963-105">This function is used by the monitor configuration API to access functionality in the display driver.</span></span> <span data-ttu-id="27963-106">Les applications ne doivent pas appeler cette fonction.</span><span class="sxs-lookup"><span data-stu-id="27963-106">Applications should not call this function.</span></span>

 

<span data-ttu-id="27963-107">Obtient le nombre d’analyses phyical associées à un périphérique d’affichage.</span><span class="sxs-lookup"><span data-stu-id="27963-107">Gets the number of phyical monitors associated with a display device.</span></span>

## <a name="syntax"></a><span data-ttu-id="27963-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="27963-108">Syntax</span></span>


```C++
NTSTATUS WINAPI GetNumberOfPhysicalMonitors(
  _In_  UNICODE_STRING *pstrDeviceName,
  _Out_ LPDWORD        pdwNumberOfPhysicalMonitors
);
```



## <a name="parameters"></a><span data-ttu-id="27963-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="27963-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="27963-110">*pstrDeviceName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="27963-110">*pstrDeviceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="27963-111">Pointeur vers une structure [**de \_ chaîne Unicode**](/windows/desktop/api/subauth/ns-subauth-unicode_string) qui contient le nom du périphérique d’affichage, tel que retourné par la fonction [**GetMonitorInfo**](/windows/desktop/api/winuser/nf-winuser-getmonitorinfoa) .</span><span class="sxs-lookup"><span data-stu-id="27963-111">A pointer to a [**UNICODE\_STRING**](/windows/desktop/api/subauth/ns-subauth-unicode_string) structure that contains the name of the display device, as returned by the [**GetMonitorInfo**](/windows/desktop/api/winuser/nf-winuser-getmonitorinfoa) function.</span></span>

</dd> <dt>

<span data-ttu-id="27963-112">*pdwNumberOfPhysicalMonitors* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="27963-112">*pdwNumberOfPhysicalMonitors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="27963-113">Reçoit le nombre de moniteurs physiques.</span><span class="sxs-lookup"><span data-stu-id="27963-113">Receives the number of physical monitors.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="27963-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="27963-114">Return value</span></span>

<span data-ttu-id="27963-115">Si la méthode réussit, elle retourne l' **état \_ Success**.</span><span class="sxs-lookup"><span data-stu-id="27963-115">If the method succeeds, it returns **STATUS\_SUCCESS**.</span></span> <span data-ttu-id="27963-116">Sinon, elle retourne un code d’erreur **NTSTATUS** .</span><span class="sxs-lookup"><span data-stu-id="27963-116">Otherwise, it returns an **NTSTATUS** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="27963-117">Notes</span><span class="sxs-lookup"><span data-stu-id="27963-117">Remarks</span></span>

<span data-ttu-id="27963-118">Au lieu d’utiliser cette fonction, les applications doivent appeler l’une des fonctions suivantes :</span><span class="sxs-lookup"><span data-stu-id="27963-118">Instead of using this function, applications should call one of the following functions:</span></span>

-   [<span data-ttu-id="27963-119">**GetNumberOfPhysicalMonitorsFromHMONITOR**</span><span class="sxs-lookup"><span data-stu-id="27963-119">**GetNumberOfPhysicalMonitorsFromHMONITOR**</span></span>](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getnumberofphysicalmonitorsfromhmonitor)
-   [<span data-ttu-id="27963-120">**GetNumberOfPhysicalMonitorsFromIDirect3DDevice9**</span><span class="sxs-lookup"><span data-stu-id="27963-120">**GetNumberOfPhysicalMonitorsFromIDirect3DDevice9**</span></span>](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getnumberofphysicalmonitorsfromidirect3ddevice9)

<span data-ttu-id="27963-121">Cette fonction n’a pas de bibliothèque d’importation associée.</span><span class="sxs-lookup"><span data-stu-id="27963-121">This function has no associated import library.</span></span> <span data-ttu-id="27963-122">Pour appeler cette fonction, vous devez utiliser les fonctions [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) pour établir une liaison dynamique à Gdi32.dll.</span><span class="sxs-lookup"><span data-stu-id="27963-122">To call this function, you must use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Gdi32.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="27963-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="27963-123">Requirements</span></span>



| <span data-ttu-id="27963-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="27963-124">Requirement</span></span> | <span data-ttu-id="27963-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="27963-125">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="27963-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="27963-126">Minimum supported client</span></span><br/> | <span data-ttu-id="27963-127">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="27963-127">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="27963-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="27963-128">Minimum supported server</span></span><br/> | <span data-ttu-id="27963-129">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="27963-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="27963-130">DLL</span><span class="sxs-lookup"><span data-stu-id="27963-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="27963-131"><dt>Gdi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="27963-131"><dt>Gdi32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="27963-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="27963-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27963-133">Surveiller les fonctions de configuration</span><span class="sxs-lookup"><span data-stu-id="27963-133">Monitor Configuration Functions</span></span>](monitor-configuration-functions.md)
</dt> </dl>

 

