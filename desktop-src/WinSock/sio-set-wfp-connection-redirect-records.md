---
description: Le code de contrôle définit l’enregistrement de redirection sur le nouveau socket TCP utilisé pour la connexion du service de redirection.
ms.assetid: 0AC78ED4-A6EC-4D62-919C-1EF7CDE8EE80
title: SIO_SET_WFP_CONNECTION_REDIRECT_RECORDS, code de contrôle
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 11ce07c94104ecd986dc117b00dba2a49a7b5dc5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106529345"
---
# <a name="sio_set_wfp_connection_redirect_records-control-code"></a><span data-ttu-id="68c81-103">SIO_SET_WFP_CONNECTION_REDIRECT_RECORDS, code de contrôle</span><span class="sxs-lookup"><span data-stu-id="68c81-103">SIO_SET_WFP_CONNECTION_REDIRECT_RECORDS Control Code</span></span>

## <a name="description"></a><span data-ttu-id="68c81-104">Description</span><span class="sxs-lookup"><span data-stu-id="68c81-104">Description</span></span>

<span data-ttu-id="68c81-105">Le code de contrôle des **\_ \_ \_ \_ \_ enregistrements de redirection de connexion SIO Set WFP** définit l’enregistrement de redirection sur le nouveau socket TCP utilisé pour se connecter à la destination finale en vue d’une utilisation par un service de redirection de plateforme de filtrage Windows (WFP).</span><span class="sxs-lookup"><span data-stu-id="68c81-105">The **SIO\_SET\_WFP\_CONNECTION\_REDIRECT\_RECORDS** control code sets the redirect record to the new TCP socket used for connecting to the final destination for use by a Windows Filtering Platform (WFP) redirect service.</span></span>

<span data-ttu-id="68c81-106">Pour effectuer cette opération, appelez la fonction [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** avec les paramètres suivants.</span><span class="sxs-lookup"><span data-stu-id="68c81-106">To perform this operation, call the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function with the following parameters.</span></span>

```cpp
int WSAIoctl(
  (socket) s,                              // descriptor identifying a socket
  SIO_SET_WFP_CONNECTION_REDIRECT_RECORDS, // dwIoControlCode
  (LPVOID) lpvInputBuffer,                 // lpvInBuffer
  (DWORD) cbInputBuffer,                   // cbInBuffer
  NULL,                                    // output buffer
  0,                                       // size of output buffer
  (LPDWORD) lpcbBytesReturned,             // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,          // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine, // completion routine
);
```

```cpp
int WSPIoctl(
  (socket) s,                              // descriptor identifying a socket
  SIO_SET_WFP_CONNECTION_REDIRECT_RECORDS, // dwIoControlCode
  (LPVOID) lpvInputBuffer,                 // lpvInBuffer
  (DWORD) cbInputBuffer,                   // cbInBuffer
  NULL,                                    // output buffer
  0,                                       // size of output buffer
  (LPDWORD) lpcbBytesReturned,             // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,          // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
  (LPWSATHREADID) lpThreadId,              // a WSATHREADID structure
  (LPINT) lpErrno                          // a pointer to the error code.
);
```

## <a name="parameters"></a><span data-ttu-id="68c81-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="68c81-107">Parameters</span></span>

### <a name="s"></a><span data-ttu-id="68c81-108">s</span><span class="sxs-lookup"><span data-stu-id="68c81-108">s</span></span>

<span data-ttu-id="68c81-109">Descripteur identifiant un Socket.</span><span class="sxs-lookup"><span data-stu-id="68c81-109">A descriptor identifying a socket.</span></span>

### <a name="dwiocontrolcode"></a><span data-ttu-id="68c81-110">dwIoControlCode</span><span class="sxs-lookup"><span data-stu-id="68c81-110">dwIoControlCode</span></span>

<span data-ttu-id="68c81-111">Code de contrôle de l’opération.</span><span class="sxs-lookup"><span data-stu-id="68c81-111">The control code for the operation.</span></span>
<span data-ttu-id="68c81-112">Utilisez **SIO pour \_ définir les \_ \_ \_ \_ enregistrements de redirection de connexion WFP** pour cette opération.</span><span class="sxs-lookup"><span data-stu-id="68c81-112">Use **SIO\_SET\_WFP\_CONNECTION\_REDIRECT\_RECORDS** for this operation.</span></span>

### <a name="lpvinbuffer"></a><span data-ttu-id="68c81-113">lpvInBuffer</span><span class="sxs-lookup"><span data-stu-id="68c81-113">lpvInBuffer</span></span>

<span data-ttu-id="68c81-114">Pointeur vers la mémoire tampon d’entrée.</span><span class="sxs-lookup"><span data-stu-id="68c81-114">A pointer to the input buffer.</span></span>
<span data-ttu-id="68c81-115">Ce paramètre contient un pointeur vers l’enregistrement de redirection WFP associé au socket.</span><span class="sxs-lookup"><span data-stu-id="68c81-115">This parameter contains a pointer to the WFP redirect record associated with the socket.</span></span>

### <a name="cbinbuffer"></a><span data-ttu-id="68c81-116">cbInBuffer</span><span class="sxs-lookup"><span data-stu-id="68c81-116">cbInBuffer</span></span>

<span data-ttu-id="68c81-117">Taille, en octets, de la mémoire tampon d’entrée.</span><span class="sxs-lookup"><span data-stu-id="68c81-117">The size, in bytes, of the input buffer.</span></span>

### <a name="lpvoutbuffer"></a><span data-ttu-id="68c81-118">lpvOutBuffer</span><span class="sxs-lookup"><span data-stu-id="68c81-118">lpvOutBuffer</span></span>

<span data-ttu-id="68c81-119">Pointeur vers la mémoire tampon de sortie.</span><span class="sxs-lookup"><span data-stu-id="68c81-119">A pointer to the output buffer.</span></span>
<span data-ttu-id="68c81-120">Ce paramètre n’est pas utilisé pour cette opération.</span><span class="sxs-lookup"><span data-stu-id="68c81-120">This parameter is unused for this operation.</span></span>

### <a name="cboutbuffer"></a><span data-ttu-id="68c81-121">cbOutBuffer</span><span class="sxs-lookup"><span data-stu-id="68c81-121">cbOutBuffer</span></span>

<span data-ttu-id="68c81-122">Taille, en octets, de la mémoire tampon de sortie.</span><span class="sxs-lookup"><span data-stu-id="68c81-122">The size, in bytes, of the output buffer.</span></span>
<span data-ttu-id="68c81-123">Ce paramètre doit avoir la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="68c81-123">This parameter must be set to zero.</span></span>

### <a name="lpcbbytesreturned"></a><span data-ttu-id="68c81-124">lpcbBytesReturned</span><span class="sxs-lookup"><span data-stu-id="68c81-124">lpcbBytesReturned</span></span>

<span data-ttu-id="68c81-125">Pointeur vers une variable qui reçoit la taille, en octets, des données stockées dans la mémoire tampon de sortie.</span><span class="sxs-lookup"><span data-stu-id="68c81-125">A pointer to a variable that receives the size, in bytes, of the data stored in the output buffer.</span></span>

<span data-ttu-id="68c81-126">Si la mémoire tampon de sortie est trop petite, l’appel échoue, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) retourne [**WSAEINVAL**](windows-sockets-error-codes-2.md)et le paramètre *LpcbBytesReturned* pointe vers une valeur **DWORD** égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="68c81-126">If the output buffer is too small, the call fails, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) returns [**WSAEINVAL**](windows-sockets-error-codes-2.md), and the *lpcbBytesReturned* parameter points to a **DWORD** value of zero.</span></span>

<span data-ttu-id="68c81-127">Si *lpOverlapped* a la valeur **null**, la valeur **DWORD** vers laquelle pointe le paramètre *lpcbBytesReturned* retourné sur un appel réussi ne peut pas être égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="68c81-127">If *lpOverlapped* is **NULL**, the **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned on a successful call cannot be zero.</span></span>

<span data-ttu-id="68c81-128">Si le paramètre *lpOverlapped* n’a pas la **valeur null** pour les sockets superposés, les opérations qui ne peuvent pas être terminées immédiatement seront lancées et l’achèvement sera indiqué ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="68c81-128">If the *lpOverlapped* parameter is not **NULL** for overlapped sockets, operations that cannot be completed immediately will be initiated, and completion will be indicated at a later time.</span></span>
<span data-ttu-id="68c81-129">La valeur **DWORD** pointée par le paramètre *lpcbBytesReturned* retourné peut être égale à zéro, car la taille des données stockées ne peut pas être déterminée tant que l’opération avec chevauchement n’est pas terminée.</span><span class="sxs-lookup"><span data-stu-id="68c81-129">The **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned may be zero since the size of the data stored can't be determined until the overlapped operation has completed.</span></span>
<span data-ttu-id="68c81-130">L’état d’achèvement final peut être récupéré lorsque la méthode d’achèvement appropriée est signalée lorsque l’opération est terminée.</span><span class="sxs-lookup"><span data-stu-id="68c81-130">The final completion status can be retrieved when the appropriate completion method is signaled when the operation has completed.</span></span>

### <a name="lpvoverlapped"></a><span data-ttu-id="68c81-131">lpvOverlapped</span><span class="sxs-lookup"><span data-stu-id="68c81-131">lpvOverlapped</span></span>

<span data-ttu-id="68c81-132">Pointeur vers une structure [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) .</span><span class="sxs-lookup"><span data-stu-id="68c81-132">A pointer to a [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="68c81-133">Si le socket *s* a été créé sans l’attribut Overlapped, le paramètre *lpOverlapped* est ignoré.</span><span class="sxs-lookup"><span data-stu-id="68c81-133">If socket *s* was created without the overlapped attribute, the *lpOverlapped* parameter is ignored.</span></span>

<span data-ttu-id="68c81-134">Si *s* a été ouvert avec l’attribut Overlapped et que le paramètre *lpOverlapped* n’a pas la **valeur null**, l’opération est exécutée en tant qu’opération Overlapped (asynchrone).</span><span class="sxs-lookup"><span data-stu-id="68c81-134">If *s* was opened with the overlapped attribute and the *lpOverlapped* parameter is not **NULL**, the operation is performed as an overlapped (asynchronous) operation.</span></span>
<span data-ttu-id="68c81-135">Dans ce cas, le paramètre *lpOverlapped* doit pointer vers une structure [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) valide.</span><span class="sxs-lookup"><span data-stu-id="68c81-135">In this case, *lpOverlapped* parameter must point to a valid [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="68c81-136">Pour les opérations avec chevauchement, la fonction [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** retourne immédiatement, et la méthode d’achèvement appropriée est signalée lorsque l’opération est terminée.</span><span class="sxs-lookup"><span data-stu-id="68c81-136">For overlapped operations, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns immediately, and the appropriate completion method is signaled when the operation has been completed.</span></span>
<span data-ttu-id="68c81-137">Sinon, la fonction ne retourne pas jusqu’à ce que l’opération soit terminée ou qu’une erreur se produise.</span><span class="sxs-lookup"><span data-stu-id="68c81-137">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

### <a name="lpcompletionroutine"></a><span data-ttu-id="68c81-138">lpCompletionRoutine</span><span class="sxs-lookup"><span data-stu-id="68c81-138">lpCompletionRoutine</span></span>

<span data-ttu-id="68c81-139">Type : \_ In_opt \_ [ **LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span><span class="sxs-lookup"><span data-stu-id="68c81-139">Type: \_In_opt\_ [**LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span></span>

<span data-ttu-id="68c81-140">Pointeur vers la routine de saisie semi-automatique appelée lorsque l’opération est terminée (ignoré pour les sockets non superposés).</span><span class="sxs-lookup"><span data-stu-id="68c81-140">A pointer to the completion routine called when the operation has been completed (ignored for non-overlapped sockets).</span></span>

### <a name="lpthreadid"></a><span data-ttu-id="68c81-141">lpThreadId</span><span class="sxs-lookup"><span data-stu-id="68c81-141">lpThreadId</span></span>

<span data-ttu-id="68c81-142">Pointeur vers une structure [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) qui doit être utilisée par le fournisseur dans un appel ultérieur à [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc).</span><span class="sxs-lookup"><span data-stu-id="68c81-142">A pointer to a [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure to be used by the provider in a subsequent call to [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc).</span></span>
<span data-ttu-id="68c81-143">Le fournisseur doit stocker la structure [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) référencée (pas le pointeur vers le même) jusqu’à ce que la fonction [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) soit retournée.</span><span class="sxs-lookup"><span data-stu-id="68c81-143">The provider should store the referenced [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure (not the pointer to same) until after the [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) function returns.</span></span>

<span data-ttu-id="68c81-144">**Remarque**  Ce paramètre s’applique uniquement à la fonction **WSPIoctl** .</span><span class="sxs-lookup"><span data-stu-id="68c81-144">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

### <a name="lperrno"></a><span data-ttu-id="68c81-145">lpErrno</span><span class="sxs-lookup"><span data-stu-id="68c81-145">lpErrno</span></span>

<span data-ttu-id="68c81-146">Pointeur vers le code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="68c81-146">A pointer to the error code.</span></span>

<span data-ttu-id="68c81-147">**Remarque**  Ce paramètre s’applique uniquement à la fonction **WSPIoctl** .</span><span class="sxs-lookup"><span data-stu-id="68c81-147">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

## <a name="return-value"></a><span data-ttu-id="68c81-148">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="68c81-148">Return value</span></span>

<span data-ttu-id="68c81-149">Si l’opération se termine correctement, la fonction [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** retourne la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="68c81-149">If the operation completes successfully, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns zero.</span></span>

<span data-ttu-id="68c81-150">Si l’opération échoue ou est en attente, la fonction [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** retourne une **\_ erreur de socket**.</span><span class="sxs-lookup"><span data-stu-id="68c81-150">If the operation fails or is pending, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns **SOCKET\_ERROR**.</span></span>
<span data-ttu-id="68c81-151">Pour afficher les informations d’erreur étendues, appelez [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span><span class="sxs-lookup"><span data-stu-id="68c81-151">To get extended error information, call [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>

| <span data-ttu-id="68c81-152">Code d'erreur</span><span class="sxs-lookup"><span data-stu-id="68c81-152">Error code</span></span> | <span data-ttu-id="68c81-153">Signification</span><span class="sxs-lookup"><span data-stu-id="68c81-153">Meaning</span></span> |
|------------|---------|
| <span data-ttu-id="68c81-154">**\_e/s WSA \_ en attente**</span><span class="sxs-lookup"><span data-stu-id="68c81-154">**WSA\_IO\_PENDING**</span></span> | <span data-ttu-id="68c81-155">L’opération d’e/s avec chevauchement est en cours.</span><span class="sxs-lookup"><span data-stu-id="68c81-155">Overlapped I/O operation is in progress.</span></span> <span data-ttu-id="68c81-156">Cette valeur est retournée si une opération avec chevauchement a été correctement initiée et que son achèvement sera indiqué ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="68c81-156">This value is returned if an overlapped operation was successfully initiated and completion will be indicated at a later time.</span></span> |
| <span data-ttu-id="68c81-157">**\_opération WSA \_ abandonnée**</span><span class="sxs-lookup"><span data-stu-id="68c81-157">**WSA\_OPERATION\_ABORTED**</span></span> | <span data-ttu-id="68c81-158">L’opération d’e/s a été annulée en raison de la sortie d’un thread ou d’une demande de l’application.</span><span class="sxs-lookup"><span data-stu-id="68c81-158">The I/O operation has been aborted because of either a thread exit or an application request.</span></span> <span data-ttu-id="68c81-159">Cette erreur est retournée si une opération avec chevauchement a été annulée en raison de la fermeture du socket ou de l’exécution de la commande **SIO_FLUSH** ioctl.</span><span class="sxs-lookup"><span data-stu-id="68c81-159">This error is returned if an overlapped operation was canceled due to the closure of the socket or the execution of the **SIO_FLUSH** IOCTL command.</span></span> |
| <span data-ttu-id="68c81-160">**WSAEACCES**</span><span class="sxs-lookup"><span data-stu-id="68c81-160">**WSAEACCES**</span></span> | <span data-ttu-id="68c81-161">Une tentative a été effectuée pour accéder à un socket de manière interdite par ses autorisations d’accès.</span><span class="sxs-lookup"><span data-stu-id="68c81-161">An attempt was made to access a socket in a way forbidden by its access permissions.</span></span> <span data-ttu-id="68c81-162">Cette erreur est retournée dans plusieurs conditions : l’utilisateur n’a pas les privilèges d’administrateur requis sur l’ordinateur local ou l’application ne s’exécute pas dans un interpréteur de commandes amélioré en tant qu’administrateur intégré ( `RunAs administrator` ).</span><span class="sxs-lookup"><span data-stu-id="68c81-162">This error is returned under several conditions that include the following: the user lacks the required administrative privileges on the local computer or the application is not running in an enhanced shell as the built-in Administrator (`RunAs administrator`).</span></span> |
| <span data-ttu-id="68c81-163">**WSAEFAULT**</span><span class="sxs-lookup"><span data-stu-id="68c81-163">**WSAEFAULT**</span></span> | <span data-ttu-id="68c81-164">Le système a détecté une adresse de pointeur non valide lors de la tentative d’utilisation d’un argument de pointeur dans un appel.</span><span class="sxs-lookup"><span data-stu-id="68c81-164">The system detected an invalid pointer address in attempting to use a pointer argument in a call.</span></span> <span data-ttu-id="68c81-165">Cette erreur est retournée par le paramètre *lpvInBuffer*, *lpvoutBuffer*, *lpcbBytesReturned*, *lpOverlapped* ou *lpCompletionRoutine* n’est pas entièrement contenu dans une partie valide de l’espace d’adressage de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="68c81-165">This error is returned of the *lpvInBuffer*, *lpvoutBuffer*, *lpcbBytesReturned*, *lpOverlapped* or *lpCompletionRoutine* parameter is not totally contained in a valid part of the user address space.</span></span> |
| <span data-ttu-id="68c81-166">**WSAEINPROGRESS**</span><span class="sxs-lookup"><span data-stu-id="68c81-166">**WSAEINPROGRESS**</span></span> | <span data-ttu-id="68c81-167">Une opération de blocage est actuellement en cours d'exécution.</span><span class="sxs-lookup"><span data-stu-id="68c81-167">A blocking operation is currently executing.</span></span> <span data-ttu-id="68c81-168">Cette erreur est retournée si la fonction est appelée lorsqu’un rappel est en cours.</span><span class="sxs-lookup"><span data-stu-id="68c81-168">This error is returned if the function is invoked when a callback is in progress.</span></span> |
| <span data-ttu-id="68c81-169">**WSAEINTR**</span><span class="sxs-lookup"><span data-stu-id="68c81-169">**WSAEINTR**</span></span> | <span data-ttu-id="68c81-170">Une opération de blocage a été interrompue par un appel à **WSACancelBlockingCall**.</span><span class="sxs-lookup"><span data-stu-id="68c81-170">A blocking operation was interrupted by a call to **WSACancelBlockingCall**.</span></span> <span data-ttu-id="68c81-171">Cette erreur est retournée si une opération de blocage a été interrompue.</span><span class="sxs-lookup"><span data-stu-id="68c81-171">This error is returned if a blocking operation was interrupted.</span></span> |
| <span data-ttu-id="68c81-172">**WSAEINVAL**</span><span class="sxs-lookup"><span data-stu-id="68c81-172">**WSAEINVAL**</span></span> | <span data-ttu-id="68c81-173">Argument non valide fourni.</span><span class="sxs-lookup"><span data-stu-id="68c81-173">An invalid argument was supplied.</span></span> <span data-ttu-id="68c81-174">Cette erreur est retournée si le paramètre *dwIoControlCode* n’est pas une commande valide, si un paramètre d’entrée spécifié n’est pas acceptable ou si la commande n’est pas applicable au type de socket spécifié.</span><span class="sxs-lookup"><span data-stu-id="68c81-174">This error is returned if the *dwIoControlCode* parameter is not a valid command, or a specified input parameter is not acceptable, or the command is not applicable to the type of socket specified.</span></span> |
| <span data-ttu-id="68c81-175">**WSAENETDOWN**</span><span class="sxs-lookup"><span data-stu-id="68c81-175">**WSAENETDOWN**</span></span> | <span data-ttu-id="68c81-176">Une opération de socket a rencontré un réseau inactif.</span><span class="sxs-lookup"><span data-stu-id="68c81-176">A socket operation encountered a dead network.</span></span> <span data-ttu-id="68c81-177">Cette erreur est retournée si le sous-système réseau a échoué.</span><span class="sxs-lookup"><span data-stu-id="68c81-177">This error is returned if the network subsystem has failed.</span></span> |
| <span data-ttu-id="68c81-178">**WSAENOTSOCK**</span><span class="sxs-lookup"><span data-stu-id="68c81-178">**WSAENOTSOCK**</span></span> | <span data-ttu-id="68c81-179">Une opération a été tentée sur un qui n’est pas un Socket.</span><span class="sxs-lookup"><span data-stu-id="68c81-179">An operation was attempted on something that is not a socket.</span></span> <span data-ttu-id="68c81-180">Cette erreur est retournée si le *descripteur* n’est pas un Socket.</span><span class="sxs-lookup"><span data-stu-id="68c81-180">This error is returned if the descriptor *s* is not a socket.</span></span> |
| <span data-ttu-id="68c81-181">**WSAEOPNOTSUPP**</span><span class="sxs-lookup"><span data-stu-id="68c81-181">**WSAEOPNOTSUPP**</span></span> | <span data-ttu-id="68c81-182">L’opération tentée n’est pas prise en charge pour le type d’objet référencé.</span><span class="sxs-lookup"><span data-stu-id="68c81-182">The attempted operation is not supported for the type of object referenced.</span></span> <span data-ttu-id="68c81-183">Cette erreur est retournée si la commande IOCTL spécifiée n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="68c81-183">This error is returned if the specified IOCTL command is not supported.</span></span> <span data-ttu-id="68c81-184">Cette erreur est également retournée si **les \_ \_ \_ \_ \_ enregistrements de redirection de connexion SIO Set WFP** ne sont pas pris en charge par le fournisseur de transport.</span><span class="sxs-lookup"><span data-stu-id="68c81-184">This error is also returned if the **SIO\_SET\_WFP\_CONNECTION\_REDIRECT\_RECORDS** IOCTL is not supported by the transport provider.</span></span> |

## <a name="remarks"></a><span data-ttu-id="68c81-185">Notes</span><span class="sxs-lookup"><span data-stu-id="68c81-185">Remarks</span></span>

<span data-ttu-id="68c81-186">Les **\_ enregistrements de \_ \_ \_ redirection \_ de connexion SIO Set WFP** sont pris en charge sur Windows 8, Windows Server 2012 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="68c81-186">The **SIO\_SET\_WFP\_CONNECTION\_REDIRECT\_RECORDS** IOCTL is supported on Windows 8, and Windows Server 2012, and later versions of the operating system.</span></span>

<span data-ttu-id="68c81-187">WFP autorise l’accès au chemin de traitement des paquets TCP/IP, où les paquets sortants et entrants peuvent être examinés ou modifiés avant d’autoriser leur traitement ultérieur.</span><span class="sxs-lookup"><span data-stu-id="68c81-187">WFP allows access to the TCP/IP packet processing path, wherein outgoing and incoming packets can be examined or changed before allowing them to be processed further.</span></span>
<span data-ttu-id="68c81-188">En appuyant sur le chemin de traitement TCP/IP, les éditeurs de logiciels indépendants (ISV) peuvent créer plus facilement des pare-feu, des logiciels antivirus, des logiciels de diagnostic et d’autres types d’applications et de services.</span><span class="sxs-lookup"><span data-stu-id="68c81-188">By tapping into the TCP/IP processing path, independent software vendors (ISVs) can more easily create firewalls, antivirus software, diagnostic software, and other types of applications and services.</span></span>
<span data-ttu-id="68c81-189">WFP fournit des composants en mode utilisateur et en mode noyau afin que les éditeurs de logiciels indépendants puissent participer aux décisions de filtrage qui ont lieu dans plusieurs couches de la pile de protocole TCP/IP et dans tout le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="68c81-189">WFP provides user-mode and kernel-mode components so that third-party ISVs can participate in the filtering decisions that take place at several layers in the TCP/IP protocol stack and throughout the operating system.</span></span>
<span data-ttu-id="68c81-190">La fonctionnalité de redirection de connexion WFP permet à un pilote de noyau de légende WFP de rediriger une connexion localement vers un processus en mode utilisateur, d’effectuer l’inspection du contenu en mode utilisateur et de transférer le contenu inspecté à l’aide d’une connexion différente à la destination d’origine.</span><span class="sxs-lookup"><span data-stu-id="68c81-190">The WFP connection redirect feature allows a WFP callout kernel driver to redirect a connection locally to a user-mode process, perform content inspection in user-mode, and forward the inspected content using a different connection to the original destination.</span></span>

<span data-ttu-id="68c81-191">La **\_ connexion SIO \_ Set \_ WFP \_ redirige les \_ enregistrements** IOCTL et plusieurs autres IOCTL connexes sont des composants en mode utilisateur utilisés pour permettre à plusieurs applications de proxy de connexion WFP d’inspecter le même flux de trafic de manière coopérative.</span><span class="sxs-lookup"><span data-stu-id="68c81-191">The **SIO\_SET\_WFP\_CONNECTION\_REDIRECT\_RECORDS** IOCTL and several other related IOCTLS are user-mode components used to allow multiple WFP-based connection proxy applications to inspect the same traffic flow in a cooperative manner.</span></span>
<span data-ttu-id="68c81-192">Chaque agent d’inspection peut réinspecter en toute sécurité le trafic réseau qui a déjà été inspecté par un autre agent d’inspection.</span><span class="sxs-lookup"><span data-stu-id="68c81-192">Each inspection agent can safely re-inspect network traffic that has already been inspected by another inspection agent.</span></span>
<span data-ttu-id="68c81-193">Avec la présence de plusieurs proxys (développés par différents éditeurs de logiciels indépendants, par exemple), la connexion utilisée par un proxy pour communiquer avec la destination finale peut à son tour être redirigée par un second proxy, et cette nouvelle connexion peut être redirigée par le proxy d’origine.</span><span class="sxs-lookup"><span data-stu-id="68c81-193">With the presence of multiple proxies (developed by different ISVs, for example) the connection used by one proxy to communicate with the final destination could in turn be redirected by a second proxy, and that new connection could again be redirected by the original proxy.</span></span>
<span data-ttu-id="68c81-194">Sans le suivi de connexion, la connexion d’origine risque de ne jamais atteindre sa destination finale, car elle est bloquée dans une boucle de proxy infinie.</span><span class="sxs-lookup"><span data-stu-id="68c81-194">Without connection tracking, the original connection might never reach its final destination as it gets stuck in an infinite proxy loop.</span></span>

<span data-ttu-id="68c81-195">Les **\_ enregistrements de \_ \_ \_ redirection \_ de connexion SIO Set WFP** permettent d’assurer le suivi des connexions en proxy sur les connexions de socket redirigées.</span><span class="sxs-lookup"><span data-stu-id="68c81-195">The **SIO\_SET\_WFP\_CONNECTION\_REDIRECT\_RECORDS** IOCTL is used to provide proxied connection tracking on redirected socket connections.</span></span>
<span data-ttu-id="68c81-196">Cette fonctionnalité WFP facilite le suivi des enregistrements de redirection à partir de la redirection initiale d’une connexion à la connexion finale à la destination.</span><span class="sxs-lookup"><span data-stu-id="68c81-196">This WFP feature facilitates tracking of redirection records from the initial redirect of a connection to the final connection to the destination.</span></span>

<span data-ttu-id="68c81-197">Le [**SIO_QUERY_WFP_CONNECTION_REDIRECT_RECORDS**](sio-query-wfp-connection-redirect-records.md) IOCTL est utilisé par un service de redirection basé sur WFP pour récupérer l’enregistrement de redirection à partir de la connexion de paquet TCP/IP acceptée (le socket connecté pour un socket TCP ou un socket UDP, par exemple) redirigé vers celui-ci par son compagnon en mode noyau qui est inscrit aux couches de  **\_ \_ redirection de connexion ALE** dans un pilote en mode noyau.</span><span class="sxs-lookup"><span data-stu-id="68c81-197">The [**SIO_QUERY_WFP_CONNECTION_REDIRECT_RECORDS**](sio-query-wfp-connection-redirect-records.md) IOCTL is used by a WFP-based redirect service to retrieve the redirect record from the accepted TCP/IP packet connection (the connected socket for a TCP socket or a UDP socket, for example) redirected to it by its companion kernel-mode callout registered at  **ALE\_CONNECT\_REDIRECT** layers in a kernel-mode driver.</span></span>
<span data-ttu-id="68c81-198">L’IOCTL [**SIO_QUERY_WFP_CONNECTION_REDIRECT_CONTEXT**](sio-query-wfp-connection-redirect-context.md) récupère le contexte de redirection pour un enregistrement de redirection, qui est utilisé.</span><span class="sxs-lookup"><span data-stu-id="68c81-198">The [**SIO_QUERY_WFP_CONNECTION_REDIRECT_CONTEXT**](sio-query-wfp-connection-redirect-context.md) IOCTL retrieves the redirect context for a redirect record, which is used.</span></span>
<span data-ttu-id="68c81-199">Le contexte de redirection est facultatif et est utilisé si l’état de redirection actuel d’une connexion est que la connexion a été redirigée par le service de redirection appelant ou si la connexion a été précédemment redirigée par le service de redirection appelant, mais redirigée ultérieurement par un autre service de redirection. Le service de redirection transfère l’enregistrement de redirection récupéré au socket TCP qu’il utilise pour effectuer un proxy du contenu d’origine à l’aide de l' **SIO \_ définir la \_ connexion WFP des \_ \_ \_ enregistrements de redirection** ioctl.</span><span class="sxs-lookup"><span data-stu-id="68c81-199">The redirect context is optional and is used if the current redirection state of a connection is that the connection was redirected by the calling redirect service or the connection was previously redirected by the calling redirect service but later redirected again by a different redirect service.The redirect service transfers the retrieved redirect record to the TCP socket it uses to proxy the original content using the **SIO\_SET\_WFP\_CONNECTION\_REDIRECT\_RECORDS** IOCTL.</span></span>

<span data-ttu-id="68c81-200">L’application qui appelle **les \_ \_ \_ \_ \_ enregistrements de redirection de connexion SIO Set WFP** n’a pas besoin de comprendre l’objet blob contenant l’enregistrement de redirection en cours de définition.</span><span class="sxs-lookup"><span data-stu-id="68c81-200">The application calling the **SIO\_SET\_WFP\_CONNECTION\_REDIRECT\_RECORDS** IOCTL does not need to understand the blob containing the redirect record being set.</span></span>
<span data-ttu-id="68c81-201">Il s’agit d’un objet blob opaque de données que l’application doit renvoyer au nouveau Socket.</span><span class="sxs-lookup"><span data-stu-id="68c81-201">This is an opaque blob of data that the application needs to pass back to the new socket.</span></span>

## <a name="see-also"></a><span data-ttu-id="68c81-202">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="68c81-202">See also</span></span>

[<span data-ttu-id="68c81-203">**Options de socket IPPROTO_IP**</span><span class="sxs-lookup"><span data-stu-id="68c81-203">**IPPROTO_IP Socket Options**</span></span>](/windows/desktop/winsock/ipproto-ip-socket-options)

[<span data-ttu-id="68c81-204">**SIO_QUERY_WFP_CONNECTION_REDIRECT_CONTEXT**</span><span class="sxs-lookup"><span data-stu-id="68c81-204">**SIO_QUERY_WFP_CONNECTION_REDIRECT_CONTEXT**</span></span>](sio-query-wfp-connection-redirect-context.md)

[<span data-ttu-id="68c81-205">**SIO_QUERY_WFP_CONNECTION_REDIRECT_RECORDS**</span><span class="sxs-lookup"><span data-stu-id="68c81-205">**SIO_QUERY_WFP_CONNECTION_REDIRECT_RECORDS**</span></span>](sio-query-wfp-connection-redirect-records.md)

[<span data-ttu-id="68c81-206">**socle**</span><span class="sxs-lookup"><span data-stu-id="68c81-206">**socket**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-socket)

[<span data-ttu-id="68c81-207">**WSAGetLastError**</span><span class="sxs-lookup"><span data-stu-id="68c81-207">**WSAGetLastError**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetlasterror)

[<span data-ttu-id="68c81-208">**WSAGetOverlappedResult**</span><span class="sxs-lookup"><span data-stu-id="68c81-208">**WSAGetOverlappedResult**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[<span data-ttu-id="68c81-209">**WSAIoctl**</span><span class="sxs-lookup"><span data-stu-id="68c81-209">**WSAIoctl**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[<span data-ttu-id="68c81-210">**WSAOVERLAPPED**</span><span class="sxs-lookup"><span data-stu-id="68c81-210">**WSAOVERLAPPED**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[<span data-ttu-id="68c81-211">**WSASocketA**</span><span class="sxs-lookup"><span data-stu-id="68c81-211">**WSASocketA**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[<span data-ttu-id="68c81-212">**WSASocketW**</span><span class="sxs-lookup"><span data-stu-id="68c81-212">**WSASocketW**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
