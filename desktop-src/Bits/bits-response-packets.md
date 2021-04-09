---
title: Paquets de réponse BITS
description: Paquets de réponse BITS
ms.assetid: 30755476-daa9-42ea-8fb3-5b505fc9dd75
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 755e28b749d201a2c90640ea9e456f012f790453
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839369"
---
# <a name="bits-response-packets"></a><span data-ttu-id="43da2-103">Paquets de réponse BITS</span><span class="sxs-lookup"><span data-stu-id="43da2-103">BITS Response Packets</span></span>

<span data-ttu-id="43da2-104">Le tableau suivant répertorie les paquets de réponse envoyés au client BITS pour les travaux de chargement et de chargement-réponse.</span><span class="sxs-lookup"><span data-stu-id="43da2-104">The following table lists the response packets sent to the BITS client for upload and upload-reply jobs.</span></span> <span data-ttu-id="43da2-105">Le tableau répertorie les paquets dans la séquence type qu’ils envoient au client.</span><span class="sxs-lookup"><span data-stu-id="43da2-105">The table lists the packets in the typical sequence they are sent to the client.</span></span>



| <span data-ttu-id="43da2-106">Paquet de réponse</span><span class="sxs-lookup"><span data-stu-id="43da2-106">Response packet</span></span>                                      | <span data-ttu-id="43da2-107">Objectif</span><span class="sxs-lookup"><span data-stu-id="43da2-107">Purpose</span></span>                                                                                                                                                                                     |
|------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="43da2-108">ACK pour ping</span><span class="sxs-lookup"><span data-stu-id="43da2-108">Ack for Ping</span></span>](ack-for-ping.md)                     | <span data-ttu-id="43da2-109">Accuse réception de la demande [ping](ping.md) .</span><span class="sxs-lookup"><span data-stu-id="43da2-109">Acknowledges the [Ping](ping.md) request.</span></span>                                                                                                                                                  |
| [<span data-ttu-id="43da2-110">ACK pour Create-session</span><span class="sxs-lookup"><span data-stu-id="43da2-110">Ack for Create-Session</span></span>](ack-for-create-session.md) | <span data-ttu-id="43da2-111">Accuse réception de la demande de [création de session](create-session.md) et retourne un identificateur de session que le client bits utilise sur toutes les demandes suivantes pour identifier cette session de transfert de fichiers.</span><span class="sxs-lookup"><span data-stu-id="43da2-111">Acknowledges the [Create-Session](create-session.md) request and returns a session identifier that the BITS client uses on all subsequent requests to identify this file transfer session.</span></span> |
| [<span data-ttu-id="43da2-112">ACK pour fragment</span><span class="sxs-lookup"><span data-stu-id="43da2-112">Ack for Fragment</span></span>](ack-for-fragment.md)             | <span data-ttu-id="43da2-113">Accuse réception de la demande de [fragment](fragment.md) et écrit le fragment dans le fichier de téléchargement sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="43da2-113">Acknowledges the [Fragment](fragment.md) request and writes the fragment to the upload file on the server.</span></span>                                                                                 |
| [<span data-ttu-id="43da2-114">ACK pour Close-session</span><span class="sxs-lookup"><span data-stu-id="43da2-114">Ack for Close-Session</span></span>](ack-for-close-session.md)   | <span data-ttu-id="43da2-115">Accuse réception de la demande de [fermeture de session](close-session.md) et libère toutes les ressources associées à la session.</span><span class="sxs-lookup"><span data-stu-id="43da2-115">Acknowledges the [Close-Session](close-session.md) request and releases all resources associated with the session.</span></span>                                                                         |
| [<span data-ttu-id="43da2-116">ACK pour Cancel-session</span><span class="sxs-lookup"><span data-stu-id="43da2-116">Ack for Cancel-Session</span></span>](ack-for-cancel-session.md) | <span data-ttu-id="43da2-117">Accuse réception de la demande d' [annulation de session](cancel-session.md) et libère toutes les ressources associées à la session.</span><span class="sxs-lookup"><span data-stu-id="43da2-117">Acknowledges the [Cancel-Session](cancel-session.md) request and releases all resources associated with the session.</span></span>                                                                       |



 

 

 




