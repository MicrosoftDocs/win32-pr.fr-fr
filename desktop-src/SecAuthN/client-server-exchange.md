---
description: Échange client/serveur
ms.assetid: 2449c4b3-720d-4b84-b3cf-fcc4abd05d33
title: Échange client/serveur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6274705ef6719c846f0551f90fca8790ba89f2e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114943"
---
# <a name="clientserver-exchange"></a><span data-ttu-id="ca09f-103">Échange client/serveur</span><span class="sxs-lookup"><span data-stu-id="ca09f-103">Client/Server Exchange</span></span>

<span data-ttu-id="ca09f-104">Une fois qu’un utilisateur a un ticket vers un serveur, le client de station de travail peut établir une session de communication sécurisée avec ce serveur.</span><span class="sxs-lookup"><span data-stu-id="ca09f-104">After a user has a ticket to a server, the workstation client can establish a secure communications session with that server.</span></span>

<span data-ttu-id="ca09f-105">**Pour établir une session de communication sécurisée avec un serveur**</span><span class="sxs-lookup"><span data-stu-id="ca09f-105">**To establish a secure communications session with a server**</span></span>

1.  <span data-ttu-id="ca09f-106">Le client envoie au serveur un message de type KRB \_ AP \_ req (demande d’application Kerberos).</span><span class="sxs-lookup"><span data-stu-id="ca09f-106">The client sends the server a message of type KRB\_AP\_REQ (Kerberos Application Request).</span></span> <span data-ttu-id="ca09f-107">Ce message contient un message d’authentificateur chiffré avec la clé envoyée par le [*Centre de distribution de clés*](/windows/desktop/SecGloss/k-gly) (KDC) pour la session avec le serveur, le ticket pour les sessions avec le serveur et un indicateur qui indique si le client demande une authentification mutuelle.</span><span class="sxs-lookup"><span data-stu-id="ca09f-107">This message contains an authenticator message that is encrypted with the key sent by the [*Key Distribution Center*](/windows/desktop/SecGloss/k-gly) (KDC) for the session with the server, the ticket for sessions with the server, and a flag that indicates whether the client requests mutual authentication.</span></span> <span data-ttu-id="ca09f-108">La définition de l’indicateur qui demande l’authentification mutuelle est l’une des options de configuration de [*Kerberos*](/windows/desktop/SecGloss/k-gly).</span><span class="sxs-lookup"><span data-stu-id="ca09f-108">Setting the flag that requests mutual authentication is one of the options in configuring [*Kerberos*](/windows/desktop/SecGloss/k-gly).</span></span> <span data-ttu-id="ca09f-109">L’utilisateur n’est jamais invité à utiliser l’authentification mutuelle.</span><span class="sxs-lookup"><span data-stu-id="ca09f-109">The user is never asked whether mutual authentication should be used.</span></span>
2.  <span data-ttu-id="ca09f-110">Le serveur reçoit une \_ demande KRB AP \_ , déchiffre le ticket, puis extrait les données d’autorisation de l’utilisateur et la [*clé de session*](/windows/desktop/SecGloss/s-gly).</span><span class="sxs-lookup"><span data-stu-id="ca09f-110">The server receives KRB\_AP\_REQ, decrypts the ticket, and extracts the user's authorization data and the [*session key*](/windows/desktop/SecGloss/s-gly).</span></span>
3.  <span data-ttu-id="ca09f-111">Le serveur utilise la clé de session du ticket pour déchiffrer le message de l’authentificateur de l’utilisateur et évalue l’horodatage à l’intérieur de.</span><span class="sxs-lookup"><span data-stu-id="ca09f-111">The server uses the session key from the ticket to decrypt the user's authenticator message and evaluates the time stamp inside.</span></span>
4.  <span data-ttu-id="ca09f-112">Si le message de l’authentificateur est valide, le serveur vérifie l’indicateur d’authentification mutuelle dans la demande du client.</span><span class="sxs-lookup"><span data-stu-id="ca09f-112">If the authenticator message is valid, the server checks the mutual authentication flag in the client's request.</span></span>
5.  <span data-ttu-id="ca09f-113">Si l’indicateur d’authentification mutuelle est défini, le serveur utilise la clé de session pour chiffrer l’heure à partir du message de l’authentificateur de l’utilisateur et retourne le résultat dans un message de type KRB \_ AP \_ Rep (réponse de l’application Kerberos).</span><span class="sxs-lookup"><span data-stu-id="ca09f-113">If the mutual authentication flag is set, the server uses the session key to encrypt the time from the user's authenticator message and returns the result in a message of type KRB\_AP\_REP (Kerberos Application Reply).</span></span>
6.  <span data-ttu-id="ca09f-114">Lorsque le client reçoit un \_ \_ REP AP, il déchiffre le message de l’authentificateur du serveur avec la clé de session qu’il partage avec le serveur et compare l’heure renvoyée par le service à l’heure de son message d’authentificateur d’origine.</span><span class="sxs-lookup"><span data-stu-id="ca09f-114">When the client receives KRB\_AP\_REP, it decrypts the server's authenticator message with the session key it shares with the server and compares the time sent back by the service with the time in its original authenticator message.</span></span> <span data-ttu-id="ca09f-115">S’ils correspondent, le client est assuré que le service est authentique et que la connexion se poursuit.</span><span class="sxs-lookup"><span data-stu-id="ca09f-115">If they match, the client is assured that the service is genuine, and the connection proceeds.</span></span>

 

 
