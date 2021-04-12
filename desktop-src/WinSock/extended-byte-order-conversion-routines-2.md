---
description: Windows Sockets 2 ne suppose pas que l’ordre d’octet du réseau pour tous les protocoles est le même.
ms.assetid: 517c21b5-4b56-49f8-88ae-103fdfce6441
title: Routines de conversion de Byte-Order étendues
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9addb2b1527546b8a7d13eb90581a333f87c6f0e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526182"
---
# <a name="extended-byte-order-conversion-routines"></a><span data-ttu-id="28df5-103">Routines de conversion de Byte-Order étendues</span><span class="sxs-lookup"><span data-stu-id="28df5-103">Extended Byte-Order Conversion Routines</span></span>

<span data-ttu-id="28df5-104">Windows Sockets 2 ne suppose pas que l’ordre d’octet du réseau pour tous les protocoles est le même.</span><span class="sxs-lookup"><span data-stu-id="28df5-104">Windows Sockets 2 does not assume that the network byte order for all protocols is the same.</span></span> <span data-ttu-id="28df5-105">Un ensemble de routines de conversion est fourni pour convertir les quantités 16 bits et 32 bits vers et à partir de l’ordre d’octet du réseau.</span><span class="sxs-lookup"><span data-stu-id="28df5-105">A set of conversion routines is supplied for converting 16-bit and 32-bit quantities to and from network byte order.</span></span> <span data-ttu-id="28df5-106">Ces routines prennent comme paramètre d’entrée le handle de socket auquel est associée une structure [**WSAPROTOCOL \_ info**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) .</span><span class="sxs-lookup"><span data-stu-id="28df5-106">These routines take as an input parameter the socket handle that has a [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure associated with it.</span></span> <span data-ttu-id="28df5-107">Le membre **NetworkByteOrder** de la structure **WSAPROTOCOL \_ info** spécifie l’ordre d’octet réseau souhaité (à l’heure actuelle Big-endian ou Little-endian).</span><span class="sxs-lookup"><span data-stu-id="28df5-107">The **NetworkByteOrder** member of the **WSAPROTOCOL\_INFO** structure specifies the desired network byte order (currently either big-endian or little-endian).</span></span>

## <a name="related-topics"></a><span data-ttu-id="28df5-108">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="28df5-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="28df5-109">**htonl**</span><span class="sxs-lookup"><span data-stu-id="28df5-109">**htonl**</span></span>](/windows/desktop/api/winsock/nf-winsock-htonl)
</dt> <dt>

[<span data-ttu-id="28df5-110">**htons**</span><span class="sxs-lookup"><span data-stu-id="28df5-110">**htons**</span></span>](/windows/desktop/api/winsock/nf-winsock-htons)
</dt> <dt>

[<span data-ttu-id="28df5-111">**ntohl**</span><span class="sxs-lookup"><span data-stu-id="28df5-111">**ntohl**</span></span>](/windows/desktop/api/winsock/nf-winsock-ntohl)
</dt> <dt>

[<span data-ttu-id="28df5-112">**ntohs**</span><span class="sxs-lookup"><span data-stu-id="28df5-112">**ntohs**</span></span>](/windows/desktop/api/winsock/nf-winsock-ntohs)
</dt> <dt>

[<span data-ttu-id="28df5-113">Portage d’applications de socket vers Winsock</span><span class="sxs-lookup"><span data-stu-id="28df5-113">Porting Socket Applications to Winsock</span></span>](porting-socket-applications-to-winsock.md)
</dt> <dt>

[<span data-ttu-id="28df5-114">Considérations sur la programmation Winsock</span><span class="sxs-lookup"><span data-stu-id="28df5-114">Winsock Programming Considerations</span></span>](winsock-programming-considerations.md)
</dt> <dt>

[<span data-ttu-id="28df5-115">**WSAHtonl**</span><span class="sxs-lookup"><span data-stu-id="28df5-115">**WSAHtonl**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsahtonl)
</dt> <dt>

[<span data-ttu-id="28df5-116">**WSAHtons**</span><span class="sxs-lookup"><span data-stu-id="28df5-116">**WSAHtons**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsahtons)
</dt> <dt>

[<span data-ttu-id="28df5-117">**WSANtohl**</span><span class="sxs-lookup"><span data-stu-id="28df5-117">**WSANtohl**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsantohl)
</dt> <dt>

[<span data-ttu-id="28df5-118">**WSANtohs**</span><span class="sxs-lookup"><span data-stu-id="28df5-118">**WSANtohs**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsantohs)
</dt> <dt>

[<span data-ttu-id="28df5-119">**\_informations WSAPROTOCOL**</span><span class="sxs-lookup"><span data-stu-id="28df5-119">**WSAPROTOCOL\_INFO**</span></span>](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa)
</dt> </dl>

 

 
