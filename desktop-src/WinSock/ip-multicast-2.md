---
description: La multidiffusion IP se trouve dans la catégorie du plan de données et du plan de contrôle qui ne sont pas associés à une racine.
ms.assetid: 474a1c7f-0ece-4192-a2d9-6e2f3df2ac02
title: Multidiffusion IP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bf9469822ae974b7c616b7904f9dc7120682acb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544658"
---
# <a name="ip-multicast"></a>Multidiffusion IP

La multidiffusion IP se trouve dans la catégorie du plan de données et du plan de contrôle qui ne sont pas associés à une racine. Toutes les applications jouent un rôle feuille. Actuellement, la plupart des implémentations de multidiffusion IP utilisent un ensemble d’options de socket proposées par Steve Deering à l’IETF (Internet Engineering Task Force). Cinq opérations sont donc rendues disponibles :

-   \_TTL de multidiffusion IP \_ : définit la portée de la durée de vie et contrôle l’étendue d’une session de multidiffusion.
-   Multidiffusion IP \_ \_ si : détermine l’interface à utiliser pour la multidiffusion.
-   IP \_ Add \_ MEMBERSHI : joint une session de multidiffusion spécifiée.
-   \_Adhésion IP Drop \_ : abandon d’une session de multidiffusion.
-   \_Boucle de multidiffusion IP \_ : contrôle le bouclage du trafic de multidiffusion.

La définition de la durée de vie d’un socket IP-multicast correspond directement à l’utilisation du \_ \_ Code de commande d’étendue de multidiffusion SIO pour [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl).

La méthode permettant de déterminer l’interface IP à utiliser pour la multidiffusion consiste à utiliser une option de socket spécifique à TCP/IP, comme décrit dans l’annexe Windows Sockets 2 Protocol-Specific. Les trois opérations restantes sont traitées correctement avec la sémantique Windows Sockets 2 décrite ici.

L’application ouvre les sockets avec des \_ indicateurs feuille p feuille/d \_ dans [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa). Elle utilise [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) pour s’ajouter à un groupe de multidiffusion sur l’interface par défaut désignée pour les opérations de multidiffusion. Si l’indicateur dans **WSAJoinLeaf** indique que ce socket n’est qu’un expéditeur, l’opération de jointure est essentiellement un non-op et aucun message IGMP n’a besoin d’être envoyé. Dans le cas contraire, un paquet IGMP est envoyé au routeur pour indiquer les intérêts de réception des paquets envoyés à l’adresse de multidiffusion spécifiée. Étant donné que l’application a créé des \_ sockets feuille c feuille/d spéciaux \_ , utilisés uniquement pour l’exécution de la multidiffusion, la fonction [**opération closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) standard serait utilisée pour sortir de la session de multidiffusion. Le \_ \_ Code de commande de bouclage multipoint SIO pour [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) fournit un mécanisme de contrôle générique permettant de déterminer si les données envoyées sur un \_ Socket de feuille d dans un schéma multipoint sans racine peuvent également être reçues sur le même socket.

> [!Note]  
> La version Winsock de l' \_ option de boucle de multidiffusion IP \_ est sémantiquement différente de la version UNIX de l' \_ option de boucle de multidiffusion IP \_ :

 

-   Dans Winsock, l' \_ option de boucle de multidiffusion IP \_ s’applique uniquement au chemin de réception.
-   Dans la version UNIX, l' \_ option de boucle de multidiffusion IP \_ s’applique au chemin d’envoi.

Par exemple, les applications ACTIVÉes et désactivées (plus faciles à suivre que X et Y) rejoignent le même groupe sur la même interface ; application sur définit l' \_ \_ option de boucle de multidiffusion IP activée, la désactivation de l’application définit l' \_ option de boucle de multidiffusion IP \_ désactivée. Si ON et OFF sont des applications Winsock, OFF peut envoyer à ON, mais ON ne peut pas l’envoyer à OFF. En revanche, si ON et OFF sont des applications UNIX, ON peut envoyer à OFF, mais OFF ne peut pas envoyer à ON.

 

 



