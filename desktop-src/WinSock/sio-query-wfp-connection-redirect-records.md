---
description: Le code de contrôle récupère l’enregistrement de redirection pour la connexion TCP/IP acceptée pour une utilisation par un service de redirection de plateforme de filtrage Windows.
ms.assetid: E0D7CC1A-8F93-45A0-9543-3F2ACAF352F5
title: Code de contrôle SIO_QUERY_WFP_CONNECTION_REDIRECT_RECORDS
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 2389914d29bd403a33e23065c29f549a01adbb67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516989"
---
# <a name="sio_query_wfp_connection_redirect_records-control-code"></a><span data-ttu-id="dda0b-103">Code de contrôle SIO_QUERY_WFP_CONNECTION_REDIRECT_RECORDS</span><span class="sxs-lookup"><span data-stu-id="dda0b-103">SIO_QUERY_WFP_CONNECTION_REDIRECT_RECORDS Control Code</span></span>

## <a name="description"></a><span data-ttu-id="dda0b-104">Description</span><span class="sxs-lookup"><span data-stu-id="dda0b-104">Description</span></span>

<span data-ttu-id="dda0b-105">Le code de contrôle des enregistrements de la **\_ \_ \_ connexion \_ \_ WFP de la requête SIO** récupère l’enregistrement de redirection pour la connexion TCP/IP acceptée pour une utilisation par un service de redirection de plateforme de filtrage Windows (WFP).</span><span class="sxs-lookup"><span data-stu-id="dda0b-105">The **SIO\_QUERY\_WFP\_CONNECTION\_REDIRECT\_RECORDS** control code retrieves the redirect record for the accepted TCP/IP connection for use by a Windows Filtering Platform (WFP) redirect service.</span></span>

<span data-ttu-id="dda0b-106">Pour effectuer cette opération, appelez la fonction [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** avec les paramètres suivants.</span><span class="sxs-lookup"><span data-stu-id="dda0b-106">To perform this operation, call the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function with the following parameters.</span></span>

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_QUERY_WFP_CONNECTION_REDIRECT_RECORDS, // dwIoControlCode
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
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_QUERY_WFP_CONNECTION_REDIRECT_RECORDS, // dwIoControlCode
  NULL,                         // lpvInBuffer
  0,                            // cbInBuffer
  (LPVOID) lpvOutBuffer,         // output buffer
  (DWORD) cbOutBuffer,       // size of output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

## <a name="parameters"></a><span data-ttu-id="dda0b-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dda0b-107">Parameters</span></span>

### <a name="s"></a><span data-ttu-id="dda0b-108">s</span><span class="sxs-lookup"><span data-stu-id="dda0b-108">s</span></span>

<span data-ttu-id="dda0b-109">Descripteur identifiant un Socket.</span><span class="sxs-lookup"><span data-stu-id="dda0b-109">A descriptor identifying a socket.</span></span>

### <a name="dwiocontrolcode"></a><span data-ttu-id="dda0b-110">dwIoControlCode</span><span class="sxs-lookup"><span data-stu-id="dda0b-110">dwIoControlCode</span></span>

<span data-ttu-id="dda0b-111">Code de contrôle de l’opération.</span><span class="sxs-lookup"><span data-stu-id="dda0b-111">The control code for the operation.</span></span>
<span data-ttu-id="dda0b-112">Utilisez **les \_ \_ \_ \_ \_ enregistrements de redirection de connexion WFP de la requête SIO** pour cette opération.</span><span class="sxs-lookup"><span data-stu-id="dda0b-112">Use **SIO\_QUERY\_WFP\_CONNECTION\_REDIRECT\_RECORDS** for this operation.</span></span>

### <a name="lpvinbuffer"></a><span data-ttu-id="dda0b-113">lpvInBuffer</span><span class="sxs-lookup"><span data-stu-id="dda0b-113">lpvInBuffer</span></span>

<span data-ttu-id="dda0b-114">Pointeur vers la mémoire tampon d’entrée.</span><span class="sxs-lookup"><span data-stu-id="dda0b-114">A pointer to the input buffer.</span></span>
<span data-ttu-id="dda0b-115">Ce paramètre n’est pas utilisé pour cette opération.</span><span class="sxs-lookup"><span data-stu-id="dda0b-115">This parameter is unused for this operation.</span></span>

### <a name="cbinbuffer"></a><span data-ttu-id="dda0b-116">cbInBuffer</span><span class="sxs-lookup"><span data-stu-id="dda0b-116">cbInBuffer</span></span>

<span data-ttu-id="dda0b-117">Taille, en octets, de la mémoire tampon d’entrée.</span><span class="sxs-lookup"><span data-stu-id="dda0b-117">The size, in bytes, of the input buffer.</span></span>
<span data-ttu-id="dda0b-118">Ce paramètre n’est pas utilisé pour cette opération.</span><span class="sxs-lookup"><span data-stu-id="dda0b-118">This parameter is unused for this operation.</span></span>

### <a name="lpvoutbuffer"></a><span data-ttu-id="dda0b-119">lpvOutBuffer</span><span class="sxs-lookup"><span data-stu-id="dda0b-119">lpvOutBuffer</span></span>

<span data-ttu-id="dda0b-120">Pointeur vers la mémoire tampon de sortie.</span><span class="sxs-lookup"><span data-stu-id="dda0b-120">A pointer to the output buffer.</span></span>
<span data-ttu-id="dda0b-121">Ce paramètre doit pointer vers un type de données **ULong** si les paramètres *lpOverlapped* et *lpCompletionRoutine* ont la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="dda0b-121">This parameter should point to a **ULONG** data type if the *lpOverlapped* and *lpCompletionRoutine* parameters are **NULL**.</span></span>

### <a name="cboutbuffer"></a><span data-ttu-id="dda0b-122">cbOutBuffer</span><span class="sxs-lookup"><span data-stu-id="dda0b-122">cbOutBuffer</span></span>

<span data-ttu-id="dda0b-123">Taille, en octets, de la mémoire tampon de sortie.</span><span class="sxs-lookup"><span data-stu-id="dda0b-123">The size, in bytes, of the output buffer.</span></span>
<span data-ttu-id="dda0b-124">Ce paramètre doit avoir au moins la taille d’un type de données **ULong** .</span><span class="sxs-lookup"><span data-stu-id="dda0b-124">This parameter must be at least the size of a **ULONG** data type.</span></span>

### <a name="lpcbbytesreturned"></a><span data-ttu-id="dda0b-125">lpcbBytesReturned</span><span class="sxs-lookup"><span data-stu-id="dda0b-125">lpcbBytesReturned</span></span>

<span data-ttu-id="dda0b-126">Pointeur vers une variable qui reçoit la taille, en octets, des données stockées dans la mémoire tampon de sortie.</span><span class="sxs-lookup"><span data-stu-id="dda0b-126">A pointer to a variable that receives the size, in bytes, of the data stored in the output buffer.</span></span>

<span data-ttu-id="dda0b-127">Si la mémoire tampon de sortie est trop petite, l’appel échoue, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) retourne [**WSAEINVAL**](windows-sockets-error-codes-2.md)et le paramètre *LpcbBytesReturned* pointe vers une valeur **DWORD** égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="dda0b-127">If the output buffer is too small, the call fails, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) returns [**WSAEINVAL**](windows-sockets-error-codes-2.md), and the *lpcbBytesReturned* parameter points to a **DWORD** value of zero.</span></span>

<span data-ttu-id="dda0b-128">Si *lpOverlapped* a la valeur **null**, la valeur **DWORD** vers laquelle pointe le paramètre *lpcbBytesReturned* retourné sur un appel réussi ne peut pas être égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="dda0b-128">If *lpOverlapped* is **NULL**, the **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned on a successful call cannot be zero.</span></span>

<span data-ttu-id="dda0b-129">Si le paramètre *lpOverlapped* n’a pas la **valeur null** pour les sockets superposés, les opérations qui ne peuvent pas être terminées immédiatement seront lancées et l’achèvement sera indiqué ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="dda0b-129">If the *lpOverlapped* parameter is not **NULL** for overlapped sockets, operations that cannot be completed immediately will be initiated, and completion will be indicated at a later time.</span></span>
<span data-ttu-id="dda0b-130">La valeur **DWORD** pointée par le paramètre *lpcbBytesReturned* retourné peut être égale à zéro, car la taille des données stockées ne peut pas être déterminée tant que l’opération avec chevauchement n’est pas terminée.</span><span class="sxs-lookup"><span data-stu-id="dda0b-130">The **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned may be zero since the size of the data stored can't be determined until the overlapped operation has completed.</span></span>
<span data-ttu-id="dda0b-131">L’état d’achèvement final peut être récupéré lorsque la méthode d’achèvement appropriée est signalée lorsque l’opération est terminée.</span><span class="sxs-lookup"><span data-stu-id="dda0b-131">The final completion status can be retrieved when the appropriate completion method is signaled when the operation has completed.</span></span>

### <a name="lpvoverlapped"></a><span data-ttu-id="dda0b-132">lpvOverlapped</span><span class="sxs-lookup"><span data-stu-id="dda0b-132">lpvOverlapped</span></span>

<span data-ttu-id="dda0b-133">Pointeur vers une structure [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) .</span><span class="sxs-lookup"><span data-stu-id="dda0b-133">A pointer to a [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="dda0b-134">Si le socket *s* a été créé sans l’attribut Overlapped, le paramètre *lpOverlapped* est ignoré.</span><span class="sxs-lookup"><span data-stu-id="dda0b-134">If socket *s* was created without the overlapped attribute, the *lpOverlapped* parameter is ignored.</span></span>

<span data-ttu-id="dda0b-135">Si *s* a été ouvert avec l’attribut Overlapped et que le paramètre *lpOverlapped* n’a pas la **valeur null**, l’opération est exécutée en tant qu’opération Overlapped (asynchrone).</span><span class="sxs-lookup"><span data-stu-id="dda0b-135">If *s* was opened with the overlapped attribute and the *lpOverlapped* parameter is not **NULL**, the operation is performed as an overlapped (asynchronous) operation.</span></span>
<span data-ttu-id="dda0b-136">Dans ce cas, le paramètre *lpOverlapped* doit pointer vers une structure [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) valide.</span><span class="sxs-lookup"><span data-stu-id="dda0b-136">In this case, *lpOverlapped* parameter must point to a valid [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="dda0b-137">Pour les opérations avec chevauchement, la fonction [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** retourne immédiatement, et la méthode d’achèvement appropriée est signalée lorsque l’opération est terminée.</span><span class="sxs-lookup"><span data-stu-id="dda0b-137">For overlapped operations, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns immediately, and the appropriate completion method is signaled when the operation has been completed.</span></span>
<span data-ttu-id="dda0b-138">Sinon, la fonction ne retourne pas jusqu’à ce que l’opération soit terminée ou qu’une erreur se produise.</span><span class="sxs-lookup"><span data-stu-id="dda0b-138">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

### <a name="lpcompletionroutine"></a><span data-ttu-id="dda0b-139">lpCompletionRoutine</span><span class="sxs-lookup"><span data-stu-id="dda0b-139">lpCompletionRoutine</span></span>

<span data-ttu-id="dda0b-140">Type : \_ In_opt \_ [ **LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span><span class="sxs-lookup"><span data-stu-id="dda0b-140">Type: \_In_opt\_ [**LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span></span>

<span data-ttu-id="dda0b-141">Pointeur vers la routine de saisie semi-automatique appelée lorsque l’opération est terminée (ignoré pour les sockets non superposés).</span><span class="sxs-lookup"><span data-stu-id="dda0b-141">A pointer to the completion routine called when the operation has been completed (ignored for non-overlapped sockets).</span></span>

### <a name="lpthreadid"></a><span data-ttu-id="dda0b-142">lpThreadId</span><span class="sxs-lookup"><span data-stu-id="dda0b-142">lpThreadId</span></span>

<span data-ttu-id="dda0b-143">Pointeur vers une structure [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) qui doit être utilisée par le fournisseur dans un appel ultérieur à [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc).</span><span class="sxs-lookup"><span data-stu-id="dda0b-143">A pointer to a [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure to be used by the provider in a subsequent call to [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc).</span></span>
<span data-ttu-id="dda0b-144">Le fournisseur doit stocker la structure [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) référencée (pas le pointeur vers le même) jusqu’à ce que la fonction [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) soit retournée.</span><span class="sxs-lookup"><span data-stu-id="dda0b-144">The provider should store the referenced [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure (not the pointer to same) until after the [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) function returns.</span></span>

<span data-ttu-id="dda0b-145">**Remarque**  Ce paramètre s’applique uniquement à la fonction **WSPIoctl** .</span><span class="sxs-lookup"><span data-stu-id="dda0b-145">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

### <a name="lperrno"></a><span data-ttu-id="dda0b-146">lpErrno</span><span class="sxs-lookup"><span data-stu-id="dda0b-146">lpErrno</span></span>

<span data-ttu-id="dda0b-147">Pointeur vers le code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="dda0b-147">A pointer to the error code.</span></span>

<span data-ttu-id="dda0b-148">**Remarque**  Ce paramètre s’applique uniquement à la fonction **WSPIoctl** .</span><span class="sxs-lookup"><span data-stu-id="dda0b-148">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

## <a name="return-value"></a><span data-ttu-id="dda0b-149">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="dda0b-149">Return value</span></span>

<span data-ttu-id="dda0b-150">Si l’opération se termine correctement, la fonction [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** retourne la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="dda0b-150">If the operation completes successfully, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns zero.</span></span>

<span data-ttu-id="dda0b-151">Si l’opération échoue ou est en attente, la fonction [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** retourne une **\_ erreur de socket**.</span><span class="sxs-lookup"><span data-stu-id="dda0b-151">If the operation fails or is pending, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns **SOCKET\_ERROR**.</span></span>
<span data-ttu-id="dda0b-152">Pour afficher les informations d’erreur étendues, appelez [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span><span class="sxs-lookup"><span data-stu-id="dda0b-152">To get extended error information, call [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>

| <span data-ttu-id="dda0b-153">Code d'erreur</span><span class="sxs-lookup"><span data-stu-id="dda0b-153">Error code</span></span> | <span data-ttu-id="dda0b-154">Signification</span><span class="sxs-lookup"><span data-stu-id="dda0b-154">Meaning</span></span> |
|------------|---------|
| <span data-ttu-id="dda0b-155">**ERREUR \_ de \_ mémoire tampon insuffisante**</span><span class="sxs-lookup"><span data-stu-id="dda0b-155">**ERROR\_INSUFFICIENT\_BUFFER**</span></span> | <span data-ttu-id="dda0b-156">La zone de données passée à un appel système est insuffisante.</span><span class="sxs-lookup"><span data-stu-id="dda0b-156">The data area passed to a system call is too small.</span></span> <span data-ttu-id="dda0b-157">Cette erreur est retournée si la mémoire tampon vers laquelle pointe le paramètre *lpvOutBuffer* avec une taille de mémoire tampon passée dans le paramètre *cbOutBuffer* est trop petite.</span><span class="sxs-lookup"><span data-stu-id="dda0b-157">This error is returned if the buffer pointed to by the *lpvOutBuffer* parameter with a buffer size passed in the *cbOutBuffer* parameter is too small.</span></span> <span data-ttu-id="dda0b-158">La taille de la mémoire tampon requise est retournée dans le paramètre *lpcbBytesReturned* .</span><span class="sxs-lookup"><span data-stu-id="dda0b-158">The buffer size required will be returned in the *lpcbBytesReturned* parameter.</span></span> |
| <span data-ttu-id="dda0b-159">**WSA_IO_PENDING**</span><span class="sxs-lookup"><span data-stu-id="dda0b-159">**WSA_IO_PENDING**</span></span> | <span data-ttu-id="dda0b-160">Une opération avec chevauchement a été correctement initiée et l’achèvement sera indiqué ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="dda0b-160">An overlapped operation was successfully initiated and completion will be indicated at a later time.</span></span> |
| <span data-ttu-id="dda0b-161">**WSA_OPERATION_ABORTED**</span><span class="sxs-lookup"><span data-stu-id="dda0b-161">**WSA_OPERATION_ABORTED**</span></span> | <span data-ttu-id="dda0b-162">Une opération avec chevauchement a été annulée en raison de la fermeture du socket ou de l’exécution de la commande **SIO_FLUSH** ioctl.</span><span class="sxs-lookup"><span data-stu-id="dda0b-162">An overlapped operation was canceled due to the closure of the socket or the execution of the **SIO_FLUSH** IOCTL command.</span></span> |
| <span data-ttu-id="dda0b-163">**WSAEFAULT**</span><span class="sxs-lookup"><span data-stu-id="dda0b-163">**WSAEFAULT**</span></span> | <span data-ttu-id="dda0b-164">Le paramètre *lpvOutBuffer*, *lpcbBytesReturned*, *lpOverlapped* ou *lpCompletionRoutine* n’est pas entièrement contenu dans une partie valide de l’espace d’adressage de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="dda0b-164">The *lpvOutBuffer*, *lpcbBytesReturned*, *lpOverlapped*, or *lpCompletionRoutine* parameter is not totally contained in a valid part of the user address space.</span></span> |
| <span data-ttu-id="dda0b-165">**WSAEINPROGRESS**</span><span class="sxs-lookup"><span data-stu-id="dda0b-165">**WSAEINPROGRESS**</span></span> | <span data-ttu-id="dda0b-166">La fonction est appelée lorsqu’un rappel est en cours.</span><span class="sxs-lookup"><span data-stu-id="dda0b-166">The function is invoked when a callback is in progress.</span></span> |
| <span data-ttu-id="dda0b-167">**WSAEINTR**</span><span class="sxs-lookup"><span data-stu-id="dda0b-167">**WSAEINTR**</span></span> | <span data-ttu-id="dda0b-168">Une opération de blocage a été interrompue.</span><span class="sxs-lookup"><span data-stu-id="dda0b-168">A blocking operation was interrupted.</span></span> |
| <span data-ttu-id="dda0b-169">**WSAEINVAL**</span><span class="sxs-lookup"><span data-stu-id="dda0b-169">**WSAEINVAL**</span></span> | <span data-ttu-id="dda0b-170">Le paramètre *dwIoControlCode* n’est pas une commande valide, ou un paramètre d’entrée spécifié n’est pas acceptable, ou la commande n’est pas applicable au type de socket spécifié.</span><span class="sxs-lookup"><span data-stu-id="dda0b-170">The *dwIoControlCode* parameter is not a valid command, or a specified input parameter is not acceptable, or the command is not applicable to the type of socket specified.</span></span> <span data-ttu-id="dda0b-171">Cette erreur est retournée si le paramètre *cbOutBuffer* est inférieur à la taille d’un type de données **ULong** .</span><span class="sxs-lookup"><span data-stu-id="dda0b-171">This error is returned if the *cbOutBuffer* parameter is less than the size of a **ULONG** data type.</span></span> |
| <span data-ttu-id="dda0b-172">**WSAENETDOWN**</span><span class="sxs-lookup"><span data-stu-id="dda0b-172">**WSAENETDOWN**</span></span> | <span data-ttu-id="dda0b-173">Le sous-système réseau a échoué.</span><span class="sxs-lookup"><span data-stu-id="dda0b-173">The network subsystem has failed.</span></span> |
| <span data-ttu-id="dda0b-174">**WSAENOPROTOOPT**</span><span class="sxs-lookup"><span data-stu-id="dda0b-174">**WSAENOPROTOOPT**</span></span> | <span data-ttu-id="dda0b-175">L’option de socket n’est pas prise en charge sur le protocole spécifié.</span><span class="sxs-lookup"><span data-stu-id="dda0b-175">The socket option is not supported on the specified protocol.</span></span> |
| <span data-ttu-id="dda0b-176">**WSAENOTCONN**</span><span class="sxs-lookup"><span data-stu-id="dda0b-176">**WSAENOTCONN**</span></span> | <span data-ttu-id="dda0b-177">Le socket *n'* est pas connecté.</span><span class="sxs-lookup"><span data-stu-id="dda0b-177">The socket *s* is not connected.</span></span> |
| <span data-ttu-id="dda0b-178">**WSAENOTSOCK**</span><span class="sxs-lookup"><span data-stu-id="dda0b-178">**WSAENOTSOCK**</span></span> | <span data-ttu-id="dda0b-179">Le descripteur *s* n’est pas un Socket.</span><span class="sxs-lookup"><span data-stu-id="dda0b-179">The descriptor *s* is not a socket.</span></span> |
| <span data-ttu-id="dda0b-180">**WSAEOPNOTSUPP**</span><span class="sxs-lookup"><span data-stu-id="dda0b-180">**WSAEOPNOTSUPP**</span></span> | <span data-ttu-id="dda0b-181">La commande IOCTL spécifiée n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="dda0b-181">The specified IOCTL command is not supported.</span></span> <span data-ttu-id="dda0b-182">Cette erreur est retournée si les enregistrements de la **\_ connexion WFP de la requête SIO \_ \_ \_ redirigent \_** IOCTL n’est pas pris en charge par le fournisseur de transport.</span><span class="sxs-lookup"><span data-stu-id="dda0b-182">This error is returned if the **SIO\_QUERY\_WFP\_CONNECTION\_REDIRECT\_RECORDS** IOCTL is not supported by the transport provider.</span></span> |

## <a name="remarks"></a><span data-ttu-id="dda0b-183">Notes</span><span class="sxs-lookup"><span data-stu-id="dda0b-183">Remarks</span></span>

<span data-ttu-id="dda0b-184">Les **\_ enregistrements de \_ \_ \_ redirection \_ de connexion WFP de la requête SIO** sont pris en charge sur Windows 8, Windows Server 2012 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="dda0b-184">The **SIO\_QUERY\_WFP\_CONNECTION\_REDIRECT\_RECORDS** IOCTL is supported on Windows 8, and Windows Server 2012, and later versions of the operating system.</span></span>

<span data-ttu-id="dda0b-185">WFP autorise l’accès au chemin de traitement des paquets TCP/IP, où les paquets sortants et entrants peuvent être examinés ou modifiés avant d’autoriser leur traitement ultérieur.</span><span class="sxs-lookup"><span data-stu-id="dda0b-185">WFP allows access to the TCP/IP packet processing path, wherein outgoing and incoming packets can be examined or changed before allowing them to be processed further.</span></span>
<span data-ttu-id="dda0b-186">En appuyant sur le chemin de traitement TCP/IP, les éditeurs de logiciels indépendants (ISV) peuvent créer plus facilement des pare-feu, des logiciels antivirus, des logiciels de diagnostic et d’autres types d’applications et de services.</span><span class="sxs-lookup"><span data-stu-id="dda0b-186">By tapping into the TCP/IP processing path, independent software vendors (ISVs) can more easily create firewalls, antivirus software, diagnostic software, and other types of applications and services.</span></span>
<span data-ttu-id="dda0b-187">WFP fournit des composants en mode utilisateur et en mode noyau afin que les éditeurs de logiciels indépendants puissent participer aux décisions de filtrage qui ont lieu dans plusieurs couches de la pile de protocole TCP/IP et dans tout le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="dda0b-187">WFP provides user-mode and kernel-mode components so that third-party ISVs can participate in the filtering decisions that take place at several layers in the TCP/IP protocol stack and throughout the operating system.</span></span>
<span data-ttu-id="dda0b-188">La fonctionnalité de redirection de connexion WFP permet à un pilote de noyau de légende WFP de rediriger une connexion localement vers un processus en mode utilisateur, d’effectuer l’inspection du contenu en mode utilisateur et de transférer le contenu inspecté à l’aide d’une connexion différente à la destination d’origine.</span><span class="sxs-lookup"><span data-stu-id="dda0b-188">The WFP connection redirect feature allows a WFP callout kernel driver to redirect a connection locally to a user-mode process, perform content inspection in user-mode, and forward the inspected content using a different connection to the original destination.</span></span>

<span data-ttu-id="dda0b-189">La **requête SIO la \_ \_ \_ connexion WFP \_ redirige les \_ enregistrements** IOCTL et plusieurs autres IOCTL connexes sont des composants en mode utilisateur utilisés pour permettre à plusieurs applications de proxy de connexion WFP d’inspecter le même flux de trafic de manière coopérative.</span><span class="sxs-lookup"><span data-stu-id="dda0b-189">The **SIO\_QUERY\_WFP\_CONNECTION\_REDIRECT\_RECORDS** IOCTL and several other related IOCTLS are user-mode components used to allow multiple WFP-based connection proxy applications to inspect the same traffic flow in a cooperative manner.</span></span>
<span data-ttu-id="dda0b-190">Chaque agent d’inspection peut réinspecter en toute sécurité le trafic réseau qui a déjà été inspecté par un autre agent d’inspection.</span><span class="sxs-lookup"><span data-stu-id="dda0b-190">Each inspection agent can safely re-inspect network traffic that has already been inspected by another inspection agent.</span></span>
<span data-ttu-id="dda0b-191">Avec la présence de plusieurs proxys (développés par différents éditeurs de logiciels indépendants, par exemple), la connexion utilisée par un proxy pour communiquer avec la destination finale peut à son tour être redirigée par un second proxy, et cette nouvelle connexion peut être redirigée par le proxy d’origine.</span><span class="sxs-lookup"><span data-stu-id="dda0b-191">With the presence of multiple proxies (developed by different ISVs, for example) the connection used by one proxy to communicate with the final destination could in turn be redirected by a second proxy, and that new connection could again be redirected by the original proxy.</span></span>
<span data-ttu-id="dda0b-192">Sans le suivi de connexion, la connexion d’origine risque de ne jamais atteindre sa destination finale, car elle est bloquée dans une boucle de proxy infinie.</span><span class="sxs-lookup"><span data-stu-id="dda0b-192">Without connection tracking, the original connection might never reach its final destination as it gets stuck in an infinite proxy loop.</span></span>

<span data-ttu-id="dda0b-193">Les **\_ enregistrements de \_ \_ \_ redirection \_ de connexion WFP de la requête SIO** sont utilisés pour fournir le suivi de connexion en proxy sur les connexions de socket redirigées.</span><span class="sxs-lookup"><span data-stu-id="dda0b-193">The **SIO\_QUERY\_WFP\_CONNECTION\_REDIRECT\_RECORDS** IOCTL is used to provide proxied connection tracking on redirected socket connections.</span></span>
<span data-ttu-id="dda0b-194">Cette fonctionnalité WFP facilite le suivi des enregistrements de redirection à partir de la redirection initiale d’une connexion à la connexion finale à la destination.</span><span class="sxs-lookup"><span data-stu-id="dda0b-194">This WFP feature facilitates tracking of redirection records from the initial redirect of a connection to the final connection to the destination.</span></span>

<span data-ttu-id="dda0b-195">Les **enregistrements de la \_ connexion WFP de la requête SIO \_ \_ \_ redirect \_** sont utilisés par un service de redirection basé sur WFP pour récupérer l’enregistrement de redirection à partir de la connexion au paquet TCP/IP acceptée (le socket connecté pour un socket TCP ou UDP, par exemple) redirigé vers celui-ci par le biais de son compagnon en mode noyau inscrit sur **ALE_CONNECT_REDIRECT** couches dans un pilote en mode noyau</span><span class="sxs-lookup"><span data-stu-id="dda0b-195">The **SIO\_QUERY\_WFP\_CONNECTION\_REDIRECT\_RECORDS** IOCTL is used by a WFP-based redirect service to retrieve the redirect record from the accepted TCP/IP packet connection (the connected socket for a TCP socket or a UDP socket, for example) redirected to it by its companion kernel-mode callout registered at **ALE_CONNECT_REDIRECT** layers in a kernel-mode driver.</span></span>
<span data-ttu-id="dda0b-196">L’IOCTL du contexte de redirection de **\_ \_ \_ connexion \_ \_ WFP de la requête SIO** est utilisée par un service de redirection basé sur WFP pour récupérer le contexte de redirection d’un enregistrement de redirection à partir de la connexion de paquet TCP/IP acceptée (le socket connecté pour un socket TCP ou UDP, par exemple) redirigé vers celui-ci par son appel compagnon enregistré dans les couches de **\_ \_ redirection**</span><span class="sxs-lookup"><span data-stu-id="dda0b-196">The **SIO\_QUERY\_WFP\_CONNECTION\_REDIRECT\_CONTEXT** IOCTL is used by a WFP-based redirect service to retrieve the redirect context for a redirect record from the accepted TCP/IP packet connection (the connected socket for a TCP socket or a UDP socket, for example) redirected to it by its companion callout registered at **ALE\_CONNECT\_REDIRECT** layers.</span></span>
<span data-ttu-id="dda0b-197">Le contexte de redirection est un contexte facultatif alloué par le pilote utilisé si l’état de redirection actuel d’une connexion est que la connexion a été redirigée par le service de redirection appelant ou que la connexion a été précédemment redirigée par le service de redirection appelant, mais redirigée ultérieurement par un autre service de redirection.</span><span class="sxs-lookup"><span data-stu-id="dda0b-197">The redirect context is an optional driver-allocated context used if the current redirection state of a connection is that the connection was redirected by the calling redirect service or the connection was previously redirected by the calling redirect service but later redirected again by a different redirect service.</span></span>
<span data-ttu-id="dda0b-198">Pour une connexion de proxy TCP, le service de redirection transfère l’enregistrement de redirection récupéré au socket TCP qu’il utilise pour effectuer un proxy du contenu d’origine à l’aide de l’IOCTL **SIO \_ définir la \_ connexion WFP des \_ \_ \_ enregistrements de redirection** .</span><span class="sxs-lookup"><span data-stu-id="dda0b-198">For a TCP proxy connection, the redirect service transfers the retrieved redirect record to the TCP socket it uses to proxy the original content using the **SIO\_SET\_WFP\_CONNECTION\_REDIRECT\_RECORDS** IOCTL.</span></span>

<span data-ttu-id="dda0b-199">Lorsque le service de redirection redirige un socket non-TCP (UDP, par exemple), les enregistrements de redirection retournés par la **requête SIO les \_ \_ \_ \_ \_ enregistrements** de redirection de connexion WFP l’indiquent au service de redirection à l’aide de la structure [**WSAMSG**](/windows/desktop/api/ws2def/ns-ws2def-wsamsg) utilisée avec la fonction [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) .</span><span class="sxs-lookup"><span data-stu-id="dda0b-199">When the redirect service is redirecting a non-TCP socket (UDP, for example), the redirect records returned by the **SIO\_QUERY\_WFP\_CONNECTION\_REDIRECT\_RECORDS** IOCTL indicate this to the redirect service using the [**WSAMSG**](/windows/desktop/api/ws2def/ns-ws2def-wsamsg) structure used with the [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) function.</span></span>
<span data-ttu-id="dda0b-200">Le membre de contrôle de la structure [**WSAMSG**](/windows/desktop/api/ws2def/ns-ws2def-wsamsg) a un cmsg_type dans la structure **WSACMSGHDR** défini sur **l' \_ \_ \_ enregistrement de redirection de connexion IP**.</span><span class="sxs-lookup"><span data-stu-id="dda0b-200">The Control member of the [**WSAMSG**](/windows/desktop/api/ws2def/ns-ws2def-wsamsg) structure would have a cmsg_type in the **WSACMSGHDR** structure set to **IP\_CONNECTION\_REDIRECT\_RECORD**.</span></span>
<span data-ttu-id="dda0b-201">Le paramètre [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) doit être fourni par le service de redirection lors de l’acceptation de redirections non-TCP.</span><span class="sxs-lookup"><span data-stu-id="dda0b-201">The [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) parameter must be supplied by the redirect service when accepting non-TCP redirects.</span></span>

<span data-ttu-id="dda0b-202">Pour le trafic non-TCP, l’enregistrement de redirection est transféré à l’aide de la structure [**WSAMSG**](/windows/desktop/api/ws2def/ns-ws2def-wsamsg) avec la fonction [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) .</span><span class="sxs-lookup"><span data-stu-id="dda0b-202">For non-TCP traffic, the redirect record is forwarded using the [**WSAMSG**](/windows/desktop/api/ws2def/ns-ws2def-wsamsg) structure with the [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) function.</span></span>

<span data-ttu-id="dda0b-203">Notez que pour le trafic non-TCP, seul le paquet de création de flux contiendra l' **\_ \_ \_ enregistrement de redirection de connexion IP**.</span><span class="sxs-lookup"><span data-stu-id="dda0b-203">Note that for non-TCP traffic, only the flow-creating packet will carry the **IP\_CONNECTION\_REDIRECT\_RECORD**.</span></span>
<span data-ttu-id="dda0b-204">Par conséquent, seul le premier paquet proxy doit inclure ces informations à l’aide de la fonction [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) .</span><span class="sxs-lookup"><span data-stu-id="dda0b-204">As a result, only the first proxied packet needs to include this information using the [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) function.</span></span>

<span data-ttu-id="dda0b-205">Étant donné que l’enregistrement de redirection WFP est un objet blob de données de longueur variable, l’appelant peut soit fournir une mémoire tampon de sortie importante (une mémoire tampon de 1 024 octets pointée par le paramètre *lpvOutBuffer* , par exemple), soit passer une taille de mémoire tampon de sortie dans le paramètre *cbOutBuffer* de 0 pour interroger la taille de mémoire tampon requise pour contenir l’objet BLOB retourné.</span><span class="sxs-lookup"><span data-stu-id="dda0b-205">Since the WFP redirect record is a variable length data blob, the caller can either supply a large output buffer (a 1,024 byte buffer pointed to by the *lpvOutBuffer* parameter, for example) or can pass an output buffer size in the *cbOutBuffer* parameter of 0 to query the buffer size required to hold the returned blob.</span></span>
<span data-ttu-id="dda0b-206">Si la taille de la mémoire tampon de sortie n’est pas suffisante pour contenir les données, les fonctions [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** retournent l' **erreur \_ \_ mémoire tampon insuffisante** et la taille de mémoire tampon requise est retournée dans la valeur désignée par le paramètre *lpcbBytesReturned* .</span><span class="sxs-lookup"><span data-stu-id="dda0b-206">If the output buffer size is not sufficient to the hold the data, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** functions will return **ERROR\_INSUFFICIENT\_BUFFER** and the required buffer size will be returned in value pointed to by the *lpcbBytesReturned* parameter.</span></span>

<span data-ttu-id="dda0b-207">L’application qui appelle le [**SIO_QUERY_WFP_CONNECTION_REDIRECT_CONTEXT**](sio-query-wfp-connection-redirect-context.md) n’a pas besoin de comprendre l’objet blob contenant le contexte de redirection récupéré.</span><span class="sxs-lookup"><span data-stu-id="dda0b-207">The application calling the [**SIO_QUERY_WFP_CONNECTION_REDIRECT_CONTEXT**](sio-query-wfp-connection-redirect-context.md) does not need to understand the blob containing the redirect context retrieved.</span></span>
<span data-ttu-id="dda0b-208">Il s’agit d’un objet blob opaque de données que l’application doit récupérer et renvoyer au nouveau Socket.</span><span class="sxs-lookup"><span data-stu-id="dda0b-208">This is an opaque blob of data that the application needs to retrieve and pass back to the new socket.</span></span>

## <a name="see-also"></a><span data-ttu-id="dda0b-209">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dda0b-209">See also</span></span>

[<span data-ttu-id="dda0b-210">**Options de socket IPPROTO_IP**</span><span class="sxs-lookup"><span data-stu-id="dda0b-210">**IPPROTO_IP Socket Options**</span></span>](/windows/desktop/winsock/ipproto-ip-socket-options)

[<span data-ttu-id="dda0b-211">**SIO_QUERY_WFP_CONNECTION_REDIRECT_CONTEXT**</span><span class="sxs-lookup"><span data-stu-id="dda0b-211">**SIO_QUERY_WFP_CONNECTION_REDIRECT_CONTEXT**</span></span>](sio-query-wfp-connection-redirect-context.md)

[<span data-ttu-id="dda0b-212">**socle**</span><span class="sxs-lookup"><span data-stu-id="dda0b-212">**socket**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-socket)

[<span data-ttu-id="dda0b-213">**WSAGetLastError**</span><span class="sxs-lookup"><span data-stu-id="dda0b-213">**WSAGetLastError**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetlasterror)

[<span data-ttu-id="dda0b-214">**WSAGetOverlappedResult**</span><span class="sxs-lookup"><span data-stu-id="dda0b-214">**WSAGetOverlappedResult**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[<span data-ttu-id="dda0b-215">**WSAIoctl**</span><span class="sxs-lookup"><span data-stu-id="dda0b-215">**WSAIoctl**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[<span data-ttu-id="dda0b-216">**WSAMSG**</span><span class="sxs-lookup"><span data-stu-id="dda0b-216">**WSAMSG**</span></span>](/windows/desktop/api/ws2def/ns-ws2def-wsamsg)

[<span data-ttu-id="dda0b-217">**WSAOVERLAPPED**</span><span class="sxs-lookup"><span data-stu-id="dda0b-217">**WSAOVERLAPPED**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[<span data-ttu-id="dda0b-218">**LPFN_WSARECVMSG (WSARecvMsg)**</span><span class="sxs-lookup"><span data-stu-id="dda0b-218">**LPFN_WSARECVMSG (WSARecvMsg)**</span></span>](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg)

[<span data-ttu-id="dda0b-219">**WSASendMsg**</span><span class="sxs-lookup"><span data-stu-id="dda0b-219">**WSASendMsg**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg)

[<span data-ttu-id="dda0b-220">**WSASocketA**</span><span class="sxs-lookup"><span data-stu-id="dda0b-220">**WSASocketA**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[<span data-ttu-id="dda0b-221">**WSASocketW**</span><span class="sxs-lookup"><span data-stu-id="dda0b-221">**WSASocketW**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
