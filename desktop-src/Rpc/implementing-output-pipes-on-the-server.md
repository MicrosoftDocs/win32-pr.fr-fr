---
title: Implémentation de canaux de sortie sur le serveur
description: Pour commencer à recevoir des données à partir d’un serveur, un client appelle l’une des procédures distantes du serveur.
ms.assetid: 5d791f4f-1d95-4bc0-b68f-db4fccc75ff8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 234d93b2933499ca86ab49732d46cf2abe3c37247ed7bfa5e653e5aa0119b1e7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120020489"
---
# <a name="implementing-output-pipes-on-the-server"></a>Implémentation de canaux de sortie sur le serveur

Pour commencer à recevoir des données à partir d’un serveur, un client appelle l’une des procédures distantes du serveur. Cette procédure doit appeler à plusieurs reprises la procédure push dans le stub du serveur. Le compilateur MIDL utilise le fichier IDL de l’application pour générer automatiquement la procédure push du serveur.

La routine de serveur distant doit remplir la mémoire tampon du canal de sortie avec des données avant d’appeler la procédure push. Chaque fois que le programme serveur appelle la procédure push dans son stub, la procédure Push marshale les données et les transmet au client. La boucle se poursuit jusqu’à ce que le serveur envoie une mémoire tampon de longueur nulle.

l’exemple suivant provient du programme Pipedemo contenu dans les exemples fournis avec le SDK Windows. Il illustre une procédure de serveur distant qui utilise un canal pour transmettre les données du serveur au client.


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



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[canal](/windows/desktop/Midl/pipe)
</dt> <dt>

[**/OI**](/windows/desktop/Midl/-oi)
</dt> </dl>

 

 