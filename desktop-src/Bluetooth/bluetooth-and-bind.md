---
title: Bluetooth et liaison
description: Bluetooth utilise la fonction de liaison pour établir une liaison à un Socket.
ms.assetid: 308d2680-de51-49e6-a0da-7aba494d9572
keywords:
- bind
- Bluetooth
- Bluetooth
- Bluetooth et liaison
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12ccbd088ab61edcfa3dfc511ea591593d0cf781
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842681"
---
# <a name="bluetooth-and-bind"></a><span data-ttu-id="45c05-107">Bluetooth et liaison</span><span class="sxs-lookup"><span data-stu-id="45c05-107">Bluetooth and bind</span></span>

<span data-ttu-id="45c05-108">Bluetooth utilise la fonction de [**liaison**](/windows/desktop/api/winsock/nf-winsock-bind) pour établir une liaison à un Socket.</span><span class="sxs-lookup"><span data-stu-id="45c05-108">Bluetooth uses the [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) function to bind to a socket.</span></span> <span data-ttu-id="45c05-109">Pour lier un Socket Bluetooth, appelez la fonction **Bind** à l’aide de la structure [**\_ BTH sockaddr**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth) .</span><span class="sxs-lookup"><span data-stu-id="45c05-109">To bind a Bluetooth socket, call the **bind** function using the [**SOCKADDR\_BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth) structure.</span></span> <span data-ttu-id="45c05-110">Utilisez la **structure \_ BTH sockaddr** avec les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="45c05-110">Use the **SOCKADDR\_BTH** structure with the following settings:</span></span>

``` syntax
name.addressFamily = AF_BTH;
name.btAddr = 0;
name.serviceClassId = GUID_NULL;
name.port = number of service channel, 0 or BT_PORT_ANY;
```

<span data-ttu-id="45c05-111">Sur les applications clientes, le membre de port doit être égal à zéro pour permettre l’attribution d’un point de terminaison local approprié.</span><span class="sxs-lookup"><span data-stu-id="45c05-111">On client applications, the port member must be zero to enable an appropriate local endpoint to be assigned.</span></span> <span data-ttu-id="45c05-112">Sur les applications serveur, le membre de port doit être un numéro de port ou un port BT valide \_ \_ . les ports attribués automatiquement à l’aide \_ du port BT \_ peuvent être interrogés par la suite avec un appel à la fonction [**GetSockName**](bluetooth-and-getsockname.md) .</span><span class="sxs-lookup"><span data-stu-id="45c05-112">On server applications, the port member must be a valid port number or BT\_PORT\_ANY; ports automatically assigned using BT\_PORT\_ANY may be queried subsequently with a call to the [**getsockname**](bluetooth-and-getsockname.md) function.</span></span> <span data-ttu-id="45c05-113">La plage valide pour la demande d’un port RFCOMM spécifique est comprise entre 1 et 30.</span><span class="sxs-lookup"><span data-stu-id="45c05-113">The valid range for requesting a specific RFCOMM port is 1 through 30.</span></span> <span data-ttu-id="45c05-114">Les canaux de serveur sont des ressources globales, et seulement 30 canaux de serveurs sont disponibles pour la RFCOMM sur n’importe quel périphérique Bluetooth, qui doit être partagé par tous les sockets Windows appartenant à la famille d’adresses Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="45c05-114">Server channels are global resource, and only 30 server channels are available for RFCOMM on any Bluetooth device, which must be shared by all Windows Sockets that belong to the Bluetooth address family.</span></span> <span data-ttu-id="45c05-115">Si aucun canal serveur n’est disponible, ou si le canal serveur spécifié est déjà réservé, l’appel de [**liaison**](/windows/desktop/api/winsock/nf-winsock-bind) échoue.</span><span class="sxs-lookup"><span data-stu-id="45c05-115">If no server channel is available, or if the specified server channel is already reserved, the [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) call fails.</span></span>

<span data-ttu-id="45c05-116">En cas de retour réussi de bind, le canal serveur est réservé jusqu’à la fermeture du Socket.</span><span class="sxs-lookup"><span data-stu-id="45c05-116">Upon successful return from bind, the server channel is reserved until the socket is closed.</span></span> <span data-ttu-id="45c05-117">Utilisez la fonction [**GetSockName**](bluetooth-and-getsockname.md) pour récupérer le numéro de canal pour l’inscription SDP.</span><span class="sxs-lookup"><span data-stu-id="45c05-117">Use the [**getsockname**](bluetooth-and-getsockname.md) function to retrieve the channel number for SDP registration.</span></span>

<span data-ttu-id="45c05-118">Les applications doivent utiliser l’allocation automatique pour le canal serveur.</span><span class="sxs-lookup"><span data-stu-id="45c05-118">Applications should use auto-allocation for the server channel.</span></span>

<span data-ttu-id="45c05-119">La fonction de [**liaison**](/windows/desktop/api/winsock/nf-winsock-bind) ne publie pas automatiquement l’application serveur à l’aide du SDP Bluetooth ; les applications doivent appeler la fonction [**WSASetService**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea) pour être recherchées par les applications Bluetooth distantes.</span><span class="sxs-lookup"><span data-stu-id="45c05-119">The [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) function does not automatically advertise the server application using the Bluetooth SDP; applications must call the [**WSASetService**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea) function to be found by remote Bluetooth applications.</span></span>

## <a name="related-topics"></a><span data-ttu-id="45c05-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="45c05-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="45c05-121">Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="45c05-121">Windows Sockets</span></span>](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[<span data-ttu-id="45c05-122">**établis**</span><span class="sxs-lookup"><span data-stu-id="45c05-122">**bind**</span></span>](/windows/desktop/api/winsock/nf-winsock-bind)
</dt> </dl>

 

 