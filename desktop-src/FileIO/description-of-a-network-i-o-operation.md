---
description: Décrit le processus d’une opération d’e/s réseau sous Windows.
ms.assetid: 72dc0c57-28ae-4289-bb0d-b399d294c126
title: Description d’une opération d’e/s réseau
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 371b72389554f1c3fa2ec43180b1a6e4c76dc012
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319297"
---
# <a name="description-of-a-network-io-operation"></a><span data-ttu-id="aad56-103">Description d’une opération d’e/s réseau</span><span class="sxs-lookup"><span data-stu-id="aad56-103">Description of a Network I/O Operation</span></span>

<span data-ttu-id="aad56-104">La figure suivante illustre le processus d’une opération d’e/s réseau sous Windows.</span><span class="sxs-lookup"><span data-stu-id="aad56-104">The following figure illustrates the process of a network I/O operation under Windows.</span></span>

![opération d’e/s réseau sous Windows](images/fig4.png)

<span data-ttu-id="aad56-106">Quand une application appelle une fonction d’e/s de fichier pour accéder à un fichier sur un ordinateur distant, les événements suivants se produisent :</span><span class="sxs-lookup"><span data-stu-id="aad56-106">When an application calls a file I/O function to access a file on a remote computer, the following events occur:</span></span>

-   <span data-ttu-id="aad56-107">La requête d’e/s est interceptée par un [redirecteur réseau](network-redirectors.md), également appelé simplement redirecteur, sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="aad56-107">The I/O request is intercepted by a [network redirector](network-redirectors.md), also referred to simply as a redirector, on the local computer.</span></span> <span data-ttu-id="aad56-108">Cela est représenté dans l’illustration précédente par la flèche pleine entre l’application et le redirecteur du client.</span><span class="sxs-lookup"><span data-stu-id="aad56-108">This is depicted in the preceding figure by the solid arrow between the application and the client redirector.</span></span>
-   <span data-ttu-id="aad56-109">Le redirecteur construit un paquet de données contenant toutes les informations sur la demande et l’envoie au serveur où se trouve le fichier.</span><span class="sxs-lookup"><span data-stu-id="aad56-109">The redirector constructs a data packet containing all of the information about the request, and sends it to the server where the file is located.</span></span> <span data-ttu-id="aad56-110">Cela est illustré dans la figure précédente par la flèche pleine entre le redirecteur du client et le redirecteur du serveur.</span><span class="sxs-lookup"><span data-stu-id="aad56-110">This is depicted in the preceding figure by the solid arrow between the client redirector and the server redirector.</span></span>
-   <span data-ttu-id="aad56-111">Le redirecteur sur le serveur reçoit le paquet du client, authentifie l’accès au fichier requis par la requête d’e/s et, s’il est authentifié, exécute la demande pour le compte du client.</span><span class="sxs-lookup"><span data-stu-id="aad56-111">The redirector on the server receives the packet from the client, authenticates the access to the file required by the I/O request, and, if authenticated, executes the request on behalf of the client.</span></span> <span data-ttu-id="aad56-112">Si ce n’est pas le cas, il renvoie un code d’erreur au redirecteur sur le client.</span><span class="sxs-lookup"><span data-stu-id="aad56-112">If not, it returns an error code to the redirector on the client.</span></span> <span data-ttu-id="aad56-113">Cela est représenté dans l’illustration précédente par la flèche pleine courbée entre le redirecteur du serveur et le fichier.</span><span class="sxs-lookup"><span data-stu-id="aad56-113">This is depicted in the preceding figure by the curved solid arrow between the server redirector and the file.</span></span>
-   <span data-ttu-id="aad56-114">Lorsque la requête a été exécutée, le redirecteur sur le serveur envoie toutes les données résultant de la demande d’e/s au redirecteur sur le client, ainsi qu’une notification de réussite.</span><span class="sxs-lookup"><span data-stu-id="aad56-114">When the request has been executed, the redirector on the server sends any data resulting from the I/O request to the redirector on the client along with a success notification.</span></span> <span data-ttu-id="aad56-115">Cela est illustré dans la figure précédente par la flèche en pointillés entre le serveur et le redirecteur du client.</span><span class="sxs-lookup"><span data-stu-id="aad56-115">This is depicted in the preceding figure by the dotted arrow between the server and the client redirector.</span></span>
-   <span data-ttu-id="aad56-116">Le redirecteur sur le client reçoit le paquet du serveur et transmet les données du paquet à l’application, ainsi qu’une notification de réussite.</span><span class="sxs-lookup"><span data-stu-id="aad56-116">The redirector on the client receives the packet from the server and passes the data in the packet to the application along with a success notification.</span></span> <span data-ttu-id="aad56-117">Cela est illustré dans la figure précédente par la flèche pointillée entre le redirecteur du client et l’application.</span><span class="sxs-lookup"><span data-stu-id="aad56-117">This is depicted in the preceding figure by the dotted arrow between the client redirector and the application.</span></span>

<span data-ttu-id="aad56-118">Windows peut utiliser divers protocoles réseau pour effectuer une opération d’e/s réseau, notamment le [protocole SMB Microsoft et la vue d’ensemble du protocole CIFS](microsoft-smb-protocol-and-cifs-protocol-overview.md) et NFS.</span><span class="sxs-lookup"><span data-stu-id="aad56-118">Windows can use a variety of networking protocols to perform a network I/O operation, including [Microsoft SMB Protocol and CIFS Protocol Overview](microsoft-smb-protocol-and-cifs-protocol-overview.md) and NFS.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="aad56-119">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="aad56-119">In this section</span></span>



| <span data-ttu-id="aad56-120">Rubrique</span><span class="sxs-lookup"><span data-stu-id="aad56-120">Topic</span></span>                                                                                       | <span data-ttu-id="aad56-121">Description</span><span class="sxs-lookup"><span data-stu-id="aad56-121">Description</span></span>                                                          |
|---------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [<span data-ttu-id="aad56-122">Différences dans les e/s locales et réseau</span><span class="sxs-lookup"><span data-stu-id="aad56-122">Differences in Local and Network I/O</span></span>](differences-in-local-and-network-i-o.md)<br/> | <span data-ttu-id="aad56-123">Différences entre les e/s locales et les e/s réseau sur Windows.</span><span class="sxs-lookup"><span data-stu-id="aad56-123">Differences between local I/O and network I/O on Windows.</span></span><br/> |
| [<span data-ttu-id="aad56-124">Redirecteurs réseau</span><span class="sxs-lookup"><span data-stu-id="aad56-124">Network Redirectors</span></span>](network-redirectors.md)<br/>                                   | <span data-ttu-id="aad56-125">Décrit les fonctionnalités d’un redirecteur réseau.</span><span class="sxs-lookup"><span data-stu-id="aad56-125">Describes the functionality of a network redirector.</span></span><br/>      |



 

 

 




