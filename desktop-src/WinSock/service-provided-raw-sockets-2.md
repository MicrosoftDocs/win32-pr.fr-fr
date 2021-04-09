---
description: Un socket brut est un type de socket qui autorise l’accès au fournisseur de transport sous-jacent. L’utilisation de sockets bruts lors du Portage d’applications vers Winsock n’est pas recommandée pour plusieurs raisons.
ms.assetid: b78c75b7-255c-4e85-9a88-0efb3b5f0e51
title: Sockets bruts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 209c884e85327a7a8c1d21292d9342a0c032747a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114907"
---
# <a name="raw-sockets"></a><span data-ttu-id="4a594-104">Sockets bruts</span><span class="sxs-lookup"><span data-stu-id="4a594-104">Raw Sockets</span></span>

<span data-ttu-id="4a594-105">Un socket brut est un type de socket qui autorise l’accès au fournisseur de transport sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="4a594-105">A raw socket is a type of socket that allows access to the underlying transport provider.</span></span> <span data-ttu-id="4a594-106">L’utilisation de sockets bruts lors du Portage d’applications vers Winsock n’est pas recommandée pour plusieurs raisons.</span><span class="sxs-lookup"><span data-stu-id="4a594-106">The use of raw sockets when porting applications to Winsock is not recommended for several reasons.</span></span>

<span data-ttu-id="4a594-107">La spécification Windows Sockets ne requiert pas qu’un fournisseur de services Winsock prenne en charge les sockets bruts, autrement dit, les sockets de type **chaussette \_ RAW**.</span><span class="sxs-lookup"><span data-stu-id="4a594-107">The Windows Sockets specification does not mandate that a Winsock service provider support raw sockets, that is, sockets of type **SOCK\_RAW**.</span></span> <span data-ttu-id="4a594-108">Toutefois, les fournisseurs de services sont encouragés à fournir une prise en charge des sockets bruts.</span><span class="sxs-lookup"><span data-stu-id="4a594-108">However, service providers are encouraged to supply raw socket support.</span></span> <span data-ttu-id="4a594-109">Une application compatible avec Windows Sockets qui souhaite utiliser des sockets bruts doit tenter d’ouvrir le socket avec l’appel de [**Socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) et, si elle échoue, tente d’utiliser un autre type de socket ou indique l’échec de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="4a594-109">A Windows Sockets-compliant application that wishes to use raw sockets should attempt to open the socket with the [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) call, and if it fails either attempt to use another socket type or indicate the failure to the user.</span></span>

<span data-ttu-id="4a594-110">Sur Windows 7, Windows Server 2008 R2, Windows Vista et Windows XP avec Service Pack 2 (SP2), la possibilité d’envoyer du trafic sur des sockets bruts a été restreinte de plusieurs façons.</span><span class="sxs-lookup"><span data-stu-id="4a594-110">On Windows 7, Windows Server 2008 R2, Windows Vista, and Windows XP with Service Pack 2 (SP2), the ability to send traffic over raw sockets has been restricted in several ways.</span></span> <span data-ttu-id="4a594-111">Pour plus d’informations, consultez [sockets bruts TCP/IP](tcp-ip-raw-sockets-2.md).</span><span class="sxs-lookup"><span data-stu-id="4a594-111">For more information, see [TCP/IP Raw Sockets](tcp-ip-raw-sockets-2.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="4a594-112">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4a594-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4a594-113">Portage d’applications de socket vers Winsock</span><span class="sxs-lookup"><span data-stu-id="4a594-113">Porting Socket Applications to Winsock</span></span>](porting-socket-applications-to-winsock.md)
</dt> <dt>

[<span data-ttu-id="4a594-114">**socle**</span><span class="sxs-lookup"><span data-stu-id="4a594-114">**socket**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-socket)
</dt> <dt>

[<span data-ttu-id="4a594-115">Sockets bruts TCP/IP</span><span class="sxs-lookup"><span data-stu-id="4a594-115">TCP/IP Raw Sockets</span></span>](tcp-ip-raw-sockets-2.md)
</dt> <dt>

[<span data-ttu-id="4a594-116">Considérations sur la programmation Winsock</span><span class="sxs-lookup"><span data-stu-id="4a594-116">Winsock Programming Considerations</span></span>](winsock-programming-considerations.md)
</dt> </dl>

 

 



