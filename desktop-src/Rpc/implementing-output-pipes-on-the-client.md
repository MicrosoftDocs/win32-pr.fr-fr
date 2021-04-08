---
title: Implémentation de canaux de sortie sur le client
description: Lorsque vous utilisez un canal de sortie pour transférer des données du serveur vers le client, vous devez implémenter une procédure push dans votre client.
ms.assetid: ab544daf-fbf7-4b00-95a8-55c149a86c27
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ff274491e2b665d86b550853d07c3ff6a4b2a83
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727789"
---
# <a name="implementing-output-pipes-on-the-client"></a><span data-ttu-id="34125-103">Implémentation de canaux de sortie sur le client</span><span class="sxs-lookup"><span data-stu-id="34125-103">Implementing Output Pipes on the Client</span></span>

<span data-ttu-id="34125-104">Lorsque vous utilisez un canal de sortie pour transférer des données du serveur vers le client, vous devez implémenter une procédure push dans votre client.</span><span class="sxs-lookup"><span data-stu-id="34125-104">When using an output pipe to transfer data from the server to the client, you must implement a push procedure in your client.</span></span> <span data-ttu-id="34125-105">La procédure Push prend un pointeur vers une mémoire tampon et un nombre d’éléments à partir du stub client et, si le nombre d’éléments est supérieur à 0, traite les données.</span><span class="sxs-lookup"><span data-stu-id="34125-105">The push procedure takes a pointer to a buffer and an element count from the client stub and, if the element count is greater than 0, processes the data.</span></span> <span data-ttu-id="34125-106">Par exemple, il peut copier les données de la mémoire tampon du stub dans sa propre mémoire.</span><span class="sxs-lookup"><span data-stu-id="34125-106">For example, it could copy the data from the stub's buffer to its own memory.</span></span> <span data-ttu-id="34125-107">Il peut également traiter les données dans la mémoire tampon du stub et les enregistrer dans un fichier.</span><span class="sxs-lookup"><span data-stu-id="34125-107">Alternately, it could process the data in the stub's buffer and save it to a file.</span></span> <span data-ttu-id="34125-108">Lorsque le nombre d’éléments est égal à zéro, la procédure Push effectue toutes les tâches de nettoyage nécessaires avant de retourner.</span><span class="sxs-lookup"><span data-stu-id="34125-108">When the element count equals zero, the push procedure completes any needed cleanup tasks before returning.</span></span>

<span data-ttu-id="34125-109">Dans l’exemple suivant, la fonction cliente ReceiveLongs alloue une structure de canal et une mémoire tampon globale.</span><span class="sxs-lookup"><span data-stu-id="34125-109">In the following example, the client function ReceiveLongs allocates a pipe structure and a global memory buffer.</span></span> <span data-ttu-id="34125-110">Il initialise la structure, effectue l’appel de procédure distante, puis libère la mémoire.</span><span class="sxs-lookup"><span data-stu-id="34125-110">It initializes the structure, makes the remote procedure call, and then frees the memory.</span></span>

## <a name="example"></a><span data-ttu-id="34125-111">Exemple</span><span class="sxs-lookup"><span data-stu-id="34125-111">Example</span></span>


```C++
//file: client.c (fragment)
#include <windows.h>
#include "pipedemo.h"
long *  globalPipeData;
long    globalBuffer[BUF_SIZE];
 
ulong   pipeDataIndex; /* state variable */
 
void ReceiveLongs()
{
    LONG_PIPE *outputPipe;
    idl_long_int i;
 
    globalPipeData =
        (long *)malloc( sizeof(long) * PIPE_SIZE );
    
    pipeDataIndex = 0;
    outputPipe.state =  (rpc_ss_pipe_state_t )&pipeDataIndex;
    outputPipe.push  = PipePush;
    outputPipe.alloc = PipeAlloc;
 
    OutPipe( &outputPipe ); /* Make the rpc */
 
    free( (void *)globalPipeData );
 
}//end ReceiveLongs()

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
 
void PipePush( rpc_ss_pipe_state_t stateInfo,
               long *buffer,
               ulong numberOfElements )
{
    ulong elementsToCopy, i;
    ulong *state = (ulong *)stateInfo;

    if (numberOfElements == 0)/* end of data */
    {
        *state = 0; /* Reset the state = global index */
    }
    else
    {
        if (*state + numberOfElements > PIPE_SIZE)
            elementsToCopy = PIPE_SIZE - *state;
        else
            elementsToCopy = numberOfElements;
 
        for (i=0; i <elementsToCopy; i++)
        { 
            /*client receives data */
            globalPipeData[*state] = buffer[i];
            (*state)++;
        }
    }
}//end PipePush
```



<span data-ttu-id="34125-112">Cet exemple comprend le fichier d’en-tête généré par le compilateur MIDL.</span><span class="sxs-lookup"><span data-stu-id="34125-112">This example includes the header file generated by the MIDL compiler.</span></span> <span data-ttu-id="34125-113">Pour plus d’informations [, consultez Définition de canaux dans le fichier IDL](defining-pipes-in-idl-files.md).</span><span class="sxs-lookup"><span data-stu-id="34125-113">For details see [Defining Pipes in IDL File](defining-pipes-in-idl-files.md).</span></span> <span data-ttu-id="34125-114">Elle déclare également une variable, globalPipeData, qu’elle utilise comme récepteur de données.</span><span class="sxs-lookup"><span data-stu-id="34125-114">It also declares a variable, globalPipeData, that it uses as the data sink.</span></span> <span data-ttu-id="34125-115">La variable globalBuffer est une mémoire tampon que la procédure Push utilise pour recevoir des blocs de données qu’elle stocke dans globalPipeData.</span><span class="sxs-lookup"><span data-stu-id="34125-115">The variable globalBuffer is a buffer that the push procedure uses to receive blocks of data it stores in globalPipeData.</span></span>

<span data-ttu-id="34125-116">La fonction ReceiveLongs déclare un canal et alloue de l’espace mémoire pour la variable de récepteur de données global.</span><span class="sxs-lookup"><span data-stu-id="34125-116">The ReceiveLongs function declares a pipe and allocates memory space for the global data sink variable.</span></span> <span data-ttu-id="34125-117">Dans votre programme client/serveur, le récepteur de données peut être une structure de fichiers ou de données créée par le client.</span><span class="sxs-lookup"><span data-stu-id="34125-117">In your client/server program, the data sink can be a file or data structure the client creates.</span></span> <span data-ttu-id="34125-118">Dans cet exemple simple, la source de données est une mémoire tampon allouée dynamiquement des entiers longs.</span><span class="sxs-lookup"><span data-stu-id="34125-118">In this simple example, the data source is a dynamically allocated buffer of long integers.</span></span>

<span data-ttu-id="34125-119">Avant de pouvoir commencer le transfert de données, votre programme client doit initialiser la structure du canal de sortie.</span><span class="sxs-lookup"><span data-stu-id="34125-119">Before the data transfer can begin, your client program must initialize the output pipe structure.</span></span> <span data-ttu-id="34125-120">Elle doit définir des pointeurs vers la variable d’État, la procédure push et la procédure Alloc.</span><span class="sxs-lookup"><span data-stu-id="34125-120">It must set pointers to the state variable, the push procedure, and the alloc procedure.</span></span> <span data-ttu-id="34125-121">Dans cet exemple, la variable de canal de sortie est appelée outputPipe.</span><span class="sxs-lookup"><span data-stu-id="34125-121">In this example, the output pipe variable is called outputPipe.</span></span>

<span data-ttu-id="34125-122">Les clients signalent les serveurs qu’ils sont prêts à recevoir des données en appelant une procédure distante sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="34125-122">Clients signal servers that they are ready to receive data by invoking a remote procedure on the server.</span></span> <span data-ttu-id="34125-123">Dans cet exemple, la procédure distante est appelée « subpipe ».</span><span class="sxs-lookup"><span data-stu-id="34125-123">In this example, the remote procedure is called OutPipe.</span></span> <span data-ttu-id="34125-124">Lorsque le client appelle la procédure distante, le serveur commence le transfert de données.</span><span class="sxs-lookup"><span data-stu-id="34125-124">When the client calls the remote procedure, the server begins the data transfer.</span></span> <span data-ttu-id="34125-125">À chaque fois que des données arrivent, le stub client appelle les procédures Alloc et push du client en fonction des besoins.</span><span class="sxs-lookup"><span data-stu-id="34125-125">Each time data arrives, the client stub calls the client's alloc and push procedures as needed.</span></span>

<span data-ttu-id="34125-126">Au lieu d’allouer de la mémoire à chaque fois qu’une mémoire tampon est nécessaire, la procédure Alloc de cet exemple définit simplement un pointeur vers la variable globalBuffer.</span><span class="sxs-lookup"><span data-stu-id="34125-126">Rather than allocate memory each time a buffer is needed, the alloc procedure in this example simply sets a pointer to the variable globalBuffer.</span></span> <span data-ttu-id="34125-127">La procédure d’extraction réutilise ensuite cette mémoire tampon chaque fois qu’elle transfère des données.</span><span class="sxs-lookup"><span data-stu-id="34125-127">The pull procedure then reuses this buffer each time it transfers data.</span></span> <span data-ttu-id="34125-128">Les programmes clients plus complexes peuvent avoir besoin d’allouer une nouvelle mémoire tampon chaque fois que le serveur extrait des données du client.</span><span class="sxs-lookup"><span data-stu-id="34125-128">More complex client programs may need to allocate a new buffer each time the server pulls data from the client.</span></span>

<span data-ttu-id="34125-129">Dans cet exemple, la procédure Push utilise la variable State pour effectuer le suivi de la position suivante où elle stocke les données dans la mémoire tampon du récepteur de données global.</span><span class="sxs-lookup"><span data-stu-id="34125-129">The push procedure in this example uses the state variable to track the next position where it will store data in the global data sink buffer.</span></span> <span data-ttu-id="34125-130">Il écrit des données de la mémoire tampon de canal dans la mémoire tampon du récepteur.</span><span class="sxs-lookup"><span data-stu-id="34125-130">It writes data from the pipe buffer into sink buffer.</span></span> <span data-ttu-id="34125-131">Le stub client reçoit alors le bloc de données suivant du serveur et le stocke dans la mémoire tampon du canal.</span><span class="sxs-lookup"><span data-stu-id="34125-131">The client stub then receives the next block of data from the server and stores it in the pipe buffer.</span></span> <span data-ttu-id="34125-132">Lorsque toutes les données ont été envoyées, le serveur transmet une mémoire tampon de taille zéro.</span><span class="sxs-lookup"><span data-stu-id="34125-132">When all the data has been sent, the server transmits a zero-sized buffer.</span></span> <span data-ttu-id="34125-133">Cela permet de faire une indication de la procédure Push pour cesser de recevoir des données.</span><span class="sxs-lookup"><span data-stu-id="34125-133">This cues the push procedure to stop receiving data.</span></span>

## <a name="related-topics"></a><span data-ttu-id="34125-134">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="34125-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="34125-135">canal</span><span class="sxs-lookup"><span data-stu-id="34125-135">pipe</span></span>](/windows/desktop/Midl/pipe)
</dt> <dt>

[<span data-ttu-id="34125-136">**/OI**</span><span class="sxs-lookup"><span data-stu-id="34125-136">**/Oi**</span></span>](/windows/desktop/Midl/-oi)
</dt> </dl>

 

 