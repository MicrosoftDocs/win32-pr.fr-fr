---
description: Dans un modèle d’application client/serveur, les clients sont des programmes agissant pour le compte des utilisateurs qui ont besoin d’une opération.
ms.assetid: c3e38cd3-3749-4384-80ff-0551acfe1eec
title: Concepts d’authentification de base
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 723cf42913906435c8dbc3c41950da8db8ece0ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114314"
---
# <a name="basic-authentication-concepts"></a><span data-ttu-id="1d6c8-103">Concepts d’authentification de base</span><span class="sxs-lookup"><span data-stu-id="1d6c8-103">Basic Authentication Concepts</span></span>

<span data-ttu-id="1d6c8-104">Dans un modèle d’application client/serveur, les clients sont des programmes agissant pour le compte des utilisateurs qui ont besoin d’une opération.</span><span class="sxs-lookup"><span data-stu-id="1d6c8-104">In a client/server application model, clients are programs acting on behalf of users who need something done.</span></span> <span data-ttu-id="1d6c8-105">Cela peut consister à ouvrir et à utiliser un fichier, à accéder à une boîte aux lettres, à interroger une base de données ou à imprimer un document.</span><span class="sxs-lookup"><span data-stu-id="1d6c8-105">This might be opening and using a file, accessing a mailbox, querying a database, or printing a document.</span></span> <span data-ttu-id="1d6c8-106">Les serveurs sont des programmes qui fournissent des services aux clients, tels que le stockage de fichiers, la gestion des messages, le traitement des requêtes et la mise en attente d’impression.</span><span class="sxs-lookup"><span data-stu-id="1d6c8-106">Servers are programs providing services to clients such as file storage, mail handling, query processing, and print spooling.</span></span> <span data-ttu-id="1d6c8-107">Actions initiées par les clients, les serveurs répondent.</span><span class="sxs-lookup"><span data-stu-id="1d6c8-107">Clients initiate action, servers respond.</span></span> <span data-ttu-id="1d6c8-108">En règle générale, un serveur est à l’écoute d’un port de communication en attente de la connexion des clients et de la demande de service.</span><span class="sxs-lookup"><span data-stu-id="1d6c8-108">Typically, a server listens at a communications port waiting for clients to connect and ask for service.</span></span>

<span data-ttu-id="1d6c8-109">Dans le modèle de protocole Kerberos, chaque connexion client/serveur commence par l'authentification.</span><span class="sxs-lookup"><span data-stu-id="1d6c8-109">In the Kerberos protocol model, every client/server connection begins with authentication.</span></span> <span data-ttu-id="1d6c8-110">L'un après l'autre, le client et le serveur passent par une séquence d'actions visant à vérifier l'authenticité de la partie située à l'extrémité opposée de la connexion.</span><span class="sxs-lookup"><span data-stu-id="1d6c8-110">Client and server, in turn, step through a sequence of actions designed to verify to the party on each end of the connection that the party on the other end is genuine.</span></span> <span data-ttu-id="1d6c8-111">Si l'authentification réussit, la configuration de la session est effectuée et une session client/serveur sécurisée est établie.</span><span class="sxs-lookup"><span data-stu-id="1d6c8-111">If authentication is successful, session setup completes and a secure client/server session is established.</span></span>

<span data-ttu-id="1d6c8-112">Le protocole Kerberos utilise les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="1d6c8-112">The Kerberos protocol makes use of:</span></span>

-   [<span data-ttu-id="1d6c8-113">Authentification par clé</span><span class="sxs-lookup"><span data-stu-id="1d6c8-113">Key authentication</span></span>](key-authentication.md)
-   [<span data-ttu-id="1d6c8-114">Messages de l’authentificateur</span><span class="sxs-lookup"><span data-stu-id="1d6c8-114">Authenticator messages</span></span>](authenticator-messages.md)
-   [<span data-ttu-id="1d6c8-115">Distribution de clés</span><span class="sxs-lookup"><span data-stu-id="1d6c8-115">Key distribution</span></span>](key-distribution.md)
-   [<span data-ttu-id="1d6c8-116">Tickets de session</span><span class="sxs-lookup"><span data-stu-id="1d6c8-116">Session tickets</span></span>](session-tickets.md)
-   [<span data-ttu-id="1d6c8-117">Tickets d’accord de tickets</span><span class="sxs-lookup"><span data-stu-id="1d6c8-117">Ticket-granting tickets</span></span>](ticket-granting-tickets.md)

 

 



