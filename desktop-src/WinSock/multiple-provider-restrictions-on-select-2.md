---
description: La fonction Select est utilisée pour déterminer l’état d’un ou plusieurs sockets dans un ensemble. Pour chaque socket, l’appelant peut demander des informations sur l’état de lecture, d’écriture ou d’erreur. Un ensemble de sockets est indiqué par une \_ structure FD Set.
ms.assetid: 40354d8f-1e8b-48aa-888a-81a421568f23
title: Plusieurs restrictions de fournisseur sur SELECT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2556d98aea60e6fa822f9e3df57cc142c33491d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113039"
---
# <a name="multiple-provider-restrictions-on-select"></a>Plusieurs restrictions de fournisseur sur SELECT

La fonction [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) est utilisée pour déterminer l’état d’un ou plusieurs sockets dans un ensemble. Pour chaque socket, l’appelant peut demander des informations sur l’état de lecture, d’écriture ou d’erreur. Un ensemble de sockets est indiqué par une structure [**FD \_ Set**](/windows/desktop/api/winsock/nf-winsock-fd_set) .

Windows Sockets 2 permet à une application d’utiliser plusieurs fournisseurs de services, mais la fonction [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) est limitée à un ensemble de sockets associés à un fournisseur de services unique. Cela ne permet pas d’empêcher une application de disposer de plusieurs sockets ouverts par le biais de plusieurs fournisseurs.

Il existe deux façons de déterminer l’état d’un ensemble de sockets qui s’étend sur plusieurs fournisseurs de services :

-   Utilisation des fonctions [**WSAWaitForMultipleEvents**](/windows/desktop/api/Winsock2/nf-winsock2-wsawaitformultipleevents) ou [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) lorsque la sémantique de blocage est utilisée.
-   Utilisation de la fonction [**WSAAsyncSelect**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect) lorsque des opérations de non-blocage sont utilisées et que l’application utilise déjà une pompe de messages Windows.

Quand une application doit utiliser la sémantique de blocage sur un ensemble de sockets qui s’étend sur plusieurs fournisseurs, [**WSAWaitForMultipleEvents**](/windows/desktop/api/Winsock2/nf-winsock2-wsawaitformultipleevents) est recommandé. L’application peut également utiliser la fonction [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) , qui permet aux \_ événements réseau FD xxx (voir [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect)) de s’associer à un objet d’événement et de les gérer à partir du paradigme de l’objet d’événement (décrit dans [e/s et objets d’événement avec chevauchement](overlapped-i-o-and-event-objects-2.md)).

La fonction [**WSAAsyncSelect**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect) n’est pas limitée à un fournisseur unique, car elle utilise un descripteur de socket unique comme paramètre d’entrée. Notez cependant que la fonction [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) offre de meilleures performances et une plus grande évolutivité par rapport à **WSAAsyncSelect** , car la surcharge liée à la gestion de la pompe de messages avec des messages d’événement Winsock augmente à mesure que le nombre total de sockets utilisés augmente.

 

 



