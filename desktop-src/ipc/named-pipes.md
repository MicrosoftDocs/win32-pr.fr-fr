---
description: Un canal nommé est un canal nommé, unidirectionnel ou duplex pour la communication entre le serveur de canal et un ou plusieurs clients de canal.
ms.assetid: 7a4c11ac-14c0-4a93-b72e-02fb8852cc15
title: Canaux nommés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0675244e09b7c202b4fa6b67f6268392b1b260f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952136"
---
# <a name="named-pipes"></a><span data-ttu-id="e9987-103">Canaux nommés</span><span class="sxs-lookup"><span data-stu-id="e9987-103">Named Pipes</span></span>

<span data-ttu-id="e9987-104">Un *canal nommé* est un canal nommé, unidirectionnel ou duplex pour la communication entre le serveur de canal et un ou plusieurs clients de canal.</span><span class="sxs-lookup"><span data-stu-id="e9987-104">A *named pipe* is a named, one-way or duplex pipe for communication between the pipe server and one or more pipe clients.</span></span> <span data-ttu-id="e9987-105">Toutes les instances d’un canal nommé partagent le même nom de canal, mais chaque instance possède ses propres tampons et Handles et fournit un canal de communication distinct pour la communication client/serveur.</span><span class="sxs-lookup"><span data-stu-id="e9987-105">All instances of a named pipe share the same pipe name, but each instance has its own buffers and handles, and provides a separate conduit for client/server communication.</span></span> <span data-ttu-id="e9987-106">L’utilisation d’instances permet à plusieurs clients de canal d’utiliser simultanément le même canal nommé.</span><span class="sxs-lookup"><span data-stu-id="e9987-106">The use of instances enables multiple pipe clients to use the same named pipe simultaneously.</span></span>

<span data-ttu-id="e9987-107">Tout processus peut accéder à des canaux nommés, soumis à des vérifications de sécurité, ce qui fait des canaux nommés une forme simple de communication entre les processus liés ou non associés.</span><span class="sxs-lookup"><span data-stu-id="e9987-107">Any process can access named pipes, subject to security checks, making named pipes an easy form of communication between related or unrelated processes.</span></span>

<span data-ttu-id="e9987-108">Tout processus peut agir à la fois comme un serveur et un client, ce qui rend possible la communication d’égal à égal.</span><span class="sxs-lookup"><span data-stu-id="e9987-108">Any process can act as both a server and a client, making peer-to-peer communication possible.</span></span> <span data-ttu-id="e9987-109">Comme c’est le cas ici, le terme « serveur de canal » fait référence à un processus qui crée un canal nommé, et le terme « client de canal » fait référence à un processus qui se connecte à une instance d’un canal nommé.</span><span class="sxs-lookup"><span data-stu-id="e9987-109">As used here, the term pipe server refers to a process that creates a named pipe, and the term pipe client refers to a process that connects to an instance of a named pipe.</span></span> <span data-ttu-id="e9987-110">La fonction côté serveur pour instancier un canal nommé est [**CreateNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea).</span><span class="sxs-lookup"><span data-stu-id="e9987-110">The server-side function for instantiating a named pipe is [**CreateNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea).</span></span> <span data-ttu-id="e9987-111">La fonction côté serveur pour accepter une connexion est [**ConnectNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe).</span><span class="sxs-lookup"><span data-stu-id="e9987-111">The server-side function for accepting a connection is [**ConnectNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe).</span></span> <span data-ttu-id="e9987-112">Un processus client se connecte à un canal nommé à l’aide de la fonction [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) ou [**CallNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-callnamedpipea) .</span><span class="sxs-lookup"><span data-stu-id="e9987-112">A client process connects to a named pipe by using the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) or [**CallNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-callnamedpipea) function.</span></span>

<span data-ttu-id="e9987-113">Les canaux nommés peuvent être utilisés pour assurer la communication entre les processus sur le même ordinateur ou entre des processus sur différents ordinateurs sur un réseau.</span><span class="sxs-lookup"><span data-stu-id="e9987-113">Named pipes can be used to provide communication between processes on the same computer or between processes on different computers across a network.</span></span> <span data-ttu-id="e9987-114">Si le service serveur est en cours d’exécution, tous les canaux nommés sont accessibles à distance.</span><span class="sxs-lookup"><span data-stu-id="e9987-114">If the server service is running, all named pipes are accessible remotely.</span></span> <span data-ttu-id="e9987-115">Si vous envisagez d’utiliser un canal nommé localement uniquement, refusez l’accès au réseau de l’autorité NT \\ ou basculez en RPC local.</span><span class="sxs-lookup"><span data-stu-id="e9987-115">If you intend to use a named pipe locally only, deny access to NT AUTHORITY\\NETWORK or switch to local RPC.</span></span>

<span data-ttu-id="e9987-116">Pour plus d'informations, voir les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="e9987-116">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="e9987-117">Noms de canaux</span><span class="sxs-lookup"><span data-stu-id="e9987-117">Pipe Names</span></span>](pipe-names.md)
-   [<span data-ttu-id="e9987-118">Modes ouverts du canal nommé</span><span class="sxs-lookup"><span data-stu-id="e9987-118">Named Pipe Open Modes</span></span>](named-pipe-open-modes.md)
-   [<span data-ttu-id="e9987-119">Modes de type canal nommé, lecture et attente</span><span class="sxs-lookup"><span data-stu-id="e9987-119">Named Pipe Type, Read, and Wait Modes</span></span>](named-pipe-type-read-and-wait-modes.md)
-   [<span data-ttu-id="e9987-120">Instances de canal nommé</span><span class="sxs-lookup"><span data-stu-id="e9987-120">Named Pipe Instances</span></span>](named-pipe-instances.md)
-   [<span data-ttu-id="e9987-121">Opérations de canal nommé</span><span class="sxs-lookup"><span data-stu-id="e9987-121">Named Pipe Operations</span></span>](named-pipe-operations.md)
-   [<span data-ttu-id="e9987-122">Entrée et sortie synchrones et superposées</span><span class="sxs-lookup"><span data-stu-id="e9987-122">Synchronous and Overlapped Input and Output</span></span>](synchronous-and-overlapped-input-and-output.md)
-   [<span data-ttu-id="e9987-123">Sécurité des canaux nommés et droits d’accès</span><span class="sxs-lookup"><span data-stu-id="e9987-123">Named Pipe Security and Access Rights</span></span>](named-pipe-security-and-access-rights.md)
-   [<span data-ttu-id="e9987-124">Emprunt de l’identité d’un client de canal nommé</span><span class="sxs-lookup"><span data-stu-id="e9987-124">Impersonating a Named Pipe Client</span></span>](impersonating-a-named-pipe-client.md)
-   [<span data-ttu-id="e9987-125">Utilisation de canaux</span><span class="sxs-lookup"><span data-stu-id="e9987-125">Using Pipes</span></span>](using-pipes.md)

 

 
