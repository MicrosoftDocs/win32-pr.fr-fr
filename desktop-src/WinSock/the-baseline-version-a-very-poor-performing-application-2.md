---
description: Version de référence d’une application très médiocre dans Windows Sockets (Winsock).
ms.assetid: 923884c4-f1bd-4f72-983e-6158f368e0dd
title: 'Version de référence : une application très médiocre'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7c094be5fd5cf6e3b9eaeb07c7ff38880e651dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106518728"
---
# <a name="the-baseline-version-a-very-poor-performing-application"></a>Version de référence : une application très médiocre

L’exemple de code initial le plus médiocre utilisé pour calculer les mises à jour est le suivant :

> [!Note]  
> Par souci de simplicité, il n’y a pas de gestion des erreurs dans les exemples suivants. Toutes les applications de production vérifient toujours les valeurs de retour.

 

> [!WARNING]
> Les premiers exemples de l’application offrent des performances intentionnellement médiocres, afin d’illustrer les améliorations de performances possibles avec les modifications apportées au code. N’utilisez pas ces exemples de code dans votre application. ils sont fournis à titre d’illustration uniquement.

 


```C++
#include <windows.h>

BOOL Map[ROWS][COLS];

void LifeUpdate()
{
    ComputeNext( Map );
    for( int i = 0 ; i < ROWS ; ++i )     //serialized
        for( int j = 0 ; j < COLS ; ++j )
            Set( i, j, Map[i][j] );    //chatty
}

BYTE Set(row, col, bAlive)
{
    SOCKET s = socket(...);
    BYTE byRet = 0;
    setsockopt( s, SO_SNDBUF, &Zero, sizeof(int) );
    bind( s, ... );
    connect( s, ... );
    send( s, &row, 1 );
    send( s, &col, 1 );
    send( s, &bAlive, 1 );
    recv( s, &byRet, 1 );
    closesocket( s );
    return byRet;
}
```



Dans cet État, l’application présente les pires performances réseau possibles. Les problèmes liés à cette version de l’exemple d’application sont les suivants :

-   L’application est bavarde. Chaque transaction est trop petite : il n’est pas nécessaire de mettre à jour les cellules une par une.
-   Les transactions sont strictement sérialisées, même si les cellules peuvent être mises à jour simultanément.
-   La mémoire tampon d’envoi est définie sur zéro, et l’application entraîne un délai de 200 millisecondes pour chaque envoi, soit trois fois par cellule.
-   L’application est très connectée et se connecte une seule fois pour chaque cellule. Les applications sont limitées en nombre de connexions par seconde pour une destination donnée en raison de l’état d’attente, mais ce n’est pas un problème dans la mesure où chaque transaction prend plus de 600 millisecondes.
-   L’application est FAT ; de nombreuses transactions n’ont aucun effet sur l’état du serveur, car de nombreuses cellules ne changent pas de la mise à jour à la mise à jour.
-   L’application présente une mauvaise diffusion. les petits envois consomment beaucoup d’UC et de RAM.
-   L’application suppose une représentation Little endian pour ses envois. Il s’agit d’une hypothèse naturelle pour la plate-forme Windows actuelle, mais elle peut être dangereuse pour le code à long terme.

## <a name="key-performance-metrics"></a>Principales mesures de performance

Les mesures de performances suivantes sont exprimées en temps de boucle (RTT), Goodput et surcharge de protocole. Pour obtenir une explication de ces termes, consultez la rubrique [terminologie réseau](network-terminology-2.md) .

-   L’heure de la cellule, l’heure réseau pour une mise à jour de cellule unique, requiert 4 temps \* RTT + 600 millisecondes pour Nagle et les interactions ACK différées.
-   Goodput est inférieur à 6 octets.
-   La surcharge de protocole est de 99,6%.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Amélioration d’une application lente](improving-a-slow-application-2.md)
</dt> <dt>

[Terminologie du réseau](network-terminology-2.md)
</dt> <dt>

[Révision 1 : nettoyage évident](revision-1-cleaning-up-the-obvious-2.md)
</dt> <dt>

[Révision 2 : reconception pour des connexions moins nombreuses](revision-2-redesigning-for-fewer-connects-2.md)
</dt> <dt>

[Révision 3 : envoi de bloc compressé](revision-3-compressed-block-send-2.md)
</dt> <dt>

[Améliorations futures](future-improvements-2.md)
</dt> </dl>

 

 



