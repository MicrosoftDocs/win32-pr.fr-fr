---
description: La forme la plus simple des e/s dans Windows Sockets 2 est le blocage des e/s.
ms.assetid: 8ed7e5a8-c577-4b61-9c49-8fd065d84af4
title: Blocage des entrées/sorties
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d1c846a22fcf9d10f562a48683c2ead723f9bd4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106513228"
---
# <a name="blocking-inputoutput"></a>Blocage des entrées/sorties

La forme la plus simple des e/s dans Windows Sockets 2 est le blocage des e/s. Comme mentionné dans les [indicateurs et les modes d’attribut de socket](socket-attribute-flags-and-modes-2.md), les sockets sont créés en mode blocage par défaut. Toute opération d’e/s avec un socket bloquant n’est pas retournée tant que l’opération n’a pas été complètement terminée. Ainsi, tout thread ne peut exécuter qu’une seule opération d’e/s à la fois. Par exemple, si un thread émet une opération de réception et qu’aucune donnée n’est actuellement disponible, le thread se bloque jusqu’à ce que les données deviennent disponibles et placées dans la mémoire tampon du thread. Bien que cela soit simple, il ne s’agit pas nécessairement de la méthode la plus efficace pour effectuer des e/s (pour plus d’informations, consultez la page relative aux [Pseudo-blocages et au blocage réel](pseudo-vs--true-blocking-2.md) ).

 

 



