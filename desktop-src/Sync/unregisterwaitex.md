---
description: Annule une opération d’attente inscrite émise par la fonction RegisterWaitForSingleObject.
ms.assetid: ea700e55-fce7-46cd-bb96-0c129b429d46
title: UnregisterWaitEx, fonction (Threadpoollegacyapiset. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UnregisterWaitEx
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-threadpool-l1-1-0.dll
- KernelBase.dll
- API-MS-Win-Core-threadpool-legacy-l1-1-0.dll
- API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
- MinKernelBase.dll
ms.openlocfilehash: 30f5ad5f88bec9eb7eebff5a73d8f84f633cb249
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865405"
---
# <a name="unregisterwaitex-function"></a><span data-ttu-id="4d04c-103">UnregisterWaitEx fonction)</span><span class="sxs-lookup"><span data-stu-id="4d04c-103">UnregisterWaitEx function</span></span>

<span data-ttu-id="4d04c-104">Annule une opération d’attente inscrite émise par la fonction [**RegisterWaitForSingleObject**](/windows/desktop/api/WinBase/nf-winbase-registerwaitforsingleobject) .</span><span class="sxs-lookup"><span data-stu-id="4d04c-104">Cancels a registered wait operation issued by the [**RegisterWaitForSingleObject**](/windows/desktop/api/WinBase/nf-winbase-registerwaitforsingleobject) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d04c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4d04c-105">Syntax</span></span>


```C++
BOOL WINAPI UnregisterWaitEx(
  _In_     HANDLE WaitHandle,
  _In_opt_ HANDLE CompletionEvent
);
```



## <a name="parameters"></a><span data-ttu-id="4d04c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4d04c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4d04c-107">*WaitHandle* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4d04c-107">*WaitHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4d04c-108">Handle d'attente.</span><span class="sxs-lookup"><span data-stu-id="4d04c-108">The wait handle.</span></span> <span data-ttu-id="4d04c-109">Ce descripteur est retourné par la fonction [**RegisterWaitForSingleObject**](/windows/desktop/api/WinBase/nf-winbase-registerwaitforsingleobject) .</span><span class="sxs-lookup"><span data-stu-id="4d04c-109">This handle is returned by the [**RegisterWaitForSingleObject**](/windows/desktop/api/WinBase/nf-winbase-registerwaitforsingleobject) function.</span></span>

</dd> <dt>

<span data-ttu-id="4d04c-110">*CompletionEvent* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="4d04c-110">*CompletionEvent* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4d04c-111">Handle de l’objet d’événement à signaler lorsque l’opération d’attente a été annulée.</span><span class="sxs-lookup"><span data-stu-id="4d04c-111">A handle to the event object to be signaled when the wait operation has been unregistered.</span></span> <span data-ttu-id="4d04c-112">Ce paramètre peut être **NULL**.</span><span class="sxs-lookup"><span data-stu-id="4d04c-112">This parameter can be **NULL**.</span></span>

<span data-ttu-id="4d04c-113">Si ce paramètre n’est **pas une \_ \_ valeur de handle valide**, la fonction attend la fin de toutes les fonctions de rappel avant de retourner.</span><span class="sxs-lookup"><span data-stu-id="4d04c-113">If this parameter is **INVALID\_HANDLE\_VALUE**, the function waits for all callback functions to complete before returning.</span></span>

<span data-ttu-id="4d04c-114">Si ce paramètre a la **valeur null**, la fonction marque le minuteur pour la suppression et le retourne immédiatement.</span><span class="sxs-lookup"><span data-stu-id="4d04c-114">If this parameter is **NULL**, the function marks the timer for deletion and returns immediately.</span></span> <span data-ttu-id="4d04c-115">Toutefois, la plupart des appelants doivent attendre la fin de la fonction de rappel afin qu’ils puissent effectuer tout nettoyage nécessaire.</span><span class="sxs-lookup"><span data-stu-id="4d04c-115">However, most callers should wait for the callback function to complete so they can perform any needed cleanup.</span></span>

<span data-ttu-id="4d04c-116">Si l’appelant fournit cet événement et que la fonction réussit ou que la fonction échoue avec l' **erreur \_ e/s \_ en attente**, ne fermez pas l’événement tant qu’il n’est pas signalé.</span><span class="sxs-lookup"><span data-stu-id="4d04c-116">If the caller provides this event and the function succeeds or the function fails with **ERROR\_IO\_PENDING**, do not close the event until it is signaled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4d04c-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4d04c-117">Return value</span></span>

<span data-ttu-id="4d04c-118">Si la fonction réussit, la valeur de retour est différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="4d04c-118">If the function succeeds, the return value is nonzero.</span></span>

<span data-ttu-id="4d04c-119">Si la fonction échoue, la valeur de retour est égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="4d04c-119">If the function fails, the return value is zero.</span></span> <span data-ttu-id="4d04c-120">Pour obtenir des informations détaillées sur l’erreur, appelez [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="4d04c-120">To get extended error information, call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="4d04c-121">Remarques</span><span class="sxs-lookup"><span data-stu-id="4d04c-121">Remarks</span></span>

<span data-ttu-id="4d04c-122">Vous ne pouvez pas effectuer un appel bloquant à **UnregisterWaitEx** à partir d’une fonction de rappel pour la même opération d’attente.</span><span class="sxs-lookup"><span data-stu-id="4d04c-122">You cannot make a blocking call to **UnregisterWaitEx** from within a callback function for the same wait operation.</span></span> <span data-ttu-id="4d04c-123">Dans le cas contraire, le rappel attendra qu’il se termine.</span><span class="sxs-lookup"><span data-stu-id="4d04c-123">Otherwise, the callback will be waiting for itself to finish.</span></span> <span data-ttu-id="4d04c-124">En général, un appel bloquant à **UnregisterWaitEx** crée une dépendance entre le thread actuel et le rappel, donc pour effectuer un appel de désinscription de blocage sur une autre opération d’attente, vous devez vous assurer que les fonctions de rappel ne dépendent pas les unes des autres et que la deuxième opération d’attente n’effectue pas non plus un appel de désinscription de blocage sur la première opération.</span><span class="sxs-lookup"><span data-stu-id="4d04c-124">In general, a blocking call to **UnregisterWaitEx** creates a dependency between the current thread and the callback, so to make a blocking unregister call on another wait operation, you must ensure that the callback functions do not depend on one another and that the second wait operation does not also perform a blocking unregister call on the first operation.</span></span>

<span data-ttu-id="4d04c-125">Soyez prudent lorsque vous effectuez un appel **UnregisterWaitEx** bloquant sur un thread persistant.</span><span class="sxs-lookup"><span data-stu-id="4d04c-125">Be careful when making a blocking **UnregisterWaitEx** call on a persistent thread.</span></span> <span data-ttu-id="4d04c-126">Si l’opération d’attente en cours d’annulation d’inscription a été créée avec **WT \_ EXECUTEINPERSISTENTTHREAD**, un blocage peut se produire.</span><span class="sxs-lookup"><span data-stu-id="4d04c-126">If the wait operation being unregistered was created with **WT\_EXECUTEINPERSISTENTTHREAD**, a deadlock may occur.</span></span>

<span data-ttu-id="4d04c-127">Après avoir effectué un appel non bloquant à **UnregisterWaitEx**, aucune nouvelle fonction de rappel associée à *WaitHandle* ne peut être mise en file d’attente.</span><span class="sxs-lookup"><span data-stu-id="4d04c-127">After making non-blocking call to **UnregisterWaitEx**, no new callback functions associated with *WaitHandle* can be queued.</span></span> <span data-ttu-id="4d04c-128">Toutefois, il peut y avoir des fonctions de rappel en attente déjà mises en file d’attente dans les threads de travail.</span><span class="sxs-lookup"><span data-stu-id="4d04c-128">However, there may be pending callback functions already queued to worker threads.</span></span>

<span data-ttu-id="4d04c-129">Dans certaines conditions, la fonction échoue avec l' **erreur \_ e/s \_ en attente** si *CompletionEvent* a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="4d04c-129">Under some conditions, the function will fail with **ERROR\_IO\_PENDING** if *CompletionEvent* is **NULL**.</span></span> <span data-ttu-id="4d04c-130">Cela indique qu’il existe des fonctions de rappel en attente.</span><span class="sxs-lookup"><span data-stu-id="4d04c-130">This indicates that there are outstanding callback functions.</span></span> <span data-ttu-id="4d04c-131">Ces rappels s’exécutent ou sont en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="4d04c-131">Those callbacks either will execute or are in the middle of executing.</span></span>

<span data-ttu-id="4d04c-132">Si *CompletionEvent* est un handle d’événement fourni par l’appelant, il est possible que la fonction réussisse, échoue avec une **erreur d' \_ e/s \_ en attente** ou échoue avec un code d’erreur différent.</span><span class="sxs-lookup"><span data-stu-id="4d04c-132">If *CompletionEvent* is a handle to an event provided by the caller, it is possible for the function to succeed, fail with **ERROR\_IO\_PENDING**, or fail with a different error code.</span></span> <span data-ttu-id="4d04c-133">Si la fonction réussit, ou si la fonction échoue avec l' **erreur \_ e/s \_ en attente**, l’appelant doit toujours attendre que l’événement soit signalé pour fermer l’événement.</span><span class="sxs-lookup"><span data-stu-id="4d04c-133">If the function succeeds, or if the function fails with **ERROR\_IO\_PENDING**, the caller should always wait until the event is signaled to close the event.</span></span> <span data-ttu-id="4d04c-134">Si la fonction échoue avec un code d’erreur différent, il n’est pas nécessaire d’attendre que l’événement soit signalé pour fermer l’événement.</span><span class="sxs-lookup"><span data-stu-id="4d04c-134">If the function fails with a different error code, it is not necessary to wait until the event is signaled to close the event.</span></span>

<span data-ttu-id="4d04c-135">**Windows XP :** Si *CompletionEvent* est un handle d’événement fourni par l’appelant et que la fonction échoue avec une **erreur d' \_ e/s \_ en attente**, l’appelant doit attendre jusqu’à ce que l’événement soit signalé pour fermer l’événement.</span><span class="sxs-lookup"><span data-stu-id="4d04c-135">**Windows XP:** If *CompletionEvent* is a handle to an event provided by the caller and the function fails with **ERROR\_IO\_PENDING**, the caller should wait until the event is signaled to close the event.</span></span> <span data-ttu-id="4d04c-136">Ce comportement a été modifié à partir de Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="4d04c-136">This behavior changed starting with Windows Vista.</span></span>

<span data-ttu-id="4d04c-137">Pour compiler une application qui utilise cette fonction, définissez **\_ Win32 \_ winnt** comme 0x0500 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="4d04c-137">To compile an application that uses this function, define **\_WIN32\_WINNT** as 0x0500 or later.</span></span> <span data-ttu-id="4d04c-138">Pour plus d’informations, consultez [utilisation des en-têtes Windows](../winprog/using-the-windows-headers.md).</span><span class="sxs-lookup"><span data-stu-id="4d04c-138">For more information, see [Using the Windows Headers](../winprog/using-the-windows-headers.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4d04c-139">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4d04c-139">Requirements</span></span>



| <span data-ttu-id="4d04c-140">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4d04c-140">Requirement</span></span> | <span data-ttu-id="4d04c-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="4d04c-141">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d04c-142">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4d04c-142">Minimum supported client</span></span><br/> | <span data-ttu-id="4d04c-143">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4d04c-143">Windows XP \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="4d04c-144">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4d04c-144">Minimum supported server</span></span><br/> | <span data-ttu-id="4d04c-145">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4d04c-145">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="4d04c-146">En-tête</span><span class="sxs-lookup"><span data-stu-id="4d04c-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="4d04c-147"><dt>Threadpoollegacyapiset. h sur Windows 8 et Windows Server 2012 (incluant Windows. h); </dt> <dt>WinBase. h sur Windows 7, Windows server 2008 R2, Windows Vista, Windows server 2008, Windows XP et Windows server 2003 (incluant Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4d04c-147"><dt>Threadpoollegacyapiset.h on Windows 8 and Windows Server 2012 (include Windows.h); </dt> <dt>WinBase.h on Windows 7, Windows Server 2008 R2, Windows Vista, Windows Server 2008, Windows XP and Windows Server 2003 (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="4d04c-148">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="4d04c-148">Library</span></span><br/>                  | <dl> <span data-ttu-id="4d04c-149"><dt>Kernel32.lib</dt></span><span class="sxs-lookup"><span data-stu-id="4d04c-149"><dt>Kernel32.lib</dt></span></span> </dl>                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="4d04c-150">DLL</span><span class="sxs-lookup"><span data-stu-id="4d04c-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4d04c-151"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4d04c-151"><dt>Kernel32.dll</dt></span></span> </dl>                                                                                                                                                                                                                                                                        |



## <a name="see-also"></a><span data-ttu-id="4d04c-152">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4d04c-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d04c-153">**RegisterWaitForSingleObject**</span><span class="sxs-lookup"><span data-stu-id="4d04c-153">**RegisterWaitForSingleObject**</span></span>](/windows/desktop/api/WinBase/nf-winbase-registerwaitforsingleobject)
</dt> <dt>

[<span data-ttu-id="4d04c-154">Fonctions de synchronisation</span><span class="sxs-lookup"><span data-stu-id="4d04c-154">Synchronization Functions</span></span>](synchronization-functions.md)
</dt> <dt>

[<span data-ttu-id="4d04c-155">Regroupement des threads</span><span class="sxs-lookup"><span data-stu-id="4d04c-155">Thread Pooling</span></span>](../procthread/thread-pooling.md)
</dt> </dl>

 

 
