---
description: Le code de contrôle acquiert une réservation d’exécution pour un bloc de ports TCP ou UDP.
ms.assetid: 1A2E3920-88D2-4109-B7EF-E66BD4AB6153
title: Code de contrôle SIO_ACQUIRE_PORT_RESERVATION
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 8eab53aeb945837b55c70560294b2fc295160a2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519633"
---
# <a name="sio_acquire_port_reservation-control-code"></a><span data-ttu-id="79ccb-103">Code de contrôle SIO_ACQUIRE_PORT_RESERVATION</span><span class="sxs-lookup"><span data-stu-id="79ccb-103">SIO_ACQUIRE_PORT_RESERVATION control code</span></span>

## <a name="description"></a><span data-ttu-id="79ccb-104">Description</span><span class="sxs-lookup"><span data-stu-id="79ccb-104">Description</span></span>

<span data-ttu-id="79ccb-105">Le code de contrôle de **\_ \_ \_ réservation de port SIO** acquiert une réservation d’exécution pour un bloc de ports TCP ou UDP.</span><span class="sxs-lookup"><span data-stu-id="79ccb-105">The **SIO\_ACQUIRE\_PORT\_RESERVATION** control code acquires a runtime reservation for a block of TCP or UDP ports.</span></span>

<span data-ttu-id="79ccb-106">Pour effectuer cette opération, appelez la fonction [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** avec les paramètres suivants.</span><span class="sxs-lookup"><span data-stu-id="79ccb-106">To perform this operation, call the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function with the following parameters.</span></span>

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_ACQUIRE_PORT_RESERVATION, // dwIoControlCode
  (LPVOID) lpvInBuffer,  // pointer to an INET_PORT_RANGE structure
  (DWORD) cbInBuffer,    // size, in bytes, of the input buffer
  (LPVOID) lpvOutBuffer,             // pointer to an INET_PORT_RESERVATION_INSTANCE structure
  (DWORD) cbOutBuffer,   // size, in bytes, of the output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

```cpp
int WSPIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_ACQUIRE_PORT_RESERVATION, // dwIoControlCode
  (LPVOID) lpvInBuffer,  // pointer to an INET_PORT_RANGE structure
  (DWORD) cbInBuffer,    // size, in bytes, of the input buffer
  (LPVOID) lpvOutBuffer,             // pointer to a INET_PORT_RESERVATION_INSTANCE structure
  (DWORD) cbOutBuffer,   // size, in bytes, of the output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
  (LPWSATHREADID) lpThreadId,   // a WSATHREADID structure
  (LPINT) lpErrno   // a pointer to the error code.
);
```

## <a name="parameters"></a><span data-ttu-id="79ccb-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="79ccb-107">Parameters</span></span>

### <a name="s"></a><span data-ttu-id="79ccb-108">s</span><span class="sxs-lookup"><span data-stu-id="79ccb-108">s</span></span>

<span data-ttu-id="79ccb-109">Descripteur identifiant un Socket.</span><span class="sxs-lookup"><span data-stu-id="79ccb-109">A descriptor identifying a socket.</span></span>

### <a name="dwiocontrolcode"></a><span data-ttu-id="79ccb-110">dwIoControlCode</span><span class="sxs-lookup"><span data-stu-id="79ccb-110">dwIoControlCode</span></span>

<span data-ttu-id="79ccb-111">Code de contrôle de l’opération.</span><span class="sxs-lookup"><span data-stu-id="79ccb-111">The control code for the operation.</span></span>
<span data-ttu-id="79ccb-112">Utilisez **SIO \_ Acquire \_ port \_ reservation**  pour cette opération.</span><span class="sxs-lookup"><span data-stu-id="79ccb-112">Use **SIO\_ACQUIRE\_PORT\_RESERVATION**  for this operation.</span></span>

### <a name="lpvinbuffer"></a><span data-ttu-id="79ccb-113">lpvInBuffer</span><span class="sxs-lookup"><span data-stu-id="79ccb-113">lpvInBuffer</span></span>

<span data-ttu-id="79ccb-114">Pointeur vers la mémoire tampon d’entrée.</span><span class="sxs-lookup"><span data-stu-id="79ccb-114">A pointer to the input buffer.</span></span>
<span data-ttu-id="79ccb-115">Ce paramètre contient un pointeur vers une structure de [**\_ \_ plage de ports inet**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_range) qui spécifie le numéro du point de départ et le nombre de ports à réserver.</span><span class="sxs-lookup"><span data-stu-id="79ccb-115">This parameter contains a pointer to an [**INET\_PORT\_RANGE**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_range) structure that specifies the starting point number and the number of ports to reserve.</span></span>

### <a name="cbinbuffer"></a><span data-ttu-id="79ccb-116">cbInBuffer</span><span class="sxs-lookup"><span data-stu-id="79ccb-116">cbInBuffer</span></span>

<span data-ttu-id="79ccb-117">Taille, en octets, de la mémoire tampon d’entrée.</span><span class="sxs-lookup"><span data-stu-id="79ccb-117">The size, in bytes, of the input buffer.</span></span>
<span data-ttu-id="79ccb-118">Ce paramètre doit correspondre à la taille de la structure de l' [**\_ \_ étendue du port inet**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_range) .</span><span class="sxs-lookup"><span data-stu-id="79ccb-118">This parameter should be the size of the [**INET\_PORT\_RANGE**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_range) structure.</span></span>

### <a name="lpvoutbuffer"></a><span data-ttu-id="79ccb-119">lpvOutBuffer</span><span class="sxs-lookup"><span data-stu-id="79ccb-119">lpvOutBuffer</span></span>

<span data-ttu-id="79ccb-120">Pointeur vers la mémoire tampon de sortie.</span><span class="sxs-lookup"><span data-stu-id="79ccb-120">A pointer to the output buffer.</span></span>
<span data-ttu-id="79ccb-121">En cas de sortie réussie, ce paramètre contient un pointeur vers une structure d' [**\_ instance de \_ réservation \_ de port inet**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_reservation_instance) .</span><span class="sxs-lookup"><span data-stu-id="79ccb-121">On successful output, this parameter contains a pointer to an [**INET\_PORT\_RESERVATION\_INSTANCE**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_reservation_instance) structure.</span></span>

### <a name="cboutbuffer"></a><span data-ttu-id="79ccb-122">cbOutBuffer</span><span class="sxs-lookup"><span data-stu-id="79ccb-122">cbOutBuffer</span></span>

<span data-ttu-id="79ccb-123">Taille, en octets, de la mémoire tampon de sortie.</span><span class="sxs-lookup"><span data-stu-id="79ccb-123">The size, in bytes, of the output buffer.</span></span>
<span data-ttu-id="79ccb-124">Ce paramètre doit avoir au moins la taille de la structure de l' [**\_ instance de \_ réservation \_ du port inet**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_reservation_instance) .</span><span class="sxs-lookup"><span data-stu-id="79ccb-124">This parameter must be at least the size of the [**INET\_PORT\_RESERVATION\_INSTANCE**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_reservation_instance) structure.</span></span>

### <a name="lpcbbytesreturned"></a><span data-ttu-id="79ccb-125">lpcbBytesReturned</span><span class="sxs-lookup"><span data-stu-id="79ccb-125">lpcbBytesReturned</span></span>

<span data-ttu-id="79ccb-126">Pointeur vers une variable qui reçoit la taille, en octets, des données stockées dans la mémoire tampon de sortie.</span><span class="sxs-lookup"><span data-stu-id="79ccb-126">A pointer to a variable that receives the size, in bytes, of the data stored in the output buffer.</span></span>

<span data-ttu-id="79ccb-127">Si la mémoire tampon de sortie est trop petite, l’appel échoue, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) retourne [**WSAEINVAL**](windows-sockets-error-codes-2.md)et le paramètre *LpcbBytesReturned* pointe vers une valeur **DWORD** égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="79ccb-127">If the output buffer is too small, the call fails, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) returns [**WSAEINVAL**](windows-sockets-error-codes-2.md), and the *lpcbBytesReturned* parameter points to a **DWORD** value of zero.</span></span>

<span data-ttu-id="79ccb-128">Si *lpOverlapped* a la valeur **null**, la valeur **DWORD** vers laquelle pointe le paramètre *lpcbBytesReturned* retourné sur un appel réussi ne peut pas être égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="79ccb-128">If *lpOverlapped* is **NULL**, the **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned on a successful call cannot be zero.</span></span>

<span data-ttu-id="79ccb-129">Si le paramètre *lpOverlapped* n’a pas la **valeur null** pour les sockets superposés, les opérations qui ne peuvent pas être terminées immédiatement seront lancées et l’achèvement sera indiqué ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="79ccb-129">If the *lpOverlapped* parameter is not **NULL** for overlapped sockets, operations that cannot be completed immediately will be initiated, and completion will be indicated at a later time.</span></span>
<span data-ttu-id="79ccb-130">La valeur **DWORD** pointée par le paramètre *lpcbBytesReturned* retourné peut être égale à zéro, car la taille des données stockées ne peut pas être déterminée tant que l’opération avec chevauchement n’est pas terminée.</span><span class="sxs-lookup"><span data-stu-id="79ccb-130">The **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned may be zero since the size of the data stored can't be determined until the overlapped operation has completed.</span></span>
<span data-ttu-id="79ccb-131">L’état d’achèvement final peut être récupéré lorsque la méthode d’achèvement appropriée est signalée lorsque l’opération est terminée.</span><span class="sxs-lookup"><span data-stu-id="79ccb-131">The final completion status can be retrieved when the appropriate completion method is signaled when the operation has completed.</span></span>

### <a name="lpvoverlapped"></a><span data-ttu-id="79ccb-132">lpvOverlapped</span><span class="sxs-lookup"><span data-stu-id="79ccb-132">lpvOverlapped</span></span>

<span data-ttu-id="79ccb-133">Pointeur vers une structure [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) .</span><span class="sxs-lookup"><span data-stu-id="79ccb-133">A pointer to a [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="79ccb-134">Si le socket *s* a été créé sans l’attribut Overlapped, le paramètre *lpOverlapped* est ignoré.</span><span class="sxs-lookup"><span data-stu-id="79ccb-134">If socket *s* was created without the overlapped attribute, the *lpOverlapped* parameter is ignored.</span></span>

<span data-ttu-id="79ccb-135">Si *s* a été ouvert avec l’attribut Overlapped et que le paramètre *lpOverlapped* n’a pas la **valeur null**, l’opération est exécutée en tant qu’opération Overlapped (asynchrone).</span><span class="sxs-lookup"><span data-stu-id="79ccb-135">If *s* was opened with the overlapped attribute and the *lpOverlapped* parameter is not **NULL**, the operation is performed as an overlapped (asynchronous) operation.</span></span>
<span data-ttu-id="79ccb-136">Dans ce cas, le paramètre *lpOverlapped* doit pointer vers une structure [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) valide.</span><span class="sxs-lookup"><span data-stu-id="79ccb-136">In this case, *lpOverlapped* parameter must point to a valid [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="79ccb-137">Pour les opérations avec chevauchement, la fonction [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** retourne immédiatement, et la méthode d’achèvement appropriée est signalée lorsque l’opération est terminée.</span><span class="sxs-lookup"><span data-stu-id="79ccb-137">For overlapped operations, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns immediately, and the appropriate completion method is signaled when the operation has been completed.</span></span>
<span data-ttu-id="79ccb-138">Sinon, la fonction ne retourne pas jusqu’à ce que l’opération soit terminée ou qu’une erreur se produise.</span><span class="sxs-lookup"><span data-stu-id="79ccb-138">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

### <a name="lpcompletionroutine"></a><span data-ttu-id="79ccb-139">lpCompletionRoutine</span><span class="sxs-lookup"><span data-stu-id="79ccb-139">lpCompletionRoutine</span></span>

<span data-ttu-id="79ccb-140">Type : \_ In_opt \_ [ **LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span><span class="sxs-lookup"><span data-stu-id="79ccb-140">Type: \_In_opt\_ [**LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span></span>

<span data-ttu-id="79ccb-141">Pointeur vers la routine de saisie semi-automatique appelée lorsque l’opération est terminée (ignoré pour les sockets non superposés).</span><span class="sxs-lookup"><span data-stu-id="79ccb-141">A pointer to the completion routine called when the operation has been completed (ignored for non-overlapped sockets).</span></span>

### <a name="lpthreadid"></a><span data-ttu-id="79ccb-142">lpThreadId</span><span class="sxs-lookup"><span data-stu-id="79ccb-142">lpThreadId</span></span>

<span data-ttu-id="79ccb-143">Pointeur vers une structure [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) qui doit être utilisée par le fournisseur dans un appel ultérieur à **WPUQueueApc**.</span><span class="sxs-lookup"><span data-stu-id="79ccb-143">A pointer to a [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure to be used by the provider in a subsequent call to **WPUQueueApc**.</span></span>
<span data-ttu-id="79ccb-144">Le fournisseur doit stocker la structure [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) référencée (pas le pointeur vers le même) jusqu’à ce que la fonction **WPUQueueApc** soit retournée.</span><span class="sxs-lookup"><span data-stu-id="79ccb-144">The provider should store the referenced [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure (not the pointer to same) until after the **WPUQueueApc** function returns.</span></span>

<span data-ttu-id="79ccb-145">**Remarque**  Ce paramètre s’applique uniquement à la fonction **WSPIoctl** .</span><span class="sxs-lookup"><span data-stu-id="79ccb-145">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

### <a name="lperrno"></a><span data-ttu-id="79ccb-146">lpErrno</span><span class="sxs-lookup"><span data-stu-id="79ccb-146">lpErrno</span></span>

<span data-ttu-id="79ccb-147">Pointeur vers le code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="79ccb-147">A pointer to the error code.</span></span>

<span data-ttu-id="79ccb-148">**Remarque**  Ce paramètre s’applique uniquement à la fonction **WSPIoctl** .</span><span class="sxs-lookup"><span data-stu-id="79ccb-148">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

## <a name="return-value"></a><span data-ttu-id="79ccb-149">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="79ccb-149">Return value</span></span>

<span data-ttu-id="79ccb-150">Si l’opération se termine correctement, la fonction [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** retourne la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="79ccb-150">If the operation completes successfully, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns zero.</span></span>

<span data-ttu-id="79ccb-151">Si l’opération échoue ou est en attente, la fonction [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** retourne une **\_ erreur de socket**.</span><span class="sxs-lookup"><span data-stu-id="79ccb-151">If the operation fails or is pending, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns **SOCKET\_ERROR**.</span></span>
<span data-ttu-id="79ccb-152">Pour afficher les informations d’erreur étendues, appelez [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span><span class="sxs-lookup"><span data-stu-id="79ccb-152">To get extended error information, call [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>

| <span data-ttu-id="79ccb-153">Code d'erreur</span><span class="sxs-lookup"><span data-stu-id="79ccb-153">Error code</span></span> | <span data-ttu-id="79ccb-154">Signification</span><span class="sxs-lookup"><span data-stu-id="79ccb-154">Meaning</span></span> |
|------------|---------|
|<span data-ttu-id="79ccb-155">**\_e/s WSA \_ en attente**</span><span class="sxs-lookup"><span data-stu-id="79ccb-155">**WSA\_IO\_PENDING**</span></span> | <span data-ttu-id="79ccb-156">L’opération d’e/s avec chevauchement est en cours.</span><span class="sxs-lookup"><span data-stu-id="79ccb-156">Overlapped I/O operation is in progress.</span></span> <span data-ttu-id="79ccb-157">Cette valeur est retournée si une opération avec chevauchement a été correctement initiée et que son achèvement sera indiqué ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="79ccb-157">This value is returned if an overlapped operation was successfully initiated and completion will be indicated at a later time.</span></span> |
| <span data-ttu-id="79ccb-158">**\_opération WSA \_ abandonnée**</span><span class="sxs-lookup"><span data-stu-id="79ccb-158">**WSA\_OPERATION\_ABORTED**</span></span> | <span data-ttu-id="79ccb-159">L’opération d’e/s a été annulée en raison de la sortie d’un thread ou d’une demande de l’application.</span><span class="sxs-lookup"><span data-stu-id="79ccb-159">The I/O operation has been aborted because of either a thread exit or an application request.</span></span> <span data-ttu-id="79ccb-160">Cette erreur est retournée si une opération avec chevauchement a été annulée en raison de la fermeture du socket ou de l’exécution de la commande **SIO \_ flush** ioctl.</span><span class="sxs-lookup"><span data-stu-id="79ccb-160">This error is returned if an overlapped operation was canceled due to the closure of the socket or the execution of the **SIO\_FLUSH** IOCTL command.</span></span> |
| <span data-ttu-id="79ccb-161">**WSAEFAULT**</span><span class="sxs-lookup"><span data-stu-id="79ccb-161">**WSAEFAULT**</span></span> | <span data-ttu-id="79ccb-162">Le système a détecté une adresse de pointeur non valide lors de la tentative d’utilisation d’un argument de pointeur dans un appel.</span><span class="sxs-lookup"><span data-stu-id="79ccb-162">The system detected an invalid pointer address in attempting to use a pointer argument in a call.</span></span> <span data-ttu-id="79ccb-163">Cette erreur est retournée par le paramètre *lpvInBuffer*, *lpvoutBuffer*, *lpcbBytesReturned*, *lpOverlapped* ou *lpCompletionRoutine* n’est pas entièrement contenu dans une partie valide de l’espace d’adressage de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="79ccb-163">This error is returned of the *lpvInBuffer*, *lpvoutBuffer*, *lpcbBytesReturned*, *lpOverlapped* or *lpCompletionRoutine* parameter is not totally contained in a valid part of the user address space.</span></span> |
| <span data-ttu-id="79ccb-164">**WSAEINPROGRESS**</span><span class="sxs-lookup"><span data-stu-id="79ccb-164">**WSAEINPROGRESS**</span></span> | <span data-ttu-id="79ccb-165">Une opération de blocage est actuellement en cours d'exécution.</span><span class="sxs-lookup"><span data-stu-id="79ccb-165">A blocking operation is currently executing.</span></span> <span data-ttu-id="79ccb-166">Cette erreur est retournée si la fonction est appelée lorsqu’un rappel est en cours.</span><span class="sxs-lookup"><span data-stu-id="79ccb-166">This error is returned if the function is invoked when a callback is in progress.</span></span> |
| <span data-ttu-id="79ccb-167">**WSAEINTR**</span><span class="sxs-lookup"><span data-stu-id="79ccb-167">**WSAEINTR**</span></span> | <span data-ttu-id="79ccb-168">Une opération de blocage a été interrompue par un appel à [**WSACancelBlockingCall**](/windows/desktop/api/winsock2/nf-winsock2-wsacancelblockingcall).</span><span class="sxs-lookup"><span data-stu-id="79ccb-168">A blocking operation was interrupted by a call to [**WSACancelBlockingCall**](/windows/desktop/api/winsock2/nf-winsock2-wsacancelblockingcall).</span></span> <span data-ttu-id="79ccb-169">Cette erreur est retournée si une opération de blocage a été interrompue.</span><span class="sxs-lookup"><span data-stu-id="79ccb-169">This error is returned if a blocking operation was interrupted.</span></span> |
| <span data-ttu-id="79ccb-170">**WSAEINVAL**</span><span class="sxs-lookup"><span data-stu-id="79ccb-170">**WSAEINVAL**</span></span> | <span data-ttu-id="79ccb-171">Argument non valide fourni.</span><span class="sxs-lookup"><span data-stu-id="79ccb-171">An invalid argument was supplied.</span></span> <span data-ttu-id="79ccb-172">Cette erreur est retournée si le paramètre *dwIoControlCode* n’est pas une commande valide, si un paramètre d’entrée spécifié n’est pas acceptable ou si la commande n’est pas applicable au type de socket spécifié.</span><span class="sxs-lookup"><span data-stu-id="79ccb-172">This error is returned if the *dwIoControlCode* parameter is not a valid command, or a specified input parameter is not acceptable, or the command is not applicable to the type of socket specified.</span></span> |
| <span data-ttu-id="79ccb-173">**WSAENETDOWN**</span><span class="sxs-lookup"><span data-stu-id="79ccb-173">**WSAENETDOWN**</span></span> | <span data-ttu-id="79ccb-174">Une opération de socket a rencontré un réseau inactif.</span><span class="sxs-lookup"><span data-stu-id="79ccb-174">A socket operation encountered a dead network.</span></span> <span data-ttu-id="79ccb-175">Cette erreur est retournée si le sous-système réseau a échoué.</span><span class="sxs-lookup"><span data-stu-id="79ccb-175">This error is returned if the network subsystem has failed.</span></span> |
| <span data-ttu-id="79ccb-176">**WSAENOTSOCK**</span><span class="sxs-lookup"><span data-stu-id="79ccb-176">**WSAENOTSOCK**</span></span> | <span data-ttu-id="79ccb-177">Une opération a été tentée sur un qui n’est pas un Socket.</span><span class="sxs-lookup"><span data-stu-id="79ccb-177">An operation was attempted on something that is not a socket.</span></span> <span data-ttu-id="79ccb-178">Cette erreur est retournée si le *descripteur* n’est pas un Socket.</span><span class="sxs-lookup"><span data-stu-id="79ccb-178">This error is returned if the descriptor *s* is not a socket.</span></span> |
| <span data-ttu-id="79ccb-179">**WSAEOPNOTSUPP**</span><span class="sxs-lookup"><span data-stu-id="79ccb-179">**WSAEOPNOTSUPP**</span></span> | <span data-ttu-id="79ccb-180">L’opération tentée n’est pas prise en charge pour le type d’objet référencé.</span><span class="sxs-lookup"><span data-stu-id="79ccb-180">The attempted operation is not supported for the type of object referenced.</span></span> <span data-ttu-id="79ccb-181">Cette erreur est retournée si la commande IOCTL spécifiée n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="79ccb-181">This error is returned if the specified IOCTL command is not supported.</span></span> <span data-ttu-id="79ccb-182">Cette erreur est également retournée si l’IOCTL **SIO \_ Acquire \_ port \_ reservation** n’est pas prise en charge par le fournisseur de transport.</span><span class="sxs-lookup"><span data-stu-id="79ccb-182">This error is also returned if the **SIO\_ACQUIRE\_PORT\_RESERVATION** IOCTL is not supported by the transport provider.</span></span> <span data-ttu-id="79ccb-183">Cette erreur est également retournée quand une tentative d’utilisation de l’IOCTL de **\_ réservation de \_ port \_ SIO Acquire** est effectuée sur un socket autre que UDP ou TCP.</span><span class="sxs-lookup"><span data-stu-id="79ccb-183">This error is also returned when an attempt to use the **SIO\_ACQUIRE\_PORT\_RESERVATION** IOCTL is made on a socket other than UDP or TCP.</span></span> |

## <a name="remarks"></a><span data-ttu-id="79ccb-184">Notes</span><span class="sxs-lookup"><span data-stu-id="79ccb-184">Remarks</span></span>

<span data-ttu-id="79ccb-185">L’IOCTL **SIO \_ Acquire \_ port \_ reservation**  est prise en charge sur Windows Vista et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="79ccb-185">The **SIO\_ACQUIRE\_PORT\_RESERVATION**  IOCTL is supported on Windows Vista and later versions of the operating system.</span></span>

<span data-ttu-id="79ccb-186">Les applications et les services qui doivent réserver des ports sont répartis en deux catégories.</span><span class="sxs-lookup"><span data-stu-id="79ccb-186">Applications and services which need to reserve ports fall into two categories.</span></span>
<span data-ttu-id="79ccb-187">La première catégorie comprend des composants qui ont besoin d’un port particulier dans le cadre de leur fonctionnement.</span><span class="sxs-lookup"><span data-stu-id="79ccb-187">The first category includes components which need a particular port as part of their operation.</span></span>
<span data-ttu-id="79ccb-188">De tels composants préfèrent généralement spécifier le port requis au moment de l’installation (dans un manifeste d’application, par exemple).</span><span class="sxs-lookup"><span data-stu-id="79ccb-188">Such components will generally prefer to specify their required port at installation time (in an application manifest, for example).</span></span>
<span data-ttu-id="79ccb-189">La deuxième catégorie comprend des composants qui ont besoin d’un port ou d’un bloc de ports disponibles au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="79ccb-189">The second category includes components which need any available port or block of ports at runtime.</span></span>
<span data-ttu-id="79ccb-190">Ces deux catégories correspondent à des demandes de réservation de port génériques et spécifiques.</span><span class="sxs-lookup"><span data-stu-id="79ccb-190">These two categories correspond to specific and wildcard port reservation requests.</span></span>
<span data-ttu-id="79ccb-191">Les demandes de réservation spécifiques peuvent être persistantes ou d’exécution, tandis que les demandes de réservation de port génériques sont uniquement prises en charge au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="79ccb-191">Specific reservation requests may be persistent or runtime, while wildcard port reservation requests are only supported at runtime.</span></span>

<span data-ttu-id="79ccb-192">L’IOCTL **SIO \_ Acquire \_ port \_ reservation**  est utilisée pour demander une réservation d’exécution pour un bloc de ports TCP ou UDP.</span><span class="sxs-lookup"><span data-stu-id="79ccb-192">The **SIO\_ACQUIRE\_PORT\_RESERVATION**  IOCTL is used to request a runtime reservation for a block of TCP or UDP ports.</span></span>
<span data-ttu-id="79ccb-193">Pour les réservations de port d’exécution, le pool de ports requiert que les réservations soient consommées à partir du processus sur lequel la réservation a été accordée.</span><span class="sxs-lookup"><span data-stu-id="79ccb-193">For runtime port reservations, the port pool requires that reservations be consumed from the process on whose socket the reservation was granted.</span></span>
<span data-ttu-id="79ccb-194">Les réservations de port d’exécution durent uniquement tant que la durée de vie du socket sur lequel l’IOCTL **SIO \_ Acquire \_ port \_ reservation**  a été appelée.</span><span class="sxs-lookup"><span data-stu-id="79ccb-194">Runtime port reservations last only as long as the lifetime of the socket on which the **SIO\_ACQUIRE\_PORT\_RESERVATION**  IOCTL was called.</span></span>
<span data-ttu-id="79ccb-195">En revanche, les réservations de port persistantes créées à l’aide de la fonction [**CreatePersistentTcpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistenttcpportreservation) ou [**CreatePersistentUdpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistentudpportreservation) peuvent être consommées par n’importe quel processus ayant la possibilité d’obtenir des réservations persistantes.</span><span class="sxs-lookup"><span data-stu-id="79ccb-195">In contrast, persistent port reservations created using the [**CreatePersistentTcpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistenttcpportreservation) or [**CreatePersistentUdpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistentudpportreservation) function may be consumed by any process with the ability to obtain persistent reservations.</span></span>

<span data-ttu-id="79ccb-196">Une fois qu’une réservation de port TCP ou UDP du runtime a été obtenue, une application peut demander des affectations de port à partir de la réservation de port en ouvrant un socket TCP ou UDP, puis en appelant la fonction [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) en spécifiant l’IOCTL de [**réservation de \_ \_ port \_ SIO Associate**](sio-associate-port-reservation.md) et en passant le jeton de réservation avant d’émettre un appel à la fonction de liaison sur le Socket.</span><span class="sxs-lookup"><span data-stu-id="79ccb-196">Once a runtime TCP or UDP port reservation has been obtained, an application can request port assignments from the port reservation by opening a TCP or UDP socket, then calling the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) function specifying the [**SIO\_ASSOCIATE\_PORT\_RESERVATION**](sio-associate-port-reservation.md) IOCTL and passing the reservation token before issuing a call to the bind function on the socket.</span></span>

<span data-ttu-id="79ccb-197">Si les deux paramètres *lpOverlapped* et *lpCompletionRoutine* sont **null**, le socket dans cette fonction sera traité comme un socket non superposé.</span><span class="sxs-lookup"><span data-stu-id="79ccb-197">If both *lpOverlapped* and *lpCompletionRoutine* parameters are **NULL**, the socket in this function will be treated as a non-overlapped socket.</span></span>
<span data-ttu-id="79ccb-198">Pour un socket non superposé, les paramètres *lpOverlapped* et *lpCompletionRoutine* sont ignorés, sauf que la fonction peut se bloquer si le socket *s* est en mode blocage.</span><span class="sxs-lookup"><span data-stu-id="79ccb-198">For a non-overlapped socket, *lpOverlapped* and *lpCompletionRoutine* parameters are ignored, except that the function can block if socket *s* is in blocking mode.</span></span>
<span data-ttu-id="79ccb-199">Si le socket *s* est en mode non bloquant, cette fonction sera toujours bloquée, car cette IOCTL particulière ne prend pas en charge le mode non bloquant.</span><span class="sxs-lookup"><span data-stu-id="79ccb-199">If socket *s* is in non-blocking mode, this function will still block since this particular IOCTL does not support non-blocking mode.</span></span>

<span data-ttu-id="79ccb-200">Pour les sockets superposés, les opérations qui ne peuvent pas être terminées immédiatement sont lancées et l’achèvement est indiqué ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="79ccb-200">For overlapped sockets, operations that cannot be completed immediately will be initiated, and completion will be indicated at a later time.</span></span>

<span data-ttu-id="79ccb-201">Toute IOCTL peut se bloquer indéfiniment, en fonction de l’implémentation du fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="79ccb-201">Any IOCTL may block indefinitely, depending on the service provider's implementation.</span></span>
<span data-ttu-id="79ccb-202">Si l’application ne peut pas tolérer le blocage dans un appel de fonction WSAIoctl ou **WSPIoctl** , les e/s avec chevauchement sont conseillées pour les IOCTL qui sont particulièrement susceptibles de se bloquer.</span><span class="sxs-lookup"><span data-stu-id="79ccb-202">If the application cannot tolerate blocking in a WSAIoctl or **WSPIoctl** function call, overlapped I/O would be advised for IOCTLs that are especially likely to block.</span></span>

<span data-ttu-id="79ccb-203">L’IOCTL de **\_ réservation de \_ port \_ SIO Acquire**  peut échouer avec l’opération **WSAEINTR** ou **WSA \_ \_ abandonnée** dans les cas suivants :</span><span class="sxs-lookup"><span data-stu-id="79ccb-203">The **SIO\_ACQUIRE\_PORT\_RESERVATION**  IOCTL can fail with **WSAEINTR** or **WSA\_OPERATION\_ABORTED** under the following cases:</span></span>

* <span data-ttu-id="79ccb-204">La demande est annulée par le gestionnaire d’e/s.</span><span class="sxs-lookup"><span data-stu-id="79ccb-204">The request is canceled by the I/O Manager.</span></span>
* <span data-ttu-id="79ccb-205">Le socket est fermé.</span><span class="sxs-lookup"><span data-stu-id="79ccb-205">The socket is closed.</span></span>

## <a name="examples"></a><span data-ttu-id="79ccb-206">Exemples</span><span class="sxs-lookup"><span data-stu-id="79ccb-206">Examples</span></span>

<span data-ttu-id="79ccb-207">L’exemple suivant acquiert une réservation de port d’exécution, puis crée un socket et alloue un port à partir de la réservation du port d’exécution pour le socket, puis ferme le socket et libère la réservation du port d’exécution.</span><span class="sxs-lookup"><span data-stu-id="79ccb-207">The following example acquires a runtime port reservation, then creates a socket and allocates a port from the runtime port reservation for the socket, and then closes the socket and the releases the runtime port reservation.</span></span>

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

    // Note that the sockaddr_in struct works only with AF_INET not AF_INET6
    // An application needs to use the sockaddr_in6 for AF_INET6
    sockaddr_in service;
    sockaddr_in sockName;
    int nameLen = sizeof (sockName);

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

            sockRes = socket(iFamily, iType, iProtocol);
            if (sockRes == INVALID_SOCKET) {
                wprintf(L"socket function for second socket failed with error = %d\n",
                        WSAGetLastError());
                closesocket(sock);
                WSACleanup();
                return 1;
            } else {
                wprintf(L"socket function for second socket succeeded\n");

                iResult =
                    WSAIoctl(sock, SIO_ASSOCIATE_PORT_RESERVATION,
                             (LPVOID) & portRes.Token, sizeof (ULONG64), NULL, 0,
                             &bytesReturned, NULL, NULL);
                if (iResult != 0) {
                    wprintf
                        (L"WSAIoctl(SIO_ASSOCIATE_PORT_RESERVATION) failed with error = %d\n",
                         WSAGetLastError());
                } else {
                    wprintf
                        (L"WSAIoctl(SIO_ASSOCIATE_PORT_RESERVATION) succeeded, bytesReturned = %u\n",
                         bytesReturned);

                    service.sin_family = (ADDRESS_FAMILY) iFamily;
                    service.sin_addr.s_addr = INADDR_ANY;
                    service.sin_port = 0;

                    iResult = bind(sock, (SOCKADDR *) & service, sizeof (service));
                    if (iResult == SOCKET_ERROR)
                        wprintf(L"bind failed with error = %d\n", WSAGetLastError());
                    else {
                        wprintf(L"bind succeeded\n");
                        iResult = getsockname(sock, (SOCKADDR *) & sockName, &nameLen);
                        if (iResult == SOCKET_ERROR)
                            wprintf(L"getsockname failed with error = %d\n",
                                    WSAGetLastError());
                        else {
                            wprintf(L"getsockname succeeded\n");
                            wprintf(L"Port number allocated = %u\n",
                                    ntohs(sockName.sin_port));
                        }
                    }
                }
            }

            // comment out this block of code if you don't want to delete the reservation just created
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

        if (sockRes != INVALID_SOCKET) {
            iResult = closesocket(sockRes);
            if (iResult == SOCKET_ERROR) {
                wprintf(L"closesocket for second socket failed with error = %d\n",
                        WSAGetLastError());
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

## <a name="see-also"></a><span data-ttu-id="79ccb-208">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="79ccb-208">See also</span></span>

[<span data-ttu-id="79ccb-209">**accepter**</span><span class="sxs-lookup"><span data-stu-id="79ccb-209">**accept**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-accept)

[<span data-ttu-id="79ccb-210">**établis**</span><span class="sxs-lookup"><span data-stu-id="79ccb-210">**bind**</span></span>](/windows/desktop/api/winsock/nf-winsock-bind)

[<span data-ttu-id="79ccb-211">**CreatePersistentTcpPortReservation**</span><span class="sxs-lookup"><span data-stu-id="79ccb-211">**CreatePersistentTcpPortReservation**</span></span>](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistenttcpportreservation)

[<span data-ttu-id="79ccb-212">**CreatePersistentUdpPortReservation**</span><span class="sxs-lookup"><span data-stu-id="79ccb-212">**CreatePersistentUdpPortReservation**</span></span>](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistentudpportreservation)

[<span data-ttu-id="79ccb-213">**DeletePersistentTcpPortReservation**</span><span class="sxs-lookup"><span data-stu-id="79ccb-213">**DeletePersistentTcpPortReservation**</span></span>](/windows/desktop/api/iphlpapi/nf-iphlpapi-deletepersistenttcpportreservation)

[<span data-ttu-id="79ccb-214">**DeletePersistentUdpPortReservation**</span><span class="sxs-lookup"><span data-stu-id="79ccb-214">**DeletePersistentUdpPortReservation**</span></span>](/windows/desktop/api/iphlpapi/nf-iphlpapi-deletepersistentudpportreservation)

[<span data-ttu-id="79ccb-215">**\_étendue du port inet \_**</span><span class="sxs-lookup"><span data-stu-id="79ccb-215">**INET\_PORT\_RANGE**</span></span>](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_range)

[<span data-ttu-id="79ccb-216">**\_instance de \_ réservation de port inet \_**</span><span class="sxs-lookup"><span data-stu-id="79ccb-216">**INET\_PORT\_RESERVATION\_INSTANCE**</span></span>](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_reservation_instance)

[<span data-ttu-id="79ccb-217">**LookupPersistentTcpPortReservation**</span><span class="sxs-lookup"><span data-stu-id="79ccb-217">**LookupPersistentTcpPortReservation**</span></span>](/windows/desktop/api/iphlpapi/nf-iphlpapi-lookuppersistenttcpportreservation)

[<span data-ttu-id="79ccb-218">**LookupPersistentUdpPortReservation**</span><span class="sxs-lookup"><span data-stu-id="79ccb-218">**LookupPersistentUdpPortReservation**</span></span>](/windows/desktop/api/iphlpapi/nf-iphlpapi-lookuppersistentudpportreservation)

[<span data-ttu-id="79ccb-219">**\_réservation de \_ port SIO Associate \_**</span><span class="sxs-lookup"><span data-stu-id="79ccb-219">**SIO\_ASSOCIATE\_PORT\_RESERVATION**</span></span>](sio-associate-port-reservation.md)

[<span data-ttu-id="79ccb-220">**\_réservation de \_ port de libération SIO \_**</span><span class="sxs-lookup"><span data-stu-id="79ccb-220">**SIO\_RELEASE\_PORT\_RESERVATION**</span></span>](sio-release-port-reservation.md)

[<span data-ttu-id="79ccb-221">**socle**</span><span class="sxs-lookup"><span data-stu-id="79ccb-221">**socket**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-socket)

[<span data-ttu-id="79ccb-222">**WSAGetLastError**</span><span class="sxs-lookup"><span data-stu-id="79ccb-222">**WSAGetLastError**</span></span>](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)

[<span data-ttu-id="79ccb-223">**WSAGetOverlappedResult**</span><span class="sxs-lookup"><span data-stu-id="79ccb-223">**WSAGetOverlappedResult**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[<span data-ttu-id="79ccb-224">**WSAIoctl**</span><span class="sxs-lookup"><span data-stu-id="79ccb-224">**WSAIoctl**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[<span data-ttu-id="79ccb-225">**WSAOVERLAPPED**</span><span class="sxs-lookup"><span data-stu-id="79ccb-225">**WSAOVERLAPPED**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[<span data-ttu-id="79ccb-226">**WSASocketA**</span><span class="sxs-lookup"><span data-stu-id="79ccb-226">**WSASocketA**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[<span data-ttu-id="79ccb-227">**WSASocketW**</span><span class="sxs-lookup"><span data-stu-id="79ccb-227">**WSASocketW**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
