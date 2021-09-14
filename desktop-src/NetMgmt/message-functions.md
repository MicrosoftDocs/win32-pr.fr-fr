---
title: Fonctions de message (gestion de réseau)
description: Les fonctions de message de gestion de réseau envoient des messages et gèrent les alias de message. Les fonctions de message sont répertoriées ci-après.
ms.assetid: 9face737-3472-4a53-97b6-e861a60ee96a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3629a281637fe4ecd0c937ce0c7504beac8e11d2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127009397"
---
# <a name="message-functions-network-management"></a>Fonctions de message (gestion de réseau)

\[les fonctions de message ne sont pas prises en charge à partir de Windows Vista, car les services alertes et messenger ne sont pas pris en charge.\]

Les fonctions de message de gestion de réseau envoient des messages et gèrent les alias de message. Les fonctions de message sont répertoriées ci-après.

**Windows Server 2003 :** Les services alertes et Messenger sont désactivés par défaut. Vous devez réactiver les services avant d’appeler les fonctions d' [alerte](alert-functions.md) de gestion de réseau ou les fonctions de message de gestion de réseau.



| Fonction                                               | Description                                                                     |
|--------------------------------------------------------|---------------------------------------------------------------------------------|
| [**NetMessageBufferSend**](/windows/desktop/api/Lmmsg/nf-lmmsg-netmessagebuffersend)   | Envoie un message à un alias de message enregistré.                                  |
| [**NetMessageNameAdd**](/windows/desktop/api/Lmmsg/nf-lmmsg-netmessagenameadd)         | Inscrit un alias de message dans la table de noms de message.                            |
| [**NetMessageNameDel**](/windows/desktop/api/Lmmsg/nf-lmmsg-netmessagenamedel)         | Supprime un alias de message de la table de noms de messages.                            |
| [**NetMessageNameEnum**](/windows/desktop/api/Lmmsg/nf-lmmsg-netmessagenameenum)       | Répertorie tous les alias de messages stockés dans la table des noms de message.                 |
| [**NetMessageNameGetInfo**](/windows/desktop/api/Lmmsg/nf-lmmsg-netmessagenamegetinfo) | Retourne des informations sur un alias de message particulier dans la table des noms de messages. |



 

Un *message* est une mémoire tampon de données texte envoyée à un utilisateur ou une application sur le réseau. Pour recevoir un message, un utilisateur ou une application doit inscrire un alias de message dans la table de noms des messages d’un ordinateur. Les alias suivants sont inscrits par défaut : « User », « machine », « Domain » ou « \* » (le domaine actuel de l’ordinateur). L’alias « Domain » spécifie l’ensemble des ordinateurs qui ont le même nom de domaine défini comme domaine ou comme groupe de travail et qui écoutent les diffusions sur le même sous-réseau. Pour NetBIOS sur TCP/IP, la spécification de l’alias « Domain » peut également aboutir sur des sous-réseaux si le nom de domaine est résolu par un serveur de noms, ou si les diffusions de datagramme NetBIOS sont transférées entre les routeurs. Par conséquent, les messages envoyés à un domaine n’ont pas la garantie de remise à tous les membres du domaine. Il est également possible que certains membres du domaine reçoivent le message plusieurs fois s’ils ont plusieurs transports installés qui prennent en charge NetBIOS.

Vous pouvez également inscrire un alias de message en appelant la fonction [**NetMessageNameAdd**](/windows/desktop/api/Lmmsg/nf-lmmsg-netmessagenameadd) . Une *table de noms de message* contient une liste d’alias de message inscrits (utilisateurs et applications) autorisés à recevoir des messages. Les alias enregistrés dans la table de noms de message ne respectent pas la casse.

Le service Messenger doit être en cours d’exécution sur l’ordinateur récepteur pour afficher un message contextuel lorsque le message est reçu. En outre, le service station de travail doit être en cours d’exécution sur l’ordinateur local. NetBIOS est le mécanisme de transport utilisé entre l’expéditeur et le destinataire.

Les fonctions de message sont disponibles à deux niveaux d’informations :

-   [**\_Infos MSG \_ 0**](/windows/desktop/api/Lmmsg/ns-lmmsg-msg_info_0)
-   [**\_Infos MSG \_ 1**](/windows/desktop/api/Lmmsg/ns-lmmsg-msg_info_1)

Le niveau d’information **MSG \_ info \_ 1** existe uniquement pour la compatibilité. Le service Messenger ne transfère pas les noms ou n’autorise pas le transfert des noms.

 

 




