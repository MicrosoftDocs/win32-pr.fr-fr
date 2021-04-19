---
description: Une fois qu’un ticket TGT (Ticket-Granting Ticket) et une clé de session ont été établis pour le client, le client peut demander une clé de session et un ticket distincts pour le service.
ms.assetid: b4f63642-9282-4e11-b40c-eec406b2dd2b
title: Échange de service TG (ticket-granting)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3b227ee551d762abd145ca56c6cced110b6a2dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106529758"
---
# <a name="ticket-granting-service-exchange"></a><span data-ttu-id="57a6a-103">Échange de service TG (ticket-granting)</span><span class="sxs-lookup"><span data-stu-id="57a6a-103">Ticket-Granting Service Exchange</span></span>

<span data-ttu-id="57a6a-104">Une fois qu’un ticket TGT (Ticket-Granting Ticket) et une [*clé de session*](../secgloss/s-gly.md) ont été établis pour le client, le client peut demander une clé de session et un ticket distincts pour le service.</span><span class="sxs-lookup"><span data-stu-id="57a6a-104">After a ticket-granting ticket (TGT) and [*session key*](../secgloss/s-gly.md) have been established for the client, the client can request a separate session key and ticket for the service.</span></span>

<span data-ttu-id="57a6a-105">**Pour demander un ticket pour un autre service**</span><span class="sxs-lookup"><span data-stu-id="57a6a-105">**To request a ticket for another service**</span></span>

1.  <span data-ttu-id="57a6a-106">Le client Kerberos sur la station de travail de l’utilisateur demande des [*informations d’identification*](../secgloss/c-gly.md) pour le service en envoyant au [*Centre de distribution de clés*](../secgloss/k-gly.md) (KDC) un message de type KRB \_ TGS \_ REQ (demande de service de Ticket-Granting Kerberos).</span><span class="sxs-lookup"><span data-stu-id="57a6a-106">The Kerberos client on the user's workstation requests [*credentials*](../secgloss/c-gly.md) for the service by sending, to the [*Key Distribution Center*](../secgloss/k-gly.md) (KDC), a message of type KRB\_TGS\_REQ (Kerberos Ticket-Granting Service Request).</span></span> <span data-ttu-id="57a6a-107">Ce message est constitué de l’identité du service pour lequel le client demande des informations d’identification, d’un message d’authentificateur chiffré avec la nouvelle [*clé de session*](../secgloss/s-gly.md)de connexion de l’utilisateur et du TGT obtenu auprès de l' [échange du service d’authentification](authentication-service-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="57a6a-107">This message consists of the identity of the service for which the client is requesting credentials, an authenticator message encrypted with the user's new logon [*session key*](../secgloss/s-gly.md), and the TGT obtained from the [Authentication Service Exchange](authentication-service-exchange.md).</span></span>
2.  <span data-ttu-id="57a6a-108">Lorsque le KDC reçoit une \_ demande TGS de KRB \_ , le KDC déchiffre le ticket TGT avec sa clé secrète et extrait la clé de session de connexion de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="57a6a-108">When the KDC receives a KRB\_TGS\_REQ, the KDC decrypts the TGT with its secret key and extracts the user's logon session key.</span></span>
3.  <span data-ttu-id="57a6a-109">Le KDC utilise la [*clé de session*](../secgloss/s-gly.md) de connexion pour déchiffrer le message de l’authentificateur de l’utilisateur et l’évalue.</span><span class="sxs-lookup"><span data-stu-id="57a6a-109">The KDC uses the logon [*session key*](../secgloss/s-gly.md) to decrypt the user's authenticator message and evaluates it.</span></span> <span data-ttu-id="57a6a-110">Si l’authentificateur réussit le test, le KDC extrait les données d’autorisation de l’utilisateur à partir du TGT et invente une clé de session à partager avec le serveur demandé.</span><span class="sxs-lookup"><span data-stu-id="57a6a-110">If the authenticator passes the test, the KDC extracts the user's authorization data from the TGT and invents a session key for the user to share with the requested server.</span></span>
4.  <span data-ttu-id="57a6a-111">Le KDC chiffre une copie de la clé de session de service avec la clé de session de connexion de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="57a6a-111">The KDC encrypts one copy of the service session key with the user's logon session key.</span></span>
5.  <span data-ttu-id="57a6a-112">Le KDC incorpore une autre copie de la clé de session de service dans un ticket, avec les données d’autorisation de l’utilisateur, et chiffre le ticket avec la [*clé principale*](../secgloss/m-gly.md)du serveur.</span><span class="sxs-lookup"><span data-stu-id="57a6a-112">The KDC embeds another copy of the service session key in a ticket, along with the user's authorization data, and encrypts the ticket with the server's [*master key*](../secgloss/m-gly.md).</span></span>
6.  <span data-ttu-id="57a6a-113">Le KDC renvoie ces informations d’identification au client en répondant à l’aide d’un message de type KRB \_ TGS \_ Rep (Kerberos Ticket-Granting service Reply).</span><span class="sxs-lookup"><span data-stu-id="57a6a-113">The KDC sends these credentials back to the client by replying with a message of type KRB\_TGS\_REP (Kerberos Ticket-Granting Service Reply).</span></span>
7.  <span data-ttu-id="57a6a-114">Lorsque le client reçoit la réponse, il déchiffre la clé de session de service avec la clé de session de connexion de l’utilisateur et stocke la clé de session de service dans son cache de tickets.</span><span class="sxs-lookup"><span data-stu-id="57a6a-114">When the client receives the reply, it decrypts the service session key with the user's logon session key and stores the service session key in its ticket cache.</span></span>
8.  <span data-ttu-id="57a6a-115">Le client extrait le ticket sur le serveur et le stocke dans son cache de tickets.</span><span class="sxs-lookup"><span data-stu-id="57a6a-115">The client extracts the ticket to the server and stores that in its ticket cache.</span></span>

 

 
