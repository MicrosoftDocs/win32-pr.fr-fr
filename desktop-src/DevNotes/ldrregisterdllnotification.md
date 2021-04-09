---
description: Enregistre une notification lorsqu’une DLL est chargée pour la première fois. Cette notification se produit avant que la liaison dynamique ait lieu.
ms.assetid: c2757aa0-76fa-427a-a4f6-cb26e7f7d0d1
title: LdrRegisterDllNotification fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LdrRegisterDllNotification
api_type:
- DllExport
api_location:
- ntdll.dll
ms.openlocfilehash: 82ec05a24f4cccc89cece666b18cb63412a78259
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104033597"
---
# <a name="ldrregisterdllnotification-function"></a><span data-ttu-id="08f86-104">LdrRegisterDllNotification fonction)</span><span class="sxs-lookup"><span data-stu-id="08f86-104">LdrRegisterDllNotification function</span></span>

<span data-ttu-id="08f86-105">\[Cette fonction peut être modifiée ou supprimée de Windows sans préavis.\]</span><span class="sxs-lookup"><span data-stu-id="08f86-105">\[This function may be changed or removed from Windows without further notice.\]</span></span>

<span data-ttu-id="08f86-106">Enregistre une notification lorsqu’une DLL est chargée pour la première fois.</span><span class="sxs-lookup"><span data-stu-id="08f86-106">Registers for notification when a DLL is first loaded.</span></span> <span data-ttu-id="08f86-107">Cette notification se produit avant que la liaison dynamique ait lieu.</span><span class="sxs-lookup"><span data-stu-id="08f86-107">This notification occurs before dynamic linking takes place.</span></span>

## <a name="syntax"></a><span data-ttu-id="08f86-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="08f86-108">Syntax</span></span>


```C++
NTSTATUS NTAPI LdrRegisterDllNotification(
  _In_     ULONG                          Flags,
  _In_     PLDR_DLL_NOTIFICATION_FUNCTION NotificationFunction,
  _In_opt_ PVOID                          Context,
  _Out_    PVOID                          *Cookie
);
```



## <a name="parameters"></a><span data-ttu-id="08f86-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="08f86-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="08f86-110">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="08f86-110">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08f86-111">Ce paramètre doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="08f86-111">This parameter must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="08f86-112">*NotificationFunction* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="08f86-112">*NotificationFunction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08f86-113">Pointeur vers une fonction de rappel de notification [*LdrDllNotification*](ldrdllnotification.md) à appeler lorsque la dll est chargée.</span><span class="sxs-lookup"><span data-stu-id="08f86-113">A pointer to an [*LdrDllNotification*](ldrdllnotification.md) notification callback function to call when the DLL is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="08f86-114">*Contexte* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="08f86-114">*Context* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="08f86-115">Pointeur vers les données de contexte pour la fonction de rappel.</span><span class="sxs-lookup"><span data-stu-id="08f86-115">A pointer to context data for the callback function.</span></span>

</dd> <dt>

<span data-ttu-id="08f86-116">*Cookie* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="08f86-116">*Cookie* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="08f86-117">Pointeur vers une variable qui doit recevoir un identificateur pour la fonction de rappel.</span><span class="sxs-lookup"><span data-stu-id="08f86-117">A pointer to a variable to receive an identifier for the callback function.</span></span> <span data-ttu-id="08f86-118">Cet identificateur est utilisé pour annuler l’inscription de la fonction de rappel de notification.</span><span class="sxs-lookup"><span data-stu-id="08f86-118">This identifier is used to unregister the notification callback function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="08f86-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="08f86-119">Return value</span></span>

<span data-ttu-id="08f86-120">Si la fonction réussit, elle retourne l' **état \_ Success**.</span><span class="sxs-lookup"><span data-stu-id="08f86-120">If the function succeeds, it returns **STATUS\_SUCCESS**.</span></span>

<span data-ttu-id="08f86-121">Les formulaires et la signification des codes d’erreur de **NTSTATUS** sont répertoriés dans le fichier d’en-tête Ntstatus. h disponible dans le kit WDK et sont décrits dans la documentation WDK.</span><span class="sxs-lookup"><span data-stu-id="08f86-121">The forms and significance of **NTSTATUS** error codes are listed in the Ntstatus.h header file available in the WDK, and are described in the WDK documentation.</span></span>

## <a name="remarks"></a><span data-ttu-id="08f86-122">Notes</span><span class="sxs-lookup"><span data-stu-id="08f86-122">Remarks</span></span>

<span data-ttu-id="08f86-123">Cette fonction n’a aucun fichier d’en-tête associé.</span><span class="sxs-lookup"><span data-stu-id="08f86-123">This function has no associated header file.</span></span> <span data-ttu-id="08f86-124">La bibliothèque d’importation associée, ntdll. lib, est disponible dans le kit WDK.</span><span class="sxs-lookup"><span data-stu-id="08f86-124">The associated import library, Ntdll.lib, is available in the WDK.</span></span> <span data-ttu-id="08f86-125">Vous pouvez également utiliser les fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) pour établir une liaison dynamique à Ntdll.dll.</span><span class="sxs-lookup"><span data-stu-id="08f86-125">You can also use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Ntdll.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="08f86-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="08f86-126">Requirements</span></span>



| <span data-ttu-id="08f86-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="08f86-127">Requirement</span></span> | <span data-ttu-id="08f86-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="08f86-128">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="08f86-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="08f86-129">Minimum supported client</span></span><br/> | <span data-ttu-id="08f86-130">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="08f86-130">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="08f86-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="08f86-131">Minimum supported server</span></span><br/> | <span data-ttu-id="08f86-132">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="08f86-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="08f86-133">DLL</span><span class="sxs-lookup"><span data-stu-id="08f86-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="08f86-134"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="08f86-134"><dt>Ntdll.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="08f86-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="08f86-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08f86-136">*LdrDllNotification*</span><span class="sxs-lookup"><span data-stu-id="08f86-136">*LdrDllNotification*</span></span>](ldrdllnotification.md)
</dt> <dt>

[<span data-ttu-id="08f86-137">**LdrUnregisterDllNotification**</span><span class="sxs-lookup"><span data-stu-id="08f86-137">**LdrUnregisterDllNotification**</span></span>](ldrunregisterdllnotification.md)
</dt> </dl>

 

 
