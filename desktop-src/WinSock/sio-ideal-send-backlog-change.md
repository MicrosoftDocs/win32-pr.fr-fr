---
description: Code de contrôle notifie une application lorsque la valeur de backlog d’envoi idéale change pour la connexion.
ms.assetid: 337883a5-7ceb-40d3-b318-b86dd488b94a
title: Code de contrôle SIO_IDEAL_SEND_BACKLOG_CHANGE
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 4eb07efecd39774c60d47cbcf7245c5831760e06
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755069"
---
# <a name="sio_ideal_send_backlog_change-control-code"></a><span data-ttu-id="8d4cb-103">Code de contrôle SIO_IDEAL_SEND_BACKLOG_CHANGE</span><span class="sxs-lookup"><span data-stu-id="8d4cb-103">SIO_IDEAL_SEND_BACKLOG_CHANGE Control Code</span></span>

## <a name="description"></a><span data-ttu-id="8d4cb-104">Description</span><span class="sxs-lookup"><span data-stu-id="8d4cb-104">Description</span></span>

<span data-ttu-id="8d4cb-105">Le code de contrôle de **\_ modification du backlog d' \_ envoi \_ \_ SIO idéal** notifie une application lorsque la valeur d’un backlog d’envoi (ISB) idéal change pour la connexion.</span><span class="sxs-lookup"><span data-stu-id="8d4cb-105">The **SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE** control code notifies an application when the ideal send backlog (ISB) value changes for the connection.</span></span>

<span data-ttu-id="8d4cb-106">Pour effectuer cette opération, appelez la fonction [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** avec les paramètres suivants.</span><span class="sxs-lookup"><span data-stu-id="8d4cb-106">To perform this operation, call the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function with the following parameters.</span></span>

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_IDEAL_SEND_BACKLOG_CHANGE, // dwIoControlCode
  NULL,                         // lpvInBuffer
  0,                            // cbInBuffer
  NULL,         // output buffer
  0,       // size of output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

```cpp
int WSPIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_IDEAL_SEND_BACKLOG_CHANGE, // dwIoControlCode
  NULL,                         // lpvInBuffer
  0,                            // cbInBuffer
  NULL,         // output buffer
  0,       // size of output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
  (LPWSATHREADID) lpThreadId,   // a WSATHREADID structure
  (LPINT) lpErrno   // a pointer to the error code.
);
```

## <a name="parameters"></a><span data-ttu-id="8d4cb-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8d4cb-107">Parameters</span></span>

### <a name="s"></a><span data-ttu-id="8d4cb-108">s</span><span class="sxs-lookup"><span data-stu-id="8d4cb-108">s</span></span>

<span data-ttu-id="8d4cb-109">Descripteur identifiant un Socket.</span><span class="sxs-lookup"><span data-stu-id="8d4cb-109">A descriptor identifying a socket.</span></span>

### <a name="dwiocontrolcode"></a><span data-ttu-id="8d4cb-110">dwIoControlCode</span><span class="sxs-lookup"><span data-stu-id="8d4cb-110">dwIoControlCode</span></span>

<span data-ttu-id="8d4cb-111">Code de contrôle de l’opération.</span><span class="sxs-lookup"><span data-stu-id="8d4cb-111">The control code for the operation.</span></span>
<span data-ttu-id="8d4cb-112">Utilisez **SIO pour la modification de \_ \_ BACKLOG d’envoi \_ \_ idéale** pour cette opération.</span><span class="sxs-lookup"><span data-stu-id="8d4cb-112">Use **SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE** for this operation.</span></span>

### <a name="lpvinbuffer"></a><span data-ttu-id="8d4cb-113">lpvInBuffer</span><span class="sxs-lookup"><span data-stu-id="8d4cb-113">lpvInBuffer</span></span>

<span data-ttu-id="8d4cb-114">Pointeur vers la mémoire tampon d’entrée.</span><span class="sxs-lookup"><span data-stu-id="8d4cb-114">A pointer to the input buffer.</span></span>
<span data-ttu-id="8d4cb-115">Ce paramètre n’est pas utilisé pour cette opération.</span><span class="sxs-lookup"><span data-stu-id="8d4cb-115">This parameter is unused for this operation.</span></span>

### <a name="cbinbuffer"></a><span data-ttu-id="8d4cb-116">cbInBuffer</span><span class="sxs-lookup"><span data-stu-id="8d4cb-116">cbInBuffer</span></span>

<span data-ttu-id="8d4cb-117">Taille, en octets, de la mémoire tampon d’entrée. Ce paramètre n’est pas utilisé pour cette opération.</span><span class="sxs-lookup"><span data-stu-id="8d4cb-117">The size, in bytes, of the input buffer.This parameter is unused for this operation.</span></span>

### <a name="lpvoutbuffer"></a><span data-ttu-id="8d4cb-118">lpvOutBuffer</span><span class="sxs-lookup"><span data-stu-id="8d4cb-118">lpvOutBuffer</span></span>

<span data-ttu-id="8d4cb-119">Pointeur vers la mémoire tampon de sortie.</span><span class="sxs-lookup"><span data-stu-id="8d4cb-119">A pointer to the output buffer.</span></span>
<span data-ttu-id="8d4cb-120">Ce paramètre n’est pas utilisé pour cette opération.</span><span class="sxs-lookup"><span data-stu-id="8d4cb-120">This parameter is unused for this operation.</span></span>

### <a name="cboutbuffer"></a><span data-ttu-id="8d4cb-121">cbOutBuffer</span><span class="sxs-lookup"><span data-stu-id="8d4cb-121">cbOutBuffer</span></span>

<span data-ttu-id="8d4cb-122">Taille, en octets, de la mémoire tampon de sortie.</span><span class="sxs-lookup"><span data-stu-id="8d4cb-122">The size, in bytes, of the output buffer.</span></span>
<span data-ttu-id="8d4cb-123">Ce paramètre doit avoir la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="8d4cb-123">This parameter must be set to zero.</span></span>

### <a name="lpcbbytesreturned"></a><span data-ttu-id="8d4cb-124">lpcbBytesReturned</span><span class="sxs-lookup"><span data-stu-id="8d4cb-124">lpcbBytesReturned</span></span>

<span data-ttu-id="8d4cb-125">Pointeur vers une variable qui reçoit la taille, en octets, des données stockées dans la mémoire tampon de sortie.</span><span class="sxs-lookup"><span data-stu-id="8d4cb-125">A pointer to a variable that receives the size, in bytes, of the data stored in the output buffer.</span></span>
<span data-ttu-id="8d4cb-126">Ce paramètre retourné pointe vers une valeur **DWORD** égale à zéro pour cette opération, car il n’y a pas de sortie.</span><span class="sxs-lookup"><span data-stu-id="8d4cb-126">This returned parameter points to a **DWORD** value of zero for this operation, since there is no output.</span></span>

### <a name="lpvoverlapped"></a><span data-ttu-id="8d4cb-127">lpvOverlapped</span><span class="sxs-lookup"><span data-stu-id="8d4cb-127">lpvOverlapped</span></span>

<span data-ttu-id="8d4cb-128">Pointeur vers une structure [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) .</span><span class="sxs-lookup"><span data-stu-id="8d4cb-128">A pointer to a [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="8d4cb-129">Si le socket *s* a été créé sans l’attribut Overlapped, le paramètre *lpOverlapped* est ignoré.</span><span class="sxs-lookup"><span data-stu-id="8d4cb-129">If socket *s* was created without the overlapped attribute, the *lpOverlapped* parameter is ignored.</span></span>

<span data-ttu-id="8d4cb-130">Si *s* a été ouvert avec l’attribut Overlapped et que le paramètre *lpOverlapped* n’a pas la **valeur null**, l’opération est exécutée en tant qu’opération Overlapped (asynchrone).</span><span class="sxs-lookup"><span data-stu-id="8d4cb-130">If *s* was opened with the overlapped attribute and the *lpOverlapped* parameter is not **NULL**, the operation is performed as an overlapped (asynchronous) operation.</span></span>
<span data-ttu-id="8d4cb-131">Dans ce cas, le paramètre *lpOverlapped* doit pointer vers une structure [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) valide.</span><span class="sxs-lookup"><span data-stu-id="8d4cb-131">In this case, *lpOverlapped* parameter must point to a valid [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="8d4cb-132">Pour les opérations avec chevauchement, la fonction [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** retourne immédiatement, et la méthode d’achèvement appropriée est signalée lorsque l’opération est terminée.</span><span class="sxs-lookup"><span data-stu-id="8d4cb-132">For overlapped operations, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns immediately, and the appropriate completion method is signaled when the operation has been completed.</span></span>
<span data-ttu-id="8d4cb-133">Sinon, la fonction ne retourne pas jusqu’à ce que l’opération soit terminée ou qu’une erreur se produise.</span><span class="sxs-lookup"><span data-stu-id="8d4cb-133">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

### <a name="lpcompletionroutine"></a><span data-ttu-id="8d4cb-134">lpCompletionRoutine</span><span class="sxs-lookup"><span data-stu-id="8d4cb-134">lpCompletionRoutine</span></span>

<span data-ttu-id="8d4cb-135">Type : \_ In_opt \_ [ **LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span><span class="sxs-lookup"><span data-stu-id="8d4cb-135">Type: \_In_opt\_ [**LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span></span>

<span data-ttu-id="8d4cb-136">Pointeur vers la routine de saisie semi-automatique appelée lorsque l’opération est terminée (ignoré pour les sockets non superposés).</span><span class="sxs-lookup"><span data-stu-id="8d4cb-136">A pointer to the completion routine called when the operation has been completed (ignored for non-overlapped sockets).</span></span>

### <a name="lpthreadid"></a><span data-ttu-id="8d4cb-137">lpThreadId</span><span class="sxs-lookup"><span data-stu-id="8d4cb-137">lpThreadId</span></span>

<span data-ttu-id="8d4cb-138">Pointeur vers une structure [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) qui doit être utilisée par le fournisseur dans un appel ultérieur à [**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc).</span><span class="sxs-lookup"><span data-stu-id="8d4cb-138">A pointer to a [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure to be used by the provider in a subsequent call to [**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc).</span></span>
<span data-ttu-id="8d4cb-139">Le fournisseur doit stocker la structure [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) référencée (pas le pointeur vers le même) jusqu’à ce que la fonction [**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc) soit retournée.</span><span class="sxs-lookup"><span data-stu-id="8d4cb-139">The provider should store the referenced [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure (not the pointer to same) until after the [**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc) function returns.</span></span>

<span data-ttu-id="8d4cb-140">**Remarque**  Ce paramètre s’applique uniquement à la fonction **WSPIoctl** .</span><span class="sxs-lookup"><span data-stu-id="8d4cb-140">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

### <a name="lperrno"></a><span data-ttu-id="8d4cb-141">lpErrno</span><span class="sxs-lookup"><span data-stu-id="8d4cb-141">lpErrno</span></span>

<span data-ttu-id="8d4cb-142">Pointeur vers le code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="8d4cb-142">A pointer to the error code.</span></span>

<span data-ttu-id="8d4cb-143">**Remarque**  Ce paramètre s’applique uniquement à la fonction **WSPIoctl** .</span><span class="sxs-lookup"><span data-stu-id="8d4cb-143">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

## <a name="return-value"></a><span data-ttu-id="8d4cb-144">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8d4cb-144">Return value</span></span>

<span data-ttu-id="8d4cb-145">Si l’opération se termine correctement, la fonction [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** retourne la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="8d4cb-145">If the operation completes successfully, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns zero.</span></span>

<span data-ttu-id="8d4cb-146">Si l’opération échoue ou est en attente, la fonction [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** retourne une **\_ erreur de socket**.</span><span class="sxs-lookup"><span data-stu-id="8d4cb-146">If the operation fails or is pending, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns **SOCKET\_ERROR**.</span></span>
<span data-ttu-id="8d4cb-147">Pour afficher les informations d’erreur étendues, appelez [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span><span class="sxs-lookup"><span data-stu-id="8d4cb-147">To get extended error information, call [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>

| <span data-ttu-id="8d4cb-148">Code d'erreur</span><span class="sxs-lookup"><span data-stu-id="8d4cb-148">Error code</span></span> | <span data-ttu-id="8d4cb-149">Signification</span><span class="sxs-lookup"><span data-stu-id="8d4cb-149">Meaning</span></span> |
|------------|---------|
| <span data-ttu-id="8d4cb-150">**\_e/s WSA \_ en attente**</span><span class="sxs-lookup"><span data-stu-id="8d4cb-150">**WSA\_IO\_PENDING**</span></span> | <span data-ttu-id="8d4cb-151">Une opération avec chevauchement a été correctement initiée et l’achèvement sera indiqué ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="8d4cb-151">An overlapped operation was successfully initiated and completion will be indicated at a later time.</span></span> |
| <span data-ttu-id="8d4cb-152">**\_opération WSA \_ abandonnée**</span><span class="sxs-lookup"><span data-stu-id="8d4cb-152">**WSA\_OPERATION\_ABORTED**</span></span> | <span data-ttu-id="8d4cb-153">Une opération avec chevauchement a été annulée en raison de la fermeture du socket ou de l’exécution de la commande **SIO \_ flush** ioctl.</span><span class="sxs-lookup"><span data-stu-id="8d4cb-153">An overlapped operation was canceled due to the closure of the socket or the execution of the **SIO\_FLUSH** IOCTL command.</span></span> |
| <span data-ttu-id="8d4cb-154">**WSAEFAULT**</span><span class="sxs-lookup"><span data-stu-id="8d4cb-154">**WSAEFAULT**</span></span> | <span data-ttu-id="8d4cb-155">Le paramètre *lpOverlapped* ou *lpCompletionRoutine* n’est pas entièrement contenu dans une partie valide de l’espace d’adressage de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="8d4cb-155">The *lpOverlapped* or *lpCompletionRoutine* parameter is not totally contained in a valid part of the user address space.</span></span> |
| <span data-ttu-id="8d4cb-156">**WSAEINPROGRESS**</span><span class="sxs-lookup"><span data-stu-id="8d4cb-156">**WSAEINPROGRESS**</span></span> | <span data-ttu-id="8d4cb-157">La fonction est appelée lorsqu’un rappel est en cours.</span><span class="sxs-lookup"><span data-stu-id="8d4cb-157">The function is invoked when a callback is in progress.</span></span> |
| <span data-ttu-id="8d4cb-158">**WSAEINTR**</span><span class="sxs-lookup"><span data-stu-id="8d4cb-158">**WSAEINTR**</span></span> | <span data-ttu-id="8d4cb-159">Une opération de blocage a été interrompue.</span><span class="sxs-lookup"><span data-stu-id="8d4cb-159">A blocking operation was interrupted.</span></span> |
| <span data-ttu-id="8d4cb-160">**WSAEINVAL**</span><span class="sxs-lookup"><span data-stu-id="8d4cb-160">**WSAEINVAL**</span></span> | <span data-ttu-id="8d4cb-161">Le paramètre *dwIoControlCode* n’est pas une commande valide, ou un paramètre d’entrée spécifié n’est pas acceptable, ou la commande n’est pas applicable au type de socket spécifié.</span><span class="sxs-lookup"><span data-stu-id="8d4cb-161">The *dwIoControlCode* parameter is not a valid command, or a specified input parameter is not acceptable, or the command is not applicable to the type of socket specified.</span></span> <span data-ttu-id="8d4cb-162">Cette erreur est retournée si le paramètre *cbOutBuffer* n’est pas égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="8d4cb-162">This error is returned if the *cbOutBuffer* parameter is not zero.</span></span> |
| <span data-ttu-id="8d4cb-163">**WSAENETDOWN**</span><span class="sxs-lookup"><span data-stu-id="8d4cb-163">**WSAENETDOWN**</span></span> | <span data-ttu-id="8d4cb-164">Le sous-système réseau a échoué.</span><span class="sxs-lookup"><span data-stu-id="8d4cb-164">The network subsystem has failed.</span></span> |
| <span data-ttu-id="8d4cb-165">**WSAENOPROTOOPT**</span><span class="sxs-lookup"><span data-stu-id="8d4cb-165">**WSAENOPROTOOPT**</span></span> | <span data-ttu-id="8d4cb-166">L’option de socket n’est pas prise en charge sur le protocole spécifié.</span><span class="sxs-lookup"><span data-stu-id="8d4cb-166">The socket option is not supported on the specified protocol.</span></span> |
| <span data-ttu-id="8d4cb-167">**WSAENOTCONN**</span><span class="sxs-lookup"><span data-stu-id="8d4cb-167">**WSAENOTCONN**</span></span> | <span data-ttu-id="8d4cb-168">Le socket *n'* est pas connecté.</span><span class="sxs-lookup"><span data-stu-id="8d4cb-168">The socket *s* is not connected.</span></span> |
| <span data-ttu-id="8d4cb-169">**WSAENOTSOCK**</span><span class="sxs-lookup"><span data-stu-id="8d4cb-169">**WSAENOTSOCK**</span></span> | <span data-ttu-id="8d4cb-170">Le descripteur *s* n’est pas un Socket.</span><span class="sxs-lookup"><span data-stu-id="8d4cb-170">The descriptor *s* is not a socket.</span></span> |
| <span data-ttu-id="8d4cb-171">**WSAEOPNOTSUPP**</span><span class="sxs-lookup"><span data-stu-id="8d4cb-171">**WSAEOPNOTSUPP**</span></span> | <span data-ttu-id="8d4cb-172">La commande IOCTL spécifiée n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="8d4cb-172">The specified IOCTL command is not supported.</span></span> <span data-ttu-id="8d4cb-173">Cette erreur est retournée si la modification IOCTL du **\_ BACKLOG d' \_ envoi \_ \_ SIO idéale** n’est pas prise en charge par le fournisseur de transport.</span><span class="sxs-lookup"><span data-stu-id="8d4cb-173">This error is returned if the **SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE** IOCTL is not supported by the transport provider.</span></span> <span data-ttu-id="8d4cb-174">Cette erreur est également retournée lorsqu’une tentative d’utilisation de la **SIO de modification de \_ \_ BACKLOG d’envoi \_ \_ idéale** est effectuée sur un socket datagramme.</span><span class="sxs-lookup"><span data-stu-id="8d4cb-174">This error is also returned when an attempt to use the **SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE** IOCTL is made on a datagram socket.</span></span> |

## <a name="remarks"></a><span data-ttu-id="8d4cb-175">Notes</span><span class="sxs-lookup"><span data-stu-id="8d4cb-175">Remarks</span></span>

<span data-ttu-id="8d4cb-176">L’IOCTL **SIO de modification du \_ BACKLOG d' \_ envoi \_ \_ idéal** est prise en charge sur Windows Server 2008, Windows Vista avec Service Pack 1 (SP1) et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="8d4cb-176">The **SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE** IOCTL is supported on Windows Server 2008, Windows Vista with Service Pack 1 (SP1), and later versions of the operating system.</span></span>

<span data-ttu-id="8d4cb-177">Lors de l’envoi de données via une connexion TCP à l’aide de Windows Sockets, il est important de conserver une quantité suffisante de données en attente (envoyées mais non acceptées) dans TCP afin d’obtenir le débit le plus élevé.</span><span class="sxs-lookup"><span data-stu-id="8d4cb-177">When sending data over a TCP connection using Windows sockets, it is important to keep a sufficient amount of data outstanding (sent but not acknowledged yet) in TCP in order to achieve the highest throughput.</span></span>
<span data-ttu-id="8d4cb-178">La valeur idéale pour la quantité de données en suspens pour obtenir le meilleur débit pour la connexion TCP est appelée taille du backlog d’envoi (ISB) idéal.</span><span class="sxs-lookup"><span data-stu-id="8d4cb-178">The ideal value for the amount of data outstanding to achieve the best throughput for the TCP connection is called the ideal send backlog (ISB) size.</span></span>
<span data-ttu-id="8d4cb-179">La valeur ISB est une fonction du produit Bandwidth-Delay de la connexion TCP et de la fenêtre de réception publiée du récepteur (et en partie la quantité de congestion dans le réseau).</span><span class="sxs-lookup"><span data-stu-id="8d4cb-179">The ISB value is a function of the bandwidth-delay product of the TCP connection and the receiver's advertised receive window (and partly the amount of congestion in the network).</span></span>

<span data-ttu-id="8d4cb-180">La valeur ISB par connexion est disponible à partir de l’implémentation du protocole TCP dans Windows Server 2008, Windows Vista avec SP1 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="8d4cb-180">The ISB value per connection is available from the TCP protocol implementation in Windows Server 2008, Windows Vista with SP1, and later versions of the operating system.</span></span>
<span data-ttu-id="8d4cb-181">L’IOCTL **SIO de modification de \_ BACKLOG d' \_ envoi \_ \_ idéale** peut être utilisée par une application pour recevoir une notification lorsque la valeur ISB change de manière dynamique pour une connexion.</span><span class="sxs-lookup"><span data-stu-id="8d4cb-181">The **SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE** IOCTL can be used by an application to get a notification when the ISB value changes dynamically for a connection.</span></span>

<span data-ttu-id="8d4cb-182">Sur Windows Server 2008, Windows Vista avec SP1 et les versions ultérieures du système d’exploitation, les **SIO de \_ \_ \_ journalisation des travaux en souffrance \_ d’envoi idéales** et SIO sont pris en charge sur les sockets orientés flux qui sont dans un état connecté. [**\_ \_ \_ \_**](sio-ideal-send-backlog-query.md)</span><span class="sxs-lookup"><span data-stu-id="8d4cb-182">On Windows Server 2008, Windows Vista with SP1, and later versions of the operating system, the **SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE** and [**SIO\_IDEAL\_SEND\_BACKLOG\_QUERY**](sio-ideal-send-backlog-query.md) IOCTLs are supported on stream-oriented sockets that are in a connected state.</span></span>

<span data-ttu-id="8d4cb-183">La plage de la valeur ISB pour une connexion TCP peut théoriquement varier de 0 à 16 mégaoctets au maximum.</span><span class="sxs-lookup"><span data-stu-id="8d4cb-183">The range for the ISB value for a TCP connection can theoretically vary from 0 to a maximum of 16 megabytes.</span></span>

<span data-ttu-id="8d4cb-184">Consultez la page de référence de la requête d’IOCTL de [**\_ Journal des travaux en \_ \_ souffrance \_ d’envoi SIO idéale**](sio-ideal-send-backlog-query.md) pour une utilisation classique du mécanisme ISB afin d’obtenir un meilleur débit sur les connexions de produits à bande passante élevée.</span><span class="sxs-lookup"><span data-stu-id="8d4cb-184">See the [**SIO\_IDEAL\_SEND\_BACKLOG\_QUERY**](sio-ideal-send-backlog-query.md) IOCTL reference page for typical usage of the ISB mechanism for achieving better throughput over high bandwidth-delay product connections.</span></span>

<span data-ttu-id="8d4cb-185">L’IOCTL **SIO de modification du \_ BACKLOG d' \_ envoi \_ \_ idéal** est autorisé uniquement sur un socket de flux qui est dans l’état connecté.</span><span class="sxs-lookup"><span data-stu-id="8d4cb-185">The **SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE** IOCTL is allowed only on a stream socket that is in the connected state.</span></span>
<span data-ttu-id="8d4cb-186">Dans le cas contraire, la fonction [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** échouera avec **WSAENOTCONN**.</span><span class="sxs-lookup"><span data-stu-id="8d4cb-186">Otherwise the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function will fail with **WSAENOTCONN**.</span></span>

<span data-ttu-id="8d4cb-187">L’IOCTL **SIO de modification du \_ BACKLOG d' \_ envoi \_ \_ idéal** n’utilise aucune mémoire tampon d’entrée ou de sortie et pends ou bloque jusqu’à ce qu’une modification d’ISB se produise sur la connexion sous-jacente.</span><span class="sxs-lookup"><span data-stu-id="8d4cb-187">The **SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE** IOCTL uses no input or output buffers and pends or blocks until an ISB change occurs on the underlying connection.</span></span>
<span data-ttu-id="8d4cb-188">Lorsque cette IOCTL est terminée, une application Winsock peut utiliser l’IOCTL de [**\_ requête d’envoi de \_ \_ BACKLOG \_ SIO idéale**](sio-ideal-send-backlog-query.md) pour récupérer la nouvelle valeur ISB sur la connexion.</span><span class="sxs-lookup"><span data-stu-id="8d4cb-188">When this IOCTL is completed, a Winsock application can use the [**SIO\_IDEAL\_SEND\_BACKLOG\_QUERY**](sio-ideal-send-backlog-query.md) IOCTL to retrieve the new ISB value on the connection.</span></span>

<span data-ttu-id="8d4cb-189">L’IOCTL **SIO de modification du \_ BACKLOG d' \_ envoi \_ \_ idéal** ne prend pas en charge le mode non bloquant.</span><span class="sxs-lookup"><span data-stu-id="8d4cb-189">The **SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE** IOCTL does not support non-blocking mode.</span></span>
<span data-ttu-id="8d4cb-190">Une application est autorisée à émettre cette IOCTL sur un socket non bloquant, mais le IOCTL bloque simplement ou met en attente jusqu’à ce que la valeur ISB change.</span><span class="sxs-lookup"><span data-stu-id="8d4cb-190">An application is allowed to issue this IOCTL on a non-blocking socket, but the IOCTL will simply block or pend until the ISB value changes.</span></span>

<span data-ttu-id="8d4cb-191">Si les deux paramètres *lpOverlapped* et *lpCompletionRoutine* sont NULL, le socket dans cette fonction sera traité comme un socket non superposé.</span><span class="sxs-lookup"><span data-stu-id="8d4cb-191">If both *lpOverlapped* and *lpCompletionRoutine* parameters are NULL, the socket in this function will be treated as a non-overlapped socket.</span></span>
<span data-ttu-id="8d4cb-192">Pour un socket non superposé, les paramètres *lpOverlapped* et *lpCompletionRoutine* sont ignorés, sauf que la fonction peut se bloquer si le socket *s* est en mode blocage.</span><span class="sxs-lookup"><span data-stu-id="8d4cb-192">For a non-overlapped socket, *lpOverlapped* and *lpCompletionRoutine* parameters are ignored, except that the function can block if socket *s* is in blocking mode.</span></span>
<span data-ttu-id="8d4cb-193">Si le socket *s* est en mode non bloquant, cette fonction sera toujours bloquée, car cette IOCTL particulière ne prend pas en charge le mode non bloquant.</span><span class="sxs-lookup"><span data-stu-id="8d4cb-193">If socket *s* is in non-blocking mode, this function will still block since this particular IOCTL does not support non-blocking mode.</span></span>

<span data-ttu-id="8d4cb-194">Pour les sockets superposés, les opérations qui ne peuvent pas être terminées immédiatement sont lancées et l’achèvement est indiqué ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="8d4cb-194">For overlapped sockets, operations that cannot be completed immediately will be initiated, and completion will be indicated at a later time.</span></span>

<span data-ttu-id="8d4cb-195">Toute IOCTL peut se bloquer indéfiniment, en fonction de l’implémentation du fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="8d4cb-195">Any IOCTL may block indefinitely, depending on the service provider's implementation.</span></span>
<span data-ttu-id="8d4cb-196">Si l’application ne peut pas tolérer le blocage dans un appel de fonction [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** , les e/s avec chevauchement sont conseillées pour les IOCTL qui sont particulièrement susceptibles de se bloquer.</span><span class="sxs-lookup"><span data-stu-id="8d4cb-196">If the application cannot tolerate blocking in a [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function call, overlapped I/O would be advised for IOCTLs that are especially likely to block.</span></span>

<span data-ttu-id="8d4cb-197">L’IOCTL **SIO de modification de \_ BACKLOG d’envoi idéale \_ \_ \_** fournit une notification et doit bloquer ou mettre en attente jusqu’à ce que la valeur ISB change.</span><span class="sxs-lookup"><span data-stu-id="8d4cb-197">The **SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE** IOCTL provides a notification and is expected to block or pend until the ISB value changes.</span></span>
<span data-ttu-id="8d4cb-198">Il est donc communément appelé de façon asynchrone avec le paramètre *lpOverlapped* défini sur une structure WSAOVERLAPPED valide.</span><span class="sxs-lookup"><span data-stu-id="8d4cb-198">So it would commonly be called asynchronously with the *lpOverlapped* parameter set to a valid WSAOVERLAPPED structure.</span></span>

<span data-ttu-id="8d4cb-199">La **modification IOCTL du \_ \_ \_ BACKLOG \_ d’envoi SIO idéale** peut échouer avec l’opération **WSAEINTR** ou **WSA \_ \_ abandonnée** dans les cas suivants :</span><span class="sxs-lookup"><span data-stu-id="8d4cb-199">The **SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE** IOCTL can fail with **WSAEINTR** or **WSA\_OPERATION\_ABORTED** under the following cases:</span></span>

* <span data-ttu-id="8d4cb-200">La connexion TCP est déconnectée en douceur dans le sens de l’envoi.</span><span class="sxs-lookup"><span data-stu-id="8d4cb-200">The TCP connection is gracefully disconnected in the send direction.</span></span> <span data-ttu-id="8d4cb-201">Cela peut se produire à la suite d’un appel à la fonction Shutdown avec la méthode How définie sur l' **\_ envoi SD**, d’un appel à la fonction **DisconnectEx** ou d’un appel à la fonction **TransmitFile** ou **TransmitPackets** avec le paramètre *dwFlags* défini sur **tf \_ Disconnect** ou **tf \_** Remain.</span><span class="sxs-lookup"><span data-stu-id="8d4cb-201">This can occur as a result of a call to shutdown function with the how parameter set to **SD\_SEND**, a call to the **DisconnectEx** function, or a call to the **TransmitFile** or **TransmitPackets** function with *dwFlags* parameter set to **TF\_DISCONNECT** or **TF\_REUSE**.</span></span>
* <span data-ttu-id="8d4cb-202">La connexion TCP a été réinitialisée ou abandonnée.</span><span class="sxs-lookup"><span data-stu-id="8d4cb-202">The TCP connection has been reset or aborted.</span></span>
* <span data-ttu-id="8d4cb-203">L’application émet un ioctl de **modification de BACKLOG d’envoi SIO idéal lorsqu’il existe déjà une demande de notification en \_ \_ \_ attente \_** .</span><span class="sxs-lookup"><span data-stu-id="8d4cb-203">The application issues a **SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE** IOCTL when there is already a pended notification request.</span></span> <span data-ttu-id="8d4cb-204">Seules 1 1 en **attente SIO demande de \_ \_ modification de \_ BACKLOG \_ d’envoi idéale** sont autorisées à la fois.</span><span class="sxs-lookup"><span data-stu-id="8d4cb-204">Only one one pended **SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE** request is allowed at a time.</span></span>
* <span data-ttu-id="8d4cb-205">La demande est annulée par le gestionnaire d’e/s.</span><span class="sxs-lookup"><span data-stu-id="8d4cb-205">The request is canceled by the I/O Manager.</span></span>
* <span data-ttu-id="8d4cb-206">Le socket est fermé.</span><span class="sxs-lookup"><span data-stu-id="8d4cb-206">The socket is closed.</span></span>

<span data-ttu-id="8d4cb-207">Deux fonctions wrapper Inline pour ces IOCTL sont définies dans le fichier d’en-tête *Ws2tcpip. h* .</span><span class="sxs-lookup"><span data-stu-id="8d4cb-207">Two inline wrapper functions for these IOCTLs are defined in the *Ws2tcpip.h* header file.</span></span>
<span data-ttu-id="8d4cb-208">Il est recommandé d’utiliser ces fonctions inline au lieu d’utiliser la **SIO \_ de \_ \_ journalisation \_ des travaux en souffrance Send idéale** et SIO des IOCTL de [**\_ \_ \_ \_ requête Send backlog**](sio-ideal-send-backlog-query.md) directement.</span><span class="sxs-lookup"><span data-stu-id="8d4cb-208">It is recommended that these inline functions be used instead of using the **SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE** and [**SIO\_IDEAL\_SEND\_BACKLOG\_QUERY**](sio-ideal-send-backlog-query.md) IOCTLs directly.</span></span>

<span data-ttu-id="8d4cb-209">La fonction de wrapper Inline pour le **SIO \_ idéal \_ Send \_ BACKLOG \_ change** IOCTL est la fonction **idealsendbacklognotify** .</span><span class="sxs-lookup"><span data-stu-id="8d4cb-209">The inline wrapper function for the **SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE** IOCTL is the **idealsendbacklognotify** function.</span></span>

<span data-ttu-id="8d4cb-210">La fonction de wrapper Inline pour l’IOCTL de [**requête d' \_ envoi de \_ \_ BACKLOG \_ SIO idéale**](sio-ideal-send-backlog-query.md) est la fonction **idealsendbacklogquery** .</span><span class="sxs-lookup"><span data-stu-id="8d4cb-210">The inline wrapper function for the [**SIO\_IDEAL\_SEND\_BACKLOG\_QUERY**](sio-ideal-send-backlog-query.md) IOCTL is the **idealsendbacklogquery** function.</span></span>

## <a name="see-also"></a><span data-ttu-id="8d4cb-211">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8d4cb-211">See also</span></span>

[<span data-ttu-id="8d4cb-212">**SIO_IDEAL_SEND_BACKLOG_QUERY**</span><span class="sxs-lookup"><span data-stu-id="8d4cb-212">**SIO_IDEAL_SEND_BACKLOG_QUERY**</span></span>](sio-ideal-send-backlog-query.md)

[<span data-ttu-id="8d4cb-213">**socle**</span><span class="sxs-lookup"><span data-stu-id="8d4cb-213">**socket**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-socket)

[<span data-ttu-id="8d4cb-214">**WSAGetLastError**</span><span class="sxs-lookup"><span data-stu-id="8d4cb-214">**WSAGetLastError**</span></span>](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)

[<span data-ttu-id="8d4cb-215">**WSAGetOverlappedResult**</span><span class="sxs-lookup"><span data-stu-id="8d4cb-215">**WSAGetOverlappedResult**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[<span data-ttu-id="8d4cb-216">**WSAIoctl**</span><span class="sxs-lookup"><span data-stu-id="8d4cb-216">**WSAIoctl**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[<span data-ttu-id="8d4cb-217">**WSAOVERLAPPED**</span><span class="sxs-lookup"><span data-stu-id="8d4cb-217">**WSAOVERLAPPED**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[<span data-ttu-id="8d4cb-218">**WSASocketA**</span><span class="sxs-lookup"><span data-stu-id="8d4cb-218">**WSASocketA**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[<span data-ttu-id="8d4cb-219">**WSASocketW**</span><span class="sxs-lookup"><span data-stu-id="8d4cb-219">**WSASocketW**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
