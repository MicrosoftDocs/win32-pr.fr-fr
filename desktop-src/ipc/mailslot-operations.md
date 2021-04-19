---
description: Descriptions des fonctions à utiliser lors de l’utilisation des mailslots, des clients et des serveurs.
ms.assetid: 40758d5e-8538-47d9-b8ca-8de5b053ee8b
title: Opérations mailslot
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0055ad434971659dc2cfd058146029bb63023654
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106537026"
---
# <a name="mailslot-operations"></a><span data-ttu-id="3abaa-103">Opérations mailslot</span><span class="sxs-lookup"><span data-stu-id="3abaa-103">Mailslot Operations</span></span>

<span data-ttu-id="3abaa-104">Lorsque vous utilisez des mailslots, les clients et les serveurs doivent utiliser uniquement les fonctions décrites dans les tableaux suivants.</span><span class="sxs-lookup"><span data-stu-id="3abaa-104">When working with mailslots, clients and servers should use only the functions discussed in the following tables.</span></span> <span data-ttu-id="3abaa-105">N’utilisez pas d’autres fonctions, même si elles acceptent des handles de fichiers ou des noms de fichiers en tant que paramètres, car elles ne sont pas conçues pour fonctionner avec des mailslots.</span><span class="sxs-lookup"><span data-stu-id="3abaa-105">Do not use other functions, even if they accept file handles or file names as parameters, as they are not designed to work with mailslots.</span></span>

## <a name="mailslot-server-functions"></a><span data-ttu-id="3abaa-106">Fonctions du serveur mailslot</span><span class="sxs-lookup"><span data-stu-id="3abaa-106">Mailslot Server Functions</span></span>

<span data-ttu-id="3abaa-107">Les serveurs mailslot ont une utilisation exclusive de trois fonctions, comme indiqué dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="3abaa-107">Mailslot servers have exclusive use of three functions, as shown in the following table.</span></span>



| <span data-ttu-id="3abaa-108">Fonction</span><span class="sxs-lookup"><span data-stu-id="3abaa-108">Function</span></span>                                   | <span data-ttu-id="3abaa-109">Description</span><span class="sxs-lookup"><span data-stu-id="3abaa-109">Description</span></span>                                                                                                                                                                                                  |
|--------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3abaa-110">**CreateMailslot**</span><span class="sxs-lookup"><span data-stu-id="3abaa-110">**CreateMailslot**</span></span>](/windows/desktop/api/Winbase/nf-winbase-createmailslota)   | <span data-ttu-id="3abaa-111">Crée un mailslot et retourne un handle mailslot.</span><span class="sxs-lookup"><span data-stu-id="3abaa-111">Creates a mailslot and returns a mailslot handle.</span></span>                                                                                                                                                            |
| [<span data-ttu-id="3abaa-112">**GetMailslotInfo**</span><span class="sxs-lookup"><span data-stu-id="3abaa-112">**GetMailslotInfo**</span></span>](/windows/desktop/api/Winbase/nf-winbase-getmailslotinfo) | <span data-ttu-id="3abaa-113">Récupère la taille maximale des messages, la taille des messages MailSlot, la taille du message suivant dans le mailslot, le nombre de messages dans le mailslot et la durée pendant laquelle une opération de lecture peut attendre un message.</span><span class="sxs-lookup"><span data-stu-id="3abaa-113">Retrieves the maximum message size, the mailslot size, the size of the next message in the mailslot, the number of messages in the mailslot, and the amount of time a read operation can wait for a message.</span></span> |
| [<span data-ttu-id="3abaa-114">**SetMailslotInfo**</span><span class="sxs-lookup"><span data-stu-id="3abaa-114">**SetMailslotInfo**</span></span>](/windows/desktop/api/Winbase/nf-winbase-setmailslotinfo) | <span data-ttu-id="3abaa-115">Modifie le délai d’attente de lecture pour un mailslot.</span><span class="sxs-lookup"><span data-stu-id="3abaa-115">Changes the read time-out for a mailslot.</span></span>                                                                                                                                                                    |



 

<span data-ttu-id="3abaa-116">Les fonctions suivantes sont également utilisées par les serveurs mailslot.</span><span class="sxs-lookup"><span data-stu-id="3abaa-116">The following functions are also used by mailslot servers.</span></span>



| <span data-ttu-id="3abaa-117">Fonction</span><span class="sxs-lookup"><span data-stu-id="3abaa-117">Function</span></span>                                                         | <span data-ttu-id="3abaa-118">Description</span><span class="sxs-lookup"><span data-stu-id="3abaa-118">Description</span></span>                                         |
|------------------------------------------------------------------|-----------------------------------------------------|
| [<span data-ttu-id="3abaa-119">**DuplicateHandle**</span><span class="sxs-lookup"><span data-stu-id="3abaa-119">**DuplicateHandle**</span></span>](/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle)                      | <span data-ttu-id="3abaa-120">Duplique le handle mailslot.</span><span class="sxs-lookup"><span data-stu-id="3abaa-120">Duplicates the mailslot handle.</span></span>                     |
| <span data-ttu-id="3abaa-121">[**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile), [ **ReadFileEx**](/windows/desktop/api/fileapi/nf-fileapi-readfileex)</span><span class="sxs-lookup"><span data-stu-id="3abaa-121">[**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile), [**ReadFileEx**](/windows/desktop/api/fileapi/nf-fileapi-readfileex)</span></span> | <span data-ttu-id="3abaa-122">Récupère les messages d’un mailslot.</span><span class="sxs-lookup"><span data-stu-id="3abaa-122">Retrieves messages from a mailslot.</span></span>                 |
| [<span data-ttu-id="3abaa-123">**GetFileTime**</span><span class="sxs-lookup"><span data-stu-id="3abaa-123">**GetFileTime**</span></span>](/windows/desktop/api/fileapi/nf-fileapi-getfiletime)                              | <span data-ttu-id="3abaa-124">Récupère la date et l’heure de création d’un mailslot.</span><span class="sxs-lookup"><span data-stu-id="3abaa-124">Retrieves the date and time a mailslot was created.</span></span> |
| [<span data-ttu-id="3abaa-125">**SetFileTime**</span><span class="sxs-lookup"><span data-stu-id="3abaa-125">**SetFileTime**</span></span>](/windows/desktop/api/fileapi/nf-fileapi-setfiletime)                              | <span data-ttu-id="3abaa-126">Définit la date et l’heure de création d’un mailslot.</span><span class="sxs-lookup"><span data-stu-id="3abaa-126">Sets the date and time a mailslot was created.</span></span>      |
| [<span data-ttu-id="3abaa-127">**GetHandleInformation**</span><span class="sxs-lookup"><span data-stu-id="3abaa-127">**GetHandleInformation**</span></span>](/windows/desktop/api/handleapi/nf-handleapi-gethandleinformation)            | <span data-ttu-id="3abaa-128">Récupère les propriétés du handle mailslot.</span><span class="sxs-lookup"><span data-stu-id="3abaa-128">Retrieves properties of the mailslot handle.</span></span>        |
| [<span data-ttu-id="3abaa-129">**SetHandleInformation**</span><span class="sxs-lookup"><span data-stu-id="3abaa-129">**SetHandleInformation**</span></span>](/windows/desktop/api/handleapi/nf-handleapi-sethandleinformation)            | <span data-ttu-id="3abaa-130">Définit les propriétés du handle mailslot.</span><span class="sxs-lookup"><span data-stu-id="3abaa-130">Sets properties of the mailslot handle.</span></span>             |



 

## <a name="mailslot-client-functions"></a><span data-ttu-id="3abaa-131">Fonctions du client mailslot</span><span class="sxs-lookup"><span data-stu-id="3abaa-131">Mailslot Client Functions</span></span>

<span data-ttu-id="3abaa-132">Un processus client utilise les fonctions suivantes lors de l’interaction avec un mailslot.</span><span class="sxs-lookup"><span data-stu-id="3abaa-132">A client process uses the following functions when interacting with a mailslot.</span></span>



| <span data-ttu-id="3abaa-133">Fonction</span><span class="sxs-lookup"><span data-stu-id="3abaa-133">Function</span></span>                                                             | <span data-ttu-id="3abaa-134">Description</span><span class="sxs-lookup"><span data-stu-id="3abaa-134">Description</span></span>                                     |
|----------------------------------------------------------------------|-------------------------------------------------|
| [<span data-ttu-id="3abaa-135">**CloseHandle**</span><span class="sxs-lookup"><span data-stu-id="3abaa-135">**CloseHandle**</span></span>](/windows/desktop/api/handleapi/nf-handleapi-closehandle)                                  | <span data-ttu-id="3abaa-136">Ferme un handle mailslot pour un processus client.</span><span class="sxs-lookup"><span data-stu-id="3abaa-136">Closes a mailslot handle for a client process.</span></span>  |
| [<span data-ttu-id="3abaa-137">**CreateFile**</span><span class="sxs-lookup"><span data-stu-id="3abaa-137">**CreateFile**</span></span>](/windows/desktop/api/fileapi/nf-fileapi-createfilea)                                    | <span data-ttu-id="3abaa-138">Crée un handle de mailslot pour un processus client.</span><span class="sxs-lookup"><span data-stu-id="3abaa-138">Creates a mailslot handle for a client process.</span></span> |
| [<span data-ttu-id="3abaa-139">**DuplicateHandle**</span><span class="sxs-lookup"><span data-stu-id="3abaa-139">**DuplicateHandle**</span></span>](/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle)                          | <span data-ttu-id="3abaa-140">Duplique un handle de mailslot.</span><span class="sxs-lookup"><span data-stu-id="3abaa-140">Duplicates a mailslot handle.</span></span>                   |
| <span data-ttu-id="3abaa-141">[**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile), [ **WriteFileEx**](/windows/desktop/api/fileapi/nf-fileapi-writefileex)</span><span class="sxs-lookup"><span data-stu-id="3abaa-141">[**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile), [**WriteFileEx**](/windows/desktop/api/fileapi/nf-fileapi-writefileex)</span></span> | <span data-ttu-id="3abaa-142">Écrit des données sur un mailslot.</span><span class="sxs-lookup"><span data-stu-id="3abaa-142">Writes data to a mailslot.</span></span>                      |



 

 

 
