---
title: Bluetooth et accepter
description: Bluetooth utilise la fonction Accept pour activer les tentatives de connexion entrante sur un Socket.
ms.assetid: 79708118-2f70-4759-b5d6-cf5cfc33c27e
keywords:
- accepter
- Bluetooth
- Bluetooth
- Bluetooth et accepter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28dff84ec05429411614e64a08ab159a5ee134b6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106509875"
---
# <a name="bluetooth-and-accept"></a><span data-ttu-id="42910-107">Bluetooth et accepter</span><span class="sxs-lookup"><span data-stu-id="42910-107">Bluetooth and accept</span></span>

<span data-ttu-id="42910-108">Bluetooth utilise la fonction [**Accept**](/windows/desktop/api/winsock2/nf-winsock2-accept) pour activer les tentatives de connexion entrante sur un Socket.</span><span class="sxs-lookup"><span data-stu-id="42910-108">Bluetooth uses the [**accept**](/windows/desktop/api/winsock2/nf-winsock2-accept) function to enable incoming connection attempts on a socket.</span></span> <span data-ttu-id="42910-109">L' \_ adresse BTH de l’application cliente est obtenue en lisant la section spécifique au transport Bluetooth de la structure [**sockaddr**](/windows/desktop/WinSock/sockaddr-2) retournée.</span><span class="sxs-lookup"><span data-stu-id="42910-109">The BTH\_ADDR of the client application is obtained by reading the Bluetooth transport-specific section of the returned [**sockaddr**](/windows/desktop/WinSock/sockaddr-2) structure.</span></span> <span data-ttu-id="42910-110">L’utilisation de la fonction **Accept** avec Bluetooth a le format suivant :</span><span class="sxs-lookup"><span data-stu-id="42910-110">Use of the **accept** function with Bluetooth has the following format:</span></span>

-   <span data-ttu-id="42910-111">Le paramètre *addr* de la fonction [**Accept**](/windows/desktop/api/winsock2/nf-winsock2-accept) est un pointeur facultatif vers une mémoire tampon qui reçoit l’adresse de l’entité qui se connecte, telle qu’elle est connue de la couche de communication.</span><span class="sxs-lookup"><span data-stu-id="42910-111">The *addr* parameter of the [**accept**](/windows/desktop/api/winsock2/nf-winsock2-accept) function is an optional pointer to a buffer that receives the address of the connecting entity, as known to the communications layer.</span></span> <span data-ttu-id="42910-112">Un pointeur vers une [**structure \_ BTH sockaddr**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth) avec l’adresse de l’appareil Bluetooth distant est retourné.</span><span class="sxs-lookup"><span data-stu-id="42910-112">A pointer to a [**SOCKADDR\_BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth) structure with the remote Bluetooth device address is returned.</span></span>
-   <span data-ttu-id="42910-113">Le paramètre *addrlen* de la fonction [**Accept**](/windows/desktop/api/winsock2/nf-winsock2-accept) est un pointeur facultatif vers un entier qui contient la longueur, en octets, de addr. L’entier doit être supérieur ou égal à la valeur de **sizeof** ([**sockaddr \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth)).</span><span class="sxs-lookup"><span data-stu-id="42910-113">The *addrlen* parameter of the [**accept**](/windows/desktop/api/winsock2/nf-winsock2-accept) function is an optional pointer to an integer that contains the length, in bytes, of addr. The integer must be greater or equal to the value of **sizeof** ([**SOCKADDR\_BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="42910-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="42910-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="42910-115">Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="42910-115">Windows Sockets</span></span>](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[<span data-ttu-id="42910-116">**accepter**</span><span class="sxs-lookup"><span data-stu-id="42910-116">**accept**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-accept)
</dt> </dl>

 

 