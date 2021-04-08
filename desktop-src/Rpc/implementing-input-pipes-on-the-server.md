---
title: Implémentation de canaux d’entrée sur le serveur
description: Pour commencer à envoyer des données à un serveur, un client appelle l’une des procédures distantes du serveur.
ms.assetid: 6abaa851-41bf-4a03-8d12-cd595d74c8c9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d60c2436129b59619f5a9954c70823631d72ae3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840214"
---
# <a name="implementing-input-pipes-on-the-server"></a><span data-ttu-id="7f905-103">Implémentation de canaux d’entrée sur le serveur</span><span class="sxs-lookup"><span data-stu-id="7f905-103">Implementing Input Pipes on the Server</span></span>

<span data-ttu-id="7f905-104">Pour commencer à envoyer des données à un serveur, un client appelle l’une des procédures distantes du serveur.</span><span class="sxs-lookup"><span data-stu-id="7f905-104">To begin sending data to a server, a client calls one of the server's remote procedures.</span></span> <span data-ttu-id="7f905-105">Cette procédure doit appeler à plusieurs reprises la procédure pull dans le stub du serveur.</span><span class="sxs-lookup"><span data-stu-id="7f905-105">This procedure must repeatedly call the pull procedure in the server's stub.</span></span> <span data-ttu-id="7f905-106">Le compilateur MIDL utilise le fichier IDL de l’application pour générer automatiquement la procédure pull du serveur.</span><span class="sxs-lookup"><span data-stu-id="7f905-106">The MIDL compiler uses the application's IDL file to automatically generate the server's pull procedure.</span></span>

<span data-ttu-id="7f905-107">Chaque fois que le programme serveur appelle la procédure pull dans son stub, la procédure pull reçoit des blocs de données du client.</span><span class="sxs-lookup"><span data-stu-id="7f905-107">Each time the server program invokes the pull procedure in its stub, the pull procedure receives blocks of data from the client.</span></span> <span data-ttu-id="7f905-108">Elle démarshale les données dans la mémoire tampon du serveur.</span><span class="sxs-lookup"><span data-stu-id="7f905-108">It unmarshals the data into the server's buffer.</span></span> <span data-ttu-id="7f905-109">La procédure distante du serveur peut ensuite traiter ces données de quelque manière que ce soit.</span><span class="sxs-lookup"><span data-stu-id="7f905-109">The server's remote procedure can then process this data in any way required.</span></span> <span data-ttu-id="7f905-110">La boucle se poursuit jusqu’à ce que le serveur reçoive une mémoire tampon de longueur nulle.</span><span class="sxs-lookup"><span data-stu-id="7f905-110">The loop continues until the server receives a buffer of zero length.</span></span>

<span data-ttu-id="7f905-111">L’exemple suivant provient du programme Pipedemo contenu dans les exemples fournis avec le kit de développement logiciel (SDK) de la plateforme.</span><span class="sxs-lookup"><span data-stu-id="7f905-111">The following example is from the Pipedemo program contained in the samples that come with the Platform Software Development Kit (SDK).</span></span> <span data-ttu-id="7f905-112">Il illustre une procédure de serveur distant qui utilise un canal pour extraire des données du client vers le serveur.</span><span class="sxs-lookup"><span data-stu-id="7f905-112">It illustrates a remote server procedure that uses a pipe to pull data from the client to the server.</span></span>

``` syntax
//file: server.c (fragment)
#include uc_server.c
#define PIPE_TRANSFER_SIZE 100 /* Transfer 100 pipe elements at one time */
 
void InPipe(LONG_PIPE     long_pipe )
{
    long local_pipe_buf[PIPE_TRANSFER_SIZE];
    ulong actual_transfer_count = PIPE_TRANSFER_SIZE;
 
    while(actual_transfer_count > 0) /* Loop to get all 
                                        the pipe data elements */
    {
        long_pipe.pull( long_pipe.state,
                        local_pipe_buf,
                        PIPE_TRANSFER_SIZE,
                        &actual_transfer_count);
        /* process the elements */
    } // end while
} //end InPipe
```

 

 




