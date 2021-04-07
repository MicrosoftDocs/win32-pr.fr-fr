---
title: Comment le client établit une connexion
description: Pour établir une session de communication client/serveur avec un programme serveur, les applications clientes avec des handles explicites doivent créer un handle de liaison.
ms.assetid: c67c9b1a-084f-4b85-ac6c-8cf25a6b0cca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70c5fd8437fb5821c2b52240256a1938e8de31c3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029327"
---
# <a name="how-the-client-establishes-a-connection"></a><span data-ttu-id="adbd3-103">Comment le client établit une connexion</span><span class="sxs-lookup"><span data-stu-id="adbd3-103">How the Client Establishes a Connection</span></span>

<span data-ttu-id="adbd3-104">Pour établir une session de communication client/serveur avec un programme serveur, les applications clientes avec des handles explicites doivent créer un handle de liaison.</span><span class="sxs-lookup"><span data-stu-id="adbd3-104">To establish a client/server communication session with a server program, client applications with explicit handles need to create a binding handle.</span></span> <span data-ttu-id="adbd3-105">Après cela, la bibliothèque Runtime RPC recherche l’ordinateur qui héberge le programme serveur.</span><span class="sxs-lookup"><span data-stu-id="adbd3-105">After they do, the RPC run-time library finds the computer that hosts the server program.</span></span> <span data-ttu-id="adbd3-106">Il recherche ensuite le point de terminaison que le programme serveur écoute et dirige l’appel vers celui-ci.</span><span class="sxs-lookup"><span data-stu-id="adbd3-106">It then finds the endpoint that the server program is listening to and directs the call to it.</span></span> <span data-ttu-id="adbd3-107">Le diagramme suivant illustre ce processus.</span><span class="sxs-lookup"><span data-stu-id="adbd3-107">The following diagram illustrates this process.</span></span>

![un client RPC établit une connexion avec un serveur RPC](images/clntcon.png)

<span data-ttu-id="adbd3-109">Cette section contient des informations sur la façon dont le client se connecte au programme serveur et exécute les procédures distantes qu’il offre.</span><span class="sxs-lookup"><span data-stu-id="adbd3-109">This section presents information about how the client connects to the server program and executes remote procedures that it offers.</span></span> <span data-ttu-id="adbd3-110">Il existe de nombreuses approches pour effectuer ces étapes. selon la conception choisie, une application peut choisir un autre ensemble d’étapes.</span><span class="sxs-lookup"><span data-stu-id="adbd3-110">There are many approaches to completing these steps; depending on the design chosen, an application may choose a different set of steps.</span></span> <span data-ttu-id="adbd3-111">Cet exemple est simplement l’une des façons de procéder.</span><span class="sxs-lookup"><span data-stu-id="adbd3-111">This example is simply one way of doing so.</span></span>

<span data-ttu-id="adbd3-112">La discussion comprend les sections suivantes :</span><span class="sxs-lookup"><span data-stu-id="adbd3-112">The discussion is divided into the following sections:</span></span>

-   [<span data-ttu-id="adbd3-113">Création d’un handle de liaison</span><span class="sxs-lookup"><span data-stu-id="adbd3-113">Creating a Binding Handle</span></span>](creating-a-binding-handle.md)
-   [<span data-ttu-id="adbd3-114">Exécution d’un appel de procédure distante</span><span class="sxs-lookup"><span data-stu-id="adbd3-114">Making a Remote Procedure Call</span></span>](making-a-remote-procedure-call.md)
-   [<span data-ttu-id="adbd3-115">Recherche du programme serveur</span><span class="sxs-lookup"><span data-stu-id="adbd3-115">Finding the Server Program</span></span>](finding-the-server-program.md)
-   [<span data-ttu-id="adbd3-116">Envoi de l’appel au programme serveur</span><span class="sxs-lookup"><span data-stu-id="adbd3-116">Sending the Call to the Server Program</span></span>](sending-the-call-to-the-server-program.md)

 

 




