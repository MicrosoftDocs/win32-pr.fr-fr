---
title: Paquets de demande BITS
description: Paquets de demande BITS
ms.assetid: 4d8fd5f3-7621-438f-926f-38ece7a52f52
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6738f77477342f1329818ae7c2ffb5c010b074c3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103939713"
---
# <a name="bits-request-packets"></a><span data-ttu-id="6cca1-103">Paquets de demande BITS</span><span class="sxs-lookup"><span data-stu-id="6cca1-103">BITS Request Packets</span></span>

<span data-ttu-id="6cca1-104">Les paquets de demande décrivent les demandes des clients.</span><span class="sxs-lookup"><span data-stu-id="6cca1-104">Request packets describe client requests.</span></span> <span data-ttu-id="6cca1-105">Il ne peut y avoir qu’une seule demande en suspens à un moment donné. vous devez recevoir un [accusé](bits-response-packets.md) de réception pour la demande en cours à partir du serveur avant d’envoyer une autre demande.</span><span class="sxs-lookup"><span data-stu-id="6cca1-105">There can be only one outstanding request at any given time; you must receive an [Ack](bits-response-packets.md) for the current request from the server before sending another request.</span></span>

<span data-ttu-id="6cca1-106">Le tableau suivant répertorie les paquets de demande envoyés au serveur BITS pour les travaux de chargement et de chargement-réponse.</span><span class="sxs-lookup"><span data-stu-id="6cca1-106">The following table lists the request packets sent to the BITS server for upload and upload-reply jobs.</span></span> <span data-ttu-id="6cca1-107">Le tableau répertorie les paquets dans la séquence type qu’ils envoient au serveur.</span><span class="sxs-lookup"><span data-stu-id="6cca1-107">The table lists the packets in the typical sequence they are sent to the server.</span></span>



| <span data-ttu-id="6cca1-108">Paquet de demande</span><span class="sxs-lookup"><span data-stu-id="6cca1-108">Request packet</span></span>                       | <span data-ttu-id="6cca1-109">Objectif</span><span class="sxs-lookup"><span data-stu-id="6cca1-109">Purpose</span></span>                                                                                                                                                        |
|--------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6cca1-110">Ping</span><span class="sxs-lookup"><span data-stu-id="6cca1-110">Ping</span></span>](ping.md)                     | <span data-ttu-id="6cca1-111">Établit une connexion et négocie la sécurité avec le serveur.</span><span class="sxs-lookup"><span data-stu-id="6cca1-111">Establishes a connection and negotiates security with the server.</span></span>                                                                                              |
| [<span data-ttu-id="6cca1-112">Créer une session</span><span class="sxs-lookup"><span data-stu-id="6cca1-112">Create-Session</span></span>](create-session.md) | <span data-ttu-id="6cca1-113">Demande une session de chargement avec le serveur BITS.</span><span class="sxs-lookup"><span data-stu-id="6cca1-113">Requests an upload session with the BITS server.</span></span>                                                                                                               |
| [<span data-ttu-id="6cca1-114">Fragment</span><span class="sxs-lookup"><span data-stu-id="6cca1-114">Fragment</span></span>](fragment.md)             | <span data-ttu-id="6cca1-115">Envoie un fragment du fichier au serveur BITS.</span><span class="sxs-lookup"><span data-stu-id="6cca1-115">Sends a fragment of the file to the BITS server.</span></span> <span data-ttu-id="6cca1-116">Le nombre de requêtes de fragment envoyées dépend de la taille de fragment que vous choisissez et de la taille du fichier de téléchargement.</span><span class="sxs-lookup"><span data-stu-id="6cca1-116">The number of fragment requests sent depends on the fragment size you choose and the size of the upload file.</span></span> |
| [<span data-ttu-id="6cca1-117">Fermer-session</span><span class="sxs-lookup"><span data-stu-id="6cca1-117">Close-Session</span></span>](close-session.md)   | <span data-ttu-id="6cca1-118">Met fin à la session de chargement de fichier avec le serveur BITS.</span><span class="sxs-lookup"><span data-stu-id="6cca1-118">Ends the file upload session with the BITS server.</span></span>                                                                                                             |
| [<span data-ttu-id="6cca1-119">Annuler-session</span><span class="sxs-lookup"><span data-stu-id="6cca1-119">Cancel-Session</span></span>](cancel-session.md) | <span data-ttu-id="6cca1-120">Met fin à la session de chargement de fichier avec le serveur BITS.</span><span class="sxs-lookup"><span data-stu-id="6cca1-120">Ends the file upload session with the BITS server.</span></span> <span data-ttu-id="6cca1-121">En règle générale, vous envoyez le paquet Cancel-Session si l’utilisateur a annulé le travail.</span><span class="sxs-lookup"><span data-stu-id="6cca1-121">Typically, you send the Cancel-Session packet if the user canceled the job.</span></span>                                 |



 

<span data-ttu-id="6cca1-122">Le paquet ping est facultatif.</span><span class="sxs-lookup"><span data-stu-id="6cca1-122">The Ping packet is optional.</span></span> <span data-ttu-id="6cca1-123">Au lieu d’envoyer un paquet ping, vous pouvez utiliser le paquet Create-Session pour établir une connexion et négocier la sécurité.</span><span class="sxs-lookup"><span data-stu-id="6cca1-123">Instead of sending a Ping packet, you can use the Create-Session packet to establish a connection and negotiate security.</span></span> <span data-ttu-id="6cca1-124">Toutefois, il est plus efficace d’utiliser le paquet ping à cet effet.</span><span class="sxs-lookup"><span data-stu-id="6cca1-124">However, it is more efficient to use the Ping packet for this purpose.</span></span>

 

 




