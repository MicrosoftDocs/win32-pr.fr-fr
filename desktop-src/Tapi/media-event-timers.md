---
description: De nombreuses applications dépendent de la relation de synchronisation entre les événements de média (par exemple, les chiffres DTMF reçus) pour déterminer la nature d’une opération demandée.
ms.assetid: 8d25a31f-de40-4c74-b8e7-a81fbfd47db2
title: Minuteurs d’événements de média
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a584518c9c33e8991bd2388f01cb863bab1c7a3
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "106543005"
---
# <a name="media-event-timers"></a>Minuteurs d’événements de média

De nombreuses applications dépendent de la relation de synchronisation entre les événements de média (par exemple, les chiffres DTMF reçus) pour déterminer la nature d’une opération demandée. Par exemple, dans une application de messagerie vocale, deux chiffres DTMF successifs « 1 » peuvent signifier « sauvegarder deux segments » ou « relire à partir du début du message », en fonction du temps écoulé entre les deux chiffres. Dans un environnement client/serveur, si la détection DTMF est effectuée sur un processeur distinct de celui sur lequel l’application est en cours d’exécution, la latence dans le réseau local rend très probable que la relation de synchronisation entre les événements de média sera faussée, avec pour conséquence que ces différences basées sur le minutage peuvent être perdues ou devenir peu fiables.

Pour résoudre ce problème, plusieurs messages TAPI peuvent être horodatés. Étant donné qu’il s’agit de la synchronisation relative entre ces événements qui est importante, le « temps horloge » de l’événement n’est pas important et le temps de la sous-seconde est pris en compte, ces horodateurs utilisent l’heure de résolution (en millisecondes) qui s’est écoulée depuis le début des fenêtres renvoyées par la fonction [**GetTickCount**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-gettickcount) . Les applications doivent savoir qu’il s’agit du nombre de cycles sur le serveur (ou l’ordinateur sur lequel le fournisseur de services qui gère directement le matériel est en cours d’exécution) et n’est pas nécessairement le même ordinateur sur lequel l’application s’exécute ; ainsi, les horodateurs de ces messages TAPI ne peuvent être comparés qu’entre eux, et non à la valeur retournée par **GetTickCount** sur le processeur sur lequel l’application s’exécute.

Les messages TAPI qui peuvent être horodatés sont : [**line \_ GATHERDIGITS**](line-gatherdigits.md), [**line \_ generate**](line-generate.md), [**line \_ MONITORDIGITS**](line-monitordigits.md), [**line \_ MONITORMEDIA**](line-monitormedia.md)et [**line \_ MONITORTONE**](line-monitortone.md). Le nombre de cycles est inséré dans le *dwParam3* de ces messages. Si l’horodatage n’est pas pris en charge par le fournisseur de services (qui est indiqué par le paramètre du fournisseur de services *dwParam3* dans ces messages à 0), TAPI lui-même insère le nombre de cycles dans les *dwParam3* de tous ces messages (il peut être légèrement incliné, mais inférieur à si l’application a été parcourue comme un schéma de communication interprocessus).

 

 
