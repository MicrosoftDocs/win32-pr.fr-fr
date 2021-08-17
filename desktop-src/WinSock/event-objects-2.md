---
description: L’introduction d’e/s avec chevauchement nécessite un mécanisme permettant aux applications d’associer sans ambiguïté les demandes d’envoi et de réception à leurs indications d’achèvement ultérieures.
ms.assetid: 944d87bd-388f-420d-ac7d-69c4a28f8a5c
title: objets d’événement (Windows sockets 2)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34820d7df92704d86f7dbdc100816789488426e2fdd553456be94da921811c3f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132592"
---
# <a name="event-objects-windows-sockets-2"></a>objets d’événement (Windows sockets 2)

L’introduction d’e/s avec chevauchement nécessite un mécanisme permettant aux applications d’associer sans ambiguïté les demandes d’envoi et de réception à leurs indications d’achèvement ultérieures. dans Windows sockets 2, cela s’effectue avec les objets d’événement qui sont modélisés après Windows événements. Windows Les objets d’événement sockets sont des constructions assez simples qui peuvent être créées et fermées, définies et désactivées, et attendues et interrogées. Leur utilitaire principal est la capacité d’une application à se bloquer et à attendre jusqu’à ce qu’un ou plusieurs objets d’événement soient définis.

Les applications utilisent [**WSACreateEvent**](/windows/desktop/api/Winsock2/nf-winsock2-wsacreateevent) pour obtenir un descripteur d’objet d’événement qui peut ensuite être fourni comme paramètre obligatoire aux versions avec chevauchement des appels d’envoi et de réception ( [**WSASend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend), [**WSASendTo**](/windows/desktop/api/Winsock2/nf-winsock2-wsasendto), [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv), [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom)). L’objet d’événement, qui est effacé lors de sa création, est défini par les fournisseurs de transport lorsque l’opération d’e/s avec chevauchement associée est terminée (avec succès ou avec des erreurs). Chaque objet d’événement créé par **WSACreateEvent** doit avoir un [**WSACloseEvent**](/windows/desktop/api/Winsock2/nf-winsock2-wsacloseevent) correspondant pour le détruire.

Les objets d’événement sont également utilisés dans [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) pour associer un ou plusieurs \_ événements réseau FD xxx à un objet d’événement. Cela est décrit dans [notification asynchrone à l’aide d’objets d’événement](asynchronous-notification-using-event-objects-2.md).

dans les environnements 32 bits, les fonctions relatives aux objets d’événement, notamment [**WSACreateEvent**](/windows/desktop/api/Winsock2/nf-winsock2-wsacreateevent), [**WSACloseEvent**](/windows/desktop/api/Winsock2/nf-winsock2-wsacloseevent), [**WSASetEvent**](/windows/desktop/api/Winsock2/nf-winsock2-wsasetevent), [**WSAResetEvent**](/windows/desktop/api/Winsock2/nf-winsock2-wsaresetevent)et [**WSAWaitForMultipleEvents**](/windows/desktop/api/Winsock2/nf-winsock2-wsawaitformultipleevents) , sont mappées directement aux fonctions Windows natives correspondantes, en utilisant le même nom de fonction, mais sans le préfixe WSA.

 

 



