---
title: Implémentation de canaux de sortie sur le client
description: Lorsque vous utilisez un canal de sortie pour transférer des données du serveur vers le client, vous devez implémenter une procédure push dans votre client.
ms.assetid: ab544daf-fbf7-4b00-95a8-55c149a86c27
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ff274491e2b665d86b550853d07c3ff6a4b2a83
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127194192"
---
# <a name="implementing-output-pipes-on-the-client"></a>Implémentation de canaux de sortie sur le client

Lorsque vous utilisez un canal de sortie pour transférer des données du serveur vers le client, vous devez implémenter une procédure push dans votre client. La procédure Push prend un pointeur vers une mémoire tampon et un nombre d’éléments à partir du stub client et, si le nombre d’éléments est supérieur à 0, traite les données. Par exemple, il peut copier les données de la mémoire tampon du stub dans sa propre mémoire. Il peut également traiter les données dans la mémoire tampon du stub et les enregistrer dans un fichier. Lorsque le nombre d’éléments est égal à zéro, la procédure Push effectue toutes les tâches de nettoyage nécessaires avant de retourner.

Dans l’exemple suivant, la fonction cliente ReceiveLongs alloue une structure de canal et une mémoire tampon globale. Il initialise la structure, effectue l’appel de procédure distante, puis libère la mémoire.

## <a name="example"></a>Exemple


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



Cet exemple comprend le fichier d’en-tête généré par le compilateur MIDL. Pour plus d’informations [, consultez Définition de canaux dans le fichier IDL](defining-pipes-in-idl-files.md). Elle déclare également une variable, globalPipeData, qu’elle utilise comme récepteur de données. La variable globalBuffer est une mémoire tampon que la procédure Push utilise pour recevoir des blocs de données qu’elle stocke dans globalPipeData.

La fonction ReceiveLongs déclare un canal et alloue de l’espace mémoire pour la variable de récepteur de données global. Dans votre programme client/serveur, le récepteur de données peut être une structure de fichiers ou de données créée par le client. Dans cet exemple simple, la source de données est une mémoire tampon allouée dynamiquement des entiers longs.

Avant de pouvoir commencer le transfert de données, votre programme client doit initialiser la structure du canal de sortie. Elle doit définir des pointeurs vers la variable d’État, la procédure push et la procédure Alloc. Dans cet exemple, la variable de canal de sortie est appelée outputPipe.

Les clients signalent les serveurs qu’ils sont prêts à recevoir des données en appelant une procédure distante sur le serveur. Dans cet exemple, la procédure distante est appelée « subpipe ». Lorsque le client appelle la procédure distante, le serveur commence le transfert de données. À chaque fois que des données arrivent, le stub client appelle les procédures Alloc et push du client en fonction des besoins.

Au lieu d’allouer de la mémoire à chaque fois qu’une mémoire tampon est nécessaire, la procédure Alloc de cet exemple définit simplement un pointeur vers la variable globalBuffer. La procédure d’extraction réutilise ensuite cette mémoire tampon chaque fois qu’elle transfère des données. Les programmes clients plus complexes peuvent avoir besoin d’allouer une nouvelle mémoire tampon chaque fois que le serveur extrait des données du client.

Dans cet exemple, la procédure Push utilise la variable State pour effectuer le suivi de la position suivante où elle stocke les données dans la mémoire tampon du récepteur de données global. Il écrit des données de la mémoire tampon de canal dans la mémoire tampon du récepteur. Le stub client reçoit alors le bloc de données suivant du serveur et le stocke dans la mémoire tampon du canal. Lorsque toutes les données ont été envoyées, le serveur transmet une mémoire tampon de taille zéro. Cela permet de faire une indication de la procédure Push pour cesser de recevoir des données.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[canal](/windows/desktop/Midl/pipe)
</dt> <dt>

[**/OI**](/windows/desktop/Midl/-oi)
</dt> </dl>

 

 