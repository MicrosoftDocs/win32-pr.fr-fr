---
description: Le code de contrôle permet à un socket de recevoir tous les paquets IPv4 ou IPv6 passant par une interface réseau.
ms.assetid: 1c198a70-6669-4599-bd9a-ffc26c9fe1d0
title: Code de contrôle SIO_RCVALL
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: ddff631f1fa4b6b9f9af74f71e2b1eb38a2bf48e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517267"
---
# <a name="sio_rcvall-control-code"></a><span data-ttu-id="83389-103">Code de contrôle SIO_RCVALL</span><span class="sxs-lookup"><span data-stu-id="83389-103">SIO_RCVALL Control Code</span></span>

## <a name="description"></a><span data-ttu-id="83389-104">Description</span><span class="sxs-lookup"><span data-stu-id="83389-104">Description</span></span>
<span data-ttu-id="83389-105">Le code de contrôle **SIO \_ RCVALL** permet à un socket de recevoir tous les paquets IPv4 ou IPv6 passant par une interface réseau.</span><span class="sxs-lookup"><span data-stu-id="83389-105">The **SIO\_RCVALL** control code enables a socket to receive all IPv4 or IPv6 packets passing through a network interface.</span></span>

<span data-ttu-id="83389-106">Pour effectuer cette opération, appelez la fonction [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** avec les paramètres suivants.</span><span class="sxs-lookup"><span data-stu-id="83389-106">To perform this operation, call the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function with the following parameters.</span></span>

```cpp
int WSAIoctl(
  (socket) s,            // descriptor identifying a socket
  SIO_RCV_ALL,                       // dwIoControlCode
  NULL,                              // lpvInBuffer0,                                 // cbInBuffer
  NULL,                              // lpvOutBuffer output buffer
  (DWORD) cbOutBuffer,            // size of output buffer  
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped, // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

```cpp
int WSAIoctl(
  (socket) s,            // descriptor identifying a socket
  SIO_RCV_ALL,                       // dwIoControlCode
  NULL,                              // lpvInBuffer
  0,                                 // cbInBuffer
  NULL,                              // lpvOutBuffer output buffer
  (DWORD) cbOutBuffer,            // size of output buffer  
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped, // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

## <a name="parameters"></a><span data-ttu-id="83389-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="83389-107">Parameters</span></span>

### <a name="s"></a><span data-ttu-id="83389-108">s</span><span class="sxs-lookup"><span data-stu-id="83389-108">s</span></span>

<span data-ttu-id="83389-109">Descripteur identifiant un Socket.</span><span class="sxs-lookup"><span data-stu-id="83389-109">A descriptor identifying a socket.</span></span>

### <a name="dwiocontrolcode"></a><span data-ttu-id="83389-110">dwIoControlCode</span><span class="sxs-lookup"><span data-stu-id="83389-110">dwIoControlCode</span></span>

<span data-ttu-id="83389-111">Code de contrôle de l’opération.</span><span class="sxs-lookup"><span data-stu-id="83389-111">The control code for the operation.</span></span>
<span data-ttu-id="83389-112">Utilisez **SIO \_ RCVALL** pour cette opération.</span><span class="sxs-lookup"><span data-stu-id="83389-112">Use **SIO\_RCVALL** for this operation.</span></span>

### <a name="lpvinbuffer"></a><span data-ttu-id="83389-113">lpvInBuffer</span><span class="sxs-lookup"><span data-stu-id="83389-113">lpvInBuffer</span></span>

<span data-ttu-id="83389-114">Pointeur vers la mémoire tampon d’entrée qui doit contenir la valeur de l’option.</span><span class="sxs-lookup"><span data-stu-id="83389-114">A pointer to the input buffer that should contain the option value.</span></span>
<span data-ttu-id="83389-115">Les valeurs possibles de l’option **SIO \_ RCVALL** IOCTL sont spécifiées dans l’énumération **RCVALL_VALUE** définie dans le fichier d’en-tête *Mstcpip. h* .</span><span class="sxs-lookup"><span data-stu-id="83389-115">The possible values for the **SIO\_RCVALL** IOCTL option are specified in the **RCVALL_VALUE** enumeration defined in the *Mstcpip.h* header file.</span></span>

<span data-ttu-id="83389-116">Les valeurs possibles pour **SIO \_ RCVALL** sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="83389-116">The possible values for **SIO\_RCVALL** are as follows:</span></span>

| <span data-ttu-id="83389-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="83389-117">Value</span></span> | <span data-ttu-id="83389-118">Signification</span><span class="sxs-lookup"><span data-stu-id="83389-118">Meaning</span></span> |
|-------|---------|
| <span data-ttu-id="83389-119">**RCVALL \_ désactivé**</span><span class="sxs-lookup"><span data-stu-id="83389-119">**RCVALL\_OFF**</span></span> | <span data-ttu-id="83389-120">Désactivez cette option pour qu’un socket ne reçoive pas tous les paquets IPv4 ou IPv6 passant par une interface réseau.</span><span class="sxs-lookup"><span data-stu-id="83389-120">Disable this option so a socket does not receive all IPv4 or IPv6 packets passing through a network interface.</span></span> |
| <span data-ttu-id="83389-121">**RCVALL \_ sur**</span><span class="sxs-lookup"><span data-stu-id="83389-121">**RCVALL\_ON**</span></span> | <span data-ttu-id="83389-122">Activez cette option pour qu’un socket reçoive tous les paquets IPv4 ou IPv6 passant par une interface réseau.</span><span class="sxs-lookup"><span data-stu-id="83389-122">Enable this option so a socket receives all IPv4 or IPv6 packets passing through a network interface.</span></span> <span data-ttu-id="83389-123">Cette option active le mode de proximité sur la carte d’interface réseau (NIC), si la carte réseau prend en charge le mode de proximité.</span><span class="sxs-lookup"><span data-stu-id="83389-123">This option enables promiscuous mode on the network interface card (NIC), if the NIC supports promiscuous mode.</span></span> <span data-ttu-id="83389-124">Sur un segment LAN avec un concentrateur réseau, une carte réseau qui prend en charge le mode promiscuité capture tout le trafic IPv4 ou IPv6 sur le réseau local, y compris le trafic entre les autres ordinateurs sur le même segment de réseau local.</span><span class="sxs-lookup"><span data-stu-id="83389-124">On a LAN segment with a network hub, a NIC that supports promiscuous mode will capture all IPv4 or IPv6 traffic on the LAN, including traffic between other computers on the same LAN segment.</span></span> <span data-ttu-id="83389-125">Tous les paquets capturés (IPv4 ou IPv6, selon le socket) sont remis au socket brut.</span><span class="sxs-lookup"><span data-stu-id="83389-125">All of the captured packets (IPv4 or IPv6, depending on the socket) will be delivered to the raw socket.</span></span> <span data-ttu-id="83389-126">Cette option ne capture pas les autres paquets (paquets ARP, IPX et NetBEUI, par exemple) sur l’interface.</span><span class="sxs-lookup"><span data-stu-id="83389-126">This option will not capture other packets (ARP, IPX, and NetBEUI packets, for example) on the interface.</span></span> <span data-ttu-id="83389-127">Netmon utilise le même mode pour l’interface réseau, mais n’utilise pas cette option pour capturer le trafic.</span><span class="sxs-lookup"><span data-stu-id="83389-127">Netmon uses the same mode for the network interface, but does not use this option to capture traffic.</span></span> |
| <span data-ttu-id="83389-128">**RCVALL \_ SOCKETLEVELONLY**</span><span class="sxs-lookup"><span data-stu-id="83389-128">**RCVALL\_SOCKETLEVELONLY**</span></span> | <span data-ttu-id="83389-129">Cette fonctionnalité n’est pas implémentée pour l’instant. par conséquent, la définition de cette option n’a aucun effet.</span><span class="sxs-lookup"><span data-stu-id="83389-129">This feature is not currently implemented, so setting this option does not have any affect.</span></span> |
| <span data-ttu-id="83389-130">**RCVALL \_ IPLEVEL**</span><span class="sxs-lookup"><span data-stu-id="83389-130">**RCVALL\_IPLEVEL**</span></span> | <span data-ttu-id="83389-131">Activez cette option pour qu’un socket IPv4 ou IPv6 reçoive tous les paquets au niveau IP en passant par une interface réseau.</span><span class="sxs-lookup"><span data-stu-id="83389-131">Enable this option so an IPv4 or IPv6 socket receives all packets at the IP level passing through a network interface.</span></span> <span data-ttu-id="83389-132">Cette option n’active pas le mode de proximité sur la carte d’interface réseau.</span><span class="sxs-lookup"><span data-stu-id="83389-132">This option does not enable promiscuous mode on the network interface card.</span></span> <span data-ttu-id="83389-133">Cette option affecte uniquement le traitement des paquets au niveau de l’adresse IP.</span><span class="sxs-lookup"><span data-stu-id="83389-133">This option only affects packet processing at the IP level.</span></span> <span data-ttu-id="83389-134">La carte réseau reçoit toujours uniquement les paquets dirigés vers ses adresses de monodiffusion et de multidiffusion configurées.</span><span class="sxs-lookup"><span data-stu-id="83389-134">The NIC still receives only packets directed to its configured unicast and multicast addresses.</span></span> <span data-ttu-id="83389-135">Toutefois, un socket avec cette option activée recevra non seulement les paquets dirigés vers des adresses IP spécifiques, mais recevra tous les paquets IPv4 ou IPv6 reçus par la carte réseau.</span><span class="sxs-lookup"><span data-stu-id="83389-135">However, a socket with this option enabled will receive not only packets directed to specific IP addresses, but will receive all the IPv4 or IPv6 packets the NIC receives.</span></span> <span data-ttu-id="83389-136">Cette option ne capture pas les autres paquets (par exemple, les paquets ARP, IPX et NetBEUI) reçus sur l’interface.</span><span class="sxs-lookup"><span data-stu-id="83389-136">This option will not capture other packets (ARP, IPX, and NetBEUI packets, for example) received on the interface.</span></span> |

### <a name="cbinbuffer"></a><span data-ttu-id="83389-137">cbInBuffer</span><span class="sxs-lookup"><span data-stu-id="83389-137">cbInBuffer</span></span>

<span data-ttu-id="83389-138">Taille, en octets, de la mémoire tampon d’entrée.</span><span class="sxs-lookup"><span data-stu-id="83389-138">The size, in bytes, of the input buffer.</span></span>
<span data-ttu-id="83389-139">Ce paramètre doit être supérieur ou égal à la taille du **RCVALL_VALUE** valeur d’énumération vers laquelle pointe le paramètre *lpvInBuffer* .</span><span class="sxs-lookup"><span data-stu-id="83389-139">This parameter should be equal to or greater than the size of the **RCVALL_VALUE** enumeration value pointed to by the *lpvInBuffer* parameter.</span></span>

### <a name="lpvoutbuffer"></a><span data-ttu-id="83389-140">lpvOutBuffer</span><span class="sxs-lookup"><span data-stu-id="83389-140">lpvOutBuffer</span></span>

<span data-ttu-id="83389-141">Pointeur vers la mémoire tampon de sortie.</span><span class="sxs-lookup"><span data-stu-id="83389-141">A pointer to the output buffer.</span></span>
<span data-ttu-id="83389-142">Ce paramètre n’est pas utilisé pour cette opération.</span><span class="sxs-lookup"><span data-stu-id="83389-142">This parameter is unused for this operation.</span></span>

### <a name="cboutbuffer"></a><span data-ttu-id="83389-143">cbOutBuffer</span><span class="sxs-lookup"><span data-stu-id="83389-143">cbOutBuffer</span></span>

<span data-ttu-id="83389-144">Taille, en octets, de la mémoire tampon de sortie.</span><span class="sxs-lookup"><span data-stu-id="83389-144">The size, in bytes, of the output buffer.</span></span>
<span data-ttu-id="83389-145">Ce paramètre n’est pas utilisé pour cette opération.</span><span class="sxs-lookup"><span data-stu-id="83389-145">This parameter is unused for this operation.</span></span>

### <a name="lpcbbytesreturned"></a><span data-ttu-id="83389-146">lpcbBytesReturned</span><span class="sxs-lookup"><span data-stu-id="83389-146">lpcbBytesReturned</span></span>

<span data-ttu-id="83389-147">Pointeur vers une variable qui reçoit la taille, en octets, des données stockées dans la mémoire tampon de sortie.</span><span class="sxs-lookup"><span data-stu-id="83389-147">A pointer to a variable that receives the size, in bytes, of the data stored in the output buffer.</span></span>
<span data-ttu-id="83389-148">Ce paramètre n’est pas utilisé pour cette opération.</span><span class="sxs-lookup"><span data-stu-id="83389-148">This parameter is unused for this operation.</span></span>

### <a name="lpvoverlapped"></a><span data-ttu-id="83389-149">lpvOverlapped</span><span class="sxs-lookup"><span data-stu-id="83389-149">lpvOverlapped</span></span>

<span data-ttu-id="83389-150">Pointeur vers une structure [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) .</span><span class="sxs-lookup"><span data-stu-id="83389-150">A pointer to a [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="83389-151">Si le socket *s* a été créé sans l’attribut Overlapped, le paramètre *lpOverlapped* est ignoré.</span><span class="sxs-lookup"><span data-stu-id="83389-151">If socket *s* was created without the overlapped attribute, the *lpOverlapped* parameter is ignored.</span></span>

<span data-ttu-id="83389-152">Si *s* a été ouvert avec l’attribut Overlapped et que le paramètre *lpOverlapped* n’a pas la **valeur null**, l’opération est exécutée en tant qu’opération Overlapped (asynchrone).</span><span class="sxs-lookup"><span data-stu-id="83389-152">If *s* was opened with the overlapped attribute and the *lpOverlapped* parameter is not **NULL**, the operation is performed as an overlapped (asynchronous) operation.</span></span>
<span data-ttu-id="83389-153">Dans ce cas, le paramètre *lpOverlapped* doit pointer vers une structure [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) valide.</span><span class="sxs-lookup"><span data-stu-id="83389-153">In this case, *lpOverlapped* parameter must point to a valid [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="83389-154">Pour les opérations avec chevauchement, la fonction [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** retourne immédiatement, et la méthode d’achèvement appropriée est signalée lorsque l’opération est terminée.</span><span class="sxs-lookup"><span data-stu-id="83389-154">For overlapped operations, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns immediately, and the appropriate completion method is signaled when the operation has been completed.</span></span>
<span data-ttu-id="83389-155">Sinon, la fonction ne retourne pas jusqu’à ce que l’opération soit terminée ou qu’une erreur se produise.</span><span class="sxs-lookup"><span data-stu-id="83389-155">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

### <a name="lpcompletionroutine"></a><span data-ttu-id="83389-156">lpCompletionRoutine</span><span class="sxs-lookup"><span data-stu-id="83389-156">lpCompletionRoutine</span></span>

<span data-ttu-id="83389-157">Type : \_ In_opt \_ [ **LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span><span class="sxs-lookup"><span data-stu-id="83389-157">Type: \_In_opt\_ [**LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span></span>

<span data-ttu-id="83389-158">Pointeur vers la routine de saisie semi-automatique appelée lorsque l’opération est terminée (ignoré pour les sockets non superposés).</span><span class="sxs-lookup"><span data-stu-id="83389-158">A pointer to the completion routine called when the operation has been completed (ignored for non-overlapped sockets).</span></span>

### <a name="lpthreadid"></a><span data-ttu-id="83389-159">lpThreadId</span><span class="sxs-lookup"><span data-stu-id="83389-159">lpThreadId</span></span>

<span data-ttu-id="83389-160">Pointeur vers une structure [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) qui doit être utilisée par le fournisseur dans un appel ultérieur à [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc).</span><span class="sxs-lookup"><span data-stu-id="83389-160">A pointer to a [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure to be used by the provider in a subsequent call to [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc).</span></span>
<span data-ttu-id="83389-161">Le fournisseur doit stocker la structure [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) référencée (pas le pointeur vers le même) jusqu’à ce que la fonction [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) soit retournée.</span><span class="sxs-lookup"><span data-stu-id="83389-161">The provider should store the referenced [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure (not the pointer to same) until after the [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) function returns.</span></span>

<span data-ttu-id="83389-162">**Remarque**  Ce paramètre s’applique uniquement à la fonction **WSPIoctl** .</span><span class="sxs-lookup"><span data-stu-id="83389-162">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

### <a name="lperrno"></a><span data-ttu-id="83389-163">lpErrno</span><span class="sxs-lookup"><span data-stu-id="83389-163">lpErrno</span></span>

<span data-ttu-id="83389-164">Pointeur vers le code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="83389-164">A pointer to the error code.</span></span>

<span data-ttu-id="83389-165">**Remarque**  Ce paramètre s’applique uniquement à la fonction **WSPIoctl** .</span><span class="sxs-lookup"><span data-stu-id="83389-165">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

## <a name="return-value"></a><span data-ttu-id="83389-166">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="83389-166">Return value</span></span>

<span data-ttu-id="83389-167">Si l’opération se termine correctement, la fonction [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** retourne la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="83389-167">If the operation completes successfully, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns zero.</span></span>

<span data-ttu-id="83389-168">Si l’opération échoue ou est en attente, la fonction [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** retourne une **\_ erreur de socket**.</span><span class="sxs-lookup"><span data-stu-id="83389-168">If the operation fails or is pending, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns **SOCKET\_ERROR**.</span></span>
<span data-ttu-id="83389-169">Pour afficher les informations d’erreur étendues, appelez [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span><span class="sxs-lookup"><span data-stu-id="83389-169">To get extended error information, call [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>

| <span data-ttu-id="83389-170">Code d'erreur</span><span class="sxs-lookup"><span data-stu-id="83389-170">Error code</span></span> | <span data-ttu-id="83389-171">Signification</span><span class="sxs-lookup"><span data-stu-id="83389-171">Meaning</span></span> |
|------------|---------|
| <span data-ttu-id="83389-172">**\_e/s WSA \_ en attente**</span><span class="sxs-lookup"><span data-stu-id="83389-172">**WSA\_IO\_PENDING**</span></span> | <span data-ttu-id="83389-173">Une opération avec chevauchement a été correctement initiée et l’achèvement sera indiqué ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="83389-173">An overlapped operation was successfully initiated and completion will be indicated at a later time.</span></span> |
| <span data-ttu-id="83389-174">**\_opération WSA \_ abandonnée**</span><span class="sxs-lookup"><span data-stu-id="83389-174">**WSA\_OPERATION\_ABORTED**</span></span> | <span data-ttu-id="83389-175">Une opération avec chevauchement a été annulée en raison de la fermeture du socket ou de l’exécution de la commande **SIO_FLUSH** ioctl.</span><span class="sxs-lookup"><span data-stu-id="83389-175">An overlapped operation was canceled due to the closure of the socket or the execution of the **SIO_FLUSH** IOCTL command.</span></span> |
| <span data-ttu-id="83389-176">**WSAEFAULT**</span><span class="sxs-lookup"><span data-stu-id="83389-176">**WSAEFAULT**</span></span> | <span data-ttu-id="83389-177">Le paramètre *lpOverlapped* ou *lpCompletionRoutine* n’est pas entièrement contenu dans une partie valide de l’espace d’adressage de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="83389-177">The *lpOverlapped* or *lpCompletionRoutine* parameter is not totally contained in a valid part of the user address space.</span></span> |
| <span data-ttu-id="83389-178">**WSAEINPROGRESS**</span><span class="sxs-lookup"><span data-stu-id="83389-178">**WSAEINPROGRESS**</span></span> | <span data-ttu-id="83389-179">La fonction est appelée lorsqu’un rappel est en cours.</span><span class="sxs-lookup"><span data-stu-id="83389-179">The function is invoked when a callback is in progress.</span></span> |
| <span data-ttu-id="83389-180">**WSAEINTR**</span><span class="sxs-lookup"><span data-stu-id="83389-180">**WSAEINTR**</span></span> | <span data-ttu-id="83389-181">Une opération de blocage a été interrompue.</span><span class="sxs-lookup"><span data-stu-id="83389-181">A blocking operation was interrupted.</span></span> |
| <span data-ttu-id="83389-182">**WSAEINVAL**</span><span class="sxs-lookup"><span data-stu-id="83389-182">**WSAEINVAL**</span></span> | <span data-ttu-id="83389-183">Le paramètre *dwIoControlCode* n’est pas une commande valide, ou un paramètre d’entrée spécifié n’est pas acceptable, ou la commande n’est pas applicable au type de socket spécifié.</span><span class="sxs-lookup"><span data-stu-id="83389-183">The *dwIoControlCode* parameter is not a valid command, or a specified input parameter is not acceptable, or the command is not applicable to the type of socket specified.</span></span> <span data-ttu-id="83389-184">Cette erreur est également retournée si le paramètre *cbInBuffer* est inférieur à `sizeof(UCHAR)` ou si le paramètre *lpvInBuffer* pointe vers une valeur qui n’est pas une **RCVALL_VALUE** valeur d’énumération.</span><span class="sxs-lookup"><span data-stu-id="83389-184">This error is also returned if the *cbInBuffer* parameter is less than the `sizeof(UCHAR)` or the *lpvInBuffer* parameter points to value that is not a **RCVALL_VALUE** enumeration value.</span></span> <span data-ttu-id="83389-185">Cette erreur peut également être renvoyée si l’interface réseau associée au socket est introuvable.</span><span class="sxs-lookup"><span data-stu-id="83389-185">This error can also be returned if the network interface associated with the socket cannot be found.</span></span> <span data-ttu-id="83389-186">Cela peut se produire si l’interface réseau associée au socket est supprimée ou supprimée (par exemple, un périphérique réseau PCMCIA ou USB).</span><span class="sxs-lookup"><span data-stu-id="83389-186">This could occur if the network interface associated with the socket is deleted or removed (a remove PCMCIA or USB network device, for example).</span></span> |
| <span data-ttu-id="83389-187">**WSAENETDOWN**</span><span class="sxs-lookup"><span data-stu-id="83389-187">**WSAENETDOWN**</span></span> | <span data-ttu-id="83389-188">Le sous-système réseau a échoué.</span><span class="sxs-lookup"><span data-stu-id="83389-188">The network subsystem has failed.</span></span> |
| <span data-ttu-id="83389-189">**WSAENOBUFS**</span><span class="sxs-lookup"><span data-stu-id="83389-189">**WSAENOBUFS**</span></span> | <span data-ttu-id="83389-190">Aucun espace de mémoire tampon n’est disponible.</span><span class="sxs-lookup"><span data-stu-id="83389-190">No buffer space available.</span></span> |
| <span data-ttu-id="83389-191">**WSAENOPROTOOPT**</span><span class="sxs-lookup"><span data-stu-id="83389-191">**WSAENOPROTOOPT**</span></span> | <span data-ttu-id="83389-192">L’option de socket n’est pas prise en charge sur le protocole spécifié.</span><span class="sxs-lookup"><span data-stu-id="83389-192">The socket option is not supported on the specified protocol.</span></span> |
| <span data-ttu-id="83389-193">**WSAENOTSOCK**</span><span class="sxs-lookup"><span data-stu-id="83389-193">**WSAENOTSOCK**</span></span> | <span data-ttu-id="83389-194">Le descripteur *s* n’est pas un Socket.</span><span class="sxs-lookup"><span data-stu-id="83389-194">The descriptor *s* is not a socket.</span></span> |
| <span data-ttu-id="83389-195">**WSAEOPNOTSUPP**</span><span class="sxs-lookup"><span data-stu-id="83389-195">**WSAEOPNOTSUPP**</span></span> | <span data-ttu-id="83389-196">La commande IOCTL spécifiée n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="83389-196">The specified IOCTL command is not supported.</span></span> <span data-ttu-id="83389-197">Cette erreur est retournée si l’IOCTL **SIO \_ RCVALL** n’est pas prise en charge par le fournisseur de transport.</span><span class="sxs-lookup"><span data-stu-id="83389-197">This error is returned if the **SIO\_RCVALL** IOCTL is not supported by the transport provider.</span></span> |

## <a name="remarks"></a><span data-ttu-id="83389-198">Notes</span><span class="sxs-lookup"><span data-stu-id="83389-198">Remarks</span></span>

<span data-ttu-id="83389-199">L’IOCTL **SIO \_ RCVALL** est prise en charge sur Windows 2000 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="83389-199">The **SIO\_RCVALL** IOCTL is supported on Windows 2000 and later versions of the operating system.</span></span>

<span data-ttu-id="83389-200">L’IOCTL **SIO \_ RCVALL** permet à un socket de recevoir tous les paquets IPv4 ou IPv6 sur une interface réseau.</span><span class="sxs-lookup"><span data-stu-id="83389-200">The **SIO\_RCVALL** IOCTL enables a socket to receive all IPv4 or IPv6 packets on a network interface.</span></span>
<span data-ttu-id="83389-201">Le descripteur de socket passé à la fonction [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** doit être l’un des suivants :</span><span class="sxs-lookup"><span data-stu-id="83389-201">The socket handle passed to the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function must be one of the following:</span></span>

* <span data-ttu-id="83389-202">Un socket IPv4 qui a été créé avec la famille d’adresses définie sur AF_INET, le type de socket défini sur SOCK_RAW et le protocole défini sur IPPROTO_IP.</span><span class="sxs-lookup"><span data-stu-id="83389-202">An IPv4 socket that was created with the address family set to AF_INET, the socket type set to SOCK_RAW, and the protocol set to IPPROTO_IP.</span></span>
* <span data-ttu-id="83389-203">Un socket IPv6 qui a été créé avec la famille d’adresses définie sur AF_INET6, le type de socket défini sur SOCK_RAW et le protocole défini sur IPPROTO_IPV6.</span><span class="sxs-lookup"><span data-stu-id="83389-203">An IPv6 socket that was created with the address family set to AF_INET6, the socket type set to SOCK_RAW, and the protocol set to IPPROTO_IPV6.</span></span>

<span data-ttu-id="83389-204">Pour plus d’informations sur les sockets bruts, consultez [**sockets bruts TCP/IP**](/windows/desktop/winsock/tcp-ip-raw-sockets-2).</span><span class="sxs-lookup"><span data-stu-id="83389-204">For more information on raw sockets, see [**TCP/IP Raw Sockets**](/windows/desktop/winsock/tcp-ip-raw-sockets-2).</span></span>

<span data-ttu-id="83389-205">Le socket doit également être lié à une interface IPv4 ou IPv6 locale explicite, ce qui signifie que vous ne pouvez pas effectuer de liaison pour **inadr \_ any** ou **in6addr \_ any**.</span><span class="sxs-lookup"><span data-stu-id="83389-205">The socket also must be bound to an explicit local IPv4 or IPv6 interface, which means that you cannot bind to **INADDR\_ANY** or **in6addr\_any**.</span></span>

<span data-ttu-id="83389-206">Une fois que le socket est lié et que l’IOCTL s’est terminée avec succès, les appels aux fonctions [**WSARecv**](/windows/desktop/api/winsock2/nf-winsock2-wsarecv) ou [**recv**](/windows/desktop/api/winsock/nf-winsock-recv) renvoient des datagrammes IPv4 passant par l’interface IPv4 donnée ou retournent des datagrammes IPv6 passant par l’interface IPv6 donnée.</span><span class="sxs-lookup"><span data-stu-id="83389-206">Once the socket is bound and the IOCTL completes successfully, calls to the [**WSARecv**](/windows/desktop/api/winsock2/nf-winsock2-wsarecv) or [**recv**](/windows/desktop/api/winsock/nf-winsock-recv) functions return IPv4 datagrams passing through the given IPv4 interface or return IPv6 datagrams passing through the given IPv6 interface.</span></span>
<span data-ttu-id="83389-207">Notez que vous devez fournir une mémoire tampon suffisamment grande.</span><span class="sxs-lookup"><span data-stu-id="83389-207">Note that you must supply a sufficiently large buffer.</span></span>
<span data-ttu-id="83389-208">La définition de cette IOCTL ne capture que les paquets IPv4 ou IPv6 sur une interface donnée.</span><span class="sxs-lookup"><span data-stu-id="83389-208">Setting this IOCTL will only capture IPv4 or IPv6 packets on a given interface.</span></span>
<span data-ttu-id="83389-209">Cette IOCTL ne capture pas d’autres paquets (paquets ARP, IPX et NetBEUI, par exemple) sur l’interface.</span><span class="sxs-lookup"><span data-stu-id="83389-209">This IOCTL will not capture other packets (ARP, IPX, and NetBEUI packets, for example) on the interface.</span></span>

<span data-ttu-id="83389-210">Un socket lié à une interface locale spécifique avec l’IOCTL **SIO \_ RCVALL** recevra uniquement les paquets passant par cette interface.</span><span class="sxs-lookup"><span data-stu-id="83389-210">A socket bound to a specific local interface with the **SIO\_RCVALL** IOCTL will receive only packets passing through that interface.</span></span>
<span data-ttu-id="83389-211">Elle ne reçoit pas de paquets reçus sur une autre interface et est transférée vers une autre interface différente du socket lié à **SIO \_ RCVALL** ioctl.</span><span class="sxs-lookup"><span data-stu-id="83389-211">It will not receive packets received on another interface and getting forwarded out on another interface different from the socket bound with **SIO\_RCVALL** IOCTL.</span></span>

<span data-ttu-id="83389-212">Sur Windows Server 2008 et versions antérieures, le paramètre IOCTL **SIO \_ RCVALL** ne capture pas les paquets locaux envoyés à partir d’une interface réseau.</span><span class="sxs-lookup"><span data-stu-id="83389-212">On Windows Server 2008 and earlier, the **SIO\_RCVALL** IOCTL setting would not capture local packets sent out of a network interface.</span></span>
<span data-ttu-id="83389-213">Cela inclut les paquets reçus sur une autre interface et a transmis l’interface réseau spécifiée pour l’IOCTL **SIO \_ RCVALL** .</span><span class="sxs-lookup"><span data-stu-id="83389-213">This included packets received on another interface and forwarded out the network interface specified for the **SIO\_RCVALL** IOCTL.</span></span>

<span data-ttu-id="83389-214">Sur Windows 7 et Windows Server 2008 R2, cela a été modifié afin que les paquets locaux envoyés à partir d’une interface réseau soient également capturés.</span><span class="sxs-lookup"><span data-stu-id="83389-214">On Windows 7 and Windows Server 2008 R2 , this was changed so that local packets sent out of a network interface are also captured.</span></span>
<span data-ttu-id="83389-215">Cela comprend les paquets reçus sur une autre interface, puis le transfert de l’interface réseau liée au socket avec **SIO \_ RCVALL** ioctl.</span><span class="sxs-lookup"><span data-stu-id="83389-215">This includes packets received on another interface and then forwarded out the network interface bound to the socket with **SIO\_RCVALL** IOCTL.</span></span>

<span data-ttu-id="83389-216">La définition de cette IOCTL requiert des privilèges d’administrateur sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="83389-216">Setting this IOCTL requires Administrator privilege on the local computer.</span></span>

<span data-ttu-id="83389-217">Cette fonctionnalité est parfois appelée « mode promiscuité ».</span><span class="sxs-lookup"><span data-stu-id="83389-217">This feature is sometimes referred to as promiscuous mode.</span></span>
<span data-ttu-id="83389-218">Toute modification directe de l’application de cette option sur une interface, puis vers une autre interface avec un appel unique à l’aide de cette IOCTL n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="83389-218">Any direct change from applying this option on one interface and then to another interface with a single call using this IOCTL is not supported.</span></span>
<span data-ttu-id="83389-219">Une application doit tout d’abord utiliser cette IOCTL pour désactiver le comportement sur la première interface, puis utiliser cette IOCTL pour activer le comportement sur une nouvelle interface.</span><span class="sxs-lookup"><span data-stu-id="83389-219">An application must first use this IOCTL to turn off the behavior on the first interface, and then use this IOCTL to enable the behavior on a new interface.</span></span>

## <a name="see-also"></a><span data-ttu-id="83389-220">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="83389-220">See also</span></span>

[<span data-ttu-id="83389-221">**socle**</span><span class="sxs-lookup"><span data-stu-id="83389-221">**socket**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-socket)

[<span data-ttu-id="83389-222">**Sockets bruts TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="83389-222">**TCP/IP Raw Sockets**</span></span>](/windows/desktop/winsock/tcp-ip-raw-sockets-2)

[<span data-ttu-id="83389-223">**WSAGetLastError**</span><span class="sxs-lookup"><span data-stu-id="83389-223">**WSAGetLastError**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetlasterror)

[<span data-ttu-id="83389-224">**WSAGetOverlappedResult**</span><span class="sxs-lookup"><span data-stu-id="83389-224">**WSAGetOverlappedResult**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[<span data-ttu-id="83389-225">**WSAIoctl**</span><span class="sxs-lookup"><span data-stu-id="83389-225">**WSAIoctl**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[<span data-ttu-id="83389-226">**WSAOVERLAPPED**</span><span class="sxs-lookup"><span data-stu-id="83389-226">**WSAOVERLAPPED**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[<span data-ttu-id="83389-227">**WSASocketA**</span><span class="sxs-lookup"><span data-stu-id="83389-227">**WSASocketA**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[<span data-ttu-id="83389-228">**WSASocketW**</span><span class="sxs-lookup"><span data-stu-id="83389-228">**WSASocketW**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
