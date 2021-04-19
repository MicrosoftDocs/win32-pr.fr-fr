---
description: Dans cette version de l’exemple de programme, quelques changements évidents ont été apportés, qui prendront des Strides initiaux pour améliorer les performances.
ms.assetid: ef9d594c-31fe-44c0-b707-47c01e2c5bf0
title: 'Révision 1 : nettoyage évident'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 631bea7395000531cce542b41ace3b3aab9afff0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524594"
---
# <a name="revision-one-cleaning-up-the-obvious"></a>Révision 1 : nettoyage évident

Dans cette version de l’exemple de programme, quelques changements évidents ont été apportés, qui prendront des Strides initiaux pour améliorer les performances. Cette version du code est loin de l’optimisation des performances, mais il s’agit d’une bonne étape incrémentielle qui permet d’examiner les effets de meilleures approches de manière incrémentielle.

> [!WARNING]
> Cet exemple de l’application fournit intentionnellement des performances médiocres, afin d’illustrer les améliorations de performances possibles avec les modifications apportées au code. N’utilisez pas cet exemple de code dans votre application. elle est fournie à titre d’illustration uniquement.

 


```C++
#include <windows.h>

BYTE Set(row, col, bAlive)
{
    SOCKET s = socket(...);
    BYTE byRet = 0;
    BYTE tmp[3];
    tmp[0] = (BYTE)row;
    tmp[1] = (BYTE)col;
    tmp[2] = (BYTE)bAlive;
    bind( s, ... );
    connect( s, ... );
    send( s, &tmp, 3 );
    recv( s, &byRet, 1 );
    closesocket( s );
    return byRet;
}
```



## <a name="changes-in-this-version"></a>Modifications de cette version

Cette version reflète les modifications suivantes :

-   Suppression de SNDBUF = 0. Les retards de 200 millisecondes dus aux envois non mis en mémoire tampon et aux accusés de réception différés sont supprimés.
-   Suppression du comportement Send-Send-Receive. Cette modification élimine les retards de 200 millisecondes dus à Nagle et aux interactions ACK retardées.
-   Suppression de l’hypothèse Little-endian supprimée. Les octets sont maintenant dans l’ordre.

## <a name="remaining-problems"></a>Problèmes restants

Dans cette version, les problèmes suivants sont conservés :

-   L’application se connecte toujours lourd. Étant donné que les retards de 600 millisecondes sont supprimés, l’application atteint maintenant le taux soutenu de 12 connexions par seconde. De nombreuses connexions simultanées deviennent maintenant un problème.
-   L’application est toujours FAT ; les cellules inchangées sont toujours propagées vers le serveur.
-   L’application présente toujours une mauvaise diffusion. les envois de 3 octets sont toujours des émissions de petite taille.
-   L’application envoie à présent 2 octets/RTT, soit 4 Ko/s sur une connexion Ethernet directement connectée. Cela n’est pas trop rapide, mais TIME-WAIT entraînera probablement d’abord des problèmes.
-   La surcharge est inférieure à 99,3%, ce qui n’est toujours pas un bon pourcentage de charge.

## <a name="key-performance-metrics"></a>Principales mesures de performance

Les métriques de performances clés suivantes sont exprimées en temps de trajet aller-retour (RTT), Goodput et surcharge de protocole. Pour obtenir une explication de ces termes, consultez la rubrique [terminologie réseau](network-terminology-2.md) .

Cette version reflète les mesures de performances suivantes :

-   Heure de la cellule — 2 × RTT
-   Goodput : 2 octets/RTT
-   Surcharge de protocole — 99.3 pour cent

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Amélioration d’une application lente](improving-a-slow-application-2.md)
</dt> <dt>

[Terminologie du réseau](network-terminology-2.md)
</dt> <dt>

[Version de référence : une application très médiocre](the-baseline-version-a-very-poor-performing-application-2.md)
</dt> <dt>

[Révision 2 : reconception pour des connexions moins nombreuses](revision-2-redesigning-for-fewer-connects-2.md)
</dt> <dt>

[Révision 3 : envoi de bloc compressé](revision-3-compressed-block-send-2.md)
</dt> <dt>

[Améliorations futures](future-improvements-2.md)
</dt> </dl>

 

 



