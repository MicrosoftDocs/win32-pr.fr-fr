---
description: Veillez à prendre en compte toutes les différences entre l’ordonnancement d’octets utilisé pour stocker des entiers par l’architecture de l’hôte et l’ordre des octets utilisé sur le câble par les protocoles de transport individuels.
ms.assetid: 54c84cdb-50a1-4f5e-a18f-0477d90c74d2
title: Classement des octets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47af5ea9d22c01e6ae1ad3d78af48b4216f71ecc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484953"
---
# <a name="byte-ordering"></a><span data-ttu-id="3d5cb-103">Classement des octets</span><span class="sxs-lookup"><span data-stu-id="3d5cb-103">Byte Ordering</span></span>

<span data-ttu-id="3d5cb-104">Veillez à prendre en compte toutes les différences entre l’ordonnancement d’octets utilisé pour stocker des entiers par l’architecture de l’hôte et l’ordre des octets utilisé sur le câble par les protocoles de transport individuels.</span><span class="sxs-lookup"><span data-stu-id="3d5cb-104">Care must always be taken to account for any differences between the byte ordering used for storing integers by the host architecture and the byte ordering used on the wire by individual transport protocols.</span></span> <span data-ttu-id="3d5cb-105">Toute référence à une adresse ou à un numéro de port transmis à ou à partir d’une routine Windows Sockets doit se trouver dans l’ordre de réseau (Big-endian) pour le protocole utilisé.</span><span class="sxs-lookup"><span data-stu-id="3d5cb-105">Any reference to an address or port number passed to or from a Windows Sockets routine must be in the network order (big-endian) for the protocol being utilized.</span></span> <span data-ttu-id="3d5cb-106">Dans le cas d’IP, cela comprend l’adresse IP et les paramètres de port d’une structure [**sockaddr**](sockaddr-2.md) (mais pas le paramètre de *\_ famille Sin* ).</span><span class="sxs-lookup"><span data-stu-id="3d5cb-106">In the case of IP, this includes the IP address and port parameters of a [**sockaddr**](sockaddr-2.md) structure (but not the *sin\_family* parameter).</span></span>

<span data-ttu-id="3d5cb-107">Un certain nombre de systèmes UNIX fonctionnent sur des unités centrales qui représentent des entiers dans l’ordre d’octet (Big-endian) réseau.</span><span class="sxs-lookup"><span data-stu-id="3d5cb-107">A number of the UNIX systems operate on CPUs that represent integers in network byte order (big-endian).</span></span> <span data-ttu-id="3d5cb-108">Par conséquent, la nécessité de convertir des entiers de l’ordre d’octet de l’hôte en ordre d’octet réseau peut être ignorée sans causer de problèmes, même si cela n’est pas recommandé pour la portabilité.</span><span class="sxs-lookup"><span data-stu-id="3d5cb-108">So the need to convert integers from host byte order to network byte order can be ignored without causing problems even if this is not recommended for portability.</span></span>

<span data-ttu-id="3d5cb-109">En revanche, l’ordre des octets utilisé pour représenter les entiers par la plupart des processeurs® Intel est Little-endian.</span><span class="sxs-lookup"><span data-stu-id="3d5cb-109">In contrast, the byte ordering used to represent integers by most Intel® CPUs is little-endian.</span></span> <span data-ttu-id="3d5cb-110">Il devient donc obligatoire que les entiers soient convertis de l’ordre d’octet de l’hôte en ordre d’octet réseau, avant d’être utilisés dans les structures et les fonctions Winsock Sockets.</span><span class="sxs-lookup"><span data-stu-id="3d5cb-110">So it is becomes mandatory that integers be converted from host byte-order to network byte order before being used in Winsock Sockets functions and structures.</span></span>

<span data-ttu-id="3d5cb-111">Prenons l’exemple d’une application qui contacte normalement un serveur sur le port TCP correspondant au service de temps, mais qui fournit un mécanisme permettant à l’utilisateur de spécifier un autre port.</span><span class="sxs-lookup"><span data-stu-id="3d5cb-111">Consider an application that normally contacts a server on the TCP port corresponding to the time service, but provides a mechanism for the user to specify an alternative port.</span></span> <span data-ttu-id="3d5cb-112">Le numéro de port renvoyé par [**getservbyname**](/windows/desktop/api/winsock/nf-winsock-getservbyname) est déjà dans l’ordre du réseau, qui est le format requis pour construire une adresse afin qu’aucune traduction ne soit requise.</span><span class="sxs-lookup"><span data-stu-id="3d5cb-112">The port number returned by [**getservbyname**](/windows/desktop/api/winsock/nf-winsock-getservbyname) is already in network order, which is the format required for constructing an address so that no translation is required.</span></span> <span data-ttu-id="3d5cb-113">Toutefois, si l’utilisateur choisit d’utiliser un autre port, entré sous la forme d’un entier, l’application doit la convertir de l’hôte en ordre de réseau TCP/IP (à l’aide de la fonction [**htons**](/windows/desktop/api/winsock/nf-winsock-htons) ou [**WSAHtons**](/windows/desktop/api/Winsock2/nf-winsock2-wsahtons) ) avant de l’utiliser pour construire une adresse.</span><span class="sxs-lookup"><span data-stu-id="3d5cb-113">However, if the user elects to use a different port, entered as an integer, the application must convert this from host to TCP/IP network order (using the [**htons**](/windows/desktop/api/winsock/nf-winsock-htons) or [**WSAHtons**](/windows/desktop/api/Winsock2/nf-winsock2-wsahtons) function) before using it to construct an address.</span></span> <span data-ttu-id="3d5cb-114">À l’inverse, si l’application devait afficher le numéro du port dans une adresse (retourné par [**getpeername**](/windows/desktop/api/winsock/nf-winsock-getpeername) par exemple), le numéro de port doit être converti de l’ordre réseau à l’ordinateur hôte (à l’aide de la fonction [**ntohs**](/windows/desktop/api/winsock/nf-winsock-ntohs) ou [**WSANtohs**](/windows/desktop/api/Winsock2/nf-winsock2-wsantohs) ) avant de pouvoir être affiché.</span><span class="sxs-lookup"><span data-stu-id="3d5cb-114">Conversely, if the application were to display the number of the port within an address (returned by [**getpeername**](/windows/desktop/api/winsock/nf-winsock-getpeername) for example), the port number must be converted from network to host order (using the [**ntohs**](/windows/desktop/api/winsock/nf-winsock-ntohs) or [**WSANtohs**](/windows/desktop/api/Winsock2/nf-winsock2-wsantohs) function) before it can be displayed.</span></span>

<span data-ttu-id="3d5cb-115">Étant donné que les commandes d’octet Intel et Internet sont différentes, les conversions décrites dans les précédentes sont inévitables.</span><span class="sxs-lookup"><span data-stu-id="3d5cb-115">Since the Intel and Internet byte orders are different, the conversions described in the preceding are unavoidable.</span></span> <span data-ttu-id="3d5cb-116">Les enregistreurs d’applications doivent utiliser les fonctions de conversion standard fournies dans le cadre de Winsock plutôt que d’écrire leur propre code de conversion dans la mesure où les futures implémentations de Winsock sont susceptibles de s’exécuter sur des systèmes dont l’ordre des hôtes est identique à l’ordre des octets du réseau.</span><span class="sxs-lookup"><span data-stu-id="3d5cb-116">Application writers are cautioned that they should use the standard conversion functions provided as part of Winsock rather than writing their own conversion code since future implementations of Winsock are likely to run on systems for which the host order is identical to the network byte order.</span></span> <span data-ttu-id="3d5cb-117">Seules les applications qui utilisent les fonctions de conversion standard entre l’hôte et l’ordre des octets du réseau sont susceptibles d’être portables.</span><span class="sxs-lookup"><span data-stu-id="3d5cb-117">Only applications that use the standard conversion functions between host and network byte order are likely to be portable.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3d5cb-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3d5cb-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3d5cb-119">**getpeername**</span><span class="sxs-lookup"><span data-stu-id="3d5cb-119">**getpeername**</span></span>](/windows/desktop/api/winsock/nf-winsock-getpeername)
</dt> <dt>

[<span data-ttu-id="3d5cb-120">**getservbyname**</span><span class="sxs-lookup"><span data-stu-id="3d5cb-120">**getservbyname**</span></span>](/windows/desktop/api/winsock/nf-winsock-getservbyname)
</dt> <dt>

[<span data-ttu-id="3d5cb-121">**htonl**</span><span class="sxs-lookup"><span data-stu-id="3d5cb-121">**htonl**</span></span>](/windows/desktop/api/winsock/nf-winsock-htonl)
</dt> <dt>

[<span data-ttu-id="3d5cb-122">**htons**</span><span class="sxs-lookup"><span data-stu-id="3d5cb-122">**htons**</span></span>](/windows/desktop/api/winsock/nf-winsock-htons)
</dt> <dt>

[<span data-ttu-id="3d5cb-123">**ntohl**</span><span class="sxs-lookup"><span data-stu-id="3d5cb-123">**ntohl**</span></span>](/windows/desktop/api/winsock/nf-winsock-ntohl)
</dt> <dt>

[<span data-ttu-id="3d5cb-124">**ntohs**</span><span class="sxs-lookup"><span data-stu-id="3d5cb-124">**ntohs**</span></span>](/windows/desktop/api/winsock/nf-winsock-ntohs)
</dt> <dt>

[<span data-ttu-id="3d5cb-125">Portage d’applications de socket vers Winsock</span><span class="sxs-lookup"><span data-stu-id="3d5cb-125">Porting Socket Applications to Winsock</span></span>](porting-socket-applications-to-winsock.md)
</dt> <dt>

[<span data-ttu-id="3d5cb-126">**sockaddr**</span><span class="sxs-lookup"><span data-stu-id="3d5cb-126">**sockaddr**</span></span>](sockaddr-2.md)
</dt> <dt>

[<span data-ttu-id="3d5cb-127">Considérations sur la programmation Winsock</span><span class="sxs-lookup"><span data-stu-id="3d5cb-127">Winsock Programming Considerations</span></span>](winsock-programming-considerations.md)
</dt> <dt>

[<span data-ttu-id="3d5cb-128">**WSAHtonl**</span><span class="sxs-lookup"><span data-stu-id="3d5cb-128">**WSAHtonl**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsahtonl)
</dt> <dt>

[<span data-ttu-id="3d5cb-129">**WSAHtons**</span><span class="sxs-lookup"><span data-stu-id="3d5cb-129">**WSAHtons**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsahtons)
</dt> <dt>

[<span data-ttu-id="3d5cb-130">**WSANtohl**</span><span class="sxs-lookup"><span data-stu-id="3d5cb-130">**WSANtohl**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsantohl)
</dt> <dt>

[<span data-ttu-id="3d5cb-131">**WSANtohs**</span><span class="sxs-lookup"><span data-stu-id="3d5cb-131">**WSANtohs**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsantohs)
</dt> </dl>

 

 



