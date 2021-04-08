---
description: Exécution de l’exemple de code complet du client TCP/IP et de l’application serveur.
ms.assetid: 617dfdf6-f7a7-4e72-8c77-8cfa3ab232e7
title: Exécution de l’exemple de code du client et du serveur Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9b3588af6bac668f0b7c785bafe2f69de4ef2b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951177"
---
# <a name="running-the-winsock-client-and-server-code-sample"></a><span data-ttu-id="8e386-103">Exécution de l’exemple de code du client et du serveur Winsock</span><span class="sxs-lookup"><span data-stu-id="8e386-103">Running the Winsock Client and Server Code Sample</span></span>

<span data-ttu-id="8e386-104">Cette section contient le code source complet pour les applications clientes et serveur TCP/IP :</span><span class="sxs-lookup"><span data-stu-id="8e386-104">This section contains the complete source code for the TCP/IP Client and Server applications:</span></span>

-   [<span data-ttu-id="8e386-105">Code client Winsock complet</span><span class="sxs-lookup"><span data-stu-id="8e386-105">Complete Winsock Client Code</span></span>](complete-client-code.md)
-   [<span data-ttu-id="8e386-106">Compléter le code du serveur Winsock</span><span class="sxs-lookup"><span data-stu-id="8e386-106">Complete Winsock Server Code</span></span>](complete-server-code.md)

<span data-ttu-id="8e386-107">L’application serveur doit être démarrée avant le démarrage de l’application cliente.</span><span class="sxs-lookup"><span data-stu-id="8e386-107">The server application should be started before the client application is started.</span></span>

<span data-ttu-id="8e386-108">Pour exécuter le serveur, compilez le code source complet du serveur et exécutez le fichier exécutable.</span><span class="sxs-lookup"><span data-stu-id="8e386-108">To execute the server, compile the complete server source code and run the executable file.</span></span> <span data-ttu-id="8e386-109">L’application serveur écoute sur le port TCP 27015 pour qu’un client se connecte.</span><span class="sxs-lookup"><span data-stu-id="8e386-109">The server application listens on TCP port 27015 for a client to connect.</span></span> <span data-ttu-id="8e386-110">Une fois qu’un client se connecte, le serveur reçoit des données du client et renvoie (envoie) les données reçues au client.</span><span class="sxs-lookup"><span data-stu-id="8e386-110">Once a client connects, the server receives data from the client and echoes (sends) the data received back to the client.</span></span> <span data-ttu-id="8e386-111">Lorsque le client arrête la connexion, le serveur arrête le socket client, ferme le socket et se ferme.</span><span class="sxs-lookup"><span data-stu-id="8e386-111">When the client shuts down the connection, the server shuts down the client socket, closes the socket, and exits.</span></span>

<span data-ttu-id="8e386-112">Pour exécuter le client, compilez le code source complet du client et exécutez le fichier exécutable.</span><span class="sxs-lookup"><span data-stu-id="8e386-112">To execute the client, compile the complete client source code and run the executable file.</span></span> <span data-ttu-id="8e386-113">L’application cliente exige que le nom de l’ordinateur ou de l’adresse IP de l’ordinateur sur lequel l’application serveur s’exécute est passé en tant que paramètre de ligne de commande lors de l’exécution du client.</span><span class="sxs-lookup"><span data-stu-id="8e386-113">The client application requires that name of the computer or IP address of the computer where the server application is running is passed as a command-line parameter when the client is executed.</span></span> <span data-ttu-id="8e386-114">Si le client et le serveur sont exécutés sur l’ordinateur d’exemple, le client peut être démarré comme suit :</span><span class="sxs-lookup"><span data-stu-id="8e386-114">If the client and server are executed on the sample computer, the client can be started as follows:</span></span>

<span data-ttu-id="8e386-115">**localhost du client**</span><span class="sxs-lookup"><span data-stu-id="8e386-115">**client localhost**</span></span>

<span data-ttu-id="8e386-116">Le client tente de se connecter au serveur sur le port TCP 27015.</span><span class="sxs-lookup"><span data-stu-id="8e386-116">The client tries to connect to the server on TCP port 27015.</span></span> <span data-ttu-id="8e386-117">Une fois que le client se connecte, le client envoie des données au serveur et reçoit toutes les données renvoyées par le serveur.</span><span class="sxs-lookup"><span data-stu-id="8e386-117">Once the client connects, the client sends data to the server and receives any data send back from the server.</span></span> <span data-ttu-id="8e386-118">Le client ferme ensuite le socket et s’arrête.</span><span class="sxs-lookup"><span data-stu-id="8e386-118">The client then closes the socket and exits.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8e386-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8e386-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8e386-120">Prise en main avec Winsock</span><span class="sxs-lookup"><span data-stu-id="8e386-120">Getting Started With Winsock</span></span>](getting-started-with-winsock.md)
</dt> </dl>

 

 



