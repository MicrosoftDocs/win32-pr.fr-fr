---
title: Implémentation de canaux d’entrée sur le serveur
description: Pour commencer à envoyer des données à un serveur, un client appelle l’une des procédures distantes du serveur.
ms.assetid: 6abaa851-41bf-4a03-8d12-cd595d74c8c9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d60c2436129b59619f5a9954c70823631d72ae3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127194196"
---
# <a name="implementing-input-pipes-on-the-server"></a>Implémentation de canaux d’entrée sur le serveur

Pour commencer à envoyer des données à un serveur, un client appelle l’une des procédures distantes du serveur. Cette procédure doit appeler à plusieurs reprises la procédure pull dans le stub du serveur. Le compilateur MIDL utilise le fichier IDL de l’application pour générer automatiquement la procédure pull du serveur.

Chaque fois que le programme serveur appelle la procédure pull dans son stub, la procédure pull reçoit des blocs de données du client. Elle démarshale les données dans la mémoire tampon du serveur. La procédure distante du serveur peut ensuite traiter ces données de quelque manière que ce soit. La boucle se poursuit jusqu’à ce que le serveur reçoive une mémoire tampon de longueur nulle.

L’exemple suivant provient du programme Pipedemo contenu dans les exemples fournis avec le kit de développement logiciel (SDK) de la plateforme. Il illustre une procédure de serveur distant qui utilise un canal pour extraire des données du client vers le serveur.

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

 

 




