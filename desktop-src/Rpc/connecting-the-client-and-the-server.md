---
title: Connexion du client et du serveur
description: Pour communiquer, les programmes clients et serveurs doivent établir une session de communication sur le réseau ou les réseaux qui les connectent.
ms.assetid: 1164252a-7615-4958-9d2f-cf35c0db513a
keywords:
- Appel de procédure distante RPC, tâches, connexion du client et du serveur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98a22ea7a9a6dd30f2b9495b6d2ee868aac217f0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462282"
---
# <a name="connecting-the-client-and-the-server"></a><span data-ttu-id="9019e-104">Connexion du client et du serveur</span><span class="sxs-lookup"><span data-stu-id="9019e-104">Connecting the Client and the Server</span></span>

<span data-ttu-id="9019e-105">Pour communiquer, les programmes clients et serveurs doivent établir une session de communication sur le réseau ou les réseaux qui les connectent.</span><span class="sxs-lookup"><span data-stu-id="9019e-105">To communicate, client and server programs must establish a communication session across the network or networks that connect them.</span></span> <span data-ttu-id="9019e-106">Une fois la connexion établie, le client peut appeler des procédures distantes dans le programme serveur comme si elles étaient locales pour le programme client.</span><span class="sxs-lookup"><span data-stu-id="9019e-106">Once they establish the connection, the client can call remote procedures in the server program as if they were local to the client program.</span></span>

<span data-ttu-id="9019e-107">Cette section fournit une vue d’ensemble conceptuelle de l’établissement d’une connexion entre les clients et les serveurs pour les appels de procédure distante.</span><span class="sxs-lookup"><span data-stu-id="9019e-107">This section provides a conceptual overview of how to establish a connection between clients and servers for remote procedure calls.</span></span> <span data-ttu-id="9019e-108">Il ne fournit pas de description détaillée de cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="9019e-108">It does not provide an in-depth discussion of this topic.</span></span> <span data-ttu-id="9019e-109">Tous les concepts de cette section sont présentés en détail dans les chapitres ultérieurs et dans la section Référence des fonctions RPC.</span><span class="sxs-lookup"><span data-stu-id="9019e-109">All of the concepts in this section are presented in detail in later chapters and in the RPC Function Reference section.</span></span>

<span data-ttu-id="9019e-110">La discussion présentée dans cette section est composée des rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="9019e-110">The discussion presented in this section is divided into the following topics:</span></span>

-   [<span data-ttu-id="9019e-111">Terminologie des liaisons RPC essentielles</span><span class="sxs-lookup"><span data-stu-id="9019e-111">Essential RPC Binding Terminology</span></span>](essential-rpc-binding-terminology.md)
-   [<span data-ttu-id="9019e-112">Préparation d’une connexion par le serveur</span><span class="sxs-lookup"><span data-stu-id="9019e-112">How the Server Prepares for a Connection</span></span>](how-the-server-prepares-for-a-connection.md)
-   [<span data-ttu-id="9019e-113">Comment le client établit une connexion</span><span class="sxs-lookup"><span data-stu-id="9019e-113">How the Client Establishes a Connection</span></span>](how-the-client-establishes-a-connection.md)

<span data-ttu-id="9019e-114">Notez que la discussion suppose des handles de liaison explicites.</span><span class="sxs-lookup"><span data-stu-id="9019e-114">Note that the discussion assumes explicit binding handles.</span></span> <span data-ttu-id="9019e-115">Toutefois, si votre application utilise d’autres types de descripteurs de liaison, vous devrez peut-être modifier les étapes présentées dans cette section.</span><span class="sxs-lookup"><span data-stu-id="9019e-115">However, if your application uses other types of binding handles, you may have to modify the steps presented in this section.</span></span> <span data-ttu-id="9019e-116">Pour plus d’informations, consultez [liaison et Handles](binding-and-handles.md).</span><span class="sxs-lookup"><span data-stu-id="9019e-116">For more information, see [Binding and Handles](binding-and-handles.md).</span></span>

 

 




