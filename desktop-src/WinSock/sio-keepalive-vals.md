---
description: Le code de contrôle active ou désactive le paramètre par connexion de l’option TCP Keep-Alive qui spécifie le délai d’expiration et l’intervalle de conservation TCP.
ms.assetid: c02e8ad5-bfad-489f-83bf-39b53fd68bde
title: Code de contrôle SIO_KEEPALIVE_VALS
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: ea8aabf452436ca2bbd6307366e7fc24f913dbdb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114903"
---
# <a name="sio_keepalive_vals-control-code"></a><span data-ttu-id="e7c17-103">Code de contrôle SIO_KEEPALIVE_VALS</span><span class="sxs-lookup"><span data-stu-id="e7c17-103">SIO_KEEPALIVE_VALS Control Code</span></span>

## <a name="description"></a><span data-ttu-id="e7c17-104">Description</span><span class="sxs-lookup"><span data-stu-id="e7c17-104">Description</span></span>

<span data-ttu-id="e7c17-105">Le code de contrôle **\_ KeepAlive SIO \_ Vals** active ou désactive le paramètre par connexion de l’option TCP Keep-Alive qui spécifie le délai d’expiration et l’intervalle de conservation TCP.</span><span class="sxs-lookup"><span data-stu-id="e7c17-105">The **SIO\_KEEPALIVE\_VALS** control code enables or disables the per-connection setting of the TCP keep-alive option which specifies the TCP keep-alive timeout and interval.</span></span>

<span data-ttu-id="e7c17-106">Pour effectuer cette opération, appelez la fonction [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** avec les paramètres suivants.</span><span class="sxs-lookup"><span data-stu-id="e7c17-106">To perform this operation, call the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function with the following parameters.</span></span>

```cpp
int WSAIoctl(
  (socket) s,              // descriptor identifying a socket
  SIO_KEEPALIVE_VALS,                  // dwIoControlCode
  (LPVOID) lpvInBuffer,    // pointer to tcp_keepalive struct
  (DWORD) cbInBuffer,      // length of input buffer
  NULL,         // output buffer
  0,       // size of output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

```cpp
int WSPIoctl(
  (socket) s,              // descriptor identifying a socket
  SIO_KEEPALIVE_VALS,                  // dwIoControlCode
  (LPVOID) lpvInBuffer,    // pointer to tcp_keepalive struct
  (DWORD) cbInBuffer,      // length of input buffer
  NULL,         // output buffer
  0,       // size of output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
  (LPWSATHREADID) lpThreadId,   // a WSATHREADID structure
  (LPINT) lpErrno   // a pointer to the error code.
);
```

## <a name="parameters"></a><span data-ttu-id="e7c17-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e7c17-107">Parameters</span></span>

### <a name="s"></a><span data-ttu-id="e7c17-108">s</span><span class="sxs-lookup"><span data-stu-id="e7c17-108">s</span></span>

<span data-ttu-id="e7c17-109">Descripteur identifiant un Socket.</span><span class="sxs-lookup"><span data-stu-id="e7c17-109">A descriptor identifying a socket.</span></span>

### <a name="dwiocontrolcode"></a><span data-ttu-id="e7c17-110">dwIoControlCode</span><span class="sxs-lookup"><span data-stu-id="e7c17-110">dwIoControlCode</span></span>

<span data-ttu-id="e7c17-111">Code de contrôle de l’opération.</span><span class="sxs-lookup"><span data-stu-id="e7c17-111">The control code for the operation.</span></span>
<span data-ttu-id="e7c17-112">Utilisez **SIO \_ KeepAlive \_ Vals** pour cette opération.</span><span class="sxs-lookup"><span data-stu-id="e7c17-112">Use **SIO\_KEEPALIVE\_VALS** for this operation.</span></span>

### <a name="lpvinbuffer"></a><span data-ttu-id="e7c17-113">lpvInBuffer</span><span class="sxs-lookup"><span data-stu-id="e7c17-113">lpvInBuffer</span></span>

<span data-ttu-id="e7c17-114">Pointeur vers la mémoire tampon d’entrée.</span><span class="sxs-lookup"><span data-stu-id="e7c17-114">A pointer to the input buffer.</span></span>
<span data-ttu-id="e7c17-115">Ce paramètre doit pointer vers une structure **\_ KeepAlive TCP** .</span><span class="sxs-lookup"><span data-stu-id="e7c17-115">This parameter should point to a **tcp\_keepalive** structure.</span></span>

### <a name="cbinbuffer"></a><span data-ttu-id="e7c17-116">cbInBuffer</span><span class="sxs-lookup"><span data-stu-id="e7c17-116">cbInBuffer</span></span>

<span data-ttu-id="e7c17-117">Taille, en octets, de la mémoire tampon d’entrée.</span><span class="sxs-lookup"><span data-stu-id="e7c17-117">The size, in bytes, of the input buffer.</span></span>
<span data-ttu-id="e7c17-118">Ce paramètre doit être supérieur ou égal à la taille de la **structure \_ KeepAlive TCP** vers laquelle pointe le paramètre *lpvInBuffer* .</span><span class="sxs-lookup"><span data-stu-id="e7c17-118">This parameter should equal to or greater than the size of the **tcp\_keepalive** structure pointed to by the *lpvInBuffer* parameter.</span></span>

### <a name="lpvoutbuffer"></a><span data-ttu-id="e7c17-119">lpvOutBuffer</span><span class="sxs-lookup"><span data-stu-id="e7c17-119">lpvOutBuffer</span></span>

<span data-ttu-id="e7c17-120">Pointeur vers la mémoire tampon de sortie.</span><span class="sxs-lookup"><span data-stu-id="e7c17-120">A pointer to the output buffer.</span></span>
<span data-ttu-id="e7c17-121">Ce paramètre n’est pas utilisé pour cette opération.</span><span class="sxs-lookup"><span data-stu-id="e7c17-121">This parameter is unused for this operation.</span></span>

### <a name="cboutbuffer"></a><span data-ttu-id="e7c17-122">cbOutBuffer</span><span class="sxs-lookup"><span data-stu-id="e7c17-122">cbOutBuffer</span></span>

<span data-ttu-id="e7c17-123">Taille, en octets, de la mémoire tampon de sortie.</span><span class="sxs-lookup"><span data-stu-id="e7c17-123">The size, in bytes, of the output buffer.</span></span>
<span data-ttu-id="e7c17-124">Ce paramètre doit avoir la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="e7c17-124">This parameter must be set to zero.</span></span>

### <a name="lpcbbytesreturned"></a><span data-ttu-id="e7c17-125">lpcbBytesReturned</span><span class="sxs-lookup"><span data-stu-id="e7c17-125">lpcbBytesReturned</span></span>

<span data-ttu-id="e7c17-126">Pointeur vers une variable qui reçoit la taille, en octets, des données stockées dans la mémoire tampon de sortie.</span><span class="sxs-lookup"><span data-stu-id="e7c17-126">A pointer to a variable that receives the size, in bytes, of the data stored in the output buffer.</span></span>
<span data-ttu-id="e7c17-127">Ce paramètre retourné pointe vers une valeur **DWORD** égale à zéro pour cette opération, car il n’y a pas de sortie.</span><span class="sxs-lookup"><span data-stu-id="e7c17-127">This returned parameter points to a **DWORD** value of zero for this operation, since there is no output.</span></span>

### <a name="lpvoverlapped"></a><span data-ttu-id="e7c17-128">lpvOverlapped</span><span class="sxs-lookup"><span data-stu-id="e7c17-128">lpvOverlapped</span></span>

<span data-ttu-id="e7c17-129">Pointeur vers une structure [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) .</span><span class="sxs-lookup"><span data-stu-id="e7c17-129">A pointer to a [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="e7c17-130">Si le socket *s* a été créé sans l’attribut Overlapped, le paramètre *lpOverlapped* est ignoré.</span><span class="sxs-lookup"><span data-stu-id="e7c17-130">If socket *s* was created without the overlapped attribute, the *lpOverlapped* parameter is ignored.</span></span>

<span data-ttu-id="e7c17-131">Si *s* a été ouvert avec l’attribut Overlapped et que le paramètre *lpOverlapped* n’a pas la **valeur null**, l’opération est exécutée en tant qu’opération Overlapped (asynchrone).</span><span class="sxs-lookup"><span data-stu-id="e7c17-131">If *s* was opened with the overlapped attribute and the *lpOverlapped* parameter is not **NULL**, the operation is performed as an overlapped (asynchronous) operation.</span></span>
<span data-ttu-id="e7c17-132">Dans ce cas, le paramètre *lpOverlapped* doit pointer vers une structure [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) valide.</span><span class="sxs-lookup"><span data-stu-id="e7c17-132">In this case, *lpOverlapped* parameter must point to a valid [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="e7c17-133">Pour les opérations avec chevauchement, la fonction [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** retourne immédiatement, et la méthode d’achèvement appropriée est signalée lorsque l’opération est terminée.</span><span class="sxs-lookup"><span data-stu-id="e7c17-133">For overlapped operations, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns immediately, and the appropriate completion method is signaled when the operation has been completed.</span></span>
<span data-ttu-id="e7c17-134">Sinon, la fonction ne retourne pas jusqu’à ce que l’opération soit terminée ou qu’une erreur se produise.</span><span class="sxs-lookup"><span data-stu-id="e7c17-134">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

### <a name="lpcompletionroutine"></a><span data-ttu-id="e7c17-135">lpCompletionRoutine</span><span class="sxs-lookup"><span data-stu-id="e7c17-135">lpCompletionRoutine</span></span>

<span data-ttu-id="e7c17-136">Type : \_ In_opt \_ [ **LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span><span class="sxs-lookup"><span data-stu-id="e7c17-136">Type: \_In_opt\_ [**LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span></span>

<span data-ttu-id="e7c17-137">Pointeur vers la routine de saisie semi-automatique appelée lorsque l’opération est terminée (ignoré pour les sockets non superposés).</span><span class="sxs-lookup"><span data-stu-id="e7c17-137">A pointer to the completion routine called when the operation has been completed (ignored for non-overlapped sockets).</span></span>

### <a name="lpthreadid"></a><span data-ttu-id="e7c17-138">lpThreadId</span><span class="sxs-lookup"><span data-stu-id="e7c17-138">lpThreadId</span></span>

<span data-ttu-id="e7c17-139">Pointeur vers une structure [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) qui doit être utilisée par le fournisseur dans un appel ultérieur à [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc).</span><span class="sxs-lookup"><span data-stu-id="e7c17-139">A pointer to a [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure to be used by the provider in a subsequent call to [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc).</span></span>
<span data-ttu-id="e7c17-140">Le fournisseur doit stocker la structure [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) référencée (pas le pointeur vers le même) jusqu’à ce que la fonction [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) soit retournée.</span><span class="sxs-lookup"><span data-stu-id="e7c17-140">The provider should store the referenced [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure (not the pointer to same) until after the [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) function returns.</span></span>

<span data-ttu-id="e7c17-141">**Remarque**  Ce paramètre s’applique uniquement à la fonction **WSPIoctl** .</span><span class="sxs-lookup"><span data-stu-id="e7c17-141">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

### <a name="lperrno"></a><span data-ttu-id="e7c17-142">lpErrno</span><span class="sxs-lookup"><span data-stu-id="e7c17-142">lpErrno</span></span>

<span data-ttu-id="e7c17-143">Pointeur vers le code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="e7c17-143">A pointer to the error code.</span></span>

<span data-ttu-id="e7c17-144">**Remarque**  Ce paramètre s’applique uniquement à la fonction **WSPIoctl** .</span><span class="sxs-lookup"><span data-stu-id="e7c17-144">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

## <a name="return-value"></a><span data-ttu-id="e7c17-145">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e7c17-145">Return value</span></span>

<span data-ttu-id="e7c17-146">Si l’opération se termine correctement, la fonction [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** retourne la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="e7c17-146">If the operation completes successfully, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns zero.</span></span>

<span data-ttu-id="e7c17-147">Si l’opération échoue ou est en attente, la fonction [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** retourne une **\_ erreur de socket**.</span><span class="sxs-lookup"><span data-stu-id="e7c17-147">If the operation fails or is pending, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns **SOCKET\_ERROR**.</span></span>
<span data-ttu-id="e7c17-148">Pour afficher les informations d’erreur étendues, appelez [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span><span class="sxs-lookup"><span data-stu-id="e7c17-148">To get extended error information, call [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>

| <span data-ttu-id="e7c17-149">Code d'erreur</span><span class="sxs-lookup"><span data-stu-id="e7c17-149">Error code</span></span> | <span data-ttu-id="e7c17-150">Signification</span><span class="sxs-lookup"><span data-stu-id="e7c17-150">Meaning</span></span> |
|------------|---------|
|<span data-ttu-id="e7c17-151">**\_e/s WSA \_ en attente**</span><span class="sxs-lookup"><span data-stu-id="e7c17-151">**WSA\_IO\_PENDING**</span></span> | <span data-ttu-id="e7c17-152">Une opération avec chevauchement a été correctement initiée et l’achèvement sera indiqué ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="e7c17-152">An overlapped operation was successfully initiated and completion will be indicated at a later time.</span></span> |
| <span data-ttu-id="e7c17-153">**\_opération WSA \_ abandonnée**</span><span class="sxs-lookup"><span data-stu-id="e7c17-153">**WSA\_OPERATION\_ABORTED**</span></span> | <span data-ttu-id="e7c17-154">Une opération avec chevauchement a été annulée en raison de la fermeture du socket ou de l’exécution de la commande **SIO_FLUSH IOCTL** .</span><span class="sxs-lookup"><span data-stu-id="e7c17-154">An overlapped operation was canceled due to the closure of the socket or the execution of the **SIO_FLUSH IOCTL** command.</span></span> |
| <span data-ttu-id="e7c17-155">**WSAEFAULT**</span><span class="sxs-lookup"><span data-stu-id="e7c17-155">**WSAEFAULT**</span></span> | <span data-ttu-id="e7c17-156">Le paramètre *lpOverlapped* ou *lpCompletionRoutine* n’est pas entièrement contenu dans une partie valide de l’espace d’adressage de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e7c17-156">The *lpOverlapped* or *lpCompletionRoutine* parameter is not totally contained in a valid part of the user address space.</span></span> |
| <span data-ttu-id="e7c17-157">**WSAEINPROGRESS**</span><span class="sxs-lookup"><span data-stu-id="e7c17-157">**WSAEINPROGRESS**</span></span> | <span data-ttu-id="e7c17-158">La fonction est appelée lorsqu’un rappel est en cours.</span><span class="sxs-lookup"><span data-stu-id="e7c17-158">The function is invoked when a callback is in progress.</span></span> |
| <span data-ttu-id="e7c17-159">**WSAEINTR**</span><span class="sxs-lookup"><span data-stu-id="e7c17-159">**WSAEINTR**</span></span> | <span data-ttu-id="e7c17-160">Une opération de blocage a été interrompue.</span><span class="sxs-lookup"><span data-stu-id="e7c17-160">A blocking operation was interrupted.</span></span> |
| <span data-ttu-id="e7c17-161">**WSAEINVAL**</span><span class="sxs-lookup"><span data-stu-id="e7c17-161">**WSAEINVAL**</span></span> | <span data-ttu-id="e7c17-162">Le paramètre *dwIoControlCode* n’est pas une commande valide, ou un paramètre d’entrée spécifié n’est pas acceptable, ou la commande n’est pas applicable au type de socket spécifié.</span><span class="sxs-lookup"><span data-stu-id="e7c17-162">The *dwIoControlCode* parameter is not a valid command, or a specified input parameter is not acceptable, or the command is not applicable to the type of socket specified.</span></span> |
| <span data-ttu-id="e7c17-163">**WSAENETDOWN**</span><span class="sxs-lookup"><span data-stu-id="e7c17-163">**WSAENETDOWN**</span></span> | <span data-ttu-id="e7c17-164">Le sous-système réseau a échoué.</span><span class="sxs-lookup"><span data-stu-id="e7c17-164">The network subsystem has failed.</span></span> |
| <span data-ttu-id="e7c17-165">**WSAENOPROTOOPT**</span><span class="sxs-lookup"><span data-stu-id="e7c17-165">**WSAENOPROTOOPT**</span></span> | <span data-ttu-id="e7c17-166">L’option de socket n’est pas prise en charge sur le protocole spécifié.</span><span class="sxs-lookup"><span data-stu-id="e7c17-166">The socket option is not supported on the specified protocol.</span></span> <span data-ttu-id="e7c17-167">Cette erreur est retournée pour un socket datagramme.</span><span class="sxs-lookup"><span data-stu-id="e7c17-167">This error is returned for a datagram socket.</span></span> |
| <span data-ttu-id="e7c17-168">**WSAENOTSOCK**</span><span class="sxs-lookup"><span data-stu-id="e7c17-168">**WSAENOTSOCK**</span></span> | <span data-ttu-id="e7c17-169">Le descripteur s n’est pas un Socket.</span><span class="sxs-lookup"><span data-stu-id="e7c17-169">The descriptor s is not a socket.</span></span> |
| <span data-ttu-id="e7c17-170">**WSAEOPNOTSUPP**</span><span class="sxs-lookup"><span data-stu-id="e7c17-170">**WSAEOPNOTSUPP**</span></span> | <span data-ttu-id="e7c17-171">La commande IOCTL spécifiée n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="e7c17-171">The specified IOCTL command is not supported.</span></span> <span data-ttu-id="e7c17-172">Cette erreur est retournée si le **SIO \_ KeepAlive \_ Vals** IOCTL n’est pas pris en charge par le fournisseur de transport.</span><span class="sxs-lookup"><span data-stu-id="e7c17-172">This error is returned if the **SIO\_KEEPALIVE\_VALS** IOCTL is not supported by the transport provider.</span></span> |

## <a name="remarks"></a><span data-ttu-id="e7c17-173">Notes</span><span class="sxs-lookup"><span data-stu-id="e7c17-173">Remarks</span></span>

<span data-ttu-id="e7c17-174">Le **SIO \_ KeepAlive \_ Vals** IOCTL est pris en charge sur Windows 2000 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="e7c17-174">The **SIO\_KEEPALIVE\_VALS** IOCTL is supported on Windows 2000 and later versions of the operating system.</span></span>

<span data-ttu-id="e7c17-175">Le code de contrôle **\_ KeepAlive \_ Vals SIO** active ou désactive le paramètre par connexion de l’option TCP Keep-Alive qui spécifie le délai d’expiration et l’intervalle de conservation TCP utilisés pour les paquets TCP Keep-Alive.</span><span class="sxs-lookup"><span data-stu-id="e7c17-175">The **SIO\_KEEPALIVE\_VALS** control code enables or disables the per-connection setting of the TCP keep-alive option which specifies the TCP keep-alive timeout and interval used for TCP keep-alive packets.</span></span>
<span data-ttu-id="e7c17-176">Pour plus d’informations sur l’option Keep-Alive, consultez la section 4.2.3.6 sur la configuration requise pour les hôtes Internet — couches de communication spécifiées dans le document RFC 1122 disponible sur le [site Web](https://www.ietf.org/rfc/rfc1122.txt)de l’IETF.</span><span class="sxs-lookup"><span data-stu-id="e7c17-176">For more information on the keep-alive option, see section 4.2.3.6 on the Requirements for Internet Hosts—Communication Layers specified in RFC 1122 available at the [IETF website](https://www.ietf.org/rfc/rfc1122.txt).</span></span>
<span data-ttu-id="e7c17-177">(Cette ressource peut uniquement être disponible en anglais.)</span><span class="sxs-lookup"><span data-stu-id="e7c17-177">(This resource may only be available in English.)</span></span>

<span data-ttu-id="e7c17-178">Le paramètre *lpvInBuffer* doit pointer vers une structure **TCP \_ KeepAlive** définie dans le fichier d’en-tête *Mstcpip. h* .</span><span class="sxs-lookup"><span data-stu-id="e7c17-178">The *lpvInBuffer* parameter should point to a **tcp\_keepalive** structure defined in the *Mstcpip.h* header file.</span></span>
<span data-ttu-id="e7c17-179">Cette structure est définie comme suit :</span><span class="sxs-lookup"><span data-stu-id="e7c17-179">This structure is defined as follows:</span></span>

```cpp
/* Argument structure for SIO_KEEPALIVE_VALS */
struct tcp_keepalive {
    u_long  onoff;
    u_long  keepalivetime;
    u_long  keepaliveinterval;
};
```

<span data-ttu-id="e7c17-180">La valeur spécifiée dans le membre **microphone** détermine si TCP Keep-Alive est activé ou désactivé.</span><span class="sxs-lookup"><span data-stu-id="e7c17-180">The value specified in the **onoff** member determines if TCP keep-alive is enabled or disabled.</span></span>
<span data-ttu-id="e7c17-181">Si le membre **microphone** est défini sur une valeur différente de zéro, TCP Keep-Alive est activé et les autres membres de la structure sont utilisés.</span><span class="sxs-lookup"><span data-stu-id="e7c17-181">If the **onoff** member is set to a nonzero value, TCP keep-alive is enabled and the other members in the structure are used.</span></span>
<span data-ttu-id="e7c17-182">Le membre **keepAliveTime** spécifie le délai d’attente, en millisecondes, sans activité jusqu’à l’envoi du premier paquet Keep-Alive.</span><span class="sxs-lookup"><span data-stu-id="e7c17-182">The **keepalivetime** member specifies the timeout, in milliseconds, with no activity until the first keep-alive packet is sent.</span></span>
<span data-ttu-id="e7c17-183">Le membre **keepAliveInterval** spécifie l’intervalle, en millisecondes, entre l’envoi des paquets Keep-Alive successifs si aucun accusé de réception n’est reçu.</span><span class="sxs-lookup"><span data-stu-id="e7c17-183">The **keepaliveinterval** member specifies the interval, in milliseconds, between when successive keep-alive packets are sent if no acknowledgement is received.</span></span>

<span data-ttu-id="e7c17-184">L’option [**SO_KEEPALIVE**](/windows/desktop/winsock/so-keepalive) , qui est l’une des [**Options de socket SOL_SOCKET**](/windows/desktop/winsock/sol-socket-socket-options), peut également être utilisée pour activer ou désactiver le protocole TCP Keep-Alive sur une connexion, ainsi que pour interroger l’état actuel de cette option.</span><span class="sxs-lookup"><span data-stu-id="e7c17-184">The [**SO_KEEPALIVE**](/windows/desktop/winsock/so-keepalive) option, which is one of the [**SOL_SOCKET Socket Options**](/windows/desktop/winsock/sol-socket-socket-options), can also be used to enable or disable the TCP keep-alive on a connection, as well as query the current state of this option.</span></span>
<span data-ttu-id="e7c17-185">Pour demander si TCP Keep-Alive est activé sur un socket, la fonction getsockopt peut être appelée avec l’option [**SO_KEEPALIVE**](/windows/desktop/winsock/so-keepalive) .</span><span class="sxs-lookup"><span data-stu-id="e7c17-185">To query whether TCP keep-alive is enabled on a socket, the getsockopt function can be called with the [**SO_KEEPALIVE**](/windows/desktop/winsock/so-keepalive) option.</span></span>
<span data-ttu-id="e7c17-186">Pour activer ou désactiver le protocole TCP Keep-Alive, la fonction **setsockopt** peut être appelée avec l’option [**SO_KEEPALIVE**](/windows/desktop/winsock/so-keepalive) .</span><span class="sxs-lookup"><span data-stu-id="e7c17-186">To enable or disable TCP keep-alive, the **setsockopt** function can be called with the [**SO_KEEPALIVE**](/windows/desktop/winsock/so-keepalive) option.</span></span>
<span data-ttu-id="e7c17-187">Si TCP Keep-Alive est activé avec [**SO_KEEPALIVE**](/windows/desktop/winsock/so-keepalive), les paramètres TCP par défaut sont utilisés pour le délai d’expiration et l’intervalle Keep-Alive, à moins que ces valeurs aient été modifiées à l’aide de **SIO \_ KeepAlive \_ Vals**.</span><span class="sxs-lookup"><span data-stu-id="e7c17-187">If TCP keep-alive is enabled with [**SO_KEEPALIVE**](/windows/desktop/winsock/so-keepalive), then the default TCP settings are used for keep-alive timeout and interval unless these values have been changed using **SIO\_KEEPALIVE\_VALS**.</span></span>

<span data-ttu-id="e7c17-188">La valeur par défaut au niveau du système du délai d’expiration Keep-Alive est contrôlable via le paramètre de Registre [**keepAliveTime**](/previous-versions/windows/it-pro/windows-server-2003/cc782936(v=ws.10)) qui prend une valeur en millisecondes.</span><span class="sxs-lookup"><span data-stu-id="e7c17-188">The default system-wide value of the keep-alive timeout is controllable through the [**KeepAliveTime**](/previous-versions/windows/it-pro/windows-server-2003/cc782936(v=ws.10)) registry setting which takes a value in milliseconds.</span></span> <span data-ttu-id="e7c17-189">Si la clé n’est pas définie, le délai d’expiration persistant par défaut est de 2 heures.</span><span class="sxs-lookup"><span data-stu-id="e7c17-189">If the key is not set, the default keep-alive timeout is 2 hours.</span></span>
<span data-ttu-id="e7c17-190">La valeur par défaut à l’ensemble du système de l’intervalle Keep-Alive est contrôlable via le paramètre de Registre [**keepAliveInterval**](/previous-versions/windows/it-pro/windows-server-2003/cc758083(v=ws.10)) qui prend une valeur en millisecondes.</span><span class="sxs-lookup"><span data-stu-id="e7c17-190">The default system-wide value of the keep-alive interval is controllable through the [**KeepAliveInterval**](/previous-versions/windows/it-pro/windows-server-2003/cc758083(v=ws.10)) registry setting which takes a value in milliseconds.</span></span> <span data-ttu-id="e7c17-191">Si la clé n’est pas définie, l’intervalle de conservation par défaut est de 1 seconde.</span><span class="sxs-lookup"><span data-stu-id="e7c17-191">If the key is not set, the default keep-alive interval is 1 second.</span></span>

<span data-ttu-id="e7c17-192">Sur Windows Vista et versions ultérieures, le nombre de sondes KeepAlive (retransmissions de données) est défini sur 10 et ne peut pas être modifié.</span><span class="sxs-lookup"><span data-stu-id="e7c17-192">On Windows Vista and later, the number of keep-alive probes (data retransmissions) is set to 10 and cannot be changed.</span></span>

<span data-ttu-id="e7c17-193">Sur Windows Server 2003, Windows XP et Windows 2000, le paramètre par défaut pour le nombre de sondes KeepAlive est 5.</span><span class="sxs-lookup"><span data-stu-id="e7c17-193">On Windows Server 2003, Windows XP, and Windows 2000, the default setting for number of keep-alive probes is 5.</span></span>
<span data-ttu-id="e7c17-194">Le nombre de sondes KeepAlive est contrôlable via les paramètres de Registre **TcpMaxDataRetransmissions** et [**PPTPTcpMaxDataRetransmissions**](/previous-versions/windows/it-pro/windows-server-2003/cc775408(v=ws.10)) .</span><span class="sxs-lookup"><span data-stu-id="e7c17-194">The number of keep-alive probes is controllable through the **TcpMaxDataRetransmissions** and [**PPTPTcpMaxDataRetransmissions**](/previous-versions/windows/it-pro/windows-server-2003/cc775408(v=ws.10)) registry settings.</span></span>
<span data-ttu-id="e7c17-195">Le nombre de sondes KeepAlive est défini sur la plus grande des deux valeurs de clé de registre.</span><span class="sxs-lookup"><span data-stu-id="e7c17-195">The number of keep-alive probes is set to the larger of the two registry key values.</span></span>
<span data-ttu-id="e7c17-196">Si ce nombre est 0, les sondes de conservation des connexions actives ne sont pas envoyées.</span><span class="sxs-lookup"><span data-stu-id="e7c17-196">If this number is 0, then keep-alive probes will not be sent.</span></span>
<span data-ttu-id="e7c17-197">Si ce nombre est supérieur à 255, il est ajusté à 255.</span><span class="sxs-lookup"><span data-stu-id="e7c17-197">If this number is above 255, then it is adjusted to 255.</span></span>

## <a name="see-also"></a><span data-ttu-id="e7c17-198">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e7c17-198">See also</span></span>

<span data-ttu-id="e7c17-199">[**KeepAliveTime**](/previous-versions/windows/it-pro/windows-server-2003/cc782936(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="e7c17-199">[**KeepAliveTime**](/previous-versions/windows/it-pro/windows-server-2003/cc782936(v=ws.10))</span></span>

<span data-ttu-id="e7c17-200">[**KeepAliveInterval**](/previous-versions/windows/it-pro/windows-server-2003/cc758083(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="e7c17-200">[**KeepAliveInterval**](/previous-versions/windows/it-pro/windows-server-2003/cc758083(v=ws.10))</span></span>

<span data-ttu-id="e7c17-201">[**PPTPTcpMaxDataRetransmissions**](/previous-versions/windows/it-pro/windows-server-2003/cc775408(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="e7c17-201">[**PPTPTcpMaxDataRetransmissions**](/previous-versions/windows/it-pro/windows-server-2003/cc775408(v=ws.10))</span></span>

[<span data-ttu-id="e7c17-202">socle</span><span class="sxs-lookup"><span data-stu-id="e7c17-202">socket</span></span>](/windows/desktop/api/winsock2/nf-winsock2-socket)

[<span data-ttu-id="e7c17-203">**SO_KEEPALIVE**</span><span class="sxs-lookup"><span data-stu-id="e7c17-203">**SO_KEEPALIVE**</span></span>](/windows/desktop/winsock/so-keepalive)

[<span data-ttu-id="e7c17-204">**WSAGetLastError**</span><span class="sxs-lookup"><span data-stu-id="e7c17-204">**WSAGetLastError**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetlasterror)

[<span data-ttu-id="e7c17-205">**WSAGetOverlappedResult**</span><span class="sxs-lookup"><span data-stu-id="e7c17-205">**WSAGetOverlappedResult**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[<span data-ttu-id="e7c17-206">**WSAIoctl**</span><span class="sxs-lookup"><span data-stu-id="e7c17-206">**WSAIoctl**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[<span data-ttu-id="e7c17-207">**WSAOVERLAPPED**</span><span class="sxs-lookup"><span data-stu-id="e7c17-207">**WSAOVERLAPPED**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[<span data-ttu-id="e7c17-208">**WSASocketA**</span><span class="sxs-lookup"><span data-stu-id="e7c17-208">**WSASocketA**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[<span data-ttu-id="e7c17-209">**WSASocketW**</span><span class="sxs-lookup"><span data-stu-id="e7c17-209">**WSASocketW**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
