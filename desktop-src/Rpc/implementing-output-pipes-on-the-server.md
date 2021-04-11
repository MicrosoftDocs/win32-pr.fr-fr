---
title: Implémentation de canaux de sortie sur le serveur
description: Pour commencer à recevoir des données à partir d’un serveur, un client appelle l’une des procédures distantes du serveur.
ms.assetid: 5d791f4f-1d95-4bc0-b68f-db4fccc75ff8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb3eb1362736207f9cc79d82ab6c981431d0bfe7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031742"
---
# <a name="implementing-output-pipes-on-the-server"></a><span data-ttu-id="a9496-103">Implémentation de canaux de sortie sur le serveur</span><span class="sxs-lookup"><span data-stu-id="a9496-103">Implementing Output Pipes on the Server</span></span>

<span data-ttu-id="a9496-104">Pour commencer à recevoir des données à partir d’un serveur, un client appelle l’une des procédures distantes du serveur.</span><span class="sxs-lookup"><span data-stu-id="a9496-104">To begin receiving data from a server, a client calls one of the server's remote procedures.</span></span> <span data-ttu-id="a9496-105">Cette procédure doit appeler à plusieurs reprises la procédure push dans le stub du serveur.</span><span class="sxs-lookup"><span data-stu-id="a9496-105">This procedure must repeatedly call the push procedure in the server's stub.</span></span> <span data-ttu-id="a9496-106">Le compilateur MIDL utilise le fichier IDL de l’application pour générer automatiquement la procédure push du serveur.</span><span class="sxs-lookup"><span data-stu-id="a9496-106">The MIDL compiler uses the application's IDL file to automatically generate the server's push procedure.</span></span>

<span data-ttu-id="a9496-107">La routine de serveur distant doit remplir la mémoire tampon du canal de sortie avec des données avant d’appeler la procédure push.</span><span class="sxs-lookup"><span data-stu-id="a9496-107">The remote server routine must fill the output pipe's buffer with data before it calls the push procedure.</span></span> <span data-ttu-id="a9496-108">Chaque fois que le programme serveur appelle la procédure push dans son stub, la procédure Push marshale les données et les transmet au client.</span><span class="sxs-lookup"><span data-stu-id="a9496-108">Each time the server program invokes the push procedure in its stub, the push procedure marshals the data and transmits it to the client.</span></span> <span data-ttu-id="a9496-109">La boucle se poursuit jusqu’à ce que le serveur envoie une mémoire tampon de longueur nulle.</span><span class="sxs-lookup"><span data-stu-id="a9496-109">The loop continues until the server sends a buffer of zero length.</span></span>

<span data-ttu-id="a9496-110">L’exemple suivant provient du programme Pipedemo contenu dans les exemples fournis avec le SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="a9496-110">The following example is from the Pipedemo program contained in the samples that come with the Windows SDK.</span></span> <span data-ttu-id="a9496-111">Il illustre une procédure de serveur distant qui utilise un canal pour transmettre les données du serveur au client.</span><span class="sxs-lookup"><span data-stu-id="a9496-111">It illustrates a remote server procedure that uses a pipe to push data from the server to the client.</span></span>


```C++
void OutPipe(LONG_PIPE *outputPipe )
{
    long *outputPipeData;
    ulong index = 0;
    ulong elementsToSend = PIPE_TRANSFER_SIZE;
 
    /* Allocate memory for the data to be passed back in the pipe */
    outputPipeData = (long *)malloc( sizeof(long) * PIPE_SIZE );
    
    while(elementsToSend >0) /* Loop to send pipe data elements */
    {
        if (index >= PIPE_SIZE)
            elementsToSend = 0;
        else
        {
            if ( (index + PIPE_TRANSFER_SIZE) > PIPE_SIZE )
                elementsToSend = PIPE_SIZE - index;
            else
                elementsToSend = PIPE_TRANSFER_SIZE;
        }
                    
        outputPipe->push( outputPipe->state,
                          &(outputPipeData[index]),
                          elementsToSend ); 
        index += elementsToSend;
 
    } //end while
 
    free((void *)outputPipeData);
 
}
```



## <a name="related-topics"></a><span data-ttu-id="a9496-112">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a9496-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a9496-113">canal</span><span class="sxs-lookup"><span data-stu-id="a9496-113">pipe</span></span>](/windows/desktop/Midl/pipe)
</dt> <dt>

[<span data-ttu-id="a9496-114">**/OI**</span><span class="sxs-lookup"><span data-stu-id="a9496-114">**/Oi**</span></span>](/windows/desktop/Midl/-oi)
</dt> </dl>

 

 