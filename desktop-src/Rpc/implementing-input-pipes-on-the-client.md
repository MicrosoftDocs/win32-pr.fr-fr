---
title: Implémentation de canaux d’entrée sur le client
description: Lorsque vous utilisez un canal d’entrée pour transférer des données du client vers le serveur, vous devez implémenter une procédure d’extraction.
ms.assetid: e941a6be-ca91-42b1-9323-ffc63d521f6c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2810caa31c4932294797a5ed502c6f93d8613ea0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127194199"
---
# <a name="implementing-input-pipes-on-the-client"></a>Implémentation de canaux d’entrée sur le client

Lorsque vous utilisez un canal d’entrée pour transférer des données du client vers le serveur, vous devez implémenter une procédure d’extraction. La procédure pull doit rechercher les données à transférer, lire les données dans la mémoire tampon et définir le nombre d’éléments à envoyer. Toutes les données ne doivent pas être dans la mémoire tampon lorsque le serveur commence à extraire des données. La procédure pull peut remplir la mémoire tampon de manière incrémentielle.

Lorsqu’il n’y a plus de données à envoyer, la procédure définit son dernier argument sur zéro. Lorsque toutes les données sont envoyées, la procédure pull doit effectuer tout nettoyage nécessaire avant de retourner. Pour un paramètre qui est un \[ canal in, out \] , la procédure pull doit réinitialiser la variable d’État du client une fois que toutes les données ont été transmises, afin que la procédure Push puisse l’utiliser pour recevoir des données.

L’exemple suivant est extrait du programme Pipedemo inclus dans le kit de développement logiciel (SDK) de la plateforme.


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



Cet exemple comprend le fichier d’en-tête généré par le compilateur MIDL. Pour plus d’informations [, consultez Définition de canaux dans des fichiers IDL](defining-pipes-in-idl-files.md). Elle déclare également une variable qu’elle utilise comme source de données appelée globalPipeData. La variable globalBuffer est une mémoire tampon que la procédure d’extraction utilise pour envoyer les blocs de données qu’elle obtient à partir de globalPipeData.

La fonction SendLongs déclare le canal d’entrée et alloue de la mémoire pour la variable de source de données globalPipeData. Dans votre programme client/serveur, la source de données peut être un fichier ou une structure créé (e) par le client. Vous pouvez également faire en sorte que votre programme client obtienne des données à partir du serveur, les traite et les renvoie au serveur à l’aide d’un canal d’entrée. Dans cet exemple simple, la source de données est une mémoire tampon allouée dynamiquement des entiers longs.

Avant de pouvoir commencer le transfert, le client doit définir des pointeurs vers la variable d’État, la procédure pull et la procédure Alloc. Ces pointeurs sont conservés dans la variable de canal que le client déclare. Dans ce cas, SendLongs déclare le canal d’échange. Vous pouvez utiliser n’importe quel type de données approprié pour votre variable d’État.

Les clients lancent des transferts de données sur un canal en appelant une procédure distante sur le serveur. L’appel de la procédure distante indique au programme serveur que le client est prêt à être transmis. Le serveur peut ensuite extraire les données vers lui-même. Cet exemple appelle une procédure distante appelée « pipe ». Une fois les données transférées vers le serveur, la fonction SendLongs libère la mémoire tampon allouée dynamiquement.

Au lieu d’allouer de la mémoire à chaque fois qu’une mémoire tampon est nécessaire. la procédure Alloc de cet exemple définit simplement un pointeur vers la variable globalBuffer. La procédure d’extraction réutilise cette mémoire tampon chaque fois qu’elle transfère des données. Les programmes clients plus complexes peuvent avoir besoin d’allouer une nouvelle mémoire tampon chaque fois que le serveur extrait des données du client.

Le stub client appelle la procédure pull. La procédure pull dans cet exemple utilise la variable State pour effectuer le suivi de la position suivante dans la mémoire tampon de la source de données globale à lire. Il lit les données de la mémoire tampon source dans la mémoire tampon du canal. Le stub client transmet les données au serveur. Lorsque toutes les données ont été envoyées, la procédure pull définit la taille de la mémoire tampon sur zéro. Cela indique au serveur d’arrêter l’extraction des données.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[canal](/windows/desktop/Midl/pipe)
</dt> <dt>

[**/OI**](/windows/desktop/Midl/-oi)
</dt> </dl>

 

 