---
title: Protocole de téléchargement BITS
description: Cette section décrit le protocole réseau pour les types de tâches chargement BITS et chargement-réponse.
ms.assetid: d0706ab1-1bf4-4b17-9321-ec3e00dd25e2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 642426decd0bc37390fa9fdd9b1ad2be11a0aa84
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671629"
---
# <a name="bits-upload-protocol"></a><span data-ttu-id="a5a8f-103">Protocole de téléchargement BITS</span><span class="sxs-lookup"><span data-stu-id="a5a8f-103">BITS Upload Protocol</span></span>

<span data-ttu-id="a5a8f-104">Cette section décrit le protocole réseau pour les types de tâches chargement BITS et chargement-réponse.</span><span class="sxs-lookup"><span data-stu-id="a5a8f-104">This section describes the network protocol for BITS upload and upload-reply job types.</span></span> <span data-ttu-id="a5a8f-105">Le protocole de téléchargement BITS est superposé sur HTTP 1,1 et utilise un grand nombre d’en-têtes HTTP existants et définit de nouveaux en-têtes.</span><span class="sxs-lookup"><span data-stu-id="a5a8f-105">The BITS upload protocol is layered on top of HTTP 1.1 and uses many of the existing HTTP headers and defines new headers.</span></span> <span data-ttu-id="a5a8f-106">Le protocole de téléchargement BITS prend en charge un seul fichier de téléchargement par session.</span><span class="sxs-lookup"><span data-stu-id="a5a8f-106">The BITS upload protocol supports a single upload file per session.</span></span>

<span data-ttu-id="a5a8f-107">BITS utilise des paquets pour décrire les demandes du client et les réponses du serveur.</span><span class="sxs-lookup"><span data-stu-id="a5a8f-107">BITS uses packets to describe client requests and server responses.</span></span> <span data-ttu-id="a5a8f-108">L’en-tête BITS-Packet-type spécifie le type de paquet envoyé.</span><span class="sxs-lookup"><span data-stu-id="a5a8f-108">The BITS-Packet-Type header specifies the type of packet being sent.</span></span> <span data-ttu-id="a5a8f-109">Chaque paquet contient des en-têtes spécifiques.</span><span class="sxs-lookup"><span data-stu-id="a5a8f-109">Each packet contains specific headers.</span></span> <span data-ttu-id="a5a8f-110">BITS utilise le \_ verbe de publication bits pour identifier les paquets de chargement bits.</span><span class="sxs-lookup"><span data-stu-id="a5a8f-110">BITS uses the BITS\_POST verb to identify BITS upload packets.</span></span> <span data-ttu-id="a5a8f-111">Les paquets de réponse utilisent toujours le type de paquet ACK qui correspond à la reconnaissance.</span><span class="sxs-lookup"><span data-stu-id="a5a8f-111">Response packets always use the Ack packet type which stands for acknowledge.</span></span> <span data-ttu-id="a5a8f-112">Le paquet ACK est envoyé dans le contexte de la demande précédente ; il ne peut y avoir qu’une seule demande en suspens à la fois.</span><span class="sxs-lookup"><span data-stu-id="a5a8f-112">The Ack packet is sent in the context of the previous request; there can be only one outstanding request at one time.</span></span>

<span data-ttu-id="a5a8f-113">Pour les travaux de chargement-réponse, BITS utilise ce protocole pour télécharger le fichier, mais n’utilise pas ce protocole pour envoyer la réponse au client.</span><span class="sxs-lookup"><span data-stu-id="a5a8f-113">For upload-reply jobs, BITS uses this protocol to upload the file but does not use this protocol to send the reply to the client.</span></span> <span data-ttu-id="a5a8f-114">Au lieu de cela, le serveur BITS envoie l’emplacement du fichier de réponse au client et le client crée un travail de téléchargement BITS pour télécharger le fichier de réponse.</span><span class="sxs-lookup"><span data-stu-id="a5a8f-114">Instead, the BITS server sends the location of the reply file to the client and the client creates a BITS download job to download the reply file.</span></span>

<span data-ttu-id="a5a8f-115">Utilisez le protocole de téléchargement pour remplacer le logiciel client ou serveur BITS par votre propre implémentation.</span><span class="sxs-lookup"><span data-stu-id="a5a8f-115">Use the upload protocol to replace the BITS client or server software with your own implementation.</span></span> <span data-ttu-id="a5a8f-116">Pour obtenir la liste des paquets de demande envoyés par le client BITS, consultez [paquets de demande bits](bits-request-packets.md).</span><span class="sxs-lookup"><span data-stu-id="a5a8f-116">For a list of request packets sent by the BITS client, see [BITS Request Packets](bits-request-packets.md).</span></span> <span data-ttu-id="a5a8f-117">Pour obtenir la liste des paquets de réponse envoyés par le serveur BITS, consultez [paquets de réponse bits](bits-response-packets.md).</span><span class="sxs-lookup"><span data-stu-id="a5a8f-117">For a list of response packets sent by the BITS server, see [BITS Response Packets](bits-response-packets.md).</span></span>

<span data-ttu-id="a5a8f-118">Le client détermine comment il répond aux erreurs ou aux paquets inattendus du serveur BITS.</span><span class="sxs-lookup"><span data-stu-id="a5a8f-118">The client determines how it responds to errors or unexpected packets from the BITS server.</span></span> <span data-ttu-id="a5a8f-119">Si le serveur reçoit un paquet qui ne s’attend pas, le serveur doit envoyer un paquet ACK avec un code de retour 400 (demande incorrecte).</span><span class="sxs-lookup"><span data-stu-id="a5a8f-119">If the server receives a packet that it does not expect, the server should send an Ack packet with a 400 (Bad Request) return code.</span></span>

 

 




