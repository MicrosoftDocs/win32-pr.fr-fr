---
description: Installe un nouvel appareil. L’utilisateur est invité à sélectionner l’appareil.
ms.assetid: 9bdee82c-1d0a-41ea-8b42-7ad96ac37663
title: InstallNewDevice fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InstallNewDevice
api_type:
- DllExport
api_location:
- NewDev.dll
ms.openlocfilehash: 76a458ae071c61b9f1030aad535c4d4c6a31078c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111174"
---
# <a name="installnewdevice-function"></a><span data-ttu-id="11f0f-104">InstallNewDevice fonction)</span><span class="sxs-lookup"><span data-stu-id="11f0f-104">InstallNewDevice function</span></span>

<span data-ttu-id="11f0f-105">Installe un nouvel appareil.</span><span class="sxs-lookup"><span data-stu-id="11f0f-105">Installs a new device.</span></span> <span data-ttu-id="11f0f-106">L’utilisateur est invité à sélectionner l’appareil.</span><span class="sxs-lookup"><span data-stu-id="11f0f-106">The user is prompted to select the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="11f0f-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="11f0f-107">Syntax</span></span>


```C++
BOOL WINAPI InstallNewDevice(
  _In_  HWND   hwndParent,
  _In_  LPGUID ClassGuid,
  _Out_ PDWORD pReboot
);
```



## <a name="parameters"></a><span data-ttu-id="11f0f-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="11f0f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="11f0f-109">*hwndParent* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="11f0f-109">*hwndParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11f0f-110">Handle de la fenêtre de niveau supérieur à utiliser pour toute interface utilisateur requise.</span><span class="sxs-lookup"><span data-stu-id="11f0f-110">A handle to the top-level window to be used for any required user interface.</span></span>

</dd> <dt>

<span data-ttu-id="11f0f-111">*ClassGuid* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="11f0f-111">*ClassGuid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11f0f-112">Pointeur vers un **GUID** de classe.</span><span class="sxs-lookup"><span data-stu-id="11f0f-112">A pointer to a class **GUID**.</span></span> <span data-ttu-id="11f0f-113">Ce paramètre est facultatif.</span><span class="sxs-lookup"><span data-stu-id="11f0f-113">This parameter is optional.</span></span> <span data-ttu-id="11f0f-114">Si ce paramètre a la **valeur null**, l’utilisateur démarre sur la page choix de détection.</span><span class="sxs-lookup"><span data-stu-id="11f0f-114">If this parameter is **NULL**, the user starts at the detection choice page.</span></span> <span data-ttu-id="11f0f-115">Si ce paramètre est **\_ null GUID** ou **GUID \_ DEVCLASS \_ Unknown**, l’utilisateur démarre sur la page de sélection de la classe.</span><span class="sxs-lookup"><span data-stu-id="11f0f-115">If this parameter is **GUID\_NULL** or **GUID\_DEVCLASS\_UNKNOWN**, the user starts at the class selection page.</span></span>

</dd> <dt>

<span data-ttu-id="11f0f-116">*prédémarrage* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="11f0f-116">*pReboot* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="11f0f-117">Pointeur vers une variable qui reçoit l’état de redémarrage.</span><span class="sxs-lookup"><span data-stu-id="11f0f-117">A pointer to a variable that receives the reboot status.</span></span> <span data-ttu-id="11f0f-118">Ce paramètre peut être **di \_ NEEDRESTART** ou **di \_ NEEDREBOOT**.</span><span class="sxs-lookup"><span data-stu-id="11f0f-118">This parameter can be **DI\_NEEDRESTART** or **DI\_NEEDREBOOT**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="11f0f-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="11f0f-119">Return value</span></span>

<span data-ttu-id="11f0f-120">Si la fonction réussit, la valeur de retour est différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="11f0f-120">If the function succeeds, the return value is nonzero.</span></span>

<span data-ttu-id="11f0f-121">Si la fonction échoue, la valeur de retour est égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="11f0f-121">If the function fails, the return value is zero.</span></span> <span data-ttu-id="11f0f-122">Pour obtenir des informations détaillées sur l’erreur, appelez [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="11f0f-122">To get extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="11f0f-123">Remarques</span><span class="sxs-lookup"><span data-stu-id="11f0f-123">Remarks</span></span>

<span data-ttu-id="11f0f-124">Cette fonction n’a pas de bibliothèque d’importation associée.</span><span class="sxs-lookup"><span data-stu-id="11f0f-124">This function has no associated import library.</span></span> <span data-ttu-id="11f0f-125">Vous devez utiliser les fonctions [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) pour établir une liaison dynamique à NewDev.dll.</span><span class="sxs-lookup"><span data-stu-id="11f0f-125">You must use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to NewDev.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="11f0f-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="11f0f-126">Requirements</span></span>



| <span data-ttu-id="11f0f-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="11f0f-127">Requirement</span></span> | <span data-ttu-id="11f0f-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="11f0f-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="11f0f-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="11f0f-129">Minimum supported client</span></span><br/> | <span data-ttu-id="11f0f-130">Windows XP</span><span class="sxs-lookup"><span data-stu-id="11f0f-130">Windows XP</span></span><br/>                                                                 |
| <span data-ttu-id="11f0f-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="11f0f-131">Minimum supported server</span></span><br/> | <span data-ttu-id="11f0f-132">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="11f0f-132">Windows Server 2003</span></span><br/>                                                        |
| <span data-ttu-id="11f0f-133">DLL</span><span class="sxs-lookup"><span data-stu-id="11f0f-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="11f0f-134"><dt>NewDev.dll</dt></span><span class="sxs-lookup"><span data-stu-id="11f0f-134"><dt>NewDev.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="11f0f-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="11f0f-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11f0f-136">Fonctions de gestion des appareils</span><span class="sxs-lookup"><span data-stu-id="11f0f-136">Device Management Functions</span></span>](device-management-functions.md)
</dt> </dl>

 

