---
description: Vous pouvez réduire l’impact de votre application sur d’autres clients et l’impact qu’elle a sur votre application en accordant autant de partage que possible, en demandant le niveau d’accès minimal nécessaire et en utilisant le verrou opportuniste le moins intrusif adapté à votre application.
ms.assetid: c28b0ae0-0d35-4b59-9f54-87c55ca72716
title: Réponse du serveur pour les demandes d’ouverture sur les fichiers verrouillés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d397613f6b54f2b42c26a5674a787b796f5f19e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526859"
---
# <a name="server-response-to-open-requests-on-locked-files"></a>Réponse du serveur pour les demandes d’ouverture sur les fichiers verrouillés

La durée de vie d’un verrou opportuniste comprend trois intervalles de temps distincts. Au cours de chaque, le serveur détermine, par différents moyens, sa réaction à une demande d’un client pour ouvrir un fichier verrouillé par un autre client. En général, vous pouvez réduire l’impact de votre application sur d’autres clients et l’impact qu’elle a sur votre application en accordant autant de partage que possible, en demandant le niveau d’accès minimal nécessaire et en utilisant le verrou opportuniste le moins intrusif adapté à votre application.

Tout d’abord, la période après laquelle le serveur ouvre un fichier pour un client, mais avant d’accorder un verrou. Pendant ce temps, aucun verrou n’existe sur le fichier, et le serveur dépend du partage, des modes d’accès et du type de verrou opportuniste que vous demandez pour déterminer sa réaction à une autre demande d’ouverture du même fichier. Par exemple, si vous ouvrez le fichier en question pour l’accès en écriture, vous pouvez empêcher d’accorder des verrous opportunistes qui autorisent l’accès à la mise en cache de lecture à d’autres clients. L’intervalle de temps avant que le serveur n’accorde un verrou se trouve généralement dans la plage de millisecondes, mais peut être plus long.

Une fois le verrou opportuniste accordé, le serveur examine le verrou pour déterminer la réaction du serveur à une demande d’ouverture sur un fichier verrouillé. Là encore, la façon dont votre application a ouvert le fichier et le type de verrou qu’il détient affecte la façon dont le serveur répond. Pour plus d’informations sur la façon dont le serveur répond dans chaque cas, consultez [types de verrous opportunistes](types-of-opportunistic-locks.md).

Enfin, il existe une étendue après que le serveur a déterminé que votre verrouillage doit être interrompu (terminé), mais avant que votre application n’ait terminé sa réaction à l’arrêt. Selon le type de verrou, votre application peut rétrograder le verrou à un niveau inférieur ou à aucun. Votre application peut également fermer le fichier et le verrou. Pendant ce temps, le serveur conserve dans abeyance toutes les demandes d’autres clients pour ouvrir le fichier précédemment verrouillé. Cet intervalle de temps peut être compris entre les millisecondes et les dizaines de secondes. Pour plus d’informations, consultez [interruption des verrous opportunistes](breaking-opportunistic-locks.md).

 

 



