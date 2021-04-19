---
description: Le code de contrôle applique un ou plusieurs paramètres de transport à un Socket.
ms.assetid: FA0657EE-B65E-4EFA-AF1E-CA0EA7B27715
title: Code de contrôle SIO_APPLY_TRANSPORT_SETTING
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: e167a87e70dc3c6c44a263308beb333176a3d525
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518175"
---
# <a name="sio_apply_transport_setting-control-code"></a><span data-ttu-id="05a50-103">Code de contrôle SIO_APPLY_TRANSPORT_SETTING</span><span class="sxs-lookup"><span data-stu-id="05a50-103">SIO_APPLY_TRANSPORT_SETTING Control Code</span></span>

## <a name="description"></a><span data-ttu-id="05a50-104">Description</span><span class="sxs-lookup"><span data-stu-id="05a50-104">Description</span></span>

<span data-ttu-id="05a50-105">Le **SIO \_ appliquer \_ \_** le code de contrôle du paramètre de transport applique un ou plusieurs paramètres de transport à un Socket.</span><span class="sxs-lookup"><span data-stu-id="05a50-105">The **SIO\_APPLY\_TRANSPORT\_SETTING** control code applies one or more transport settings to a socket.</span></span>

<span data-ttu-id="05a50-106">Pour effectuer cette opération, appelez la fonction [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** avec les paramètres suivants.</span><span class="sxs-lookup"><span data-stu-id="05a50-106">To perform this operation, call the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function with the following parameters.</span></span>

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_APPLY_TRANSPORT_SETTING, // dwIoControlCode
  (LPVOID) lpvInBuffer,  // pointer to the input buffer
  (DWORD) cbInBuffer,    // size, in bytes, of the input buffer
  (LPVOID) lpvOutBuffer,             // pointer to the output buffer
  (DWORD) cbOutBuffer,   // size, in bytes, of the output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

```cpp
int WSPIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_APPLY_TRANSPORT_SETTING, // dwIoControlCode
  (LPVOID) lpvInBuffer,  // pointer to the input buffer
  (DWORD) cbInBuffer,    // size, in bytes, of the input buffer
  (LPVOID) lpvOutBuffer,             // pointer to the output buffer
  (DWORD) cbOutBuffer,   // size, in bytes, of the output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
  (LPWSATHREADID) lpThreadId,   // a WSATHREADID structure
  (LPINT) lpErrno   // a pointer to the error code.
);
```

## <a name="parameters"></a><span data-ttu-id="05a50-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="05a50-107">Parameters</span></span>

### <a name="s"></a><span data-ttu-id="05a50-108">s</span><span class="sxs-lookup"><span data-stu-id="05a50-108">s</span></span>

<span data-ttu-id="05a50-109">Descripteur identifiant un Socket.</span><span class="sxs-lookup"><span data-stu-id="05a50-109">A descriptor identifying a socket.</span></span>

### <a name="dwiocontrolcode"></a><span data-ttu-id="05a50-110">dwIoControlCode</span><span class="sxs-lookup"><span data-stu-id="05a50-110">dwIoControlCode</span></span>

<span data-ttu-id="05a50-111">Code de contrôle de l’opération.</span><span class="sxs-lookup"><span data-stu-id="05a50-111">The control code for the operation.</span></span>
<span data-ttu-id="05a50-112">Utilisez **SIO \_ appliquer \_ le \_ paramètre de transport** pour cette opération.</span><span class="sxs-lookup"><span data-stu-id="05a50-112">Use **SIO\_APPLY\_TRANSPORT\_SETTING** for this operation.</span></span>

### <a name="lpvinbuffer"></a><span data-ttu-id="05a50-113">lpvInBuffer</span><span class="sxs-lookup"><span data-stu-id="05a50-113">lpvInBuffer</span></span>

<span data-ttu-id="05a50-114">Pointeur vers la mémoire tampon d’entrée.</span><span class="sxs-lookup"><span data-stu-id="05a50-114">A pointer to the input buffer.</span></span>
<span data-ttu-id="05a50-115">Ce paramètre contient un pointeur vers une structure dans laquelle le premier membre de la structure est une structure [**TRANSPORT_SETTING_ID**](/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id) qui détermine le paramètre de transport appliqué.</span><span class="sxs-lookup"><span data-stu-id="05a50-115">This parameter contains a pointer to a structure where the first member of the structure is a [**TRANSPORT_SETTING_ID**](/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id) structure that determines what transport setting is being applied.</span></span>

### <a name="cbinbuffer"></a><span data-ttu-id="05a50-116">cbInBuffer</span><span class="sxs-lookup"><span data-stu-id="05a50-116">cbInBuffer</span></span>

<span data-ttu-id="05a50-117">Taille, en octets, de la mémoire tampon d’entrée.</span><span class="sxs-lookup"><span data-stu-id="05a50-117">The size, in bytes, of the input buffer.</span></span>
<span data-ttu-id="05a50-118">Ce paramètre dépend du paramètre de transport appliqué.</span><span class="sxs-lookup"><span data-stu-id="05a50-118">This parameter depends on the transport setting being applied.</span></span>

### <a name="lpvoutbuffer"></a><span data-ttu-id="05a50-119">lpvOutBuffer</span><span class="sxs-lookup"><span data-stu-id="05a50-119">lpvOutBuffer</span></span>

<span data-ttu-id="05a50-120">Pointeur vers la mémoire tampon de sortie.</span><span class="sxs-lookup"><span data-stu-id="05a50-120">A pointer to the output buffer.</span></span>
<span data-ttu-id="05a50-121">Ce paramètre dépend du paramètre de transport appliqué.</span><span class="sxs-lookup"><span data-stu-id="05a50-121">This parameter depends on the transport setting being applied.</span></span>

### <a name="cboutbuffer"></a><span data-ttu-id="05a50-122">cbOutBuffer</span><span class="sxs-lookup"><span data-stu-id="05a50-122">cbOutBuffer</span></span>

<span data-ttu-id="05a50-123">Taille, en octets, de la mémoire tampon de sortie.</span><span class="sxs-lookup"><span data-stu-id="05a50-123">The size, in bytes, of the output buffer.</span></span>

### <a name="lpcbbytesreturned"></a><span data-ttu-id="05a50-124">lpcbBytesReturned</span><span class="sxs-lookup"><span data-stu-id="05a50-124">lpcbBytesReturned</span></span>

<span data-ttu-id="05a50-125">Pointeur vers une variable qui reçoit la taille, en octets, des données stockées dans la mémoire tampon de sortie.</span><span class="sxs-lookup"><span data-stu-id="05a50-125">A pointer to a variable that receives the size, in bytes, of the data stored in the output buffer.</span></span>

<span data-ttu-id="05a50-126">Si la mémoire tampon de sortie est trop petite, l’appel échoue, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) retourne [**WSAEINVAL**](windows-sockets-error-codes-2.md)et le paramètre *LpcbBytesReturned* pointe vers une valeur **DWORD** égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="05a50-126">If the output buffer is too small, the call fails, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) returns [**WSAEINVAL**](windows-sockets-error-codes-2.md), and the *lpcbBytesReturned* parameter points to a **DWORD** value of zero.</span></span>

<span data-ttu-id="05a50-127">Si *lpOverlapped* a la valeur **null**, la valeur **DWORD** vers laquelle pointe le paramètre *lpcbBytesReturned* retourné sur un appel réussi ne peut pas être égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="05a50-127">If *lpOverlapped* is **NULL**, the **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned on a successful call cannot be zero.</span></span>

<span data-ttu-id="05a50-128">Si le paramètre *lpOverlapped* n’a pas la **valeur null** pour les sockets superposés, les opérations qui ne peuvent pas être terminées immédiatement seront lancées et l’achèvement sera indiqué ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="05a50-128">If the *lpOverlapped* parameter is not **NULL** for overlapped sockets, operations that cannot be completed immediately will be initiated, and completion will be indicated at a later time.</span></span>
<span data-ttu-id="05a50-129">La valeur **DWORD** pointée par le paramètre *lpcbBytesReturned* retourné peut être égale à zéro, car la taille des données stockées ne peut pas être déterminée tant que l’opération avec chevauchement n’est pas terminée.</span><span class="sxs-lookup"><span data-stu-id="05a50-129">The **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned may be zero since the size of the data stored can't be determined until the overlapped operation has completed.</span></span>
<span data-ttu-id="05a50-130">L’état d’achèvement final peut être récupéré lorsque la méthode d’achèvement appropriée est signalée lorsque l’opération est terminée.</span><span class="sxs-lookup"><span data-stu-id="05a50-130">The final completion status can be retrieved when the appropriate completion method is signaled when the operation has completed.</span></span>

### <a name="lpvoverlapped"></a><span data-ttu-id="05a50-131">lpvOverlapped</span><span class="sxs-lookup"><span data-stu-id="05a50-131">lpvOverlapped</span></span>

<span data-ttu-id="05a50-132">Pointeur vers une structure [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) .</span><span class="sxs-lookup"><span data-stu-id="05a50-132">A pointer to a [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="05a50-133">Si le socket *s* a été créé sans l’attribut Overlapped, le paramètre *lpOverlapped* est ignoré.</span><span class="sxs-lookup"><span data-stu-id="05a50-133">If socket *s* was created without the overlapped attribute, the *lpOverlapped* parameter is ignored.</span></span>

<span data-ttu-id="05a50-134">Si *s* a été ouvert avec l’attribut Overlapped et que le paramètre *lpOverlapped* n’a pas la **valeur null**, l’opération est exécutée en tant qu’opération Overlapped (asynchrone).</span><span class="sxs-lookup"><span data-stu-id="05a50-134">If *s* was opened with the overlapped attribute and the *lpOverlapped* parameter is not **NULL**, the operation is performed as an overlapped (asynchronous) operation.</span></span>
<span data-ttu-id="05a50-135">Dans ce cas, le paramètre *lpOverlapped* doit pointer vers une structure [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) valide.</span><span class="sxs-lookup"><span data-stu-id="05a50-135">In this case, *lpOverlapped* parameter must point to a valid [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="05a50-136">Pour les opérations avec chevauchement, la fonction [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** retourne immédiatement, et la méthode d’achèvement appropriée est signalée lorsque l’opération est terminée.</span><span class="sxs-lookup"><span data-stu-id="05a50-136">For overlapped operations, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns immediately, and the appropriate completion method is signaled when the operation has been completed.</span></span>
<span data-ttu-id="05a50-137">Sinon, la fonction ne retourne pas jusqu’à ce que l’opération soit terminée ou qu’une erreur se produise.</span><span class="sxs-lookup"><span data-stu-id="05a50-137">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

### <a name="lpcompletionroutine"></a><span data-ttu-id="05a50-138">lpCompletionRoutine</span><span class="sxs-lookup"><span data-stu-id="05a50-138">lpCompletionRoutine</span></span>

<span data-ttu-id="05a50-139">Type : \_ In_opt \_ [ **LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span><span class="sxs-lookup"><span data-stu-id="05a50-139">Type: \_In_opt\_ [**LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span></span>

<span data-ttu-id="05a50-140">Pointeur vers la routine de saisie semi-automatique appelée lorsque l’opération est terminée (ignoré pour les sockets non superposés).</span><span class="sxs-lookup"><span data-stu-id="05a50-140">A pointer to the completion routine called when the operation has been completed (ignored for non-overlapped sockets).</span></span>

### <a name="lpthreadid"></a><span data-ttu-id="05a50-141">lpThreadId</span><span class="sxs-lookup"><span data-stu-id="05a50-141">lpThreadId</span></span>

<span data-ttu-id="05a50-142">Pointeur vers une structure [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) qui doit être utilisée par le fournisseur dans un appel ultérieur à [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc).</span><span class="sxs-lookup"><span data-stu-id="05a50-142">A pointer to a [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure to be used by the provider in a subsequent call to [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc).</span></span>
<span data-ttu-id="05a50-143">Le fournisseur doit stocker la structure [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) référencée (pas le pointeur vers le même) jusqu’à ce que la fonction [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) soit retournée.</span><span class="sxs-lookup"><span data-stu-id="05a50-143">The provider should store the referenced [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure (not the pointer to same) until after the [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) function returns.</span></span>

<span data-ttu-id="05a50-144">**Remarque**  Ce paramètre s’applique uniquement à la fonction **WSPIoctl** .</span><span class="sxs-lookup"><span data-stu-id="05a50-144">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

### <a name="lperrno"></a><span data-ttu-id="05a50-145">lpErrno</span><span class="sxs-lookup"><span data-stu-id="05a50-145">lpErrno</span></span>

<span data-ttu-id="05a50-146">Pointeur vers le code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="05a50-146">A pointer to the error code.</span></span>

<span data-ttu-id="05a50-147">**Remarque**  Ce paramètre s’applique uniquement à la fonction **WSPIoctl** .</span><span class="sxs-lookup"><span data-stu-id="05a50-147">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

## <a name="return-value"></a><span data-ttu-id="05a50-148">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="05a50-148">Return value</span></span>

<span data-ttu-id="05a50-149">Si l’opération se termine correctement, la fonction [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** retourne la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="05a50-149">If the operation completes successfully, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns zero.</span></span>

<span data-ttu-id="05a50-150">Si l’opération échoue ou est en attente, la fonction [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** retourne une **\_ erreur de socket**.</span><span class="sxs-lookup"><span data-stu-id="05a50-150">If the operation fails or is pending, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns **SOCKET\_ERROR**.</span></span>
<span data-ttu-id="05a50-151">Pour afficher les informations d’erreur étendues, appelez [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span><span class="sxs-lookup"><span data-stu-id="05a50-151">To get extended error information, call [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>

| <span data-ttu-id="05a50-152">Code d'erreur</span><span class="sxs-lookup"><span data-stu-id="05a50-152">Error code</span></span> | <span data-ttu-id="05a50-153">Signification</span><span class="sxs-lookup"><span data-stu-id="05a50-153">Meaning</span></span> |
|------------|---------|
|<span data-ttu-id="05a50-154">**\_e/s WSA \_ en attente**</span><span class="sxs-lookup"><span data-stu-id="05a50-154">**WSA\_IO\_PENDING**</span></span> | <span data-ttu-id="05a50-155">L’opération d’e/s avec chevauchement est en cours.</span><span class="sxs-lookup"><span data-stu-id="05a50-155">Overlapped I/O operation is in progress.</span></span> <span data-ttu-id="05a50-156">Cette valeur est retournée si une opération avec chevauchement a été correctement initiée et que son achèvement sera indiqué ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="05a50-156">This value is returned if an overlapped operation was successfully initiated and completion will be indicated at a later time.</span></span> |
| <span data-ttu-id="05a50-157">**\_opération WSA \_ abandonnée**</span><span class="sxs-lookup"><span data-stu-id="05a50-157">**WSA\_OPERATION\_ABORTED**</span></span> | <span data-ttu-id="05a50-158">L’opération d’e/s a été annulée en raison de la sortie d’un thread ou d’une demande de l’application.</span><span class="sxs-lookup"><span data-stu-id="05a50-158">The I/O operation has been aborted because of either a thread exit or an application request.</span></span> <span data-ttu-id="05a50-159">Cette erreur est retournée si une opération avec chevauchement a été annulée en raison de la fermeture du socket ou de l’exécution de la commande **SIO \_ flush** ioctl.</span><span class="sxs-lookup"><span data-stu-id="05a50-159">This error is returned if an overlapped operation was canceled due to the closure of the socket or the execution of the **SIO\_FLUSH** IOCTL command.</span></span> |
| <span data-ttu-id="05a50-160">**WSAEFAULT**</span><span class="sxs-lookup"><span data-stu-id="05a50-160">**WSAEFAULT**</span></span> | <span data-ttu-id="05a50-161">Le système a détecté une adresse de pointeur non valide lors de la tentative d’utilisation d’un argument de pointeur dans un appel.</span><span class="sxs-lookup"><span data-stu-id="05a50-161">The system detected an invalid pointer address in attempting to use a pointer argument in a call.</span></span> <span data-ttu-id="05a50-162">Cette erreur est retournée par le paramètre *lpvInBuffer*, *lpvoutBuffer*, *lpcbBytesReturned*, *lpOverlapped* ou *lpCompletionRoutine* n’est pas entièrement contenu dans une partie valide de l’espace d’adressage de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="05a50-162">This error is returned of the *lpvInBuffer*, *lpvoutBuffer*, *lpcbBytesReturned*, *lpOverlapped* or *lpCompletionRoutine* parameter is not totally contained in a valid part of the user address space.</span></span> |
| <span data-ttu-id="05a50-163">**WSAEINPROGRESS**</span><span class="sxs-lookup"><span data-stu-id="05a50-163">**WSAEINPROGRESS**</span></span> | <span data-ttu-id="05a50-164">Une opération de blocage est actuellement en cours d'exécution.</span><span class="sxs-lookup"><span data-stu-id="05a50-164">A blocking operation is currently executing.</span></span> <span data-ttu-id="05a50-165">Cette erreur est retournée si la fonction est appelée lorsqu’un rappel est en cours.</span><span class="sxs-lookup"><span data-stu-id="05a50-165">This error is returned if the function is invoked when a callback is in progress.</span></span> |
| <span data-ttu-id="05a50-166">**WSAEINTR**</span><span class="sxs-lookup"><span data-stu-id="05a50-166">**WSAEINTR**</span></span> | <span data-ttu-id="05a50-167">Une opération de blocage a été interrompue par un appel à [**WSACancelBlockingCall**](/windows/desktop/api/winsock2/nf-winsock2-wsacancelblockingcall).</span><span class="sxs-lookup"><span data-stu-id="05a50-167">A blocking operation was interrupted by a call to [**WSACancelBlockingCall**](/windows/desktop/api/winsock2/nf-winsock2-wsacancelblockingcall).</span></span> <span data-ttu-id="05a50-168">Cette erreur est retournée si une opération de blocage a été interrompue.</span><span class="sxs-lookup"><span data-stu-id="05a50-168">This error is returned if a blocking operation was interrupted.</span></span> |
| <span data-ttu-id="05a50-169">**WSAEINVAL**</span><span class="sxs-lookup"><span data-stu-id="05a50-169">**WSAEINVAL**</span></span> | <span data-ttu-id="05a50-170">Argument non valide fourni.</span><span class="sxs-lookup"><span data-stu-id="05a50-170">An invalid argument was supplied.</span></span> <span data-ttu-id="05a50-171">Cette erreur est retournée si le paramètre *dwIoControlCode* n’est pas une commande valide, si un paramètre d’entrée spécifié n’est pas acceptable ou si la commande n’est pas applicable au type de socket spécifié.</span><span class="sxs-lookup"><span data-stu-id="05a50-171">This error is returned if the *dwIoControlCode* parameter is not a valid command, or a specified input parameter is not acceptable, or the command is not applicable to the type of socket specified.</span></span> |
| <span data-ttu-id="05a50-172">**WSAENETDOWN**</span><span class="sxs-lookup"><span data-stu-id="05a50-172">**WSAENETDOWN**</span></span> | <span data-ttu-id="05a50-173">Une opération de socket a rencontré un réseau inactif.</span><span class="sxs-lookup"><span data-stu-id="05a50-173">A socket operation encountered a dead network.</span></span> <span data-ttu-id="05a50-174">Cette erreur est retournée si le sous-système réseau a échoué.</span><span class="sxs-lookup"><span data-stu-id="05a50-174">This error is returned if the network subsystem has failed.</span></span> |
| <span data-ttu-id="05a50-175">**WSAENOTSOCK**</span><span class="sxs-lookup"><span data-stu-id="05a50-175">**WSAENOTSOCK**</span></span> | <span data-ttu-id="05a50-176">Une opération a été tentée sur un qui n’est pas un Socket.</span><span class="sxs-lookup"><span data-stu-id="05a50-176">An operation was attempted on something that is not a socket.</span></span> <span data-ttu-id="05a50-177">Cette erreur est retournée si le *descripteur* n’est pas un Socket.</span><span class="sxs-lookup"><span data-stu-id="05a50-177">This error is returned if the descriptor *s* is not a socket.</span></span> |
| <span data-ttu-id="05a50-178">**WSAEOPNOTSUPP**</span><span class="sxs-lookup"><span data-stu-id="05a50-178">**WSAEOPNOTSUPP**</span></span> | <span data-ttu-id="05a50-179">L’opération tentée n’est pas prise en charge pour le type d’objet référencé.</span><span class="sxs-lookup"><span data-stu-id="05a50-179">The attempted operation is not supported for the type of object referenced.</span></span> <span data-ttu-id="05a50-180">Cette erreur est retournée si la commande IOCTL spécifiée n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="05a50-180">This error is returned if the specified IOCTL command is not supported.</span></span> <span data-ttu-id="05a50-181">Cette erreur est également retournée si l’IOCTL **SIO \_ appliquer le \_ \_ paramètre de transport** n’est pas prise en charge par le fournisseur de transport.</span><span class="sxs-lookup"><span data-stu-id="05a50-181">This error is also returned if the **SIO\_APPLY\_TRANSPORT\_SETTING** IOCTL is not supported by the transport provider.</span></span> <span data-ttu-id="05a50-182">Cette erreur est également retournée lorsqu’une tentative d’utilisation **du \_ \_ \_ paramètre de transport SIO Apply** est effectuée sur un socket autre que UDP ou TCP.</span><span class="sxs-lookup"><span data-stu-id="05a50-182">This error is also returned when an attempt to use the **SIO\_APPLY\_TRANSPORT\_SETTING** IOCTL is made on a socket other than UDP or TCP.</span></span> |

## <a name="remarks"></a><span data-ttu-id="05a50-183">Notes</span><span class="sxs-lookup"><span data-stu-id="05a50-183">Remarks</span></span>

<span data-ttu-id="05a50-184">Le **\_ paramètre d’application SIO Apply \_ transport \_** IOCTL est pris en charge sur windows 8, Windows Server 2012 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="05a50-184">The **SIO\_APPLY\_TRANSPORT\_SETTING** IOCTL is supported on Windows 8, and Windows Server 2012, and later versions of the operating system.</span></span>

<span data-ttu-id="05a50-185">Le **\_ paramètre de \_ transport \_ apply SIO** IOCTL est un ioctl générique utilisé pour appliquer le paramètre de transport au socket.</span><span class="sxs-lookup"><span data-stu-id="05a50-185">The **SIO\_APPLY\_TRANSPORT\_SETTING** IOCTL is a generic IOCTL used to apply transport setting to socket.</span></span>
<span data-ttu-id="05a50-186">Le paramètre de transport appliqué est basé sur le [**TRANSPORT_SETTING_ID**](/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id) passé dans le paramètre *lpvInBuffer* .</span><span class="sxs-lookup"><span data-stu-id="05a50-186">The transport setting being applied is based on the [**TRANSPORT_SETTING_ID**](/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id) passed in the *lpvInBuffer* parameter.</span></span>

<span data-ttu-id="05a50-187">À compter de Windows 8 et de Windows Server 2012, le système définit la fonctionnalité **REAL_TIME_NOTIFICATION_CAPABILITY** sur un socket TCP.</span><span class="sxs-lookup"><span data-stu-id="05a50-187">Starting with Windows 8 and Windows Server 2012, the system defines the **REAL_TIME_NOTIFICATION_CAPABILITY** capability on a TCP socket.</span></span>
<span data-ttu-id="05a50-188">À compter de Windows 10 et de Windows Server 2016, **associer le \_ \_ contexte NAMERES** est également défini.</span><span class="sxs-lookup"><span data-stu-id="05a50-188">Starting with Windows 10 and Windows Server 2016, **ASSOCIATE\_NAMERES\_CONTEXT** is also defined.</span></span>
<span data-ttu-id="05a50-189">Pour plus d’informations, consultez [**addrinfoex4**](/windows/desktop/api/ws2def/ns-ws2def-addrinfoex4) et [**ASSOCIATE_NAMERES_CONTEXT_INPUT**](/windows/desktop/api/mstcpip/ns-mstcpip-associate_nameres_context_input).</span><span class="sxs-lookup"><span data-stu-id="05a50-189">For more information, see [**addrinfoex4**](/windows/desktop/api/ws2def/ns-ws2def-addrinfoex4) and [**ASSOCIATE_NAMERES_CONTEXT_INPUT**](/windows/desktop/api/mstcpip/ns-mstcpip-associate_nameres_context_input).</span></span>

<span data-ttu-id="05a50-190">Si le [**TRANSPORT_SETTING_ID**](/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id) passé dans le paramètre lpvInBuffer a le membre GUID défini sur **la \_ \_ \_ fonctionnalité de notification en temps réel**, il s’agit d’une demande d’application des paramètres de notification en temps réel pour le socket TCP utilisé avec [**ControlChannelTrigger**](/uwp/api/Windows.Networking.Sockets.ControlChannelTrigger) pour recevoir des notifications de réseau en arrière-plan dans une application Windows Store.</span><span class="sxs-lookup"><span data-stu-id="05a50-190">If the [**TRANSPORT_SETTING_ID**](/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id) passed in the lpvInBuffer parameter has the Guid member set to **REAL\_TIME\_NOTIFICATION\_CAPABILITY**, then this is a request to apply real time notification settings for the TCP socket used with the [**ControlChannelTrigger**](/uwp/api/Windows.Networking.Sockets.ControlChannelTrigger) to receive background network notifications in a Windows Store app.</span></span>
<span data-ttu-id="05a50-191">Le paramètre *lpvInBuffer* doit pointer vers une structure **REAL_TIME_NOTIFICATION_SETTING_INPUT** .</span><span class="sxs-lookup"><span data-stu-id="05a50-191">The *lpvInBuffer* parameter should point to a **REAL_TIME_NOTIFICATION_SETTING_INPUT** structure.</span></span>
<span data-ttu-id="05a50-192">Le paramètre *lpvOutBuffer* n’est pas utilisé pour cette opération.</span><span class="sxs-lookup"><span data-stu-id="05a50-192">The *lpvOutBuffer* parameter is unused for this operation.</span></span>
<span data-ttu-id="05a50-193">Ce paramètre de transport s’applique uniquement aux sockets TCP.</span><span class="sxs-lookup"><span data-stu-id="05a50-193">This transport setting applies only to TCP sockets.</span></span>
<span data-ttu-id="05a50-194">Ce paramètre de transport permet à WinInet ou aux services réseau similaires de marquer un socket TCP donné comme [**ControlChannelTrigger**](/uwp/api/Windows.Networking.Sockets.ControlChannelTrigger) activé.</span><span class="sxs-lookup"><span data-stu-id="05a50-194">This transport setting provides a way for WinInet or similar network services to mark a given TCP socket as [**ControlChannelTrigger**](/uwp/api/Windows.Networking.Sockets.ControlChannelTrigger) enabled.</span></span>
<span data-ttu-id="05a50-195">Windows marque le socket TCP correspondant et configure les paramètres matériels et logiciels appropriés lorsque cette option est appelée.</span><span class="sxs-lookup"><span data-stu-id="05a50-195">Windows will mark the corresponding TCP socket and configure appropriate hardware and software settings when this option is called.</span></span>
<span data-ttu-id="05a50-196">Une application du Windows Store n’appellera pas cette IOCTL directement.</span><span class="sxs-lookup"><span data-stu-id="05a50-196">A Windows Store app will not call this IOCTL directly.</span></span>

## <a name="see-also"></a><span data-ttu-id="05a50-197">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="05a50-197">See also</span></span>

[<span data-ttu-id="05a50-198">**ControlChannelTrigger**</span><span class="sxs-lookup"><span data-stu-id="05a50-198">**ControlChannelTrigger**</span></span>](/uwp/api/Windows.Networking.Sockets.ControlChannelTrigger)

[<span data-ttu-id="05a50-199">socle</span><span class="sxs-lookup"><span data-stu-id="05a50-199">socket</span></span>](/windows/desktop/api/winsock2/nf-winsock2-socket)

[<span data-ttu-id="05a50-200">**SIO_QUERY_TRANSPORT_SETTING**</span><span class="sxs-lookup"><span data-stu-id="05a50-200">**SIO_QUERY_TRANSPORT_SETTING**</span></span>](sio-query-transport-setting.md)

[<span data-ttu-id="05a50-201">**TRANSPORT_SETTING_ID**</span><span class="sxs-lookup"><span data-stu-id="05a50-201">**TRANSPORT_SETTING_ID**</span></span>](/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id)

[<span data-ttu-id="05a50-202">**WSAGetLastError**</span><span class="sxs-lookup"><span data-stu-id="05a50-202">**WSAGetLastError**</span></span>](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)

[<span data-ttu-id="05a50-203">**WSAGetOverlappedResult**</span><span class="sxs-lookup"><span data-stu-id="05a50-203">**WSAGetOverlappedResult**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[<span data-ttu-id="05a50-204">**WSAIoctl**</span><span class="sxs-lookup"><span data-stu-id="05a50-204">**WSAIoctl**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[<span data-ttu-id="05a50-205">**WSAOVERLAPPED**</span><span class="sxs-lookup"><span data-stu-id="05a50-205">**WSAOVERLAPPED**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[<span data-ttu-id="05a50-206">**WSASocketA**</span><span class="sxs-lookup"><span data-stu-id="05a50-206">**WSASocketA**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[<span data-ttu-id="05a50-207">**WSASocketW**</span><span class="sxs-lookup"><span data-stu-id="05a50-207">**WSASocketW**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
