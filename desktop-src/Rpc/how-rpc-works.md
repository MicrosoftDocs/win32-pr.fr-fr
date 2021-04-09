---
title: Fonctionnement de RPC
description: Les outils RPC s’affichent pour les utilisateurs comme si un client appelle directement une procédure située dans un programme serveur distant.
ms.assetid: 265f31b8-9a41-4255-b070-fd50b00b935b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12832d0de4eb972bb1d9d51df0c871191d4d079a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103674089"
---
# <a name="how-rpc-works"></a><span data-ttu-id="a6697-103">Fonctionnement de RPC</span><span class="sxs-lookup"><span data-stu-id="a6697-103">How RPC Works</span></span>

<span data-ttu-id="a6697-104">Les outils RPC s’affichent pour les utilisateurs comme si un client appelle directement une procédure située dans un programme serveur distant.</span><span class="sxs-lookup"><span data-stu-id="a6697-104">The RPC tools make it appear to users as though a client directly calls a procedure located in a remote server program.</span></span> <span data-ttu-id="a6697-105">Le client et le serveur ont chacun leurs propres espaces d’adressage ; autrement dit, chaque a sa propre ressource mémoire allouée aux données utilisées par la procédure.</span><span class="sxs-lookup"><span data-stu-id="a6697-105">The client and server each have their own address spaces; that is, each has its own memory resource allocated to data used by the procedure.</span></span> <span data-ttu-id="a6697-106">La figure ci-dessous illustre l’architecture RPC.</span><span class="sxs-lookup"><span data-stu-id="a6697-106">The following figure illustrates the RPC architecture.</span></span>

![architecture RPC](images/prog-a11.png)

<span data-ttu-id="a6697-108">Comme le montre l’illustration, l’application cliente appelle une procédure stub locale au lieu du code réel qui implémente la procédure.</span><span class="sxs-lookup"><span data-stu-id="a6697-108">As the illustration shows, the client application calls a local stub procedure instead of the actual code implementing the procedure.</span></span> <span data-ttu-id="a6697-109">Les stubs sont compilés et liés à l’application cliente.</span><span class="sxs-lookup"><span data-stu-id="a6697-109">Stubs are compiled and linked with the client application.</span></span> <span data-ttu-id="a6697-110">Au lieu de contenir le code réel qui implémente la procédure distante, le code stub du client :</span><span class="sxs-lookup"><span data-stu-id="a6697-110">Instead of containing the actual code that implements the remote procedure, the client stub code:</span></span>

-   <span data-ttu-id="a6697-111">Récupère les paramètres requis à partir de l’espace d’adressage du client.</span><span class="sxs-lookup"><span data-stu-id="a6697-111">Retrieves the required parameters from the client address space.</span></span>
-   <span data-ttu-id="a6697-112">Traduit les paramètres en fonction des besoins dans un format de rapport de non-remise standard pour la transmission sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="a6697-112">Translates the parameters as needed into a standard NDR format for transmission over the network.</span></span>
-   <span data-ttu-id="a6697-113">Appelle des fonctions dans la bibliothèque Runtime du client RPC pour envoyer la demande et ses paramètres au serveur.</span><span class="sxs-lookup"><span data-stu-id="a6697-113">Calls functions in the RPC client run-time library to send the request and its parameters to the server.</span></span>

<span data-ttu-id="a6697-114">Le serveur effectue les étapes suivantes pour appeler la procédure distante.</span><span class="sxs-lookup"><span data-stu-id="a6697-114">The server performs the following steps to call the remote procedure.</span></span>

1.  <span data-ttu-id="a6697-115">Les fonctions de la bibliothèque Runtime RPC du serveur acceptent la demande et appellent la procédure stub du serveur.</span><span class="sxs-lookup"><span data-stu-id="a6697-115">The server RPC run-time library functions accept the request and call the server stub procedure.</span></span>
2.  <span data-ttu-id="a6697-116">Le stub serveur récupère les paramètres à partir de la mémoire tampon réseau et les convertit du format de transmission réseau au format requis par le serveur.</span><span class="sxs-lookup"><span data-stu-id="a6697-116">The server stub retrieves the parameters from the network buffer and converts them from the network transmission format to the format the server needs.</span></span>
3.  <span data-ttu-id="a6697-117">Le stub serveur appelle la procédure réelle sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="a6697-117">The server stub calls the actual procedure on the server.</span></span>

<span data-ttu-id="a6697-118">La procédure distante s’exécute, générant éventuellement des paramètres de sortie et une valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="a6697-118">The remote procedure then runs, possibly generating output parameters and a return value.</span></span> <span data-ttu-id="a6697-119">Une fois la procédure distante terminée, une séquence d’étapes similaire retourne les données au client.</span><span class="sxs-lookup"><span data-stu-id="a6697-119">When the remote procedure is complete, a similar sequence of steps returns the data to the client.</span></span>

1.  <span data-ttu-id="a6697-120">La procédure distante retourne ses données au stub serveur.</span><span class="sxs-lookup"><span data-stu-id="a6697-120">The remote procedure returns its data to the server stub.</span></span>
2.  <span data-ttu-id="a6697-121">Le stub serveur convertit les paramètres de sortie au format requis pour la transmission sur le réseau et les retourne aux fonctions de la bibliothèque Runtime RPC.</span><span class="sxs-lookup"><span data-stu-id="a6697-121">The server stub converts output parameters to the format required for transmission over the network and returns them to the RPC run-time library functions.</span></span>
3.  <span data-ttu-id="a6697-122">Les fonctions de la bibliothèque Runtime RPC du serveur transmettent les données sur le réseau à l’ordinateur client.</span><span class="sxs-lookup"><span data-stu-id="a6697-122">The server RPC run-time library functions transmit the data on the network to the client computer.</span></span>

<span data-ttu-id="a6697-123">Le client termine le processus en acceptant les données sur le réseau et en le retournant à la fonction appelante.</span><span class="sxs-lookup"><span data-stu-id="a6697-123">The client completes the process by accepting the data over the network and returning it to the calling function.</span></span>

1.  <span data-ttu-id="a6697-124">La bibliothèque Runtime RPC client reçoit les valeurs de retour de procédure distante et les retourne au stub client.</span><span class="sxs-lookup"><span data-stu-id="a6697-124">The client RPC run-time library receives the remote-procedure return values and returns them to the client stub.</span></span>
2.  <span data-ttu-id="a6697-125">Le stub client convertit les données de son rapport de non-remise au format utilisé par l’ordinateur client.</span><span class="sxs-lookup"><span data-stu-id="a6697-125">The client stub converts the data from its NDR to the format used by the client computer.</span></span> <span data-ttu-id="a6697-126">Le stub écrit des données dans la mémoire du client et retourne le résultat au programme appelant sur le client.</span><span class="sxs-lookup"><span data-stu-id="a6697-126">The stub writes data into the client memory and returns the result to the calling program on the client.</span></span>
3.  <span data-ttu-id="a6697-127">La procédure appelante continue comme si la procédure avait été appelée sur le même ordinateur.</span><span class="sxs-lookup"><span data-stu-id="a6697-127">The calling procedure continues as if the procedure had been called on the same computer.</span></span>

<span data-ttu-id="a6697-128">Les bibliothèques Runtime sont fournies en deux parties : une bibliothèque d’importation, qui est liée à l’application et à la bibliothèque Runtime RPC, qui est implémentée en tant que bibliothèque de liens dynamiques (DLL).</span><span class="sxs-lookup"><span data-stu-id="a6697-128">The run-time libraries are provided in two parts: an import library, which is linked with the application and the RPC run-time library, which is implemented as a dynamic-link library (DLL).</span></span>

<span data-ttu-id="a6697-129">L’application serveur contient des appels aux fonctions de la bibliothèque Runtime du serveur qui inscrivent l’interface du serveur et permettent au serveur d’accepter les appels de procédure distante.</span><span class="sxs-lookup"><span data-stu-id="a6697-129">The server application contains calls to the server run-time library functions which register the server's interface and allow the server to accept remote procedure calls.</span></span> <span data-ttu-id="a6697-130">L’application serveur contient également les procédures distantes spécifiques à l’application qui sont appelées par les applications clientes.</span><span class="sxs-lookup"><span data-stu-id="a6697-130">The server application also contains the application-specific remote procedures that are called by the client applications.</span></span>

 

 




