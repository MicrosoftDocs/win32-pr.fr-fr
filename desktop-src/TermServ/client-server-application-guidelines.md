---
title: Instructions pour les applications client/serveur
description: Les applications client/serveur ne doivent pas supposer qu’une seule connexion d’ordinateur équivaut à une seule session utilisateur.
ms.assetid: 69822ef1-eca8-4302-b014-8e5894d52109
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd0c1a71256f3ab469bfeb1c08b2d096b56ac1b5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106512734"
---
# <a name="clientserver-application-guidelines"></a>Instructions pour les applications client/serveur

Les applications client/serveur ne doivent pas supposer qu’une seule connexion d’ordinateur équivaut à une seule session utilisateur. Il s’agit d’un cas particulier du problème abordé dans [adresses IP et noms d’ordinateurs](ip-addresses-and-computer-names.md).

Pour identifier de façon unique une connexion client/serveur, chaque module client doit utiliser un nom ou un identificateur unique. Les applications peuvent utiliser des objets nommés, des canaux, des sockets ou d’autres méthodes IPC. Pour plus d’informations, consultez [espaces de noms d’objets noyau](kernel-object-namespaces.md).

Pour être Services Bureau à distance compatible, le module serveur dans une application client/serveur doit être en mesure de gérer plusieurs clients se connectant à partir du même ordinateur. Pour ce faire, le module serveur doit accepter les connexions client via une interface globale bien définie, telle que RPC ou canaux nommés. Le serveur et le client doivent négocier un canal de communication différent pour chaque session utilisateur. Le client doit établir une connexion au serveur à l’aide de protocoles qui prennent facilement en charge ce type d’opération, tel que TCP/IP, où une connexion de socket différente peut être utilisée pour chaque application cliente.

Le module client peut appeler la fonction [**ProcessIdToSessionId**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-processidtosessionid) pour récupérer l’identificateur de sa session services Bureau à distance. Le client utilise ensuite une forme de communication interprocessus pour passer son identificateur de session au module serveur. Les modules client et serveur peuvent ensuite utiliser l’identificateur de session pour configurer un canal de communication privé. Par exemple, le module de serveur peut utiliser un identificateur de session pour accéder aux objets dans l’espace de noms de la session pour les objets de noyau.

En outre, le module de serveur peut utiliser l’identificateur de session dans un appel [**WTSQuerySessionInformation**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsquerysessioninformationa) pour récupérer des informations supplémentaires sur le client. Le module de serveur peut également utiliser l’identificateur de session dans un appel [**WTSSendMessage**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtssendmessagea) pour afficher un message sur le terminal client. Le module de serveur peut également créer deux événements pour surveiller la connexion au client et la déconnexion d’une session. Toutefois, il doit être inscrit sur le serveur de l’hôte de session Bureau à distance (hôte de session Bureau à distance) pour effectuer cette opération. Pour plus d’informations, consultez [surveillance des connexions de session et des déconnexions](monitoring-session-connections-and-disconnections.md).

Les invites de saisie utilisateur constituent une source potentielle de problèmes pour les applications client/serveur. Par exemple, si un service appelle la fonction [**MessageBox**](/windows/desktop/api/winuser/nf-winuser-messagebox) , la boîte de message s’affiche sur le Bureau du serveur hôte de session Bureau à distance, et non sur le Bureau du client. Pour afficher un message sur un bureau client, le service peut appeler la fonction [**WtsSendMessage**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtssendmessagea) . Le service peut également demander une entrée à partir du module client et le module client peut afficher l’interface utilisateur et renvoyer l’entrée résultante au service.

Les processus générés à partir de plusieurs sessions peuvent envoyer et recevoir des données à l’aide de blocs de mémoire partagée. Pour plus d’informations, consultez Création d’une [mémoire partagée nommée](/windows/desktop/Memory/creating-named-shared-memory). La mémoire partagée ne peut pas être utilisée dans les conditions suivantes :

-   Les processus qui utilisent le bloc de mémoire partagée ont été générés par plusieurs sessions.
-   Les sessions partagent les mêmes informations d’identification d’authentification utilisateur.

 

 