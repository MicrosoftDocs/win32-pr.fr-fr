---
description: Annule la notification de chargement de la DLL précédemment inscrite en appelant la fonction LdrRegisterDllNotification.
ms.assetid: 18c3a027-e3cb-4083-afdc-00f416a70d8c
title: LdrUnregisterDllNotification fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LdrUnregisterDllNotification
api_type:
- DllExport
api_location:
- ntdll.dll
ms.openlocfilehash: 1fee03b4a06d274b495070eb40833b270a795158
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104392923"
---
# <a name="ldrunregisterdllnotification-function"></a><span data-ttu-id="3aa8c-103">LdrUnregisterDllNotification fonction)</span><span class="sxs-lookup"><span data-stu-id="3aa8c-103">LdrUnregisterDllNotification function</span></span>

<span data-ttu-id="3aa8c-104">\[Cette fonction peut être modifiée ou supprimée de Windows sans préavis.\]</span><span class="sxs-lookup"><span data-stu-id="3aa8c-104">\[This function may be changed or removed from Windows without further notice.\]</span></span>

<span data-ttu-id="3aa8c-105">Annule la notification de chargement de la DLL précédemment inscrite en appelant la fonction [**LdrRegisterDllNotification**](ldrregisterdllnotification.md) .</span><span class="sxs-lookup"><span data-stu-id="3aa8c-105">Cancels DLL load notification previously registered by calling the [**LdrRegisterDllNotification**](ldrregisterdllnotification.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="3aa8c-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3aa8c-106">Syntax</span></span>


```C++
NTSTATUS NTAPI LdrUnregisterDllNotification(
  _In_ PVOID Cookie
);
```



## <a name="parameters"></a><span data-ttu-id="3aa8c-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3aa8c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3aa8c-108">*Cookie* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3aa8c-108">*Cookie* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3aa8c-109">Pointeur vers l’identificateur de rappel reçu de l’appel de [**LdrRegisterDllNotification**](ldrregisterdllnotification.md) qui s’est inscrit pour la notification.</span><span class="sxs-lookup"><span data-stu-id="3aa8c-109">A pointer to the callback identifier received from the [**LdrRegisterDllNotification**](ldrregisterdllnotification.md) call that registered for notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3aa8c-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3aa8c-110">Return value</span></span>

<span data-ttu-id="3aa8c-111">Retourne un code **NTSTATUS** ou d’erreur.</span><span class="sxs-lookup"><span data-stu-id="3aa8c-111">Returns an **NTSTATUS** or error code.</span></span>

<span data-ttu-id="3aa8c-112">Si la fonction réussit, elle retourne l' **état \_ Success**.</span><span class="sxs-lookup"><span data-stu-id="3aa8c-112">If the function succeeds, it returns **STATUS\_SUCCESS**.</span></span>

<span data-ttu-id="3aa8c-113">Si la fonction de rappel est introuvable, la fonction retourne la **dll d’état \_ \_ \_ introuvable**.</span><span class="sxs-lookup"><span data-stu-id="3aa8c-113">If the callback function is not found, the function returns **STATUS\_DLL\_NOT\_FOUND**.</span></span>

<span data-ttu-id="3aa8c-114">Les formulaires et la signification des codes d’erreur de **NTSTATUS** sont répertoriés dans le fichier d’en-tête Ntstatus. h disponible dans le kit WDK et sont décrits dans la documentation WDK.</span><span class="sxs-lookup"><span data-stu-id="3aa8c-114">The forms and significance of **NTSTATUS** error codes are listed in the Ntstatus.h header file available in the WDK, and are described in the WDK documentation.</span></span>

## <a name="remarks"></a><span data-ttu-id="3aa8c-115">Notes</span><span class="sxs-lookup"><span data-stu-id="3aa8c-115">Remarks</span></span>

<span data-ttu-id="3aa8c-116">Cette fonction n’a aucun fichier d’en-tête associé.</span><span class="sxs-lookup"><span data-stu-id="3aa8c-116">This function has no associated header file.</span></span> <span data-ttu-id="3aa8c-117">La bibliothèque d’importation associée, ntdll. lib, est disponible dans le kit WDK.</span><span class="sxs-lookup"><span data-stu-id="3aa8c-117">The associated import library, Ntdll.lib, is available in the WDK.</span></span> <span data-ttu-id="3aa8c-118">Vous pouvez également utiliser les fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) pour établir une liaison dynamique à Ntdll.dll.</span><span class="sxs-lookup"><span data-stu-id="3aa8c-118">You can also use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Ntdll.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="3aa8c-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3aa8c-119">Requirements</span></span>



| <span data-ttu-id="3aa8c-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3aa8c-120">Requirement</span></span> | <span data-ttu-id="3aa8c-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="3aa8c-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="3aa8c-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3aa8c-122">Minimum supported client</span></span><br/> | <span data-ttu-id="3aa8c-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3aa8c-123">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="3aa8c-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3aa8c-124">Minimum supported server</span></span><br/> | <span data-ttu-id="3aa8c-125">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3aa8c-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="3aa8c-126">DLL</span><span class="sxs-lookup"><span data-stu-id="3aa8c-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3aa8c-127"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3aa8c-127"><dt>Ntdll.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3aa8c-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3aa8c-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3aa8c-129">**LdrRegisterDllNotification**</span><span class="sxs-lookup"><span data-stu-id="3aa8c-129">**LdrRegisterDllNotification**</span></span>](ldrregisterdllnotification.md)
</dt> </dl>

 

 
