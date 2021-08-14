---
description: la notion de blocage dans un environnement de Windows a été très importante.
ms.assetid: bd2ede96-34a4-4912-b9d2-ef11d37d2292
title: Opérations bloquantes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d130de2322e10de15bc73e9901b7d55764b34cfbb609e2e25942fb55a3cf445
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118322434"
---
# <a name="blocking-operations"></a>Opérations bloquantes

la notion de blocage dans un environnement de Windows a été très importante. dans Windows environnements sockets 1,1, les appels bloquants ont été déconseillés, car ils ont tendance à désactiver l’interaction continue avec le système. En outre, ils utilisent une technique pseudoblocking qui, pour diverses raisons, ne fonctionne pas toujours comme prévu. toutefois, dans les environnements de Windows planifiés de manière préventive, les appels de blocage prennent bien plus de sens, peuvent être implémentés par les services de système d’exploitation natif et sont en fait un mécanisme généralement préféré. l’API Winsock 2 ne prend plus en charge psuedoblocking, mais étant donné que Windows les shims de compatibilité 1,1 sockets doivent continuer à émuler ce comportement, les fournisseurs de services doivent le prendre en charge comme décrit dans les éléments suivants.

 

 



