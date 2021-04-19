---
description: La notion de blocage dans un environnement Windows a été historiquement très importante.
ms.assetid: bd2ede96-34a4-4912-b9d2-ef11d37d2292
title: Opérations bloquantes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8040865b4c6ededab925279e15d67cb89f7bc6a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515455"
---
# <a name="blocking-operations"></a>Opérations bloquantes

La notion de blocage dans un environnement Windows a été historiquement très importante. Dans les environnements Windows Sockets 1,1, les appels bloquants ont été déconseillés, car ils ont tendance à désactiver l’interaction continue avec le système. En outre, ils utilisent une technique pseudoblocking qui, pour diverses raisons, ne fonctionne pas toujours comme prévu. Toutefois, dans les environnements Windows préprogrammés, les appels bloquants sont bien plus parlants, peuvent être implémentés par les services du système d’exploitation natif et sont en fait un mécanisme généralement préféré. L’API Winsock 2 ne prend plus en charge psuedoblocking, mais étant donné que les shims de compatibilité Windows Sockets 1,1 doivent continuer à émuler ce comportement, les fournisseurs de services doivent le prendre en charge comme décrit dans les éléments suivants.

 

 



