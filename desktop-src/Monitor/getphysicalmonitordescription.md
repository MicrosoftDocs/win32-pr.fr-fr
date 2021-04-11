---
title: GetPhysicalMonitorDescription fonction)
description: Obtient une description d’une analyse physique.
ms.assetid: 81789eaf-7831-4833-87e1-7f318f831c96
keywords:
- Configuration de l’analyse de fonction GetPhysicalMonitorDescription
topic_type:
- apiref
api_name:
- GetPhysicalMonitorDescription
api_location:
- gdi32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 259ced1185e229fccd426adfbf94fa47af22b170
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103600"
---
# <a name="getphysicalmonitordescription-function"></a><span data-ttu-id="57f0f-104">GetPhysicalMonitorDescription fonction)</span><span class="sxs-lookup"><span data-stu-id="57f0f-104">GetPhysicalMonitorDescription function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="57f0f-105">Cette fonction est utilisée par l’API de configuration de l’analyse pour accéder aux fonctionnalités dans le pilote d’affichage.</span><span class="sxs-lookup"><span data-stu-id="57f0f-105">This function is used by the monitor configuration API to access functionality in the display driver.</span></span> <span data-ttu-id="57f0f-106">Les applications ne doivent pas appeler cette fonction.</span><span class="sxs-lookup"><span data-stu-id="57f0f-106">Applications should not call this function.</span></span>

 

<span data-ttu-id="57f0f-107">Obtient une description d’une analyse physique.</span><span class="sxs-lookup"><span data-stu-id="57f0f-107">Gets a description of a physical monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="57f0f-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="57f0f-108">Syntax</span></span>


```C++
NTSTATUS WINAPI GetPhysicalMonitorDescription(
  _In_  HANDLE hMonitor,
  _In_  DWORD  dwPhysicalMonitorDescriptionSizeInChars,
  _Out_ LPWSTR szPhysicalMonitorDescription
);
```



## <a name="parameters"></a><span data-ttu-id="57f0f-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="57f0f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="57f0f-110">*hMonitor* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="57f0f-110">*hMonitor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="57f0f-111">Handle d’une analyse physique.</span><span class="sxs-lookup"><span data-stu-id="57f0f-111">A handle to a physical monitor.</span></span>

</dd> <dt>

<span data-ttu-id="57f0f-112">*dwPhysicalMonitorDescriptionSizeInChars* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="57f0f-112">*dwPhysicalMonitorDescriptionSizeInChars* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="57f0f-113">Nombre de caractères dans le tableau *szPhysicalMonitorDescription* .</span><span class="sxs-lookup"><span data-stu-id="57f0f-113">The number of characters in the *szPhysicalMonitorDescription* array.</span></span>

</dd> <dt>

<span data-ttu-id="57f0f-114">*szPhysicalMonitorDescription* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="57f0f-114">*szPhysicalMonitorDescription* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="57f0f-115">Pointeur vers un tableau qui reçoit la description.</span><span class="sxs-lookup"><span data-stu-id="57f0f-115">A pointer to an array that receives the description.</span></span> <span data-ttu-id="57f0f-116">Le nombre d’éléments dans le tableau doit être au moins de la taille de la description de l' **\_ analyse \_ \_ physique**.</span><span class="sxs-lookup"><span data-stu-id="57f0f-116">The number of elements in the array should be at least **PHYSICAL\_MONITOR\_DESCRIPTION\_SIZE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="57f0f-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="57f0f-117">Return value</span></span>

<span data-ttu-id="57f0f-118">Si la méthode réussit, elle retourne l' **état \_ Success**.</span><span class="sxs-lookup"><span data-stu-id="57f0f-118">If the method succeeds, it returns **STATUS\_SUCCESS**.</span></span> <span data-ttu-id="57f0f-119">Sinon, elle retourne un code d’erreur **NTSTATUS** .</span><span class="sxs-lookup"><span data-stu-id="57f0f-119">Otherwise, it returns an **NTSTATUS** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="57f0f-120">Notes</span><span class="sxs-lookup"><span data-stu-id="57f0f-120">Remarks</span></span>

<span data-ttu-id="57f0f-121">Au lieu d’utiliser cette fonction, les applications doivent appeler l’une des fonctions suivantes :</span><span class="sxs-lookup"><span data-stu-id="57f0f-121">Instead of using this function, applications should call one of the following functions:</span></span>

-   [<span data-ttu-id="57f0f-122">**GetPhysicalMonitorsFromHMONITOR**</span><span class="sxs-lookup"><span data-stu-id="57f0f-122">**GetPhysicalMonitorsFromHMONITOR**</span></span>](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromhmonitor)
-   [<span data-ttu-id="57f0f-123">**GetPhysicalMonitorsFromIDirect3DDevice9**</span><span class="sxs-lookup"><span data-stu-id="57f0f-123">**GetPhysicalMonitorsFromIDirect3DDevice9**</span></span>](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromidirect3ddevice9)

<span data-ttu-id="57f0f-124">Cette fonction n’a pas de bibliothèque d’importation associée.</span><span class="sxs-lookup"><span data-stu-id="57f0f-124">This function has no associated import library.</span></span> <span data-ttu-id="57f0f-125">Pour appeler cette fonction, vous devez utiliser les fonctions [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) pour établir une liaison dynamique à Gdi32.dll.</span><span class="sxs-lookup"><span data-stu-id="57f0f-125">To call this function, you must use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Gdi32.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="57f0f-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="57f0f-126">Requirements</span></span>



| <span data-ttu-id="57f0f-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="57f0f-127">Requirement</span></span> | <span data-ttu-id="57f0f-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="57f0f-128">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="57f0f-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="57f0f-129">Minimum supported client</span></span><br/> | <span data-ttu-id="57f0f-130">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="57f0f-130">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="57f0f-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="57f0f-131">Minimum supported server</span></span><br/> | <span data-ttu-id="57f0f-132">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="57f0f-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="57f0f-133">DLL</span><span class="sxs-lookup"><span data-stu-id="57f0f-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="57f0f-134"><dt>Gdi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="57f0f-134"><dt>Gdi32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="57f0f-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="57f0f-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57f0f-136">Surveiller les fonctions de configuration</span><span class="sxs-lookup"><span data-stu-id="57f0f-136">Monitor Configuration Functions</span></span>](monitor-configuration-functions.md)
</dt> </dl>

 

