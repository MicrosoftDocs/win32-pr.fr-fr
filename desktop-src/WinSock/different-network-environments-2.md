---
description: Plusieurs environnements réseau affectent le comportement réseau d’une application.
ms.assetid: 4a530a17-5e61-4730-95f5-233261b4ceb0
title: Différents environnements réseau
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63dca7eacd48973a9106e6a1e3a4eb5959afcfef
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2021
ms.locfileid: "104211199"
---
# <a name="different-network-environments"></a>Différents environnements réseau

Plusieurs environnements réseau affectent le comportement réseau d’une application. Les propriétés qui différencient les environnements réseau incluent une bande passante faible ou élevée, et un temps RTT faible ou élevé. Les environnements réseau affectent les applications transactionnelles et de streaming de différentes manières. Les applications transactionnelles sont plus sensibles au temps RTT. les applications de streaming sont plus sensibles aux produits de délai de bande passante.

![Diagramme montrant comment différents environnements réseau affectent le comportement en réseau d’une application.](images/hperf-1.png)

Les réseaux d’accès à distance et certains réseaux sans fil ont une variable RTT. En règle générale, les réseaux satellites ont une bande passante asymétrique entre en amont et en aval. Les réseaux locaux sans fil et xDSL sont de bons exemples de réseaux avec des produits avec un délai de bande passante similaire à celui de Fast Ethernet.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Applications Windows Sockets hautes performances](high-performance-windows-sockets-applications-2.md)
</dt> <dt>

[Dimensions de performances](performance-dimensions-2.md)
</dt> </dl>

 

 



