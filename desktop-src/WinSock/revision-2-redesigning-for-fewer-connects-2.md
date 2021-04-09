---
description: Dans cette révision, l’exemple d’application est repensé pour éliminer les connexions inutiles.
ms.assetid: 0db6ded4-0a59-454e-824e-8cd7f0dc9fec
title: 'Révision deux : reconception pour des connexions moins nombreuses'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae8d5a8c8648f43f9ddac93c9d17f667b4b97011
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114911"
---
# <a name="revision-two-redesigning-for-fewer-connects"></a>Révision deux : reconception pour des connexions moins nombreuses

Dans cette révision, l’exemple d’application est repensé pour éliminer les connexions inutiles.

> [!WARNING]
> Cet exemple d’application fournit également des performances intentionnellement médiocres, afin d’illustrer les améliorations de performances possibles avec les modifications apportées au code. N’utilisez pas cet exemple de code dans votre application. elle est fournie à titre d’illustration uniquement.

 


```C++
ComputeNext( Map );
bind( s, ... );
connect( s, ... );
for(int i=0 ; i < ROWS ; ++i)
  for(int j=0 ; j < COLS ; ++j)
  {
    BYTE tmp[3];
    tmp[0] = i;
    tmp[1] = j;
    tmp[2] = Map[i][j];
    send( s, tmp, 3 );
    recv( s, &byRet, 1 );
  }
closesocket( s );
```



## <a name="remaining-problems"></a>Problèmes restants

Les modifications apportées à la révision deux ont remanié l’application pour n’effectuer qu’une seule connexion par mise à jour. L’application comprend toujours les problèmes de performances suivants :

-   L’application est toujours sérialisée et bavarde.
-   L’application a toujours une conception FAT ; Il existe de nombreux envois qui ne nécessitent aucune opération dans cette conception.
-   Les envois sont toujours uniquement de 3 octets, ce qui correspond à une mauvaise diffusion.

## <a name="key-performance-metrics"></a>Principales mesures de performance

Les mesures de performances suivantes sont exprimées en temps de boucle (RTT), Goodput et surcharge de protocole. Pour obtenir une explication de ces termes, consultez la rubrique [terminologie réseau](network-terminology-2.md) .

Cette version reflète les mesures de performances suivantes :

-   Heure de la cellule — 1 \* RTT
-   Goodput — 4 octets/RTT
-   Surcharge de protocole : 96,8%

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

[Révision 3 : envoi de bloc compressé](revision-3-compressed-block-send-2.md)
</dt> <dt>

[Améliorations futures](future-improvements-2.md)
</dt> </dl>

 

 



