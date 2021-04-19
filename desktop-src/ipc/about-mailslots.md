---
description: Un mailslot est un pseudofile qui réside en mémoire, et vous utilisez des fonctions de fichier standard pour y accéder.
ms.assetid: 9a68905d-c235-4c72-bc71-1cccdf5cdadc
title: À propos des mailslots
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bd83fc0d952577efdb149d4c7f25fffbab9784f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106538215"
---
# <a name="about-mailslots"></a><span data-ttu-id="de774-103">À propos des mailslots</span><span class="sxs-lookup"><span data-stu-id="de774-103">About Mailslots</span></span>

<span data-ttu-id="de774-104">Un mailslot est un pseudofile qui réside en mémoire, et vous utilisez des fonctions de fichier standard pour y accéder.</span><span class="sxs-lookup"><span data-stu-id="de774-104">A mailslot is a pseudofile that resides in memory, and you use standard file functions to access it.</span></span> <span data-ttu-id="de774-105">Les données d’un message mailslot peuvent se présenter sous n’importe quelle forme, mais elles ne peuvent pas être supérieures à 424 octets lors de leur envoi entre des ordinateurs.</span><span class="sxs-lookup"><span data-stu-id="de774-105">The data in a mailslot message can be in any form, but cannot be larger than 424 bytes when sent between computers.</span></span> <span data-ttu-id="de774-106">Contrairement aux fichiers sur disque, les mailslots sont temporaires.</span><span class="sxs-lookup"><span data-stu-id="de774-106">Unlike disk files, mailslots are temporary.</span></span> <span data-ttu-id="de774-107">Lorsque tous les descripteurs d’un mailslot sont fermés, le mailslot et toutes les données qu’il contient sont supprimés.</span><span class="sxs-lookup"><span data-stu-id="de774-107">When all handles to a mailslot are closed, the mailslot and all the data it contains are deleted.</span></span>

<span data-ttu-id="de774-108">Un *serveur mailslot* est un processus qui crée un mailslot et en possède un.</span><span class="sxs-lookup"><span data-stu-id="de774-108">A *mailslot server* is a process that creates and owns a mailslot.</span></span> <span data-ttu-id="de774-109">Quand le serveur crée un mailslot, il reçoit un handle mailslot.</span><span class="sxs-lookup"><span data-stu-id="de774-109">When the server creates a mailslot, it receives a mailslot handle.</span></span> <span data-ttu-id="de774-110">Ce descripteur doit être utilisé lorsqu’un processus lit des messages de la mailslot.</span><span class="sxs-lookup"><span data-stu-id="de774-110">This handle must be used when a process reads messages from the mailslot.</span></span> <span data-ttu-id="de774-111">Seul le processus qui crée un mailslot ou a obtenu le descripteur par un autre mécanisme (tel que l’héritage) peut lire à partir de la mailslot.</span><span class="sxs-lookup"><span data-stu-id="de774-111">Only the process that creates a mailslot or has obtained the handle by some other mechanism (such as inheritance) can read from the mailslot.</span></span> <span data-ttu-id="de774-112">Tous les mailslots sont locaux au processus qui les crée.</span><span class="sxs-lookup"><span data-stu-id="de774-112">All mailslots are local to the process that creates them.</span></span> <span data-ttu-id="de774-113">Un processus ne peut pas créer de mailslot distant.</span><span class="sxs-lookup"><span data-stu-id="de774-113">A process cannot create a remote mailslot.</span></span>

<span data-ttu-id="de774-114">Un *client mailslot* est un processus qui écrit un message sur un mailslot.</span><span class="sxs-lookup"><span data-stu-id="de774-114">A *mailslot client* is a process that writes a message to a mailslot.</span></span> <span data-ttu-id="de774-115">Tout processus qui porte le nom d’un mailslot peut y placer un message.</span><span class="sxs-lookup"><span data-stu-id="de774-115">Any process that has the name of a mailslot can put a message there.</span></span> <span data-ttu-id="de774-116">Les nouveaux messages suivent tous les messages existants dans le mailslot.</span><span class="sxs-lookup"><span data-stu-id="de774-116">New messages follow any existing messages in the mailslot.</span></span>

<span data-ttu-id="de774-117">Les mailslots peuvent diffuser des messages au sein d’un domaine.</span><span class="sxs-lookup"><span data-stu-id="de774-117">Mailslots can broadcast messages within a domain.</span></span> <span data-ttu-id="de774-118">Si plusieurs processus d’un domaine créent chacun un mailslot en utilisant le même nom, tous les messages adressés à ce mailslot et envoyés au domaine sont reçus par les processus participants.</span><span class="sxs-lookup"><span data-stu-id="de774-118">If several processes in a domain each create a mailslot using the same name, every message that is addressed to that mailslot and sent to the domain is received by the participating processes.</span></span> <span data-ttu-id="de774-119">Étant donné qu’un processus peut contrôler à la fois un handle de serveur mailslot et le descripteur du client récupéré lorsque le mailslot est ouvert pour une opération d’écriture, les applications peuvent facilement implémenter une fonctionnalité simple de transmission de messages dans un domaine.</span><span class="sxs-lookup"><span data-stu-id="de774-119">Because one process can control both a server mailslot handle and the client handle retrieved when the mailslot is opened for a write operation, applications can easily implement a simple message-passing facility within a domain.</span></span>

<span data-ttu-id="de774-120">Pour envoyer des messages d’une taille supérieure à 424 octets entre les ordinateurs, utilisez à la place des [canaux nommés](named-pipes.md) ou des [sockets Windows](/windows/desktop/WinSock/windows-sockets-start-page-2) .</span><span class="sxs-lookup"><span data-stu-id="de774-120">To send messages that are larger than 424 bytes between computers, use [named pipes](named-pipes.md) or [Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2) instead.</span></span>

## <a name="related-topics"></a><span data-ttu-id="de774-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="de774-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="de774-122">Noms des mailslot</span><span class="sxs-lookup"><span data-stu-id="de774-122">Mailslot Names</span></span>](mailslot-names.md)
</dt> <dt>

[<span data-ttu-id="de774-123">Opérations mailslot</span><span class="sxs-lookup"><span data-stu-id="de774-123">Mailslot Operations</span></span>](mailslot-operations.md)
</dt> </dl>

 

 
