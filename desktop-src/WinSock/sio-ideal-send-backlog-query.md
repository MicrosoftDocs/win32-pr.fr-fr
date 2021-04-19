---
description: Le code de contrôle récupère la valeur de backlog d’envoi idéale pour la connexion sous-jacente.
ms.assetid: 03fe964b-26f7-4af7-83bf-62cc877d01a8
title: Code de contrôle SIO_IDEAL_SEND_BACKLOG_QUERY
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 440e42477a8939a62eeb84b800c0fd8feead5aab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521100"
---
# <a name="sio_ideal_send_backlog_query-control-code"></a><span data-ttu-id="dc170-103">Code de contrôle SIO_IDEAL_SEND_BACKLOG_QUERY</span><span class="sxs-lookup"><span data-stu-id="dc170-103">SIO_IDEAL_SEND_BACKLOG_QUERY Control Code</span></span>

## <a name="description"></a><span data-ttu-id="dc170-104">Description</span><span class="sxs-lookup"><span data-stu-id="dc170-104">Description</span></span>

<span data-ttu-id="dc170-105">Le code de contrôle de **\_ requête de journal des travaux en \_ \_ souffrance \_ d’envoi idéal SIO** récupère la valeur d’un backlog d’envoi idéal pour la connexion sous-jacente.</span><span class="sxs-lookup"><span data-stu-id="dc170-105">The **SIO\_IDEAL\_SEND\_BACKLOG\_QUERY** control code retrieves the ideal send backlog (ISB) value for the underlying connection.</span></span>

<span data-ttu-id="dc170-106">Pour effectuer cette opération, appelez la fonction [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** avec les paramètres suivants.</span><span class="sxs-lookup"><span data-stu-id="dc170-106">To perform this operation, call the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function with the following parameters.</span></span>

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_IDEAL_SEND_BACKLOG_QUERY, // dwIoControlCode
  NULL,                         // lpvInBuffer
  0,                            // cbInBuffer
  (LPVOID) lpvOutBuffer,         // output buffer
  (DWORD) cbOutBuffer,       // size of output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

```cpp
int WSPIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_IDEAL_SEND_BACKLOG_QUERY, // dwIoControlCode
  NULL,                         // lpvInBuffer
  0,                            // cbInBuffer
  (LPVOID) lpvOutBuffer,         // output buffer
  (DWORD) cbOutBuffer,       // size of output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
  (LPWSATHREADID) lpThreadId,   // a WSATHREADID structure
  (LPINT) lpErrno   // a pointer to the error code.
);
```

## <a name="parameters"></a><span data-ttu-id="dc170-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dc170-107">Parameters</span></span>

### <a name="s"></a><span data-ttu-id="dc170-108">s</span><span class="sxs-lookup"><span data-stu-id="dc170-108">s</span></span>

<span data-ttu-id="dc170-109">Descripteur identifiant un Socket.</span><span class="sxs-lookup"><span data-stu-id="dc170-109">A descriptor identifying a socket.</span></span>

### <a name="dwiocontrolcode"></a><span data-ttu-id="dc170-110">dwIoControlCode</span><span class="sxs-lookup"><span data-stu-id="dc170-110">dwIoControlCode</span></span>

<span data-ttu-id="dc170-111">Code de contrôle de l’opération.</span><span class="sxs-lookup"><span data-stu-id="dc170-111">The control code for the operation.</span></span>
<span data-ttu-id="dc170-112">Utilisez **SIO \_ pour \_ \_ \_** cette opération.</span><span class="sxs-lookup"><span data-stu-id="dc170-112">Use **SIO\_IDEAL\_SEND\_BACKLOG\_QUERY** for this operation.</span></span>

### <a name="lpvinbuffer"></a><span data-ttu-id="dc170-113">lpvInBuffer</span><span class="sxs-lookup"><span data-stu-id="dc170-113">lpvInBuffer</span></span>

<span data-ttu-id="dc170-114">Pointeur vers la mémoire tampon d’entrée.</span><span class="sxs-lookup"><span data-stu-id="dc170-114">A pointer to the input buffer.</span></span>
<span data-ttu-id="dc170-115">Ce paramètre n’est pas utilisé pour cette opération.</span><span class="sxs-lookup"><span data-stu-id="dc170-115">This parameter is unused for this operation.</span></span>

### <a name="cbinbuffer"></a><span data-ttu-id="dc170-116">cbInBuffer</span><span class="sxs-lookup"><span data-stu-id="dc170-116">cbInBuffer</span></span>

<span data-ttu-id="dc170-117">Taille, en octets, de la mémoire tampon d’entrée.</span><span class="sxs-lookup"><span data-stu-id="dc170-117">The size, in bytes, of the input buffer.</span></span>
<span data-ttu-id="dc170-118">Ce paramètre n’est pas utilisé pour cette opération.</span><span class="sxs-lookup"><span data-stu-id="dc170-118">This parameter is unused for this operation.</span></span>

### <a name="lpvoutbuffer"></a><span data-ttu-id="dc170-119">lpvOutBuffer</span><span class="sxs-lookup"><span data-stu-id="dc170-119">lpvOutBuffer</span></span>

<span data-ttu-id="dc170-120">Pointeur vers la mémoire tampon de sortie.</span><span class="sxs-lookup"><span data-stu-id="dc170-120">A pointer to the output buffer.</span></span>
<span data-ttu-id="dc170-121">Ce paramètre doit pointer vers un type de données **ULong** si les paramètres *lpOverlapped* et *lpCompletionRoutine* ont la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="dc170-121">This parameter should point to a **ULONG** data type if the *lpOverlapped* and *lpCompletionRoutine* parameters are **NULL**.</span></span>

### <a name="cboutbuffer"></a><span data-ttu-id="dc170-122">cbOutBuffer</span><span class="sxs-lookup"><span data-stu-id="dc170-122">cbOutBuffer</span></span>

<span data-ttu-id="dc170-123">Taille, en octets, de la mémoire tampon de sortie.</span><span class="sxs-lookup"><span data-stu-id="dc170-123">The size, in bytes, of the output buffer.</span></span>
<span data-ttu-id="dc170-124">Ce paramètre doit avoir au moins la taille d’un type de données **ULong** .</span><span class="sxs-lookup"><span data-stu-id="dc170-124">This parameter must be at least the size of a **ULONG** data type.</span></span>

### <a name="lpcbbytesreturned"></a><span data-ttu-id="dc170-125">lpcbBytesReturned</span><span class="sxs-lookup"><span data-stu-id="dc170-125">lpcbBytesReturned</span></span>

<span data-ttu-id="dc170-126">Pointeur vers une variable qui reçoit la taille, en octets, des données stockées dans la mémoire tampon de sortie.</span><span class="sxs-lookup"><span data-stu-id="dc170-126">A pointer to a variable that receives the size, in bytes, of the data stored in the output buffer.</span></span>

<span data-ttu-id="dc170-127">Si la mémoire tampon de sortie est trop petite, l’appel échoue, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) retourne [**WSAEINVAL**](windows-sockets-error-codes-2.md)et le paramètre *LpcbBytesReturned* pointe vers une valeur **DWORD** égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="dc170-127">If the output buffer is too small, the call fails, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) returns [**WSAEINVAL**](windows-sockets-error-codes-2.md), and the *lpcbBytesReturned* parameter points to a **DWORD** value of zero.</span></span>

<span data-ttu-id="dc170-128">Si *lpOverlapped* a la valeur **null**, la valeur **DWORD** vers laquelle pointe le paramètre *lpcbBytesReturned* retourné sur un appel réussi ne peut pas être égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="dc170-128">If *lpOverlapped* is **NULL**, the **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned on a successful call cannot be zero.</span></span>

<span data-ttu-id="dc170-129">Si le paramètre *lpOverlapped* n’a pas la **valeur null** pour les sockets superposés, les opérations qui ne peuvent pas être terminées immédiatement seront lancées et l’achèvement sera indiqué ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="dc170-129">If the *lpOverlapped* parameter is not **NULL** for overlapped sockets, operations that cannot be completed immediately will be initiated, and completion will be indicated at a later time.</span></span>
<span data-ttu-id="dc170-130">La valeur **DWORD** pointée par le paramètre *lpcbBytesReturned* retourné peut être égale à zéro, car la taille des données stockées ne peut pas être déterminée tant que l’opération avec chevauchement n’est pas terminée.</span><span class="sxs-lookup"><span data-stu-id="dc170-130">The **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned may be zero since the size of the data stored can't be determined until the overlapped operation has completed.</span></span>
<span data-ttu-id="dc170-131">L’état d’achèvement final peut être récupéré lorsque la méthode d’achèvement appropriée est signalée lorsque l’opération est terminée.</span><span class="sxs-lookup"><span data-stu-id="dc170-131">The final completion status can be retrieved when the appropriate completion method is signaled when the operation has completed.</span></span>

### <a name="lpvoverlapped"></a><span data-ttu-id="dc170-132">lpvOverlapped</span><span class="sxs-lookup"><span data-stu-id="dc170-132">lpvOverlapped</span></span>

<span data-ttu-id="dc170-133">Pointeur vers une structure [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) .</span><span class="sxs-lookup"><span data-stu-id="dc170-133">A pointer to a [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="dc170-134">Si le socket *s* a été créé sans l’attribut Overlapped, le paramètre *lpOverlapped* est ignoré.</span><span class="sxs-lookup"><span data-stu-id="dc170-134">If socket *s* was created without the overlapped attribute, the *lpOverlapped* parameter is ignored.</span></span>

<span data-ttu-id="dc170-135">Si *s* a été ouvert avec l’attribut Overlapped et que le paramètre *lpOverlapped* n’a pas la **valeur null**, l’opération est exécutée en tant qu’opération Overlapped (asynchrone).</span><span class="sxs-lookup"><span data-stu-id="dc170-135">If *s* was opened with the overlapped attribute and the *lpOverlapped* parameter is not **NULL**, the operation is performed as an overlapped (asynchronous) operation.</span></span>
<span data-ttu-id="dc170-136">Dans ce cas, le paramètre *lpOverlapped* doit pointer vers une structure [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) valide.</span><span class="sxs-lookup"><span data-stu-id="dc170-136">In this case, *lpOverlapped* parameter must point to a valid [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="dc170-137">Pour les opérations avec chevauchement, la fonction [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** retourne immédiatement, et la méthode d’achèvement appropriée est signalée lorsque l’opération est terminée.</span><span class="sxs-lookup"><span data-stu-id="dc170-137">For overlapped operations, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns immediately, and the appropriate completion method is signaled when the operation has been completed.</span></span>
<span data-ttu-id="dc170-138">Sinon, la fonction ne retourne pas jusqu’à ce que l’opération soit terminée ou qu’une erreur se produise.</span><span class="sxs-lookup"><span data-stu-id="dc170-138">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

### <a name="lpcompletionroutine"></a><span data-ttu-id="dc170-139">lpCompletionRoutine</span><span class="sxs-lookup"><span data-stu-id="dc170-139">lpCompletionRoutine</span></span>

<span data-ttu-id="dc170-140">Type : \_ In_opt \_ [ **LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span><span class="sxs-lookup"><span data-stu-id="dc170-140">Type: \_In_opt\_ [**LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span></span>

<span data-ttu-id="dc170-141">Pointeur vers la routine de saisie semi-automatique appelée lorsque l’opération est terminée (ignoré pour les sockets non superposés).</span><span class="sxs-lookup"><span data-stu-id="dc170-141">A pointer to the completion routine called when the operation has been completed (ignored for non-overlapped sockets).</span></span>

### <a name="lpthreadid"></a><span data-ttu-id="dc170-142">lpThreadId</span><span class="sxs-lookup"><span data-stu-id="dc170-142">lpThreadId</span></span>

<span data-ttu-id="dc170-143">Pointeur vers une structure [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) qui doit être utilisée par le fournisseur dans un appel ultérieur à [**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc).</span><span class="sxs-lookup"><span data-stu-id="dc170-143">A pointer to a [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure to be used by the provider in a subsequent call to [**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc).</span></span>
<span data-ttu-id="dc170-144">Le fournisseur doit stocker la structure [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) référencée (pas le pointeur vers le même) jusqu’à ce que la fonction [**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc) soit retournée.</span><span class="sxs-lookup"><span data-stu-id="dc170-144">The provider should store the referenced [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure (not the pointer to same) until after the [**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc) function returns.</span></span>

<span data-ttu-id="dc170-145">**Remarque**  Ce paramètre s’applique uniquement à la fonction **WSPIoctl** .</span><span class="sxs-lookup"><span data-stu-id="dc170-145">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

### <a name="lperrno"></a><span data-ttu-id="dc170-146">lpErrno</span><span class="sxs-lookup"><span data-stu-id="dc170-146">lpErrno</span></span>

<span data-ttu-id="dc170-147">Pointeur vers le code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="dc170-147">A pointer to the error code.</span></span>

<span data-ttu-id="dc170-148">**Remarque**  Ce paramètre s’applique uniquement à la fonction **WSPIoctl** .</span><span class="sxs-lookup"><span data-stu-id="dc170-148">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

## <a name="return-value"></a><span data-ttu-id="dc170-149">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="dc170-149">Return value</span></span>

<span data-ttu-id="dc170-150">Si l’opération se termine correctement, la fonction [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** retourne la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="dc170-150">If the operation completes successfully, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns zero.</span></span>

<span data-ttu-id="dc170-151">Si l’opération échoue ou est en attente, la fonction [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** retourne une **\_ erreur de socket**.</span><span class="sxs-lookup"><span data-stu-id="dc170-151">If the operation fails or is pending, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns **SOCKET\_ERROR**.</span></span>
<span data-ttu-id="dc170-152">Pour afficher les informations d’erreur étendues, appelez [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span><span class="sxs-lookup"><span data-stu-id="dc170-152">To get extended error information, call [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>

| <span data-ttu-id="dc170-153">Code d'erreur</span><span class="sxs-lookup"><span data-stu-id="dc170-153">Error code</span></span> | <span data-ttu-id="dc170-154">Signification</span><span class="sxs-lookup"><span data-stu-id="dc170-154">Meaning</span></span> |
|------------|---------|
| <span data-ttu-id="dc170-155">**\_e/s WSA \_ en attente**</span><span class="sxs-lookup"><span data-stu-id="dc170-155">**WSA\_IO\_PENDING**</span></span> | <span data-ttu-id="dc170-156">Une opération avec chevauchement a été correctement initiée et l’achèvement sera indiqué ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="dc170-156">An overlapped operation was successfully initiated and completion will be indicated at a later time.</span></span> |
| <span data-ttu-id="dc170-157">**\_opération WSA \_ abandonnée**</span><span class="sxs-lookup"><span data-stu-id="dc170-157">**WSA\_OPERATION\_ABORTED**</span></span> | <span data-ttu-id="dc170-158">Une opération avec chevauchement a été annulée en raison de la fermeture du socket ou de l’exécution de la commande **SIO \_ flush** ioctl.</span><span class="sxs-lookup"><span data-stu-id="dc170-158">An overlapped operation was canceled due to the closure of the socket or the execution of the **SIO\_FLUSH** IOCTL command.</span></span> |
| <span data-ttu-id="dc170-159">**WSAEFAULT**</span><span class="sxs-lookup"><span data-stu-id="dc170-159">**WSAEFAULT**</span></span> | <span data-ttu-id="dc170-160">Le paramètre *lpvInBuffer*, *lpvoutBuffer*, *lpcbBytesReturned*, *lpOverlapped* ou *lpCompletionRoutine* n’est pas entièrement contenu dans une partie valide de l’espace d’adressage de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="dc170-160">The *lpvInBuffer*, *lpvoutBuffer*, *lpcbBytesReturned*, *lpOverlapped* or *lpCompletionRoutine* parameter is not totally contained in a valid part of the user address space.</span></span> |
| <span data-ttu-id="dc170-161">**WSAEINPROGRESS**</span><span class="sxs-lookup"><span data-stu-id="dc170-161">**WSAEINPROGRESS**</span></span> | <span data-ttu-id="dc170-162">La fonction est appelée lorsqu’un rappel est en cours.</span><span class="sxs-lookup"><span data-stu-id="dc170-162">The function is invoked when a callback is in progress.</span></span> |
| <span data-ttu-id="dc170-163">**WSAEINTR**</span><span class="sxs-lookup"><span data-stu-id="dc170-163">**WSAEINTR**</span></span> | <span data-ttu-id="dc170-164">Une opération de blocage a été interrompue.</span><span class="sxs-lookup"><span data-stu-id="dc170-164">A blocking operation was interrupted.</span></span> |
| <span data-ttu-id="dc170-165">**WSAEINVAL**</span><span class="sxs-lookup"><span data-stu-id="dc170-165">**WSAEINVAL**</span></span> | <span data-ttu-id="dc170-166">Le paramètre *dwIoControlCode* n’est pas une commande valide, ou un paramètre d’entrée spécifié n’est pas acceptable, ou la commande n’est pas applicable au type de socket spécifié.</span><span class="sxs-lookup"><span data-stu-id="dc170-166">The *dwIoControlCode* parameter is not a valid command, or a specified input parameter is not acceptable, or the command is not applicable to the type of socket specified.</span></span> <span data-ttu-id="dc170-167">Cette erreur est retournée si le paramètre *cbOutBuffer* est inférieur à la taille d’un type de données **ULong** .</span><span class="sxs-lookup"><span data-stu-id="dc170-167">This error is returned if the *cbOutBuffer* parameter is less than the size of a **ULONG** data type.</span></span>
| <span data-ttu-id="dc170-168">**WSAENETDOWN**</span><span class="sxs-lookup"><span data-stu-id="dc170-168">**WSAENETDOWN**</span></span> | <span data-ttu-id="dc170-169">Le sous-système réseau a échoué.</span><span class="sxs-lookup"><span data-stu-id="dc170-169">The network subsystem has failed.</span></span> |
| <span data-ttu-id="dc170-170">**WSAENOPROTOOPT**</span><span class="sxs-lookup"><span data-stu-id="dc170-170">**WSAENOPROTOOPT**</span></span> | <span data-ttu-id="dc170-171">L’option de socket n’est pas prise en charge sur le protocole spécifié.</span><span class="sxs-lookup"><span data-stu-id="dc170-171">The socket option is not supported on the specified protocol.</span></span> |
| <span data-ttu-id="dc170-172">**WSAENOTCONN**</span><span class="sxs-lookup"><span data-stu-id="dc170-172">**WSAENOTCONN**</span></span> | <span data-ttu-id="dc170-173">Le socket n’est pas connecté.</span><span class="sxs-lookup"><span data-stu-id="dc170-173">The socket s is not connected.</span></span> |
| <span data-ttu-id="dc170-174">**WSAENOTSOCK**</span><span class="sxs-lookup"><span data-stu-id="dc170-174">**WSAENOTSOCK**</span></span> | <span data-ttu-id="dc170-175">Le descripteur *s* n’est pas un Socket.</span><span class="sxs-lookup"><span data-stu-id="dc170-175">The descriptor *s* is not a socket.</span></span> |
| <span data-ttu-id="dc170-176">**WSAEOPNOTSUPP**</span><span class="sxs-lookup"><span data-stu-id="dc170-176">**WSAEOPNOTSUPP**</span></span> | <span data-ttu-id="dc170-177">La commande IOCTL spécifiée n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="dc170-177">The specified IOCTL command is not supported.</span></span> <span data-ttu-id="dc170-178">Cette erreur est retournée si l’IOCTL d’une **\_ requête de BACKLOG d' \_ envoi \_ \_ SIO idéale** n’est pas prise en charge par le fournisseur de transport.</span><span class="sxs-lookup"><span data-stu-id="dc170-178">This error is returned if the **SIO\_IDEAL\_SEND\_BACKLOG\_QUERY** IOCTL is not supported by the transport provider.</span></span> <span data-ttu-id="dc170-179">Cette erreur est également retournée lorsqu’une tentative d’utilisation de l’IOCTL d' **\_ envoi de journal des travaux en \_ \_ \_ souffrance SIO idéal** est effectuée sur un socket datagramme.</span><span class="sxs-lookup"><span data-stu-id="dc170-179">This error is also returned when an attempt to use the **SIO\_IDEAL\_SEND\_BACKLOG\_QUERY** IOCTL is made on a datagram socket.</span></span> |

## <a name="remarks"></a><span data-ttu-id="dc170-180">Notes</span><span class="sxs-lookup"><span data-stu-id="dc170-180">Remarks</span></span>

<span data-ttu-id="dc170-181">L’IOCTL de **\_ requête d’envoi de \_ \_ BACKLOG \_ SIO idéale** est prise en charge sur Windows Server 2008, Windows Vista avec Service Pack 1 (SP1) et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="dc170-181">The **SIO\_IDEAL\_SEND\_BACKLOG\_QUERY** IOCTL is supported on Windows Server 2008, Windows Vista with Service Pack 1 (SP1), and later versions of the operating system.</span></span>

<span data-ttu-id="dc170-182">Lors de l’envoi de données via une connexion TCP à l’aide de Windows Sockets, il est important de conserver une quantité suffisante de données en attente (envoyées mais non acceptées) dans TCP afin d’obtenir le débit le plus élevé.</span><span class="sxs-lookup"><span data-stu-id="dc170-182">When sending data over a TCP connection using Windows sockets, it is important to keep a sufficient amount of data outstanding (sent but not acknowledged yet) in TCP in order to achieve the highest throughput.</span></span>
<span data-ttu-id="dc170-183">La valeur idéale pour la quantité de données en suspens pour obtenir le meilleur débit pour la connexion TCP est appelée taille du backlog d’envoi (ISB) idéal.</span><span class="sxs-lookup"><span data-stu-id="dc170-183">The ideal value for the amount of data outstanding to achieve the best throughput for the TCP connection is called the ideal send backlog (ISB) size.</span></span>
<span data-ttu-id="dc170-184">La valeur ISB est une fonction du produit Bandwidth-Delay de la connexion TCP et de la fenêtre de réception publiée du récepteur (et en partie la quantité de congestion dans le réseau).</span><span class="sxs-lookup"><span data-stu-id="dc170-184">The ISB value is a function of the bandwidth-delay product of the TCP connection and the receiver's advertised receive window (and partly the amount of congestion in the network).</span></span>

<span data-ttu-id="dc170-185">La valeur ISB par connexion est disponible à partir de l’implémentation du protocole TCP dans Windows Server 2008, Windows Vista avec SP1 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="dc170-185">The ISB value per connection is available from the TCP protocol implementation in Windows Server 2008, Windows Vista with SP1, and later versions of the operating system.</span></span>
<span data-ttu-id="dc170-186">L’IOCTL d’une **\_ requête de BACKLOG d' \_ envoi \_ \_ SIO idéale** peut être utilisée par une application pour recevoir une notification lorsque la valeur ISB change de manière dynamique pour une connexion.</span><span class="sxs-lookup"><span data-stu-id="dc170-186">The **SIO\_IDEAL\_SEND\_BACKLOG\_QUERY** IOCTL can be used by an application to get a notification when the ISB value changes dynamically for a connection.</span></span>

<span data-ttu-id="dc170-187">Sur Windows Server 2008, Windows Vista avec SP1 et les versions ultérieures du système d’exploitation, les [**SIO de \_ \_ \_ journalisation des travaux en souffrance \_ d’envoi idéales**](sio-ideal-send-backlog-change.md) et SIO sont pris en charge sur les sockets orientés flux qui sont dans un état connecté. **\_ \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="dc170-187">On Windows Server 2008, Windows Vista with SP1, and later versions of the operating system, the [**SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE**](sio-ideal-send-backlog-change.md) and **SIO\_IDEAL\_SEND\_BACKLOG\_QUERY** IOCTLs are supported on stream-oriented sockets that are in a connected state.</span></span>

<span data-ttu-id="dc170-188">La plage de la valeur ISB pour une connexion TCP peut théoriquement varier de 0 à 16 mégaoctets au maximum.</span><span class="sxs-lookup"><span data-stu-id="dc170-188">The range for the ISB value for a TCP connection can theoretically vary from 0 to a maximum of 16 megabytes.</span></span>

<span data-ttu-id="dc170-189">L’utilisation classique de la [**SIO \_ de \_ \_ journalisation \_ des travaux en souffrance des envois**](sio-ideal-send-backlog-change.md) et SIO idéale d’envoi de **Journal des travaux en \_ \_ \_ souffrance \_** est basée sur la méthode Send utilisée par les applications.</span><span class="sxs-lookup"><span data-stu-id="dc170-189">The typical usage of the [**SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE**](sio-ideal-send-backlog-change.md) and **SIO\_IDEAL\_SEND\_BACKLOG\_QUERY** IOCTLs is based on the send method used by the applications.</span></span>
<span data-ttu-id="dc170-190">Deux cas courants sont abordés.</span><span class="sxs-lookup"><span data-stu-id="dc170-190">Two common cases are discussed.</span></span>

<span data-ttu-id="dc170-191">Les applications qui exécutent une requête d’envoi de blocage ou non bloquant à la fois s’appuient généralement sur la mise en mémoire tampon d’envoi interne par Winsock pour atteindre un débit correct.</span><span class="sxs-lookup"><span data-stu-id="dc170-191">Applications that perform one blocking or non-blocking send request at a time typically rely on internal send buffering by Winsock to achieve decent throughput.</span></span>
<span data-ttu-id="dc170-192">La limite de mémoire tampon d’envoi pour une connexion donnée est contrôlée par l’option de socket **\_ SNDBUF** .</span><span class="sxs-lookup"><span data-stu-id="dc170-192">The send buffer limit for a given connection is controlled by the **SO\_SNDBUF** socket option.</span></span>
<span data-ttu-id="dc170-193">Pour la méthode de blocage et d’envoi non bloquant, la limite de mémoire tampon d’envoi détermine la quantité de données conservées en attente dans TCP.</span><span class="sxs-lookup"><span data-stu-id="dc170-193">For the blocking and non-blocking send method, the send buffer limit determines how much data is kept outstanding in TCP.</span></span>
<span data-ttu-id="dc170-194">Si la valeur d’ISB pour la connexion est supérieure à la limite de mémoire tampon d’envoi, le débit atteint sur la connexion n’est pas optimal.</span><span class="sxs-lookup"><span data-stu-id="dc170-194">If the ISB value for the connection is larger than the send buffer limit, then the throughput achieved on the connection will not be optimal.</span></span>
<span data-ttu-id="dc170-195">Afin d’obtenir un meilleur débit, les applications peuvent définir la limite de mémoire tampon d’envoi en fonction du résultat de la requête ISB, car les notifications de modification ISB se produisent sur la connexion.</span><span class="sxs-lookup"><span data-stu-id="dc170-195">In order to achieve better throughput, the applications can set the send buffer limit based on the result of the ISB query as ISB change notifications occur on the connection.</span></span>

<span data-ttu-id="dc170-196">Pour les applications qui utilisent la méthode Send avec chevauchement avec plusieurs demandes d’envoi en attente, la quantité de données restantes en suspens dans TCP est déterminée par la limite de mémoire tampon d’envoi dans Winsock et par la quantité totale de données contenues dans les demandes d’envoi superposées en suspens.</span><span class="sxs-lookup"><span data-stu-id="dc170-196">For applications that use the overlapped send method with multiple send requests outstanding, the amount of data kept outstanding in TCP is determined by the send buffer limit in Winsock and the total amount of data contained in the outstanding overlapped send requests.</span></span>
<span data-ttu-id="dc170-197">Dans ce cas, les applications doivent utiliser la valeur ISB pour déterminer le nombre de demandes d’envoi en suspens qu’elles doivent conserver et la taille des données pour chaque demande d’envoi.</span><span class="sxs-lookup"><span data-stu-id="dc170-197">In this case, applications should use the ISB value to determine how many outstanding send requests they should keep and what the data size for each send request should be.</span></span>
<span data-ttu-id="dc170-198">Dans l’idéal, l’application doit tenter de garder l’équation suivante satisfaite :</span><span class="sxs-lookup"><span data-stu-id="dc170-198">Ideally, the application should try to keep the following equation satisfied:</span></span>

`ISB value == send buffer limit + (number of simultaneous overlapped send requests * data length per send request)`

<span data-ttu-id="dc170-199">Notez que l’utilisation des IOCTL d’ISB sur des sockets TCP de la manière ci-dessus peut entraîner une augmentation de l’utilisation de la mémoire dans Exchange pour une augmentation du débit sur les connexions avec un produit avec un délai de bande passante élevé.</span><span class="sxs-lookup"><span data-stu-id="dc170-199">Note that using the ISB IOCTLs over TCP sockets in the above fashion can lead to increased memory usage in exchange for increased throughput on connections with a high bandwidth-delay product.</span></span>
<span data-ttu-id="dc170-200">L’implémentation TCP dans Windows limite les valeurs ISB en fonction de l’utilisation globale de la mémoire système.</span><span class="sxs-lookup"><span data-stu-id="dc170-200">The TCP implementation in Windows will throttle ISB values as necessary based on overall system memory usage.</span></span>

<span data-ttu-id="dc170-201">L’IOCTL d’une **\_ requête de BACKLOG d' \_ envoi \_ \_ SIO idéale** est autorisée uniquement sur un socket de flux qui est dans l’état connecté.</span><span class="sxs-lookup"><span data-stu-id="dc170-201">The **SIO\_IDEAL\_SEND\_BACKLOG\_QUERY** IOCTL is allowed only on a stream socket that is in the connected state.</span></span>
<span data-ttu-id="dc170-202">Dans le cas contraire, la fonction [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** échouera avec **WSAENOTCONN**.</span><span class="sxs-lookup"><span data-stu-id="dc170-202">Otherwise the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function will fail with **WSAENOTCONN**.</span></span>

<span data-ttu-id="dc170-203">Toute IOCTL peut se bloquer indéfiniment, en fonction de l’implémentation du fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="dc170-203">Any IOCTL may block indefinitely, depending on the service provider's implementation.</span></span>
<span data-ttu-id="dc170-204">Si l’application ne peut pas tolérer le blocage dans un appel de fonction [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** , les e/s avec chevauchement sont conseillées pour les IOCTL qui sont particulièrement susceptibles de se bloquer.</span><span class="sxs-lookup"><span data-stu-id="dc170-204">If the application cannot tolerate blocking in a [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function call, overlapped I/O would be advised for IOCTLs that are especially likely to block.</span></span>

<span data-ttu-id="dc170-205">L’IOCTL d’une **requête de BACKLOG d' \_ \_ envoi \_ \_ SIO idéale** n’est pas susceptible de se bloquer et est normalement appelée en mode synchrone avec les paramètres *lpOverlapped* et *lpCompletionRoutine* définis sur **null**.</span><span class="sxs-lookup"><span data-stu-id="dc170-205">The **SIO\_IDEAL\_SEND\_BACKLOG\_QUERY** IOCTL is not likely to block so it is normally called synchronously with the *lpOverlapped* and *lpCompletionRoutine* parameters set to **NULL**.</span></span>

<span data-ttu-id="dc170-206">L’IOCTL d’une **requête de BACKLOG d' \_ \_ envoi \_ \_ SIO idéale** peut échouer avec l’opération **WSAEINTR** ou **WSA \_ \_ abandonnée** dans les cas suivants :</span><span class="sxs-lookup"><span data-stu-id="dc170-206">The **SIO\_IDEAL\_SEND\_BACKLOG\_QUERY** IOCTL can fail with **WSAEINTR** or **WSA\_OPERATION\_ABORTED** under the following cases:</span></span>

<span data-ttu-id="dc170-207">La connexion TCP est déconnectée en douceur dans le sens de l’envoi.</span><span class="sxs-lookup"><span data-stu-id="dc170-207">The TCP connection is gracefully disconnected in the send direction.</span></span>
<span data-ttu-id="dc170-208">Cela peut se produire à la suite d’un appel à la fonction Shutdown avec la méthode How définie sur l' **\_ envoi SD**, d’un appel à la fonction **DisconnectEx** ou d’un appel à la fonction **TransmitFile** ou **TransmitPackets** avec le paramètre *dwFlags* défini sur **tf \_ Disconnect** ou **tf \_** Remain.</span><span class="sxs-lookup"><span data-stu-id="dc170-208">This can occur as a result of a call to shutdown function with the how parameter set to **SD\_SEND**, a call to the **DisconnectEx** function, or a call to the **TransmitFile** or **TransmitPackets** function with *dwFlags* parameter set to **TF\_DISCONNECT** or **TF\_REUSE**.</span></span>
<span data-ttu-id="dc170-209">La connexion TCP a été réinitialisée ou abandonnée.</span><span class="sxs-lookup"><span data-stu-id="dc170-209">The TCP connection has been reset or aborted.</span></span>
<span data-ttu-id="dc170-210">La demande est annulée par le gestionnaire d’e/s.</span><span class="sxs-lookup"><span data-stu-id="dc170-210">The request is canceled by the I/O Manager.</span></span>

<span data-ttu-id="dc170-211">Deux fonctions wrapper Inline pour ces IOCTL sont définies dans le fichier d’en-tête *Ws2tcpip. h* .</span><span class="sxs-lookup"><span data-stu-id="dc170-211">Two inline wrapper functions for these IOCTLs are defined in the *Ws2tcpip.h* header file.</span></span>
<span data-ttu-id="dc170-212">Il est recommandé d’utiliser ces fonctions inline au lieu d’utiliser la [**SIO \_ de \_ \_ journalisation \_ des travaux en souffrance Send idéale**](sio-ideal-send-backlog-change.md) et SIO des IOCTL de **\_ \_ \_ \_ requête Send backlog** directement.</span><span class="sxs-lookup"><span data-stu-id="dc170-212">It is recommended that these inline functions be used instead of using the [**SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE**](sio-ideal-send-backlog-change.md) and **SIO\_IDEAL\_SEND\_BACKLOG\_QUERY** IOCTLs directly.</span></span>

<span data-ttu-id="dc170-213">La fonction de wrapper Inline pour le [**SIO \_ idéal \_ Send \_ BACKLOG \_ change**](sio-ideal-send-backlog-change.md) IOCTL est la fonction **idealsendbacklognotify** .</span><span class="sxs-lookup"><span data-stu-id="dc170-213">The inline wrapper function for the [**SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE**](sio-ideal-send-backlog-change.md) IOCTL is the **idealsendbacklognotify** function.</span></span>

<span data-ttu-id="dc170-214">La fonction de wrapper Inline pour l’IOCTL de **requête d' \_ envoi de \_ \_ BACKLOG \_ SIO idéale** est la fonction **idealsendbacklogquery** .</span><span class="sxs-lookup"><span data-stu-id="dc170-214">The inline wrapper function for the **SIO\_IDEAL\_SEND\_BACKLOG\_QUERY** IOCTL is the **idealsendbacklogquery** function.</span></span>

<span data-ttu-id="dc170-215">La mise en mémoire tampon d’envoi dynamique pour TCP a été ajoutée sur Windows 7 et Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="dc170-215">Dynamic send buffering for TCP was added on Windows 7 and Windows Server 2008 R2.</span></span>
<span data-ttu-id="dc170-216">Par défaut, la mise en mémoire tampon d’envoi dynamique pour TCP est activée, sauf si une application définit l’option de socket **\_ SNDBUF** sur le socket de flux.</span><span class="sxs-lookup"><span data-stu-id="dc170-216">By default, dynamic send buffering for TCP is enabled unless an application sets the **SO\_SNDBUF** socket option on the stream socket.</span></span>

<span data-ttu-id="dc170-217">L’utilisation de netsh est la méthode recommandée pour interroger ou définir la mise en mémoire tampon d’envoi dynamique pour TCP.</span><span class="sxs-lookup"><span data-stu-id="dc170-217">Using netsh is the recommended method to query or set dynamic send buffering for TCP.</span></span>

<span data-ttu-id="dc170-218">La valeur actuelle de la mise en mémoire tampon d’envoi dynamique pour TCP peut être récupérée à l’aide de la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="dc170-218">The current value for dynamic send buffering for TCP can be retrieved using the following command:</span></span>

`netsh winsock show autotuning`

<span data-ttu-id="dc170-219">La mise en mémoire tampon d’envoi dynamique pour TCP peut être désactivée à l’aide de la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="dc170-219">Dynamic send buffering for TCP can be disabled using the following command:</span></span>

`netsh winsock set autotuning off`

<span data-ttu-id="dc170-220">La mise en mémoire tampon d’envoi dynamique pour TCP peut être activée à l’aide de la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="dc170-220">Dynamic send buffering for TCP can be enabled using the following command:</span></span>

`netsh winsock set autotuning on`

<span data-ttu-id="dc170-221">Bien qu’elle soit déconseillée, la mise en mémoire tampon d’envoi dynamique peut être désactivée à partir d’une application en affectant à la valeur de Registre suivante la valeur zéro :</span><span class="sxs-lookup"><span data-stu-id="dc170-221">While it is discouraged, dynamic send buffering can be disabled from an application by setting the following registry value to zero:</span></span>

`HKEY_LOCAL_MACHINE\SYSTEM\Current Control Set\Services\AFD\Parameters\DynamicSendBufferDisable`

<span data-ttu-id="dc170-222">Lors de la modification de la valeur de la mise en mémoire tampon d’envoi dynamique à l’aide de NetSh.exe ou de la modification de la valeur de Registre, l’ordinateur doit être redémarré pour que la modification prenne effet.</span><span class="sxs-lookup"><span data-stu-id="dc170-222">When changing the value for dynamic send buffering using NetSh.exe or changing the registry value, the computer must be restarted for the change to take effect.</span></span>

<span data-ttu-id="dc170-223">Avec la mise en mémoire tampon d’envoi dynamique sur Windows 7 et Windows Server 2008 R2, l’utilisation de la [**SIO de \_ \_ \_ journalisation des travaux en souffrance \_**](sio-ideal-send-backlog-change.md) des envois idéale et SIO des IOCTL de requête d' **\_ envoi du \_ \_ backlog \_** sont nécessaires uniquement dans des circonstances particulières.</span><span class="sxs-lookup"><span data-stu-id="dc170-223">With dynamic send buffering on Windows 7 and Windows Server 2008 R2, the use of the [**SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE**](sio-ideal-send-backlog-change.md) and **SIO\_IDEAL\_SEND\_BACKLOG\_QUERY** IOCTLs are needed only in special circumstances.</span></span>

## <a name="see-also"></a><span data-ttu-id="dc170-224">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dc170-224">See also</span></span>

[<span data-ttu-id="dc170-225">**SIO_IDEAL_SEND_BACKLOG_CHANGE**</span><span class="sxs-lookup"><span data-stu-id="dc170-225">**SIO_IDEAL_SEND_BACKLOG_CHANGE**</span></span>](sio-ideal-send-backlog-change.md)

[<span data-ttu-id="dc170-226">**socle**</span><span class="sxs-lookup"><span data-stu-id="dc170-226">**socket**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-socket)

[<span data-ttu-id="dc170-227">**WSAGetLastError**</span><span class="sxs-lookup"><span data-stu-id="dc170-227">**WSAGetLastError**</span></span>](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)

[<span data-ttu-id="dc170-228">**WSAGetOverlappedResult**</span><span class="sxs-lookup"><span data-stu-id="dc170-228">**WSAGetOverlappedResult**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[<span data-ttu-id="dc170-229">**WSAIoctl**</span><span class="sxs-lookup"><span data-stu-id="dc170-229">**WSAIoctl**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[<span data-ttu-id="dc170-230">**WSAOVERLAPPED**</span><span class="sxs-lookup"><span data-stu-id="dc170-230">**WSAOVERLAPPED**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[<span data-ttu-id="dc170-231">**WSASocketA**</span><span class="sxs-lookup"><span data-stu-id="dc170-231">**WSASocketA**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[<span data-ttu-id="dc170-232">**WSASocketW**</span><span class="sxs-lookup"><span data-stu-id="dc170-232">**WSASocketW**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
