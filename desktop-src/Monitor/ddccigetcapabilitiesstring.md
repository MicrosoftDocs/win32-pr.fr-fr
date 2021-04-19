---
title: DDCCIGetCapabilitiesString fonction)
description: Obtient une chaîne qui décrit les fonctionnalités d’une analyse.
ms.assetid: 54041126-b710-4448-a9f0-9b644d6b8186
keywords:
- Configuration de l’analyse de fonction DDCCIGetCapabilitiesString
topic_type:
- apiref
api_name:
- DDCCIGetCapabilitiesString
api_location:
- gdi32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9a49a6d7672ee505b4095afd3c6603c719679f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511148"
---
# <a name="ddccigetcapabilitiesstring-function"></a><span data-ttu-id="cff28-104">DDCCIGetCapabilitiesString fonction)</span><span class="sxs-lookup"><span data-stu-id="cff28-104">DDCCIGetCapabilitiesString function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="cff28-105">Cette fonction est utilisée par l’API de configuration de l’analyse pour accéder aux fonctionnalités dans le pilote d’affichage.</span><span class="sxs-lookup"><span data-stu-id="cff28-105">This function is used by the monitor configuration API to access functionality in the display driver.</span></span> <span data-ttu-id="cff28-106">Les applications ne doivent pas appeler cette fonction.</span><span class="sxs-lookup"><span data-stu-id="cff28-106">Applications should not call this function.</span></span>

 

<span data-ttu-id="cff28-107">Obtient une chaîne qui décrit les fonctionnalités d’une analyse.</span><span class="sxs-lookup"><span data-stu-id="cff28-107">Gets a string that describes the capabilities of a monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="cff28-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cff28-108">Syntax</span></span>


```C++
NTSTATUS WINAPI DDCCIGetCapabilitiesString(
  _In_  HANDLE hMonitor,
  _Out_ LPSTR  pszString,
  _In_  DWORD  dwLength
);
```



## <a name="parameters"></a><span data-ttu-id="cff28-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cff28-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cff28-110">*hMonitor* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cff28-110">*hMonitor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cff28-111">Handle d’une analyse physique.</span><span class="sxs-lookup"><span data-stu-id="cff28-111">A handle to a physical monitor.</span></span>

</dd> <dt>

<span data-ttu-id="cff28-112">*pszString* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="cff28-112">*pszString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cff28-113">Pointeur vers une mémoire tampon qui reçoit la chaîne de fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="cff28-113">A pointer to a buffer that receives the capabilities string.</span></span> <span data-ttu-id="cff28-114">Pour connaître la longueur de la chaîne de fonctionnalités, appelez [**DDCCIGetCapabilitiesStringLength**](ddccigetcapabilitiesstringlength.md).</span><span class="sxs-lookup"><span data-stu-id="cff28-114">To get the length of the capabilities string, call [**DDCCIGetCapabilitiesStringLength**](ddccigetcapabilitiesstringlength.md).</span></span>

</dd> <dt>

<span data-ttu-id="cff28-115">*dwLength* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cff28-115">*dwLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cff28-116">Taille de la mémoire tampon *pszString* , en caractères, y compris le caractère null de fin.</span><span class="sxs-lookup"><span data-stu-id="cff28-116">The size of the *pszString* buffer, in characters, including the terminating null character.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cff28-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="cff28-117">Return value</span></span>

<span data-ttu-id="cff28-118">Si la méthode réussit, elle retourne l' **état \_ Success**.</span><span class="sxs-lookup"><span data-stu-id="cff28-118">If the method succeeds, it returns **STATUS\_SUCCESS**.</span></span> <span data-ttu-id="cff28-119">Sinon, elle retourne un code d’erreur **NTSTATUS** .</span><span class="sxs-lookup"><span data-stu-id="cff28-119">Otherwise, it returns an **NTSTATUS** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="cff28-120">Notes</span><span class="sxs-lookup"><span data-stu-id="cff28-120">Remarks</span></span>

<span data-ttu-id="cff28-121">Les applications doivent appeler [**CapabilitiesRequestAndCapabilitiesReply**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-capabilitiesrequestandcapabilitiesreply) au lieu d’appeler cette fonction.</span><span class="sxs-lookup"><span data-stu-id="cff28-121">Applications should call [**CapabilitiesRequestAndCapabilitiesReply**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-capabilitiesrequestandcapabilitiesreply) instead of calling this function.</span></span>

<span data-ttu-id="cff28-122">Cette fonction n’a pas de bibliothèque d’importation associée.</span><span class="sxs-lookup"><span data-stu-id="cff28-122">This function has no associated import library.</span></span> <span data-ttu-id="cff28-123">Pour appeler cette fonction, vous devez utiliser les fonctions [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) pour établir une liaison dynamique à Gdi32.dll.</span><span class="sxs-lookup"><span data-stu-id="cff28-123">To call this function, you must use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Gdi32.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="cff28-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cff28-124">Requirements</span></span>



| <span data-ttu-id="cff28-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cff28-125">Requirement</span></span> | <span data-ttu-id="cff28-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="cff28-126">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="cff28-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cff28-127">Minimum supported client</span></span><br/> | <span data-ttu-id="cff28-128">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cff28-128">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="cff28-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cff28-129">Minimum supported server</span></span><br/> | <span data-ttu-id="cff28-130">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cff28-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="cff28-131">DLL</span><span class="sxs-lookup"><span data-stu-id="cff28-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cff28-132"><dt>Gdi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cff28-132"><dt>Gdi32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cff28-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cff28-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cff28-134">Surveiller les fonctions de configuration</span><span class="sxs-lookup"><span data-stu-id="cff28-134">Monitor Configuration Functions</span></span>](monitor-configuration-functions.md)
</dt> </dl>

 

