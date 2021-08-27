---
description: Dans cette version de l’application, un envoi de bloc compressé de données est utilisé. Cette modification entraîne une amélioration significative des performances.
ms.assetid: 3f0a129b-5b67-4334-a0aa-cd80ee7018b9
title: 'Révision trois : envoi de bloc compressé'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bba84010a09755c5b978665cbd8aa1b29068ec42294ab7b1e499c631fc6b472
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120121279"
---
# <a name="revision-three-compressed-block-send"></a>Révision trois : envoi de bloc compressé

Dans cette version de l’application, un envoi de bloc compressé de données est utilisé. Cette modification entraîne une amélioration significative des performances.


```C++
BYTE tmp[3*ROWS*COLS];
FIELD Old = Map;
ComputeNext( Map );
n=Compact(Map,Old,tmp);
bind( s, ... );
connect( s, ... );
send( s, tmp, 3*n );
//can't do recv(s,tmp,n)
for(int i=0; i < n; )
    recv( s, tmp+i, n-i );
closesocket( s );
```



## <a name="changes-in-this-version"></a>Modifications de cette version

Cette version reflète les modifications suivantes :

-   Les mises à jour de cellules ne sont plus sérialisées.
-   Étant donné qu’un bloc Send est utilisé, l’application n’est plus bavarde.
-   La compression des données est utilisée, ce qui se traduit par une application moins FAT.

Il y a toujours un problème avec cette version de l’application ; le risque d’interblocage existe, car une grande transmission est utilisée sans réception. Le serveur envoie un octet pour tous les 3 octets reçus. Cela peut provoquer un blocage si la taille de la mémoire tampon de réception est inférieure à 1000 octets pour cet exemple d’application.

## <a name="key-performance-metrics"></a>Principales mesures de performance

Les mesures de performances suivantes sont exprimées en temps de boucle (RTT), Goodput et surcharge de protocole. Pour obtenir une explication de ces termes, consultez la rubrique [terminologie réseau](network-terminology-2.md) .

Cette version reflète les mesures de performances suivantes :

-   Heure de la cellule —. 002 \* RTT
-   Goodput : 2 kilo-octets/RTT
-   Surcharge de protocole : 14%

De la surcharge de 14%, 6% provient des en-têtes Ethernet et les 8 autres% proviennent du démarrage et de la destruction de la connexion.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Amélioration d’une application lente](improving-a-slow-application-2.md)
</dt> <dt>

[Terminologie du réseau](network-terminology-2.md)
</dt> <dt>

[Version de référence : une application très médiocre](the-baseline-version-a-very-poor-performing-application-2.md)
</dt> <dt>

[Révision 1 : nettoyage évident](revision-1-cleaning-up-the-obvious-2.md)
</dt> <dt>

[Révision 2 : reconception pour des connexions moins nombreuses](revision-2-redesigning-for-fewer-connects-2.md)
</dt> <dt>

[Améliorations futures](future-improvements-2.md)
</dt> </dl>

 

 



