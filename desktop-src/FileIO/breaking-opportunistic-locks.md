---
description: La rupture d’un verrou opportuniste est le processus qui consiste à dégrader le verrou d’un client sur un fichier de sorte qu’un autre client puisse ouvrir le fichier, avec ou sans verrou opportuniste.
ms.assetid: 0356c167-2973-4820-85a9-bc14abcbf163
title: Interruption des verrous opportunistes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74b797feed06c5f02f1b87ff4e05e2d82d44a34f0efe86d7a0881ec1d722023f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119582599"
---
# <a name="breaking-opportunistic-locks"></a>Interruption des verrous opportunistes

La rupture d’un verrou opportuniste est le processus qui consiste à dégrader le verrou d’un client sur un fichier de sorte qu’un autre client puisse ouvrir le fichier, avec ou sans verrou opportuniste. Lorsque l’autre client demande l’opération d’ouverture, le serveur retarde l’opération d’ouverture et avertit le client qui détient le verrou opportuniste.

Le client qui détient le verrou prend ensuite les mesures appropriées pour le type de verrou, par exemple en abandonnant les tampons de lecture, en fermant le fichier, etc. Uniquement lorsque le client qui détient le verrou opportuniste notifie le serveur qu’il est terminé, le serveur ouvre le fichier pour le client qui demande l’opération d’ouverture. Toutefois, lorsqu’un verrou de niveau 2 est endommagé, le serveur signale au client qu’il a été interrompu, mais n’attend pas d’accusé de réception, car il n’existe aucune donnée en cache à vider sur le serveur.

Lors de la réception d’une interruption d’un verrou exclusif (filtre, niveau 1 ou lot), le détenteur d’un verrou cassé ne peut pas demander un autre verrou exclusif. Il peut dégrader un verrou exclusif à un verrou de niveau 2 ou aucun verrou. Le détenteur libère généralement le verrou et ferme le fichier lorsqu’il est sur le le même de fermer le fichier.

Les applications sont averties qu’un verrou opportuniste est interrompu à l’aide du membre **hEvent** de la structure [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) associée au fichier sur lequel le verrou est interrompu. Les applications peuvent également utiliser des fonctions telles que [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) et [**HasOverlappedIoCompleted**](/windows/desktop/api/winbase/nf-winbase-hasoverlappediocompleted).

 

 
