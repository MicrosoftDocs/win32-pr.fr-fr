---
title: Implémentation de canaux d’entrée sur le client
description: Lorsque vous utilisez un canal d’entrée pour transférer des données du client vers le serveur, vous devez implémenter une procédure d’extraction.
ms.assetid: e941a6be-ca91-42b1-9323-ffc63d521f6c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2810caa31c4932294797a5ed502c6f93d8613ea0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842549"
---
# <a name="implementing-input-pipes-on-the-client"></a><span data-ttu-id="9a959-103">Implémentation de canaux d’entrée sur le client</span><span class="sxs-lookup"><span data-stu-id="9a959-103">Implementing Input Pipes on the Client</span></span>

<span data-ttu-id="9a959-104">Lorsque vous utilisez un canal d’entrée pour transférer des données du client vers le serveur, vous devez implémenter une procédure d’extraction.</span><span class="sxs-lookup"><span data-stu-id="9a959-104">When using an input pipe to transfer data from the client to the server, you must implement a pull procedure.</span></span> <span data-ttu-id="9a959-105">La procédure pull doit rechercher les données à transférer, lire les données dans la mémoire tampon et définir le nombre d’éléments à envoyer.</span><span class="sxs-lookup"><span data-stu-id="9a959-105">The pull procedure must find the data to be transferred, read the data into the buffer, and set the number of elements to send.</span></span> <span data-ttu-id="9a959-106">Toutes les données ne doivent pas être dans la mémoire tampon lorsque le serveur commence à extraire des données.</span><span class="sxs-lookup"><span data-stu-id="9a959-106">Not all of the data has to be in the buffer when the server begins to pull data to itself.</span></span> <span data-ttu-id="9a959-107">La procédure pull peut remplir la mémoire tampon de manière incrémentielle.</span><span class="sxs-lookup"><span data-stu-id="9a959-107">The pull procedure can fill the buffer incrementally.</span></span>

<span data-ttu-id="9a959-108">Lorsqu’il n’y a plus de données à envoyer, la procédure définit son dernier argument sur zéro.</span><span class="sxs-lookup"><span data-stu-id="9a959-108">When there is no more data to send, the procedure sets its last argument to zero.</span></span> <span data-ttu-id="9a959-109">Lorsque toutes les données sont envoyées, la procédure pull doit effectuer tout nettoyage nécessaire avant de retourner.</span><span class="sxs-lookup"><span data-stu-id="9a959-109">When all the data is sent, the pull procedure should do any needed cleanup before returning.</span></span> <span data-ttu-id="9a959-110">Pour un paramètre qui est un \[ canal in, out \] , la procédure pull doit réinitialiser la variable d’État du client une fois que toutes les données ont été transmises, afin que la procédure Push puisse l’utiliser pour recevoir des données.</span><span class="sxs-lookup"><span data-stu-id="9a959-110">For a parameter that is an \[in, out\] pipe, the pull procedure must reset the client's state variable after all the data has been transmitted, so that the push procedure can use it to receive data.</span></span>

<span data-ttu-id="9a959-111">L’exemple suivant est extrait du programme Pipedemo inclus dans le kit de développement logiciel (SDK) de la plateforme.</span><span class="sxs-lookup"><span data-stu-id="9a959-111">The following example is extracted from the Pipedemo program included with the Platform Software Development Kit (SDK).</span></span>


```C++
//file: client.c (fragment)
#include <windows.h>
#include "pipedemo.h"
long *globalPipeData;
long    globalBuffer[BUF_SIZE];
 
ulong   pipeDataIndex; /* state variable */
 
void SendLongs()
{
    LONG_PIPE inPipe;
    int i;
    globalPipeData =
        (long *)malloc( sizeof(long) * PIPE_SIZE );
 
    for (i=0; i<PIPE_SIZE; i++)
        globalPipeData[i] = IN_VALUE;
 
    pipeDataIndex = 0;
    inPipe.state =  (rpc_ss_pipe_state_t )&pipeDataIndex;
    inPipe.pull  = PipePull;
    inPipe.alloc = PipeAlloc;
 
    InPipe( inPipe ); /* Make the rpc */
 
    free( (void *)globalPipeData );

}//end SendLongs
 
void PipeAlloc( rpc_ss_pipe_state_t stateInfo,
                ulong requestedSize,
                long **allocatedBuffer,
                ulong *allocatedSize )
{ 
    ulong *state = (ulong *)stateInfo;
    if ( requestedSize > (BUF_SIZE*sizeof(long)) )
    {
       *allocatedSize = BUF_SIZE * sizeof(long);
    }
    else
    {
       *allocatedSize = requestedSize;
    }
    *allocatedBuffer = globalBuffer; 
} //end PipeAlloc
 
void PipePull( rpc_ss_pipe_state_t stateInfo,
               long *inputBuffer,
               ulong maxBufSize,
               ulong *sizeToSend )
{
    ulong currentIndex;
    ulong i;
    ulong elementsToRead;
    ulong *state = (ulong *)stateInfo;

    currentIndex = *state;
    if (*state >=  PIPE_SIZE )
    {
        *sizeToSend = 0; /* end of pipe data */
        *state = 0; /* Reset the state = global index */
    }
    else 
    {
        if ( currentIndex + maxBufSize > PIPE_SIZE )
            elementsToRead = PIPE_SIZE - currentIndex;
        else
            elementsToRead = maxBufSize;
 
        for (i=0; i < elementsToRead; i++)
        {
            /*client sends data */
            inputBuffer[i] = globalPipeData[i + currentIndex];
        }
 
        *state +=   elementsToRead;
        *sizeToSend = elementsToRead;
    } 
}//end PipePull
```



<span data-ttu-id="9a959-112">Cet exemple comprend le fichier d’en-tête généré par le compilateur MIDL.</span><span class="sxs-lookup"><span data-stu-id="9a959-112">This example includes the header file generated by the MIDL compiler.</span></span> <span data-ttu-id="9a959-113">Pour plus d’informations [, consultez Définition de canaux dans des fichiers IDL](defining-pipes-in-idl-files.md).</span><span class="sxs-lookup"><span data-stu-id="9a959-113">For details see [Defining Pipes in IDL Files](defining-pipes-in-idl-files.md).</span></span> <span data-ttu-id="9a959-114">Elle déclare également une variable qu’elle utilise comme source de données appelée globalPipeData.</span><span class="sxs-lookup"><span data-stu-id="9a959-114">It also declares a variable it uses as the data source called globalPipeData.</span></span> <span data-ttu-id="9a959-115">La variable globalBuffer est une mémoire tampon que la procédure d’extraction utilise pour envoyer les blocs de données qu’elle obtient à partir de globalPipeData.</span><span class="sxs-lookup"><span data-stu-id="9a959-115">The variable globalBuffer is a buffer that the pull procedure uses to send the blocks of data it obtains from globalPipeData.</span></span>

<span data-ttu-id="9a959-116">La fonction SendLongs déclare le canal d’entrée et alloue de la mémoire pour la variable de source de données globalPipeData.</span><span class="sxs-lookup"><span data-stu-id="9a959-116">The SendLongs function declares the input pipe, and allocates memory for the data source variable globalPipeData.</span></span> <span data-ttu-id="9a959-117">Dans votre programme client/serveur, la source de données peut être un fichier ou une structure créé (e) par le client.</span><span class="sxs-lookup"><span data-stu-id="9a959-117">In your client/server program, the data source can be a file or structure that the client creates.</span></span> <span data-ttu-id="9a959-118">Vous pouvez également faire en sorte que votre programme client obtienne des données à partir du serveur, les traite et les renvoie au serveur à l’aide d’un canal d’entrée.</span><span class="sxs-lookup"><span data-stu-id="9a959-118">You can also have your client program obtain data from the server, process it, and return it to the server using an input pipe.</span></span> <span data-ttu-id="9a959-119">Dans cet exemple simple, la source de données est une mémoire tampon allouée dynamiquement des entiers longs.</span><span class="sxs-lookup"><span data-stu-id="9a959-119">In this simple example, the data source is a dynamically allocated buffer of long integers.</span></span>

<span data-ttu-id="9a959-120">Avant de pouvoir commencer le transfert, le client doit définir des pointeurs vers la variable d’État, la procédure pull et la procédure Alloc.</span><span class="sxs-lookup"><span data-stu-id="9a959-120">Before the transfer can begin, the client must set pointers to the state variable, the pull procedure, and the alloc procedure.</span></span> <span data-ttu-id="9a959-121">Ces pointeurs sont conservés dans la variable de canal que le client déclare.</span><span class="sxs-lookup"><span data-stu-id="9a959-121">These pointers are kept in the pipe variable the client declares.</span></span> <span data-ttu-id="9a959-122">Dans ce cas, SendLongs déclare le canal d’échange.</span><span class="sxs-lookup"><span data-stu-id="9a959-122">In this case, SendLongs declares inPipe.</span></span> <span data-ttu-id="9a959-123">Vous pouvez utiliser n’importe quel type de données approprié pour votre variable d’État.</span><span class="sxs-lookup"><span data-stu-id="9a959-123">You can use any appropriate data type for your state variable.</span></span>

<span data-ttu-id="9a959-124">Les clients lancent des transferts de données sur un canal en appelant une procédure distante sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="9a959-124">Clients initiate data transfers across a pipe by invoking a remote procedure on the server.</span></span> <span data-ttu-id="9a959-125">L’appel de la procédure distante indique au programme serveur que le client est prêt à être transmis.</span><span class="sxs-lookup"><span data-stu-id="9a959-125">Calling the remote procedure tells the server program that the client is ready to transmit.</span></span> <span data-ttu-id="9a959-126">Le serveur peut ensuite extraire les données vers lui-même.</span><span class="sxs-lookup"><span data-stu-id="9a959-126">The server can then pull the data to itself.</span></span> <span data-ttu-id="9a959-127">Cet exemple appelle une procédure distante appelée « pipe ».</span><span class="sxs-lookup"><span data-stu-id="9a959-127">This example invokes a remote procedure called InPipe.</span></span> <span data-ttu-id="9a959-128">Une fois les données transférées vers le serveur, la fonction SendLongs libère la mémoire tampon allouée dynamiquement.</span><span class="sxs-lookup"><span data-stu-id="9a959-128">After the data is transferred to the server, the SendLongs function frees the dynamically allocated buffer.</span></span>

<span data-ttu-id="9a959-129">Au lieu d’allouer de la mémoire à chaque fois qu’une mémoire tampon est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="9a959-129">Rather than allocate memory each time a buffer is needed.</span></span> <span data-ttu-id="9a959-130">la procédure Alloc de cet exemple définit simplement un pointeur vers la variable globalBuffer.</span><span class="sxs-lookup"><span data-stu-id="9a959-130">the alloc procedure in this example simply sets a pointer to the variable globalBuffer.</span></span> <span data-ttu-id="9a959-131">La procédure d’extraction réutilise cette mémoire tampon chaque fois qu’elle transfère des données.</span><span class="sxs-lookup"><span data-stu-id="9a959-131">The pull procedure reuses this buffer each time it transfers data.</span></span> <span data-ttu-id="9a959-132">Les programmes clients plus complexes peuvent avoir besoin d’allouer une nouvelle mémoire tampon chaque fois que le serveur extrait des données du client.</span><span class="sxs-lookup"><span data-stu-id="9a959-132">More complex client programs may need to allocate a new buffer each time the server pulls data from the client.</span></span>

<span data-ttu-id="9a959-133">Le stub client appelle la procédure pull.</span><span class="sxs-lookup"><span data-stu-id="9a959-133">The client stub calls the pull procedure.</span></span> <span data-ttu-id="9a959-134">La procédure pull dans cet exemple utilise la variable State pour effectuer le suivi de la position suivante dans la mémoire tampon de la source de données globale à lire.</span><span class="sxs-lookup"><span data-stu-id="9a959-134">The pull procedure in this example uses the state variable to track the next position in the global data source buffer to read from.</span></span> <span data-ttu-id="9a959-135">Il lit les données de la mémoire tampon source dans la mémoire tampon du canal.</span><span class="sxs-lookup"><span data-stu-id="9a959-135">It reads data from the source buffer into the pipe buffer.</span></span> <span data-ttu-id="9a959-136">Le stub client transmet les données au serveur.</span><span class="sxs-lookup"><span data-stu-id="9a959-136">The client stub transmits the data to the server.</span></span> <span data-ttu-id="9a959-137">Lorsque toutes les données ont été envoyées, la procédure pull définit la taille de la mémoire tampon sur zéro.</span><span class="sxs-lookup"><span data-stu-id="9a959-137">When all the data has been sent, the pull procedure sets the buffer size to zero.</span></span> <span data-ttu-id="9a959-138">Cela indique au serveur d’arrêter l’extraction des données.</span><span class="sxs-lookup"><span data-stu-id="9a959-138">This tells the server to stop pulling data.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9a959-139">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9a959-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9a959-140">canal</span><span class="sxs-lookup"><span data-stu-id="9a959-140">pipe</span></span>](/windows/desktop/Midl/pipe)
</dt> <dt>

[<span data-ttu-id="9a959-141">**/OI**</span><span class="sxs-lookup"><span data-stu-id="9a959-141">**/Oi**</span></span>](/windows/desktop/Midl/-oi)
</dt> </dl>

 

 