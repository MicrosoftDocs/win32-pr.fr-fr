---
description: Les fonctions WSARecv, WSARecvFrom, WSARecvMsg, WSASend, WSASendMsg et WSASendTo prennent toutes un tableau de mémoires tampons d’application en tant que paramètres d’entrée et peuvent être utilisées pour les e/s de ventilation/regroupement (ou vectorielle).
ms.assetid: c42e6cea-3b40-44ad-8715-09ce57e82217
title: E/s de ventilation/regroupement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c572892a75b3532d68a39e2fabdcc971f0a3327
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524592"
---
# <a name="scattergather-io"></a>E/s de ventilation/regroupement

Les fonctions [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv), [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom), [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg), [**WSASend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend), [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg)et [**WSASendTo**](/windows/desktop/api/Winsock2/nf-winsock2-wsasendto) prennent toutes un tableau de mémoires tampons d’application en tant que paramètres d’entrée et peuvent être utilisées pour les e/s de ventilation/regroupement (ou vectorielle). Cela peut être très utile dans les instances où des parties de chaque message en cours de transmission se composent d’un ou de plusieurs composants d’en-tête de longueur fixe, en plus du corps du message. Ces composants d’en-tête n’ont pas besoin d’être concaténés par l’application en une seule mémoire tampon contiguë avant l’envoi. De même, à la réception, les composants d’en-tête peuvent être automatiquement divisés en mémoires tampons distinctes, ce qui laisse le corps du message par lui-même.

Lors de la réception dans plusieurs mémoires tampons, la saisie semi-automatique se produit à mesure que les données arrivent du réseau, que toutes les mémoires tampons fournies soient utilisées ou non.

 

 
