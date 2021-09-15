---
description: 'Il existe deux types d’applications réseau fondamentaux : transactionnel et streaming. Ces types d’applications sont également appelés types d’applications de traitement interactif et de traitement par lots, respectivement.'
ms.assetid: 85795cdd-5a4f-4199-98bd-b5ce2299338b
title: Applications transactionnelles et applications de streaming
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a000f3aa9c52fe6ce60622a613d6f4b9689b8bf
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127296639"
---
# <a name="transactional-versus-streaming-applications"></a>Applications transactionnelles et applications de streaming

Il existe deux types d’applications réseau fondamentaux : *transactionnel* et *streaming*. Ces types d’applications sont également appelés types d’applications de traitement *interactif* et de *traitement par lots* , respectivement.

Les applications transactionnelles sont des applications Stop-and-go. Ils effectuent généralement des opérations de demande/réponse, souvent ordonnées. Les exemples d’applications transactionnelles incluent l’appel de procédure distante synchrone (RPC), ainsi que certaines implémentations du système de noms de domaine (DNS) et HTTP.

Les applications de streaming déplacent les données. Pour décrire les applications de streaming à l’aide d’un terme parallèle, les applications de streaming adhèrent à une philosophie de transmission de données en métal, généralement avec peu de préoccupation pour le classement des données. La sauvegarde réseau et le protocole FTP (File Transfer Protocol) sont des exemples d’applications de streaming.

Une fois que le type d’application est déterminé, ses caractéristiques de protocole et de réseau sont également déterminées.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Applications de sockets Windows hautes performances](high-performance-windows-sockets-applications-2.md)
</dt> <dt>

[Dimensions de performances](performance-dimensions-2.md)
</dt> </dl>

 

 



