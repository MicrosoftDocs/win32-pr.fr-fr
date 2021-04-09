---
description: Dans deux cas, il était nécessaire de renommer les fonctions utilisées dans les sockets Berkeley afin d’éviter les conflits avec d’autres fonctions de l’API Microsoft Windows.
ms.assetid: b53b1622-cba4-47e3-a371-b3186de6d61b
title: Fonctions renommées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a8fd2af33bdeb74dd7a4c83fe535bae2a020530
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863814"
---
# <a name="renamed-functions"></a><span data-ttu-id="f6a40-103">Fonctions renommées</span><span class="sxs-lookup"><span data-stu-id="f6a40-103">Renamed Functions</span></span>

<span data-ttu-id="f6a40-104">Dans deux cas, il était nécessaire de renommer les fonctions utilisées dans les sockets Berkeley afin d’éviter les conflits avec d’autres fonctions de l’API Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="f6a40-104">In two cases it was necessary to rename functions that are used in Berkeley Sockets in order to avoid clashes with other Microsoft Windows API functions.</span></span>

## <a name="close-and-closesocket"></a><span data-ttu-id="f6a40-105">Fermer et opération closesocket</span><span class="sxs-lookup"><span data-stu-id="f6a40-105">Close and Closesocket</span></span>

<span data-ttu-id="f6a40-106">Les sockets sont représentés par des descripteurs de fichiers standard dans les sockets Berkeley. la fonction **Close** peut donc être utilisée pour fermer des sockets et des fichiers normaux.</span><span class="sxs-lookup"><span data-stu-id="f6a40-106">Sockets are represented by standard file descriptors in Berkeley Sockets, so the **close** function can be used to close sockets as well as regular files.</span></span> <span data-ttu-id="f6a40-107">Bien que rien dans Windows Sockets ne permette à une implémentation d’utiliser des handles de fichiers normaux pour identifier des sockets, rien ne l’exige.</span><span class="sxs-lookup"><span data-stu-id="f6a40-107">While nothing in Windows Sockets prevents an implementation from using regular file handles to identify sockets, nothing requires it either.</span></span> <span data-ttu-id="f6a40-108">Sur Windows, les sockets doivent être fermés à l’aide de la routine [**opération closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) .</span><span class="sxs-lookup"><span data-stu-id="f6a40-108">On Windows, sockets must be closed by using the [**closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) routine.</span></span> <span data-ttu-id="f6a40-109">SUR Windows, l’utilisation de la fonction **Close** pour fermer un socket est incorrecte et les effets de cette action ne sont pas définis par cette spécification.</span><span class="sxs-lookup"><span data-stu-id="f6a40-109">ON Windows, using the **close** function to close a socket is incorrect and the effects of doing so are undefined by this specification.</span></span>

## <a name="ioctl-and-ioctlsocketwsaioctl"></a><span data-ttu-id="f6a40-110">IOCTL et ioctlsocket/WSAIoctl</span><span class="sxs-lookup"><span data-stu-id="f6a40-110">Ioctl and Ioctlsocket/WSAIoctl</span></span>

<span data-ttu-id="f6a40-111">Différents systèmes Runtime en langage C utilisent les IOCTL à des fins non liées à Windows Sockets.</span><span class="sxs-lookup"><span data-stu-id="f6a40-111">Various C language run-time systems use the IOCTLs for purposes unrelated to Windows Sockets.</span></span> <span data-ttu-id="f6a40-112">Par conséquent, la fonction [**ioctlsocket**](/windows/desktop/api/winsock/nf-winsock-ioctlsocket) et la fonction [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) ont été définies pour gérer les fonctions de socket qui ont été effectuées par **IOCTL** et **fcntl** dans la distribution de logiciels Berkeley.</span><span class="sxs-lookup"><span data-stu-id="f6a40-112">As a consequence, the [**ioctlsocket**](/windows/desktop/api/winsock/nf-winsock-ioctlsocket) function and the [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) function were defined to handle socket functions that were performed by **IOCTL** and **fcntl** in the Berkeley Software Distribution.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f6a40-113">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f6a40-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f6a40-114">**opération closesocket**</span><span class="sxs-lookup"><span data-stu-id="f6a40-114">**closesocket**</span></span>](/windows/desktop/api/winsock/nf-winsock-closesocket)
</dt> <dt>

[<span data-ttu-id="f6a40-115">**ioctlsocket**</span><span class="sxs-lookup"><span data-stu-id="f6a40-115">**ioctlsocket**</span></span>](/windows/desktop/api/winsock/nf-winsock-ioctlsocket)
</dt> <dt>

[<span data-ttu-id="f6a40-116">Portage d’applications de socket vers Winsock</span><span class="sxs-lookup"><span data-stu-id="f6a40-116">Porting Socket Applications to Winsock</span></span>](porting-socket-applications-to-winsock.md)
</dt> <dt>

[<span data-ttu-id="f6a40-117">Considérations sur la programmation Winsock</span><span class="sxs-lookup"><span data-stu-id="f6a40-117">Winsock Programming Considerations</span></span>](winsock-programming-considerations.md)
</dt> <dt>

[<span data-ttu-id="f6a40-118">**WSAIoctl**</span><span class="sxs-lookup"><span data-stu-id="f6a40-118">**WSAIoctl**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl)
</dt> </dl>

 

 



