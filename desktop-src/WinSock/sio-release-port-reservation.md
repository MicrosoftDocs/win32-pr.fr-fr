---
description: Le code de contrôle libère une réservation d’exécution pour un bloc de ports TCP ou UDP.
ms.assetid: 24D67A40-8CE9-4AF1-90BF-599D19C87B89
title: Code de contrôle SIO_RELEASE_PORT_RESERVATION
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 57f96d0396d661eba12f9e64238c492f38e97b2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106543108"
---
# <a name="sio_release_port_reservation-control-code"></a><span data-ttu-id="d5e34-103">Code de contrôle SIO_RELEASE_PORT_RESERVATION</span><span class="sxs-lookup"><span data-stu-id="d5e34-103">SIO_RELEASE_PORT_RESERVATION Control Code</span></span>

## <a name="description"></a><span data-ttu-id="d5e34-104">Description</span><span class="sxs-lookup"><span data-stu-id="d5e34-104">Description</span></span>

<span data-ttu-id="d5e34-105">Le code de contrôle de **\_ réservation du \_ port \_** de la version de SiO libère une réservation d’exécution pour un bloc de ports TCP ou UDP.</span><span class="sxs-lookup"><span data-stu-id="d5e34-105">The **SIO\_RELEASE\_PORT\_RESERVATION** control code releases a runtime reservation for a block of TCP or UDP ports.</span></span>
<span data-ttu-id="d5e34-106">La réservation d’exécution à libérer doit avoir été obtenue à partir du processus d’émission à l’aide du [**SIO_ACQUIRE_PORT_RESERVATION**](sio-acquire-port-reservation.md) ioctl.</span><span class="sxs-lookup"><span data-stu-id="d5e34-106">The runtime reservation to be released must have been obtained from the issuing process using the [**SIO_ACQUIRE_PORT_RESERVATION**](sio-acquire-port-reservation.md) IOCTL.</span></span>

<span data-ttu-id="d5e34-107">Pour effectuer cette opération, appelez la fonction [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** avec les paramètres suivants.</span><span class="sxs-lookup"><span data-stu-id="d5e34-107">To perform this operation, call the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function with the following parameters.</span></span>

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_RELEASE_PORT_RESERVATION, // dwIoControlCode
  (LPVOID) lpvInBuffer,  // pointer to a INET_PORT_RESERVATION_TOKEN structure
  (DWORD) cbInBuffer,    // size, in bytes, of the input buffer
  NULL,           // lpvOutBuffer is a pointer to the output buffer
  0,              // cbOutBuffer is the size, in bytes, of the output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);

```

```cpp
int WSPIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_RELEASE_PORT_RESERVATION, // dwIoControlCode
  (LPVOID) lpvInBuffer,  // pointer to a INET_PORT_RESERVATION_TOKEN structure
  (DWORD) cbInBuffer,    // size, in bytes, of the input buffer
  NULL,           // lpvOutBuffer is a pointer to the output buffer
  0,              // cbOutBuffer is the size, in bytes, of the output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
  (LPWSATHREADID) lpThreadId,   // a WSATHREADID structure
  (LPINT) lpErrno   // a pointer to the error code.
);
```

## <a name="parameters"></a><span data-ttu-id="d5e34-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d5e34-108">Parameters</span></span>

### <a name="s"></a><span data-ttu-id="d5e34-109">s</span><span class="sxs-lookup"><span data-stu-id="d5e34-109">s</span></span>

<span data-ttu-id="d5e34-110">Descripteur identifiant un Socket.</span><span class="sxs-lookup"><span data-stu-id="d5e34-110">A descriptor identifying a socket.</span></span>

### <a name="dwiocontrolcode"></a><span data-ttu-id="d5e34-111">dwIoControlCode</span><span class="sxs-lookup"><span data-stu-id="d5e34-111">dwIoControlCode</span></span>

<span data-ttu-id="d5e34-112">Code de contrôle de l’opération.</span><span class="sxs-lookup"><span data-stu-id="d5e34-112">The control code for the operation.</span></span>
<span data-ttu-id="d5e34-113">Utilisez **la \_ \_ \_ réservation de port de libération SIO** pour cette opération.</span><span class="sxs-lookup"><span data-stu-id="d5e34-113">Use **SIO\_RELEASE\_PORT\_RESERVATION** for this operation.</span></span>

### <a name="lpvinbuffer"></a><span data-ttu-id="d5e34-114">lpvInBuffer</span><span class="sxs-lookup"><span data-stu-id="d5e34-114">lpvInBuffer</span></span>

<span data-ttu-id="d5e34-115">Pointeur vers la mémoire tampon d’entrée.</span><span class="sxs-lookup"><span data-stu-id="d5e34-115">A pointer to the input buffer.</span></span>
<span data-ttu-id="d5e34-116">Ce paramètre contient un pointeur vers une structure [**INET_PORT_RESERVATION_TOKEN**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_reservation_token) avec le jeton de la réservation de port TCP ou UDP à libérer.</span><span class="sxs-lookup"><span data-stu-id="d5e34-116">This parameter contains a pointer to an [**INET_PORT_RESERVATION_TOKEN**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_reservation_token) structure with the token for the TCP or UDP port reservation to release.</span></span>

### <a name="cbinbuffer"></a><span data-ttu-id="d5e34-117">cbInBuffer</span><span class="sxs-lookup"><span data-stu-id="d5e34-117">cbInBuffer</span></span>

<span data-ttu-id="d5e34-118">Taille, en octets, de la mémoire tampon d’entrée.</span><span class="sxs-lookup"><span data-stu-id="d5e34-118">The size, in bytes, of the input buffer.</span></span>
<span data-ttu-id="d5e34-119">Ce paramètre doit avoir au moins la taille de la structure [**INET_PORT_RESERVATION_TOKEN**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_reservation_token) .</span><span class="sxs-lookup"><span data-stu-id="d5e34-119">This parameter must be at least the size of the [**INET_PORT_RESERVATION_TOKEN**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_reservation_token) structure.</span></span>

### <a name="lpvoutbuffer"></a><span data-ttu-id="d5e34-120">lpvOutBuffer</span><span class="sxs-lookup"><span data-stu-id="d5e34-120">lpvOutBuffer</span></span>

<span data-ttu-id="d5e34-121">Pointeur vers la mémoire tampon de sortie.</span><span class="sxs-lookup"><span data-stu-id="d5e34-121">A pointer to the output buffer.</span></span>
<span data-ttu-id="d5e34-122">Ce paramètre n’est pas utilisé pour cette opération.</span><span class="sxs-lookup"><span data-stu-id="d5e34-122">This parameter is unused for this operation.</span></span>

### <a name="cboutbuffer"></a><span data-ttu-id="d5e34-123">cbOutBuffer</span><span class="sxs-lookup"><span data-stu-id="d5e34-123">cbOutBuffer</span></span>

<span data-ttu-id="d5e34-124">Taille, en octets, de la mémoire tampon de sortie.</span><span class="sxs-lookup"><span data-stu-id="d5e34-124">The size, in bytes, of the output buffer.</span></span>
<span data-ttu-id="d5e34-125">Ce paramètre doit avoir la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="d5e34-125">This parameter must be set to zero.</span></span>

### <a name="lpcbbytesreturned"></a><span data-ttu-id="d5e34-126">lpcbBytesReturned</span><span class="sxs-lookup"><span data-stu-id="d5e34-126">lpcbBytesReturned</span></span>

<span data-ttu-id="d5e34-127">Pointeur vers une variable qui reçoit la taille, en octets, des données stockées dans la mémoire tampon de sortie.</span><span class="sxs-lookup"><span data-stu-id="d5e34-127">A pointer to a variable that receives the size, in bytes, of the data stored in the output buffer.</span></span>

<span data-ttu-id="d5e34-128">Si la mémoire tampon de sortie est trop petite, l’appel échoue, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) retourne [**WSAEINVAL**](windows-sockets-error-codes-2.md)et le paramètre *LpcbBytesReturned* pointe vers une valeur **DWORD** égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="d5e34-128">If the output buffer is too small, the call fails, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) returns [**WSAEINVAL**](windows-sockets-error-codes-2.md), and the *lpcbBytesReturned* parameter points to a **DWORD** value of zero.</span></span>

<span data-ttu-id="d5e34-129">Si *lpOverlapped* a la valeur **null**, la valeur **DWORD** vers laquelle pointe le paramètre *lpcbBytesReturned* retourné sur un appel réussi ne peut pas être égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="d5e34-129">If *lpOverlapped* is **NULL**, the **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned on a successful call cannot be zero.</span></span>

<span data-ttu-id="d5e34-130">Si le paramètre *lpOverlapped* n’a pas la **valeur null** pour les sockets superposés, les opérations qui ne peuvent pas être terminées immédiatement seront lancées et l’achèvement sera indiqué ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="d5e34-130">If the *lpOverlapped* parameter is not **NULL** for overlapped sockets, operations that cannot be completed immediately will be initiated, and completion will be indicated at a later time.</span></span>
<span data-ttu-id="d5e34-131">La valeur **DWORD** pointée par le paramètre *lpcbBytesReturned* retourné peut être égale à zéro, car la taille des données stockées ne peut pas être déterminée tant que l’opération avec chevauchement n’est pas terminée.</span><span class="sxs-lookup"><span data-stu-id="d5e34-131">The **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned may be zero since the size of the data stored can't be determined until the overlapped operation has completed.</span></span>
<span data-ttu-id="d5e34-132">L’état d’achèvement final peut être récupéré lorsque la méthode d’achèvement appropriée est signalée lorsque l’opération est terminée.</span><span class="sxs-lookup"><span data-stu-id="d5e34-132">The final completion status can be retrieved when the appropriate completion method is signaled when the operation has completed.</span></span>

### <a name="lpvoverlapped"></a><span data-ttu-id="d5e34-133">lpvOverlapped</span><span class="sxs-lookup"><span data-stu-id="d5e34-133">lpvOverlapped</span></span>

<span data-ttu-id="d5e34-134">Pointeur vers une structure [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) .</span><span class="sxs-lookup"><span data-stu-id="d5e34-134">A pointer to a [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="d5e34-135">Si le socket *s* a été créé sans l’attribut Overlapped, le paramètre *lpOverlapped* est ignoré.</span><span class="sxs-lookup"><span data-stu-id="d5e34-135">If socket *s* was created without the overlapped attribute, the *lpOverlapped* parameter is ignored.</span></span>

<span data-ttu-id="d5e34-136">Si *s* a été ouvert avec l’attribut Overlapped et que le paramètre *lpOverlapped* n’a pas la **valeur null**, l’opération est exécutée en tant qu’opération Overlapped (asynchrone).</span><span class="sxs-lookup"><span data-stu-id="d5e34-136">If *s* was opened with the overlapped attribute and the *lpOverlapped* parameter is not **NULL**, the operation is performed as an overlapped (asynchronous) operation.</span></span>
<span data-ttu-id="d5e34-137">Dans ce cas, le paramètre *lpOverlapped* doit pointer vers une structure [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) valide.</span><span class="sxs-lookup"><span data-stu-id="d5e34-137">In this case, *lpOverlapped* parameter must point to a valid [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="d5e34-138">Pour les opérations avec chevauchement, la fonction [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** retourne immédiatement, et la méthode d’achèvement appropriée est signalée lorsque l’opération est terminée.</span><span class="sxs-lookup"><span data-stu-id="d5e34-138">For overlapped operations, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns immediately, and the appropriate completion method is signaled when the operation has been completed.</span></span>
<span data-ttu-id="d5e34-139">Sinon, la fonction ne retourne pas jusqu’à ce que l’opération soit terminée ou qu’une erreur se produise.</span><span class="sxs-lookup"><span data-stu-id="d5e34-139">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

### <a name="lpcompletionroutine"></a><span data-ttu-id="d5e34-140">lpCompletionRoutine</span><span class="sxs-lookup"><span data-stu-id="d5e34-140">lpCompletionRoutine</span></span>

<span data-ttu-id="d5e34-141">Type : \_ In_opt \_ [ **LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span><span class="sxs-lookup"><span data-stu-id="d5e34-141">Type: \_In_opt\_ [**LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span></span>

<span data-ttu-id="d5e34-142">Pointeur vers la routine de saisie semi-automatique appelée lorsque l’opération est terminée (ignoré pour les sockets non superposés).</span><span class="sxs-lookup"><span data-stu-id="d5e34-142">A pointer to the completion routine called when the operation has been completed (ignored for non-overlapped sockets).</span></span>

### <a name="lpthreadid"></a><span data-ttu-id="d5e34-143">lpThreadId</span><span class="sxs-lookup"><span data-stu-id="d5e34-143">lpThreadId</span></span>

<span data-ttu-id="d5e34-144">Pointeur vers une structure [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) qui doit être utilisée par le fournisseur dans un appel ultérieur à [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc).</span><span class="sxs-lookup"><span data-stu-id="d5e34-144">A pointer to a [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure to be used by the provider in a subsequent call to [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc).</span></span>
<span data-ttu-id="d5e34-145">Le fournisseur doit stocker la structure [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) référencée (pas le pointeur vers le même) jusqu’à ce que la fonction [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) soit retournée.</span><span class="sxs-lookup"><span data-stu-id="d5e34-145">The provider should store the referenced [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure (not the pointer to same) until after the [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) function returns.</span></span>

<span data-ttu-id="d5e34-146">**Remarque**  Ce paramètre s’applique uniquement à la fonction **WSPIoctl** .</span><span class="sxs-lookup"><span data-stu-id="d5e34-146">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

### <a name="lperrno"></a><span data-ttu-id="d5e34-147">lpErrno</span><span class="sxs-lookup"><span data-stu-id="d5e34-147">lpErrno</span></span>

<span data-ttu-id="d5e34-148">Pointeur vers le code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="d5e34-148">A pointer to the error code.</span></span>

<span data-ttu-id="d5e34-149">**Remarque**  Ce paramètre s’applique uniquement à la fonction **WSPIoctl** .</span><span class="sxs-lookup"><span data-stu-id="d5e34-149">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

## <a name="return-value"></a><span data-ttu-id="d5e34-150">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d5e34-150">Return value</span></span>

<span data-ttu-id="d5e34-151">Si l’opération se termine correctement, la fonction [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** retourne la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="d5e34-151">If the operation completes successfully, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns zero.</span></span>

<span data-ttu-id="d5e34-152">Si l’opération échoue ou est en attente, la fonction [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** retourne une **\_ erreur de socket**.</span><span class="sxs-lookup"><span data-stu-id="d5e34-152">If the operation fails or is pending, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns **SOCKET\_ERROR**.</span></span>
<span data-ttu-id="d5e34-153">Pour afficher les informations d’erreur étendues, appelez [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span><span class="sxs-lookup"><span data-stu-id="d5e34-153">To get extended error information, call [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>

| <span data-ttu-id="d5e34-154">Code d'erreur</span><span class="sxs-lookup"><span data-stu-id="d5e34-154">Error code</span></span> | <span data-ttu-id="d5e34-155">Signification</span><span class="sxs-lookup"><span data-stu-id="d5e34-155">Meaning</span></span> |
|------------|---------|
| <span data-ttu-id="d5e34-156">**\_e/s WSA \_ en attente**</span><span class="sxs-lookup"><span data-stu-id="d5e34-156">**WSA\_IO\_PENDING**</span></span> | <span data-ttu-id="d5e34-157">L’opération d’e/s avec chevauchement est en cours.</span><span class="sxs-lookup"><span data-stu-id="d5e34-157">Overlapped I/O operation is in progress.</span></span> <span data-ttu-id="d5e34-158">Cette valeur est retournée si une opération avec chevauchement a été correctement initiée et que son achèvement sera indiqué ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="d5e34-158">This value is returned if an overlapped operation was successfully initiated and completion will be indicated at a later time.</span></span> |
| <span data-ttu-id="d5e34-159">**\_opération WSA \_ abandonnée**</span><span class="sxs-lookup"><span data-stu-id="d5e34-159">**WSA\_OPERATION\_ABORTED**</span></span> | <span data-ttu-id="d5e34-160">L’opération d’e/s a été annulée en raison de la sortie d’un thread ou d’une demande de l’application.</span><span class="sxs-lookup"><span data-stu-id="d5e34-160">The I/O operation has been aborted because of either a thread exit or an application request.</span></span> <span data-ttu-id="d5e34-161">Cette erreur est retournée si une opération avec chevauchement a été annulée en raison de la fermeture du socket ou de l’exécution de la commande **SIO_FLUSH** ioctl.</span><span class="sxs-lookup"><span data-stu-id="d5e34-161">This error is returned if an overlapped operation was canceled due to the closure of the socket or the execution of the **SIO_FLUSH** IOCTL command.</span></span> |
| <span data-ttu-id="d5e34-162">**WSAEFAULT**</span><span class="sxs-lookup"><span data-stu-id="d5e34-162">**WSAEFAULT**</span></span> | <span data-ttu-id="d5e34-163">Le système a détecté une adresse de pointeur non valide lors de la tentative d’utilisation d’un argument de pointeur dans un appel.</span><span class="sxs-lookup"><span data-stu-id="d5e34-163">The system detected an invalid pointer address in attempting to use a pointer argument in a call.</span></span> <span data-ttu-id="d5e34-164">Cette erreur renvoyée par le paramètre *lpOverlapped* ou *lpCompletionRoutine* n’est pas entièrement contenue dans une partie valide de l’espace d’adressage de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="d5e34-164">This error is returned of the *lpOverlapped* or *lpCompletionRoutine* parameter is not totally contained in a valid part of the user address space.</span></span> |
| <span data-ttu-id="d5e34-165">**WSAEINPROGRESS**</span><span class="sxs-lookup"><span data-stu-id="d5e34-165">**WSAEINPROGRESS**</span></span> | <span data-ttu-id="d5e34-166">Une opération de blocage est actuellement en cours d'exécution.</span><span class="sxs-lookup"><span data-stu-id="d5e34-166">A blocking operation is currently executing.</span></span> <span data-ttu-id="d5e34-167">Cette erreur est retournée si la fonction est appelée lorsqu’un rappel est en cours.</span><span class="sxs-lookup"><span data-stu-id="d5e34-167">This error is returned if the function is invoked when a callback is in progress.</span></span> |
| <span data-ttu-id="d5e34-168">**WSAEINTR**</span><span class="sxs-lookup"><span data-stu-id="d5e34-168">**WSAEINTR**</span></span> | <span data-ttu-id="d5e34-169">Une opération de blocage a été interrompue par un appel à **WSACancelBlockingCall**.</span><span class="sxs-lookup"><span data-stu-id="d5e34-169">A blocking operation was interrupted by a call to **WSACancelBlockingCall**.</span></span> <span data-ttu-id="d5e34-170">Cette erreur est retournée si une opération de blocage a été interrompue.</span><span class="sxs-lookup"><span data-stu-id="d5e34-170">This error is returned if a blocking operation was interrupted.</span></span> |
| <span data-ttu-id="d5e34-171">**WSAEINVAL**</span><span class="sxs-lookup"><span data-stu-id="d5e34-171">**WSAEINVAL**</span></span> | <span data-ttu-id="d5e34-172">Argument non valide fourni.</span><span class="sxs-lookup"><span data-stu-id="d5e34-172">An invalid argument was supplied.</span></span> <span data-ttu-id="d5e34-173">Cette erreur est retournée si le paramètre *dwIoControlCode* n’est pas une commande valide, si un paramètre d’entrée spécifié n’est pas acceptable ou si la commande n’est pas applicable au type de socket spécifié.</span><span class="sxs-lookup"><span data-stu-id="d5e34-173">This error is returned if the *dwIoControlCode* parameter is not a valid command, or a specified input parameter is not acceptable, or the command is not applicable to the type of socket specified.</span></span> |
| <span data-ttu-id="d5e34-174">**WSAENETDOWN**</span><span class="sxs-lookup"><span data-stu-id="d5e34-174">**WSAENETDOWN**</span></span> | <span data-ttu-id="d5e34-175">Une opération de socket a rencontré un réseau inactif.</span><span class="sxs-lookup"><span data-stu-id="d5e34-175">A socket operation encountered a dead network.</span></span> <span data-ttu-id="d5e34-176">Cette erreur est retournée si le sous-système réseau a échoué.</span><span class="sxs-lookup"><span data-stu-id="d5e34-176">This error is returned if the network subsystem has failed.</span></span> |
| <span data-ttu-id="d5e34-177">**WSAENOTSOCK**</span><span class="sxs-lookup"><span data-stu-id="d5e34-177">**WSAENOTSOCK**</span></span> | <span data-ttu-id="d5e34-178">Une opération a été tentée sur un qui n’est pas un Socket.</span><span class="sxs-lookup"><span data-stu-id="d5e34-178">An operation was attempted on something that is not a socket.</span></span> <span data-ttu-id="d5e34-179">Cette erreur est retournée si le *descripteur* n’est pas un Socket.</span><span class="sxs-lookup"><span data-stu-id="d5e34-179">This error is returned if the descriptor *s* is not a socket.</span></span> |
| <span data-ttu-id="d5e34-180">**WSAEOPNOTSUPP**</span><span class="sxs-lookup"><span data-stu-id="d5e34-180">**WSAEOPNOTSUPP**</span></span> | <span data-ttu-id="d5e34-181">L’opération tentée n’est pas prise en charge pour le type d’objet référencé.</span><span class="sxs-lookup"><span data-stu-id="d5e34-181">The attempted operation is not supported for the type of object referenced.</span></span> <span data-ttu-id="d5e34-182">Cette erreur est retournée si la commande IOCTL spécifiée n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="d5e34-182">This error is returned if the specified IOCTL command is not supported.</span></span> <span data-ttu-id="d5e34-183">Cette erreur est également retournée si l’IOCTL de réservation de port de la **\_ version \_ \_ SIO** n’est pas prise en charge par le fournisseur de transport.</span><span class="sxs-lookup"><span data-stu-id="d5e34-183">This error is also returned if the **SIO\_RELEASE\_PORT\_RESERVATION** IOCTL is not supported by the transport provider.</span></span> <span data-ttu-id="d5e34-184">Cette erreur est également retournée lorsqu’une tentative d’utilisation de l’IOCTL de **\_ réservation de \_ port \_ de libération SIO** est effectuée sur un socket autre que UDP ou TCP.</span><span class="sxs-lookup"><span data-stu-id="d5e34-184">This error is also returned when an attempt to use the **SIO\_RELEASE\_PORT\_RESERVATION** IOCTL is made on a socket other than UDP or TCP.</span></span> |

## <a name="remarks"></a><span data-ttu-id="d5e34-185">Notes</span><span class="sxs-lookup"><span data-stu-id="d5e34-185">Remarks</span></span>

<span data-ttu-id="d5e34-186">L’IOCTL de réservation de port de la **\_ version \_ \_ SIO** est prise en charge sur Windows Vista et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="d5e34-186">The **SIO\_RELEASE\_PORT\_RESERVATION** IOCTL is supported on Windows Vista and later versions of the operating system.</span></span>

<span data-ttu-id="d5e34-187">Les applications et les services qui doivent réserver des ports sont répartis en deux catégories.</span><span class="sxs-lookup"><span data-stu-id="d5e34-187">Applications and services which need to reserve ports fall into two categories.</span></span>
<span data-ttu-id="d5e34-188">La première catégorie comprend des composants qui ont besoin d’un port particulier dans le cadre de leur fonctionnement.</span><span class="sxs-lookup"><span data-stu-id="d5e34-188">The first category includes components which need a particular port as part of their operation.</span></span>
<span data-ttu-id="d5e34-189">De tels composants préfèrent généralement spécifier le port requis au moment de l’installation (dans un manifeste d’application, par exemple).</span><span class="sxs-lookup"><span data-stu-id="d5e34-189">Such components will generally prefer to specify their required port at installation time (in an application manifest, for example).</span></span>
<span data-ttu-id="d5e34-190">La deuxième catégorie comprend des composants qui ont besoin d’un port ou d’un bloc de ports disponibles au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="d5e34-190">The second category includes components which need any available port or block of ports at runtime.</span></span>
<span data-ttu-id="d5e34-191">Ces deux catégories correspondent à des demandes de réservation de port génériques et spécifiques.</span><span class="sxs-lookup"><span data-stu-id="d5e34-191">These two categories correspond to specific and wildcard port reservation requests.</span></span>
<span data-ttu-id="d5e34-192">Les demandes de réservation spécifiques peuvent être persistantes ou d’exécution, tandis que les demandes de réservation de port génériques sont uniquement prises en charge au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="d5e34-192">Specific reservation requests may be persistent or runtime, while wildcard port reservation requests are only supported at runtime.</span></span>

<span data-ttu-id="d5e34-193">Le [**SIO_ACQUIRE_PORT_RESERVATION**](sio-acquire-port-reservation.md) IOCTL est utilisé pour demander une réservation au moment de l’exécution pour un bloc de ports TCP ou UDP.</span><span class="sxs-lookup"><span data-stu-id="d5e34-193">The [**SIO_ACQUIRE_PORT_RESERVATION**](sio-acquire-port-reservation.md) IOCTL is used to request a runtime reservation for a block of TCP or UDP ports.</span></span>
<span data-ttu-id="d5e34-194">Pour les réservations de port d’exécution, le pool de ports requiert que les réservations soient consommées à partir du processus sur lequel la réservation a été accordée.</span><span class="sxs-lookup"><span data-stu-id="d5e34-194">For runtime port reservations, the port pool requires that reservations be consumed from the process on whose socket the reservation was granted.</span></span>
<span data-ttu-id="d5e34-195">Les réservations de port d’exécution durent uniquement tant que la durée de vie du socket sur lequel la [**SIO_ACQUIRE_PORT_RESERVATION**](sio-acquire-port-reservation.md) IOCTL a été appelée.</span><span class="sxs-lookup"><span data-stu-id="d5e34-195">Runtime port reservations last only as long as the lifetime of the socket on which the [**SIO_ACQUIRE_PORT_RESERVATION**](sio-acquire-port-reservation.md) IOCTL was called.</span></span>
<span data-ttu-id="d5e34-196">En revanche, les réservations de port persistantes créées à l’aide de la fonction [**CreatePersistentTcpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistenttcpportreservation) ou [**CreatePersistentUdpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistentudpportreservation) peuvent être consommées par n’importe quel processus ayant la possibilité d’obtenir des réservations persistantes.</span><span class="sxs-lookup"><span data-stu-id="d5e34-196">In contrast, persistent port reservations created using the [**CreatePersistentTcpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistenttcpportreservation) or [**CreatePersistentUdpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistentudpportreservation) function may be consumed by any process with the ability to obtain persistent reservations.</span></span>

<span data-ttu-id="d5e34-197">L’IOCTL de réservation de port de la **\_ version \_ \_ SIO** est utilisée pour libérer une réservation d’exécution pour un bloc de ports TCP ou UDP.</span><span class="sxs-lookup"><span data-stu-id="d5e34-197">The **SIO\_RELEASE\_PORT\_RESERVATION** IOCTL is used to release a runtime reservation for a block of TCP or UDP ports.</span></span>

<span data-ttu-id="d5e34-198">Si les deux paramètres *lpOverlapped* et *lpCompletionRoutine* sont **null**, le socket dans cette fonction sera traité comme un socket non superposé.</span><span class="sxs-lookup"><span data-stu-id="d5e34-198">If both *lpOverlapped* and *lpCompletionRoutine* parameters are **NULL**, the socket in this function will be treated as a non-overlapped socket.</span></span>
<span data-ttu-id="d5e34-199">Pour un socket non superposé, les paramètres *lpOverlapped* et *lpCompletionRoutine* sont ignorés, sauf que la fonction peut se bloquer si le socket *s* est en mode blocage.</span><span class="sxs-lookup"><span data-stu-id="d5e34-199">For a non-overlapped socket, *lpOverlapped* and *lpCompletionRoutine* parameters are ignored, except that the function can block if socket *s* is in blocking mode.</span></span>
<span data-ttu-id="d5e34-200">Si le socket *s* est en mode non bloquant, cette fonction sera toujours bloquée, car cette IOCTL particulière ne prend pas en charge le mode non bloquant.</span><span class="sxs-lookup"><span data-stu-id="d5e34-200">If socket *s* is in non-blocking mode, this function will still block since this particular IOCTL does not support non-blocking mode.</span></span>

<span data-ttu-id="d5e34-201">Pour les sockets superposés, les opérations qui ne peuvent pas être terminées immédiatement sont lancées et l’achèvement est indiqué ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="d5e34-201">For overlapped sockets, operations that cannot be completed immediately will be initiated, and completion will be indicated at a later time.</span></span>

<span data-ttu-id="d5e34-202">Toute IOCTL peut se bloquer indéfiniment, en fonction de l’implémentation du fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="d5e34-202">Any IOCTL may block indefinitely, depending on the service provider's implementation.</span></span>
<span data-ttu-id="d5e34-203">Si l’application ne peut pas tolérer le blocage dans un appel de fonction [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** , les e/s avec chevauchement sont conseillées pour les IOCTL qui sont particulièrement susceptibles de se bloquer.</span><span class="sxs-lookup"><span data-stu-id="d5e34-203">If the application cannot tolerate blocking in a [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function call, overlapped I/O would be advised for IOCTLs that are especially likely to block.</span></span>

<span data-ttu-id="d5e34-204">L’IOCTL de **réservation de \_ port de libération \_ \_ SIO** peut échouer avec l’opération **WSAEINTR** ou **WSA \_ \_ abandonnée** dans les cas suivants :</span><span class="sxs-lookup"><span data-stu-id="d5e34-204">The **SIO\_RELEASE\_PORT\_RESERVATION** IOCTL can fail with **WSAEINTR** or **WSA\_OPERATION\_ABORTED** under the following cases:</span></span>

* <span data-ttu-id="d5e34-205">La demande est annulée par le gestionnaire d’e/s.</span><span class="sxs-lookup"><span data-stu-id="d5e34-205">The request is canceled by the I/O Manager.</span></span>
* <span data-ttu-id="d5e34-206">Le socket est fermé.</span><span class="sxs-lookup"><span data-stu-id="d5e34-206">The socket is closed.</span></span>

## <a name="examples"></a><span data-ttu-id="d5e34-207">Exemples</span><span class="sxs-lookup"><span data-stu-id="d5e34-207">Examples</span></span>

<span data-ttu-id="d5e34-208">L’exemple suivant acquiert une réservation de port d’exécution, puis libère la réservation de port d’exécution.</span><span class="sxs-lookup"><span data-stu-id="d5e34-208">The following example acquires a runtime port reservation and then releases the runtime port reservation.</span></span>

```cpp
#ifndef UNICODE
#define UNICODE
#endif

#ifndef WIN32_LEAN_AND_MEAN
#define WIN32_LEAN_AND_MEAN
#endif

#include <Windows.h.>
#include <winsock2.h>
#include <mstcpip.h>
#include <ws2ipdef.h>
#include <stdio.h>
#include <stdlib.h>

// Need to link with Ws2_32.lib for Winsock functions
#pragma comment(lib, "ws2_32.lib")

int wmain(int argc, WCHAR ** argv)
{

    // Declare and initialize variables

    int startPort = 0;          // host byte order
    int numPorts = 0;
    USHORT startPortns = 0;     // Network byte order

    INET_PORT_RANGE portRange = { 0 };
    INET_PORT_RESERVATION_INSTANCE portRes = { 0 };

    unsigned long status = 0;

    WSADATA wsaData = { 0 };
    int iResult = 0;

    SOCKET sock = INVALID_SOCKET;
    int iFamily = AF_INET;
    int iType = 0;
    int iProtocol = 0;

    SOCKET sockRes = INVALID_SOCKET;

    DWORD bytesReturned = 0;

    // Validate the parameters
    if (argc != 6) {
        wprintf
            (L"usage: %s <addressfamily> <type> <protocol> <StartingPort> <NumberOfPorts>\n",
             argv[0]);
        wprintf(L"Opens a socket for the specified family, type, & protocol\n");
        wprintf
            (L"and then acquires a runtime port reservation for the protocol specified\n");
        wprintf(L"%ws example usage\n", argv[0]);
        wprintf(L"   %ws 2 2 17 5000 20\n", argv[0]);
        wprintf(L"   where AF_INET=2 SOCK_DGRAM=2 IPPROTO_UDP=17 StartPort=5000 NumPorts=20", argv[0]);

        return 1;
    }

    iFamily = _wtoi(argv[1]);
    iType = _wtoi(argv[2]);
    iProtocol = _wtoi(argv[3]);

    startPort = _wtoi(argv[4]);
    if (startPort < 0 || startPort > 65535) {
        wprintf(L"Starting point must be either 0 or between 1 and 65,535\n");
        return 1;
    }
    startPortns = htons((USHORT) startPort);

    numPorts = _wtoi(argv[5]);
    if (numPorts < 0) {
        wprintf(L"Number of ports must be a positive number\n");
        return 1;
    }

    portRange.StartPort = startPortns;
    portRange.NumberOfPorts = (USHORT) numPorts;

    // Initialize Winsock
    iResult = WSAStartup(MAKEWORD(2, 2), &wsaData);
    if (iResult != 0) {
        wprintf(L"WSAStartup failed with error = %d\n", iResult);
        return 1;
    }

    sock = socket(iFamily, iType, iProtocol);
    if (sock == INVALID_SOCKET) {
        wprintf(L"socket function failed with error = %d\n", WSAGetLastError());
        WSACleanup();
        return 1;
    } else {
        wprintf(L"socket function succeeded\n");

        iResult =
            WSAIoctl(sock, SIO_ACQUIRE_PORT_RESERVATION, (LPVOID) & portRange,
                     sizeof (INET_PORT_RANGE), (LPVOID) & portRes,
                     sizeof (INET_PORT_RESERVATION_INSTANCE), &bytesReturned, NULL, NULL);
        if (iResult != 0) {
            wprintf(L"WSAIoctl(SIO_ACQUIRE_PORT_RESERVATION) failed with error = %d\n",
                    WSAGetLastError());
            closesocket(sock);
            WSACleanup();
            return 1;
        } else {
            wprintf
                (L"WSAIoctl(SIO_ACQUIRE_PORT_RESERVATION) succeeded, bytesReturned = %u\n",
                 bytesReturned);
            wprintf(L"  Starting port=%d,  Number of Ports=%d, Token=%I64d\n",
                    htons(portRes.Reservation.StartPort),
                    portRes.Reservation.NumberOfPorts, portRes.Token);

            iResult =
                WSAIoctl(sock, SIO_RELEASE_PORT_RESERVATION, (LPVOID) & portRes.Token,
                         sizeof (ULONG64), NULL, 0, &bytesReturned, NULL, NULL);
            if (iResult != 0) {
                wprintf
                    (L"WSAIoctl(SIO_RELEASE_PORT_RESERVATION) failed with error = %d\n",
                     WSAGetLastError());
            } else {
                wprintf
                    (L"WSAIoctl(SIO_RELEASE_PORT_RESERVATION) succeeded, bytesReturned = %u\n",
                     bytesReturned);
            }
        }

        if (sock != INVALID_SOCKET) {
            iResult = closesocket(sock);
            if (iResult == SOCKET_ERROR) {
                wprintf(L"closesocket for first socket failed with error = %d\n",
                        WSAGetLastError());
            }
        }
    }

    WSACleanup();

    return 0;
}
```

## <a name="see-also"></a><span data-ttu-id="d5e34-209">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d5e34-209">See also</span></span>

[<span data-ttu-id="d5e34-210">**CreatePersistentTcpPortReservation**</span><span class="sxs-lookup"><span data-stu-id="d5e34-210">**CreatePersistentTcpPortReservation**</span></span>](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistenttcpportreservation)

[<span data-ttu-id="d5e34-211">**CreatePersistentUdpPortReservation**</span><span class="sxs-lookup"><span data-stu-id="d5e34-211">**CreatePersistentUdpPortReservation**</span></span>](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistentudpportreservation)

[<span data-ttu-id="d5e34-212">**DeletePersistentTcpPortReservation**</span><span class="sxs-lookup"><span data-stu-id="d5e34-212">**DeletePersistentTcpPortReservation**</span></span>](/windows/desktop/api/iphlpapi/nf-iphlpapi-deletepersistenttcpportreservation)

[<span data-ttu-id="d5e34-213">**DeletePersistentUdpPortReservation**</span><span class="sxs-lookup"><span data-stu-id="d5e34-213">**DeletePersistentUdpPortReservation**</span></span>](/windows/desktop/api/iphlpapi/nf-iphlpapi-deletepersistentudpportreservation)

[<span data-ttu-id="d5e34-214">**INET_PORT_RESERVATION_TOKEN**</span><span class="sxs-lookup"><span data-stu-id="d5e34-214">**INET_PORT_RESERVATION_TOKEN**</span></span>](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_reservation_token)

[<span data-ttu-id="d5e34-215">**LookupPersistentTcpPortReservation**</span><span class="sxs-lookup"><span data-stu-id="d5e34-215">**LookupPersistentTcpPortReservation**</span></span>](/windows/desktop/api/iphlpapi/nf-iphlpapi-lookuppersistenttcpportreservation)

[<span data-ttu-id="d5e34-216">**LookupPersistentUdpPortReservation**</span><span class="sxs-lookup"><span data-stu-id="d5e34-216">**LookupPersistentUdpPortReservation**</span></span>](/windows/desktop/api/iphlpapi/nf-iphlpapi-lookuppersistentudpportreservation)

[<span data-ttu-id="d5e34-217">**SIO_ACQUIRE_PORT_RESERVATION**</span><span class="sxs-lookup"><span data-stu-id="d5e34-217">**SIO_ACQUIRE_PORT_RESERVATION**</span></span>](sio-acquire-port-reservation.md)

[<span data-ttu-id="d5e34-218">**SIO_ASSOCIATE_PORT_RESERVATION**</span><span class="sxs-lookup"><span data-stu-id="d5e34-218">**SIO_ASSOCIATE_PORT_RESERVATION**</span></span>](sio-associate-port-reservation.md)

[<span data-ttu-id="d5e34-219">socle</span><span class="sxs-lookup"><span data-stu-id="d5e34-219">socket</span></span>](/windows/desktop/api/winsock2/nf-winsock2-socket)

[<span data-ttu-id="d5e34-220">**WSAGetLastError**</span><span class="sxs-lookup"><span data-stu-id="d5e34-220">**WSAGetLastError**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetlasterror)

[<span data-ttu-id="d5e34-221">**WSAGetOverlappedResult**</span><span class="sxs-lookup"><span data-stu-id="d5e34-221">**WSAGetOverlappedResult**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[<span data-ttu-id="d5e34-222">**WSAIoctl**</span><span class="sxs-lookup"><span data-stu-id="d5e34-222">**WSAIoctl**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[<span data-ttu-id="d5e34-223">**WSAOVERLAPPED**</span><span class="sxs-lookup"><span data-stu-id="d5e34-223">**WSAOVERLAPPED**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[<span data-ttu-id="d5e34-224">**WSASocketA**</span><span class="sxs-lookup"><span data-stu-id="d5e34-224">**WSASocketA**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[<span data-ttu-id="d5e34-225">**WSASocketW**</span><span class="sxs-lookup"><span data-stu-id="d5e34-225">**WSASocketW**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
