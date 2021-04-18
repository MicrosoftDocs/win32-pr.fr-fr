---
description: Calcul de la surcharge avec netstat
ms.assetid: d96a8fba-8d76-443f-be49-81a8ad7050fa
title: Calcul de la surcharge avec netstat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7843c3cd445bee66e25a9f191ae4b78093faea0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516248"
---
# <a name="calculating-overhead-with-netstat"></a>Calcul de la surcharge avec netstat

Le calcul de la surcharge avec netstat doit être effectué sur un réseau silencieux pour éviter que d’autres trafics réseau n’inclinent les données, telles que le trafic de diffusion ou de multidiffusion.

**Pour calculer la surcharge réseau d’une application à l’aide de netstat**

1.  Récupérez les statistiques d’interface actuelles à l’aide de netstat.
2.  Exécutez l'application.
3.  Récupérez les statistiques de l’interface, à nouveau à l’aide de netstat.
4.  Calculez le nombre d’octets reçus entre les deux mesures netstat.

## <a name="example"></a>Exemple

L’exemple suivant illustre ces étapes, à l’aide de TTCP, pour envoyer 10 octets de données, un octet à la fois.

Tout d’abord, une surcharge théorique pour l’application est calculée. Pour ce test, tous les paquets sont de 60 octets (la valeur Ethernet minimale). Ce transfert requiert trois paquets pour configurer la connexion, 10 paquets de données, 10 paquets d’accusés de réception (ACK retardé est déclenché presque à tout moment) et quatre paquets pour fermer la connexion correctement.

Cela équivaut à 27 paquets de 60 octets chacun, ou à 1620 octets (3 + 4 + 10 + 10) \* 60 = 1620). Étant donné que seuls 10 octets de données sont transférés, la charge est de 1610 octets, ce qui correspond à plus de 99% de la charge de protocole.

### <a name="commands"></a>Commandes

**netstat-e**

``` syntax
Interface Statistics
                     Received     Sent
Bytes                392291400    444684566
Unicast packets      487627       570086
Non-unicast packets  1159163      11300
Discards             0            0
Errors               0            0
Unknown protocols    52812
```

**TTCP-t-H0-D-L1-n10-P9 172.31.71.99**

``` syntax
ttcp-t: 10 bytes in 2168 real milliseconds = 0 KB/sec
ttcp-t: 10 I/O calls, msec/call = 216, calls/sec = 4, bytes/call = 1
```

**netstat-e**

``` syntax
Interface Statistics
                      Received     Sent
Bytes                 39229207     444685382
Unicast packets       487641       570100
Non-unicast packets   1159164      11301
Discards              0            0
Errors                0            0
Unknown protocols     52812
```

### <a name="calculations"></a>Calculs

**Envoyé :** 816 octets

**Reçu :** 674 octets

**Nombre total d’octets :** 1490

**Octets utilisateur :** 10

**Surcharge :** 1480/1490 = 99,3%

* * Goodput : * * = 5 octets/seconde (ou 40 bits/s)

> [!Note]  
> Les octets réels transférés ne correspondent pas aux valeurs théoriques en raison des octets de remplissage non pris en compte pour les valeurs netstat.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Comportement de l’application](application-behavior-2.md)
</dt> <dt>

[Applications Windows Sockets hautes performances](high-performance-windows-sockets-applications-2.md)
</dt> </dl>

 

 



