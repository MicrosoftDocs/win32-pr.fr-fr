---
description: Plusieurs environnements réseau affectent le comportement réseau d’une application.
ms.assetid: 4a530a17-5e61-4730-95f5-233261b4ceb0
title: Différents environnements réseau
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13acdd27930a9b60af3004440b2cb4cf3a049cf2cce5f72f387cb51699e23782
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119858432"
---
# <a name="different-network-environments"></a>Différents environnements réseau

Plusieurs environnements réseau affectent le comportement réseau d’une application. Les propriétés qui différencient les environnements réseau incluent une bande passante faible ou élevée, et un temps RTT faible ou élevé. Les environnements réseau affectent les applications transactionnelles et de streaming de différentes manières. Les applications transactionnelles sont plus sensibles au temps RTT. les applications de streaming sont plus sensibles aux produits de délai de bande passante.

![Diagramme montrant comment différents environnements réseau affectent le comportement en réseau d’une application.](images/hperf-1.png)

Les réseaux d’accès à distance et certains réseaux sans fil ont une variable RTT. En règle générale, les réseaux satellites ont une bande passante asymétrique entre en amont et en aval. Les réseaux locaux sans fil et xDSL sont de bons exemples de réseaux avec des produits avec un délai de bande passante similaire à celui de Fast Ethernet.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Applications de sockets Windows hautes performances](high-performance-windows-sockets-applications-2.md)
</dt> <dt>

[Dimensions de performances](performance-dimensions-2.md)
</dt> </dl>

 

 



