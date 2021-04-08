---
title: DestroyPhysicalMonitorInternal fonction)
description: Ferme un handle vers une analyse physique.
ms.assetid: 86705f1b-6445-444c-8e04-66a435927af3
keywords:
- Configuration de l’analyse de fonction DestroyPhysicalMonitorInternal
topic_type:
- apiref
api_name:
- DestroyPhysicalMonitorInternal
api_location:
- gdi32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b8ea52645e97bc5bec49fba053f9dbab5306bcb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843526"
---
# <a name="destroyphysicalmonitorinternal-function"></a><span data-ttu-id="7ebbc-104">DestroyPhysicalMonitorInternal fonction)</span><span class="sxs-lookup"><span data-stu-id="7ebbc-104">DestroyPhysicalMonitorInternal function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7ebbc-105">Cette fonction est utilisée par l’API de configuration de l’analyse pour accéder aux fonctionnalités dans le pilote d’affichage.</span><span class="sxs-lookup"><span data-stu-id="7ebbc-105">This function is used by the monitor configuration API to access functionality in the display driver.</span></span> <span data-ttu-id="7ebbc-106">Les applications ne doivent pas appeler cette fonction.</span><span class="sxs-lookup"><span data-stu-id="7ebbc-106">Applications should not call this function.</span></span>

 

<span data-ttu-id="7ebbc-107">Ferme un handle vers une analyse physique.</span><span class="sxs-lookup"><span data-stu-id="7ebbc-107">Closes a handle to a physical monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ebbc-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7ebbc-108">Syntax</span></span>


```C++
NTSTATUS WINAPI DestroyPhysicalMonitorInternal(
  _In_ HANDLE hMonitor
);
```



## <a name="parameters"></a><span data-ttu-id="7ebbc-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7ebbc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7ebbc-110">*hMonitor* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7ebbc-110">*hMonitor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ebbc-111">Handle d’une analyse physique.</span><span class="sxs-lookup"><span data-stu-id="7ebbc-111">A handle to a physical monitor.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7ebbc-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7ebbc-112">Return value</span></span>

<span data-ttu-id="7ebbc-113">Si la méthode réussit, elle retourne l' **état \_ Success**.</span><span class="sxs-lookup"><span data-stu-id="7ebbc-113">If the method succeeds, it returns **STATUS\_SUCCESS**.</span></span> <span data-ttu-id="7ebbc-114">Sinon, elle retourne un code d’erreur **NTSTATUS** .</span><span class="sxs-lookup"><span data-stu-id="7ebbc-114">Otherwise, it returns an **NTSTATUS** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="7ebbc-115">Notes</span><span class="sxs-lookup"><span data-stu-id="7ebbc-115">Remarks</span></span>

<span data-ttu-id="7ebbc-116">Les applications doivent appeler [**DestroyPhysicalMonitor**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-destroyphysicalmonitor) au lieu d’appeler cette fonction.</span><span class="sxs-lookup"><span data-stu-id="7ebbc-116">Applications should call [**DestroyPhysicalMonitor**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-destroyphysicalmonitor) instead of calling this function.</span></span>

<span data-ttu-id="7ebbc-117">Cette fonction n’a pas de bibliothèque d’importation associée.</span><span class="sxs-lookup"><span data-stu-id="7ebbc-117">This function has no associated import library.</span></span> <span data-ttu-id="7ebbc-118">Pour appeler cette fonction, vous devez utiliser les fonctions [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) pour établir une liaison dynamique à Gdi32.dll.</span><span class="sxs-lookup"><span data-stu-id="7ebbc-118">To call this function, you must use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Gdi32.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="7ebbc-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7ebbc-119">Requirements</span></span>



| <span data-ttu-id="7ebbc-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7ebbc-120">Requirement</span></span> | <span data-ttu-id="7ebbc-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="7ebbc-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="7ebbc-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7ebbc-122">Minimum supported client</span></span><br/> | <span data-ttu-id="7ebbc-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7ebbc-123">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="7ebbc-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7ebbc-124">Minimum supported server</span></span><br/> | <span data-ttu-id="7ebbc-125">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7ebbc-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="7ebbc-126">DLL</span><span class="sxs-lookup"><span data-stu-id="7ebbc-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7ebbc-127"><dt>Gdi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7ebbc-127"><dt>Gdi32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7ebbc-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7ebbc-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ebbc-129">Surveiller les fonctions de configuration</span><span class="sxs-lookup"><span data-stu-id="7ebbc-129">Monitor Configuration Functions</span></span>](monitor-configuration-functions.md)
</dt> </dl>

 

