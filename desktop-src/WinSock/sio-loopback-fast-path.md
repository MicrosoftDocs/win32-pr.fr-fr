---
description: Le code de contrôle configure un socket TCP pour une latence plus faible et des opérations plus rapides sur l’interface de bouclage.
ms.assetid: 4F7A6454-E3ED-4529-A531-B0640B0767EF
title: Code de contrôle SIO_LOOPBACK_FAST_PATH
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: f32cba8a081d2eb268a3e93a362ccec9bf414d8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106528260"
---
# <a name="sio_loopback_fast_path-control-code"></a><span data-ttu-id="3f8e8-103">Code de contrôle SIO_LOOPBACK_FAST_PATH</span><span class="sxs-lookup"><span data-stu-id="3f8e8-103">SIO_LOOPBACK_FAST_PATH Control Code</span></span>

## <a name="description"></a><span data-ttu-id="3f8e8-104">Description</span><span class="sxs-lookup"><span data-stu-id="3f8e8-104">Description</span></span>

<span data-ttu-id="3f8e8-105">Le code de contrôle du **\_ \_ \_ chemin d’accès rapide de bouclage SIO** configure un socket TCP pour une latence plus faible et des opérations plus rapides sur l’interface de bouclage.</span><span class="sxs-lookup"><span data-stu-id="3f8e8-105">The **SIO\_LOOPBACK\_FAST\_PATH** control code configures a TCP socket for lower latency and faster operations on the loopback interface.</span></span>

<span data-ttu-id="3f8e8-106">**Important**  Le **\_ \_ \_ chemin d’accès rapide de bouclage SIO** est déconseillé et il n’est pas recommandé de l’utiliser dans votre code.</span><span class="sxs-lookup"><span data-stu-id="3f8e8-106">**Important**  The **SIO\_LOOPBACK\_FAST\_PATH** is deprecated and is not recommended to be used in your code.</span></span>

<span data-ttu-id="3f8e8-107">Pour effectuer cette opération, appelez la fonction [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** avec les paramètres suivants.</span><span class="sxs-lookup"><span data-stu-id="3f8e8-107">To perform this operation, call the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function with the following parameters.</span></span>

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_LOOPBACK_FAST_PATH,                // dwIoControlCode
  (LPVOID) lpvInBuffer,   // pointer to a Boolean value
  (DWORD) cbInBuffer,    // size, in bytes, of the input buffer
  (LPVOID) lpvOutBuffer,         // pointer to output buffer
  (DWORD) cbOutBuffer,       // size of output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

```cpp
int WSPIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_LOOPBACK_FAST_PATH,                // dwIoControlCode
  (LPVOID) lpvInBuffer,   // pointer to a Boolean value
  (DWORD) cbInBuffer,           // size, in bytes, of the input buffer
  (LPVOID) lpvOutBuffer,         // pointer to output buffer
  (DWORD) cbOutBuffer,       // size of output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
  (LPWSATHREADID) lpThreadId,   // a WSATHREADID structure
  (LPINT) lpErrno   // a pointer to the error code.
);
```

## <a name="parameters"></a><span data-ttu-id="3f8e8-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3f8e8-108">Parameters</span></span>

### <a name="s"></a><span data-ttu-id="3f8e8-109">s</span><span class="sxs-lookup"><span data-stu-id="3f8e8-109">s</span></span>

<span data-ttu-id="3f8e8-110">Descripteur identifiant un Socket.</span><span class="sxs-lookup"><span data-stu-id="3f8e8-110">A descriptor identifying a socket.</span></span>

### <a name="dwiocontrolcode"></a><span data-ttu-id="3f8e8-111">dwIoControlCode</span><span class="sxs-lookup"><span data-stu-id="3f8e8-111">dwIoControlCode</span></span>

<span data-ttu-id="3f8e8-112">Code de contrôle de l’opération.</span><span class="sxs-lookup"><span data-stu-id="3f8e8-112">The control code for the operation.</span></span>
<span data-ttu-id="3f8e8-113">Utilisez **le \_ \_ \_ chemin d’accès rapide de bouclage SIO** pour cette opération.</span><span class="sxs-lookup"><span data-stu-id="3f8e8-113">Use **SIO\_LOOPBACK\_FAST\_PATH** for this operation.</span></span>

### <a name="lpvinbuffer"></a><span data-ttu-id="3f8e8-114">lpvInBuffer</span><span class="sxs-lookup"><span data-stu-id="3f8e8-114">lpvInBuffer</span></span>

<span data-ttu-id="3f8e8-115">Pointeur vers la mémoire tampon d’entrée.</span><span class="sxs-lookup"><span data-stu-id="3f8e8-115">A pointer to the input buffer.</span></span>
<span data-ttu-id="3f8e8-116">Ce paramètre contient un pointeur vers une valeur booléenne qui indique si le socket doit être configuré pour les opérations de bouclage rapide.</span><span class="sxs-lookup"><span data-stu-id="3f8e8-116">This parameter contains a pointer to a Boolean value that indicates if the socket should be configured for fast loopback operations.</span></span>

### <a name="cbinbuffer"></a><span data-ttu-id="3f8e8-117">cbInBuffer</span><span class="sxs-lookup"><span data-stu-id="3f8e8-117">cbInBuffer</span></span>

<span data-ttu-id="3f8e8-118">Taille, en octets, de la mémoire tampon d’entrée.</span><span class="sxs-lookup"><span data-stu-id="3f8e8-118">The size, in bytes, of the input buffer.</span></span>

### <a name="lpvoutbuffer"></a><span data-ttu-id="3f8e8-119">lpvOutBuffer</span><span class="sxs-lookup"><span data-stu-id="3f8e8-119">lpvOutBuffer</span></span>

<span data-ttu-id="3f8e8-120">Pointeur vers la mémoire tampon de sortie.</span><span class="sxs-lookup"><span data-stu-id="3f8e8-120">A pointer to the output buffer.</span></span>
<span data-ttu-id="3f8e8-121">Ce paramètre n’est pas utilisé pour cette opération.</span><span class="sxs-lookup"><span data-stu-id="3f8e8-121">This parameter is unused for this operation.</span></span>

### <a name="cboutbuffer"></a><span data-ttu-id="3f8e8-122">cbOutBuffer</span><span class="sxs-lookup"><span data-stu-id="3f8e8-122">cbOutBuffer</span></span>

<span data-ttu-id="3f8e8-123">Taille, en octets, de la mémoire tampon de sortie.</span><span class="sxs-lookup"><span data-stu-id="3f8e8-123">The size, in bytes, of the output buffer.</span></span>
<span data-ttu-id="3f8e8-124">Ce paramètre doit avoir la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="3f8e8-124">This parameter must be set to zero.</span></span>

### <a name="lpcbbytesreturned"></a><span data-ttu-id="3f8e8-125">lpcbBytesReturned</span><span class="sxs-lookup"><span data-stu-id="3f8e8-125">lpcbBytesReturned</span></span>

<span data-ttu-id="3f8e8-126">Pointeur vers une variable qui reçoit la taille, en octets, des données stockées dans la mémoire tampon de sortie.</span><span class="sxs-lookup"><span data-stu-id="3f8e8-126">A pointer to a variable that receives the size, in bytes, of the data stored in the output buffer.</span></span>

<span data-ttu-id="3f8e8-127">Si la mémoire tampon de sortie est trop petite, l’appel échoue, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) retourne [**WSAEINVAL**](windows-sockets-error-codes-2.md)et le paramètre *LpcbBytesReturned* pointe vers une valeur **DWORD** égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="3f8e8-127">If the output buffer is too small, the call fails, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) returns [**WSAEINVAL**](windows-sockets-error-codes-2.md), and the *lpcbBytesReturned* parameter points to a **DWORD** value of zero.</span></span>

<span data-ttu-id="3f8e8-128">Si *lpOverlapped* a la valeur **null**, la valeur **DWORD** vers laquelle pointe le paramètre *lpcbBytesReturned* retourné sur un appel réussi ne peut pas être égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="3f8e8-128">If *lpOverlapped* is **NULL**, the **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned on a successful call cannot be zero.</span></span>

<span data-ttu-id="3f8e8-129">Si le paramètre *lpOverlapped* n’a pas la **valeur null** pour les sockets superposés, les opérations qui ne peuvent pas être terminées immédiatement seront lancées et l’achèvement sera indiqué ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="3f8e8-129">If the *lpOverlapped* parameter is not **NULL** for overlapped sockets, operations that cannot be completed immediately will be initiated, and completion will be indicated at a later time.</span></span>
<span data-ttu-id="3f8e8-130">La valeur **DWORD** pointée par le paramètre *lpcbBytesReturned* retourné peut être égale à zéro, car la taille des données stockées ne peut pas être déterminée tant que l’opération avec chevauchement n’est pas terminée.</span><span class="sxs-lookup"><span data-stu-id="3f8e8-130">The **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned may be zero since the size of the data stored can't be determined until the overlapped operation has completed.</span></span>
<span data-ttu-id="3f8e8-131">L’état d’achèvement final peut être récupéré lorsque la méthode d’achèvement appropriée est signalée lorsque l’opération est terminée.</span><span class="sxs-lookup"><span data-stu-id="3f8e8-131">The final completion status can be retrieved when the appropriate completion method is signaled when the operation has completed.</span></span>

### <a name="lpvoverlapped"></a><span data-ttu-id="3f8e8-132">lpvOverlapped</span><span class="sxs-lookup"><span data-stu-id="3f8e8-132">lpvOverlapped</span></span>

<span data-ttu-id="3f8e8-133">Pointeur vers une structure [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) .</span><span class="sxs-lookup"><span data-stu-id="3f8e8-133">A pointer to a [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="3f8e8-134">Si le socket *s* a été créé sans l’attribut Overlapped, le paramètre *lpOverlapped* est ignoré.</span><span class="sxs-lookup"><span data-stu-id="3f8e8-134">If socket *s* was created without the overlapped attribute, the *lpOverlapped* parameter is ignored.</span></span>

<span data-ttu-id="3f8e8-135">Si *s* a été ouvert avec l’attribut Overlapped et que le paramètre *lpOverlapped* n’a pas la **valeur null**, l’opération est exécutée en tant qu’opération Overlapped (asynchrone).</span><span class="sxs-lookup"><span data-stu-id="3f8e8-135">If *s* was opened with the overlapped attribute and the *lpOverlapped* parameter is not **NULL**, the operation is performed as an overlapped (asynchronous) operation.</span></span>
<span data-ttu-id="3f8e8-136">Dans ce cas, le paramètre *lpOverlapped* doit pointer vers une structure [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) valide.</span><span class="sxs-lookup"><span data-stu-id="3f8e8-136">In this case, *lpOverlapped* parameter must point to a valid [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="3f8e8-137">Pour les opérations avec chevauchement, la fonction [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** retourne immédiatement, et la méthode d’achèvement appropriée est signalée lorsque l’opération est terminée.</span><span class="sxs-lookup"><span data-stu-id="3f8e8-137">For overlapped operations, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns immediately, and the appropriate completion method is signaled when the operation has been completed.</span></span>
<span data-ttu-id="3f8e8-138">Sinon, la fonction ne retourne pas jusqu’à ce que l’opération soit terminée ou qu’une erreur se produise.</span><span class="sxs-lookup"><span data-stu-id="3f8e8-138">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

### <a name="lpcompletionroutine"></a><span data-ttu-id="3f8e8-139">lpCompletionRoutine</span><span class="sxs-lookup"><span data-stu-id="3f8e8-139">lpCompletionRoutine</span></span>

<span data-ttu-id="3f8e8-140">Type : \_ In_opt \_ [ **LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span><span class="sxs-lookup"><span data-stu-id="3f8e8-140">Type: \_In_opt\_ [**LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span></span>

<span data-ttu-id="3f8e8-141">Pointeur vers la routine de saisie semi-automatique appelée lorsque l’opération est terminée (ignoré pour les sockets non superposés).</span><span class="sxs-lookup"><span data-stu-id="3f8e8-141">A pointer to the completion routine called when the operation has been completed (ignored for non-overlapped sockets).</span></span>

### <a name="lpthreadid"></a><span data-ttu-id="3f8e8-142">lpThreadId</span><span class="sxs-lookup"><span data-stu-id="3f8e8-142">lpThreadId</span></span>

<span data-ttu-id="3f8e8-143">Pointeur vers une structure [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) qui doit être utilisée par le fournisseur dans un appel ultérieur à [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc).</span><span class="sxs-lookup"><span data-stu-id="3f8e8-143">A pointer to a [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure to be used by the provider in a subsequent call to [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc).</span></span>
<span data-ttu-id="3f8e8-144">Le fournisseur doit stocker la structure [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) référencée (pas le pointeur vers le même) jusqu’à ce que la fonction [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) soit retournée.</span><span class="sxs-lookup"><span data-stu-id="3f8e8-144">The provider should store the referenced [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure (not the pointer to same) until after the [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) function returns.</span></span>

<span data-ttu-id="3f8e8-145">**Remarque**  Ce paramètre s’applique uniquement à la fonction **WSPIoctl** .</span><span class="sxs-lookup"><span data-stu-id="3f8e8-145">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

### <a name="lperrno"></a><span data-ttu-id="3f8e8-146">lpErrno</span><span class="sxs-lookup"><span data-stu-id="3f8e8-146">lpErrno</span></span>

<span data-ttu-id="3f8e8-147">Pointeur vers le code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="3f8e8-147">A pointer to the error code.</span></span>

<span data-ttu-id="3f8e8-148">**Remarque**  Ce paramètre s’applique uniquement à la fonction **WSPIoctl** .</span><span class="sxs-lookup"><span data-stu-id="3f8e8-148">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

## <a name="return-value"></a><span data-ttu-id="3f8e8-149">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3f8e8-149">Return value</span></span>

<span data-ttu-id="3f8e8-150">Si l’opération se termine correctement, la fonction [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** retourne la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="3f8e8-150">If the operation completes successfully, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns zero.</span></span>

<span data-ttu-id="3f8e8-151">Si l’opération échoue ou est en attente, la fonction [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** retourne une **\_ erreur de socket**.</span><span class="sxs-lookup"><span data-stu-id="3f8e8-151">If the operation fails or is pending, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns **SOCKET\_ERROR**.</span></span>
<span data-ttu-id="3f8e8-152">Pour afficher les informations d’erreur étendues, appelez [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span><span class="sxs-lookup"><span data-stu-id="3f8e8-152">To get extended error information, call [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>

| <span data-ttu-id="3f8e8-153">Code d'erreur</span><span class="sxs-lookup"><span data-stu-id="3f8e8-153">Error code</span></span> | <span data-ttu-id="3f8e8-154">Signification</span><span class="sxs-lookup"><span data-stu-id="3f8e8-154">Meaning</span></span> |
|------------|---------|
|<span data-ttu-id="3f8e8-155">**\_e/s WSA \_ en attente**</span><span class="sxs-lookup"><span data-stu-id="3f8e8-155">**WSA\_IO\_PENDING**</span></span> | <span data-ttu-id="3f8e8-156">L’opération d’e/s avec chevauchement est en cours.</span><span class="sxs-lookup"><span data-stu-id="3f8e8-156">Overlapped I/O operation is in progress.</span></span> <span data-ttu-id="3f8e8-157">Cette valeur est retournée si une opération avec chevauchement a été correctement initiée et que son achèvement sera indiqué ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="3f8e8-157">This value is returned if an overlapped operation was successfully initiated and completion will be indicated at a later time.</span></span> |
| <span data-ttu-id="3f8e8-158">**\_opération WSA \_ abandonnée**</span><span class="sxs-lookup"><span data-stu-id="3f8e8-158">**WSA\_OPERATION\_ABORTED**</span></span> | <span data-ttu-id="3f8e8-159">L’opération d’e/s a été annulée en raison de la sortie d’un thread ou d’une demande de l’application.</span><span class="sxs-lookup"><span data-stu-id="3f8e8-159">The I/O operation has been aborted because of either a thread exit or an application request.</span></span> <span data-ttu-id="3f8e8-160">Cette erreur est retournée si une opération avec chevauchement a été annulée en raison de la fermeture du socket ou de l’exécution de la commande **SIO \_ flush IOCTL** .</span><span class="sxs-lookup"><span data-stu-id="3f8e8-160">This error is returned if an overlapped operation was canceled due to the closure of the socket or the execution of the **SIO\_FLUSH IOCTL** command.</span></span> |
| <span data-ttu-id="3f8e8-161">**WSAEACCES**</span><span class="sxs-lookup"><span data-stu-id="3f8e8-161">**WSAEACCES**</span></span> | <span data-ttu-id="3f8e8-162">Une tentative a été effectuée pour accéder à un socket de manière interdite par ses autorisations d’accès.</span><span class="sxs-lookup"><span data-stu-id="3f8e8-162">An attempt was made to access a socket in a way forbidden by its access permissions.</span></span> <span data-ttu-id="3f8e8-163">Cette erreur est retournée dans plusieurs conditions pour les réservations de port persistantes, notamment : l’utilisateur n’a pas les privilèges d’administrateur requis sur l’ordinateur local ou l’application n’est pas exécutée dans un interpréteur de commandes amélioré en tant qu’administrateur intégré ( `RunAs administrator` ).</span><span class="sxs-lookup"><span data-stu-id="3f8e8-163">This error is returned under several conditions for persistent port reservations that include the following: the user lacks the required administrative privileges on the local computer or the application is not running in an enhanced shell as the built-in Administrator (`RunAs administrator`).</span></span> |
| <span data-ttu-id="3f8e8-164">**WSAEFAULT**</span><span class="sxs-lookup"><span data-stu-id="3f8e8-164">**WSAEFAULT**</span></span> | <span data-ttu-id="3f8e8-165">Le système a détecté une adresse de pointeur non valide lors de la tentative d’utilisation d’un argument de pointeur dans un appel.</span><span class="sxs-lookup"><span data-stu-id="3f8e8-165">The system detected an invalid pointer address in attempting to use a pointer argument in a call.</span></span> <span data-ttu-id="3f8e8-166">Cette erreur est retournée par le paramètre *lpvInBuffer*, *lpvoutBuffer*, *lpcbBytesReturned*, *lpOverlapped* ou *lpCompletionRoutine* n’est pas entièrement contenu dans une partie valide de l’espace d’adressage de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="3f8e8-166">This error is returned of the *lpvInBuffer*, *lpvoutBuffer*, *lpcbBytesReturned*, *lpOverlapped* or *lpCompletionRoutine* parameter is not totally contained in a valid part of the user address space.</span></span> |
| <span data-ttu-id="3f8e8-167">**WSAEINPROGRESS**</span><span class="sxs-lookup"><span data-stu-id="3f8e8-167">**WSAEINPROGRESS**</span></span> | <span data-ttu-id="3f8e8-168">Une opération de blocage est actuellement en cours d'exécution.</span><span class="sxs-lookup"><span data-stu-id="3f8e8-168">A blocking operation is currently executing.</span></span> <span data-ttu-id="3f8e8-169">Cette erreur est retournée si la fonction est appelée lorsqu’un rappel est en cours.</span><span class="sxs-lookup"><span data-stu-id="3f8e8-169">This error is returned if the function is invoked when a callback is in progress.</span></span> |
| <span data-ttu-id="3f8e8-170">**WSAEINTR**</span><span class="sxs-lookup"><span data-stu-id="3f8e8-170">**WSAEINTR**</span></span> | <span data-ttu-id="3f8e8-171">Une opération de blocage a été interrompue par un appel à [**WSACancelBlockingCall**](/windows/desktop/api/winsock2/nf-winsock2-wsacancelblockingcall).</span><span class="sxs-lookup"><span data-stu-id="3f8e8-171">A blocking operation was interrupted by a call to [**WSACancelBlockingCall**](/windows/desktop/api/winsock2/nf-winsock2-wsacancelblockingcall).</span></span> <span data-ttu-id="3f8e8-172">Cette erreur est retournée si une opération de blocage a été interrompue.</span><span class="sxs-lookup"><span data-stu-id="3f8e8-172">This error is returned if a blocking operation was interrupted.</span></span> |
| <span data-ttu-id="3f8e8-173">**WSAEINVAL**</span><span class="sxs-lookup"><span data-stu-id="3f8e8-173">**WSAEINVAL**</span></span> | <span data-ttu-id="3f8e8-174">Argument non valide fourni.</span><span class="sxs-lookup"><span data-stu-id="3f8e8-174">An invalid argument was supplied.</span></span> <span data-ttu-id="3f8e8-175">Cette erreur est retournée si le paramètre *dwIoControlCode* n’est pas une commande valide, si un paramètre d’entrée spécifié n’est pas acceptable ou si la commande n’est pas applicable au type de socket spécifié.</span><span class="sxs-lookup"><span data-stu-id="3f8e8-175">This error is returned if the *dwIoControlCode* parameter is not a valid command, or a specified input parameter is not acceptable, or the command is not applicable to the type of socket specified.</span></span> |
| <span data-ttu-id="3f8e8-176">**WSAENETDOWN**</span><span class="sxs-lookup"><span data-stu-id="3f8e8-176">**WSAENETDOWN**</span></span> | <span data-ttu-id="3f8e8-177">Une opération de socket a rencontré un réseau inactif.</span><span class="sxs-lookup"><span data-stu-id="3f8e8-177">A socket operation encountered a dead network.</span></span> <span data-ttu-id="3f8e8-178">Cette erreur est retournée si le sous-système réseau a échoué.</span><span class="sxs-lookup"><span data-stu-id="3f8e8-178">This error is returned if the network subsystem has failed.</span></span> |
| <span data-ttu-id="3f8e8-179">**WSAENOTSOCK**</span><span class="sxs-lookup"><span data-stu-id="3f8e8-179">**WSAENOTSOCK**</span></span> | <span data-ttu-id="3f8e8-180">Une opération a été tentée sur un qui n’est pas un Socket.</span><span class="sxs-lookup"><span data-stu-id="3f8e8-180">An operation was attempted on something that is not a socket.</span></span> <span data-ttu-id="3f8e8-181">Cette erreur est retournée si le *descripteur* n’est pas un Socket.</span><span class="sxs-lookup"><span data-stu-id="3f8e8-181">This error is returned if the descriptor *s* is not a socket.</span></span> |
| <span data-ttu-id="3f8e8-182">**WSAEOPNOTSUPP**</span><span class="sxs-lookup"><span data-stu-id="3f8e8-182">**WSAEOPNOTSUPP**</span></span> | <span data-ttu-id="3f8e8-183">L’opération tentée n’est pas prise en charge pour le type d’objet référencé.</span><span class="sxs-lookup"><span data-stu-id="3f8e8-183">The attempted operation is not supported for the type of object referenced.</span></span> <span data-ttu-id="3f8e8-184">Cette erreur est retournée si la commande IOCTL spécifiée n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="3f8e8-184">This error is returned if the specified IOCTL command is not supported.</span></span> <span data-ttu-id="3f8e8-185">Cette erreur est également retournée si l’IOCTL du **\_ \_ \_ chemin d’accès rapide de bouclage SIO** n’est pas prise en charge par le fournisseur de transport.</span><span class="sxs-lookup"><span data-stu-id="3f8e8-185">This error is also returned if the **SIO\_LOOPBACK\_FAST\_PATH** IOCTL is not supported by the transport provider.</span></span> |

## <a name="remarks"></a><span data-ttu-id="3f8e8-186">Notes</span><span class="sxs-lookup"><span data-stu-id="3f8e8-186">Remarks</span></span>

<span data-ttu-id="3f8e8-187">Une application peut utiliser l’IOCTL du **\_ \_ \_ chemin d’accès rapide de bouclage SIO** pour réduire la latence et améliorer les performances des opérations de bouclage sur un socket TCP.</span><span class="sxs-lookup"><span data-stu-id="3f8e8-187">An application can use the **SIO\_LOOPBACK\_FAST\_PATH** IOCTL to reduce the latency and improve the performance of loopback operations on a TCP socket.</span></span>
<span data-ttu-id="3f8e8-188">Cette IOCTL demande que la pile TCP/IP utilise un chemin d’accès rapide spécial pour les opérations de bouclage sur ce Socket.</span><span class="sxs-lookup"><span data-stu-id="3f8e8-188">This IOCTL requests that the TCP/IP stack uses a special fast path for loopback operations on this socket.</span></span>
<span data-ttu-id="3f8e8-189">L’IOCTL du **\_ \_ \_ chemin d’accès rapide de bouclage SIO** peut être utilisé uniquement avec les sockets TCP.</span><span class="sxs-lookup"><span data-stu-id="3f8e8-189">The **SIO\_LOOPBACK\_FAST\_PATH** IOCTL can be used only with TCP sockets.</span></span>
<span data-ttu-id="3f8e8-190">Cette IOCTL doit être utilisée des deux côtés de la session de bouclage.</span><span class="sxs-lookup"><span data-stu-id="3f8e8-190">This IOCTL must be used on both sides of the loopback session.</span></span>
<span data-ttu-id="3f8e8-191">Le chemin d’accès rapide de bouclage TCP est pris en charge à l’aide de l’interface de bouclage IPv4 ou IPv6.</span><span class="sxs-lookup"><span data-stu-id="3f8e8-191">The TCP loopback fast path is supported using either the IPv4 or IPv6 loopback interface.</span></span>

<span data-ttu-id="3f8e8-192">Le socket qui prévoit d’initier la demande de connexion doit appliquer cette IOCTL avant d’effectuer la demande de connexion.</span><span class="sxs-lookup"><span data-stu-id="3f8e8-192">The socket that plans to initiate the connection request must apply this IOCTL before making the connection request.</span></span>
<span data-ttu-id="3f8e8-193">Par conséquent, le socket utilisé par la fonction [**Connect**](/windows/desktop/api/winsock2/nf-winsock2-connect), [**ConnectEx**](/windows/desktop/api/mswsock/nc-mswsock-lpfn_connectex), [**WSAConnect**](/windows/desktop/api/winsock2/nf-winsock2-wsaconnect), [**WSAConnectByList**](/windows/desktop/api/winsock2/nf-winsock2-wsaconnectbylist)ou [**WSACONNECTBYNAME**](/windows/desktop/api/winsock2/nf-winsock2-wsaconnectbynamew) pour initier la connexion doit appliquer cette ioctl pour utiliser le chemin d’accès rapide pour les opérations de bouclage.</span><span class="sxs-lookup"><span data-stu-id="3f8e8-193">So the socket used by the [**connect**](/windows/desktop/api/winsock2/nf-winsock2-connect), [**ConnectEx**](/windows/desktop/api/mswsock/nc-mswsock-lpfn_connectex), [**WSAConnect**](/windows/desktop/api/winsock2/nf-winsock2-wsaconnect), [**WSAConnectByList**](/windows/desktop/api/winsock2/nf-winsock2-wsaconnectbylist), or [**WSAConnectByName**](/windows/desktop/api/winsock2/nf-winsock2-wsaconnectbynamew) function to initiate the connection must apply this IOCTL to use the fast path for loopback operations.</span></span>

<span data-ttu-id="3f8e8-194">Le socket qui écoute la demande de connexion doit appliquer ce IOCTL avant d’accepter la connexion.</span><span class="sxs-lookup"><span data-stu-id="3f8e8-194">The socket that is listening for the connection request must apply this IOCTL before accepting the connection.</span></span>
<span data-ttu-id="3f8e8-195">Par conséquent, le socket utilisé par la fonction listen doit appliquer cette IOCTL afin que tous les sockets acceptés utilisent le chemin d’accès rapide pour le bouclage.</span><span class="sxs-lookup"><span data-stu-id="3f8e8-195">So the socket used by the listen function must apply this IOCTL so any sockets that are accepted will use the fast path for loopback.</span></span>
<span data-ttu-id="3f8e8-196">Tous les sockets retournés par la fonction listen et transmis à la fonction [**Accept**](/windows/desktop/api/winsock2/nf-winsock2-accept), [**accepted**](/windows/desktop/api/winsock/nf-winsock-acceptex)ou [**WSAAccept**](/windows/desktop/api/winsock2/nf-winsock2-wsaaccept) sont marqués pour utiliser le chemin d’accès rapide spécial pour les opérations de bouclage.</span><span class="sxs-lookup"><span data-stu-id="3f8e8-196">Any sockets returned by the listen function and passed to the [**accept**](/windows/desktop/api/winsock2/nf-winsock2-accept), [**AcceptEx**](/windows/desktop/api/winsock/nf-winsock-acceptex), or [**WSAAccept**](/windows/desktop/api/winsock2/nf-winsock2-wsaaccept) function will be marked to use the special fast path for loopback operations.</span></span>

<span data-ttu-id="3f8e8-197">Une fois qu’une application établit la connexion sur une interface de bouclage à l’aide du chemin d’accès rapide, tous les paquets pour la durée de vie de la connexion doivent utiliser le chemin d’accès rapide.</span><span class="sxs-lookup"><span data-stu-id="3f8e8-197">Once an application establishes the connection on a loopback interface using the fast path, all packets for the lifetime of the connection must use the fast path.</span></span>

<span data-ttu-id="3f8e8-198">L’application du **\_ \_ \_ chemin d’accès rapide de bouclage SIO** à un socket qui sera connecté à un chemin d’accès sans bouclage n’aura aucun effet.</span><span class="sxs-lookup"><span data-stu-id="3f8e8-198">Applying **SIO\_LOOPBACK\_FAST\_PATH** to a socket which will be connected to a non-loopback path will have no effect.</span></span>

<span data-ttu-id="3f8e8-199">Cette optimisation de bouclage TCP entraîne des paquets qui transitent par la couche de transport (TL) au lieu du bouclage traditionnel via la couche réseau.</span><span class="sxs-lookup"><span data-stu-id="3f8e8-199">This TCP loopback optimization results in packets that flow through the Transport Layer (TL) instead of the traditional loopback through the Network Layer.</span></span>
<span data-ttu-id="3f8e8-200">Cette optimisation améliore la latence des paquets de bouclage.</span><span class="sxs-lookup"><span data-stu-id="3f8e8-200">This optimization improves the latency for loopback packets.</span></span>
<span data-ttu-id="3f8e8-201">Une fois qu’une application a défini un paramètre de niveau de connexion pour utiliser le chemin d’accès rapide de bouclage, tous les paquets suivent le chemin de bouclage.</span><span class="sxs-lookup"><span data-stu-id="3f8e8-201">Once an application opts in for a connection level setting to use the loopback fast path, all packets will follow the loopback path.</span></span>
<span data-ttu-id="3f8e8-202">Pour les communications de bouclage, la congestion et le rejet de paquets ne sont pas attendus.</span><span class="sxs-lookup"><span data-stu-id="3f8e8-202">For loopback communications, congestion and packet drop are not expected.</span></span>
<span data-ttu-id="3f8e8-203">La notion de contrôle d’encombrement et de remise fiable dans TCP n’est pas nécessaire.</span><span class="sxs-lookup"><span data-stu-id="3f8e8-203">The notion of congestion control and reliable delivery in TCP will be unnecessary.</span></span>
<span data-ttu-id="3f8e8-204">Toutefois, cela n’est pas vrai pour le contrôle de Flow.</span><span class="sxs-lookup"><span data-stu-id="3f8e8-204">This, however, is not true for flow control.</span></span>
<span data-ttu-id="3f8e8-205">Sans contrôle de Flow, l’expéditeur peut saturer la mémoire tampon de réception, ce qui se traduit par un comportement de bouclage TCP erroné.</span><span class="sxs-lookup"><span data-stu-id="3f8e8-205">Without flow control, the sender can overwhelm the receive buffer, leading to erroneous TCP loopback behavior.</span></span>
<span data-ttu-id="3f8e8-206">Le contrôle de Flow dans le chemin de bouclage optimisé TCP est conservé en plaçant les demandes Send dans une file d’attente.</span><span class="sxs-lookup"><span data-stu-id="3f8e8-206">The flow control in the TCP optimized loopback path is maintained by placing send requests in a queue.</span></span>
<span data-ttu-id="3f8e8-207">Lorsque la mémoire tampon de réception est pleine, la pile TCP/IP garantit que les envois ne se terminent pas tant que la file d’attente ne prend pas en service le contrôle de Workflow.</span><span class="sxs-lookup"><span data-stu-id="3f8e8-207">When receive buffer is full, the TCP/IP stack guarantees that the sends won't complete until the queue is serviced maintaining flow control.</span></span>

<span data-ttu-id="3f8e8-208">Les connexions de bouclage TCP Fast Path en présence d’une légende de plateforme de filtrage Windows (WFP) pour les données de connexion doivent prendre le chemin lent non optimisé pour le bouclage.</span><span class="sxs-lookup"><span data-stu-id="3f8e8-208">TCP fast path loopback connections in the presence of a Windows Filtering Platform (WFP) callout for connection data must take the un-optimized slow path for loopback.</span></span>
<span data-ttu-id="3f8e8-209">Par conséquent, les filtres WFP empêchent l’utilisation de ce nouveau chemin d’accès rapide de bouclage.</span><span class="sxs-lookup"><span data-stu-id="3f8e8-209">So WFP filters will prevent this new loopback fast path from being used.</span></span>
<span data-ttu-id="3f8e8-210">Quand un filtre WFP est activé, le système utilise le chemin d’accès lent même si l’IOCTL du **\_ \_ \_ chemin d’accès rapide de bouclage SIO** a été définie.</span><span class="sxs-lookup"><span data-stu-id="3f8e8-210">When a WFP filter is enabled, the system we will use the slow path even if the **SIO\_LOOPBACK\_FAST\_PATH** IOCTL was set.</span></span>
<span data-ttu-id="3f8e8-211">Cela garantit que les applications en mode utilisateur disposent de la fonctionnalité de sécurité WFP complète.</span><span class="sxs-lookup"><span data-stu-id="3f8e8-211">This ensures that user-mode applications have the full WFP security capability.</span></span>

<span data-ttu-id="3f8e8-212">Par défaut, **le \_ \_ \_ chemin d’accès rapide de bouclage SIO** est désactivé.</span><span class="sxs-lookup"><span data-stu-id="3f8e8-212">By default, **SIO\_LOOPBACK\_FAST\_PATH** is disabled.</span></span>

<span data-ttu-id="3f8e8-213">Seul un sous-ensemble des options de socket TCP/IP est pris en charge lorsque l’IOCTL du **\_ \_ \_ chemin d’accès rapide de bouclage SIO** est utilisé pour activer le chemin d’accès rapide de bouclage sur un Socket.</span><span class="sxs-lookup"><span data-stu-id="3f8e8-213">Only a subset of the TCP/IP socket options are supported when the **SIO\_LOOPBACK\_FAST\_PATH** IOCTL is used to enable the loopback fast path on a socket.</span></span>
<span data-ttu-id="3f8e8-214">La liste des options prises en charge comprend les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="3f8e8-214">The list of supported options includes the following:</span></span>

* <span data-ttu-id="3f8e8-215">**\_TTL IP**</span><span class="sxs-lookup"><span data-stu-id="3f8e8-215">**IP\_TTL**</span></span>
* <span data-ttu-id="3f8e8-216">**monodiffusion IP \_ \_ si**</span><span class="sxs-lookup"><span data-stu-id="3f8e8-216">**IP\_UNICAST\_IF**</span></span>
* <span data-ttu-id="3f8e8-217">**\_Tronçons de monodiffusion IPv6 \_**</span><span class="sxs-lookup"><span data-stu-id="3f8e8-217">**IPV6\_UNICAST\_HOPS**</span></span>
* <span data-ttu-id="3f8e8-218">**Monodiffusion IPV6 \_ \_ si**</span><span class="sxs-lookup"><span data-stu-id="3f8e8-218">**IPV6\_UNICAST\_IF**</span></span>
* <span data-ttu-id="3f8e8-219">**\_V6ONLY IPv6**</span><span class="sxs-lookup"><span data-stu-id="3f8e8-219">**IPV6\_V6ONLY**</span></span>
* <span data-ttu-id="3f8e8-220">**\_accepter l' \_ acceptation conditionnelle**</span><span class="sxs-lookup"><span data-stu-id="3f8e8-220">**SO\_CONDITIONAL\_ACCEPT**</span></span>
* <span data-ttu-id="3f8e8-221">**\_EXCLUSIVEADDRUSE**</span><span class="sxs-lookup"><span data-stu-id="3f8e8-221">**SO\_EXCLUSIVEADDRUSE**</span></span>
* <span data-ttu-id="3f8e8-222">**\_ \_ l’évolutivité des ports**</span><span class="sxs-lookup"><span data-stu-id="3f8e8-222">**SO\_PORT\_SCALABILITY**</span></span>
* <span data-ttu-id="3f8e8-223">**\_RCVBUF**</span><span class="sxs-lookup"><span data-stu-id="3f8e8-223">**SO\_RCVBUF**</span></span>
* <span data-ttu-id="3f8e8-224">**\_REUSEADDR**</span><span class="sxs-lookup"><span data-stu-id="3f8e8-224">**SO\_REUSEADDR**</span></span>
* <span data-ttu-id="3f8e8-225">**\_BSDURGENT TCP**</span><span class="sxs-lookup"><span data-stu-id="3f8e8-225">**TCP\_BSDURGENT**</span></span>

## <a name="see-also"></a><span data-ttu-id="3f8e8-226">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3f8e8-226">See also</span></span>

[<span data-ttu-id="3f8e8-227">**Options de socket IPPROTO_IP**</span><span class="sxs-lookup"><span data-stu-id="3f8e8-227">**IPPROTO_IP Socket Options**</span></span>](/windows/desktop/winsock/ipproto-ip-socket-options)

[<span data-ttu-id="3f8e8-228">**Options de socket IPPROTO_IPV6**</span><span class="sxs-lookup"><span data-stu-id="3f8e8-228">**IPPROTO_IPV6 Socket Options**</span></span>](/windows/desktop/winsock/ipproto-ipv6-socket-options)

[<span data-ttu-id="3f8e8-229">**Options de socket IPPROTO_TCP**</span><span class="sxs-lookup"><span data-stu-id="3f8e8-229">**IPPROTO_TCP Socket Options**</span></span>](/windows/desktop/winsock/ipproto-tcp-socket-options)

[<span data-ttu-id="3f8e8-230">**socle**</span><span class="sxs-lookup"><span data-stu-id="3f8e8-230">**socket**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-socket)

[<span data-ttu-id="3f8e8-231">**Options de socket SOL_SOCKET**</span><span class="sxs-lookup"><span data-stu-id="3f8e8-231">**SOL_SOCKET Socket Options**</span></span>](/windows/desktop/winsock/sol-socket-socket-options)

[<span data-ttu-id="3f8e8-232">**WSAGetLastError**</span><span class="sxs-lookup"><span data-stu-id="3f8e8-232">**WSAGetLastError**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetlasterror)

[<span data-ttu-id="3f8e8-233">**WSAGetOverlappedResult**</span><span class="sxs-lookup"><span data-stu-id="3f8e8-233">**WSAGetOverlappedResult**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[<span data-ttu-id="3f8e8-234">**WSAIoctl**</span><span class="sxs-lookup"><span data-stu-id="3f8e8-234">**WSAIoctl**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[<span data-ttu-id="3f8e8-235">**WSAOVERLAPPED**</span><span class="sxs-lookup"><span data-stu-id="3f8e8-235">**WSAOVERLAPPED**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[<span data-ttu-id="3f8e8-236">**WSASocketA**</span><span class="sxs-lookup"><span data-stu-id="3f8e8-236">**WSASocketA**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[<span data-ttu-id="3f8e8-237">**WSASocketW**</span><span class="sxs-lookup"><span data-stu-id="3f8e8-237">**WSASocketW**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
