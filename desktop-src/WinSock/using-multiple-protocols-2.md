---
description: Une application utilise la fonction WSAEnumProtocols pour déterminer les protocoles de transport et les chaînes de protocole présents, et pour obtenir des informations sur chacune d’elles, contenues dans la \_ structure WSAPROTOCOL info associée.
ms.assetid: 4f38cb07-d824-4d43-abd8-89d58dc15810
title: Utilisation de plusieurs protocoles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ab9a37dcc90f1094126f701641539dd3f26a1a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112995"
---
# <a name="using-multiple-protocols"></a>Utilisation de plusieurs protocoles

Une application utilise la fonction [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) pour déterminer les protocoles de transport et les chaînes de protocole présents, et pour obtenir des informations sur chacune d’elles, contenues dans la structure [**WSAPROTOCOL \_ info**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) associée.

Dans la plupart des cas, il existe une seule structure d' [**\_ informations de WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) pour chaque protocole ou chaîne de protocole. Toutefois, certains protocoles présentent plusieurs comportements. Par exemple, le protocole SPX est orienté message (autrement dit, les limites des messages de l’expéditeur sont conservées par le réseau), mais le socket de réception peut ignorer ces limites de message et les traiter comme un flux d’octets. Par conséquent, il existe deux entrées différentes de structure **WSAPROTOCOL \_ info** pour SPX, une pour chaque comportement.

Dans Windows Sockets 2, plusieurs nouvelles valeurs de famille d’adresses, de type de socket et de protocole apparaissent. Windows Sockets 1,1 prenait en charge une seule famille d’adresses (AF \_ inet) pour IPv4 qui consistait en un petit nombre de types de socket et d’identificateurs de protocole bien connus. Windows Sockets 2 conserve la famille d’adresses, le type de socket et les identificateurs de protocole existants pour des raisons de compatibilité, mais il prend également en charge de nouvelles valeurs de famille d’adresses pour les nouveaux protocoles de transport avec de nouveaux types de médias.

Les nouveaux identificateurs uniques ne sont pas nécessairement bien connus, mais cela ne doit pas poser de problème. Les applications qui doivent être indépendantes des protocoles sont encouragées à sélectionner un protocole sur la base de son aptitude, et non sur les valeurs affectées à leur *\_ type de socket* ou à leurs paramètres de *protocole* . L’adéquation des protocoles est indiquée par les attributs de communication, tels que le flux de messages par rapport à l’octet, et les informations fiables et non fiables, qui sont contenues dans la structure des [**\_ informations**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) du protocole WSAPROTOCOL. La sélection de protocoles sur la base de l’aptitude au lieu des noms de protocole et des types de sockets bien connus permet aux applications indépendantes du protocole de tirer parti des nouveaux protocoles de transport et de leurs types de média associés, dès qu’ils sont disponibles.

La moitié du serveur d’une application client/serveur offre des avantages en établissant des sockets d’écoute sur tous les protocoles de transport appropriés. Ensuite, le client peut établir sa connexion à l’aide de n’importe quel protocole approprié. Par exemple, cela permet à une application cliente d’être inchangée, qu’elle soit exécutée sur un ordinateur de bureau connecté via un réseau local ou sur un ordinateur portable à l’aide d’un réseau sans fil.

 

 
