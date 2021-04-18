---
description: Cette section décrit les considérations relatives au portage Winsock.
ms.assetid: 41c0c98e-3990-4600-ab9f-fa87edbea402
title: Portage d’applications de socket vers Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0e2b3480d5572405d33b3a3532892a48633caa5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519295"
---
# <a name="porting-socket-applications-to-winsock"></a><span data-ttu-id="28b7f-103">Portage d’applications de socket vers Winsock</span><span class="sxs-lookup"><span data-stu-id="28b7f-103">Porting Socket Applications to Winsock</span></span>

<span data-ttu-id="28b7f-104">Cette section décrit les considérations relatives au portage Winsock.</span><span class="sxs-lookup"><span data-stu-id="28b7f-104">This section describes Winsock porting considerations.</span></span>

<span data-ttu-id="28b7f-105">Il existe un nombre limité d’instances dans lesquelles Windows Sockets s’est détournée d’un respect strict aux conventions Berkeley, généralement en raison de problèmes d’implémentation dans l’environnement Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="28b7f-105">There are a limited number of instances where Windows Sockets has diverted from strict adherence to the Berkeley conventions, usually due to implementation difficulties in the Microsoft Windows environment.</span></span>

<span data-ttu-id="28b7f-106">Lorsqu’un écart par rapport aux conventions Berkeley se produit dans Windows Sockets, l’écart est expressément et clairement indiqué.</span><span class="sxs-lookup"><span data-stu-id="28b7f-106">When a deviation from Berkeley conventions occurs in Windows Sockets, the deviation is specifically and clearly noted.</span></span> <span data-ttu-id="28b7f-107">Par exemple, si une fonction est spécifique à Windows Sockets, cet écart est spécifié avec une expression dans la description de la fonction similaire à ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="28b7f-107">For example, if a function is specific to Windows Sockets, that deviation is specified with a phrase in the function description similar to the following:</span></span>

<span data-ttu-id="28b7f-108">La fonction **\[ de nom \] de fonction** est une extension spécifique à Microsoft de l’API Windows Sockets 2.</span><span class="sxs-lookup"><span data-stu-id="28b7f-108">The **\[function-name\]** function is a Microsoft-specific extension to the Windows Sockets 2 API.</span></span>

<span data-ttu-id="28b7f-109">Cette section fournit des informations sur le portage d’applications de sockets UNIX Berkeley (BSD) vers Winsock :</span><span class="sxs-lookup"><span data-stu-id="28b7f-109">This section provides information about porting Berkeley (BSD) UNIX socket applications to Winsock:</span></span>

-   [<span data-ttu-id="28b7f-110">Type de données Socket</span><span class="sxs-lookup"><span data-stu-id="28b7f-110">Socket Data Type</span></span>](socket-data-type-2.md)
-   [<span data-ttu-id="28b7f-111">Macros Select, FD \_ set et FD \_ xxx</span><span class="sxs-lookup"><span data-stu-id="28b7f-111">Select, FD\_SET, and FD\_XXX Macros</span></span>](select-and-fd---2.md)
-   [<span data-ttu-id="28b7f-112">Codes d’erreur-errno, h \_ errno et WSAGetLastError</span><span class="sxs-lookup"><span data-stu-id="28b7f-112">Error Codes - errno, h\_errno and WSAGetLastError</span></span>](error-codes-errno-h-errno-and-wsagetlasterror-2.md)
-   [<span data-ttu-id="28b7f-113">Pointeurs</span><span class="sxs-lookup"><span data-stu-id="28b7f-113">Pointers</span></span>](pointers-2.md)
-   [<span data-ttu-id="28b7f-114">Fonctions renommées</span><span class="sxs-lookup"><span data-stu-id="28b7f-114">Renamed Functions</span></span>](renamed-functions-2.md)
-   [<span data-ttu-id="28b7f-115">Nombre maximal de sockets pris en charge</span><span class="sxs-lookup"><span data-stu-id="28b7f-115">Maximum Number of Sockets Supported</span></span>](maximum-number-of-sockets-supported-2.md)
-   [<span data-ttu-id="28b7f-116">Fichiers include</span><span class="sxs-lookup"><span data-stu-id="28b7f-116">Include Files</span></span>](include-files-2.md)
-   [<span data-ttu-id="28b7f-117">Valeurs de retour en cas d’échec de la fonction</span><span class="sxs-lookup"><span data-stu-id="28b7f-117">Return Values on Function Failure</span></span>](return-values-on-function-failure-2.md)
-   [<span data-ttu-id="28b7f-118">Sockets bruts</span><span class="sxs-lookup"><span data-stu-id="28b7f-118">Raw Sockets</span></span>](service-provided-raw-sockets-2.md)
-   [<span data-ttu-id="28b7f-119">Classement des octets</span><span class="sxs-lookup"><span data-stu-id="28b7f-119">Byte Ordering</span></span>](byte-ordering-2.md)
-   [<span data-ttu-id="28b7f-120">Routines de conversion de Byte-Order étendues</span><span class="sxs-lookup"><span data-stu-id="28b7f-120">Extended Byte-Order Conversion Routines</span></span>](extended-byte-order-conversion-routines-2.md)

## <a name="related-topics"></a><span data-ttu-id="28b7f-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="28b7f-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="28b7f-122">Gestion des erreurs Winsock</span><span class="sxs-lookup"><span data-stu-id="28b7f-122">Handling Winsock Errors</span></span>](handling-winsock-errors.md)
</dt> <dt>

[<span data-ttu-id="28b7f-123">Portage d’applications de socket vers Winsock</span><span class="sxs-lookup"><span data-stu-id="28b7f-123">Porting Socket Applications to Winsock</span></span>](porting-socket-applications-to-winsock.md)
</dt> <dt>

[<span data-ttu-id="28b7f-124">Codes d’erreur de Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="28b7f-124">Windows Sockets Error Codes</span></span>](windows-sockets-error-codes-2.md)
</dt> <dt>

[<span data-ttu-id="28b7f-125">Considérations sur la programmation Winsock</span><span class="sxs-lookup"><span data-stu-id="28b7f-125">Winsock Programming Considerations</span></span>](winsock-programming-considerations.md)
</dt> </dl>

 

 



