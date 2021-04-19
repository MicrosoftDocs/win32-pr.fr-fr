---
description: Comme les doublons sont les descripteurs de socket et non les sockets sous-jacents, tous les États associés à un socket sont communs à tous les descripteurs.
ms.assetid: f3a2cd5a-bc3a-4aeb-8606-7b8aa6afb105
title: Plusieurs descripteurs sur un seul socket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2356f24a69d132f87e0f6543f61509ff12acba5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515023"
---
# <a name="multiple-handles-to-a-single-socket"></a>Plusieurs descripteurs sur un seul socket

Comme les doublons sont les descripteurs de socket et non les sockets sous-jacents, tous les États associés à un socket sont communs à tous les descripteurs. Par exemple, une opération [**WSPSetSockOpt**](/previous-versions/windows/hardware/network/ff566318(v=vs.85)) effectuée à l’aide d’un descripteur est visible par la suite à l’aide d’un [**WSPGetSockOpt**](/previous-versions/windows/hardware/network/ff566292(v=vs.85)) à partir d’un ou de tous les descripteurs.

La notification sur les sockets partagés est soumise aux contraintes habituelles de [**WSPAsyncSelect**](/previous-versions/windows/desktop/legacy/ms742267(v=vs.85)) et de [**WSPEventSelect**](/previous-versions/windows/hardware/network/ff566287(v=vs.85)). L’émission de l’un de ces appels à l’aide de l’un des descripteurs partagés annule toute inscription d’événement précédente pour le socket, quel que soit le descripteur utilisé pour effectuer cette inscription. Par exemple, il n’est pas possible d’avoir des événements de lecture de lecture FD de réception \_ et de traitement B pour les événements d' \_ écriture FD. Dans les situations où une étroite coordination est nécessaire, il est préférable que les développeurs envisagent d’utiliser des threads plutôt que des processus distincts.

 

 
