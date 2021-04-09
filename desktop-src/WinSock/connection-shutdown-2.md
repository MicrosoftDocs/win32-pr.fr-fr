---
description: La rubrique suivante décrit les opérations qui aboutissent à l’arrêt d’une connexion de socket établie.
ms.assetid: 052e04a4-5290-4dca-af7a-cd590ebfbe15
title: Arrêt de la connexion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbde0cfe4c3a97435c2412d28970107f830308fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862581"
---
# <a name="connection-shutdown"></a>Arrêt de la connexion

La rubrique suivante décrit les opérations qui aboutissent à l’arrêt d’une connexion de socket établie.

## <a name="initiating-shutdown-sequence"></a>Lancement de la séquence d’arrêt

Une connexion de socket peut être retirée de plusieurs façons. [**WSPShutdown**](/previous-versions/windows/desktop/legacy/ms742294(v=vs.85)) (avec *l'* équivalent de SD \_ Send ou SD \_ ) et [**WSPSendDisconnect**](/previous-versions/windows/desktop/legacy/ms742290(v=vs.85)) peut être utilisé pour initier un arrêt de connexion normal. [**WSPCloseSocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85)) peut être utilisé pour initier un arrêt normal ou d’abandon, en fonction des options de Lingo appelées par le socket fermant. Consultez la section ci-dessous pour plus d’informations sur les arrêts normaux et d’abandon, et les options de maintien.

## <a name="indicating-remote-shutdown"></a>Indication de l’arrêt à distance

Les fournisseurs de services indiquent la suppression de connexion lancée par le tiers distant via l' \_ événement réseau FD Close. L’arrêt progressif est également indiqué par le biais de [**WSPRecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85)) lorsque le nombre d’octets lus est 0 pour les protocoles de flux d’octets, ou par le biais d’un code d’erreur de retour de WSAEDISCON pour les protocoles orientés message. Dans tous les cas, un code d’erreur de retour **WSPRecv** de WSAECONNRESET indique un arrêt d’abandon.

## <a name="exchanging-user-data-at-shutdown-time"></a>Échange des données utilisateur au moment de l’arrêt

Au moment de la destruction de la connexion, il est également possible (pour les protocoles qui le prennent en charge) d’échanger des données utilisateur entre les points de terminaison. La fin qui initie la destruction peut appeler [**WSPSendDisconnect**](/previous-versions/windows/desktop/legacy/ms742290(v=vs.85)) pour indiquer qu’il n’y a plus de données à envoyer et que la séquence de destruction de la connexion est lancée. Pour certains protocoles, une partie de cette séquence de destruction est la remise de données déconnectées de l’initiateur de destruction. Après avoir reçu une notification indiquant que l’extrémité distante a initié la séquence de destruction (généralement via l' \_ indication FD Close), la fonction [**WSPRecvDisconnect**](/previous-versions/windows/desktop/legacy/ms742285(v=vs.85)) peut être appelée pour recevoir les données de déconnexion (le cas échéant).

Pour illustrer la façon dont les données de déconnexion peuvent être utilisées, examinez le scénario suivant. La moitié du client d’une application client/serveur est responsable de l’arrêt d’une connexion de Socket. Coïncide avec l’arrêt qu’il fournit (via la déconnexion des données) le nombre total de transactions qu’il a traitées avec le serveur. Le serveur répond ensuite avec le total cumulé des transactions qu’il a traitées avec tous les clients. La séquence d’appels et d’indications peut se produire comme indiqué dans le tableau suivant.

| Côté client                                                                                                               | Côté serveur                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| (1) appelle [**WSPSendDisconnect**](/previous-versions/windows/desktop/legacy/ms742290(v=vs.85)) pour conclure la session et fournir le total de la transaction.            |                                                                                                                                         |
|                                                                                                                           | (2) obtient FD \_ Close, ou [**WSPRecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85)) avec une valeur de retour égale à zéro ou WSAEDISCON indiquant un arrêt correct en cours. |
|                                                                                                                           | (3) appelle [**WSPRecvDisconnect**](/previous-versions/windows/desktop/legacy/ms742285(v=vs.85)) pour connaître le total de la transaction du client.                                         |
|                                                                                                                           | (4) calcule le total général cumulé de toutes les transactions.                                                                                |
|                                                                                                                           | (5) appelle [**WSPSendDisconnect**](/previous-versions/windows/desktop/legacy/ms742290(v=vs.85)) pour transmettre le total général.                                                   |
| (6) reçoit l' \_ indication FD Close.                                                                                        | (5 ') appelle [ **WSPCloseSocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85))                                                                                 |
| (7) appelle [**WSPRecvDisconnect**](/previous-versions/windows/desktop/legacy/ms742285(v=vs.85)) pour recevoir et stocker le total cumulé des transactions. |                                                                                                                                         |
|                                                                                                                           | (8) appelle [ **WSPCloseSocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85))                                                                                  |



 

L’étape (5 ') doit suivre l’étape (5), mais elle n’a pas de relation de minutage avec les étapes (6), (7) ou (8).

 

 
