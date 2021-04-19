---
description: Microsoft Digest effectue une authentification initiale lorsque le serveur reçoit la première réponse à la demande d’un client.
ms.assetid: c65bb134-d480-4a71-872c-30e2884237a6
title: Microsoft Digest Authentication
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 336d5eb9c2d114bae70c28d07ed9fef64f9d0514
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106524357"
---
# <a name="microsoft-digest-authentication"></a><span data-ttu-id="614cf-103">Microsoft Digest Authentication</span><span class="sxs-lookup"><span data-stu-id="614cf-103">Microsoft Digest Authentication</span></span>

<span data-ttu-id="614cf-104">Microsoft Digest effectue une authentification initiale lorsque le serveur reçoit la première réponse à la demande d’un client.</span><span class="sxs-lookup"><span data-stu-id="614cf-104">Microsoft Digest performs an initial authentication when the server receives the first challenge response from a client.</span></span> <span data-ttu-id="614cf-105">Le serveur vérifie que le client n’a pas été authentifié, puis effectue l’authentification initiale en accédant aux services d’un contrôleur de domaine.</span><span class="sxs-lookup"><span data-stu-id="614cf-105">The server verifies that the client has not been authenticated and then performs the initial authentication by accessing the services of a domain controller.</span></span> <span data-ttu-id="614cf-106">Pour obtenir une description détaillée de cette procédure, consultez [authentification initiale à l’aide de Microsoft Digest](initial-authentication-using-microsoft-digest.md).</span><span class="sxs-lookup"><span data-stu-id="614cf-106">For a detailed description of this procedure, see [Initial Authentication Using Microsoft Digest](initial-authentication-using-microsoft-digest.md).</span></span>

<span data-ttu-id="614cf-107">Lorsque l’authentification initiale est réussie, le serveur reçoit une [*clé de session*](../secgloss/s-gly.md)Digest.</span><span class="sxs-lookup"><span data-stu-id="614cf-107">When the initial authentication is successful the server receives a Digest [*session key*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="614cf-108">Le serveur met en cache cette clé et l’utilise pour authentifier les demandes ultérieures de ressources du client.</span><span class="sxs-lookup"><span data-stu-id="614cf-108">The server caches this key and uses it to authenticate subsequent requests for resources from the client.</span></span> <span data-ttu-id="614cf-109">Cette authentification est locale, c’est-à-dire qu’elle n’a pas besoin d’accéder à un contrôleur de domaine.</span><span class="sxs-lookup"><span data-stu-id="614cf-109">This authentication is local, that is, it does not require access to a domain controller.</span></span> <span data-ttu-id="614cf-110">Pour obtenir une description détaillée de cette procédure, consultez [authentification des demandes ultérieures à l’aide de Microsoft Digest](authenticating-subsequent-requests-using-microsoft-digest.md).</span><span class="sxs-lookup"><span data-stu-id="614cf-110">For a detailed description of this procedure see [Authenticating Subsequent Requests Using Microsoft Digest](authenticating-subsequent-requests-using-microsoft-digest.md).</span></span>

<span data-ttu-id="614cf-111">Si vous utilisez le protocole HTTP, aucune connexion n’est maintenue entre le client et le serveur.</span><span class="sxs-lookup"><span data-stu-id="614cf-111">When using HTTP, there is no connection maintained between client and server.</span></span> <span data-ttu-id="614cf-112">Pour réduire le trafic des contrôleurs de domaine et améliorer les performances, Microsoft Digest met en cache les informations reçues après une authentification réussie.</span><span class="sxs-lookup"><span data-stu-id="614cf-112">To reduce domain controller traffic and improve performance, Microsoft Digest caches information received after successful authentication.</span></span> <span data-ttu-id="614cf-113">Pour plus d’informations sur ce processus, consultez [maintenance du contexte de sécurité entre les connexions](maintaining-the-security-context-between-connections.md).</span><span class="sxs-lookup"><span data-stu-id="614cf-113">For information about this process, see [Maintaining the Security Context Between Connections](maintaining-the-security-context-between-connections.md).</span></span>

 

 
