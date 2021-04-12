---
description: Code de contrôle qui configure les paramètres de délai de retransmission initiaux (RTO) sur un Socket.
ms.assetid: F5ABAE57-E0F0-4AEB-825C-B53AEE8210E7
title: Code de contrôle SIO_TCP_INITIAL_RTO
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 116bab23c2c5f4ef21b77a1b7f9fefa8b3ff3099
ms.sourcegitcommit: 191184ea30e209f67267ebe5b222dc16965e54e0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2020
ms.locfileid: "104463883"
---
# <a name="sio_tcp_initial_rto-control-code"></a><span data-ttu-id="b1387-103">Code de contrôle SIO_TCP_INITIAL_RTO</span><span class="sxs-lookup"><span data-stu-id="b1387-103">SIO_TCP_INITIAL_RTO control code</span></span>

## <a name="description"></a><span data-ttu-id="b1387-104">Description</span><span class="sxs-lookup"><span data-stu-id="b1387-104">Description</span></span>

<span data-ttu-id="b1387-105">Le code de contrôle **SIO_TCP_INITIAL_RTO** configure les paramètres de délai de retransmission initiaux (RTO) sur un Socket.</span><span class="sxs-lookup"><span data-stu-id="b1387-105">The **SIO_TCP_INITIAL_RTO** control code configures initial retransmission timeout (RTO) parameters on a socket.</span></span>

<span data-ttu-id="b1387-106">Pour effectuer cette opération, appelez la fonction [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** avec les paramètres suivants.</span><span class="sxs-lookup"><span data-stu-id="b1387-106">To perform this operation, call the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function with the following parameters.</span></span>

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_TCP_INITIAL_RTO,                // dwIoControlCode
  (LPVOID) lpvInBuffer,   // pointer to a TCP_INITIAL_RTO_PARAMETERS structure
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
  SIO_TCP_INITIAL_RTO,                // dwIoControlCode
  (LPVOID) lpvInBuffer,   // pointer to a TCP_INITIAL_RTO_PARAMETERS structure
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

## <a name="parameters"></a><span data-ttu-id="b1387-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b1387-107">Parameters</span></span>

### <a name="s"></a><span data-ttu-id="b1387-108">s</span><span class="sxs-lookup"><span data-stu-id="b1387-108">s</span></span>

<span data-ttu-id="b1387-109">Descripteur identifiant un Socket.</span><span class="sxs-lookup"><span data-stu-id="b1387-109">A descriptor identifying a socket.</span></span>

### <a name="dwiocontrolcode"></a><span data-ttu-id="b1387-110">dwIoControlCode</span><span class="sxs-lookup"><span data-stu-id="b1387-110">dwIoControlCode</span></span>

<span data-ttu-id="b1387-111">Code de contrôle de l’opération.</span><span class="sxs-lookup"><span data-stu-id="b1387-111">The control code for the operation.</span></span>
<span data-ttu-id="b1387-112">Utilisez **SIO_TCP_INITIAL_RTO** pour cette opération.</span><span class="sxs-lookup"><span data-stu-id="b1387-112">Use **SIO_TCP_INITIAL_RTO** for this operation.</span></span>

### <a name="lpvinbuffer"></a><span data-ttu-id="b1387-113">lpvInBuffer</span><span class="sxs-lookup"><span data-stu-id="b1387-113">lpvInBuffer</span></span>

<span data-ttu-id="b1387-114">Pointeur vers la mémoire tampon d’entrée.</span><span class="sxs-lookup"><span data-stu-id="b1387-114">A pointer to the input buffer.</span></span>
<span data-ttu-id="b1387-115">Ce paramètre contient un pointeur vers le [**TCP_INITIAL_RTO_PARAMETERS**](/windows/desktop/api/mstcpip/ns-mstcpip-tcp_initial_rto_parameters) associé au socket.</span><span class="sxs-lookup"><span data-stu-id="b1387-115">This parameter contains a pointer to the [**TCP_INITIAL_RTO_PARAMETERS**](/windows/desktop/api/mstcpip/ns-mstcpip-tcp_initial_rto_parameters) associated with the socket.</span></span>

### <a name="cbinbuffer"></a><span data-ttu-id="b1387-116">cbInBuffer</span><span class="sxs-lookup"><span data-stu-id="b1387-116">cbInBuffer</span></span>

<span data-ttu-id="b1387-117">Taille, en octets, de la mémoire tampon d’entrée.</span><span class="sxs-lookup"><span data-stu-id="b1387-117">The size, in bytes, of the input buffer.</span></span>

### <a name="lpvoutbuffer"></a><span data-ttu-id="b1387-118">lpvOutBuffer</span><span class="sxs-lookup"><span data-stu-id="b1387-118">lpvOutBuffer</span></span>

<span data-ttu-id="b1387-119">Pointeur vers la mémoire tampon de sortie.</span><span class="sxs-lookup"><span data-stu-id="b1387-119">A pointer to the output buffer.</span></span>
<span data-ttu-id="b1387-120">Ce paramètre n’est pas utilisé pour cette opération.</span><span class="sxs-lookup"><span data-stu-id="b1387-120">This parameter is unused for this operation.</span></span>

### <a name="cboutbuffer"></a><span data-ttu-id="b1387-121">cbOutBuffer</span><span class="sxs-lookup"><span data-stu-id="b1387-121">cbOutBuffer</span></span>

<span data-ttu-id="b1387-122">Taille, en octets, de la mémoire tampon de sortie.</span><span class="sxs-lookup"><span data-stu-id="b1387-122">The size, in bytes, of the output buffer.</span></span>
<span data-ttu-id="b1387-123">Ce paramètre doit avoir la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="b1387-123">This parameter must be set to zero.</span></span>

### <a name="lpcbbytesreturned"></a><span data-ttu-id="b1387-124">lpcbBytesReturned</span><span class="sxs-lookup"><span data-stu-id="b1387-124">lpcbBytesReturned</span></span>

<span data-ttu-id="b1387-125">Pointeur vers une variable qui reçoit la taille, en octets, des données stockées dans la mémoire tampon de sortie.</span><span class="sxs-lookup"><span data-stu-id="b1387-125">A pointer to a variable that receives the size, in bytes, of the data stored in the output buffer.</span></span>

<span data-ttu-id="b1387-126">Si la mémoire tampon de sortie est trop petite, l’appel échoue, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) retourne [**WSAEINVAL**](windows-sockets-error-codes-2.md)et le paramètre *LpcbBytesReturned* pointe vers une valeur **DWORD** égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="b1387-126">If the output buffer is too small, the call fails, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) returns [**WSAEINVAL**](windows-sockets-error-codes-2.md), and the *lpcbBytesReturned* parameter points to a **DWORD** value of zero.</span></span>

<span data-ttu-id="b1387-127">Si *lpOverlapped* a la valeur **null**, la valeur **DWORD** vers laquelle pointe le paramètre *lpcbBytesReturned* retourné sur un appel réussi ne peut pas être égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="b1387-127">If *lpOverlapped* is **NULL**, the **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned on a successful call cannot be zero.</span></span>

<span data-ttu-id="b1387-128">Si le paramètre *lpOverlapped* n’a pas la **valeur null** pour les sockets superposés, les opérations qui ne peuvent pas être terminées immédiatement seront lancées et l’achèvement sera indiqué ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="b1387-128">If the *lpOverlapped* parameter is not **NULL** for overlapped sockets, operations that cannot be completed immediately will be initiated, and completion will be indicated at a later time.</span></span>
<span data-ttu-id="b1387-129">La valeur **DWORD** pointée par le paramètre *lpcbBytesReturned* retourné peut être égale à zéro, car la taille des données stockées ne peut pas être déterminée tant que l’opération avec chevauchement n’est pas terminée.</span><span class="sxs-lookup"><span data-stu-id="b1387-129">The **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned may be zero since the size of the data stored can't be determined until the overlapped operation has completed.</span></span>
<span data-ttu-id="b1387-130">L’état d’achèvement final peut être récupéré lorsque la méthode d’achèvement appropriée est signalée lorsque l’opération est terminée.</span><span class="sxs-lookup"><span data-stu-id="b1387-130">The final completion status can be retrieved when the appropriate completion method is signaled when the operation has completed.</span></span>

### <a name="lpvoverlapped"></a><span data-ttu-id="b1387-131">lpvOverlapped</span><span class="sxs-lookup"><span data-stu-id="b1387-131">lpvOverlapped</span></span>

<span data-ttu-id="b1387-132">Pointeur vers une structure [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) .</span><span class="sxs-lookup"><span data-stu-id="b1387-132">A pointer to a [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="b1387-133">Si le socket *s* a été créé sans l’attribut Overlapped, le paramètre *lpOverlapped* est ignoré.</span><span class="sxs-lookup"><span data-stu-id="b1387-133">If socket *s* was created without the overlapped attribute, the *lpOverlapped* parameter is ignored.</span></span>

<span data-ttu-id="b1387-134">Si *s* a été ouvert avec l’attribut Overlapped et que le paramètre *lpOverlapped* n’a pas la **valeur null**, l’opération est exécutée en tant qu’opération Overlapped (asynchrone).</span><span class="sxs-lookup"><span data-stu-id="b1387-134">If *s* was opened with the overlapped attribute and the *lpOverlapped* parameter is not **NULL**, the operation is performed as an overlapped (asynchronous) operation.</span></span>
<span data-ttu-id="b1387-135">Dans ce cas, le paramètre *lpOverlapped* doit pointer vers une structure [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) valide.</span><span class="sxs-lookup"><span data-stu-id="b1387-135">In this case, *lpOverlapped* parameter must point to a valid [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="b1387-136">Pour les opérations avec chevauchement, la fonction [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** retourne immédiatement, et la méthode d’achèvement appropriée est signalée lorsque l’opération est terminée.</span><span class="sxs-lookup"><span data-stu-id="b1387-136">For overlapped operations, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns immediately, and the appropriate completion method is signaled when the operation has been completed.</span></span>
<span data-ttu-id="b1387-137">Sinon, la fonction ne retourne pas jusqu’à ce que l’opération soit terminée ou qu’une erreur se produise.</span><span class="sxs-lookup"><span data-stu-id="b1387-137">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

### <a name="lpcompletionroutine"></a><span data-ttu-id="b1387-138">lpCompletionRoutine</span><span class="sxs-lookup"><span data-stu-id="b1387-138">lpCompletionRoutine</span></span>

<span data-ttu-id="b1387-139">Type : \_ In_opt \_ [ **LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span><span class="sxs-lookup"><span data-stu-id="b1387-139">Type: \_In_opt\_ [**LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span></span>

<span data-ttu-id="b1387-140">Pointeur vers la routine de saisie semi-automatique appelée lorsque l’opération est terminée (ignoré pour les sockets non superposés).</span><span class="sxs-lookup"><span data-stu-id="b1387-140">A pointer to the completion routine called when the operation has been completed (ignored for non-overlapped sockets).</span></span>

### <a name="lpthreadid"></a><span data-ttu-id="b1387-141">lpThreadId</span><span class="sxs-lookup"><span data-stu-id="b1387-141">lpThreadId</span></span>

<span data-ttu-id="b1387-142">Pointeur vers une structure [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) qui doit être utilisée par le fournisseur dans un appel ultérieur à [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc).</span><span class="sxs-lookup"><span data-stu-id="b1387-142">A pointer to a [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure to be used by the provider in a subsequent call to [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc).</span></span>
<span data-ttu-id="b1387-143">Le fournisseur doit stocker la structure [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) référencée (pas le pointeur vers le même) jusqu’à ce que la fonction [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) soit retournée.</span><span class="sxs-lookup"><span data-stu-id="b1387-143">The provider should store the referenced [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure (not the pointer to same) until after the [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) function returns.</span></span>

<span data-ttu-id="b1387-144">**Remarque**  Ce paramètre s’applique uniquement à la fonction **WSPIoctl** .</span><span class="sxs-lookup"><span data-stu-id="b1387-144">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

### <a name="lperrno"></a><span data-ttu-id="b1387-145">lpErrno</span><span class="sxs-lookup"><span data-stu-id="b1387-145">lpErrno</span></span>

<span data-ttu-id="b1387-146">Pointeur vers le code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="b1387-146">A pointer to the error code.</span></span>

<span data-ttu-id="b1387-147">**Remarque**  Ce paramètre s’applique uniquement à la fonction **WSPIoctl** .</span><span class="sxs-lookup"><span data-stu-id="b1387-147">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

## <a name="return-value"></a><span data-ttu-id="b1387-148">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b1387-148">Return value</span></span>

<span data-ttu-id="b1387-149">Si l’opération se termine correctement, la fonction [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** retourne la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="b1387-149">If the operation completes successfully, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns zero.</span></span>

<span data-ttu-id="b1387-150">Si l’opération échoue ou est en attente, la fonction [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** retourne une **\_ erreur de socket**.</span><span class="sxs-lookup"><span data-stu-id="b1387-150">If the operation fails or is pending, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns **SOCKET\_ERROR**.</span></span>
<span data-ttu-id="b1387-151">Pour afficher les informations d’erreur étendues, appelez [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span><span class="sxs-lookup"><span data-stu-id="b1387-151">To get extended error information, call [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>

| <span data-ttu-id="b1387-152">Code d'erreur</span><span class="sxs-lookup"><span data-stu-id="b1387-152">Error code</span></span> | <span data-ttu-id="b1387-153">Signification</span><span class="sxs-lookup"><span data-stu-id="b1387-153">Meaning</span></span> |
|------------|---------|
| <span data-ttu-id="b1387-154">**\_e/s WSA \_ en attente**</span><span class="sxs-lookup"><span data-stu-id="b1387-154">**WSA\_IO\_PENDING**</span></span> | <span data-ttu-id="b1387-155">L’opération d’e/s avec chevauchement est en cours.</span><span class="sxs-lookup"><span data-stu-id="b1387-155">Overlapped I/O operation is in progress.</span></span> <span data-ttu-id="b1387-156">Cette valeur est retournée si une opération avec chevauchement a été correctement initiée et que son achèvement sera indiqué ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="b1387-156">This value is returned if an overlapped operation was successfully initiated and completion will be indicated at a later time.</span></span> |
| <span data-ttu-id="b1387-157">**\_opération WSA \_ abandonnée**</span><span class="sxs-lookup"><span data-stu-id="b1387-157">**WSA\_OPERATION\_ABORTED**</span></span> | <span data-ttu-id="b1387-158">L’opération d’e/s a été annulée en raison de la sortie d’un thread ou d’une demande de l’application.</span><span class="sxs-lookup"><span data-stu-id="b1387-158">The I/O operation has been aborted because of either a thread exit or an application request.</span></span> <span data-ttu-id="b1387-159">Cette erreur est retournée si une opération avec chevauchement a été annulée en raison de la fermeture du socket ou de l’exécution de la commande **SIO \_ flush** ioctl.</span><span class="sxs-lookup"><span data-stu-id="b1387-159">This error is returned if an overlapped operation was canceled due to the closure of the socket or the execution of the **SIO\_FLUSH** IOCTL command.</span></span> |
| <span data-ttu-id="b1387-160">**WSAEACCES**</span><span class="sxs-lookup"><span data-stu-id="b1387-160">**WSAEACCES**</span></span> | <span data-ttu-id="b1387-161">Une tentative a été effectuée pour accéder à un socket de manière interdite par ses autorisations d’accès.</span><span class="sxs-lookup"><span data-stu-id="b1387-161">An attempt was made to access a socket in a way forbidden by its access permissions.</span></span> <span data-ttu-id="b1387-162">Cette erreur est retournée dans plusieurs conditions : l’utilisateur n’a pas les privilèges d’administrateur requis sur l’ordinateur local ou l’application ne s’exécute pas dans un interpréteur de commandes amélioré en tant qu’administrateur intégré ( `RunAs administrator` ).</span><span class="sxs-lookup"><span data-stu-id="b1387-162">This error is returned under several conditions that include the following: the user lacks the required administrative privileges on the local computer or the application is not running in an enhanced shell as the built-in Administrator (`RunAs administrator`).</span></span> |
| <span data-ttu-id="b1387-163">**WSAEFAULT**</span><span class="sxs-lookup"><span data-stu-id="b1387-163">**WSAEFAULT**</span></span> | <span data-ttu-id="b1387-164">Le système a détecté une adresse de pointeur non valide lors de la tentative d’utilisation d’un argument de pointeur dans un appel.</span><span class="sxs-lookup"><span data-stu-id="b1387-164">The system detected an invalid pointer address in attempting to use a pointer argument in a call.</span></span> <span data-ttu-id="b1387-165">Cette erreur est retournée par le paramètre *lpvInBuffer*, *lpvoutBuffer*, *lpcbBytesReturned*, *lpOverlapped* ou *lpCompletionRoutine* n’est pas entièrement contenu dans une partie valide de l’espace d’adressage de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b1387-165">This error is returned of the *lpvInBuffer*, *lpvoutBuffer*, *lpcbBytesReturned*, *lpOverlapped* or *lpCompletionRoutine* parameter is not totally contained in a valid part of the user address space.</span></span> |
| <span data-ttu-id="b1387-166">**WSAEINPROGRESS**</span><span class="sxs-lookup"><span data-stu-id="b1387-166">**WSAEINPROGRESS**</span></span> | <span data-ttu-id="b1387-167">Une opération de blocage est actuellement en cours d'exécution.</span><span class="sxs-lookup"><span data-stu-id="b1387-167">A blocking operation is currently executing.</span></span> <span data-ttu-id="b1387-168">Cette erreur est retournée si la fonction est appelée lorsqu’un rappel est en cours.</span><span class="sxs-lookup"><span data-stu-id="b1387-168">This error is returned if the function is invoked when a callback is in progress.</span></span> |
| <span data-ttu-id="b1387-169">**WSAEINTR**</span><span class="sxs-lookup"><span data-stu-id="b1387-169">**WSAEINTR**</span></span> | <span data-ttu-id="b1387-170">Une opération de blocage a été interrompue par un appel à *WSACancelBlockingCall*.</span><span class="sxs-lookup"><span data-stu-id="b1387-170">A blocking operation was interrupted by a call to *WSACancelBlockingCall*.</span></span> <span data-ttu-id="b1387-171">Cette erreur est retournée si une opération de blocage a été interrompue.</span><span class="sxs-lookup"><span data-stu-id="b1387-171">This error is returned if a blocking operation was interrupted.</span></span> |
| <span data-ttu-id="b1387-172">**WSAEINVAL**</span><span class="sxs-lookup"><span data-stu-id="b1387-172">**WSAEINVAL**</span></span> | <span data-ttu-id="b1387-173">Argument non valide fourni.</span><span class="sxs-lookup"><span data-stu-id="b1387-173">An invalid argument was supplied.</span></span> <span data-ttu-id="b1387-174">Cette erreur est retournée si le paramètre *dwIoControlCode* n’est pas une commande valide, si un paramètre d’entrée spécifié n’est pas acceptable ou si la commande n’est pas applicable au type de socket spécifié.</span><span class="sxs-lookup"><span data-stu-id="b1387-174">This error is returned if the *dwIoControlCode* parameter is not a valid command, or a specified input parameter is not acceptable, or the command is not applicable to the type of socket specified.</span></span> |
| <span data-ttu-id="b1387-175">**WSAENETDOWN**</span><span class="sxs-lookup"><span data-stu-id="b1387-175">**WSAENETDOWN**</span></span> | <span data-ttu-id="b1387-176">Une opération de socket a rencontré un réseau inactif.</span><span class="sxs-lookup"><span data-stu-id="b1387-176">A socket operation encountered a dead network.</span></span> <span data-ttu-id="b1387-177">Cette erreur est retournée si le sous-système réseau a échoué.</span><span class="sxs-lookup"><span data-stu-id="b1387-177">This error is returned if the network subsystem has failed.</span></span> |
| <span data-ttu-id="b1387-178">**WSAENOTSOCK**</span><span class="sxs-lookup"><span data-stu-id="b1387-178">**WSAENOTSOCK**</span></span> | <span data-ttu-id="b1387-179">Une opération a été tentée sur un qui n’est pas un Socket.</span><span class="sxs-lookup"><span data-stu-id="b1387-179">An operation was attempted on something that is not a socket.</span></span> <span data-ttu-id="b1387-180">Cette erreur est retournée si le descripteur n’est pas un Socket.</span><span class="sxs-lookup"><span data-stu-id="b1387-180">This error is returned if the descriptor s is not a socket.</span></span> |
| <span data-ttu-id="b1387-181">**WSAEOPNOTSUPP**</span><span class="sxs-lookup"><span data-stu-id="b1387-181">**WSAEOPNOTSUPP**</span></span> | <span data-ttu-id="b1387-182">L’opération tentée n’est pas prise en charge pour le type d’objet référencé.</span><span class="sxs-lookup"><span data-stu-id="b1387-182">The attempted operation is not supported for the type of object referenced.</span></span> <span data-ttu-id="b1387-183">Cette erreur est retournée si la commande IOCTL spécifiée n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="b1387-183">This error is returned if the specified IOCTL command is not supported.</span></span> <span data-ttu-id="b1387-184">Cette erreur est également retournée si le **SIO_TCP_INITIAL_RTO** IOCTL n’est pas pris en charge par le fournisseur de transport.</span><span class="sxs-lookup"><span data-stu-id="b1387-184">This error is also returned if the **SIO_TCP_INITIAL_RTO** IOCTL is not supported by the transport provider.</span></span> |

## <a name="remarks"></a><span data-ttu-id="b1387-185">Notes</span><span class="sxs-lookup"><span data-stu-id="b1387-185">Remarks</span></span>

<span data-ttu-id="b1387-186">Une application peut utiliser le **SIO_TCP_INITIAL_RTO** ioctl pour contrôler les caractéristiques de retransmission initiales (SYN/SYN + ACK) d’un socket TCP, si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="b1387-186">An application can use the **SIO_TCP_INITIAL_RTO** IOCTL to control the initial (SYN / SYN+ACK) retransmission characteristics of a TCP socket if required.</span></span>
<span data-ttu-id="b1387-187">Si vous utilisez cette option, une application doit fournir des valeurs appropriées avant de démarrer une tentative de connexion TCP sur le Socket.</span><span class="sxs-lookup"><span data-stu-id="b1387-187">An application, if using this option, must supply suitable values before starting a TCP connection attempt on the socket.</span></span>

<span data-ttu-id="b1387-188">Le [**TCP_INITIAL_RTO_PARAMETERS**](/windows/desktop/api/mstcpip/ns-mstcpip-tcp_initial_rto_parameters) IOCTL permet à une application de configurer le délai de retransmission (SYN) initial (RTO) utilisé par le Socket.</span><span class="sxs-lookup"><span data-stu-id="b1387-188">The [**TCP_INITIAL_RTO_PARAMETERS**](/windows/desktop/api/mstcpip/ns-mstcpip-tcp_initial_rto_parameters) IOCTL allows an application to configure the initial (SYN) retransmission timeout (RTO) used by the socket.</span></span>

<span data-ttu-id="b1387-189">Un pointeur vers une structure [**TCP_INITIAL_RTO_PARAMETERS**](/windows/desktop/api/mstcpip/ns-mstcpip-tcp_initial_rto_parameters) passée dans le paramètre *lpvInBuffer* permet à une application de configurer la durée de boucle initiale (RTT) initiale utilisée pour calculer le délai de retransmission.</span><span class="sxs-lookup"><span data-stu-id="b1387-189">A pointer to a [**TCP_INITIAL_RTO_PARAMETERS**](/windows/desktop/api/mstcpip/ns-mstcpip-tcp_initial_rto_parameters) structure passed in the *lpvInBuffer* parameter allows an application to configure the initial round trip time (RTT) used to compute the retransmission timeout.</span></span>
<span data-ttu-id="b1387-190">L’application peut également configurer le nombre de retransmissions qui seront tentées avant que la tentative de connexion échoue.</span><span class="sxs-lookup"><span data-stu-id="b1387-190">The application can also configure the number of retransmissions that will be attempted before the connection attempt fails.</span></span>

## <a name="see-also"></a><span data-ttu-id="b1387-191">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b1387-191">See also</span></span>

[<span data-ttu-id="b1387-192">socle</span><span class="sxs-lookup"><span data-stu-id="b1387-192">socket</span></span>](/windows/desktop/api/winsock2/nf-winsock2-socket)

[<span data-ttu-id="b1387-193">**TCP_INITIAL_RTO_PARAMETERS**</span><span class="sxs-lookup"><span data-stu-id="b1387-193">**TCP_INITIAL_RTO_PARAMETERS**</span></span>](/windows/desktop/api/mstcpip/ns-mstcpip-tcp_initial_rto_parameters)

[<span data-ttu-id="b1387-194">**WSAGetLastError**</span><span class="sxs-lookup"><span data-stu-id="b1387-194">**WSAGetLastError**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetlasterror)

[<span data-ttu-id="b1387-195">**WSAGetOverlappedResult**</span><span class="sxs-lookup"><span data-stu-id="b1387-195">**WSAGetOverlappedResult**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[<span data-ttu-id="b1387-196">**WSAIoctl**</span><span class="sxs-lookup"><span data-stu-id="b1387-196">**WSAIoctl**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[<span data-ttu-id="b1387-197">**WSAOVERLAPPED**</span><span class="sxs-lookup"><span data-stu-id="b1387-197">**WSAOVERLAPPED**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[<span data-ttu-id="b1387-198">**WSASocketA**</span><span class="sxs-lookup"><span data-stu-id="b1387-198">**WSASocketA**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[<span data-ttu-id="b1387-199">**WSASocketW**</span><span class="sxs-lookup"><span data-stu-id="b1387-199">**WSASocketW**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
