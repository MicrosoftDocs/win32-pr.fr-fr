---
description: Le code de contrôle associe un socket à une réservation persistante ou d’exécution pour un bloc de TCP ou UDP identifié par le jeton de réservation de port.
ms.assetid: 4CBFB5F8-1FA1-44BA-9932-6F0329A465CB
title: Code de contrôle SIO_ASSOCIATE_PORT_RESERVATION
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 69af4f396fabd32f948d7e43cbf348aa34fb1a9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104204125"
---
# <a name="sio_associate_port_reservation-control-code"></a><span data-ttu-id="1fb11-103">Code de contrôle SIO_ASSOCIATE_PORT_RESERVATION</span><span class="sxs-lookup"><span data-stu-id="1fb11-103">SIO_ASSOCIATE_PORT_RESERVATION Control Code</span></span>

## <a name="description"></a><span data-ttu-id="1fb11-104">Description</span><span class="sxs-lookup"><span data-stu-id="1fb11-104">Description</span></span>

<span data-ttu-id="1fb11-105">Le code de contrôle de **\_ réservation de \_ port \_ SIO Associate** associe un socket à une réservation persistante ou d’exécution pour un bloc de TCP ou UDP identifié par le jeton de réservation de port.</span><span class="sxs-lookup"><span data-stu-id="1fb11-105">The **SIO\_ASSOCIATE\_PORT\_RESERVATION** control code associates a socket with a persistent or runtime reservation for a block of TCP or UDP identified by the port reservation token.</span></span>
<span data-ttu-id="1fb11-106">Cette IOCTL doit être émise avant que le socket ne soit lié.</span><span class="sxs-lookup"><span data-stu-id="1fb11-106">This IOCTL must be issued before the socket is bound.</span></span>
<span data-ttu-id="1fb11-107">Si et quand le socket est lié, le port qui lui est assigné est sélectionné à partir de la réservation de port identifiée par le jeton donné.</span><span class="sxs-lookup"><span data-stu-id="1fb11-107">If and when the socket is bound, the port assigned to it will be selected from the port reservation identified by the given token.</span></span>
<span data-ttu-id="1fb11-108">Si aucun port n’est disponible à partir de la réservation spécifiée, l’appel de fonction de [**liaison**](/windows/desktop/api/winsock/nf-winsock-bind) échoue.</span><span class="sxs-lookup"><span data-stu-id="1fb11-108">If no ports are available from the specified reservation, the [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) function call will fail.</span></span>

<span data-ttu-id="1fb11-109">Pour effectuer cette opération, appelez la fonction [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** avec les paramètres suivants.</span><span class="sxs-lookup"><span data-stu-id="1fb11-109">To perform this operation, call the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function with the following parameters.</span></span>

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_ASSOCIATE_PORT_RESERVATION, // dwIoControlCode
  (LPVOID) lpvInBuffer,  // pointer to an INET_PORT_RESERVATION_TOKEN
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
  SIO_ASSOCIATE_PORT_RESERVATION, // dwIoControlCode
  (LPVOID) lpvInBuffer,  // pointer to an INET_PORT_RESERVATION_TOKEN
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

## <a name="parameters"></a><span data-ttu-id="1fb11-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1fb11-110">Parameters</span></span>

### <a name="s"></a><span data-ttu-id="1fb11-111">s</span><span class="sxs-lookup"><span data-stu-id="1fb11-111">s</span></span>

<span data-ttu-id="1fb11-112">Descripteur identifiant un Socket.</span><span class="sxs-lookup"><span data-stu-id="1fb11-112">A descriptor identifying a socket.</span></span>

### <a name="dwiocontrolcode"></a><span data-ttu-id="1fb11-113">dwIoControlCode</span><span class="sxs-lookup"><span data-stu-id="1fb11-113">dwIoControlCode</span></span>

<span data-ttu-id="1fb11-114">Code de contrôle de l’opération.</span><span class="sxs-lookup"><span data-stu-id="1fb11-114">The control code for the operation.</span></span>
<span data-ttu-id="1fb11-115">Utilisez **la \_ \_ \_ réservation de port SIO Associate** pour cette opération.</span><span class="sxs-lookup"><span data-stu-id="1fb11-115">Use **SIO\_ASSOCIATE\_PORT\_RESERVATION** for this operation.</span></span>

### <a name="lpvinbuffer"></a><span data-ttu-id="1fb11-116">lpvInBuffer</span><span class="sxs-lookup"><span data-stu-id="1fb11-116">lpvInBuffer</span></span>

<span data-ttu-id="1fb11-117">Pointeur vers la mémoire tampon d’entrée.</span><span class="sxs-lookup"><span data-stu-id="1fb11-117">A pointer to the input buffer.</span></span>
<span data-ttu-id="1fb11-118">Ce paramètre contient un pointeur vers une structure [**INET_PORT_RESERVATION_TOKEN**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_reservation_token) avec le jeton de la réservation de port TCP ou UDP à associer au socket.</span><span class="sxs-lookup"><span data-stu-id="1fb11-118">This parameter contains a pointer to an [**INET_PORT_RESERVATION_TOKEN**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_reservation_token) structure with the token for the TCP or UDP port reservation to associate with the socket.</span></span>

### <a name="cbinbuffer"></a><span data-ttu-id="1fb11-119">cbInBuffer</span><span class="sxs-lookup"><span data-stu-id="1fb11-119">cbInBuffer</span></span>

<span data-ttu-id="1fb11-120">Taille, en octets, de la mémoire tampon d’entrée.</span><span class="sxs-lookup"><span data-stu-id="1fb11-120">The size, in bytes, of the input buffer.</span></span>
<span data-ttu-id="1fb11-121">Ce paramètre doit avoir au moins la taille de la structure [**INET_PORT_RESERVATION_TOKEN**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_reservation_token) .</span><span class="sxs-lookup"><span data-stu-id="1fb11-121">This parameter must be at least the size of the [**INET_PORT_RESERVATION_TOKEN**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_reservation_token) structure.</span></span>

### <a name="lpvoutbuffer"></a><span data-ttu-id="1fb11-122">lpvOutBuffer</span><span class="sxs-lookup"><span data-stu-id="1fb11-122">lpvOutBuffer</span></span>

<span data-ttu-id="1fb11-123">Pointeur vers la mémoire tampon de sortie.</span><span class="sxs-lookup"><span data-stu-id="1fb11-123">A pointer to the output buffer.</span></span>
<span data-ttu-id="1fb11-124">Ce paramètre n’est pas utilisé pour cette opération.</span><span class="sxs-lookup"><span data-stu-id="1fb11-124">This parameter is unused for this operation.</span></span>

### <a name="cboutbuffer"></a><span data-ttu-id="1fb11-125">cbOutBuffer</span><span class="sxs-lookup"><span data-stu-id="1fb11-125">cbOutBuffer</span></span>

<span data-ttu-id="1fb11-126">Taille, en octets, de la mémoire tampon de sortie.</span><span class="sxs-lookup"><span data-stu-id="1fb11-126">The size, in bytes, of the output buffer.</span></span>
<span data-ttu-id="1fb11-127">Ce paramètre doit avoir la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="1fb11-127">This parameter must be set to zero.</span></span>

### <a name="lpcbbytesreturned"></a><span data-ttu-id="1fb11-128">lpcbBytesReturned</span><span class="sxs-lookup"><span data-stu-id="1fb11-128">lpcbBytesReturned</span></span>

<span data-ttu-id="1fb11-129">Pointeur vers une variable qui reçoit la taille, en octets, des données stockées dans la mémoire tampon de sortie.</span><span class="sxs-lookup"><span data-stu-id="1fb11-129">A pointer to a variable that receives the size, in bytes, of the data stored in the output buffer.</span></span>

<span data-ttu-id="1fb11-130">Si la mémoire tampon de sortie est trop petite, l’appel échoue, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) retourne [**WSAEINVAL**](windows-sockets-error-codes-2.md)et le paramètre *LpcbBytesReturned* pointe vers une valeur **DWORD** égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="1fb11-130">If the output buffer is too small, the call fails, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) returns [**WSAEINVAL**](windows-sockets-error-codes-2.md), and the *lpcbBytesReturned* parameter points to a **DWORD** value of zero.</span></span>

<span data-ttu-id="1fb11-131">Si *lpOverlapped* a la valeur **null**, la valeur **DWORD** vers laquelle pointe le paramètre *lpcbBytesReturned* retourné sur un appel réussi ne peut pas être égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="1fb11-131">If *lpOverlapped* is **NULL**, the **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned on a successful call cannot be zero.</span></span>

<span data-ttu-id="1fb11-132">Si le paramètre *lpOverlapped* n’a pas la **valeur null** pour les sockets superposés, les opérations qui ne peuvent pas être terminées immédiatement seront lancées et l’achèvement sera indiqué ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="1fb11-132">If the *lpOverlapped* parameter is not **NULL** for overlapped sockets, operations that cannot be completed immediately will be initiated, and completion will be indicated at a later time.</span></span>
<span data-ttu-id="1fb11-133">La valeur **DWORD** pointée par le paramètre *lpcbBytesReturned* retourné peut être égale à zéro, car la taille des données stockées ne peut pas être déterminée tant que l’opération avec chevauchement n’est pas terminée.</span><span class="sxs-lookup"><span data-stu-id="1fb11-133">The **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned may be zero since the size of the data stored can't be determined until the overlapped operation has completed.</span></span>
<span data-ttu-id="1fb11-134">L’état d’achèvement final peut être récupéré lorsque la méthode d’achèvement appropriée est signalée lorsque l’opération est terminée.</span><span class="sxs-lookup"><span data-stu-id="1fb11-134">The final completion status can be retrieved when the appropriate completion method is signaled when the operation has completed.</span></span>

### <a name="lpvoverlapped"></a><span data-ttu-id="1fb11-135">lpvOverlapped</span><span class="sxs-lookup"><span data-stu-id="1fb11-135">lpvOverlapped</span></span>

<span data-ttu-id="1fb11-136">Pointeur vers une structure [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) .</span><span class="sxs-lookup"><span data-stu-id="1fb11-136">A pointer to a [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="1fb11-137">Si le socket *s* a été créé sans l’attribut Overlapped, le paramètre *lpOverlapped* est ignoré.</span><span class="sxs-lookup"><span data-stu-id="1fb11-137">If socket *s* was created without the overlapped attribute, the *lpOverlapped* parameter is ignored.</span></span>

<span data-ttu-id="1fb11-138">Si *s* a été ouvert avec l’attribut Overlapped et que le paramètre *lpOverlapped* n’a pas la **valeur null**, l’opération est exécutée en tant qu’opération Overlapped (asynchrone).</span><span class="sxs-lookup"><span data-stu-id="1fb11-138">If *s* was opened with the overlapped attribute and the *lpOverlapped* parameter is not **NULL**, the operation is performed as an overlapped (asynchronous) operation.</span></span>
<span data-ttu-id="1fb11-139">Dans ce cas, le paramètre *lpOverlapped* doit pointer vers une structure [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) valide.</span><span class="sxs-lookup"><span data-stu-id="1fb11-139">In this case, *lpOverlapped* parameter must point to a valid [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="1fb11-140">Pour les opérations avec chevauchement, la fonction [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** retourne immédiatement, et la méthode d’achèvement appropriée est signalée lorsque l’opération est terminée.</span><span class="sxs-lookup"><span data-stu-id="1fb11-140">For overlapped operations, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns immediately, and the appropriate completion method is signaled when the operation has been completed.</span></span>
<span data-ttu-id="1fb11-141">Sinon, la fonction ne retourne pas jusqu’à ce que l’opération soit terminée ou qu’une erreur se produise.</span><span class="sxs-lookup"><span data-stu-id="1fb11-141">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

### <a name="lpcompletionroutine"></a><span data-ttu-id="1fb11-142">lpCompletionRoutine</span><span class="sxs-lookup"><span data-stu-id="1fb11-142">lpCompletionRoutine</span></span>

<span data-ttu-id="1fb11-143">Type : \_ In_opt \_ [ **LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span><span class="sxs-lookup"><span data-stu-id="1fb11-143">Type: \_In_opt\_ [**LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span></span>

<span data-ttu-id="1fb11-144">Pointeur vers la routine de saisie semi-automatique appelée lorsque l’opération est terminée (ignoré pour les sockets non superposés).</span><span class="sxs-lookup"><span data-stu-id="1fb11-144">A pointer to the completion routine called when the operation has been completed (ignored for non-overlapped sockets).</span></span>

### <a name="lpthreadid"></a><span data-ttu-id="1fb11-145">lpThreadId</span><span class="sxs-lookup"><span data-stu-id="1fb11-145">lpThreadId</span></span>

<span data-ttu-id="1fb11-146">Pointeur vers une structure [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) qui doit être utilisée par le fournisseur dans un appel ultérieur à [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc).</span><span class="sxs-lookup"><span data-stu-id="1fb11-146">A pointer to a [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure to be used by the provider in a subsequent call to [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc).</span></span>
<span data-ttu-id="1fb11-147">Le fournisseur doit stocker la structure [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) référencée (pas le pointeur vers le même) jusqu’à ce que la fonction [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) soit retournée.</span><span class="sxs-lookup"><span data-stu-id="1fb11-147">The provider should store the referenced [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure (not the pointer to same) until after the [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) function returns.</span></span>

<span data-ttu-id="1fb11-148">**Remarque**  Ce paramètre s’applique uniquement à la fonction **WSPIoctl** .</span><span class="sxs-lookup"><span data-stu-id="1fb11-148">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

### <a name="lperrno"></a><span data-ttu-id="1fb11-149">lpErrno</span><span class="sxs-lookup"><span data-stu-id="1fb11-149">lpErrno</span></span>

<span data-ttu-id="1fb11-150">Pointeur vers le code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="1fb11-150">A pointer to the error code.</span></span>

<span data-ttu-id="1fb11-151">**Remarque**  Ce paramètre s’applique uniquement à la fonction **WSPIoctl** .</span><span class="sxs-lookup"><span data-stu-id="1fb11-151">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

## <a name="return-value"></a><span data-ttu-id="1fb11-152">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1fb11-152">Return value</span></span>

<span data-ttu-id="1fb11-153">Si l’opération se termine correctement, la fonction [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** retourne la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="1fb11-153">If the operation completes successfully, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns zero.</span></span>

<span data-ttu-id="1fb11-154">Si l’opération échoue ou est en attente, la fonction [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** retourne une **\_ erreur de socket**.</span><span class="sxs-lookup"><span data-stu-id="1fb11-154">If the operation fails or is pending, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns **SOCKET\_ERROR**.</span></span>
<span data-ttu-id="1fb11-155">Pour afficher les informations d’erreur étendues, appelez [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span><span class="sxs-lookup"><span data-stu-id="1fb11-155">To get extended error information, call [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>

| <span data-ttu-id="1fb11-156">Code d'erreur</span><span class="sxs-lookup"><span data-stu-id="1fb11-156">Error code</span></span> | <span data-ttu-id="1fb11-157">Signification</span><span class="sxs-lookup"><span data-stu-id="1fb11-157">Meaning</span></span> |
|------------|---------|
|<span data-ttu-id="1fb11-158">**\_e/s WSA \_ en attente**</span><span class="sxs-lookup"><span data-stu-id="1fb11-158">**WSA\_IO\_PENDING**</span></span> | <span data-ttu-id="1fb11-159">L’opération d’e/s avec chevauchement est en cours.</span><span class="sxs-lookup"><span data-stu-id="1fb11-159">Overlapped I/O operation is in progress.</span></span> <span data-ttu-id="1fb11-160">Cette valeur est retournée si une opération avec chevauchement a été correctement initiée et que son achèvement sera indiqué ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="1fb11-160">This value is returned if an overlapped operation was successfully initiated and completion will be indicated at a later time.</span></span> |
| <span data-ttu-id="1fb11-161">**\_opération WSA \_ abandonnée**</span><span class="sxs-lookup"><span data-stu-id="1fb11-161">**WSA\_OPERATION\_ABORTED**</span></span> | <span data-ttu-id="1fb11-162">L’opération d’e/s a été annulée en raison de la sortie d’un thread ou d’une demande de l’application.</span><span class="sxs-lookup"><span data-stu-id="1fb11-162">The I/O operation has been aborted because of either a thread exit or an application request.</span></span> <span data-ttu-id="1fb11-163">Cette erreur est retournée si une opération avec chevauchement a été annulée en raison de la fermeture du socket ou de l’exécution de la commande **SIO \_ flush IOCTL** .</span><span class="sxs-lookup"><span data-stu-id="1fb11-163">This error is returned if an overlapped operation was canceled due to the closure of the socket or the execution of the **SIO\_FLUSH IOCTL** command.</span></span> |
| <span data-ttu-id="1fb11-164">**WSAEACCES**</span><span class="sxs-lookup"><span data-stu-id="1fb11-164">**WSAEACCES**</span></span> | <span data-ttu-id="1fb11-165">Une tentative a été effectuée pour accéder à un socket de manière interdite par ses autorisations d’accès.</span><span class="sxs-lookup"><span data-stu-id="1fb11-165">An attempt was made to access a socket in a way forbidden by its access permissions.</span></span> <span data-ttu-id="1fb11-166">Cette erreur est retournée dans plusieurs conditions pour les réservations de port persistantes, notamment : l’utilisateur n’a pas les privilèges d’administrateur requis sur l’ordinateur local ou l’application n’est pas exécutée dans un interpréteur de commandes amélioré en tant qu’administrateur intégré ( `RunAs administrator` ).</span><span class="sxs-lookup"><span data-stu-id="1fb11-166">This error is returned under several conditions for persistent port reservations that include the following: the user lacks the required administrative privileges on the local computer or the application is not running in an enhanced shell as the built-in Administrator (`RunAs administrator`).</span></span> |
| <span data-ttu-id="1fb11-167">**WSAEFAULT**</span><span class="sxs-lookup"><span data-stu-id="1fb11-167">**WSAEFAULT**</span></span> | <span data-ttu-id="1fb11-168">Le système a détecté une adresse de pointeur non valide lors de la tentative d’utilisation d’un argument de pointeur dans un appel.</span><span class="sxs-lookup"><span data-stu-id="1fb11-168">The system detected an invalid pointer address in attempting to use a pointer argument in a call.</span></span> <span data-ttu-id="1fb11-169">Cette erreur est retournée par le paramètre *lpvInBuffer*, *lpvoutBuffer*, *lpcbBytesReturned*, *lpOverlapped* ou *lpCompletionRoutine* n’est pas entièrement contenu dans une partie valide de l’espace d’adressage de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="1fb11-169">This error is returned of the *lpvInBuffer*, *lpvoutBuffer*, *lpcbBytesReturned*, *lpOverlapped* or *lpCompletionRoutine* parameter is not totally contained in a valid part of the user address space.</span></span> |
| <span data-ttu-id="1fb11-170">**WSAEINPROGRESS**</span><span class="sxs-lookup"><span data-stu-id="1fb11-170">**WSAEINPROGRESS**</span></span> | <span data-ttu-id="1fb11-171">Une opération de blocage est actuellement en cours d'exécution.</span><span class="sxs-lookup"><span data-stu-id="1fb11-171">A blocking operation is currently executing.</span></span> <span data-ttu-id="1fb11-172">Cette erreur est retournée si la fonction est appelée lorsqu’un rappel est en cours.</span><span class="sxs-lookup"><span data-stu-id="1fb11-172">This error is returned if the function is invoked when a callback is in progress.</span></span> |
| <span data-ttu-id="1fb11-173">**WSAEINTR**</span><span class="sxs-lookup"><span data-stu-id="1fb11-173">**WSAEINTR**</span></span> | <span data-ttu-id="1fb11-174">Une opération de blocage a été interrompue par un appel à [**WSACancelBlockingCall**](/windows/desktop/api/winsock2/nf-winsock2-wsacancelblockingcall).</span><span class="sxs-lookup"><span data-stu-id="1fb11-174">A blocking operation was interrupted by a call to [**WSACancelBlockingCall**](/windows/desktop/api/winsock2/nf-winsock2-wsacancelblockingcall).</span></span> <span data-ttu-id="1fb11-175">Cette erreur est retournée si une opération de blocage a été interrompue.</span><span class="sxs-lookup"><span data-stu-id="1fb11-175">This error is returned if a blocking operation was interrupted.</span></span> |
| <span data-ttu-id="1fb11-176">**WSAEINVAL**</span><span class="sxs-lookup"><span data-stu-id="1fb11-176">**WSAEINVAL**</span></span> | <span data-ttu-id="1fb11-177">Argument non valide fourni.</span><span class="sxs-lookup"><span data-stu-id="1fb11-177">An invalid argument was supplied.</span></span> <span data-ttu-id="1fb11-178">Cette erreur est retournée si le paramètre *dwIoControlCode* n’est pas une commande valide, si un paramètre d’entrée spécifié n’est pas acceptable ou si la commande n’est pas applicable au type de socket spécifié.</span><span class="sxs-lookup"><span data-stu-id="1fb11-178">This error is returned if the *dwIoControlCode* parameter is not a valid command, or a specified input parameter is not acceptable, or the command is not applicable to the type of socket specified.</span></span> |
| <span data-ttu-id="1fb11-179">**WSAENETDOWN**</span><span class="sxs-lookup"><span data-stu-id="1fb11-179">**WSAENETDOWN**</span></span> | <span data-ttu-id="1fb11-180">Une opération de socket a rencontré un réseau inactif.</span><span class="sxs-lookup"><span data-stu-id="1fb11-180">A socket operation encountered a dead network.</span></span> <span data-ttu-id="1fb11-181">Cette erreur est retournée si le sous-système réseau a échoué.</span><span class="sxs-lookup"><span data-stu-id="1fb11-181">This error is returned if the network subsystem has failed.</span></span> |
| <span data-ttu-id="1fb11-182">**WSAENOTSOCK**</span><span class="sxs-lookup"><span data-stu-id="1fb11-182">**WSAENOTSOCK**</span></span> | <span data-ttu-id="1fb11-183">Une opération a été tentée sur un qui n’est pas un Socket.</span><span class="sxs-lookup"><span data-stu-id="1fb11-183">An operation was attempted on something that is not a socket.</span></span> <span data-ttu-id="1fb11-184">Cette erreur est retournée si le *descripteur* n’est pas un Socket.</span><span class="sxs-lookup"><span data-stu-id="1fb11-184">This error is returned if the descriptor *s* is not a socket.</span></span> |
| <span data-ttu-id="1fb11-185">**WSAEOPNOTSUPP**</span><span class="sxs-lookup"><span data-stu-id="1fb11-185">**WSAEOPNOTSUPP**</span></span> | <span data-ttu-id="1fb11-186">L’opération tentée n’est pas prise en charge pour le type d’objet référencé.</span><span class="sxs-lookup"><span data-stu-id="1fb11-186">The attempted operation is not supported for the type of object referenced.</span></span> <span data-ttu-id="1fb11-187">Cette erreur est retournée si la commande IOCTL spécifiée n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="1fb11-187">This error is returned if the specified IOCTL command is not supported.</span></span> <span data-ttu-id="1fb11-188">Cette erreur est également retournée si l’IOCTL de **\_ réservation de \_ port \_ SIO Associate** n’est pas prise en charge par le fournisseur de transport.</span><span class="sxs-lookup"><span data-stu-id="1fb11-188">This error is also returned if the **SIO\_ASSOCIATE\_PORT\_RESERVATION** IOCTL is not supported by the transport provider.</span></span> <span data-ttu-id="1fb11-189">Cette erreur est également retournée lorsqu’une tentative d’utilisation de l’IOCTL de **\_ réservation de \_ port \_ SIO Associate** est effectuée sur un socket autre que UDP ou TCP.</span><span class="sxs-lookup"><span data-stu-id="1fb11-189">This error is also returned when an attempt to use the **SIO\_ASSOCIATE\_PORT\_RESERVATION** IOCTL is made on a socket other than UDP or TCP.</span></span> |

## <a name="remarks"></a><span data-ttu-id="1fb11-190">Notes</span><span class="sxs-lookup"><span data-stu-id="1fb11-190">Remarks</span></span>

<span data-ttu-id="1fb11-191">L’IOCTL de **\_ réservation de \_ port \_ SIO Associate** est prise en charge sur Windows Vista et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="1fb11-191">The **SIO\_ASSOCIATE\_PORT\_RESERVATION** IOCTL is supported on Windows Vista and later versions of the operating system.</span></span>

<span data-ttu-id="1fb11-192">Les applications et les services qui doivent réserver des ports sont répartis en deux catégories.</span><span class="sxs-lookup"><span data-stu-id="1fb11-192">Applications and services which need to reserve ports fall into two categories.</span></span>
<span data-ttu-id="1fb11-193">La première catégorie comprend des composants qui ont besoin d’un port particulier dans le cadre de leur fonctionnement.</span><span class="sxs-lookup"><span data-stu-id="1fb11-193">The first category includes components which need a particular port as part of their operation.</span></span>
<span data-ttu-id="1fb11-194">De tels composants préfèrent généralement spécifier le port requis au moment de l’installation (dans un manifeste d’application, par exemple).</span><span class="sxs-lookup"><span data-stu-id="1fb11-194">Such components will generally prefer to specify their required port at installation time (in an application manifest, for example).</span></span>
<span data-ttu-id="1fb11-195">La deuxième catégorie comprend des composants qui ont besoin d’un port ou d’un bloc de ports disponibles au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="1fb11-195">The second category includes components which need any available port or block of ports at runtime.</span></span>
<span data-ttu-id="1fb11-196">Ces deux catégories correspondent à des demandes de réservation de port génériques et spécifiques.</span><span class="sxs-lookup"><span data-stu-id="1fb11-196">These two categories correspond to specific and wildcard port reservation requests.</span></span>
<span data-ttu-id="1fb11-197">Les demandes de réservation spécifiques peuvent être persistantes ou d’exécution, tandis que les demandes de réservation de port génériques sont uniquement prises en charge au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="1fb11-197">Specific reservation requests may be persistent or runtime, while wildcard port reservation requests are only supported at runtime.</span></span>

<span data-ttu-id="1fb11-198">L’IOCTL de **\_ réservation de \_ port \_ SIO Associate** est utilisée pour associer une réservation de port TCP ou UDP à une réservation persistante ou d’exécution.</span><span class="sxs-lookup"><span data-stu-id="1fb11-198">The **SIO\_ASSOCIATE\_PORT\_RESERVATION** IOCTL is used to associate a TCP or UDP port reservation with either a persistent or runtime reservation.</span></span>

<span data-ttu-id="1fb11-199">La fonction [**CreatePersistentTcpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistenttcpportreservation) ou [**CreatePersistentUdpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistentudpportreservation) permet à une application ou à un service de réserver un bloc persistant de ports TCP ou UDP.</span><span class="sxs-lookup"><span data-stu-id="1fb11-199">The [**CreatePersistentTcpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistenttcpportreservation) or [**CreatePersistentUdpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistentudpportreservation) function provides the ability for an application or service to reserve a persistent block of TCP or UDP ports.</span></span>
<span data-ttu-id="1fb11-200">Les réservations de port persistantes sont enregistrées dans un magasin persistant pour le module TCP ou UDP dans Windows.</span><span class="sxs-lookup"><span data-stu-id="1fb11-200">Persistent port reservations are recorded in a persistent store for the TCP or UDP module in Windows.</span></span>
<span data-ttu-id="1fb11-201">Notez que le jeton pour une réservation de port persistant donnée peut changer chaque fois que le système est redémarré.</span><span class="sxs-lookup"><span data-stu-id="1fb11-201">Note that the token for a given persistent port reservation may change each time the system is restarted.</span></span>

<span data-ttu-id="1fb11-202">Une fois qu’une réservation de port TCP ou UDP persistante a été obtenue, une application peut demander des affectations de port à partir de la réservation de port en ouvrant un socket TCP ou UDP, puis en appelant la fonction [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) en spécifiant l’IOCTL de **réservation de \_ \_ port \_ SIO Associate** et en passant le jeton de réservation avant d’émettre un appel à la fonction de [**liaison**](/windows/desktop/api/winsock/nf-winsock-bind) sur le Socket.</span><span class="sxs-lookup"><span data-stu-id="1fb11-202">Once a persistent TCP or UDP port reservation has been obtained, an application can request port assignments from the port reservation by opening a TCP or UDP socket, then calling the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) function specifying the **SIO\_ASSOCIATE\_PORT\_RESERVATION** IOCTL and passing the reservation token before issuing a call to the [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) function on the socket.</span></span>

<span data-ttu-id="1fb11-203">Le [**SIO_ACQUIRE_PORT_RESERVATION**](sio-acquire-port-reservation.md) IOCTL peut être utilisé pour demander une réservation d’exécution pour un bloc de ports TCP ou UDP.</span><span class="sxs-lookup"><span data-stu-id="1fb11-203">The [**SIO_ACQUIRE_PORT_RESERVATION**](sio-acquire-port-reservation.md) IOCTL can be used to request a runtime reservation for a block of TCP or UDP ports.</span></span>
<span data-ttu-id="1fb11-204">Pour les réservations de port d’exécution, le pool de ports requiert que les réservations soient consommées à partir du processus sur lequel la réservation a été accordée.</span><span class="sxs-lookup"><span data-stu-id="1fb11-204">For runtime port reservations, the port pool requires that reservations be consumed from the process on whose socket the reservation was granted.</span></span>
<span data-ttu-id="1fb11-205">Les réservations de port d’exécution durent uniquement tant que la durée de vie du socket sur lequel la [**SIO_ACQUIRE_PORT_RESERVATION**](sio-acquire-port-reservation.md) IOCTL a été appelée.</span><span class="sxs-lookup"><span data-stu-id="1fb11-205">Runtime port reservations last only as long as the lifetime of the socket on which the [**SIO_ACQUIRE_PORT_RESERVATION**](sio-acquire-port-reservation.md) IOCTL was called.</span></span>
<span data-ttu-id="1fb11-206">En revanche, les réservations de port persistantes créées à l’aide de la fonction [**CreatePersistentTcpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistenttcpportreservation) ou [**CreatePersistentUdpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistentudpportreservation) peuvent être consommées par n’importe quel processus ayant la possibilité d’obtenir des réservations persistantes.</span><span class="sxs-lookup"><span data-stu-id="1fb11-206">In contrast, persistent port reservations created using the [**CreatePersistentTcpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistenttcpportreservation) or [**CreatePersistentUdpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistentudpportreservation) function may be consumed by any process with the ability to obtain persistent reservations.</span></span>

<span data-ttu-id="1fb11-207">Une fois qu’une réservation de port TCP ou UDP du runtime a été obtenue, une application peut demander des affectations de port à partir de la réservation de port en ouvrant un socket TCP ou UDP, puis en appelant la fonction [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) en spécifiant l’IOCTL de **réservation de \_ \_ port \_ SIO Associate** et en passant le jeton de réservation avant d’émettre un appel à la fonction de [**liaison**](/windows/desktop/api/winsock/nf-winsock-bind) sur le Socket.</span><span class="sxs-lookup"><span data-stu-id="1fb11-207">Once a runtime TCP or UDP port reservation has been obtained, an application can request port assignments from the port reservation by opening a TCP or UDP socket, then calling the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) function specifying the **SIO\_ASSOCIATE\_PORT\_RESERVATION** IOCTL and passing the reservation token before issuing a call to the [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) function on the socket.</span></span>

<span data-ttu-id="1fb11-208">Si les deux paramètres *lpOverlapped* et *lpCompletionRoutine* sont NULL, le socket dans cette fonction sera traité comme un socket non superposé.</span><span class="sxs-lookup"><span data-stu-id="1fb11-208">If both *lpOverlapped* and *lpCompletionRoutine* parameters are NULL, the socket in this function will be treated as a non-overlapped socket.</span></span>
<span data-ttu-id="1fb11-209">Pour un socket non superposé, les paramètres *lpOverlapped* et *lpCompletionRoutine* sont ignorés, sauf que la fonction peut se bloquer si le socket *s* est en mode blocage.</span><span class="sxs-lookup"><span data-stu-id="1fb11-209">For a non-overlapped socket, *lpOverlapped* and *lpCompletionRoutine* parameters are ignored, except that the function can block if socket *s* is in blocking mode.</span></span>
<span data-ttu-id="1fb11-210">Si le socket *s* est en mode non bloquant, cette fonction sera toujours bloquée, car cette IOCTL particulière ne prend pas en charge le mode non bloquant.</span><span class="sxs-lookup"><span data-stu-id="1fb11-210">If socket *s* is in non-blocking mode, this function will still block since this particular IOCTL does not support non-blocking mode.</span></span>

<span data-ttu-id="1fb11-211">Pour les sockets superposés, les opérations qui ne peuvent pas être terminées immédiatement sont lancées et l’achèvement est indiqué ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="1fb11-211">For overlapped sockets, operations that cannot be completed immediately will be initiated, and completion will be indicated at a later time.</span></span>

<span data-ttu-id="1fb11-212">Toute IOCTL peut se bloquer indéfiniment, en fonction de l’implémentation du fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="1fb11-212">Any IOCTL may block indefinitely, depending on the service provider's implementation.</span></span>
<span data-ttu-id="1fb11-213">Si l’application ne peut pas tolérer le blocage dans un appel de fonction [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** , les e/s avec chevauchement sont conseillées pour les IOCTL qui sont particulièrement susceptibles de se bloquer.</span><span class="sxs-lookup"><span data-stu-id="1fb11-213">If the application cannot tolerate blocking in a [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function call, overlapped I/O would be advised for IOCTLs that are especially likely to block.</span></span>

<span data-ttu-id="1fb11-214">L’IOCTL de **\_ réservation de \_ port \_ SIO Associate** peut échouer avec **WSAEINTR** ou **WSA_OPERATION_ABORTED** dans les cas suivants :</span><span class="sxs-lookup"><span data-stu-id="1fb11-214">The **SIO\_ASSOCIATE\_PORT\_RESERVATION** IOCTL can fail with **WSAEINTR** or **WSA_OPERATION_ABORTED** under the following cases:</span></span>

* <span data-ttu-id="1fb11-215">La demande est annulée par le gestionnaire d’e/s.</span><span class="sxs-lookup"><span data-stu-id="1fb11-215">The request is canceled by the I/O Manager.</span></span>
* <span data-ttu-id="1fb11-216">Le socket est fermé.</span><span class="sxs-lookup"><span data-stu-id="1fb11-216">The socket is closed.</span></span>

<span data-ttu-id="1fb11-217">L’IOCTL de **\_ réservation de \_ port \_ SIO Associate** transmise à la fonction [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** pour une réservation de port persistante ne peut être utilisée que dans une application lorsque l’utilisateur a ouvert une session en tant que membre du groupe administrateurs.</span><span class="sxs-lookup"><span data-stu-id="1fb11-217">The **SIO\_ASSOCIATE\_PORT\_RESERVATION** IOCTL passed to the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function for a persistent port reservation can only be used in an application when the user is logged on as a member of the Administrators group.</span></span>
<span data-ttu-id="1fb11-218">Si **SIO \_ associer \_ la \_ réservation de port** IOCTL est utilisée dans une application lorsque l’utilisateur n’est pas membre du groupe administrateurs, l’appel de fonction échoue et **WSAEACCES** est retourné.</span><span class="sxs-lookup"><span data-stu-id="1fb11-218">If **SIO\_ASSOCIATE\_PORT\_RESERVATION** IOCTL is used in an application when the user is not a member of the Administrators group, the function call will fail and **WSAEACCES** is returned.</span></span>
<span data-ttu-id="1fb11-219">L’utilisation de l’IOCTL de **\_ réservation de \_ port \_ SIO Associate** peut également échouer en raison du contrôle de compte d’utilisateur (UAC) sur Windows Vista et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="1fb11-219">The use of the **SIO\_ASSOCIATE\_PORT\_RESERVATION** IOCTL can also fail because of user account control (UAC) on Windows Vista and later.</span></span>
<span data-ttu-id="1fb11-220">Si une application qui utilise cette IOCTL avec une réservation de port persistant est exécutée par un utilisateur ayant ouvert une session en tant que membre du groupe administrateurs autre que l’administrateur intégré, cet appel échoue, sauf si l’application a été marquée dans le fichier manifeste avec un **requestedExecutionLevel** défini sur *requireAdministrator*.</span><span class="sxs-lookup"><span data-stu-id="1fb11-220">If an application that uses this IOCTL with a persistent port reservation is executed by a user logged on as a member of the Administrators group other than the built-in Administrator, this call will fail unless the application has been marked in the manifest file with a **requestedExecutionLevel** set to *requireAdministrator*.</span></span>
<span data-ttu-id="1fb11-221">Si l’application ne dispose pas de ce fichier manifeste, un utilisateur ayant ouvert une session en tant que membre du groupe administrateurs autre que l’administrateur intégré doit exécuter l’application dans un interpréteur de commandes amélioré en tant qu’administrateur intégré ( `RunAs administrator` ) pour que cette fonction aboutisse.</span><span class="sxs-lookup"><span data-stu-id="1fb11-221">If the application lacks this manifest file, a user logged on as a member of the Administrators group other than the built-in Administrator must then be executing the application in an enhanced shell as the built-in Administrator (`RunAs administrator`) for this function to succeed.</span></span>

## <a name="see-also"></a><span data-ttu-id="1fb11-222">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1fb11-222">See also</span></span>

[<span data-ttu-id="1fb11-223">**établis**</span><span class="sxs-lookup"><span data-stu-id="1fb11-223">**bind**</span></span>](/windows/desktop/api/winsock/nf-winsock-bind)

[<span data-ttu-id="1fb11-224">**CreatePersistentTcpPortReservation**</span><span class="sxs-lookup"><span data-stu-id="1fb11-224">**CreatePersistentTcpPortReservation**</span></span>](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistenttcpportreservation)

[<span data-ttu-id="1fb11-225">**CreatePersistentUdpPortReservation**</span><span class="sxs-lookup"><span data-stu-id="1fb11-225">**CreatePersistentUdpPortReservation**</span></span>](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistentudpportreservation)

[<span data-ttu-id="1fb11-226">**DeletePersistentTcpPortReservation**</span><span class="sxs-lookup"><span data-stu-id="1fb11-226">**DeletePersistentTcpPortReservation**</span></span>](/windows/desktop/api/iphlpapi/nf-iphlpapi-deletepersistenttcpportreservation)

[<span data-ttu-id="1fb11-227">**DeletePersistentUdpPortReservation**</span><span class="sxs-lookup"><span data-stu-id="1fb11-227">**DeletePersistentUdpPortReservation**</span></span>](/windows/desktop/api/iphlpapi/nf-iphlpapi-deletepersistentudpportreservation)

[<span data-ttu-id="1fb11-228">**INET_PORT_RESERVATION_TOKEN**</span><span class="sxs-lookup"><span data-stu-id="1fb11-228">**INET_PORT_RESERVATION_TOKEN**</span></span>](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_reservation_token)

[<span data-ttu-id="1fb11-229">**LookupPersistentTcpPortReservation**</span><span class="sxs-lookup"><span data-stu-id="1fb11-229">**LookupPersistentTcpPortReservation**</span></span>](/windows/desktop/api/iphlpapi/nf-iphlpapi-lookuppersistenttcpportreservation)

[<span data-ttu-id="1fb11-230">**LookupPersistentUdpPortReservation**</span><span class="sxs-lookup"><span data-stu-id="1fb11-230">**LookupPersistentUdpPortReservation**</span></span>](/windows/desktop/api/iphlpapi/nf-iphlpapi-lookuppersistentudpportreservation)

[<span data-ttu-id="1fb11-231">**SIO_ACQUIRE_PORT_RESERVATION**</span><span class="sxs-lookup"><span data-stu-id="1fb11-231">**SIO_ACQUIRE_PORT_RESERVATION**</span></span>](sio-acquire-port-reservation.md)

[<span data-ttu-id="1fb11-232">**SIO_RELEASE_PORT_RESERVATION**</span><span class="sxs-lookup"><span data-stu-id="1fb11-232">**SIO_RELEASE_PORT_RESERVATION**</span></span>](sio-release-port-reservation.md)

[<span data-ttu-id="1fb11-233">socle</span><span class="sxs-lookup"><span data-stu-id="1fb11-233">socket</span></span>](/windows/desktop/api/winsock2/nf-winsock2-socket)

[<span data-ttu-id="1fb11-234">**WSAGetLastError**</span><span class="sxs-lookup"><span data-stu-id="1fb11-234">**WSAGetLastError**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetlasterror)

[<span data-ttu-id="1fb11-235">**WSAGetOverlappedResult**</span><span class="sxs-lookup"><span data-stu-id="1fb11-235">**WSAGetOverlappedResult**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[<span data-ttu-id="1fb11-236">**WSAIoctl**</span><span class="sxs-lookup"><span data-stu-id="1fb11-236">**WSAIoctl**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[<span data-ttu-id="1fb11-237">**WSAOVERLAPPED**</span><span class="sxs-lookup"><span data-stu-id="1fb11-237">**WSAOVERLAPPED**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[<span data-ttu-id="1fb11-238">**WSASocketA**</span><span class="sxs-lookup"><span data-stu-id="1fb11-238">**WSASocketA**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[<span data-ttu-id="1fb11-239">**WSASocketW**</span><span class="sxs-lookup"><span data-stu-id="1fb11-239">**WSASocketW**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
